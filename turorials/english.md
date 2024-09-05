# Show GitHub Logs in Discord Channel Using Webhook

In this tutorial, we will learn how to automatically send GitHub logs (push events, pull requests, etc.) to a Discord channel using a webhook.

## Prerequisites

- GitHub account
- Discord account
- Admin/Moderator access to a Discord server
- A repository where you want to show the logs from

---

## Steps

### 1. Create a Webhook in Discord

1. Open your Discord app.
2. Go to the server where you want to display the GitHub logs.
3. Click on the server name at the top left, then go to **Server Settings** > **Integrations**.
4. Click on **Webhooks** > **Create Webhook**.
5. Set a name for your webhook (e.g., "GitHub Logs") and choose the channel where you want the logs to appear.
6. Copy the **Webhook URL**. We will need this for GitHub.

### 2. Set Up GitHub Webhook

1. Open your GitHub repository.
2. Go to **Settings** > **Webhooks** (left sidebar).
3. Click **Add Webhook**.
4. Paste the **Discord Webhook URL** you copied earlier in the **Payload URL** field.
5. Set the **Content type** to `application/json`.
6. In the **Which events would you like to trigger this webhook?** section, choose:
   - **Just the push event** if you only want push logs.
   - **Let me select individual events** if you want more events like pull requests, issues, etc.
7. Click **Add Webhook** to save.

### 3. Test the Webhook

1. Make a commit or open a pull request in your GitHub repository.
2. Go to your Discord channel, and you should see the logs appear as messages.

---

## Example Output in Discord

When someone pushes to the repository, you will see a message like:

