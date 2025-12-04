<template>
  <header class="app-header">
    <h1 class="title">吟霖电子设定集</h1>
    <!-- 在线人数展示 -->
    <div class="online-count" v-if="onlineCount !== null">
      当前在线：<span class="count">{{ onlineCount }}人</span>
    </div>
    <!-- 移动端汉堡按钮 -->
    <button
      class="hamburger"
      @click="toggleMobileNav"
      aria-label="Toggle navigation"
    >
      <span :class="{ open: mobileNavOpen }"></span>
      <span :class="{ open: mobileNavOpen }"></span>
      <span :class="{ open: mobileNavOpen }"></span>
    </button>

    <!-- 普通导航 & 移动端下拉导航 -->
    <nav :class="['nav-links', { 'mobile-open': mobileNavOpen }]">
      <RouterLink
        v-for="item in navItems"
        :key="item.name"
        :to="item.path"
        class="nav-item"
        active-class="active-link"
        @click="mobileNavOpen = false"
      >
        {{ item.name }}
      </RouterLink>

      <a
        href="http://36.150.237.25/#/redirector"
        target="_blank"
        rel="noopener"
        class="nav-item"
        active-class="active-link"
        @click="mobileNavOpen = false"
      >
        霜落映界
      </a>
    </nav>
  </header>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from "vue";
import { io } from "socket.io-client";

const navItems = [
  { name: "暗巷独行", path: "/" },
  { name: "悬丝纪事", path: "/timeLine" },
  { name: "罚印回响", path: "/message" },
  { name: "银丝捕影", path: "/gallery" },
  { name: "傀儡工坊", path: "/resources" },
  { name: "港藏低语", path: "/talk" },
  { name: "丝线密语", path: "/voice" },
  { name: "哀鸣协奏", path: "/music" },
  { name: "巡尉案卷", path: "/wiki" },
  { name: "此致", path: "/thanks" },
];

const mobileNavOpen = ref(false);
function toggleMobileNav() {
  mobileNavOpen.value = !mobileNavOpen.value;
}

const siteId = "yinlin";

const onlineCount = ref<number | null>(null);

// 连接时带上 query.siteId
const socket: any = io("http://36.150.237.25:3000", {
  query: { siteId },
});

onMounted(() => {
  socket.on("onlineCount", (count: number) => {
    onlineCount.value = count;
  });
});

onBeforeUnmount(() => {
  socket.disconnect();
});
</script>

<style scoped lang="scss">
/* 吟霖 — 赤电收网：深夜墨黑 / 猩红 / 导电紫 + 电弧残影 */
.app-header {
  --deep-bg: linear-gradient(
    180deg,
    #050406 0%,
    #0a0a0c 100%
  ); /* 夜幕底色（近黑） */
  --core-glow: rgba(200, 80, 80, 0.06); /* 猩红内辉 */
  --accent: #d93a3a; /* 主色：猩红（发色/热感） */
  --accent-2: #b36bff; /* 次色：导电紫（电弧） */
  --metallic: #cfcfd6; /* 金属银光点缀 */
  --muted-text: #fff6f6; /* 文字：偏暖白 */
  --arc-haze: rgba(180, 120, 230, 0.04); /* 电弧薄雾 */
  --shadow-core: rgba(6, 6, 8, 0.7);

  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  height: 64px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 40px;
  background: radial-gradient(
      420px 100px at 86% 18%,
      rgba(180, 60, 60, 0.03),
      transparent 12%
    ),
    var(--deep-bg);
  backdrop-filter: blur(6px) saturate(1);
  box-shadow: 0 10px 36px var(--shadow-core), 0 0 18px var(--core-glow) inset;
  border-bottom: 1px solid rgba(220, 80, 80, 0.04);
  animation: fadeInDown 0.45s ease-out both;
  overflow: visible;

  &::after {
    /* 电弧薄雾 + 链条暗影残影（模拟傀儡感） */
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    height: 100%;
    pointer-events: none;
    background: linear-gradient(180deg, var(--arc-haze), transparent 26%),
      repeating-linear-gradient(
        90deg,
        rgba(255, 255, 255, 0.01) 0 2px,
        transparent 2px 8px
      ); /* 细小频闪 */
    mix-blend-mode: screen;
    opacity: 0.95;
  }

  /* 右侧导电电弧与链条剪影 */
  &::before {
    content: "";
    position: absolute;
    right: 6%;
    top: 6%;
    width: 320px;
    height: 96px;
    pointer-events: none;
    background: radial-gradient(
        44px 14px at 14% 22%,
        rgba(180, 120, 230, 0.12),
        transparent 30%
      ),
      radial-gradient(
        88px 28px at 50% 40%,
        rgba(217, 58, 58, 0.06),
        transparent 46%
      ),
      linear-gradient(90deg, rgba(120, 30, 30, 0.06), rgba(0, 0, 0, 0) 40%),
      /* 简易链条条纹感（表现傀儡/拘束） */
        repeating-linear-gradient(
          -30deg,
          rgba(0, 0, 0, 0.06) 0px 4px,
          rgba(0, 0, 0, 0) 4px 10px
        );
    filter: blur(6px) contrast(1.02);
    transform: translateY(0) rotate(-3deg);
    animation: arc-drift 7.6s ease-in-out infinite;
    mix-blend-mode: screen;
  }

  .title {
    position: relative;
    font-family: "Cinzel", "Noto Serif SC", serif;
    font-style: normal;
    font-size: 26px;
    font-weight: 800;
    color: var(--muted-text);
    background: linear-gradient(90deg, var(--accent), var(--accent-2));
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    letter-spacing: 0.6px;
    text-shadow: 0 6px 18px rgba(4, 4, 6, 0.6);
    transition: transform 0.26s ease, text-shadow 0.26s ease;
    animation: surge-pulse 6.8s ease-in-out infinite;

    &:hover {
      transform: translateY(-2px) scale(1.03);
      text-shadow: 0 12px 34px rgba(180, 90, 140, 0.08);
    }
  }

  .online-count {
    position: relative;
    margin-left: 16px;
    padding: 6px 14px;
    font-family: "Noto Sans SC", "PingFang SC", sans-serif;
    font-size: 1rem;
    color: var(--muted-text);
    background: linear-gradient(
      135deg,
      rgba(8, 8, 10, 0.28),
      rgba(6, 6, 8, 0.18)
    );
    border: 1px solid rgba(180, 80, 80, 0.035);
    border-radius: 24px;
    backdrop-filter: blur(6px);
    box-shadow: 0 6px 18px rgba(6, 6, 8, 0.5),
      0 0 12px rgba(180, 80, 80, 0.04) inset;
    overflow: hidden;
    cursor: default;
    transition: transform 0.22s ease, box-shadow 0.22s ease;

    &:hover {
      transform: translateY(-2px);
      box-shadow: 0 14px 36px rgba(6, 6, 8, 0.6),
        0 0 44px rgba(179, 110, 240, 0.06);
    }

    .count {
      display: inline-block;
      margin-left: 18px;
      font-weight: 800;
      color: var(--accent-2);
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 0 10px rgba(160, 120, 230, 0.05);
    }
  }

  .nav-links {
    display: flex;
    gap: 22px;
    align-items: center;

    .nav-item {
      position: relative;
      color: var(--muted-text);
      font-weight: 600;
      text-decoration: none;
      transition: color 0.22s ease, transform 0.16s ease;
      padding: 6px 4px;
      border-radius: 6px;
      overflow: visible;
      font-family: "STKaiti", "KaiTi", "Noto Serif SC", serif;
      font-style: italic;

      &::after {
        content: "";
        position: absolute;
        left: 50%;
        bottom: -8px;
        width: 0;
        height: 6px;
        border-radius: 6px;
        background: linear-gradient(
          90deg,
          rgba(0, 0, 0, 0),
          rgba(217, 58, 58, 0.9),
          rgba(179, 107, 255, 0.88),
          rgba(0, 0, 0, 0)
        );
        transform: translateX(-50%);
        opacity: 0.95;
        filter: blur(0.9px) contrast(1.03);
        transition: width 0.36s cubic-bezier(0.2, 0.9, 0.2, 1), left 0.36s,
          opacity 0.24s;
        background-size: 200% 100%;
        animation: electric-wave 4.8s linear infinite;
      }

      &::before {
        content: "";
        position: absolute;
        right: 14%;
        top: -6px;
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background: radial-gradient(circle, var(--metallic), transparent 60%);
        opacity: 0;
        transform: translateY(-6px) scale(0.86);
        transition: opacity 0.26s, transform 0.36s;
        box-shadow: 0 6px 14px rgba(120, 40, 40, 0.06);
      }

      &:hover {
        color: var(--accent-2);
        transform: translateY(-1.8px);
        text-shadow: 0 0 8px rgba(140, 80, 150, 0.02);
      }

      &:hover::after {
        width: 72%;
        left: 50%;
        opacity: 1;
      }

      &:hover::before {
        opacity: 1;
        transform: translateY(0) scale(1);
      }
    }

    .active-link {
      color: var(--accent);
      font-weight: 700;

      &::before {
        content: "⚡";
        position: absolute;
        right: 0px;
        top: 50%;
        transform: translateY(-50%) rotate(-6deg);
        font-size: 12px;
        color: var(--metallic);
        text-shadow: 0 2px 10px rgba(180, 100, 220, 0.06);
        animation: bolt-emblem 2.8s ease-in-out infinite;
        opacity: 0.98;
      }

      &::after {
        width: 92%;
        opacity: 1;
        box-shadow: 0 6px 22px rgba(120, 40, 40, 0.06);
      }
    }
  }

  .hamburger {
    display: none;
    flex-direction: column;
    justify-content: space-around;
    width: 28px;
    height: 24px;
    background: none;
    border: none;
    cursor: pointer;
    padding: 0;

    span {
      display: block;
      width: 100%;
      height: 3px;
      background: rgba(255, 240, 240, 0.94);
      border-radius: 2px;
      transition: transform 0.28s ease, opacity 0.28s ease, background 0.28s;
      box-shadow: 0 2px 6px rgba(6, 6, 6, 0.18), 0 0 8px rgba(180, 80, 80, 0.06);
    }

    span.open:nth-child(1) {
      transform: translateY(10px) rotate(45deg);
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
    }

    span.open:nth-child(2) {
      opacity: 0;
    }

    span.open:nth-child(3) {
      transform: translateY(-10px) rotate(-45deg);
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
    }
  }

  @media (max-width: 768px) {
    padding: 0 20px;

    .title {
      display: none;
    }
    .hamburger {
      display: flex;
    }

    .nav-links {
      position: absolute;
      top: 64px;
      left: 0;
      right: 0;
      flex-direction: column;
      background: linear-gradient(
        180deg,
        rgba(8, 8, 10, 0.98),
        rgba(6, 6, 8, 0.995)
      );
      backdrop-filter: blur(12px);
      gap: 0;
      overflow: hidden;
      max-height: 0;
      transition: max-height 0.34s ease;
      border-top: 1px solid rgba(180, 80, 80, 0.03);

      &.mobile-open {
        max-height: 520px;
      }

      .nav-item {
        padding: 14px 20px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
      }
    }
  }
}

/* 动效关键帧（电弧 / 残影 / 链条抖动） */
@keyframes electric-wave {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

@keyframes surge-pulse {
  0% {
    transform: translateY(0);
  }
  45% {
    transform: translateY(-2px) scale(1.01);
    filter: drop-shadow(0 6px 18px rgba(180, 80, 140, 0.04));
  }
  100% {
    transform: translateY(0);
  }
}

@keyframes fadeInDown {
  0% {
    opacity: 0;
    transform: translateY(-8px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes arc-drift {
  0% {
    transform: translateY(0) rotate(-3deg) translateX(0);
    opacity: 0.9;
    filter: blur(6px);
  }
  50% {
    transform: translateY(-6px) rotate(2deg) translateX(-6px);
    opacity: 1;
    filter: blur(4px) saturate(1.02);
  }
  100% {
    transform: translateY(0) rotate(-3deg) translateX(0);
    opacity: 0.9;
  }
}

@keyframes spark-glint {
  0% {
    transform: translateY(0) rotate(0deg);
    opacity: 0.6;
  }
  50% {
    transform: translateY(-4px) rotate(0.4deg);
    opacity: 1;
    filter: drop-shadow(0 6px 18px rgba(180, 120, 230, 0.06));
  }
  100% {
    transform: translateY(0) rotate(0deg);
    opacity: 0.6;
  }
}

@keyframes bolt-emblem {
  0% {
    transform: translateY(-6%) rotate(-6deg);
    opacity: 0.8;
    filter: drop-shadow(0 2px 8px rgba(180, 100, 220, 0.04));
  }
  50% {
    transform: translateY(6%) rotate(2deg);
    opacity: 1;
    filter: drop-shadow(0 6px 18px rgba(200, 120, 235, 0.08));
  }
  100% {
    transform: translateY(-6%) rotate(-6deg);
    opacity: 0.8;
  }
}
</style>
