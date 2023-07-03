<!DOCTYPE html>
<html>
<head>
    <title>基于LLM大语言模型面向学生学习编程网站</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px;
        }

        nav {
            background-color: #eee;
            padding: 10px;
            display: flex;
            justify-content: center;
        }

        nav a {
            color: #333;
            text-decoration: none;
            margin: 0 10px;
            font-weight: bold;
        }

        main {
            padding: 20px;
            margin: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        section {
            margin-bottom: 20px;
        }

        h1 {
            margin: 0;
        }

        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px;
        }

        #code-input {
            width: 100%;
            border: 1px solid #ccc;
            padding: 5px;
            font-size: 14px;
            resize: vertical;
        }

        #analyze-btn {
            background-color: #333;
            color: #fff;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            font-size: 16px;
        }

        #analysis-result {
            margin-top: 10px;
            padding: 5px;
            background-color: #f2f2f2;
            border: 1px solid #ccc;
        }
    </style>
<!DOCTYPE html>
<html>
<head>
    <title>基于LLM大语言模型面向学生学习编程网站</title>
    <style>
        /* 样式保持不变 */
    </style>
</head>
<body>
    <header>
        <h1>基于LLM大语言模型面向学生学习编程网站</h1>
    </header>

    <nav>
        <a href="#" id="code-btn">编写代码</a>
        <a href="#" id="ai-btn">AI分析优化代码</a>
        <a href="#" id="forum-btn">交流论坛</a>
    </nav>

    <main>
        <section id="code-section">
            <h2>编写代码</h2>
            <p>在这里输入你的代码：</p>
            <textarea id="code-input" rows="10" cols="80"></textarea>
        </section>

       <section id="ai-section">
            <h2>AI分析优化代码</h2>
            <p>点击下方按钮，让AI对你的代码进行分析和优化：</p>
            <button id="analyze-btn">分析代码</button>
            <div id="analysis-result"></div>
        </section>

        <section id="forum-section">
            <h2>交流论坛</h2>
            <p>在这里和其他编程爱好者交流：</p>
            <div id="forum-messages"></div>
            <textarea id="forum-input" rows="5" cols="50"></textarea>
            <button id="forum-send-btn">发送</button>
        </section>
    </main>

    <footer>
        版权所有 &copy; 2023 19-CodeMentorX gaoxiao03
    </footer>
    <script src="codemirror.js"></script>
    <script>
        const codeEditor = CodeMirror(document.getElementById('code-editor'), {
            value: '',
            mode: 'javascript',
            theme: 'default',
            lineNumbers: true,
            indentUnit: 4,
            indentWithTabs: false,
            autoCloseBrackets: true,
            matchBrackets: true,
            autofocus: true
        });

        analyzeBtn.addEventListener('click', async () => {
            const code = codeEditor.getValue().trim();
            if (code) {
                const optimizedCode = await analyzeAndOptimizeCode(code);
                codeEditor.setValue(optimizedCode);
            } else {
                analysisResult.innerText = '请输入代码';
            }
        });

        async function analyzeAndOptimizeCode(code) {
            // 发送请求给后端进行代码分析和优化
            // 返回优化后的代码
        }
    </script>
    <script>
        const codeBtn = document.getElementById('code-btn');
        const aiBtn = document.getElementById('ai-btn');
        const forumBtn = document.getElementById('forum-btn');
        const codeSection = document.getElementById('code-section');
        const aiSection = document.getElementById('ai-section');
        const forumSection = document.getElementById('forum-section');
        const analyzeBtn = document.getElementById('analyze-btn');
        const codeInput = document.getElementById('code-input');
        const analysisResult = document.getElementById('analysis-result');
        const forumMessages = document.getElementById('forum-messages');
        const forumInput = document.getElementById('forum-input');
        const forumSendBtn = document.getElementById('forum-send-btn');

        codeBtn.addEventListener('click', () => {
            codeSection.style.display = 'block';
            aiSection.style.display = 'none';
            forumSection.style.display = 'none';
        });

        aiBtn.addEventListener('click', () => {
            codeSection.style.display = 'none';
            aiSection.style.display = 'block';
            forumSection.style.display = 'none';
        });

        forumBtn.addEventListener('click', () => {
            codeSection.style.display = 'none';
            aiSection.style.display = 'none';
            forumSection.style.display = 'block';
        });

        analyzeBtn.addEventListener('click', () => {
            const code = codeInput.value.trim();
            if (code) {
                // 发送请求给AI分析优化代码
                // 并显示分析结果
                const result = analyzeCode(code);
                analysisResult.innerText = result;
            } else {
                analysisResult.innerText = '请输入代码';
            }
        });

        forumSendBtn.addEventListener('click', () => {
            const message = forumInput.value.trim();
            if (message) {
                // 在这里添加发送消息的逻辑
                const messageElement = document.createElement('p');
                messageElement.textContent = message;
                forumMessages.appendChild(messageElement);

                // 清空输入框
                forumInput.value = '';
            } else {
                alert('请输入消息');
            }
        });

        function analyzeCode(code) {
            // 在这里可以使用AI模型对代码进行分析处理
            // 返回分析结果
            return '这是代码的分析结果';
        }
    </script>
    <script>
        /*上面已有的代码保持不变*/

        // 用于保存论坛消息
        let forumMessages = [];

        // 模拟一些初始消息
        forumMessages.push({
            username: 'User1',
            message: '欢迎来到论坛！'
        });
        forumMessages.push({
            username: 'User2',
            message: '大家好！'
        });

        // 在页面加载时显示初始消息
        window.addEventListener('load', () => {
            displayForumMessages();
        });
  // 显示论坛消息
  function displayForumMessages() {
            forumMessages.forEach((message) => {
                const messageElement = document.createElement('p');
                messageElement.textContent = `${message.username}: ${message.message}`;
                forumMessages.appendChild(messageElement);
            });
        }

        // 发送按钮点击事件处理函数
        forumSendBtn.addEventListener('click', () => {
            const message = forumInput.value.trim();
            if (message) {
                const username = prompt('请输入您的用户名：');
                if (username) {
                    // 创建新的消息对象
                    const newMessage = {
                        username: username,
                        message: message
                    };

                    // 将消息加入论坛消息数组
                    forumMessages.push(newMessage);

                    // 清空输入框
                    forumInput.value = '';

                    // 清空论坛消息区域并重新显示所有消息
                    clearForumMessages();
                    displayForumMessages();
                } else {
                    alert('请输入用户名');
                }
            } else {
                alert('请输入消息');
            }
        });

        // 清空论坛消息区域
        function clearForumMessages() {
            while (forumMessages.firstChild) {
                forumMessages.removeChild(forumMessages.firstChild);
            }
        }
    </script>
    <script>
        /* 上述代码不变 */
    
        analyzeBtn.addEventListener('click', async () => {
            const code = codeInput.value.trim();
            if (code) {
                const optimizedCode = await analyzeAndOptimizeCode(code);
                analysisResult.innerText = optimizedCode;
            } else {
                analysisResult.innerText = '请输入代码';
            }
        });
    
        async function analyzeAndOptimizeCode(code) {
            try {
                const response = await fetch('/analyze', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify({ code })
                });
                const data = await response.json();
                if (response.ok) {
                    return data.optimizedCode;
                } else {
                    throw new Error(data.error);
                }
            } catch (error) {
                console.error(error);
                return '代码优化失败';
            }
        }
    </script>
</body>
</html>