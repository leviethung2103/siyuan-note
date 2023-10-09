# Knowledge Management

## Tools

There are several tools to support your knowledge management. 

I personally prefer the self-hosted service instead of using the commercial products such as Notion, Evernote. 

Here some tools that I discorved/researched: 
- [Logseg](https://github.com/logseq/logseq)
    * Collaboration
    * PDF. Annotation
    * Task management 
    * Markdown support
    * Video
    * Media
    * Many plugins, themes, workflow customrizaiton options (expanble)
    * Desktop App ? 
    * Look like the RemNote app
        * FlashCard
        * Whiteboard
    * Support Web App -> Link to local database
    * Like Remnote, Obsicidian
    * Copy and paste image -> problem
    * Search mutliple notes: good
- [Affine](https://github.com/toeverything/AFFiNE)
    * Write, Draw and Plan All at Once
	* Notion + Miro (pageless feature) 
	* Draw feature
	* Support MARKDOWN syntax
    * Search feature is not GOOD
- [Siyuan-Note](https://github.com/siyuan-note/siyuan#%EF%B8%8F-development-guide)
    * Like notion
    * flash card feature
    * Easy to deploy via docker
    * Integrate the OpenAI (ChatGPT)
    * Simple, fast and reliable

I've tried these tools and they have some pros and cons. 

My requirements are more specific:
* Search feature: smart, simple
* Simple, fast, self-hosting app 
* Markdown support (support code block)
* Support multiple themes (optional)
* Use the web + desktop app
* Easy to screenshot and paste the image


Therefore, here is my rating
- Logseg: 8/10
- Affine: 7/10
- Siyuan: 10/10

Finally, I chose `Siyuan Note` as my primary knowlege mangaement tool

## How to setup Siyuan 
Setup via docker
```bash
# create the workspace folder 
mkdir -p ~/Downloads/siyuan/workspace

# run service
docker run -d --restart always -v /home/hunglv/Downloads/siyuan/workspace:/siyuan/workspace -p 3001:6806 -u 1000:1000 b3log/siyuan --workspace=/siyuan/workspace/ --accessAuthCode=xxx
```

If curernt user is root, change the user id when runnning the docker container. Check the user id
```bash
id -u
```

Here is the new command
```bash
docker run -d --restart always -v /home/hunglv/Downloads/siyuan/workspace:/siyuan/workspace -p 3001:6806 -u 0:1000 b3log/siyuan --workspace=/siyuan/workspace/ --accessAuthCode=xxx
```



