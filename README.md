# MY Stock 后台管理系统

这是一个独立的后台管理网页，可以部署到任何静态网站托管服务。

## 文件说明

- `index.html` - 后台管理系统主页面（单文件应用）
- `vercel.json` - Vercel 部署配置
- `netlify.toml` - Netlify 部署配置
- `_redirects` - Netlify 重定向规则（备用）

## 部署前配置

**重要：部署前需要修改 API 地址！**

打开 `index.html` 文件，找到以下代码（约第1211行）：

```javascript
const API_BASE = 'https://3000-il9752br2hcf0rrwgiony-d82fd949.sg1.manus.computer';
```

将其修改为您的后端 API 地址，例如：

```javascript
const API_BASE = 'https://your-api-domain.com';
```

## 部署方式

### 方式一：Vercel 部署

1. 注册/登录 [Vercel](https://vercel.com)
2. 点击 "New Project"
3. 选择 "Import Git Repository" 或直接上传文件夹
4. 部署完成后会获得一个 `*.vercel.app` 域名
5. 可在设置中绑定自定义域名

### 方式二：Netlify 部署

1. 注册/登录 [Netlify](https://netlify.com)
2. 将此文件夹拖拽到 Netlify 部署区域
3. 或通过 Git 仓库连接部署
4. 部署完成后会获得一个 `*.netlify.app` 域名
5. 可在设置中绑定自定义域名

### 方式三：GitHub Pages 部署

1. 创建一个新的 GitHub 仓库
2. 将此文件夹内容上传到仓库
3. 进入仓库 Settings → Pages
4. 选择 Branch: main，目录: / (root)
5. 保存后会获得 `username.github.io/repo-name` 地址

### 方式四：本地运行

```bash
# 使用 Python
python3 -m http.server 8082

# 或使用 Node.js
npx serve -p 8082

# 然后访问 http://localhost:8082
```

## 登录信息

- 账号：`admin`
- 密码：`admin123`

**建议登录后及时修改密码！**

## 功能模块

- **控制台** - 数据统计概览
- **用户管理** - 用户列表、余额调整、状态管理
- **交易管理** - 申请审核、持仓列表
- **财务管理** - 充值审核、提现审核、资金流水
- **系统设置** - 发送通知、操作日志

## 数据导出

支持将以下数据导出为 Excel 文件：
- 用户数据
- 交易申请记录
- 充值/提现记录
- 持仓数据
- 操作日志
