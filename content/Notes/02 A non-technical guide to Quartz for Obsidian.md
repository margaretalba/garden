---
title: A non-technical guide to quartz for Obsidian
draft: true
created: 2026-09-28T20:32:08
updated: 2026-09-29T20:33:16
---

*Disclaimer:*
I am not an coding developer/expert. This is just something I wish I found when I set up Quartz for Obsidian as a total beginner. 

These directions are **[all here as well](https://quartz.jzhao.xyz/getting-started/installation#option-a-use-the-github-template-recommended)**, but with a few extra steps for the non-technical people. 

**Before Starting**
1. Set up a [github](https://github.com/) account. It's free!
2. Set up your [Obsidian](https://obsidian.md/) if you haven't already. Make sure you have a page called index.
3. Download [Visual Studio Code](https://code.visualstudio.com/)
	1. This is helpful to personalize you digital garden
4. Download https://nodejs.org/en

**Let's Start!**
1. Log in to github.com 
2. Go to https://github.com/jackyzha0/quartz
3. Click **Use this template** > **Create a new repository**![[Screenshot 2026-09-29 at 7.31.37 PM.png|274]]
4. Rename your repository. I used 'gardenexample'. Choose public or private, then click **Create repository**![[Screenshot 2026-09-29 at 7.33.59 PM.png]]
5. If you're on mac click the finder button and look for **Terminal![[Screenshot 2026-09-29 at 7.37.33 PM.png]]**
6. In the Terminal window type the following:
`git clone https://github.com/<your-username>/<your-repo>.gitcd <your-repo>`

 Replace the address with the address from your github. You can get this address by clicking **<> Code** under **HTTPS**
 
 For example, mine would be 
  `git clone https://github.com/margaretalba/gardenexample.git`
![[Screenshot 2026-09-29 at 7.35.55 PM.png]]
8. Enter the following code in your Terminal window
   `cd gardenexample`
   (or whatever your repository name is)
9. Enter the following code in your Terminal window
   `npm i`
   
   If any errors come up, make sure you download https://nodejs.org/en
8. Then enter:
   `npx quartz create`
9. You'll see options, for me I clicked:
When prompted:

10. Choose **`Obsidian`** as your template.
    
11. Choose **`Copy an existing folder`**.
    
12. Enter your path: `/Users/margaretalba/Documents/gardenexample`
    
13. Enter your base URL: `margaretalba.github.io/gardenexample`
   obsidian
   copy an existing folder(to copy files from my obsidian vault)
14. Open you Finder window and locate your Obsidian vault location. If you don't know where it is, you can open Obsidian, and on the bottom-left of your window click the two arrows and click **Manage Vaults**. You can see the location underneath your vault. 
    
    Click the three dots > **Reveal vault in Finder**
    
    Drag and drop the Vault folder to your terminal. Click enter
15. Enter the base URL for your Quartz site:
   I used margaretalba.github.io/gardenexample
16. 8. Then enter:
`npx quartz plugin install --from-config`
17. To push your site enter the following in your terminal:
   npx quartz sync --no-pull

From now on, if you need to update your site, you can enter

npx quartz sync

You can now see your site at http://localhost:8080


**How to publish this on Squarespace**

1. In Terminal, within your site's repository
   echo "yourdomain.com" > static/CNAME npx quartz sync
2. Log into Squarespace > Domains > DNS Settings
3. Add DNS Records to Squarespace
   Under **Custom Records** click **Add record**
For something like garden.margaretalba.com
- Type: CNAME
- Host: garden
- Data/Points to: margaretalba.github.io
4.Save Domain in GitHub Pages Settings

1. Go to your repository on GitHub: `[https://github.com/margaretalba/gardenexample](https://github.com/margaretalba/gardenexample)`
    
2. Click **Settings** (gear icon) > **Pages** (left menu).
    
3. Under **Custom domain**, type `garden.margaretalba.com` and click **Save**.
    
4. Wait 5–10 minutes for GitHub to verify the DNS, then check the box for **Enforce HTTPS**.
