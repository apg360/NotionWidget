# NotionWidget
NOTION : embedding a weather widget with github pages


https://www.reddit.com/r/Notion/comments/jigaer/embedding_a_weather_widget_with_github_pages/?rdt=61246

<<<
icône r/Notion
Accéder à Notion
r/Notion
•
il y a 4 a
skifreaknyc

embedding a weather widget with github pages
Guide
i noticed that lots of people are interested in embedding weather (and other) widgets in their notion workspaces, but the existing solution (i.e. htmlsave.com) is a bit janky (and as of this moment, not working) and certainly not as robust as github's infrastructure. as such, this is a quick write-up for the more technical folks to leverage github pages to easily create and embed to your heart's content without any arbitrary restrictions.

nb: if you don't know how to clone, commit, push code to github, you may want to consult a technical friend or use the existing solutions that have been mentioned elsewhere in this sub.

# generate the embed file:

1. go to weatherwidgets.io and configure the widget<br/>
  1.click on the “Themes" tab and select the “Blank” theme (to eliminate default border)<br/>
  2.make other style adjustments under “Settings,” “Options,” and “Customize”<br/>
  3.generate the embed code by clicking “Get Code” and “Copy to Clipboard”<br/>

2.replace the designated section of the template file (gist.github.com/congenitaloptimist/18c0995c1d97ce691279605f2e9712e1.js) with the generated code and save as a file with the “.html” suffix<br/>

# set up github pages

  - 1.create or login to your github account (github.com)<br/>
  - 2.create a new repo with a default README (no need to modify/edit this file at any point unless you wish to)<br/>
  - 3.make sure this is created as a “public” not “private" repo<br/>
  - 4.once the repo has been created, click on the repo settings and navigate to the “GitHub Pages” section under the default view “Options”<br/>
  - 5.enable github pages for the repo and select the “main” branch with “/root” (if you don’t see the “main” option, you created the repo without the default “README” file; delete the repo and start again at step 2.2<br/>
    - 1.do not choose a theme<br/>
    - 2.custom domains are not in scope of this guide<br/>
  - 6.once created and the page refreshed, navigate back to the “GitHub Pages" section and copy the link to your newly published website. It’ll look like:<br/>
        - 1.YOUR-USERNAME.github.io/YOUR-REPO-NAME<br/>
  - 7.add a default “index.html” page (required for sites served from “/root”). You can copy this generic template: gist.github.com/congenitaloptimist/d52b298fb09fba8689bb5a0a7d4654b3<br/>
  - 8.now you have 2 files: i) the actual embed code we created in "generate the embed file" step 1.1 → 1.2; and ii) the default “index.html” file<br/>
      - 1.either via command-line (via clone, add, commit, push) or the web interface, push these files to your repo<br/>
   -  9.if your embed file was named “notion-weather-embed.html”, you can now concatenate that filename after the website URL for your Notion-compatible embed URL:<br/>
        - 1.YOUR-USERNAME.github.io/YOUR-REPO-NAME/notion-weather-embed.html<br/>

hope this helps.
>>>
