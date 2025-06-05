欢迎来到二巾木木资料库！
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>学习资源分享与募集</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            text-align: center;
        }
        .container {
            width: 80%;
            margin: 20px auto;
            padding: 20px;
            background: #fff;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1, h2 {
            color: #333;
        }
        .resources-list {
            list-style-type: none;
            padding: 0;
        }
        .resources-list li {
            background: #f9f9f9;
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid #ddd;
        }
        .resources-list li a {
            text-decoration: none;
            color: #007BFF;
        }
        .resources-list li a:hover {
            text-decoration: underline;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }
        .form-group button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
        }
        .form-group button:hover {
            background-color: #45a049;
        }
        .file-upload {
            display: flex;
            align-items: center;
        }
        .file-upload input[type="file"] {
            margin-left: 10px;
        }
    </style>
</head>
<body>
    <header>
        <h1>学习资源分享与募集</h1>
    </header>
    <div class="container">
        <h2>学习资源列表</h2>
        <ul class="resources-list">
            <!-- 示例资源 -->
            <li>
                <a href="www.github.com" target="_blank">工具1：自建个人网页</a>
                <p>操作：登陆github注册后新建仓库（repository）并命名，在该仓库中点最末选项卡Settings，在其中找到Pages。在“生成和部署（Build and deployment）”的 “分支（Branch）”下，使用分支下拉菜单并选择发布源main，点save。自有站点的标题为 username.github.io </p>
            </li>
            <li>
                <a href="https://example.com/resource2" target="_blank">资源2：数据结构与算法</a>
                <p>包含视频和文字资料。</p>
            </li>
        </ul>
        <h2>分享你的学习资源</h2>
        <form id="resourceForm" enctype="multipart/form-data">
            <div class="form-group">
                <label for="resourceName">资源名称</label>
                <input type="text" id="resourceName" name="resourceName" required>
            </div>
            <div class="form-group">
                <label for="resourceLink">资源链接（可选）</label>
                <input type="url" id="resourceLink" name="resourceLink">
            </div>
            <div class="form-group">
                <label for="resourceDescription">资源描述</label>
                <textarea id="resourceDescription" name="resourceDescription" rows="4"></textarea>
            </div>
            <div class="form-group file-upload">
                <label for="resourceFile">上传文件</label>
                <input type="file" id="resourceFile" name="resourceFile">
            </div>
            <div class="form-group">
                <button type="submit">提交资源</button>
            </div>
        </form>
    </div>
    <script>
        document.getElementById('resourceForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const resourceName = document.getElementById('resourceName').value;
            const resourceLink = document.getElementById('resourceLink').value;
            const resourceDescription = document.getElementById('resourceDescription').value;
            const resourceFile = document.getElementById('resourceFile').files[0];

            // 创建新的资源列表项
            const newResource = document.createElement('li');
            newResource.innerHTML = `
                <a href="${resourceLink}" target="_blank">${resourceName}</a>
                <p>${resourceDescription}</p>
            `;
            document.querySelector('.resources-list').appendChild(newResource);

            // 清空表单
            document.getElementById('resourceForm').reset();
        });
    </script>
</body>
</html>
