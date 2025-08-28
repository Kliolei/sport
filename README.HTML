<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>快樂抽抽樂 - 小學一年級抽籤系統</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.12.313/pdf.min.js"></script>
    <style>
        /* 密码输入界面样式 */
        #passwordOverlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            color: white;
            font-family: 'Comic Sans MS', 'Microsoft JhengHei', cursive, sans-serif;
        }
        
        .password-container {
            background-color: rgba(255, 255, 255, 0.2);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            text-align: center;
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255, 255, 255, 0.3);
            max-width: 500px;
            width: 90%;
        }
        
        .password-container h1 {
            font-size: 2.5em;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .password-input {
            display: flex;
            justify-content: center;
            margin-bottom: 25px;
        }
        
        .password-input input {
            padding: 15px 20px;
            font-size: 1.5em;
            border: none;
            border-radius: 50px 0 0 50px;
            width: 200px;
            text-align: center;
            outline: none;
        }
        
        .password-input button {
            padding: 15px 25px;
            font-size: 1.5em;
            border: none;
            border-radius: 0 50px 50px 0;
            background-color: #FF6B6B;
            color: white;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .password-input button:hover {
            background-color: #FF4F4F;
        }
        
        #errorMsg {
            color: #FFD166;
            font-weight: bold;
            min-height: 24px;
            margin-top: 15px;
            font-size: 1.1em;
        }
        
        .hint {
            margin-top: 30px;
            font-size: 0.9em;
            opacity: 0.8;
        }
        
        /* 原内容样式 - 初始隐藏 */
        #mainContent {
            display: none;
        }

        /* 原有样式保持不变 */
        body {
            font-family: 'Comic Sans MS', 'Microsoft JhengHei', cursive, sans-serif;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            text-align: center;
            background-color: #FFF9E6;
            color: #5E5E5E;
        }
        h1 {
            color: #FF6B6B;
            font-size: 2.5em;
            text-shadow: 2px 2px 0px #FFD166;
            margin-bottom: 10px;
        }
        h2 {
            color: #4ECDC4;
            font-size: 1.8em;
            margin-top: 0;
        }
        .container {
            background-color: white;
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            margin-bottom: 20px;
            border: 3px solid #FFD166;
        }
        .upload-section {
            background-color: #F7FFF7;
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 20px;
            border: 2px dashed #4ECDC4;
        }
        .draw-section {
            background-color: #FFE8E8;
            padding: 25px;
            border-radius: 15px;
            display: none;
            border: 2px solid #FF6B6B;
        }
        button {
            background-color: #4ECDC4;
            color: white;
            border: none;
            padding: 12px 25px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 18px;
            margin: 10px 8px;
            cursor: pointer;
            border-radius: 50px;
            transition: all 0.3s;
            font-weight: bold;
            box-shadow: 0 4px 0 rgba(0,0,0,0.1);
        }
        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 0 rgba(0,0,0,0.1);
        }
        button:active {
            transform: translateY(1px);
        }
        button:disabled {
            background-color: #CCCCCC;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }
        #stopBtn {
            background-color: #FF6B6B;
        }
        #resetBtn {
            background-color: #FF9F1C;
        }
        #result {
            font-size: 28px;
            min-height: 300px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 25px 0;
            padding: 30px;
            border: 4px dashed #FFD166;
            border-radius: 20px;
            background-color: white;
            font-weight: bold;
            position: relative;
            overflow: hidden;
        }
        #result img {
            max-height: 400px;
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }
        #pdfPreview {
            margin-top: 25px;
            max-height: 300px;
            overflow-y: auto;
            border: 2px solid #4ECDC4;
            border-radius: 15px;
            padding: 15px;
            display: none;
            background-color: white;
        }
        .name-card {
            margin: 12px;
            padding: 15px;
            background-color: #E8F7FF;
            border-radius: 15px;
            display: inline-block;
            border: 2px solid #A5D8FF;
        }
        .name-card img {
            max-width: 180px;
            border-radius: 8px;
        }
        .loading {
            display: none;
            margin: 25px 0;
        }
        .spinner {
            border: 8px solid #f3f3f3;
            border-top: 8px solid #4ECDC4;
            border-radius: 50%;
            width: 60px;
            height: 60px;
            animation: spin 1s linear infinite;
            margin: 0 auto;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        .file-upload {
            margin: 20px 0;
        }
        .file-upload label {
            display: inline-block;
            padding: 12px 25px;
            background-color: #FFD166;
            color: #5E5E5E;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            font-size: 18px;
            transition: all 0.3s;
            box-shadow: 0 4px 0 rgba(0,0,0,0.1);
        }
        .file-upload label:hover {
            background-color: #FFC233;
            transform: translateY(-3px);
            box-shadow: 0 6px 0 rgba(0,0,0,0.1);
        }
        .file-upload input[type="file"] {
            display: none;
        }
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #FF6B6B;
            opacity: 0;
        }
        .instructions {
            background-color: #E8F7FF;
            padding: 15px;
            border-radius: 15px;
            margin-bottom: 20px;
            text-align: left;
            border: 2px solid #A5D8FF;
        }
        .instructions h3 {
            color: #4ECDC4;
            margin-top: 0;
        }
        .drawn-list {
            background-color: #F0F8FF;
            padding: 15px;
            border-radius: 15px;
            margin-top: 20px;
            border: 2px solid #A5D8FF;
        }
        .drawn-list h3 {
            color: #4ECDC4;
            margin-top: 0;
        }
        .drawn-item {
            display: flex;
            align-items: center;
            margin: 10px 0;
            padding: 10px;
            background-color: white;
            border-radius: 10px;
        }
        .drawn-item img {
            width: 60px;
            height: 60px;
            object-fit: contain;
            margin-right: 15px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <!-- 密码输入界面 -->
    <div id="passwordOverlay">
        <div class="password-container">
            <h1>🔒 抽籤系統 🔒</h1>
            <p>請輸入密碼以繼續使用抽籤系統</p>
            
            <div class="password-input">
                <input type="password" id="passwordInput" placeholder="輸入密碼">
                <button id="submitPassword">確認</button>
            </div>
            
            <div id="errorMsg"></div>
            
            <p class="hint">提示：密碼是4位數字</p>
        </div>
    </div>
    
    <!-- 原内容 - 初始隐藏 -->
    <div id="mainContent">
        <div class="container">
            <h1>🎉 幸運之星 🎉</h1>
            
            <div class="instructions">
                <h3>使用說明：</h3>
                <ol>
                    <li>點擊下方按鈕上傳名牌PDF（每頁一個同學的名牌）</li>
                    <li>等待系統處理完成</li>
                    <li>點擊「開始抽籤」按鈕開始抽籤</li>
                    <li>點擊「停止」按鈕選出幸運同學</li>
                    <li>點擊「重新抽籤」可以重置抽籤記錄</li>
                </ol>
            </div>
            
            <div class="upload-section">
                <h2>第一步：上傳名牌PDF</h2>
                <div class="file-upload">
                    <label for="pdfUpload">選擇PDF檔案</label>
                    <input type="file" id="pdfUpload" accept=".pdf">
                </div>
                <div class="loading" id="uploadLoading">
                    <div class="spinner"></div>
                    <p>正在處理PDF文件，請稍候...</p>
                </div>
                <div id="pdfPreview"></div>
            </div>
            
            <div class="draw-section" id="drawSection">
                <h2>第二步：開始抽籤</h2>
                <button id="startBtn">🎲 開始抽籤</button>
                <button id="stopBtn" disabled>🛑 停止</button>
                <button id="resetBtn">🔄 重新抽籤</button>
                <div id="result">
                    <div style="color: #888;">準備抽籤，結果會顯示在這裡...</div>
                </div>
                
                <div class="drawn-list" id="drawnList" style="display: none;">
                    <h3>已抽中的同學</h3>
                    <div id="drawnItems"></div>
                </div>
            </div>
        </div>

        <!-- 新增音效元素 -->
        <audio id="drawSound" loop>
            <source src="file:///D:/Users/leiwengsi/Desktop/%E6%96%B0%E5%A2%9E%E8%B3%87%E6%96%99%E5%A4%BE/%E6%8A%BD%E7%B1%A4PDF/275398__zagi2__annoying-arcade-loop.wav" type="audio/wav">
            您的瀏覽器不支援音效元素。
        </audio>
        
        <!-- 新增彩色紙花音效元素 -->
        <audio id="confettiSound">
            <source src="file:///D:/Users/leiwengsi/Desktop/%E6%96%B0%E5%A2%9E%E8%B3%87%E6%96%99%E5%A4%BE/%E6%8A%BD%E7%B1%A4PDF/752053__qubodup__standing-ovation.flac" type="audio/flac">
            您的瀏覽器不支援音效元素。
        </audio>

        <script>
            // 密码验证功能
            document.getElementById('submitPassword').addEventListener('click', checkPassword);
            document.getElementById('passwordInput').addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    checkPassword();
                }
            });
            
            function checkPassword() {
                const password = document.getElementById('passwordInput').value;
                const errorMsg = document.getElementById('errorMsg');
                
                if (password === '4321') {
                    // 密码正确，隐藏密码界面，显示主内容
                    document.getElementById('passwordOverlay').style.display = 'none';
                    document.getElementById('mainContent').style.display = 'block';
                } else {
                    // 密码错误，显示错误消息
                    errorMsg.textContent = '密碼錯誤，請重新輸入！';
                    document.getElementById('passwordInput').value = '';
                    document.getElementById('passwordInput').focus();
                    
                    // 添加抖动动画效果
                    const inputGroup = document.querySelector('.password-input');
                    inputGroup.style.animation = 'shake 0.5s';
                    setTimeout(() => {
                        inputGroup.style.animation = '';
                    }, 500);
                }
            }
            
            // 添加抖动动画
            const style = document.createElement('style');
            style.textContent = `
                @keyframes shake {
                    0%, 100% { transform: translateX(0); }
                    20%, 60% { transform: translateX(-10px); }
                    40%, 80% { transform: translateX(10px); }
                }
            `;
            document.head.appendChild(style);

            // 設置PDF.js worker路徑
            pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.12.313/pdf.worker.min.js';
            
            let allNameCards = []; // 儲存所有名牌
            let availableNameCards = []; // 儲存可抽的名牌
            let drawnNameCards = []; // 儲存已抽中的名牌
            let drawInterval;
            let isDrawing = false;
            const drawSound = document.getElementById('drawSound'); // 抽籤音效元素
            const confettiSound = document.getElementById('confettiSound'); // 彩色紙花音效元素
            
            // 上傳PDF文件
            document.getElementById('pdfUpload').addEventListener('change', async function(e) {
                const file = e.target.files[0];
                if (!file) return;
                
                document.getElementById('uploadLoading').style.display = 'block';
                document.getElementById('pdfPreview').style.display = 'none';
                
                try {
                    const pdfData = await readFileAsArrayBuffer(file);
                    const pdf = await pdfjsLib.getDocument({data: pdfData}).promise;
                    
                    allNameCards = [];
                    const previewDiv = document.getElementById('pdfPreview');
                    previewDiv.innerHTML = '';
                    
                    // 提取每一頁作為名牌
                    for (let i = 1; i <= pdf.numPages; i++) {
                        const page = await pdf.getPage(i);
                        const viewport = page.getViewport({scale: 1.5}); // 提高解析度
                        
                        // 創建canvas來渲染PDF頁面
                        const canvas = document.createElement('canvas');
                        const context = canvas.getContext('2d');
                        canvas.height = viewport.height;
                        canvas.width = viewport.width;
                        
                        await page.render({
                            canvasContext: context,
                            viewport: viewport
                        }).promise;
                        
                        // 將canvas轉為圖片URL並存儲
                        const imageUrl = canvas.toDataURL('image/png');
                        allNameCards.push({
                            id: i,
                            image: imageUrl
                        });
                        
                        // 添加到預覽
                        const cardDiv = document.createElement('div');
                        cardDiv.className = 'name-card';
                        cardDiv.innerHTML = `<img src="${imageUrl}"><p>同學 ${i}</p>`;
                        previewDiv.appendChild(cardDiv);
                    }
                    
                    // 初始化可抽名牌
                    resetDrawing();
                    
                    document.getElementById('uploadLoading').style.display = 'none';
                    document.getElementById('pdfPreview').style.display = 'block';
                    document.getElementById('drawSection').style.display = 'block';
                    
                    console.log(`已載入 ${allNameCards.length} 個名牌`);
                } catch (error) {
                    console.error('PDF處理錯誤:', error);
                    alert('處理PDF文件時出錯: ' + error.message);
                    document.getElementById('uploadLoading').style.display = 'none';
                }
            });
            
            // 重置抽籤
            function resetDrawing() {
                availableNameCards = [...allNameCards];
                drawnNameCards = [];
                updateDrawnList();
                document.getElementById('startBtn').disabled = false;
                document.getElementById('result').innerHTML = '<div style="color: #888;">準備抽籤，結果會顯示在這裡...</div>';
                document.getElementById('drawnList').style.display = 'none';
                
                // 停止所有音效
                drawSound.pause();
                drawSound.currentTime = 0;
                confettiSound.pause();
                confettiSound.currentTime = 0;
            }
            
            // 更新已抽中列表
            function updateDrawnList() {
                const drawnItemsDiv = document.getElementById('drawnItems');
                drawnItemsDiv.innerHTML = '';
                
                if (drawnNameCards.length === 0) {
                    document.getElementById('drawnList').style.display = 'none';
                    return;
                }
                
                document.getElementById('drawnList').style.display = 'block';
                
                drawnNameCards.forEach((card, index) => {
                    const itemDiv = document.createElement('div');
                    itemDiv.className = 'drawn-item';
                    itemDiv.innerHTML = `
                        <img src="${card.image}">
                        <span>第 ${index + 1} 位: 同學 ${card.id}</span>
                    `;
                    drawnItemsDiv.appendChild(itemDiv);
                });
            }
            
            // 開始抽籤
            document.getElementById('startBtn').addEventListener('click', function() {
                if (availableNameCards.length === 0) {
                    alert('所有同學都已經抽過了！請點擊「重新抽籤」按鈕重置。');
                    return;
                }
                
                isDrawing = true;
                this.disabled = true;
                document.getElementById('stopBtn').disabled = false;
                document.getElementById('result').innerHTML = '<div style="font-size: 36px;">🎲 抽籤中... 🎲</div>';
                
                // 播放抽籤音效
                drawSound.play().catch(e => console.log('抽籤音效播放失敗:', e));
                
                // 快速切換顯示不同的名牌
                drawInterval = setInterval(() => {
                    const randomIndex = Math.floor(Math.random() * availableNameCards.length);
                    document.getElementById('result').innerHTML = 
                        `<img src="${availableNameCards[randomIndex].image}" style="max-height: 400px;">`;
                }, 100);
            });
            
            // 停止抽籤
            document.getElementById('stopBtn').addEventListener('click', function() {
                if (!isDrawing) return;
                
                clearInterval(drawInterval);
                isDrawing = false;
                document.getElementById('stopBtn').disabled = true;
                
                // 停止抽籤音效
                drawSound.pause();
                drawSound.currentTime = 0;
                
                // 如果還有可抽的名牌
                if (availableNameCards.length > 0) {
                    // 隨機選擇一個名牌
                    const randomIndex = Math.floor(Math.random() * availableNameCards.length);
                    const drawnCard = availableNameCards[randomIndex];
                    
                    // 從可抽列表中移除
                    availableNameCards.splice(randomIndex, 1);
                    
                    // 添加到已抽中列表
                    drawnNameCards.push(drawnCard);
                    updateDrawnList();
                    
                    // 顯示結果
                    document.getElementById('result').innerHTML = 
                        `<h3 style="color: #FF6B6B;">🎊 結果 🎊</h3>
                        <img src="${drawnCard.image}" style="max-height: 400px;">
                        <p>同學 ${drawnCard.id}</p>`;
                    
                    // 添加彩色紙花效果並播放音效
                    createConfetti();
                    
                    // 如果已經抽完所有名牌，禁用開始按鈕
                    if (availableNameCards.length === 0) {
                        document.getElementById('startBtn').disabled = true;
                        document.getElementById('result').innerHTML += 
                            '<p style="color: #FF6B6B; margin-top: 15px;">所有同學都已經抽過了！</p>';
                    } else {
                        document.getElementById('startBtn').disabled = false;
                    }
                }
            });
            
            // 重新抽籤
            document.getElementById('resetBtn').addEventListener('click', function() {
                if (isDrawing) {
                    clearInterval(drawInterval);
                    isDrawing = false;
                    // 停止所有音效
                    drawSound.pause();
                    drawSound.currentTime = 0;
                    confettiSound.pause();
                    confettiSound.currentTime = 0;
                }
                resetDrawing();
                document.getElementById('stopBtn').disabled = true;
            });
            
            // 將文件讀取為ArrayBuffer
            function readFileAsArrayBuffer(file) {
                return new Promise((resolve, reject) => {
                    const reader = new FileReader();
                    reader.onload = () => resolve(reader.result);
                    reader.onerror = reject;
                    reader.readAsArrayBuffer(file);
                });
            }
            
            // 創建彩色紙花效果
            function createConfetti() {
                const colors = ['#FF6B6B', '#4ECDC4', '#FFD166', '#A5D8FF', '#FF9F1C'];
                const resultDiv = document.getElementById('result');
                
                // 清除現有的紙花
                const existingConfetti = document.querySelectorAll('.confetti');
                existingConfetti.forEach(el => el.remove());
                
                // 播放彩色紙花音效
                confettiSound.play().catch(e => console.log('彩色紙花音效播放失敗:', e));
                
                // 計算最長動畫時間
                let maxDuration = 0;
                
                // 創建新的紙花
                for (let i = 0; i < 50; i++) {
                    const confetti = document.createElement('div');
                    confetti.className = 'confetti';
                    confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                    confetti.style.left = Math.random() * 100 + '%';
                    confetti.style.top = -10 + 'px';
                    confetti.style.width = Math.random() * 10 + 5 + 'px';
                    confetti.style.height = Math.random() * 10 + 5 + 'px';
                    confetti.style.transform = 'rotate(' + Math.random() * 360 + 'deg)';
                    
                    resultDiv.appendChild(confetti);
                    
                    // 動畫
                    const duration = Math.random() * 2000 + 1000;
                    if (duration > maxDuration) {
                        maxDuration = duration;
                    }
                    
                    const animation = confetti.animate([
                        { top: '-10px', opacity: 0 },
                        { top: '10%', opacity: 1 },
                        { top: '100%', opacity: 0 }
                    ], {
                        duration: duration,
                        easing: 'cubic-bezier(0.1, 0.8, 0.9, 1)'
                    });
                    
                    animation.onfinish = () => confetti.remove();
                }
                
                // 在動畫結束後1秒停止音效
                setTimeout(() => {
                    confettiSound.pause();
                    confettiSound.currentTime = 0;
                }, maxDuration + 1000);
            }
        </script>
        <h1>~李詠詩老師製作~</h1>
    </div>
</body>
</html>
