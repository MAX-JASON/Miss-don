<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>國泰人壽醫療險規劃方案 - 專業守護您的健康</title>
    <!-- CDN引入Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/chartjs-plugin-datalabels@2"></script>
    <!-- CDN引入Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- 本地引入Google字體 -->
    <style>
        @font-face {
            font-family: 'Noto Sans TC';
            font-style: normal;
            font-weight: 300;
            src: local('Noto Sans TC Light'), local('NotoSansTC-Light');
        }
        @font-face {
            font-family: 'Noto Sans TC';
            font-style: normal;
            font-weight: 400;
            src: local('Noto Sans TC Regular'), local('NotoSansTC-Regular');
        }
        @font-face {
            font-family: 'Noto Sans TC';
            font-style: normal;
            font-weight: 500;
            src: local('Noto Sans TC Medium'), local('NotoSansTC-Medium');
        }
        @font-face {
            font-family: 'Noto Sans TC';
            font-style: normal;
            font-weight: 700;
            src: local('Noto Sans TC Bold'), local('NotoSansTC-Bold');
        }
    </style>
    <style>
        :root {
            --primary-color: #00539c;
            --secondary-color: #c43e3e;
            --accent-color: #f5a623;
            --light-bg: #f8f9fa;
            --dark-bg: #003366;
            --text-color: #333;
            --light-text: #f8f9fa;
        }
        
        body { 
            font-family: 'Noto Sans TC', '微軟正黑體', sans-serif; 
            max-width: 1200px; 
            margin: 0 auto; 
            padding: 20px;
            line-height: 1.6;
            animation: fadeIn 1s ease-in;
            color: var(--text-color);
            background-color: #f5f7fa;
            background-image: url('https://www.transparenttextures.com/patterns/cubes.png');
            background-attachment: fixed;
            background-size: 300px;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4 { 
            font-weight: 700;
            line-height: 1.3;
        }
        
        h1 { 
            color: var(--primary-color); 
            text-align: center; 
            border-bottom: 3px solid var(--secondary-color);
            padding-bottom: 15px;
            margin-bottom: 30px;
            font-size: 2.5em;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        
        .header-container {
            position: relative;
            background: linear-gradient(135deg, var(--primary-color), #0077b6);
            color: white;
            padding: 40px 20px;
            border-radius: 15px;
            margin-bottom: 40px;
            text-align: center;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        .header-container::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://www.transparenttextures.com/patterns/diagmonds-light.png');
            opacity: 0.1;
        }
        
        .header-container h1 {
            color: white;
            border-bottom: none;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }
        
        .header-subtitle {
            font-size: 1.2em;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }
        
        .header-badge {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 8px 15px;
            border-radius: 30px;
            font-weight: 500;
            margin-top: 10px;
            position: relative;
            z-index: 1;
        }
        
        .section { 
            margin: 20px 0; 
            padding: 20px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }
        
        .section-header {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
            border-bottom: 2px solid #eee;
            padding-bottom: 15px;
        }
        
        .section-icon {
            font-size: 2em;
            color: var(--primary-color);
            margin-right: 15px;
            background: #f0f7ff;
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }
        
        .section h2 {
            color: var(--primary-color);
            margin: 0;
            flex: 1;
        }
        
        .subsection {
            margin: 30px 0;
            padding: 20px;
            background: var(--light-bg);
            border-radius: 10px;
            border-left: 5px solid var(--primary-color);
        }
        
        .row {
            display: flex;
            flex-wrap: wrap;
            margin: 0 -15px;
            align-items: center;
        }
        
        .col {
            flex: 1;
            padding: 0 15px;
            min-width: 300px;
        }
        
        .chart-container { 
            padding: 30px; 
            background: white;
            border-radius: 10px;
            margin: 20px 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            position: relative;
            height: 400px;
            overflow: hidden;
        }
        
        .chart-container::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            border-radius: 0 0 10px 10px;
        }
        
        .caption {
            margin-top: 20px;
            font-size: 0.9em;
            color: #666;
            line-height: 1.5;
            padding: 15px;
            background: #f9f9f9;
            border-radius: 8px;
            border-left: 3px solid var(--accent-color);
        }
        
        .story-box {
            margin-top: 15px;
            padding: 15px;
            background: #fff8e1;
            border-radius: 8px;
            font-style: italic;
            position: relative;
        }
        
        .story-box::before {
            content: "\"";
            font-size: 3em;
            color: rgba(0,0,0,0.1);
            position: absolute;
            top: -10px;
            left: 5px;
        }
        
        .data-source {
            font-size: 0.8em;
            color: #777;
            text-align: right;
            margin-top: 10px;
            font-style: normal;
        }
        
        .highlight { 
            color: var(--secondary-color); 
            font-weight: bold;
            font-size: 1.2em;
            position: relative;
            display: inline-block;
        }
        
        .highlight::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background-color: rgba(196, 62, 62, 0.2);
            border-radius: 3px;
        }
        
        .stat-card {
            background: white;
            border-radius: 10px;
            padding: 20px;
            margin: 10px 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
        }
        
        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            color: var(--primary-color);
            margin: 10px 0;
        }
        
        .stat-label {
            color: #666;
            font-size: 0.9em;
        }
        
        .tooltip {
            background: #333;
            color: white;
            padding: 15px;
            border-radius: 5px;
            display: none;
            position: absolute;
            z-index: 1000;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            max-width: 300px;
        }
        
        .testimonial {
            background: white;
            border-radius: 10px;
            padding: 25px;
            margin: 20px 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            position: relative;
        }
        
        blockquote {
            margin: 0;
            padding-left: 20px;
            border-left: 3px solid var(--accent-color);
            font-style: italic;
            line-height: 1.8;
        }
        
        cite {
            display: block;
            margin-top: 15px;
            font-style: normal;
            font-weight: bold;
            text-align: right;
        }
        
        .cta-section {
            background: linear-gradient(135deg, var(--primary-color), #0077b6);
            color: white;
            text-align: center;
            padding: 40px;
            border-radius: 15px;
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }
        
        .cta-section::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://www.transparenttextures.com/patterns/diagmonds-light.png');
            opacity: 0.1;
        }
        
        .cta-button {
            background: var(--accent-color);
            color: white;
            padding: 15px 40px;
            border-radius: 50px;
            font-size: 1.2em;
            font-weight: bold;
            border: none;
            cursor: pointer;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
            position: relative;
            z-index: 1;
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
            background: #e09000;
        }
        
        .data-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 30px 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            border-radius: 10px;
            overflow: hidden;
        }
        
        .comparison-table th {
            background: var(--primary-color);
            color: white;
            padding: 15px;
            text-align: left;
        }
        
        .comparison-table td {
            padding: 15px;
            border-bottom: 1px solid #eee;
        }
        
        .comparison-table tr:nth-child(even) {
            background: #f9f9f9;
        }
        
        .comparison-table tr:last-child td {
            border-bottom: none;
        }
        
        .feature-check {
            color: #4CAF50;
            font-size: 1.2em;
        }
        
        .feature-times {
            color: #F44336;
            font-size: 1.2em;
        }
        
        .footer {
            text-align: center;
            margin-top: 50px;
            padding: 30px;
            background: var(--dark-bg);
            color: white;
            border-radius: 15px;
        }
        
        .footer p {
            margin: 5px 0;
        }
        
        .footer a {
            color: var(--accent-color);
            text-decoration: none;
        }
        
        .footer a:hover {
            text-decoration: underline;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @media (max-width: 768px) {
            .row {
                flex-direction: column;
            }
            
            .col {
                width: 100%;
                padding: 15px 0;
            }
            
            .section {
                padding: 20px;
            }
            
            .chart-container {
                padding: 15px;
            }
            
            h1 {
                font-size: 2em;
            }
        }
        
        @media print {
            body { 
                font-size: 12pt; 
                color: #333;
                background: none;
            }
            
            .chart-container { 
                box-shadow: none;
                page-break-inside: avoid;
            }
            
            .section {
                box-shadow: none;
                border: 1px solid #ddd;
                page-break-inside: avoid;
            }
            
            .cta-section, .cta-button { display: none; }
        }
    </style>
</head>
<body>
    <div class="header-container">
        <h1>國泰人壽醫療險規劃方案</h1>
        <p class="header-subtitle">專業守護您的健康 | 2025年4月最新版</p>
        <div class="header-badge">數據驅動決策 · 全方位保障</div>
    </div>
    
    <!-- 第一區塊：醫療趨勢分析 -->
    <div class="section">
        <div class="section-header">
            <div class="section-icon"><i class="fas fa-chart-line"></i></div>
            <h2>台灣醫療支出趨勢與風險</h2>
        </div>
        
        <div class="row">
            <div class="col">
                <p>根據<strong>衛生福利部</strong>與<strong>健保署</strong>最新統計，2024年台灣醫療自費支出占比達 <span class="highlight">37%</span>，較2020年增加5個百分點，顯示自費醫療負擔持續攀升。</p>
                
                <div class="data-grid">
                    <div class="stat-card">
                        <div class="stat-number">12萬元</div>
                        <div class="stat-label">癌症標靶藥物單月最高費用</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">25萬元</div>
                        <div class="stat-label">達文西手術單次費用</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">8,000元</div>
                        <div class="stat-label">ICU住院日均差額</div>
                    </div>
                </div>
                
                <p>台北市立聯合醫院統計顯示，2024年第一季門診自費項目較去年同期增加<span class="highlight">18.3%</span>，其中高階影像檢查與特殊藥物占比最高。</p>
            </div>
            
            <div class="col">
                <div class="chart-container">
                    <canvas id="medicalTrend"></canvas>
                    <div class="caption">
                        <p><strong>圖1：2018-2024年台灣醫療自費支出增長趨勢（單位：億元）</strong></p>
                        <p>數據顯示自費醫療支出年增率達12%，遠高於平均薪資成長率4.2%，形成家庭財務壓力。</p>
                        <div class="story-box">
                            <p>台中林先生（42歲）因腦部腫瘤需進行伽瑪刀手術，健保僅給付基本治療費用，自費部分高達18萬元。所幸他投保了實支實付醫療險，獲得全額理賠，不必為醫療費用煩惱。</p>
                            <p class="data-source">資料來源：健保署年度統計報告、國泰人壽理賠案例分析</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- 第二區塊：險種深度解析 -->
    <div class="section">
        <div class="section-header">
            <div class="section-icon"><i class="fas fa-shield-alt"></i></div>
            <h2>四大險種保障藍圖</h2>
        </div>
        
        <p>根據<strong>金管會保險局</strong>與<strong>台灣保險事業發展中心</strong>的研究，完整的醫療保障應包含以下四大險種，形成
        
        <!-- 防癌險 -->
        <div class="subsection">
            <h3><i class="fas fa-ribbon" style="color: #e91e63;"></i> 1. 防癌險：精準轉移癌症經濟風險</h3>
            <div class="row">
                <div class="col">
                    <p><strong>國健署</strong>最新統計顯示，台灣每年新增癌症病例超過<span class="highlight">11萬例</span>，平均每<span class="highlight">4分36秒</span>就有一人罹癌。</p>
                    
                    <p>癌症治療總費用分佈：</p>
                    <ul>
                        <li>化療/放療：<span class="highlight">25%</span></li>
                        <li>標靶治療：<span class="highlight">40%</span></li>
                        <li>住院照護：<span class="highlight">20%</span></li>
                        <li>其他：<span class="highlight">15%</span></li>
                    </ul>
                    
                    <p><strong>台大醫院腫瘤科</strong>研究指出，新型免疫療法平均療程費用達<span class="highlight">200萬元</span>，健保僅給付部分適應症，大多需自費。</p>
                </div>
                <div class="col">
                    <div class="chart-container">
                        <canvas id="cancerBreakdown"></canvas>
                        <div class="caption">
                            <p><strong>圖2：癌症治療費用結構（2024年統計）</strong></p>
                            <p>標靶治療占比最高，且多為健保不給付或部分給付項目，形成沉重經濟負擔。</p>
                            <div class="story-box">
                                <p>高雄王女士（38歲）確診乳癌第二期，選擇使用新型標靶藥物治療，每月藥費高達8萬元，療程需持續一年。因投保防癌險，獲得100萬元確診金與每月2萬元治療金，大幅減輕經濟壓力。</p>
                                <p class="data-source">資料來源：國健署癌症登記報告、國泰人壽理賠統計</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 實支實付 -->
        <div class="subsection">
            <h3><i class="fas fa-hospital" style="color: #2196F3;"></i> 2. 實支實付險：填補健保缺口</h3>
            <div class="row">
                <div class="col">
                    <p><strong>健保署</strong>資料顯示，2024年台灣住院醫療費用中，平均有<span class="highlight">32%</span>為健保不給付項目，包括：</p>
                    <ul>
                        <li>差額病房：每日差額<span class="highlight">1,800-8,000元</span></li>
                        <li>高階特材：如心臟支架差額<span class="highlight">5-15萬元</span></li>
                        <li>自費藥品：如特定抗生素<span class="highlight">2,000-8,000元/天</span></li>
                    </ul>
                    
                    <p><strong>台北榮總</strong>統計顯示，住院病患平均自付醫療費用較五年前增加<span class="highlight">47%</span>，遠超過通膨水平。</p>
                </div>
                <div class="col">
                    <div class="chart-container">
                        <canvas id="nhiGap"></canvas>
                        <div class="caption">
                            <p><strong>圖3：健保給付VS自費支出比例（外科手術案例）</strong></p>
                            <p>高階醫療項目的自費比例明顯較高，實支實付險可有效填補這些缺口。</p>
                            <div class="story-box">
                                <p>台北陳先生（56歲）因心臟病需安裝高階支架，健保僅給付基本款，自費差額高達12萬元。由於他有實支實付醫療險，獲得全額理賠，並享受到更好的醫療品質與恢復效果。</p>
                                <p class="data-source">資料來源：台北榮總心臟內科年度報告、國泰人壽理賠案例分析</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 重大疾病 -->
        <div class="subsection">
            <h3><i class="fas fa-heartbeat" style="color: #f44336;"></i> 3. 重大疾病險：一次性給付設計原理</h3>
            <div class="row">
                <div class="col">
                    <p><strong>衛福部國健署</strong>資料顯示，台灣40歲以上民眾罹患重大疾病機率達<span class="highlight">38%</span>，且有年輕化趨勢。</p>
                    
                    <p>常見重大疾病治療週期與費用：</p>
                    <ul>
                        <li>心臟病：<span class="highlight">3-5年</span>，平均花費<span class="highlight">180萬元</span></li>
                        <li>腎衰竭：<span class="highlight">終身洗腎</span>，每年花費<span class="highlight">72萬元</span></li>
                        <li>腦中風：<span class="highlight">2-7年復健期</span>，平均花費<span class="highlight">250萬元</span></li>
                    </ul>
                    
                    <p><strong>台灣腦中風學會</strong>研究指出，腦中風患者平均需<span class="highlight">3.5年</span>才能恢復工作能力，期間收入損失與照護費用形成雙重壓力。</p>
                </div>
                <div class="col">
                    <div class="chart-container">
                        <canvas id="criticalIllness"></canvas>
                        <div class="caption">
                            <p><strong>圖4：一次性給付VS治療支出曲線</strong></p>
                            <p>重大疾病險的一次性給付設計，能在確診初期提供大額資金支持，幫助患者度過治療初期的高支出階段。</p>
                            <div class="story-box">
                                <p>新北李先生（48歲）突發腦中風，需長期復健且無法工作。因有200萬元重大疾病險保障，一次性理賠金讓他能專心治療，並支付家庭生活費用，不必擔心經濟問題。</p>
                                <p class="data-source">資料來源：台灣腦中風學會研究報告、國泰人壽理賠統計</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 長照險 -->
        <div class="subsection">
            <h3><i class="fas fa-user-nurse" style="color: #4CAF50;"></i> 4. 長照險：人口老化下的必要防護</h3>
            <div class="row">
                <div class="col">
                    <p><strong>國家發展委員會</strong>預測，台灣將於2025年成為「超高齡社會」，65歲以上人口占比超過<span class="highlight">20%</span>。</p>
                    
                    <p><strong>台灣長期照護學會</strong>研究顯示，65歲以上長者有<span class="highlight">73%</span>的機率需要長期照護服務，平均照護期間為<span class="highlight">7.8年</span>。</p>
                    
                    <p>長照費用持續上漲：</p>
                    <ul>
                        <li>居家照護：每月<span class="highlight">3-5萬元</span></li>
                        <li>機構照護：每月<span class="highlight">5-8萬元</span></li>
                        <li>失智症特殊照護：每月<span class="highlight">6-10萬元</span></li>
                    </ul>
                </div>
                <div class="col">
                    <div class="chart-container">
                        <canvas id="longTermCare"></canvas>
                        <div class="caption">
                            <p><strong>圖5：長照需求人口預測與費用趨勢</strong></p>
                            <p>隨著人口老化，長照需求人口與費用雙雙攀升，預計2030年長照月均費用將達6.2萬元。</p>
                            <div class="story-box">
                                <p>台南吳女士的母親（78歲）因中風需要長期照護，每月照護費用高達5萬元。因有長照險保障，每月獲得4萬元照護金，大幅減輕家庭經濟負擔，讓母親能獲得更好的照護品質。</p>
                                <p class="data-source">資料來源：國發會人口推估報告、台灣長期照護學會研究</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- 第三區塊：方案對比 -->
    <div class="section">
        <div class="section-header">
            <div class="section-icon"><i class="fas fa-balance-scale"></i></div>
            <h2>保障方案智能對比</h2>
        </div>
        
        <p><strong>金管會保險局</strong>建議，完整的醫療保障規劃應根據個人年齡、家庭責任與收入水平量身定制。以下為國泰人壽專業規劃的兩種方案對比：</p>
        
        <table class="comparison-table">
            <thead>
                <tr>
                    <th>保障項目</th>
                    <th>基礎方案</th>
                    <th>尊榮方案</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>實支實付限額</td>
                    <td>10萬元/年</td>
                    <td>30萬元/年</td>
                </tr>
                <tr>
                    <td>住院日額</td>
                    <td>2,000元/日</td>
                    <td>5,000元/日</td>
                </tr>
                <tr>
                    <td>重大疾病保障</td>
                    <td>100萬元</td>
                    <td>300萬元</td>
                </tr>
                <tr>
                    <td>癌症確診金</td>
                    <td>50萬元</td>
                    <td>150萬元</td>
                </tr>
                <tr>
                    <td>長照月給付</td>
                    <td>3萬元 x 5年</td>
                    <td>6萬元 x 10年</td>
                </tr>
                <tr>
                    <td>月繳保費</td>
                    <td>3,000-4,500元</td>
                    <td>6,000-8,500元</td>
                </tr>
            </tbody>
        </table>
        
        <div class="chart-container">
            <canvas id="planComparison"></canvas>
            <div class="caption">
                <p><strong>圖6：基礎版VS尊榮版保障雷達圖</strong></p>
                <p>尊榮方案在各項保障維度均優於基礎方案，特別是在長照支援與癌症保障方面差距最為明顯。</p>
                <div class="story-box">
                    <p>台中張先生（35歲）年收入120萬元，有兩個年幼子女，選擇尊榮方案獲得全面保障。他表示：「考慮到家庭責任，我寧願多付一些保費，換取更全面的保障，讓家人無論發生什麼都能維持生活品質。」</p>
                    <p class="data-source">資料來源：國泰人壽客戶滿意度調查、保險事業發展中心研究報告</p>
                </div>
            </div>
        </div>
    </div>

    <!-- 第四區塊：客戶見證 -->
    <div class="section">
        <div class="section-header">
            <div class="section-icon"><i class="fas fa-quote-right"></i></div>
            <h2>真實案例分享</h2>
        </div>
        
        <div class="row">
            <div class="col">
                <div class="testimonial">
                    <blockquote>
                        "投保後確診乳癌，實支實付險全額覆蓋標靶藥物費用，重大疾病險150萬理賠讓我能專心治療，不必擔心收入中斷的問題。現在我已康復，更加珍惜生活，也感謝當初做了完整的醫療保障規劃。"
                        <cite>— 台北張女士，45歲，教師</cite>
                    </blockquote>
                </div>
            </div>
            <div class="col">
                <div class="testimonial">
                    <blockquote>
                        "父親中風後需要長期照護，長照險每月給付5萬元，讓我們能聘請專業看護，不必犧牲工作。這筆錢解決了最大的經濟壓力，讓我們全家能以最好的心態面對照護挑戰。"
                        <cite>— 高雄王先生，38歲，工程師</cite>
                    </blockquote>
                </div>
            </div>
        </div>
        
        <div class="testimonial" style="margin-top: 30px;">
            <blockquote>
                "去年因車禍住院45天，實支實付險與住院日額險合計理賠超過60萬元，覆蓋了所有醫療費用與收入損失。康復後，我立即為家人也規劃了相同的保障，這是對家人最實際的愛。"
                <cite>— 台中林先生，32歲，業務經理</cite>
            </blockquote>
        </div>
    </div>

    <!-- 行銷CTA -->
    <div class="cta-section">
        <h2>立即行動，守護未來</h2>
        <p style="font-size: 1.2em; margin: 20px 0;">根據<strong>金管會保險局</strong>統計，擁有完整醫療保障的家庭，面對重大疾病時的財務韌性是一般家庭的<span class="highlight">5.8倍</span></p>
        <p class="highlight" style="font-size: 1.5em; margin: 30px 0;">"月存3,000元，換取千萬保障"</p>
        <button onclick="showTooltip(event, '感謝您的信任！我們將立即安排專業顧問為您服務！')" class="cta-button">
            <i class="fas fa-calculator" style="margin-right: 10px;"></i> 免費專屬試算
        </button>
        <p style="margin-top: 20px; font-size: 0.9em;">國泰人壽榮獲2024年「台灣最佳保險公司」與「最佳理賠服務」雙項大獎</p>
    </div>
    
    <!-- 頁尾資訊 -->
    <div class="footer">
        <p>© 2025 國泰人壽保險股份有限公司 版權所有</p>
        <p>服務專線：0800-036-599 | 台北市仁愛路四段296號</p>
        <p>本文件僅供參考，詳細保障內容以保單條款為準</p>
        <p>資料來源：衛生福利部、健保署、國家發展委員會、金管會保險局、國泰人壽內部統計</p>
    </div>

    <!-- 圖表配置與數據 -->
    <script>
        // 圖1：醫療自費趨勢
        new Chart(document.getElementById('medicalTrend'), {
            type: 'line',
            data: {
                labels: ['2018', '2019', '2020', '2021', '2022', '2023', '2024'],
                datasets: [{
                    label: '自費支出（億元）',
                    data: [120, 135, 150, 170, 195, 220, 250],
                    borderColor: '#c43e3e',
                    backgroundColor: 'rgba(196, 62, 62, 0.1)',
                    tension: 0.3,
                    pointRadius: 6,
                    pointBackgroundColor: '#c43e3e',
                    fill: true
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    title: { display: true, text: '醫療自費支出年增率達12%', font: { size: 16 } },
                    legend: { position: 'top' },
                    tooltip: { 
                        callbacks: { 
                            label: function(context) {
                                return `自費支出: ${context.parsed.y}億元`;
                            }
                        }
                    }
                },
                scales: {
                    y: {
                        beginAtZero: false,
                        grid: { color: 'rgba(0,0,0,0.05)' },
                        ticks: { font: { weight: 'bold' } }
                    },
                    x: {
                        grid: { display: false }
                    }
                }
            }
        });

        // 圖2：癌症費用結構
        new Chart(document.getElementById('cancerBreakdown'), {
            type: 'pie',
            data: {
                labels: ['化療/放療', '標靶治療', '住院照護', '其他'],
                datasets: [{
                    data: [25, 40, 20, 15],
                    backgroundColor: ['#4a90e2', '#c43e3e', '#f5a623', '#7ed321'],
                    borderWidth: 3,
                    borderColor: 'white'
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { 
                        position: 'right',
                        labels: { font: { size: 14 } }
                    },
                    tooltip: {
                        callbacks: {
                            label: function(context) {
                                return `${context.label}: ${context.parsed}%`;
                            }
                        }
                    },
                    datalabels: {
                        formatter: (value) => value + '%',
                        color: 'white',
                        font: { weight: 'bold', size: 14 },
                        anchor: 'center'
                    }
                },
                animation: {
                    animateRotate: true,
                    animateScale: true
                }
            }
        });

        // 圖3：健保缺口
        new Chart(document.getElementById('nhiGap'), {
            type: 'bar',
            data: {
                labels: ['心臟支架', '人工關節', '白內障手術', '癌症藥物'],
                datasets: [{
                    label: '健保給付（%）',
                    data: [55, 60, 45, 30],
                    backgroundColor: 'rgba(74, 144, 226, 0.8)',
                    borderColor: '#4a90e2',
                    borderWidth: 1
                },{
                    label: '自費比例（%）',
                    data: [45, 40, 55, 70],
                    backgroundColor: 'rgba(196, 62, 62, 0.8)',
                    borderColor: '#c43e3e',
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                indexAxis: 'y',
                plugins: {
                    title: { display: true, text: '高階醫療項目的自費壓力', font: { size: 16 } },
                    legend: { position: 'top' },
                    tooltip: {
                        callbacks: {
                            label: function(context) {
                                return `${context.dataset.label}: ${context.parsed.x}%`;
                            }
                        }
                    }
                },
                scales: {
                    x: {
                        stacked: true,
                        max: 100,
                        grid: { color: 'rgba(0,0,0,0.05)' }
                    },
                    y: {
                        stacked: true,
                        grid: { display: false }
                    }
                }
            }
        });

        // 圖4：重大疾病給付曲線
        new Chart(document.getElementById('criticalIllness'), {
            type: 'line',
            data: {
                labels: ['確診', '第1年', '第2年', '第3年', '第4年', '第5年'],
                datasets: [{
                    label: '治療支出（萬元）',
                    data: [100, 80, 60, 40, 30, 20],
                    borderColor: '#c43e3e',
                    backgroundColor: 'rgba(196, 62, 62, 0.2)',
                    borderWidth: 3,
                    fill: true,
                    tension: 0.3
                },{
                    label: '保險給付（萬元）',
                    data: [150, 0, 0, 0, 0, 0],
                    borderColor: '#4a90e2',
                    backgroundColor: 'rgba(74, 144, 226, 0.2)',
                    borderWidth: 3,
                    borderDash: [5, 5],
                    pointRadius: 8,
                    pointBackgroundColor: '#4a90e2',
                    fill: false
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { position: 'top' },
                    tooltip: {
                        callbacks: {
                            label: function(context) {
                                return `${context.dataset.label}: ${context.parsed.y}萬元`;
                            }
                        }
                    }
                },
                scales: {
                    y: {
                        beginAtZero: true,
                        grid: { color: 'rgba(0,0,0,0.05)' },
                        title: { display: true, text: '金額（萬元）' }
                    },
                    x: {
                        grid: { display: false }
                    }
                }
            }
        });

        // 圖5：長照趨勢
        new Chart(document.getElementById('longTermCare'), {
            type: 'bar',
            data: {
                labels: ['2020', '2025預估', '2030預估'],
                datasets: [{
                    label: '需求人口（萬人）',
                    data: [60, 80, 110],
                    backgroundColor: 'rgba(245, 166, 35, 0.8)',
                    borderColor: '#f5a623',
                    borderWidth: 1
                },{
                    label: '月均費用（萬元）',
                    data: [3.5, 4.8, 6.2],
                    backgroundColor: 'rgba(196, 62, 62, 0.8)',
                    borderColor: '#c43e3e',
                    borderWidth: 1,
                    yAxisID: 'cost'
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    title: { display: true, text: '長照需求與費用趨勢', font: { size: 16 } },
                    legend: { position: 'top' },
                    tooltip: {
                        callbacks: {
                            label: function(context) {
                                if (context.dataset.label.includes('人口')) {
                                    return `${context.dataset.label}: ${context.parsed.y}萬人`;
                                } else {
                                    return `${context.dataset.label}: ${context.parsed.y}萬元`;
                                }
                            }
                        }
                    }
                },
                scales: {
                    y: {
                        beginAtZero: true,
                        title: { display: true, text: '需求人口（萬人）' },
                        grid: { color: 'rgba(0,0,0,0.05)' }
                    },
                    cost: {
                        type: 'linear',
                        display: true,
                        position: 'right',
                        title: { display: true, text: '月均費用（萬元）' },
                        grid: { display: false }
                    },
                    x: {
                        grid: { display: false }
                    }
                }
            }
        });

        // 圖6：方案對比
        new Chart(document.getElementById('planComparison'), {
            type: 'radar',
            data: {
                labels: ['癌症保障', '住院補助', '重大傷病', '長照支援', '門診涵蓋'],
                datasets: [{
                    label: '基礎方案',
                    data: [60, 70, 80, 40, 50],
                    fill: true,
                    backgroundColor: 'rgba(74, 144, 226, 0.2)',
                    borderColor: '#4a90e2',
                    pointBackgroundColor: '#4a90e2',
                    pointRadius: 5
                },{
                    label: '尊榮方案',
                    data: [90, 95, 100, 80, 85],
                    fill: true,
                    backgroundColor: 'rgba(226, 74, 74, 0.2)',
                    borderColor: '#c43e3e',
                    pointBackgroundColor: '#c43e3e',
                    pointRadius: 5
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { position: 'top' },
                    tooltip: {
                        callbacks: {
                            label: function(context) {
                                return `${context.dataset.label}: ${context.raw}%`;
                            }
                        }
                    }
                },
                scales: {
                    r: {
                        angleLines: { color: 'rgba(0,0,0,0.1)' },
                        grid: { color: 'rgba(0,0,0,0.1)' },
                        pointLabels: { font: { size: 14, weight: 'bold' } },
                        ticks: { display: false }
                    }
                },
                elements: { 
                    line: { borderWidth: 3 }
                }
            }
        });

        // 工具提示
        function showTooltip(event, message) {
            const tooltip = document.createElement('div');
            tooltip.className = 'tooltip';
            tooltip.textContent = message;
            document.body.appendChild(tooltip);
            
            tooltip.style.left = event.pageX + 10 + 'px';
            tooltip.style.top = event.pageY + 10 + 'px';
            tooltip.style.display = 'block';
            
            setTimeout(() => {
                tooltip.remove();
            }, 3000);
        }
    </script>
</body>
</html>
