# GitHub Actions Telegram Notification System 🚀

Welcome to the **GitHub Actions Telegram Notification System**! This project demonstrates how to automatically send notifications to a Telegram group whenever code is pushed to your repository.

## ✨ Features

- 🔄 **Automatic Notifications**: Get instant alerts when code is pushed to `main` or `develop` branches
- 📱 **Telegram Integration**: Notifications sent directly to your Telegram group
- 🎯 **Rich Information**: Each notification includes:
  - Repository name
  - Author information
  - Branch name
  - Commit message
  - Direct link to the commit

## 🛠️ Setup Process

### 1. Create a Telegram Bot
1. Message [@BotFather](https://t.me/BotFather) on Telegram
2. Send `/newbot` command
3. Choose a name and username for your bot
4. Save the bot token (format: `123456789:ABCdefGHIjklMNOpqrsTUVwxyz`)

### 2. Get Your Chat ID
1. Add your bot to your Telegram group
2. Send a message mentioning your bot
3. Visit: `https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates`
4. Look for the chat ID in the response

### 3. Configure GitHub Secrets
Add these secrets to your repository (Settings → Secrets and variables → Actions):
- `TELEGRAM_BOT_TOKEN`: Your bot token from BotFather
- `TELEGRAM_CHAT_ID`: Your group's chat ID (usually a negative number)

### 4. Create GitHub Actions Workflow
Create `.github/workflows/telegram-notify.yml` with the notification workflow.

## 📋 How It Works

1. **Push Detection**: GitHub Actions monitors pushes to `main` and `develop` branches
2. **Notification Trigger**: When a push is detected, the workflow runs
3. **Message Formatting**: The system formats commit information into a readable message
4. **Telegram Delivery**: The notification is sent to your specified Telegram group

## 🧪 Testing

To test the notification system:
1. Make any change to your repository
2. Commit with a descriptive message
3. Push to the `main` or `develop` branch
4. Check your Telegram group for the notification

## 🎯 Example Notification

```
🚀 New Push Alert

📁 Repository: YourUsername/your-repo
👤 Author: YourName
🌿 Branch: main
📝 Message: Add new feature to improve user experience
🔗 View Commit
```

## 🔧 Troubleshooting

### Common Issues:
- **No notifications**: Check GitHub Actions logs for errors
- **"Chat not found"**: Verify your chat ID is correct
- **"Unauthorized"**: Ensure your bot token is valid
- **"Bot not in group"**: Make sure your bot is added to the group

### Debug Steps:
1. Check GitHub Actions status (green ✅ or red ❌)
2. Review workflow logs for error messages
3. Test bot manually using the Telegram API
4. Verify GitHub secrets are set correctly

## 🎉 Success!

Once configured, your team will receive automatic notifications for all code changes, keeping everyone informed about project updates in real-time!

---

**Status**: ✅ Notification system is working perfectly!
**Last Updated**: $(date)
**Next Test**: Make a commit to see this system in action!
