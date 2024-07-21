## 利用 Github Pages 实现 URL 隐性转发
如你需要显性转发，请参考 https://github.com/tynefung/explicit-url-forwarding
> 本项目旨在通过 Github Pages 实现源域名隐性转发至目标域名。以下是详细的操作步骤：

#### Step1： fork 本项目至你的仓库

* 点击本页面的 Fork 按钮  
* Repository name 填写你的项目名称，可随意填写  
* 点击 Create fork    

#### Step2： 配置源域名

* 在你的源域名的 DNS 中，增加 CNAME记录 解析至 {username}.github.io 或 {orgname}.github.io。例如，我的用户名是 tynefung，所以我应解析至 tynefung.github.io  
* 进入项目仓库，在 Code 中点击 CNAME，点击铅笔按钮 (Edit this file) 来编辑文件，将 example.com 替换为源域名   
* 点击 Commit changes 提交变更   
* 点击 Settings 中选择左侧菜单 Code and automation 下面的 Pages，在 Branch 中选择 main /(root) 并点击 Save  
* 勾选 Enforce HTTPS 选项以确保安全访问  

#### Step3： 配置目标域名

* 进入项目仓库，在 Code 中点击 index.html，点击铅笔按钮 (Edit this file) 来编辑文件，将 https://example.com 替换为目标地址  
* 点击 Commit changes 提交变更   
* 相同方法编辑 404.html，将 https://example.com 替换为目标地址  

#### 完成

* 至此，已全部完成配置，正常情况下，当访问源域名时，将隐性转发至目标域名。
* 注意，因为跨域访问限制，访问源域名页面的 title 可能无法更新。
