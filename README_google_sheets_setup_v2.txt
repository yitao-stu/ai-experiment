Google 表格写入版部署说明

你需要做 3 步：

第 1 步：部署 Google Apps Script
1. 新建一个 Google 表格。
2. 在表格里点击：扩展程序 → Apps Script。
3. 删除默认代码，把 google_apps_script_receiver_v2.gs 的全部内容复制进去。
4. 保存。
5. 点击：部署 → 新部署 → 网络应用。
6. 执行身份选择“我”。
7. 访问权限选择“任何知道链接的人”。
8. 部署后，复制生成的 Web App URL（必须是 /exec 结尾）。

第 2 步：把 URL 填进 HTML
1. 打开 full_experiment_fixed_v4_google_sheets_ready_v2.html。
2. 搜索：PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE
3. 用你的 /exec 链接替换它。
4. 保存文件。

第 3 步：上传到 GitHub Pages
1. 把 full_experiment_fixed_v4_google_sheets_ready_v2.html 改名为 index.html。
2. 上传到你的 GitHub 仓库，替换旧的 index.html。
3. 等 1–2 分钟后访问：
   https://你的用户名.github.io/ai-experiment/?reset=1

成功后，学生提交的数据会进入两个工作表：
- Responses：展开后的结构化数据
- Raw_Submissions：原始 JSON 备份

建议你先自己完整测试一遍，再发给学生。
