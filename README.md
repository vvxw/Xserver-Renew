### Xserver 自动续期脚本

#### 构建步骤
1. 创建项目，选择 Private 私密项目

2. 上传app.js 和 package.json

3. 点击 actions 菜单， set up a workflow yourself,创建一个yml文件，文件名随意 

4. 打开 .github/workflows/renew.yml 文件，全选内容复制粘贴进yml文件编辑框 保存

5. app.js 里填写账号密码 和 tg推送通知(可选)环境变量保存，或者在Settings --- secrets and variables --- Actions 里添加 secrets

### 相关环境变量

| Secret 名称         | 是否必填 | 说明                                              |
|---------------------|----------|---------------------------------------------------|
| ACCOUNTS            | ✅ 必填  | xserver登录邮箱和登录密码                             |
| TG_BOT_TOKEN        | ❌ 可选  | Telegram Bot Token（用于发送通知）                |
| TG_CHAT_ID          | ❌ 可选  | Telegram Chat ID（接收通知的用户或群组 ID）        |

ACCOUNTS格式示例：
```
[
    {
        "username": "your-xserver-email@gmail.com", 
        "password": "your-xerver-password"  
    }
]
```
