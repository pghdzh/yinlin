<template>
  <div class="megumi-page" aria-live="polite">
    <main class="container" ref="mainContainer">
      <!-- HERO 区域 -->
      <header class="hero" role="banner">
        <div class="left-col">
          <button class="avatar-card">
            <picture class="avatar-wrap">
              <img
                src="@/assets/images1/yinlin-slty (33).webp"
                class="avatar"
                loading="lazy"
                decoding="async"
              />
            </picture>
            <div class="avatar-meta">
              <span class="avatar-badge">共鸣能力：诛恶傀儡</span>
            </div>
          </button>
        </div>
        <div class="right-col" ref="metaCard">
          <div class="hero-panel">
            <h1 class="name">
              吟霖
              <!-- <span class="jp">（女特务）</span> -->
            </h1>
            <p class="subtitle">
              阳光之下的交给你们，阴暗处的老鼠，自有藏在暗处的猫去解决
            </p>
            <p class="lead">
              吟霖是天生的共鸣者，也曾是治安署的优秀巡尉。但现在却因为一起案件被消去了巡尉身份，只能在暗处独自调查着潜藏的罪恶。
            </p>
          </div>
        </div>
      </header>

      <!-- 内容卡片区 -->
      <section id="personality" class="card personality">
        <div class="card-head">
          <h2>核心机制</h2>
        </div>
        <ul class="traits">
          <li>
            【审判值】：血量上方上限为100的能量条。能量条满后，重击释放【千面魅影】，命中【缚罪标记】的目标时，将【缚罪标记】替换为【惩罚印记】。（【千面魅影】释放后摇被打断不会丢失效果）
          </li>
          <li>
            【缚罪标记】：常态攻击，R【破天雷灭击】以及变奏技能命中敌人时，附加【缚罪标记】。吟霖离场时，【缚罪标记】消失。
          </li>
          <li>
            【惩罚印记】：任意角色攻击携带【惩罚印记】的目标时，吟霖会对所有携带【惩罚印记】的目标进行协同攻击，持续18秒，每秒最多触发一次。吟霖离场，【惩罚印记】不会消失。
          </li>
          <li>
            【审判值】获取方式：平A、闪避反击、共鸣技能【磁殛咆哮】(下称“E”)获得【审判值】。其中E为吟霖协奏能量和【审判值】的主要来源，E持续的10秒中，每次攻击都会同时协同攻击所有携带【缚罪标记】的敌人，每个敌人会提供5点【审判值】，最多提供4次。
          </li>
          <li style="font-weight: bold">输出流程：</li>
          <li>基础流程：Q-E-R-AA-Z</li>
          <li>
            技能缩写：普攻 = A，重击 = Z，共鸣技能 = E，共鸣解放 = R，声骸 = Q
          </li>
        </ul>
      </section>

      <section id="resonance-status" class="card overview">
        <div class="card-head">
          <h2>共鸣状况</h2>
        </div>
        <div class="two-col">
          <div class="text-block">
            <p>
              对象声痕处于左大腿外侧，共鸣后外表体征未产生显著变化，皮肤表层有微弱电流通过，未见其对身体有负面影响。<br />
              对象可将电流收束为细丝的形态存在，能极为熟练地操控异能。<br />
              共鸣频谱检验图与已知导电频率波动区间接近，测试有较强的谐振反应。<br />
              受试样本拉贝尔曲线波动规律、具有显著周期性特征，检测结果判断为先天型共鸣者。<br />
              另外，对象曾有心律失常的病史记录，尚不明确其与共鸣能力之间的相关性。若异能力被阻隔，有诱发心房颤动的风险，需谨慎留心。
            </p>
          </div>
        </div>
      </section>

      <!-- 新增三大主题区域 -->
      <section id="food" class="card special-section">
        <div class="card-head">
          <h2>机械人偶“悬丝”</h2>
        </div>
        <div class="content two-col">
          <div class="img-area">
            <img src="./img/item1.png" loading="lazy" decoding="async" />
          </div>
          <div class="text-block">
            <p>
              最开始它不过是随处都可以买到的机关人偶，是寻常人偶制作师的练手之作，但被吟霖改造成适合她发挥共鸣能力的战斗用形态。虽然经过长久的战斗已经很陈旧了，但是从细微处也可以看出来吟霖对它的喜爱——虽然她并不会开口承认。
            </p>
          </div>
        </div>
      </section>
      <section id="shattered-crystal" class="card special-section">
        <div class="card-head">
          <h2>旗袍图鉴</h2>
        </div>
        <div class="content two-col">
          <div class="img-area">
            <img src="./img/item2.png" loading="lazy" decoding="async" />
          </div>
          <div class="text-block">
            <p>
              表面是吟霖钟爱的服装图鉴，实际是与联络员交流的动态密码本。上面的内容定期更换，用加密过的图像和符号进行沟通，即便是资深的联络员，使用起来也会感觉到吃力。
            </p>
            <p>
              吟霖钟爱旗袍，可以隐藏众多装备和武器，并且意外地方便活动，更重要的是……它足够引人瞩目。
            </p>
          </div>
        </div>
      </section>

      <section id="cyclic-clock" class="card special-section">
        <div class="card-head">
          <h2>放大镜</h2>
        </div>
        <div class="content two-col">
          <div class="img-area">
            <img src="./img/item3.png" loading="lazy" decoding="async" />
          </div>
          <div class="text-block">
            <p>
              调查专用放大镜，治安署派发给所有正式成为巡尉的新人。借着它可发现肉眼难以察觉的蛛丝马迹，被设计得非常小巧。
            </p>

            <p>
              吟霖作为潜入调查员，使用这个工具的机会并不多。因此放大镜对她而言是信物，是为了纪念父母和提醒自己，不要忘记自己真正的身份。
            </p>
          </div>
        </div>
      </section>

      <section id="collective-album" class="card special-section">
        <div class="card-head">
          <h2>灿金炒饭</h2>
        </div>
        <div class="content two-col">
          <div class="img-area">
            <img src="./img/food.png" loading="lazy" decoding="async" />
          </div>
          <div class="text-block">
            <p>
              一碗蛋炒饭，往往是学习烹饪的人最先学会的简单菜色，但是能够将简单的炒饭做到极致，每颗米粒都宛若真正的黄金，只有对食物非常挑剔的人才能做到。吟霖因为任务的需要，经常会接触那些非富则贵的人们，自己的味蕾也变得极其挑剔。而这道灿金炒饭就是其中她最中意的菜色，廉价的食材，无价的技艺，也正是她所追求的。
            </p>
          </div>
        </div>
      </section>

      <section
        id="timeline"
        class="card timeline"
        aria-labelledby="timeline-heading"
      >
        <div class="card-head">
          <h2 id="timeline-heading">共鸣链详解</h2>
        </div>
        <div class="tl-wrap" role="list">
          <div class="vl" aria-hidden="true"></div>
          <ol class="tl-list">
            <li
              v-for="(ev, i) in timeline"
              :key="i"
              class="tl-item"
              role="listitem"
              tabindex="0"
              :aria-label="``"
            >
              <div class="tl-card">
                <h3 class="tl-title">第 {{ i + 1 }} 链 · {{ ev.title }}</h3>
                <p class="tl-desc">{{ ev.desc }}</p>
              </div>
            </li>
          </ol>
        </div>
      </section>

      <section class="ll-stories" ref="storyRef">
        <div class="card" role="region" aria-labelledby="stories-title">
          <header class="card-head">
            <h2 id="stories-title" class="card-title">吟霖纪事</h2>
          </header>

          <main class="card-body">
            <transition name="fade-slide" mode="out-in">
              <article
                :key="items[current].id"
                :id="`panel-${items[current].id}`"
                class="story"
                role="tabpanel"
                :aria-labelledby="`tab-${items[current].id}`"
              >
                <h3 class="story-head">{{ items[current].title }}</h3>
                <div
                  class="story-content"
                  v-html="items[current].content"
                ></div>
              </article>
            </transition>
          </main>

          <footer class="card-foot">
            <button class="nav-btn" @click="prev" aria-label="上一则故事">
              ‹
            </button>
            <div class="pager">{{ current + 1 }} / {{ items.length }}</div>
            <button class="nav-btn" @click="next" aria-label="下一则故事">
              ›
            </button>
          </footer>
        </div>
      </section>
    </main>
    <!-- <div class="floating-chibis">
      <img
        v-for="(pet, i) in chibiList"
        :key="i"
        :src="pet.src"
        :style="{ top: pet.top + 'px', left: pet.left + 'px' }"
        class="chibi-img"
      />
    </div> -->
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, nextTick } from "vue";
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

const timeline = ref([
  {
    title: "矛盾的抉择",
    desc: ` 共鸣技能磁殛咆哮和召雷磁爆伤害提升70%。
吟霖暴击提升20%。`,
  },
  {
    title: "牵绊的俘虏",
    desc: `共鸣技能磁殛爆发命中时额外恢复5点【审判值】和5点共鸣能量。`,
  },
  {
    title: "无情的断罪",
    desc: `共鸣回路审判之雷伤害倍率提升55%。`,
  },
  {
    title: "前行的鼓舞",
    desc: `使用共鸣回路·审判之雷后，队伍中的角色攻击提升20%，持续12秒。`,
  },
  {
    title: "决意的回响",
    desc: `共鸣解放·破天雷灭击命中带有【缚罪标记】、【惩罚印记】的目标时，伤害提升100%。`,
  },
  {
    title: "正义的践行",
    desc: `施放共鸣解放破天雷灭击后的30秒内，吟霖的普攻命中目标时额外触发疾霆昭彰，造成吟霖攻击力419.59%的导电伤害，每段普攻可触发1次，最多触发4次，此次伤害为共鸣技能伤害。`,
  },
]);

const reducedMotion =
  window.matchMedia &&
  window.matchMedia("(prefers-reduced-motion: reduce)").matches;

const items = [
  {
    id: "1",
    title: "阴影中的鲜红",
    content: `今州居民没有人不认识穿着整齐制服穿梭于街道上，为人们排忧解难的巡尉。

他们维持着今州的治安，保障着今州居民的生命和财产安全。

但也有一些特殊的巡尉，他们没有机会穿着制服，也并不允许轻易表露自己的身份。

他们被称为潜入调查员，他们隐藏身份尽可能潜入到犯罪组织中，取得犯罪证据或者制止犯罪行为。

比起小偷小摸，他们往往需要面对的是更加穷凶极恶的歹徒，暴露往往就意味着任务失败，丢掉性命。

……

“就算是那些白痴巡尉，也不会有这么蠢得去当潜入调查员这样的人啊，你们说是吧？”

一个粗鲁的流放者首领将手中的匕首刺入眼前的破桌上，阴暗的破仓库里传来了一阵阵放肆的笑声。

“我们这里不会有巡尉的人吧？如果有的话记得现在就说，庆功宴我可以少订一位了。”

其他人再次发出了哄笑，但难免还是不经意地互相多看了几眼。

“今天晚上我知道会有一队车队从今州出发，上面有不少‘大货’，因为那个老板信了我们放出的谣言，没有雇用呜呜物流。”

首领拍了拍旁边一个身材瘦高长相猥琐的同伴。

“蛇仔明，还得是你啊，干得好！”

“嘿嘿……没什么，但是就算没有呜呜物流的专业物流员，那个车队还是请了一帮共鸣者当保镖的。”

“这个不用担心，喂，到时候就轮到你出场了，新人。”

首领看向了一个角落，一个有着亮丽红色长发的女子从阴影处走出，脸上带着若有若无的浅笑。

“首领……其实我早就想说，这个家伙看起来连我都打不过，真的和你说的一样能打吗？别等会把兄弟们都折进去了……”

蛇仔明露出了不怀好意的笑容，伸手想要抓住女子的手臂，但在快要触碰到她如白雪一般的肌肤之前，便硬生生停住了。

“这……这是怎么回事……你这混蛋女人对我干了什么！？”

首领摆了摆手，没好气地叹了口气——只有他注意到了蛇仔明身上被缠绕上了由雷电构成的细丝。

“新人，看在我的面上放了蛇仔明吧，他就只剩下嘴上厉害而已，今天行动之前就放过他好了。”

女子沉默着拨了拨发梢，蛇仔明身上缠绕着的细线便消失不见。

“好了，差不多该出发了……我们走，干他一票大的！”

…………

……

全身麻痹倒在地上的蛇仔明，看着原本应该成为他们目标的车队在远处缓缓驶过，不知道为什么想起了几个小时之前的事情。

（身上的麻痹感觉和那时候一模一样……是那个女人！她是内鬼！！！）

他挣扎着想要爬起来呼喊，但是却在勉强转头的时候看到一副可怖的人偶面庞，发出了凄厉的惨叫。

“啊啊啊啊……！！！“

但蛇仔明的惨叫没有持续多久，便淹没在了刹那闪现的雷光之中。`,
  },
  {
    id: "2",
    title: "人偶演出",
    content: `在今州城的闹市之中，一个带着连帽斗篷的高大男人牵着一个小男孩在偏僻的窄巷中穿行，无论谁看到都会认为是一对趁着假日出来游玩的父子吧——除非有人能够注意到小男孩脸上隐藏起来的畏惧表情。

“是的，他那个宝贝孙子已经在我们手上了……只要送出了今州城，那就别想有人能找到了。”

男人在通讯的过程中盯着手边的小男孩，示意他别想着乱动。

“只要有这小子在，别说他爷爷，就算是今州那帮巡尉都得忌惮我们几分吧……我出城之后再联系吧。”

城门已经近在咫尺，周围的警备都没有加强，很明显这小子的爷爷并没有将自己孙子被绑架的事情报告给巡尉——这是自然，毕竟他自己身上也不干净。

本来想快步穿过小巷，但却出现了一点无伤大雅的意外让他不得不停下了脚步。

一个衣着艳丽，有着长长红发的女子在小巷中表演着人偶戏，吸引了大批的小孩子和他们的父母围观，翻飞的木偶栩栩如生，引得所有小孩子都目不转睛地盯着不放，就连男人牵着的小男孩也一样。

因为专注看人偶戏的小孩子实在太多，如果强行挤过去的话，估计会太引人注目了，而且看样子人偶戏应该快要结束了，也不急于一时。

果然，一幕人偶戏很快就结束了，在满场掌声中，红发女子优雅地和手中的人偶一起鞠躬致谢。

就是现在，趁着结束的这个空挡，就能很轻易地穿过人群了，男子盯了一眼小男孩，示意他跟着自己快步离开。

“那么下一幕人偶戏，我想邀请一个小朋友一起来和我表演，那么谁有兴趣呢~？”

就在此时，红发的人偶师露出灿烂的笑容询问着台下的小孩子，几乎所有小孩子都踊跃地高高举起了手。

“好~那么就远处那个小男孩吧，对，牵着爸爸的那位！”

众人的目光聚焦到了人偶师所伸出手的方向，正是那个被连帽斗篷男子牵着的小男孩。

“我……？我吗？”

小男孩既惊喜又恐惧地看向了斗篷男子，男子也没想到居然会被点出来，思考再三之后还是牵着小男孩的手将他带到了人偶师的前面。

“不好意思……我们赶时间……”

“没关系，很快就能完事了……这位爸爸也要一起来吗？”

“我……？我就不用了……喂！”男子下意识地拒绝了，却没注意到小男孩已经迫不及待地挣脱了自己的手。

他刚想伸手拉住小男孩，却没想到触碰到的是那个奇奇怪怪的人偶，刹那间强烈的电流便贯穿了他的意识。

…………

……

“老大！老大糟了糟了！”

大宅之中，一个看起来是混混的家伙跑了进来。

“混账！你还嫌我不够心烦的吗！！”

坐在大堂中央的是一个颇具威严的老人，原本就因为孙子被绑架的事情焦头烂额的他失去了原本的从容，对着叨扰的来者就把手中的茶杯直接砸了过去。

“是那个女人，那个红发的女人回来了……她带着少主回来了！”

“什么！？”

还没等老人回过神来，一个有着火红头发的女人带着一个小男孩缓缓地走进了大堂，她正是刚才在小巷里表演的人偶师。

“爷爷……！”

在看到老人的一瞬间，小男孩便哭着冲向了老人的怀中，让他又惊又喜。

“啊啊，我的乖孙子……！你没受伤吧……你是怎么回来的！？”小男孩摇了摇头示意自己没受伤，又指了指不远处的红发女子。

“是这位姐姐把我从坏人手中带回来的！”

“是你……？你到底想干什么，你这巡尉派来的内鬼为什么要帮助我。”

红发女子甩了甩手，让手边的人偶将抓住的那个斗篷男人展示给老人看。

“我的目标暂时只是你们对家的那帮家伙，你们也不过是被我利用了而已。你们虽不能说是什么善人，但……孩子不该被卷入这场混战之中。”

她扫视了一下整个大堂中的小混混，露出了微笑。

“还是说……你们觉得凭你们能留得下我这个可恶的叛徒？”

老人闭上了眼，叹了口气，示意手下的人收起武器。

“你走吧，不要让我再看到你……”

女子优雅地告辞之后，老人叹了口气。

“那家伙能够随便进来又随便离开，还说目标'暂时’不是我们而已…看来之后的清算是怎么都避不过了。”

老人望着孙子可爱的脸蛋，陷入长久的沉默之中。”`,
  },

  {
    id: "3",
    title: "灰烬中的名字",
    content: `“很遗憾，‘麻雀’和‘金丝鸟’确认殉职了……他们失手暴露了自己的身份，所以被犯罪组织清除了。”

“不可能！师父师母他们怎么会这么简单地死去……”

激动的青年碰倒了桌上的奶瓶，摇篮中的女婴被吵醒，开始哭喊了起来，青年连忙将其抱在怀里。

“说起来，他们还有一个孩子啊，而且还是个不省心的共鸣者……看来今后必须要托付给你照顾了，不过反正你也被停职了，刚好有大把的时间不是吗。”

“我一定会照顾好她的，不用你们担心。”

“对了，你的师父他之前好像在暗中调查着什么，你知道些什么吗？”

“我不知道……”

青年知道他想问的是关于治安署有内鬼的事情，而面前的人很可能就是他们派来的……决不能向他们透露半句信息。

“我们的调查员明天会来这房子里进一步调查的，到时候请你配合一下。”

他知道自己没有办法阻止他们，尤其是还需要带着一个小婴儿在身边。

“明天……好，那我们今晚收拾一下，明天就会找新的地方搬走，这样可以了吧。”

“当然，当然……趁这个机会找一个新的地方，开始一段新的人生吧，呵呵。”

只是装作低头收拾东西的青年，自然没有错过那个巡尉眼中闪过的一丝异样的凶光。

…………

……

曾经的家被火海吞噬，仍在青年怀中的幼小生命却并没有再哭喊，只是望着匆忙走动的嘈杂人群发呆。

有人从远处走近，青年将戴着的兜帽帽檐进一步压低，把怀中的女婴再往大衣之中塞了塞。

但那人越过了他，走到了阴影处用终端发起了通讯。

“是的……已经确认过，两个人都已经解决了。”

青年相当肯定，眼前的这个人就是治安署里面的内鬼所派来的，目的就是他和怀中女婴的性命，还有他的师父师母住处中有可能存在的对他们不利的资料。

（哼……这帮家伙果然不打算放过我们，甚至还没能等到第二天再动手。）

幸好青年早有准备，使用他的共鸣能力制作了他和女婴的人偶——虽然这样制作出的人偶并不能作出应答，但让他们以为是熟睡的两人已经足够了。

这样才能瞒天过海，带上一切的资料从密道逃走，他们只有在档案中永远地变成死人才是最安全的。

从今天开始，他和怀中女婴将不能再以过去的身份活下去，他们需要一个新的名字，一个新的面孔。

他默默从怀中拿出一个丑陋的面具戴在脸上，然后用手掩住了女婴的双眼，背对着熊熊火光走向了黑暗之中不再回头。

“从今天开始……我就是‘偃师’，而你就叫‘吟霖’——那是师父师母早就为你准备好的名字。`,
  },

  {
    id: "4",
    title: "向己告别",
    content: `“偃师大人，我想去报名参加治安署的选拔。”

听到吟霖这么说的偃师并没有多惊讶，反而是身边的一个年老的女性露出了担心的表情。

“吟霖小姐啊……老太婆我啊，一直都把你当成是自己的孙女，我真的不想看到你去那种危险的地方，治安署那里是容不得我们的。”

“馆婆你放心，没有人知道我的真正身份，对于治安署来说，我不过只是一个参加选拔的外来人而已，而且还有偃师大人给我伪造身份。”

“但是啊……我真的不想再失去家人了，听馆婆的，留在归魂互助会这里，哪里都别去了……”

偃师合上手中的笔记本，摆摆手阻止了馆婆继续往下说。

“去吧，刚好我的研究计划也差不多该进行到下一步了，肯定免不了要和今州治安署产生冲突，如果在治安署的高层中有内应的话，也会更加的得心应手。”

“不，我希望能够成为一名潜入调查员……和我的父母他们一样，我想用这种方式继承他们的信念。”

吟霖看不到偃师面具背后的表情，自从吟霖懂事开始，她就从来没见过他摘下那副面具。

但他的眼神里少有地露出了复杂的感情，良久之后，才慢慢地点了点头。

“在我用人偶复活师父和师母之前，你可以尽情去了解一切你想要了解的……等到我成功之后，我们就会向治安署复仇，将所有陷害过他们的内鬼像垃圾一样全部铲除！”

吟霖还想说点什么，但是偃师却没有再看向她，而是专注于手中正在制作的一具人偶。

吟霖朝着偃师的背影点了点头，便转身离开了，她知道从现在开始，她和偃师注视的东西已经不再一致。`,
  },

  {
    id: "5",
    title: "黑暗的一角",
    content: `吟霖忍着侧腹的剧痛站起身来，艰难地靠在桌子的边缘。

一个男人跌跌撞撞地从阴影处走出，将刺入他身体的人偶的锋利双手拔出，狠狠地丢在了一边。

“虽然不知道你为什么冒险混入我们组织，却只是想要调查那两个死巡尉的资料，但现在看来是我赢了！”

吟霖勉强在指尖汇聚起雷电的长鞭向着男人甩去，却因为剧痛而失去了准头，打在了距离男人数米远的地面。

“我的共鸣能力可以让你的心率失常，引起心脏休克，只要你还是人类的话就不可能能躲过这招。”

男人手臂上的声痕再次发出亮光，吟霖连站立都维持不住，失去力量的躯体倒在了地上。

“我们组织里没有你这么强的共鸣者……巡尉那边也有我们的内应，你到底是怎么……”

他好像想起什么一样，微笑了起来。

“呵呵，我懂了……你是潜入调查员吧，真是蠢啊，居然还真有人为了这样的事情而卖命，就算让你查到我们的真相又能怎样，世界会因此改变吗？”

吟霖的呼吸越来越微弱，男人知道她的心脏已经停跳。

“是时候送你上路了，真是可惜啊，你早就应该知道残星会是惹不得的吧……”

正当男人的匕首快要刺入吟霖的咽喉的时候，一股强烈的雷击顺着匕首冲击着他的全身，瞬间让他失去了活动能力。

“为……为什么……”

他在昏迷的前一瞬间，看到了吟霖胸膛跳动的雷光——她在最后的时刻用电击刺激已经停跳的心脏，让本来休克的心脏再次跳动。

吟霖甩动雷电丝线，用人偶“悬丝”代替动弹不得的身体靠近男人，从他的怀中掏出了一份资料。

“残星会……果然是他们，我一定会让这隐藏起来的黑暗……全部连根拔起。”`,
  },
];
const current = ref(0);

function select(index) {
  current.value = index;
  // 将焦点移回当前 tab（便于无障碍与键盘导航）
  const id = `tab-${items[index].id}`;
  const el = document.getElementById(id);
  if (el) el.focus();
}
const storyRef = ref<HTMLElement | null>(null);

function prev() {
  current.value = (current.value - 1 + items.length) % items.length;
  select(current.value);
  storyRef.value.scrollIntoView({ behavior: "smooth", block: "start" });
}

function next() {
  current.value = (current.value + 1) % items.length;
  select(current.value);
  storyRef.value.scrollIntoView({ behavior: "smooth", block: "start" });
}
interface Chibi {
  src: string;
  top: number;
  left: number;
}

const chibiList = ref<Chibi[]>([]);
onMounted(async () => {
  if (!reducedMotion) {
    const tl = gsap.timeline({ defaults: { ease: "power3.out" } });
    tl.from(".avatar-card", {
      duration: 0.8,
      y: 18,
      opacity: 0,
      scale: 0.99,
    }).from(
      ".right-col > .hero-panel .name",
      { duration: 0.9, x: 24, opacity: 0 },
      "-=0.45"
    );

    gsap.utils.toArray(".tl-item").forEach((it: any, idx: number) => {
      gsap.from(it.querySelector(".tl-card"), {
        scrollTrigger: {
          trigger: it,
          start: "top 85%",
          toggleActions: "play none none reverse",
        },
        opacity: 0,
        y: 22,
        duration: 0.7,
        delay: idx * 0.06,
      });
    });

    gsap.to(".avatar-card", {
      scale: 1.007,
      duration: 2.8,
      yoyo: true,
      repeat: -1,
      ease: "sine.inOut",
    });
  } else {
    document.documentElement.classList.add("reduced-motion");
  }

  // // 1. 基础配置信息
  // const total = 6;
  // let pickCount = 3; // 每次抽取 3 张
  // const vw = window.innerWidth;
  // const vh = window.innerHeight;
  // const isMobile = window.innerWidth <= 768;
  // // 如果已知单张小人图片的宽高，可避免超出边界；
  // // 假设小人图片宽 100px、高 100px，按需替换：
  // const imgWidth = 100;
  // const imgHeight = 100;

  // // 2. Fisher–Yates 洗牌函数
  // function shuffle(array) {
  //   for (let i = array.length - 1; i > 0; i--) {
  //     const j = Math.floor(Math.random() * (i + 1));
  //     [array[i], array[j]] = [array[j], array[i]];
  //   }
  //   return array;
  // }

  // // 3. 随机选出 3 个编号
  // if (isMobile) {
  //   pickCount = 1;
  // }
  // const nums = shuffle(Array.from({ length: total }, (_, k) => k + 1));
  // const picks = nums.slice(0, pickCount);

  // // 4. 生成随机位置并填充 chibiList
  // chibiList.value = []; // 先清空
  // picks.forEach((i) => {
  //   chibiList.value.push({
  //     src: `/QImages/1 (${i}).png`,
  //     left: Math.random() * (vw - imgWidth), // 保证不超出左右边界
  //     top: Math.random() * (vh - imgHeight), // 保证不超出上下边界
  //   });
  // });

  // // 2. 等 img 渲染到 DOM
  // await nextTick();

  // // 3. 给每个小人绑定 GSAP 动画
  // const imgs = document.querySelectorAll<HTMLImageElement>(".chibi-img");
  // imgs.forEach((img, index) => {
  //   const padding = 200; // 边缘预留空间
  //   // ✅ 初始出场动画（闪现）
  //   gsap.fromTo(
  //     img,
  //     { opacity: 0, scale: 0.5 },
  //     {
  //       opacity: 1,
  //       scale: 1,
  //       duration: 0.8,
  //       ease: "back.out(2)",
  //       delay: 0.2 * index,
  //     }
  //   );

  //   // ✅ 鼠标靠近闪避
  //   img.addEventListener("mouseenter", () => {
  //     gsap.killTweensOf(img);

  //     gsap.to(img, {
  //       x: "+=" + ((Math.random() - 0.5) * 400).toFixed(0),
  //       y: "+=" + ((Math.random() - 0.5) * 400).toFixed(0),
  //       duration: 1.2,
  //       ease: "back.out(2)",
  //       onComplete: () => {
  //         // 闪避完成后，再重新启用动画
  //         animate(img);
  //       },
  //     });
  //   });

  //   const animate = (img: HTMLImageElement) => {
  //     let { x, y } = img.getBoundingClientRect();
  //     let deltaX = (Math.random() - 0.5) * 200;
  //     let deltaY = (Math.random() - 0.5) * 200;

  //     // 预测一下偏移后的位置
  //     let nextX = x + deltaX;
  //     let nextY = y + deltaY;

  //     // 校正：防漂出左、右、上、下边界
  //     if (nextX < padding) deltaX = padding - x;
  //     if (nextX + img.width > window.innerWidth - padding)
  //       deltaX = window.innerWidth - padding - (x + img.width);
  //     if (nextY < padding) deltaY = padding - y;
  //     if (nextY + img.height > window.innerHeight - padding)
  //       deltaY = window.innerHeight - padding - (y + img.height);

  //     gsap.to(img, {
  //       x: `+=${deltaX.toFixed(0)}`,
  //       y: `+=${deltaY.toFixed(0)}`,
  //       rotation: `+=${((Math.random() - 0.5) * 60).toFixed(0)}`,
  //       duration: 2 + Math.random() * 2,
  //       ease: "power1.inOut",
  //       onComplete: () => animate(img),
  //     });
  //   };
  //   animate(img);
  // });
});
</script>

<style scoped lang="scss">
/* 吟霖风格 —— 紫蓝海感（水母/幻海） + 毒药/治愈双重高光 */
$bg-deep: #050406; // 深海夜色底
$deep-2: #0a0a0c; // 次深底用于渐变
$accent-1: #d93a3a; // 暗紫主光（冷雅）
$accent-2: #b36bff; // 冷海蓝高光（湿光感）

$text-main: #fff6f6; // 文字
$card-bg: rgba(6, 8, 12, 0.46);
$card-border: rgba(184, 107, 224, 0.06);
$soft-shadow: rgba(0, 0, 0, 0.6);
$inner-glow: rgba(184, 107, 224, 0.03);
/* 固定浮动小 chibi 层（保留） */
.floating-chibis {
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 1;
  .chibi-img {
    position: absolute;
    width: 80px;
    user-select: none;
    transform-origin: center center;
    pointer-events: auto;
    z-index: 10;
  }
}

.megumi-page {
  position: relative;
  min-height: 100vh;
  background: linear-gradient(180deg, $bg-deep 0%, $deep-2 72%);
  font-family: "Noto Sans SC", system-ui, -apple-system, "Segoe UI", Roboto,
    Arial;
  color: $text-main;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: clamp(20px, 4vw, 80px);
  box-sizing: border-box;
  padding-top: 60px;

  &.reduced-motion * {
    transition: none !important;
    animation: none !important;
  }

  .container {
    position: relative;
    z-index: 10;
    max-width: 1100px;
    margin: 0 auto;
    padding: clamp(12px, 2vw, 40px);
  }
}

/* ========== HERO 区域（整体暗化 + 血玫点光） ========== */
.hero {
  position: relative;
  display: grid;
  grid-template-columns: 280px 1fr;
  gap: 28px;
  align-items: start;
  padding: 12px;
  margin-bottom: 12px;

  /* 乐谱画布 —— 在 hero 背后增加五线谱移动感 */
  &::before {
    content: "";
    position: absolute;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    background-image: repeating-linear-gradient(
      to bottom,
      rgba(255, 255, 255, 0.02) 0px,
      rgba(255, 255, 255, 0.02) 1px,
      transparent 1px,
      transparent 16px
    );
    opacity: 0.06;
    mix-blend-mode: overlay;
    transform: translateY(-4%);
    animation: staff-drift 16s linear infinite;
  }

  .left-col {
    display: flex;
    flex-direction: column;
    align-items: center;
    z-index: 6;
  }

  .avatar-card {
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.01),
      rgba(184, 107, 224, 0.01)
    );
    border-radius: 16px;
    padding: 12px;
    display: grid;
    justify-items: center;
    gap: 8px;
    border: 1px solid $card-border;
    box-shadow: 0 14px 44px $soft-shadow, inset 0 1px 0 $inner-glow;
    cursor: pointer;
    transition: transform 0.28s ease, box-shadow 0.28s ease;
    width: 100%;
  }

  .avatar-wrap {
    width: 100%;
    display: block;
  }

  .avatar {
    width: 100%;
    height: auto;
    border-radius: 12px;
    display: block;
    box-shadow: 0 12px 34px rgba(0, 0, 0, 0.5), 0 0 18px rgba($accent-1, 0.03);
    transition: transform 0.5s ease, filter 0.5s ease;
    background-color: rgba(0, 0, 0, 0.04);
    filter: saturate(0.8) contrast(0.95) brightness(0.92);
  }

  .avatar-card:hover .avatar {
    transform: translateY(-4px) scale(1.02);
    filter: saturate(0.7) contrast(0.9) brightness(0.9);
  }

  .avatar-meta {
    display: flex;
    gap: 8px;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
  }

  .avatar-badge {
    font-size: 0.9rem;
    color: $text-main;
    background: rgba(0, 0, 0, 0.18);
    padding: 6px 10px;
    border-radius: 999px;
    border: 1px solid rgba($accent-2, 0.05);
    font-weight: 600;
  }

  .right-col {
    display: flex;
    flex-direction: column;
    gap: 12px;
    z-index: 6;
  }

  .hero-panel {
    position: relative;
    z-index: 6;
    padding: 20px;
    border-radius: 14px;
    background: $card-bg;
    backdrop-filter: blur(8px) saturate(0.9);
    border: 1px solid $card-border;
    box-shadow: 0 12px 50px rgba(0, 0, 0, 0.6), inset 0 1px 0 $inner-glow;
  }

  .name {
    font-size: clamp(1.8rem, 3vw, 2.8rem);
    margin: 0;
    font-weight: 900;
    letter-spacing: 1px;
    line-height: 1;
    display: inline-block;
    /* 标题改为 暗紫 → 血玫 渐变 */
    background: linear-gradient(90deg, $accent-1 0%, $accent-2 70%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
    -webkit-text-stroke: 0.2px rgba(0, 0, 0, 0.22);
    text-shadow: 0 10px 36px rgba(0, 0, 0, 0.65);
    position: relative;
  }

  .jp {
    font-size: 0.95rem;
    color: $accent-1;
    margin-left: 8px;
    font-weight: 400;
  }

  .subtitle {
    margin: 6px 0 0;
    font-size: 1.1rem;
    color: $accent-1;
    font-weight: 600;
    line-height: 1.4;
  }

  .lead {
    margin: 10px 0 0;
    color: $text-main;
    opacity: 0.96;
    line-height: 1.7;
    max-width: 72ch;
  }
}

/* ========== 通用卡片（更暗、更锐利的边与血色提示） ========== */
.card {
  margin-top: 24px;
  background: rgba(6, 6, 8, 0.5);
  border-radius: 14px;
  padding: 24px;
  box-shadow: 0 12px 48px rgba(0, 0, 0, 0.6);
  backdrop-filter: blur(6px);
  color: $text-main;
  border: 1px solid $card-border;
  transition: transform 0.28s ease, box-shadow 0.28s ease;

  &:hover {
    transform: translateY(-8px) scale(1.01);
    box-shadow: 0 30px 90px rgba(0, 0, 0, 0.7);
  }

  h2 {
    margin: 0 0 12px 0;
    font-size: 1.3rem;
    color: $accent-2;
  }

  .card-head {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
  }
}

/* personality 列表样式（暗紫细线） */
.personality .traits li {
  padding: 12px 0;
  border-bottom: 1px dashed rgba($accent-1, 0.06);
  font-size: 1rem;
  color: rgba($text-main, 0.92);
}

/* overview 双栏布局（保持） */
.overview .two-col {
  display: flex;
  gap: 24px;
  flex-wrap: wrap;
  margin-top: 12px;
}

.overview .text-block {
  flex: 1 1 40%;
  min-width: 240px;
  line-height: 1.6;
  color: rgba($text-main, 0.96);
}

/* special-section：加入音符漂浮和暗紫边框 */
.special-section {
  position: relative;
  overflow: hidden;

  .content {
    display: flex;
    gap: 24px;
    align-items: center;
    margin-top: 16px;
  }

  .img-area {
    flex: 0 0 200px;

    img {
      width: 100%;
      height: auto;
      border-radius: 12px;
      box-shadow: 0 14px 44px rgba(0, 0, 0, 0.6), 0 0 12px rgba($accent-1, 0.02);
      border: 1px solid rgba($accent-1, 0.03);
    }
  }

  .text-block {
    flex: 1;
    line-height: 1.6;
    color: rgba($text-main, 0.95);
  }
}

/* ll-stories — 暗底 + 微血色分割线 */
.ll-stories {
  .card {
    width: min(1200px, 100%);
    border-radius: 12px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.6),
      inset 0 1px 0 rgba($accent-1, 0.02);
    color: $text-main;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    background: linear-gradient(
      180deg,
      rgba(8, 10, 12, 0.12),
      rgba(8, 6, 10, 0.06)
    );
  }

  .card-head {
    padding: 14px 16px;
    border-bottom: 1px solid rgba($accent-2, 0.03);
    display: flex;
    flex-direction: column;
    gap: 12px;

    .card-title {
      font-size: 24px;
      font-weight: 700;
      color: $accent-1;
      letter-spacing: 0.6px;
    }
  }

  .card-body {
    padding: 18px 16px;
    min-height: 160px;
    position: relative;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0), rgba(8, 8, 10, 0.02));
  }

  .story {
    color: rgba($text-main, 0.96);

    .story-head {
      font-size: 18px;
      color: $accent-2;
      font-weight: 700;
      margin-bottom: 8px;
    }

    .story-content {
      line-height: 1.7;
      color: rgba($text-main, 0.92);
      white-space: pre-wrap;
    }
  }

  .card-foot {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 8px;
    padding: 10px 14px;
    border-top: 1px solid rgba($accent-1, 0.02);
    background: linear-gradient(
      180deg,
      rgba(0, 0, 0, 0.02),
      rgba(0, 0, 0, 0.04)
    );

    .nav-btn {
      background: transparent;
      border: 1px solid rgba($accent-1, 0.06);
      color: $accent-2;
      padding: 6px 10px;
      border-radius: 6px;
      cursor: pointer;
      transition: background 180ms ease;
      &:hover {
        background: rgba($accent-2, 0.04);
      }
    }

    .pager {
      color: rgba($text-main, 0.72);
      font-size: 13px;
      font-weight: 600;
    }
  }

  /* 切换动画保留，但更暗 */
  .fade-slide-enter-active,
  .fade-slide-leave-active {
    transition: all 320ms cubic-bezier(0.2, 0.9, 0.2, 1);
  }

  .fade-slide-enter-from {
    opacity: 0;
    transform: translateY(6px);
  }

  .fade-slide-enter-to {
    opacity: 1;
    transform: translateY(0);
  }

  .fade-slide-leave-from {
    opacity: 1;
    transform: translateY(0);
  }

  .fade-slide-leave-to {
    opacity: 0;
    transform: translateY(-6px);
  }
}

/* timeline（暗紫竖线 + 微光） */
.timeline {
  position: relative;

  .tl-wrap {
    position: relative;
    padding: 24px 12px 12px 96px;
  }

  .vl {
    position: absolute;
    left: 80px;
    top: 32px;
    bottom: 20px;
    width: 4px;
    border-radius: 6px;
    background: linear-gradient(
      180deg,
      rgba($accent-2, 0.12),
      rgba($accent-1, 0.1)
    );
    box-shadow: 0 6px 18px rgba($accent-1, 0.06),
      inset 0 0 10px rgba($accent-1, 0.02);
    opacity: 0.95;
  }

  .tl-list {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .tl-item {
    position: relative;
    display: flex;
    gap: 18px;
    align-items: flex-start;
    margin: 20px 0;
    transition: transform 0.28s ease, box-shadow 0.28s ease;
  }

  .tl-card {
    background: rgba(8, 6, 10, 0.36);
    border-radius: 12px;
    padding: 16px 20px;
    box-shadow: 0 12px 36px rgba(0, 0, 0, 0.55);
    width: calc(100% - 130px);
    border-left: 4px solid transparent;
    transition: transform 0.28s ease, box-shadow 0.28s ease,
      border-color 0.28s ease;
    position: relative;
    z-index: 2;
  }

  .tl-item:hover .tl-card,
  .tl-item:focus-within .tl-card {
    transform: translateY(-8px);
    box-shadow: 0 24px 72px rgba(0, 0, 0, 0.6);
    border-left-color: rgba($accent-2, 0.18);
  }

  .tl-title {
    margin: 0 0 6px 0;
    font-size: 1.1rem;
    color: $accent-1;
    display: flex;
    align-items: baseline;
    gap: 8px;
  }

  .tl-desc {
    margin: 0;
    color: rgba($text-main, 0.92);
    white-space: pre-wrap;
  }
}

/* 浮动音符（可在模板中渲染若干 .floating-note） */
.floating-note {
  position: absolute;
  font-size: 14px;
  color: $accent-2;
  opacity: 0.95;
  transform-origin: center;
  animation: note-float 4.6s ease-in-out infinite;
  filter: drop-shadow(0 6px 18px rgba($accent-2, 0.06));
}

/* 动画关键帧 */
@keyframes staff-drift {
  0% {
    transform: translateY(-4%);
    opacity: 0.9;
  }
  50% {
    transform: translateY(6%);
    opacity: 0.95;
  }
  100% {
    transform: translateY(-4%);
    opacity: 0.9;
  }
}

@keyframes note-float {
  0% {
    transform: translateY(0) rotate(-6deg) scale(0.95);
    opacity: 0.85;
  }
  50% {
    transform: translateY(-12px) rotate(3deg) scale(1);
    opacity: 1;
  }
  100% {
    transform: translateY(0) rotate(-6deg) scale(0.95);
    opacity: 0.85;
  }
}

/* 响应式：小屏适配（保留原逻辑，仅小幅调整文字色调与阴影） */
@media (max-width: 980px) {
  .hero {
    grid-template-columns: 1fr;
    gap: 18px;
    padding: 8px;
  }

  .avatar-card {
    width: 140px;
    padding: 8px;
  }

  .hero-panel {
    padding: 14px;
  }

  .name {
    font-size: 1.8rem;
  }

  .subtitle {
    font-size: 1rem;
  }

  .lead {
    font-size: 0.95rem;
  }

  .card {
    padding: 18px;
    border-radius: 12px;
  }

  .overview .two-col {
    flex-direction: column;
  }

  .special-section .content {
    flex-direction: column;
  }

  .ll-stories {
    .card {
      border-radius: 10px;
    }

    .card-head {
      padding: 12px 12px;
    }

    .card-body {
      padding: 14px 12px;
      min-height: 180px;
    }

    .card-foot {
      padding: 8px 12px;
    }
  }

  .timeline {
    overflow: visible;
  }

  .timeline .tl-wrap {
    padding-left: 14px !important;
    padding-right: 14px;
    min-height: 0;
  }

  .timeline .vl {
    display: none !important;
  }

  .timeline .tl-list {
    overflow: visible;
  }

  .timeline .tl-item {
    display: block !important;
    margin: 14px 0 !important;
    width: 100%;
  }

  .timeline .tl-card {
    width: 100% !important;
    padding: 14px !important;
    border-left: 0 !important;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.45);
    transform: none !important;
  }
}
</style>
