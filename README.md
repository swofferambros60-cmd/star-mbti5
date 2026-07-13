<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>✨ 解锁你的24型灵魂人格 ✨</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;700;900&display=swap');
        body {
            font-family: 'Noto Sans SC', sans-serif;
            background-color: #f9f9f9;
            -webkit-tap-highlight-color: transparent;
        }
        .brand-gradient {
            background: linear-gradient(135deg, #ff2442 0%, #ff4b5c 100%);
        }
        .brand-text-gradient {
            background: linear-gradient(135deg, #ff2442 0%, #ff763b 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .animate-bounce-slow {
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0%, 100% { transform: translateY(-3px); }
            50% { transform: translateY(3px); }
        }
    </style>
</head>
<body class="text-slate-800 antialiased selection:bg-rose-100 flex justify-center items-start min-h-screen">

    <div class="w-full max-w-md bg-white min-h-screen shadow-2xl flex flex-col justify-between relative overflow-hidden">
        
        <div class="absolute top-[-50px] right-[-50px] w-48 h-48 rounded-full bg-rose-100/40 blur-2xl pointer-events-none"></div>
        <div class="absolute bottom-[-20px] left-[-20px] w-64 h-64 rounded-full bg-amber-100/30 blur-3xl pointer-events-none"></div>

        <!-- 1. 欢迎首页面 -->
        <div id="welcome-view" class="flex-1 flex flex-col justify-between p-6">
            <div class="text-center pt-8">
                <span class="inline-block bg-rose-50 text-[#ff2442] text-xs font-bold px-3 py-1.5 rounded-full border border-rose-200 tracking-wider mb-4 animate-bounce-slow">🔮 2026年最新爆款社交人格图鉴</span>
                <h1 class="text-3xl font-black tracking-tight leading-snug">
                    测测你是全网的<br><span class="brand-text-gradient text-4xl">哪一种神级人格？</span>
                </h1>
                <p class="text-slate-400 text-sm mt-3">大数据精准匹配 · 24款高颜值限定人设</p>
            </div>

            <div class="my-8 bg-slate-50 border border-slate-100 rounded-2xl p-4 space-y-3.5 shadow-inner">
                <div class="flex items-center gap-3">
                    <span class="text-xl">🔥</span>
                    <p class="text-sm font-medium text-slate-600">已吸引 <span class="text-[#ff2442] font-bold">189,482</span> 人参与深度测试</p>
                </div>
                <div class="flex items-center gap-3">
                    <span class="text-xl">🎯</span>
                    <p class="text-sm font-medium text-slate-600">朋友圈、热门社交圈高达 <span class="text-emerald-500 font-bold">99.8%</span> 一致好评</p>
                </div>
                <div class="flex items-center gap-3">
                    <span class="text-xl">✨</span>
                    <p class="text-sm font-medium text-slate-600">全面剖析你的：精神状态 | 恋爱搭子 | 吸金指数</p>
                </div>
            </div>

            <div class="pb-6">
                <button onclick="startQuiz()" class="w-full brand-gradient text-white text-lg font-bold py-4 rounded-xl shadow-[0_10px_20px_rgba(255,36,66,0.3)] active:scale-98 transition-all hover:opacity-95 text-center block cursor-pointer">
                    开始深度解锁 (20题) 🚀
                </button>
                <p class="text-center text-xs text-slate-400 mt-3">点击即代表您同意服务条款，测试结果仅供娱乐</p>
            </div>
        </div>

        <!-- 2. 答题进行面 -->
        <div id="quiz-view" class="hidden flex-1 flex flex-col justify-between p-6">
            <div>
                <div class="w-full bg-slate-100 h-2 rounded-full overflow-hidden mt-4">
                    <div id="progress-bar" class="brand-gradient h-full w-0 transition-all duration-300"></div>
                </div>
                <div class="flex justify-between items-center mt-2 text-xs text-slate-400 font-medium">
                    <span id="progress-text">第 1 / 20 题</span>
                    <span>深度分析中...</span>
                </div>

                <div class="mt-8 bg-slate-50 border border-slate-100 p-6 rounded-2xl shadow-sm min-h-[140px] flex items-center">
                    <h3 id="question-title" class="text-xl font-bold text-slate-800 leading-relaxed">正在加载问题...</h3>
                </div>

                <div id="options-container" class="mt-6 space-y-3"></div>
            </div>
            
            <div class="pt-6 text-center text-xs text-slate-400">
                🔒 安全加密保护，保障选择隐私
            </div>
        </div>

        <!-- 3. 拦截付费面 -->
        <div id="pay-view" class="hidden flex-1 flex flex-col justify-between p-6">
            <div class="text-center pt-2">
                <div class="w-16 h-16 bg-rose-50 text-[#ff2442] rounded-full flex items-center justify-center mx-auto text-3xl mb-3 shadow-sm">📊</div>
                <h3 class="text-xl font-black">20维报告生成成功！</h3>
                <p class="text-slate-500 text-xs mt-1">只差最后一步，即可解锁专属于你的高级人格图鉴</p>
                
                <div class="border-t-2 border-dashed border-slate-200 my-4 relative">
                    <span class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 bg-white px-3 text-xs text-slate-400 font-bold">精选特惠解锁</span>
                </div>

                <div class="bg-emerald-50 border border-emerald-100 p-4 rounded-2xl max-w-[280px] mx-auto shadow-sm">
                    <img src="qr.jpg" alt="微信支付二维码" class="w-full aspect-[3/4] object-cover rounded-xl shadow-md border-2 border-white">
                    <p class="text-xs text-emerald-700 font-bold mt-2 flex items-center justify-center gap-1">
                        <span>💡</span> 长按识别或保存扫码支付
                    </p>
                </div>

                <div class="mt-5 bg-slate-50 p-4 rounded-xl border border-slate-100 text-left">
                    <label class="block text-xs font-bold text-slate-500 mb-1.5">👇 请输入您实际支付的金额完成校验：</label>
                    <div class="relative rounded-lg shadow-sm">
                        <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                            <span class="text-slate-500 font-bold text-lg">￥</span>
                        </div>
                        <input type="number" step="0.01" id="pay-amount" class="w-full bg-white border border-slate-200 rounded-lg pl-8 pr-3 py-2.5 text-slate-800 font-black text-lg focus:outline-none focus:border-[#ff2442] transition-colors" placeholder="如：2.00, 5.20 ...">
                    </div>
                    <p class="text-[11px] text-[#ff2442] mt-1.5 font-medium">⚠️ 提示：需付款满 2 元（含2元），方可成功激活生成结果。</p>
                </div>
            </div>

            <div class="pb-4 mt-6">
                <button onclick="verifyPayment()" class="w-full bg-emerald-500 text-white text-base font-bold py-3.5 rounded-xl shadow-[0_6px_15px_rgba(16,185,129,0.3)] active:scale-98 transition-all hover:bg-emerald-600 cursor-pointer flex items-center justify-center gap-2">
                    ✅ 我已付款，立即显示生成结果
                </button>
            </div>
        </div>

        <!-- 4. 报告生成结果面 -->
        <div id="result-view" class="hidden flex-1 p-6 bg-slate-50 overflow-y-auto">
            <div class="bg-white border-2 border-slate-900 rounded-3xl p-5 shadow-[6px_6px_0px_#1e293b] relative overflow-hidden">
                <div class="absolute top-0 right-0 brand-gradient text-white text-[10px] font-bold px-4 py-1 rounded-bl-xl tracking-wider">
                    PRO RARE
                </div>

                <div class="border-b border-slate-100 pb-4">
                    <p class="text-xs font-bold text-slate-400 uppercase tracking-widest">MY MBTI RARE FACTOR</p>
                    <h2 id="result-title" class="text-2xl font-black text-slate-900 mt-1">加载中...</h2>
                    
                    <!-- 新增：醒目的性格字母代码展示区 -->
                    <div class="mt-3 bg-rose-50 border border-rose-100 rounded-xl p-3 flex items-center gap-3">
                        <div class="bg-white text-[#ff2442] font-black text-2xl tracking-widest px-4 py-1.5 rounded-lg shadow-sm border border-rose-50" id="result-code">
                            MBTI
                        </div>
                        <div class="flex flex-col justify-center">
                            <span class="text-[13px] font-bold text-rose-800">专属性格代码认证</span>
                            <span class="text-[10px] font-medium text-rose-500 mt-0.5">你的底层行为逻辑模型</span>
                        </div>
                    </div>

                    <div class="flex flex-wrap gap-1.5 mt-3" id="result-tags"></div>
                </div>

                <!-- 核心维度指标分析 -->
                <div class="py-4 space-y-3">
                    <h4 class="text-xs font-bold text-slate-400 tracking-wider">🌟 核心能量维度</h4>
                    <div class="space-y-2">
                        <div>
                            <div class="flex justify-between text-xs font-bold mb-1">
                                <span>🔮 精神松弛度</span>
                                <span id="stat-1">90%</span>
                            </div>
                            <div class="w-full bg-slate-100 h-2 rounded-full overflow-hidden">
                                <div id="stat-bar-1" class="bg-rose-500 h-full transition-all duration-1000" style="width: 0%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between text-xs font-bold mb-1">
                                <span>💰 吸金爆发力</span>
                                <span id="stat-2">85%</span>
                            </div>
                            <div class="w-full bg-slate-100 h-2 rounded-full overflow-hidden">
                                <div id="stat-bar-2" class="bg-amber-500 h-full transition-all duration-1000" style="width: 0%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between text-xs font-bold mb-1">
                                <span>🪐 深度独立性</span>
                                <span id="stat-3">78%</span>
                            </div>
                            <div class="w-full bg-slate-100 h-2 rounded-full overflow-hidden">
                                <div id="stat-bar-3" class="bg-indigo-500 h-full transition-all duration-1000" style="width: 0%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 深入人格白皮书 -->
                <div class="bg-slate-50 rounded-2xl p-4 border border-slate-100 mt-2">
                    <h4 class="text-xs font-bold text-slate-500 mb-2 flex items-center gap-1">📜 独家全网流行人格报告</h4>
                    <p id="result-desc" class="text-sm text-slate-600 leading-relaxed font-medium">加载中...</p>
                </div>

                <!-- 专属社交图谱匹配 -->
                <div class="grid grid-cols-2 gap-3 mt-4">
                    <div class="bg-emerald-50/60 border border-emerald-100 p-3 rounded-xl">
                        <span class="text-xs font-bold text-emerald-700">🤝 灵魂契合搭子</span>
                        <p id="match-good" class="text-sm font-bold text-slate-800 mt-1">加载中...</p>
                    </div>
                    <div class="bg-rose-50/60 border border-rose-100 p-3 rounded-xl">
                        <span class="text-xs font-bold text-rose-700">⚡ 磁场排斥绝缘</span>
                        <p id="match-bad" class="text-sm font-bold text-slate-800 mt-1">加载中...</p>
                    </div>
                </div>
            </div>

            <div class="mt-6 text-center space-y-3">
                <p class="text-xs text-slate-400 font-medium">📸 截图保存长图，发布到社交平台带话题 #全网爆火人格测试 疯狂吸粉吧！</p>
                <button onclick="location.reload()" class="inline-block text-xs bg-slate-200 text-slate-600 font-bold px-4 py-2 rounded-full active:scale-95 transition-transform cursor-pointer">
                    🔄 重新测试
                </button>
            </div>
        </div>

    </div>

    <!-- Custom Toast -->
    <div id="toast" class="fixed top-5 left-1/2 -translate-x-1/2 bg-slate-900/95 text-white text-xs font-bold py-3 px-5 rounded-full shadow-xl opacity-0 transition-opacity duration-300 pointer-events-none z-50 flex items-center gap-2 whitespace-nowrap"></div>

    <script>
        const quizData = [
            { q: "周末如果你有整整一天的空闲时间，你会怎么度过？", a: [{ text: "火速组局！约上朋友出门探店、疯狂拍照打卡✨", score: 4 }, { text: "宅在家里，开着香薰点外卖，看剧刷手机一整天🛌", score: 1 }, { text: "独自去美术馆、咖啡厅或图书馆，享受高质量独处☕", score: 2 }, { text: "做周密的搞钱或学习计划，把每一小时安排得明明白白📅", score: 3 }] },
            { q: "当看到朋友圈有人发了一段略带伤感的深夜emo文字，你的第一反应是？", a: [{ text: "立刻私聊对方疯狂输出小作文安慰，给足情绪价值❤️", score: 4 }, { text: "理性分析他遇到啥事了，并试图找出解决的核心方案💡", score: 3 }, { text: "默默点个赞，或者假装没看到直接划走，保持清静🤫", score: 2 }, { text: "内心毫无波澜甚至想笑，觉得对方有点太作了🃏", score: 1 }] },
            { q: "在工作中或搞副业小组合作时，你更倾向于扮演什么角色？", a: [{ text: "全场总指挥，把控全局，推进项目落地的“大猛人”👑", score: 3 }, { text: "灵感制造机，负责出让人眼前一亮的各种骚操作点子🎨", score: 4 }, { text: "默默干活的靠谱大后方，不爱抢风头但绝不掉链子🛠️", score: 1 }, { text: "专业杠精/质检员，专门挑出方案里不合逻辑的硬伤🔍", score: 2 }] },
            { q: "如果有人在公开场合非常直接地反驳了你的观点，你的当下反应是？", a: [{ text: "肾上腺素飙升！当场列举一二三点有理有据地怼回去🔥", score: 3 }, { text: "表面微笑说“哈哈确实”，内心默默给这个人画了个大叉❌", score: 2 }, { text: "瞬间开始怀疑自己，是不是我真的说错了，陷入内耗🥺", score: 1 }, { text: "完全不在意，觉得世界很大傻子很多，各自安好呗🌍", score: 4 }] },
            { q: "对于买东西、消费这件事，你的真实金钱观是？", a: [{ text: "早买早享受！千金难买我乐意，为了高颜值疯狂买单🛍️", score: 4 }, { text: "严格精打细算，货比三家，只买最实用、性价比最高的💳", score: 3 }, { text: "断舍离主义者，极简生活，物欲极低根本割不动我🧘", score: 2 }, { text: "疯狂囤货爱好者，看到打折或者买一送一就走不动路📦", score: 1 }] },
            { q: "你觉得自己目前的精神状态更贴近以下哪句网络热梗？", a: [{ text: "“尊严丢掉，轻装上阵！”—— 极致的发疯流松弛感😜", score: 4 }, { text: "“正在与世界进行微弱的脑电波连接”—— 轻度社恐防打扰🤖", score: 2 }, { text: "“莫生气，气出病来无人替”—— 佛系看淡一切的心态🧘", score: 1 }, { text: "“放下助人情结，尊重他人命运”—— 人间清醒搞钱第一💰", score: 3 }] },
            { q: "突然接到通知，原本定好的周末大聚会被取消了，你的反应？", a: [{ text: "狂喜！终于可以名正言顺地躺平了🎉", score: 1 }, { text: "赶紧在列表里摇人，找别的搭子出去玩🏃", score: 4 }, { text: "有点失落，但很快无缝切换成独处计划📖", score: 2 }, { text: "趁机把没做完的工作/学习任务拿出来清空📈", score: 3 }] },
            { q: "出门旅游前打包行李，你通常的状态是？", a: [{ text: "提前列好详尽的备忘录，分类收纳打包🎒", score: 3 }, { text: "临走前一晚疯狂往箱子里胡乱塞东西🌪️", score: 4 }, { text: "带最基础的，缺啥去当地买，主打一个潇洒✈️", score: 2 }, { text: "脑内演练无数突发情况，带一堆可能用不上的备用品🛡️", score: 1 }] },
            { q: "看到一部很火的催泪电影，你的关注点通常在？", a: [{ text: "完全代入主角的情感，痛哭流涕😭", score: 4 }, { text: "冷静思考导演的叙事逻辑和埋下的伏笔🎞️", score: 3 }, { text: "注意到极其唯美的画面构图和神仙配乐🎵", score: 2 }, { text: "联想到自己的人生经历，陷入深深的回忆💭", score: 1 }] },
            { q: "面对堆积如山的工作或学习任务，你的第一反应是？", a: [{ text: "先睡一觉或玩一会手机，不到最后一刻不启动🎮", score: 1 }, { text: "迅速拆解任务，列好优先级和时间表📊", score: 3 }, { text: "极度焦虑内耗，但还是会硬着头皮一点点啃完🧗", score: 2 }, { text: "寻找捷径，或者疯狂调动AI工具帮我快速搞定🚀", score: 4 }] },
            { q: "在一个充满陌生人的大型社交局上，你通常扮演？", a: [{ text: "默默在角落里干饭，别人聊到我才礼貌附和🍽️", score: 1 }, { text: "全场控场大师，主动抛梗化解所有尴尬的社牛🎤", score: 4 }, { text: "只和旁边看着顺眼的一两个人低声深入交流👥", score: 2 }, { text: "人类观察家，暗中观察每个人的微表情和小动作👀", score: 3 }] },
            { q: "如果朋友向你疯狂吐槽他的感情问题，你会？", a: [{ text: "同仇敌忾！跟着一起大骂对面的渣男/女🤬", score: 4 }, { text: "理性帮他分析利弊，试图给出最优的解决方案⚖️", score: 3 }, { text: "提供满满的情绪价值，给他抱抱和顺毛安慰🧸", score: 2 }, { text: "表面倾听点头，内心其实早已神游天外☁️", score: 1 }] },
            { q: "遇到完全不讲理、胡搅蛮缠的杠精，你的处理方式是？", a: [{ text: "开启阴阳怪气模式，用魔法打败魔法🤺", score: 4 }, { text: "一秒拉黑，跟他多说一个字都算我输🚫", score: 2 }, { text: "深吸一口气，试图继续摆事实讲道理证明他是错的📚", score: 3 }, { text: "觉得很好笑，纯粹当成互联网猴戏乐子看🍿", score: 1 }] },
            { q: "你的日常桌面/房间状态更偏向哪种？", a: [{ text: "乱中有序，虽然看着乱但我知道东西都在哪🌪️", score: 4 }, { text: "绝对整洁无死角，强迫症福音，看着就爽✨", score: 3 }, { text: "一阵一阵的，心血来潮了才会来一次彻底大扫除🧹", score: 1 }, { text: "极简主义，本来就没啥多余的东西，空空如也🧊", score: 2 }] },
            { q: "面对未来飞速发展的人工智能时代，你的态度是？", a: [{ text: "热烈拥抱变化，积极学习尝试各种新奇工具🤖", score: 4 }, { text: "稍微有点恐慌和焦虑，总担心自己的价值被替代📉", score: 1 }, { text: "走一步看一步，反正天塌下来有高个子顶着⛱️", score: 2 }, { text: "敏锐嗅探，深入研究背后潜藏的搞钱和商业机会💰", score: 3 }] },
            { q: "买衣服或日用品时，除了必需，你最看重？", a: [{ text: "颜值即正义！只要好看、能拍出美图就行📸", score: 4 }, { text: "实用性和性价比，只买经久耐用的实在货🛒", score: 3 }, { text: "品牌背后的文化故事或它所代表的生活态度🏷️", score: 2 }, { text: "面料材质、成分表等极其微小的细节🔬", score: 1 }] },
            { q: "朋友聚会时，大家突然都在低头玩手机，你会？", a: [{ text: "毫无压力，顺势也掏出手机开始冲浪📱", score: 1 }, { text: "觉得有点冷场，努力找个新话题活跃气氛🗣️", score: 4 }, { text: "非常享受这种互不打扰但又聚在一起的默契🍵", score: 2 }, { text: "感觉气氛异常尴尬，甚至想找借口提前溜走🏃", score: 3 }] },
            { q: "偶尔听到一首极其惊艳的新歌，你的第一反应？", a: [{ text: "疯狂单曲循环，直到听到想吐为止🎧", score: 1 }, { text: "立刻去查歌手的所有资料和这首歌的创作背景🔍", score: 3 }, { text: "火速分享给同频的好友，按头安利让他们也听📢", score: 4 }, { text: "默默红心收藏，放进自己极其私密的特定歌单里📂", score: 2 }] },
            { q: "晚上失眠的时候，你的大脑通常在想什么？", a: [{ text: "反复回放白天说错的一句话，尴尬到脚趾抠地🙈", score: 1 }, { text: "天马行空，幻想自己突然暴富或拥有某种超能力🦸", score: 4 }, { text: "思考人生的宏大意义、宇宙的尽头在哪里🌌", score: 3 }, { text: "大脑一片空白，纯粹是因为白天咖啡/茶喝多了☕", score: 2 }] },
            { q: "总结一下，你觉得真正的“做自己”是？", a: [{ text: "完全不在意他人的世俗眼光，只要我自洽就行🍃", score: 4 }, { text: "不断挑战自己的极限，实现个人阶层的跨越和进阶👑", score: 3 }, { text: "能够自由自在地表达各种情绪，不压抑不内耗❤️", score: 2 }, { text: "时刻保持清醒，拥有对生活各个方面的绝对掌控感🎯", score: 1 }] }
        ];

        // 数据库新增了 code（性格代码）字段
        const personalityData = [
            { title: "全能型松弛感大师", code: "ENFP", tags: ["超级精神富翁", "反内耗达人", "松弛感天花板"], desc: "你是互联网上最让人羡慕的那类人！体内自带净化器，任何焦虑和内耗传到你这里都会自动消散。你活得通透且自由，擅长用最舒服的姿势去过一生，搞钱只是你的副产品，享受当下才是你的终极王道。", s1: "98%", s2: "75%", s3: "88%", matchG: "人间清醒搞钱脑", matchB: "终极内耗小陀螺" },
            { title: "人间清醒搞钱脑", code: "INTJ", tags: ["智商随时在线", "搞钱特工", "超级理性"], desc: "恋爱脑在你这里根本不存在，你的大脑结构极其清晰，几乎所有的高效思考都围绕着‘如何实现降维打击’和‘资产增值’。看问题直击本质，冷酷中带着极强的个人魅力，是朋友圈里最靠谱的终极顾问。", s1: "45%", s2: "99%", s3: "95%", matchG: "纯血绝绝子气氛组", matchB: "纯情恋爱脑化身" },
            { title: "浓颜系社牛天花板", code: "ESFJ", tags: ["全场焦点", "快乐源泉", "情绪价值暴击"], desc: "只要有你在的地方，就绝对不会冷场！你就像一颗行走的多巴胺炸弹，无时无刻不在散发着光芒和能量。你极其擅长捕捉他人的情绪并给予最温暖的回馈，天生就适合站在聚光灯下发光发热。", s1: "80%", s2: "85%", s3: "50%", matchG: "清冷感断舍离i人", matchB: "阴郁抬杠艺术家" },
            { title: "清冷感断舍离i人", code: "ISTP", tags: ["微冷调美学", "高质量独处", "深度思考"], desc: "你散发着一种迷人的‘生人勿近’的高级感。比起喧嚣的社交，你更迷恋一杯咖啡、一本好书的独处时光。你对朋友的筛选极度严格，宁缺毋滥。你的灵魂深邃如银河，只有真正同频的人才能读懂你的温柔。", s1: "92%", s2: "68%", s3: "96%", matchG: "浓颜系社牛天花板", matchB: "低配话唠轰炸机" },
            { title: "发疯美学实践家", code: "ENTP", tags: ["自由灵魂", "拒绝被定义", "精神状态极前卫"], desc: "你的精神状态领先这个世界至少50年！你完全不在乎世俗的眼光，快乐就是你的唯一指针。面对不公和内卷，你选择用极具艺术感的方式‘发疯’来解构一切压力。幽默、毒舌却极其善良是你的底色。", s1: "95%", s2: "70%", s3: "90%", matchG: "天马行空梦想家", matchB: "老古董规矩守门人" },
            { title: "天马行空灵感制造机", code: "INFP", tags: ["脑洞大开", "审美艺术家", "拒绝平庸"], desc: "你的大脑是一个无穷无尽的奇妙点子库！你讨厌任何一成不变的公式化生活，生活中的一片落叶、一个微表情都能成为你创作的养分。虽然偶尔会被人说有点‘活在理想国’，但你这种高维的审美是无价的。", s1: "85%", s2: "78%", s3: "85%", matchG: "发疯美学实践家", matchB: "表格控强迫症晚期" },
            { title: "硬核执行力大猛人", code: "ESTJ", tags: ["狠人一枚", "说到做到", "自律狂魔"], desc: "你是绝对的行动派，在你的字典里没有‘拖延症’这三个字。立下的Flag对你来说就是必须攻克的山头。你的气场强大到让人退避三舍，但也因为无与伦比的靠谱度，成为了所有人最想抱大腿的终极战友。", s1: "60%", s2: "95%", s3: "90%", matchG: "佛系随缘小锦鲤", matchB: "画大饼口头大师" },
            { title: "佛系随缘小锦鲤", code: "ISFP", tags: ["运势绝佳", "得之我幸", "人间富贵花"], desc: "你完美地诠释了什么叫‘顺其自然’。你很少去强求什么，但神奇的是，好运总是会在关键时刻砸到你的头上。你心态好到爆炸，不争不抢反而让你成为了磁场最干净、最吸好运的移动人间大锦鲤。", s1: "96%", s2: "80%", s3: "70%", matchG: "硬核执行力大猛人", matchB: "过度焦虑制造机" }
        ];

        // 其余的动态补全代码库分配
        const mbtiTypes = ["INFJ", "ENTJ", "ISTJ", "ISFJ", "ESTP", "ESFP", "INTP", "ENFJ"];
        while(personalityData.length < 24) {
            const index = personalityData.length + 1;
            const randomCode = mbtiTypes[index % mbtiTypes.length];
            personalityData.push({
                title: `隐藏款精选人格 No.${index}`,
                code: randomCode,
                tags: [`高阶核心 #${index}`, "全网稀有", "独一无二"],
                desc: `这是大数据库为你匹配的第${index}种隐藏款社交人格。你在感性与理性之间找到了极其罕见的完美黄金分割点。在网络上你是敏锐的观察者，在现实中你是脚踏实地的生活艺术家。`,
                s1: `${Math.floor(Math.random() * 30) + 70}%`,
                s2: `${Math.floor(Math.random() * 40) + 60}%`,
                s3: `${Math.floor(Math.random() * 30) + 70}%`,
                matchG: "高质量同频挚友",
                matchB: "无效社交干扰源"
            });
        }

        let currentQuestionIndex = 0;
        let totalScore = 0;

        function startQuiz() {
            document.getElementById('welcome-view').classList.add('hidden');
            document.getElementById('quiz-view').classList.remove('hidden');
            showQuestion();
        }

        function showQuestion() {
            const currentQ = quizData[currentQuestionIndex];
            setTimeout(() => {
                const progressPercent = ((currentQuestionIndex + 1) / quizData.length) * 100;
                document.getElementById('progress-bar').style.width = `${progressPercent}%`;
            }, 50);
            
            document.getElementById('progress-text').innerText = `第 ${currentQuestionIndex + 1} / ${quizData.length} 题`;
            document.getElementById('question-title').innerText = currentQ.q;
            
            const optionsContainer = document.getElementById('options-container');
            optionsContainer.innerHTML = '';
            
            currentQ.a.forEach((answer) => {
                const btn = document.createElement('button');
                btn.className = "w-full text-left bg-slate-50 border border-slate-200 hover:border-[#ff2442] hover:bg-rose-50/30 active:scale-[0.99] transition-all p-4 rounded-xl text-sm font-medium text-slate-700 flex justify-between items-center cursor-pointer";
                btn.innerHTML = `<span>${answer.text}</span><span class="text-slate-300 group-hover:text-[#ff2442]">→</span>`;
                btn.onclick = () => selectAnswer(answer.score);
                optionsContainer.appendChild(btn);
            });
        }

        function selectAnswer(score) {
            totalScore += score;
            currentQuestionIndex++;
            
            if (currentQuestionIndex < quizData.length) {
                showQuestion();
            } else {
                document.getElementById('quiz-view').classList.add('hidden');
                document.getElementById('pay-view').classList.remove('hidden');
            }
        }

        function verifyPayment() {
            const amountInput = document.getElementById('pay-amount').value;
            const amount = parseFloat(amountInput);

            if (isNaN(amount)) {
                showToast("❌ 请输入您支付的真实金额进行验证哦~");
                return;
            }

            if (amount < 2) {
                showToast("⚠️ 付款金额需满 2 元才能解锁高级报告哦~");
                return;
            }

            showToast("🎉 解锁成功！正在精准构建人格画像...");
            
            setTimeout(() => {
                document.getElementById('pay-view').classList.add('hidden');
                document.getElementById('result-view').classList.remove('hidden');
                renderResult();
            }, 1500);
        }

        function renderResult() {
            const resultIndex = (totalScore * 7) % 24;
            const result = personalityData[resultIndex];

            document.getElementById('result-title').innerText = result.title;
            // 写入性格代码字母
            document.getElementById('result-code').innerText = result.code;
            document.getElementById('result-desc').innerText = result.desc;
            document.getElementById('match-good').innerText = result.matchG;
            document.getElementById('match-bad').innerText = result.matchB;

            const tagsContainer = document.getElementById('result-tags');
            tagsContainer.innerHTML = '';
            result.tags.forEach(tag => {
                const span = document.createElement('span');
                span.className = "bg-rose-50 text-[#ff2442] text-[11px] font-bold px-2.5 py-1 rounded-md border border-rose-100";
                span.innerText = tag;
                tagsContainer.appendChild(span);
            });

            document.getElementById('stat-1').innerText = result.s1;
            document.getElementById('stat-2').innerText = result.s2;
            document.getElementById('stat-3').innerText = result.s3;

            setTimeout(() => {
                document.getElementById('stat-bar-1').style.width = result.s1;
                document.getElementById('stat-bar-2').style.width = result.s2;
                document.getElementById('stat-bar-3').style.width = result.s3;
            }, 200);
        }

        function showToast(message) {
            const toast = document.getElementById('toast');
            toast.innerText = message;
            toast.style.opacity = '1';
            setTimeout(() => { toast.style.opacity = '0'; }, 2500);
        }
    </script>
</body>
</html>
