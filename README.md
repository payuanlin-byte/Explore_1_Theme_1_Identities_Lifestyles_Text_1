# Explore_1_Theme_1_Identities_Lifestyles_Text_1
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
            line-height: 1.8;
            padding: 20px;
            display: flex;
            justify-content: center;
        }
        .container {
            max-width: 600px;
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }
        h1 {
            font-size: 24px;
            text-align: center;
            color: #1a1a1a;
            border-bottom: 2px solid #EEE;
            padding-bottom: 10px;
        }
        p {
            font-size: 18px;
            text-indent: 2em;
        }
        /* 核心詞彙的樣式：帶有虛線下劃線，提示可點擊 */
        .vocab {
            color: #0066CC;
            border-bottom: 2px dashed #0066CC;
            cursor: pointer;
            position: relative;
            font-weight: bold;
            transition: background-color 0.2s;
        }
        .vocab:hover {
            background-color: #E6F0FA;
        }
        /* 彈窗（Tooltip）的樣式 */
        #tooltip {
            display: none;
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            background: #333;
            color: white;
            padding: 15px 25px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            text-align: center;
            z-index: 1000;
            font-size: 16px;
            animation: fadeIn 0.3s;
        }
        .pinyin { color: #4CAF50; font-weight: bold; margin-bottom: 5px;}
        .english { color: #FFF; }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translate(-50%, 20px); }
            to { opacity: 1; transform: translate(-50%, 0); }
        }

        /* 底部口語任務區 */
        .task-box {
            margin-top: 40px;
            background-color: #FFF9E6;
            padding: 20px;
            border-left: 5px solid #FFA500;
            border-radius: 5px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>💳 扔掉錢包！「靠臉吃飯」的日子來了！</h1>
    
    <p>中秋節一放假，我就從英國飛到杭州<span class="vocab" data-pinyin="tǐ yàn" data-eng="to experience">體驗</span>了一次靠臉吃飯的新綠色<span class="vocab" data-pinyin="xiāo fèi" data-eng="consumption">消費</span>生活方式。到機場後，不用再擔心排隊了，因為<span class="vocab" data-pinyin="shuā liǎn" data-eng="facial scan">刷臉</span><span class="vocab" data-pinyin="rù jìng" data-eng="enter a country">入境</span>和登機只需2-5秒。</p>

    <p>出機場後，我來到全球首個刷臉<span class="vocab" data-pinyin="zhī fù" data-eng="payment / to pay">支付</span>的肯德基餐廳吃早餐。點餐時，大約只有1-2秒，機器人就完成了人臉<span class="vocab" data-pinyin="shí bié" data-eng="recognition">識別</span>，整個過程不到10秒，真是又快又方便。</p>

    <p>我覺得這個時代變化太快，當我還在<span class="vocab" data-pinyin="jīng tàn" data-eng="marvel at">驚嘆</span>刷手機帶來的改變時，一場「扔掉手機」的刷臉時代又開始了！我認為年輕人要<span class="vocab" data-pinyin="jī jí" data-eng="actively">積極</span><span class="vocab" data-pinyin="jiē shòu" data-eng="accept">接受</span>改變，不能做不願接受<span class="vocab" data-pinyin="chuàng xīn" data-eng="innovation">創新</span>的人。</p>

    <!-- 輸出閉環：口語任務 -->
    <div class="task-box">
        <h3>🎙️ 說說看 (Say it out loud)</h3>
        <p style="font-size: 16px; text-indent: 0;">請用剛才點擊過的詞彙（如：<strong>體驗、支付、創新</strong>），告訴同桌你最想嘗試哪一種「無現金」活動？</p>
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
            // 獲取預設的拼音和英文
            const pinyin = this.getAttribute('data-pinyin');
            const eng = this.getAttribute('data-eng');
            
            // 填充彈窗內容
            ttPinyin.textContent = pinyin;
            ttEnglish.textContent = eng;
            
            // 顯示彈窗
            tooltip.style.display = 'block';
            
            // 點擊空白處或3秒後自動隱藏
            setTimeout(() => {
                tooltip.style.display = 'none';
            }, 3000);
            
            e.stopPropagation();
        });
    });

    // 點擊頁面其他地方隱藏彈窗
    document.body.addEventListener('click', () => {
        tooltip.style.display = 'none';
    });
</script>

</body>
</html>
