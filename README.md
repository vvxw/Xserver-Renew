### Xserver 自动续期脚本

#### 构建步骤
1. 创建项目，选择 pervite 私密项目

2. 上传app.js 和 package.json

3. 点击 actions 菜单，create a custom action file

4. 打开 .github/workflows/renew.yml 文件，全选复制内容粘贴进 yml文件编辑框 保存

5. app.js 里填写账号密码 和 tg推送通知环境变量 保存

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
