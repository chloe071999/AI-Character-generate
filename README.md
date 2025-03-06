# 提取推特/文章内容并生成角色

Pipeline for generating AI character files and training datasets by scraping public figures' online presence across Twitter and blogs.

> ⚠️ **IMPORTANT**: Create a new Twitter account for this tool. DO NOT use your main account as it may trigger Twitter's automation detection and result in account restrictions.

## 设置

1. Install dependencies:
   ```bash
   npm install
   ```

2. Copy the `.env.example` into a `.env` file:
   ```properties
   # (Required) Twitter Authentication
   TWITTER_USERNAME="WatchX_bot" # your twitter username
   TWITTER_PASSWORD="watchxnetwork" # your twitter password
   TWITTER_EMAIL="chloe@wahtchx.network" # your twitter email

   BLOG_URLS_FILE=./blogList.txt # path to file containing blog URLs

   # (Optional) Scraping Configuration
   MAX_TWEETS=10 # max tweets to scrape
   MAX_RETRIES=2 # max retries for scraping
   RETRY_DELAY=60 # delay between retries
   MIN_DELAY=10 # minimum delay between requests
   MAX_DELAY=60 # maximum delay between requests


   ```

## 使用设置

### 提取推特内容
```bash
npm run twitter -- username 
```
Example: `npm run twitter -- DePIN_News`

### 提取博客内容
```bash
npm run blog
```

### 生成角色
```bash
npm run character -- username date
```
Example: `npm run character -- DePIN_News 2025-03-05`
