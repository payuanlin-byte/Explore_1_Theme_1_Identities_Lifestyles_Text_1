<!DOCTYPE html>
<html lang="zh-HK">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>互動閱讀：《靠臉吃飯》</title>
    <style>
        body {
            font-family: 'Noto Sans HK', 'PingFang HK', 'Microsoft YaHei', sans-serif;
            background-color: #F5F5F7;
            color: #333333;
            line-height: 2.0;
            padding: 20px;
            display: flex;
            justify-content: center;
        }
        .container {
            max-width: 700px;
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }
        h1 {
            font-size: 26px;
            text-align: center;
            color: #1a1a1a;
            border-bottom: 2px solid #EEE;
            padding-bottom: 15px;
            margin-bottom: 10px;
        }
        .meta-info {
            text-align: center;
            color: #888;
            font-size: 14px;
            margin-bottom: 30px;
        }
        p {
            font-size: 18px;
            text-indent: 2em;
            margin-bottom: 15px;
            text-align: justify;
        }
        
        /* 詞彙交互樣式基類 */
        .vocab {
            cursor: pointer;
            position: relative;
            font-weight: bold;
            border-bottom-width: 2px;
            border-bottom-style: dashed;
            transition: background-color 0.2s, color 0.2s;
            padding: 0 2px;
            border-radius: 4px;
        }

        /* 三層分類：藍色（目標）、綠色（高階）、紅色（邏輯） */
        .vocab-blue { color: #0066CC; border-bottom-color: #0066CC; }
        .vocab-blue:hover { background-color: #E6F0FA; }
        
        .vocab-green { color: #008800; border-bottom-color: #008800; }
        .vocab-green:hover { background-color: #E6F9E6; }
        
        .vocab-red { color: #CC0000; border-bottom-color: #CC0000; }
        .vocab-red:hover { background-color: #FAE6E6; }

        /* 動態彈窗（Tooltip）樣式 */
        #tooltip {
            display: none;
            position: fixed;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            background: #333333;
            color: white;
            padding: 15px 30px;
            border-radius: 12px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
            text-align: center;
            z-index: 1000;
            font-size: 18px;
            animation: fadeIn 0.2s ease-out;
            pointer-events: none; /* 防止遮擋點擊 */
        }
        .pinyin { color: #4CAF50; font-weight: bold; margin-bottom: 5px; font-size: 20px;}
        .english { color: #FFFFFF; font-size: 16px;}
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translate(-50%, 20px); }
            to { opacity: 1; transform: translate(-50%, 0); }
        }

        /* 底部口語任務區：建立輸入到輸出的閉環 */
        .task-box {
            margin-top: 50px;
            background-color: #FFF9E6;
            padding: 25px;
            border-left: 6px solid #FFA500;
            border-radius: 8px;
        }
        .task-box h3 {
            margin-top: 0;
            color: #D35400;
            font-size: 20px;
        }
        .task-box ul {
            padding-left: 20px;
            margin-bottom: 0;
        }
        .task-box li {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>＜課文一＞ 靠臉吃飯</h1>
    <div class="meta-info">2018年9月8日 | 星期天 | 晴</div>
    
    <p>從今天起要看好我的臉，這才是我真正的身份證！因為<span class="vocab vocab-blue" data-pinyin="chéng" data-eng="to take (transportation)">乘</span>火車、坐飛機全<span class="vocab vocab-blue" data-pinyin="kào" data-eng="to rely on">靠</span>一張臉！<span class="vocab vocab-blue" data-pinyin="kào" data-eng="to rely on">靠</span>臉吃飯的日子來了！</p>

    <p>中秋節一放假，我就從英國飛到杭州<span class="vocab vocab-blue" data-pinyin="tǐ yàn" data-eng="to experience">體驗</span>了一次<span class="vocab vocab-blue" data-pinyin="kào" data-eng="to rely on">靠</span>臉吃飯的新綠色<span class="vocab vocab-blue" data-pinyin="xiāo fèi" data-eng="consumption">消費</span>生活方式。到機場後，不用再擔心排隊了，因為<span class="vocab vocab-blue" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span><span class="vocab vocab-blue" data-pinyin="rù jìng" data-eng="to enter a country">入境</span>和<span class="vocab vocab-blue" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span><span class="vocab vocab-blue" data-pinyin="dēng jī" data-eng="to board a plane">登機</span>一樣只需2-5秒。<span class="vocab vocab-red" data-pinyin="zhǐ yào" data-eng="as long as">只要</span>把簽證/護照放到機器上一刷，門<span class="vocab vocab-red" data-pinyin="jiù" data-eng="then">就</span>開了。<span class="vocab vocab-red" data-pinyin="bù jǐn rú cǐ" data-eng="not only that">不僅如此</span>，所有路口還都沒有人！<span class="vocab vocab-blue" data-pinyin="huà zhuāng" data-eng="to put on makeup">化妝</span>女士和老外也不用擔心，一樣<span class="vocab vocab-blue" data-pinyin="zhǔn què de" data-eng="accurately">準確地</span>刷他們的臉。<span class="vocab vocab-red" data-pinyin="zhè yàng yī lái" data-eng="in this way">這樣一來</span>，<span class="vocab vocab-red" data-pinyin="jí shǐ" data-eng="even if">即使</span>是壞人<span class="vocab vocab-red" data-pinyin="yě" data-eng="also">也</span>跑不了，因為他們一<span class="vocab vocab-blue" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span>，機器<span class="vocab vocab-red" data-pinyin="jiù" data-eng="then">就</span>馬上<span class="vocab vocab-blue" data-pinyin="xiǎng" data-eng="to sound / ring">響</span>起來。</p>

    <p>出機場後，我來到<span class="vocab vocab-blue" data-pinyin="quán qiú" data-eng="global">全球</span><span class="vocab vocab-blue" data-pinyin="shǒu gè" data-eng="the first">首個</span><span class="vocab vocab-blue" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span><span class="vocab vocab-blue" data-pinyin="zhī fù" data-eng="payment / to pay">支付</span>的<span class="vocab vocab-blue" data-pinyin="Kěn dé jī" data-eng="KFC">肯德基</span>餐廳吃早餐。點餐時，大約只有1-2秒，機器人<span class="vocab vocab-red" data-pinyin="jiù" data-eng="then">就</span>完成了人臉<span class="vocab vocab-blue" data-pinyin="shí bié" data-eng="recognition">識別</span>，整個<span class="vocab vocab-blue" data-pinyin="zhī fù" data-eng="payment">支付</span><span class="vocab vocab-blue" data-pinyin="guò chéng" data-eng="process">過程</span>不到10秒，真是又快又方便。<span class="vocab vocab-red" data-pinyin="bù guò" data-eng="however">不過</span>，如果是首次使用，要先在支付寶上<span class="vocab vocab-blue" data-pinyin="kāi tōng" data-eng="to activate / open">開通</span><span class="vocab vocab-blue" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span><span class="vocab vocab-blue" data-pinyin="gōng néng" data-eng="function">功能</span>。</p>

    <p>接下來搭公車、坐<span class="vocab vocab-blue" data-pinyin="dí shì" data-eng="taxi">的士</span>、騎自行車都<span class="vocab vocab-blue" data-pinyin="kào" data-eng="to rely on">靠</span><span class="vocab vocab-blue" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span>來<span class="vocab vocab-blue" data-pinyin="jiě jué" data-eng="to solve">解決</span>。<span class="vocab vocab-red" data-pinyin="bù zhǐ shì" data-eng="not only">不只是</span><span class="vocab vocab-blue" data-pinyin="zhī fù" data-eng="to pay">支付</span><span class="vocab vocab-blue" data-pinyin="jiāo tōng gōng jù" data-eng="transportation">交通工具</span>的<span class="vocab vocab-blue" data-pinyin="fèi yòng" data-eng="expense / cost">費用</span>，買飲料、看電影、吃晚餐、訂機票<span class="vocab vocab-red" data-pinyin="dōu néng" data-eng="can all">都能</span><span class="vocab vocab-blue" data-pinyin="kào" data-eng="to rely on">靠</span>臉<span class="vocab vocab-blue" data-pinyin="zhī fù" data-eng="to pay">支付</span>，這就是中國人的日常生活，<span class="vocab vocab-blue" data-pinyin="wú xiàn jīn shì" data-eng="cashless">無現金式</span>綠色<span class="vocab vocab-blue" data-pinyin="xiāo fèi" data-eng="consumption">消費</span>生活方式已經在中國城市中<span class="vocab vocab-blue" data-pinyin="qiāo qiāo de" data-eng="quietly">悄悄地</span><span class="vocab vocab-blue" data-pinyin="liú xíng" data-eng="popular">流行</span>。</p>

    <p>這次<span class="vocab vocab-blue" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span><span class="vocab vocab-blue" data-pinyin="tǐ yàn" data-eng="experience">體驗</span>，真的很有趣，也<span class="vocab vocab-green" data-pinyin="lìng rén nán wàng" data-eng="unforgettable">令人難忘</span>。科技的進步正悄悄改變我們傳統的生活方式。我覺得這個<span class="vocab vocab-blue" data-pinyin="shí dài" data-eng="era">時代</span>變化太快，當我還在<span class="vocab vocab-blue" data-pinyin="jīng tàn" data-eng="to marvel at">驚嘆</span>刷手機帶來的改變時，一場「<span class="vocab vocab-blue" data-pinyin="rēng diào" data-eng="to throw away">扔掉</span>手機」的<span class="vocab vocab-blue" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span><span class="vocab vocab-blue" data-pinyin="shí dài" data-eng="era">時代</span>又開始了！</p>

    <p>我認為作為年輕人，我們要<span class="vocab vocab-blue" data-pinyin="jī jí" data-eng="actively">積極</span><span class="vocab vocab-blue" data-pinyin="jiē shòu" data-eng="to accept">接受</span>新生活方式的改變。這個<span class="vocab vocab-blue" data-pinyin="shí dài" data-eng="era">時代</span>，最可怕的不是那些不願<span class="vocab vocab-blue" data-pinyin="jiē shòu" data-eng="to accept">接受</span><span class="vocab vocab-blue" data-pinyin="chuàng xīn" data-eng="innovation">創新</span>的人，而是不願改變的人，明明手機可以<span class="vocab vocab-blue" data-pinyin="zhuǎn zhàng" data-eng="to transfer money">轉賬</span>，<span class="vocab vocab-blue" data-pinyin="piān yào" data-eng="to insist on">偏要</span>去銀行拿號碼排隊；明明手機可以<span class="vocab vocab-blue" data-pinyin="zhī fù" data-eng="to pay">支付</span>，<span class="vocab vocab-blue" data-pinyin="piān yào" data-eng="to insist on">偏要</span>用現金讓別人找零錢；明明手機可以買票，<span class="vocab vocab-blue" data-pinyin="piān yào" data-eng="to insist on">偏要</span>去火車站排隊。</p>

    <!-- 輸出閉環：口語任務 -->
    <div class="task-box">
        <h3>🗣️ 即時挑戰 (Speaking Challenge)</h3>
        <p style="font-size: 16px; text-indent: 0; color: #555;">讀完文章後，請挑選 <strong>1 個紅色的邏輯連詞</strong> 和 <strong>2 個藍色/綠色的詞彙</strong>，造一個完整的句子。例如：</p>
        <ul style="font-size: 16px; color: #555;">
            <li><strong>即使</strong>忘記帶錢包，我也能<strong>體驗</strong>無現金的<strong>消費</strong>。</li>
        </ul>
    </div>
</div>

<!-- 用於顯示拼音和英文的動態彈窗 -->
<div id="tooltip">
    <div class="pinyin" id="tt-pinyin"></div>
    <div class="english" id="tt-english"></div>
</div>

<script>
    const vocabs = document.querySelectorAll('.vocab');
    const tooltip = document.getElementById('tooltip');
    const ttPinyin = document.getElementById('tt-pinyin');
    const ttEnglish = document.getElementById('tt-english');

    vocabs.forEach(vocab => {
        vocab.addEventListener('click', function(e) {
            const pinyin = this.getAttribute('data-pinyin');
            const eng = this.getAttribute('data-eng');
            
            ttPinyin.textContent = pinyin;
            ttEnglish.textContent = eng;
            
            tooltip.style.display = 'block';
            
            // 點擊後 3 秒自動隱藏，保護閱讀流暢度
            setTimeout(() => {
                tooltip.style.display = 'none';
            }, 3000);
            
            e.stopPropagation();
        });
    });

    document.body.addEventListener('click', () => {
        tooltip.style.display = 'none';
    });
</script>

</body>
</html>
