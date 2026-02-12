# User Guide

This document provides detailed instructions on how to use various features of the Rin blog system.

## Comment Features

### Posting Comments

1. Find the comment input box at the bottom of the article page
2. Enter your comment content
3. Click the "Submit" button to post your comment

:::tip
If you're not logged in, you'll need to log in via GitHub OAuth before posting comments.
:::

### Deleting Comments

You can delete your own comments, and administrators can delete any comment.

**Steps to delete:**

1. Find the "More" button (three dots icon ⋯) on the right side of the comment
2. Click it to reveal the action menu
3. Click the delete icon (trash bin icon)
4. Confirm the deletion in the confirmation dialog

:::warning Notice
Deleted comments cannot be recovered. Please proceed with caution.
:::

**Permission Details:**
- Regular users: Can only delete their own comments
- Administrators: Can delete any user's comments

## Article Management

### Creating Articles

1. Click the "Write" button at the top of the page
2. Compose your article in the editor (supports Markdown format)
3. Set the article title, tags, and other information
4. Click the "Publish" button to publish the article

### Editing Articles

1. Navigate to the article details page
2. Click the edit icon (pencil icon) in the top right corner
3. Modify the article content
4. Click the "Update" button to save your changes

### Deleting Articles

1. Navigate to the article details page
2. Click the delete icon (trash bin icon) in the top right corner
3. Confirm the deletion in the confirmation dialog

:::warning Notice
Deleted articles cannot be recovered. All comments associated with the article will also be deleted.
:::

### Pinning Articles

Administrators can pin important articles to the top:

1. Navigate to the article details page
2. Click the pin icon in the top right corner
3. Pinned articles will appear at the top of the homepage list

### Article Aliases

You can set custom URL aliases for articles, such as `https://yourblog.com/about`:

1. When editing an article, find the "Alias" setting
2. Enter a custom alias (only letters, numbers, and hyphens allowed)
3. After saving, the article can be accessed via the custom URL

### Privacy Settings

You can set articles to be "Visible only to me":

1. When editing an article, find the "Visibility" setting
2. Select "Visible only to me"
3. The article will not appear in public lists and will only be visible to you when logged in

### Unlisted Articles

If you don't want an article to appear in the homepage list but still want it accessible via direct link:

1. When editing an article, find the "Listed" option
2. Uncheck "Show on homepage"
3. The article will not appear on the homepage but can still be accessed directly via URL

## Image Upload

### Upload Methods

Two image upload methods are supported:

1. **Drag and Drop**: Drag image files directly into the editor
2. **Paste**: Copy an image and press Ctrl+V (or Cmd+V) in the editor

After a successful upload, the system will automatically generate an image link and insert it into the editor.

## Tag Features

### Adding Tags

You can add tags when editing an article:

1. Input tags in the article content using the format: `#TagName #TagName2`
2. The system will automatically parse and display them as tags
3. Readers can filter related articles by tags

## Blogroll (Friend Links)

### Adding Friend Links

Administrators can add friend links:

1. Go to the settings page
2. Find the "Friend Links" section
3. Fill in the link information (name, description, avatar, URL)
4. Click the "Add" button

The system automatically checks the accessibility of friend links every 20 minutes.

## Moments

A microblog-like short post feature:

1. Click the "Moments" menu
2. Enter your moment content in the input box
3. Click the "Post" button

Moments support Markdown format, suitable for sharing brief thoughts and updates.

## Webhook Notifications

If a Webhook URL is configured, the system will automatically send notifications to the specified Webhook address when new comments are posted.

For configuration instructions, please refer to [Environment Variables](/en/env).

## Frequently Asked Questions

### How do I become an administrator?

The first user to log in via GitHub OAuth will automatically become an administrator. All subsequent users will be regular users.

### Where are local drafts saved?

Local drafts are saved in the browser's localStorage. Drafts for different articles do not interfere with each other.

### Do comments require approval?

No, comments are published immediately. Administrators can delete inappropriate comments afterward.

### What Markdown syntax is supported?

Standard Markdown syntax is supported, including:
- Headings, lists, links, images
- Code blocks (with syntax highlighting)
- Tables
- Blockquotes
- And more

### Where are images stored?

Images are stored in your configured S3-compatible storage (such as Cloudflare R2). For configuration details, please refer to [Environment Variables](/en/env).
