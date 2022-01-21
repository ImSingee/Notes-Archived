---
title: Extentions
---

- 这个页面记录了该 Graph 所使用的所有扩展

- 

- 可以通过访问下面的内置页面来更好的查看扩展
	 - [[roam/js]]

	 - [[roam/css]]

- 

- Roam 42
	 - https://roamjs.com/extensions/roam42

	 - 

	 - {{[[roam/js]]}}
		 - 
```javascript
var existing = document.getElementById("roamjs-roam42-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/roam42/main.js";
  extension.id = "roamjs-roam42-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}	

```

	 - [[42 Smart Block]]

- Video Embed
	 - {{[[roam/js]]}}
		 - 
```javascript
var existing = document.getElementById("roamjs-video");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/video.js";
  extension.id = "roamjs-video";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}

```

- 

- Remove Trial Tips
	 - {{[[roam/css]]}}
		 - 
```css
.rm-plan-expired-banner {
  display: none;
}
```

- 

- Theme - Leyendecker
	 - https://github.com/theianjones/roam-research-themes/blob/master/leyendecker.css

	 - {{[[roam/css]]}}
		 - 
```css
/*  Make sure you have the fonts Lato, Open Sans, and IBM Plex installed locally on your machine.
They're free to download from Google:
https://fonts.google.com/specimen/Lato
https://fonts.google.com/specimen/Open+Sans
https://fonts.google.com/featured/Plex
*/


 :root {
    --header-font:"Lato", sans-serif;
    --body-font:"Open Sans", sans-serif;
    --code-font:"IBM Plex", monospace;
    --font-size: 0.95rem;
    --bg-color: #F8F9FB;
    --page-color: rgba(255, 255, 255, 0.95);
    --text-color: #3f4758;
    --light-text-color: #7086A9;
    --page-tag-color: #9DAFCA;
    --color-primary: #ec6f35;
    --color-primary-light: #ff913c;
    --color-primary-highlight: #fcc1786d;
    --color-secondary: #7056F2;
    --color-subtle-border: #dbe4e8;
}

/* Body Colours */
body, #app {
  background: var(--bg-color);
}
.roam-article {
  padding-right: 10px !important;
  padding-left: 20px !important;
}
.roam-article > div {
  padding: 30px 50px 50px 50px;
  background: var(--page-color);
  box-shadow: var(--page-shadow);
  border: 1px solid #e5ecf1;
  border-radius: 6px;
  margin-top: 10px !important;
  width: auto;
}
.roam-body-main {
  top: 0 !important;
  height: 100% !important;
  width: auto !important;
  position: relative !important;
  padding-left: 50px;
}
.roam-main {
  width: unset !important;
  max-width: 100% !important;
  height: 100%;
  overflow-x: scroll;
  overflow-y: hidden;
  margin: auto;
  transition: padding-left 0.15s ease-out;
}

.block-highlight-blue {
background-color: var(--color-primary-highlight) !important;
z-index: 99;
}

div::selection, textarea::selection {
background-color: var(--color-primary-highlight);
}

/* Typography */
h1, h2, h3, h4, h5, h6, .rm-level1, .rm-level2, .rm-level3 .rm-title-editing-display {
  font-family: var(--header-font);
}
.rm-title-editing-display textarea {
  font-family: var(--header-font);
  font-size: 1em;
}
div, textarea {
  font-family: var(--body-font);
  font-size: var(--font-size);
  color: var(--text-color);
}



/* Embed Blocks */
.rm-embed-container {
  background: #fcfdfd;
  border: 1px solid var(--color-subtle-border);
  border-radius: 4px;
  padding: 0.6em 0.4em;
  margin: 0.4em 0;
}
.block-highlight-yellow {
  background-color: white;
}

/* Code Syntax */
code {
  font-family: var(--code-font);
  background: #F0F4F8;
  color: var(--text-color);
  border: none;
  padding: 4px 6px;
  opacity: 90%;
}

/* Queries */
.rm-query {
  border: 0.5px solid #e4e9ec;
  border-radius: 5px;
}
.rm-query .rm-query-title {
  background-color: #f7f8f8;
  padding: 0.8em;
  color: #d1dbe2;
  font-size: 80%;
}
.rm-reference-main.rm-query-content {
  padding: 0.8em;
}
.rm-reference-main, .rm-reference-item {
  font-size: 95%;
  opacity: 95%;
}
.rm-ref-page-view-title span {
}
.rm-reference-main .rm-reference-item .controls {
  margin-left: -1em;
}
.rm-ref-page-view {
  padding: 0.4em 0.2em;
}
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page {
  padding: 6px;
}
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .top-row:hover {
    background-color: white;
}
div.flex-v-box.starred-pages-wrapper > div.flex-h-box > span {
  font-size: 14px;
  opacity: 80%;
  letter-spacing: 0.04em;
}
div.roam-sidebar-container.noselect > div > div {
  font-size: 14px;
  letter-spacing: 0.03em;
}
#block-input {
  background: white;
}
.roam-body #block-input > span > div {
  padding: 6px 24px;
  background: white;
}

.rm-block-text, .roam-block {
  font-size: 1.1em;
}
#right-sidebar > div {
  background-color: white;
  border-left: 1px solid #e9ebef;
  padding: 20px;
  overflow: none;
}
.rm-page-ref-brackets {
  display: none;
}


/* Bullet Points */
.rm-bullet .rm-bullet__inner {
box-sizing: content-box;
  display: flex;
  align-items: center;
  overflow: hidden;
  border-radius: 50%;
  width: 5px;
  height: 5px;
  background-clip: content-box;
  border: 4px solid transparent;
  background-color: #E3ECF2;
}
.rm-bullet.rm-bullet--closed .rm-bullet__inner {
  box-sizing: content-box;
  border: 4px solid #D8E5EE;
}


.block-border-left {
  border-left: 1px solid #fff;
}

/* Kanban */
.kanban-board {
  background-color: #fff;
}
.kanban-card {
  background-color: white;
  margin: 8px;
  box-shadow: 0px 1px 2px #9eb3c0;
  padding: 10px;
  border-radius: 2px;
}
.kanban-title {
  text-align: center;
  font-weight: bold;
  padding-top: 6px;
}
.kanban-column {
  background-color: #e4edf2;
  margin: 0px 4px 0px 4px;
  padding: 4px;
  border-radius: 3px;
}

/* Block references */
.rm-block-ref::before {
  content:"";
  display: inline-block;
  width: 2px;
  border-radius: 2px;
  height: 10px;
  background: var(--color-primary-light);
  margin-right: 6px;
}
.rm-block-ref:hover {
  background: none;
  cursor: pointer;
}
.rm-block-ref {
  border-bottom: none;
  font-size: 1em;
  color: var(--text-color);
  opacity: 90%;
}
.block-ref-count-button {
  color: var(--color-primary);
  font-weight: 800;
  top: -10px;
}


.checkmark {
  background: #fff;
}
.check-container input:checked ~ .checkmark {
  background: #33bdea;
}
.check-container input:checked ~ .checkmark:after {
  border-color: #fff;
}
.rm-reference-item {
  margin-top: 8px;
  border-radius: 6px;
  border: 1px solid #e4e9ee;
  margin-right: 8px;
  flex: 1 1 100%;
  word-break: break-word;
  background-color: #f7f9fb;
  padding: 8px;
}

/* Headings */
.rm-level1 div, .rm-level1 textarea {
  font-size: 1.7rem;
  font-weight: 600;
}
.rm-level2 div, .rm-level2 textarea {
  font-size: 1.4rem;
}
.rm-level3 div, .rm-level3 textarea {
  color: var(--light-text-color);
  font-weight: 400;
  font-size: 1.3rem;
}

a {
 color: var(--color-secondary);
font-weight: 600;
}
.intercom-app, .intercom-launcher-frame, #intercom-container {
  display: none;
}
.roam-body .roam-app .roam-sidebar-container {
  background-color: white;
  border-right: 1px #eee solid;
}
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page, .roam-body .roam-app .roam-sidebar-container > * {
  opacity: 80%;
  box-shadow: none;
}
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page:hover, .roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button:hover {
  background: white;
  color: black;
  opacity: 100%;
}
#buffer.tall {
  height: calc(100vh - 50px);
}
.check-container {
  padding-right: 4px;
}
span.rm-page-ref {
  border-radius: 2px;
  padding-left: 1px;
  padding-right: 1px;
}

.center-proj {
  text-align: center;
}

/* URL links */
.rm-alias--external, .rm-alias--external:hover {
  font-weight: 600;
}

/* Set the colour of popover tooltip text to white */
.bp3-tooltip .bp3-popover-content div {
color: white;
}

/* Page Link and Tag Colours */

.rm-page-ref--tag {
  color: var(--page-tag-color);
}
.rm-page-ref--link {
  color: var(--color-primary);
  font-weight: 600;
}




/* -------------------------- */

/* Custom Data Tags and Pages */

/* -------------------------- */
span.rm-page-ref[data-tag="Tweet"], span[data-link-title^="Tweet"] .rm-page-ref {
  background: #81d5ed !important;
  color: white !important;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}
span.rm-page-ref[data-tag="Literature Notes"], span[data-link-title^="Literature Notes"] .rm-page-ref {
  background: #9769ff !important;
  color: white !important;
  padding: 3px 7px;
  font-weight: 500;
  line-height: 2em;
}
span.rm-page-ref[data-tag="Evergreens"], span[data-link-title^="Evergreens"] .rm-page-ref {
  background: #0dbac6 !important;
  color: #fff !important;
  padding: 3px 8px;
  line-height: 2em;
  font-weight: 500;
}
span.rm-page-ref[data-tag="Seedling"], span[data-link-title^="Seedling"] .rm-page-ref {
  color: #0dbac6 !important;
  padding: 2px;
  font-weight: 600;
  line-height: 1.4em;
  font-size: 0.7em;
  vertical-align: 10%;
  opacity: 80%;
}
span.rm-page-ref[data-tag="Idea Bank"], span[data-link-title^="Idea Bank"] .rm-page-ref {
  color: #fcb815 !important;
  padding: 3px 4px;
  font-weight: 700;
  line-height: 1.4em;
}
span.rm-page-ref[data-tag="Idea Bank"]:before {
  content:"✦ ";
}
span.rm-page-ref[data-tag="Illustrated Notes"], span[data-link-title^="Illustrated Notes"] .rm-page-ref {
  color: #7172fc;
  padding: 3px 4px;
  font-weight: 700;
  line-height: 1.4em;
}
span.rm-page-ref[data-tag="Garden Notes"], span[data-link-title^="Garden Notes"] .rm-page-ref {
  color: #9dbc13;
  padding: 3px 4px;
  font-weight: 700;
  line-height: 1.4em;
}
span.rm-page-ref[data-tag="Video Tutorial"] {
  color: #db3b8d;
  padding: 3px 4px;
  line-height: 1.4em;
  font-weight: 700;
}
span.rm-page-ref[data-tag="Essay"], span[data-link-title^="Essay"] .rm-page-ref {
  background: #adcb2a;
  color: #fff;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}
span.rm-page-ref[data-tag="Livestream"], span[data-link-title^="Livestream"] .rm-page-ref {
  color: #b979cf;
  padding: 3px 4px;
  line-height: 1.4em;
  font-weight: 700;
}
span.rm-page-ref[data-tag="Talk"], span[data-link-title^="Talk"] .rm-page-ref {
  background: #7172fc;
  color: #fff;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}
span.rm-page-ref[data-tag="Waiting"], span[data-link-title^="Waiting"] .rm-page-ref {
  background: #f9c866;
  color: #fff;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}
span.rm-page-ref[data-tag="Researching"], span[data-link-title^="Researching"] .rm-page-ref {
  background: #ff9d66 !important;
  color: #fff;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}
span.rm-page-ref[data-tag="Synthesising"], span[data-link-title^="Synthesising"] .rm-page-ref {
  background: #fc766f !important;
  color: #fff !important;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}
span.rm-page-ref[data-tag="Alive"], span[data-link-title^="Alive"] .rm-page-ref {
  background: #ee5f85 !important;
  color: #fff !important;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}
span[data-link-title^="Book/"] .rm-page-ref {
  color: #119bf0 !important;
  font-weight: 600;
}
span[data-link-title^="Evergreen/"] .rm-page-ref {
  color: #00acc0 !important;
  font-weight: 600;
}
span[data-link-title^="➽"] .rm-page-ref {
  color: #35b2d4 !important;
  font-weight: 700;
}
span[data-link-title^="Video/"] .rm-page-ref {
  color: #119bf0 !important;
  font-weight: 600;
}
span[data-link-title^="Project/"] .rm-page-ref {
  color: #5135d4 !important;
  font-weight: 700;
}
span[data-link-title^="Area/"] .rm-page-ref {
  color: #d4357f !important;
  font-weight: 600;
}
span[data-link-title^="Article/"] .rm-page-ref {
  color: #119bf0 !important;
  font-weight: 600;
}
span[data-link-title^="Course/"] .rm-page-ref {
  color: #5391f8 !important;
  font-weight: 600;
}
span[data-link-title^="Idea/"] .rm-page-ref {
  color: #fcb815 !important;
  padding: 3px 4px;
  font-weight: 700;
  line-height: 1.4em;
}
span[data-link-title^="Idea/"] .rm-page-ref::before {
  content:"✦ ";
}


/* -------------------------- */

/* Block Styles by Tag */

/* -------------------------- */


.roam-block-container[data-page-links*='Claim'] {
  background: #FDF8EE;
  border-radius: 6px;
  padding: 0.6em 0.4em 0.4em 0em;
}

 span.rm-page-ref[data-tag="Claim"], span[data-link-title^="Claim"] .rm-page-ref {
   opacity: 70%;
   font-size: 80%;
   color: #FFC585;
}

.roam-block-container[data-page-links*='Questions'] {
  background: #ECF5FB;
  border-radius: 6px;
  padding: 0.6em 0.4em 0.4em 0em;
}

span.rm-page-ref[data-tag="Questions"], span[data-link-title^="Questions"] .rm-page-ref {
   opacity: 70%;
   font-size: 80%;
   color: #91B9E5;
}

.roam-block-container[data-page-links*='Response'] {
  background: #F3F1FD;
  margin-top: 2px;
  border-radius: 6px;
  padding: 0.6em 0.4em 0.4em 0em;
}

 span.rm-page-ref[data-tag="Response"], span[data-link-title^="Response"] .rm-page-ref {
   opacity: 70%;
   font-size: 80%;
   color: #AFA0E1;
}

.roam-block-container[data-page-links*='Evidence'] {
  background: #FEEDED;
  margin-top: 2px;
  border-radius: 6px;
  padding: 0.6em 0.4em 0.4em 0em;
}

 span.rm-page-ref[data-tag="Evidence"], span[data-link-title^="Evidence"] .rm-page-ref {
   opacity: 70%;
   font-size: 80%;
   color: #F99292;
}

.roam-block-container[data-page-links*='DirectQuote'] {
  background: #F4F6D8;
  margin-top: 2px;
  border-radius: 6px;
  padding: 0.6em 0.4em 0.4em 0em;
}

 span.rm-page-ref[data-tag="DirectQuote"], span[data-link-title^="DirectQuote"] .rm-page-ref {
   opacity: 70%;
   font-size: 80%;
   color: #A5C16A;
}
```

- Theme - Leyendarker
	 - https://github.com/theianjones/roam-research-themes/blob/master/leyendarker.css

	 - {{[[roam/css]]}}
		 - 
```css
:root {
  --header-font: 'GT Walsheim Pro', sans-serif;
  --body-font: 'Inter', sans-serif;
  --font-size: 1.02em;

  --bg-color: #141820;
  --page-color: #2d3037;
  --main-background-color: #2a2e36;

  --text-color: #4c6b8a;
  --light-text-color: #759bc1;
  --icon-color: #7ea8d3; /* #5c7080 */
  --bullet-color: rgba(0, 0, 0, 0.2);
  --selection-color: #6b4cb4c4;

  --page-shadow: 0px 6px 10px rgba(43, 45, 47, 0.05);
  --block-shadow: 0px 2px 4px rgba(90, 99, 104, 0.05);

  --color-primary: #cd7f52;
  --color-primary-highlight: #ffdd99b8;
  --color-primary-contrast: #ffffff;
  --color-secondary: #8c7beb;
  --color-secondary-contrast: #ffffff;

  --border-color: #374356;
  --subtle-border-color: #374153;
  --body-background-color: #343639;
  --reference-item-background: hsl(212, 6%, 25%);
}

.roam-body
  .roam-app
  .roam-sidebar-container
  .roam-sidebar-content
  .starred-pages-wrapper
  .starred-pages
  .page,
.roam-body .roam-app .roam-sidebar-container > * {
  opacity: 80%;
  box-shadow: none !important;
}

.roam-sidebar-container {
  box-shadow: rgba(0, 0, 0, 0.06) 0px 4px 10px 0px !important;
}

.roam-center {
  max-width: 740px;
}
::selection {
  color: #ffffffb0;
  background: var(--selection-color); /* WebKit/Blink Browsers */
}
::-moz-selection {
  color: #ffffffb0;
  background: var(--selection-color); /* Gecko Browsers */
}

.block-highlight-blue {
  color: #ffffffb0;
  background: var(--selection-color);
}

#buffer.tall {
  height: calc(100vh - 50px) !important;
}
.check-container {
  padding-right: 4px;
}
span.rm-page-ref {
  border-radius: 2px;
  padding-left: 1px;
  padding-right: 1px;
}
.content span.rm-page-ref {
  padding: 4px 1px 1px;
  /* required for fixing azo */
}
.center-proj {
  text-align: center;
}

div#buffer {
  display: none;
  visibility: hidden;
}

.zoom-path-view {
  margin-top: 20px;
}

#block-input {
  background: var(--page-color);
}

.roam-body #block-input > span > div {
  padding: 6px 24px;
  background: var(--bg-color);
}

span.bp3-icon-small.bp3-icon-star {
  display: none;
  visibility: hidden;
}

.rm-embed-inner-block-hide {
  margin-left: -40px;
}

#right-sidebar > div {
  border: none;
}

.rm-level3 {
  font-weight: 400;
  font-size: 1.3em;
}
.rm-page-ref {
  color: #9aabd0;
}
.rm-page-ref-link-color {
  color: var(--color-primary);
  font-weight: 600;
}
a {
  color: #8a3cc8;
}
.intercom-app,
.intercom-launcher-frame,
#intercom-container {
  display: none !important;
}

.rm-embed-container {
  background-color: var(--page-color);
  padding: 0.8em;
  border: 1px solid var(--border-color);
  border-radius: 4px;
  box-shadow: var(--block-shadow);
}

.block-ref-count-button {
  color: var(--color-primary) !important;
  font-weight: 800;
  top: -10px;
}

.bp3-popover-target button {
  border: 1px solid var(--color-primary) !important;
  border-radius: 6em !important;
  opacity: 60% !important;
  padding: 0 !important;
}

/* Start of "Better Roam" theming */

iframe {
  border: none !important;
}

.loading-astrolabe {
  position: absolute !important;
  width: 80px !important;
  height: 80px !important;
  opacity: 0.3 !important;
  top: calc(50% - 40px) !important;
  left: calc(50% - 40px) !important;
}

body,
#app {
  background: var(--main-background-color) !important;
}

span.checkmark {
  top: -2px;
}

.rm-level3 div,
.rm-level3 textarea {
  line-height: 1.2 !important;
  color: var(--light-text-color);
}

h1.level2 {
  font-weight: 400 !important;
  font-family: var(--header-font);
  overflow-wrap: break-word;
}

.roam-log-container .roam-log-page:first-child {
  min-height: 0 !important;
  border: none !important;
}

.CodeMirror {
  font-size: 13px !important;
}

.roam-body
  .roam-app
  .roam-sidebar-container
  .roam-sidebar-content
  .log-button:hover,
.roam-body
  .roam-app
  .roam-sidebar-container
  .roam-sidebar-content
  .starred-pages-wrapper
  .starred-pages
  .page:hover {
  color: inherit !important;
  background-color: transparent !important;
}

.roam-sidebar-content {
  padding: 0 !important;
}
.roam-sidebar-content > div:not(.log-button):not(:first-child) {
  padding: 0 !important;
}
.roam-sidebar-content > div:first-child {
  padding-bottom: 18px !important;
}

.starred-pages-wrapper > div:first-child {
  display: none;
}
.starred-pages-wrapper .flex-h-box,
.starred-pages-wrapper .flex-h-box span {
  font-size: 13px !important;
  opacity: 0.6 !important;
}

strong {
  font-weight: 700 !important;
}

/* ----- Start of my Theming -----*/

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: var(--header-font);
  font-size: 3em;
  color: var(--text-color);
}
div,
textarea {
  font-weight: 400;
  color: var(--light-text-color);
  font-family: var(--body-font);
  line-height: 1.7em !important;
  font-size: 1.001em;
}

.rm-pomodoro {
  background: #fff !important;
  color: #ff4747 !important;
  padding: 4px 14px;
  line-height: 2em;
  font-weight: 600;
  border-radius: 2em;
  border: 1px solid #ff474770;
}

.rm-title-display,
.rm-title-textarea {
  line-height: 1.2em !important;
  font-family: var(--header-font);
  color: var(--light-text-color) !important;
}

.rm-title-display {
  margin-top: 0.6em !important;

  color: var(--light-text-color);
}

/* ----- Pomo styling -----*/

.rm-pomodoro {
  background: #ff6956 !important;
  color: #fff !important;
  padding: 4px 14px;
  line-height: 2em;
  font-weight: 600;
  border-radius: 2em;
  border: 1px solid #ed5845;
}

.rm-pomodoro::first-letter {
  margin-right: 8px;
}

/* ----- Query styling -----*/

.rm-query {
  border: 0.5px solid #e4e9ec;
  border-radius: 5px;
}

.rm-query .rm-query-title {
  background-color: var(--bg-color);
  padding: 0.8em;
  color: #d1dbe2;
  font-size: 80%;
}

.rm-reference-main.rm-query-content {
  padding: 0.8em;
}

.rm-reference-main .rm-reference-item .controls {
  margin-left: -1em;
}

.rm-ref-page-view {
  padding: 0.4em 0.2em;
}

div.flex-v-box.starred-pages-wrapper > div.flex-h-box > span {
  font-size: 14px !important;
  opacity: 80%;
  letter-spacing: 0.04em;
}

div.roam-sidebar-container.noselect > div > div {
  font-size: 14px !important;
  letter-spacing: 0.03em;
}

.roam-log-container .roam-log-page {
  min-height: 0 !important;
  border-top: 1px solid var(--border-color) !important;
}

/* ------ Reference Items ------ */

.rm-reference-item {
  background: var(--reference-item-background) !important;
  margin-top: 8px;
  border-radius: 6px;
  border: 1px solid var(--border-color) !important;
  margin-right: 8px;
  flex: 1 1 100%;
  word-break: break-word;
  padding: 8px 10px 8px 2px !important;
}

/* ----- Make left borders and bullets subtle -----*/

.block-border-left {
  border-left-color: var(--subtle-border-color) !important;
}

.controls .simple-bullet-outer .simple-bullet-inner {
  background-color: var(--border-color);
}

/* ------ Kanbans ------ */

.rm-full-width {
  max-width: 100%;
}
.kanban-board {
  background-color: #fff;
}
.kanban-card {
  background-color: white;
  margin: 8px;
  box-shadow: 0px 1px 2px #9eb3c0a8;
  padding: 10px;
  border-radius: 2px;
  line-height: 1.3em;
}
.kanban-title {
  text-align: center;
  font-weight: 600;
  font-size: 1.1em;
  opacity: 80%;
  color: #485f6f;
  padding-top: 8px;
  border-bottom: 1px solid #c5d1d8;
}
.kanban-column {
  background-color: #e7eff3;
  margin: 0px 4px 0px 4px;
  padding: 4px;
  min-width: 120px;
  border-radius: 3px;
}

/* ------ Block Refs ------ */

.rm-block-ref::before {
  content: '';
  display: inline-block;
  width: 2px;
  border-radius: 40px;
  height: 12px;
  background: #ff913c;
  margin-right: 8px;
  text-decoration: none;
}
.rm-block-ref {
  border-bottom: none;
  font-size: 1em;
  color: var(--text-color);
}
.rm-block-ref:hover {
  background: none;
  cursor: pointer;
  text-decoration: none;
}

/* ------ Checkmarks ------ */

.checkmark {
  border-color: var(--color-secondary);
}
.check-container input:checked ~ .checkmark {
  background: var(--color-secondary);
}
.check-container input:checked ~ .checkmark:after {
  border-color: white;
}

.roam-body .roam-app .roam-sidebar-container {
  background-color: white;
  border-right: 1px #eee solid;
}
.rm-block-text > * {
  font-size: var(--font-size) !important;
}

.rm-block-text {
  max-width: 540px;
}

.block-highlight-yellow {
  background-color: var(--color-primary-highlight);
}

textarea {
  font-size: var(--font-size) !important;
  font-family: var(--body-font) !important;
  max-width: 540px !important;
}

/* ------- Zenith Features -------*/

html,
body,
.roam-app {
  overflow: hidden !important;
}

/* hide scrollbars */
::-webkit-scrollbar {
  width: 0px;
  background: transparent; /* Chrome/Safari/Webkit */
}

/* hide scrollbars */
* {
  scrollbar-width: none; /* Firefox */
  -ms-overflow-style: none; /* IE 10+ */
}

.bp3-button.bp3-minimal::before,
.bp3-button.bp3-minimal *,
.bp3-button.bp3-minimal *::before {
  color: var(--icon-color) !important;
}
.bp3-button.bp3-minimal:hover::before,
.bp3-button.bp3-minimal:hover *,
.bp3-button.bp3-minimal:hover *::before {
  color: var(--text-color) !important;
}

*[class*='bp3-icon'],
*[class*='bp3-icon']::before {
  color: var(--icon-color) !important;
}

.bp3-popover {
  color: var(--color-secondary-contrast) !important;
}

.rm-alias-external,
.rm-alias-external:hover {
  color: var(--color-secondary) !important;
  font-weight: 600;
}

/* -------------------------- */
/*         PAGE CARDS         */
/* -------------------------- */

.roam-article {
  padding-right: 10px !important;
  max-width: 100%;
  padding-left: 20px !important;
}

.roam-article > div {
  padding: 30px 50px 50px 50px;
  background: var(--page-color);
  box-shadow: var(--page-shadow);
  border: 1px solid var(--border-color);
  border-radius: 6px;
  margin-top: 10px !important;
}

.roam-body-main {
  top: 0 !important;
  height: 100% !important;
  width: auto !important;
  position: relative !important;
  padding-left: 50px;
}

.roam-main {
  width: unset !important;
  max-width: 100% !important;
  height: 100%;
  overflow-x: scroll;
  overflow-y: hidden;
  margin: auto;
  transition: padding-left 0.15s ease-out;
}

/* -------------------------- */
/*       RIGHT SIDEBAR        */
/* -------------------------- */

#right-sidebar {
  display: inline-flex !important;
  vertical-align: top;
  background-color: transparent !important;
  border: none !important;
  flex-direction: row !important;
  padding-right: 100px;
}
/* hide icon to close sidebar */
#right-sidebar > .flex-h-box {
  display: none;
}

/* spacing and scrolling */
#roam-right-sidebar-content > * {
  margin: 0px 0px 0 14px !important;
  overflow-y: auto !important;
  max-height: 100vh;
  padding: 50px 0px 100px 0px;
  display: block !important;
  position: relative !important;
  border: none !important;
}

#roam-right-sidebar-content {
  visibility: visible;
  display: flex;
  flex-direction: row;
  align-items: flex-start; /* allow pages to have their own height */
  justify-content: flex-end;
}

.roam-center > div:first-child {
  padding: 0 !important;
}
.roam-body-main > * {
  display: inline-block;
}

#roam-right-sidebar-content > * > .flex-h-box {
  display: block !important;
  padding: 18px 10px !important;
}
#roam-right-sidebar-content > * > div {
  background: var(--page-color);
  border: 1px solid var(--border-color);
  box-shadow: var(--page-shadow);
}
#roam-right-sidebar-content > * > div:first-child {
  border-radius: 6px 6px 0px 0px;
  border-bottom: 0;
}
#roam-right-sidebar-content > * > div:first-child:last-child {
  border-radius: 6px;
  border-top: 0;
}
#roam-right-sidebar-content > * > div:last-child:not(:first-child) {
  border-radius: 0px 0px 6px 6px;
  padding-bottom: 50px !important;
  width: 600px;
  border-top: 0;
}
#roam-right-sidebar-content > div > div:not(.flex-h-box) {
  padding: 0px 50px 0px 40px;
}
#roam-right-sidebar-content > div > .flex-h-box > .bp3-button,
#roam-right-sidebar-content .flex-h-box > .bp3-popover-wrapper {
  margin: auto !important;
  width: 20px !important;
  text-align: center;
}
#roam-right-sidebar-content > div > .flex-h-box > .bp3-button:first-child,
#roam-right-sidebar-content .flex-h-box > .bp3-button:last-child {
  display: block;
}

#roam-right-sidebar-content > div .bp3-icon-plus ~ .bp3-button,
#roam-right-sidebar-content > div .bp3-icon-plus ~ .bp3-popover-wrapper {
  display: none;
}

/* position minus button */
#roam-right-sidebar-content > div .bp3-icon-minus,
#roam-right-sidebar-content > div .bp3-icon-plus {
  position: absolute;
  top: 20px;
  left: 20px;
}
/* position filter button */
#roam-right-sidebar-content > div .bp3-icon-minus ~ .bp3-popover-wrapper {
  position: absolute;
  top: 20px;
  left: 50px;
}
/* position references button */
#roam-right-sidebar-content > div .bp3-icon-minus ~ button.bp3-button {
  position: absolute;
  top: 20px;
  left: 80px;
}
/* position close button */
#roam-right-sidebar-content > div .bp3-icon-minus ~ .bp3-button.bp3-icon-cross {
  position: absolute;
  top: 20px;
  right: 20px;
}

#roam-right-sidebar-content > div .bp3-icon-minus + * {
  margin: 20px 5px 5px 30px !important;
  max-width: 540px;
}

#roam-right-sidebar-content > div .level2 a {
  color: var(--text-color);
  line-height: 1.4em;
  transition: 400ms;
  font-size: 1.1em;
}

#roam-right-sidebar-content > div a:hover {
  color: var(--color-primary);
  text-decoration: none;
  transition: 400ms;
}

#roam-right-sidebar-content > div .bp3-icon-plus ~ h1 {
  margin-top: 10px !important;
}
#roam-right-sidebar-content > div .bp3-icon-plus ~ .bp3-button:last-child {
  margin-top: 20px !important;
}
#roam-right-sidebar-content > div .bp3-icon-plus,
#roam-right-sidebar-content > div .bp3-icon-plus ~ * {
  display: block;
  flex: none !important;
}
#roam-right-sidebar-content > div .bp3-icon-plus + * {
  white-space: nowrap;
  writing-mode: vertical-rl;
  min-width: 0;
}
#roam-right-sidebar-content > div .bp3-icon-plus + div {
  padding: 0px 12.5px;
}

/* fix positioning problems with menu icon */
.roam-topbar *[class*='icon-menu']::before {
  position: absolute !important;
  top: 4px !important;
  left: 4px !important;
}
.roam-topbar .bp3-icon-menu-open::before {
  content: ''; /* prevent menu icon from changing on hover */
}

/* -------------------------- */
/*        LEFT SIDEBAR        */
/* -------------------------- */

/* HIDE LOGO*/
#roam-sidebar-logo {
  display: none;
}

.roam-sidebar-content * {
  color: var(--icon-color) !important;
}

.starred-pages > a > .page:hover {
  background-color: transparent !important;
  color: var(--primary-color) !important;
}

.starred-pages > a {
  padding-left: 0 !important;
}

.starred-pages-wrapper {
  margin-left: 10px;
}

.log-button * {
}
.log-button {
  background: none !important;
}
.log-button:hover,
.log-button:hover * {
  color: var(--text-color) !important;
}
.roam-sidebar-content {
  color: var(--text-color) !important;
}

.roam-topbar {
  opacity: 1 !important;
  background-color: transparent !important;
  margin-top: 70px;
  width: 20px;
  display: inline-block;
  padding-left: 0px !important;
  position: relative !important;
  position: sticky !important;
  left: 0px;
  transition: none !important;
  z-index: 999;
  border: none !important;
}
.roam-sidebar-container > .roam-sidebar-content::before {
  content: '';
  position: absolute;
  top: -70px;
  right: -30px;
  width: 400px;
  height: 100vh;
  opacity: 0.7;
  z-index: -1;
}

.roam-sidebar-container {
  border: none !important;
  top: 0px !important;
  padding-top: 70px;
  visibility: hidden; /* hide background */
  transition: all 0.25s ease-out;
  width: 240px !important;
  padding-right: 40px;
  padding-left: 10px;
  backdrop-filter: blur(5px);
  background: #000000 !important;
}

.roam-sidebar-container > .roam-sidebar-content {
  display: block !important;
  height: auto !important;
  visibility: visible; /* show contents */
}
.roam-sidebar-container > .roam-sidebar-content > * {
  opacity: 0 !important;
  transition: opacity 0.6s ease-out !important;
}
.roam-sidebar-container:not([style*='top: 0px']) {
  left: -170px !important;
}
.roam-sidebar-container[style*='top: 0px'] > .roam-sidebar-content > * {
  opacity: 1 !important;
}
.roam-sidebar-container[style*='top: 0px'] + .roam-main {
  padding-left: 180px;
}

/* fix height with absolute positioning of email address */
.roam-sidebar-content > .flex-h-box {
  height: 40px;
}
.roam-sidebar-content > .flex-h-box > * {
  pointer-events: auto;
}
.roam-sidebar-content > .flex-h-box ~ * {
  pointer-events: all;
}
.roam-sidebar-content > .flex-h-box > .flex-h-box {
  position: absolute;
  left: 45px;
  top: 5px;
}

.roam-topbar > .flex-h-box {
  width: 50px;
  flex-direction: column;
  height: 1px !important;
  align-items: start !important;
  text-align: center;

  position: -webkit-sticky !important;
  position: sticky !important;
  left: 0px;
}
.roam-topbar > .flex-h-box > * {
  flex: 0 0 20px !important;
  margin: auto !important;
  max-width: 20px !important;
  max-height: 20px !important;
}
.roam-topbar > div > .bp3-button:first-child {
  align-self: start !important;
  position: fixed !important;
  left: 16px;
  top: 78px;
  z-index: 9999999 !important;
}
.roam-topbar > div > *:nth-child(2) {
  margin-top: 20px !important;
}

.rm-reference-item {
  background-color: transparent !important;
}

.rm-ref-page-view-title a {
  color: var(--light-text-color);
  font-size: 1.1em;
  text-decoration: none !important;
}

/* SOME BLACKMAGIC TO GET SEARCH ICON TO FUNCTION LIKE OTHER BUTTONS */

.roam-topbar .bp3-icon-search {
  padding: 4px;
  border-radius: 3px;
  margin: 0 !important;
  cursor: pointer;
}

/* style contains `200px` if search bar is NOT selected */
/* hovering search bar in this mode == hovering icon itself */
/* we must however have the search bar in front of the icon (but invisible) so that it can focus on click */
/* very hacky :P */
.rm-find-or-create-wrapper[style*='200px']:hover .bp3-icon-search,
.roam-topbar .bp3-icon-search:hover {
  background-color: var(--color-primary);
  color: var(--text-color) !important;
}
.roam-topbar .bp3-icon-search svg {
  padding: 1px;
}
/* fix centering on calendar icon */
.roam-topbar .bp3-icon-calendar {
  margin: 0 !important;
}

.rm-find-or-create-wrapper {
  width: 20px !important;
}
.rm-find-or-create-wrapper .bp3-overlay {
  position: fixed;
  top: 50px;
  left: calc(50% - 325px);
  width: 650px;
}

.roam-body-main {
  display: block;
  width: 100%;
}

/* -------------------------- */
/*       POPOVER STYLES       */
/* -------------------------- */

.bp3-menu-divider {
  border-color: rgba(255, 255, 255, 0.25) !important;
}
.bp3-text-small {
  color: var(--text-color) !important;
  opacity: 0.6;
}

.bp3-transition-container {
  /* not very good at these z-indexes huh? */
  z-index: 9999999999 !important;
}
.bp3-popover {
  min-width: 230px; /* fix width */
  pointer-events: none; /* prevent from getting in the way of hover*/
}
.bp3-popover .bp3-menu,
.bp3-popover .bp3-popover-content {
  pointer-events: auto;
}

.bp3-popover .bp3-popover-arrow svg * {
  fill: var(--page-color);
}

.bp3-popover .bp3-popover-content {
  background-color: var(--page-color) !important;
  max-width: 480px;
}

#app .bp3-popover .bp3-popover-arrow svg * {
  fill: rgb(var(--color-secondary));
  fill: var(--page-color);
}

/* what a mess! */

/*.roam-body-main .bp3-popover .bp3-popover-content, .roam-body-main .bp3-menu,
.roam-sidebar-container .bp3-popover .bp3-popover-content, .roam-sidebar-container .bp3-menu {
    background-color: rgb(var(--color-secondary)) !important;
}
.roam-body-main .bp3-popover .bp3-popover-content, .roam-body-main .bp3-popover .bp3-popover-content *,
.roam-sidebar-container .bp3-popover .bp3-popover-content, .roam-sidebar-container .bp3-popover .bp3-popover-content * {
    color: var(--color-secondary-contrast) !important;
}*/

body > .bp3-portal .bp3-menu {
  background-color: var(--page-color) !important;
}
body > .bp3-portal .bp3-popover-content,
body > .bp3-portal .bp3-popover-content * {
  color: var(--text-color) !important;
}

.bp3-popover .bp3-button,
.bp3-popover .bp3-button * {
  color: var(--text-color) !important;
}

body > .bp3-portal *[style*='rgba(72, 176, 240, 0.5)'] > span::before,
body > .bp3-portal *[style*='rgba(72, 176, 240, 0.5)'] * {
  color: var(--color-secondary-contrast) !important;
}
body > .bp3-portal .bp3-menu-divider {
  border-color: rgba(0, 0, 0, 0.2) !important;
}
body > .bp3-portal .bp3-text-small {
  color: rgba(0, 0, 0, 0.5) !important;
}

.emoji-mart {
  border: none !important;
}

/* -------------------------- */
/*         SEARCH BAR         */
/* -------------------------- */

#find-or-create-input {
  opacity: 0;
  z-index: 10000; /* bring in front of icon to keep clickable */
  cursor: pointer;
}

#find-or-create-input:active,
#find-or-create-input:focus {
  opacity: 1;
  position: fixed;
  width: 580px;
  top: 100px;
  left: calc(50% - 308px);
  cursor: text;
}

#find-or-create-input {
  border-radius: 10px 10px 0px 0px;
  font-size: 18px;
  padding: 20px 20px;
}
/* if input is empty (no menu) then use all-around border-radius*/
#find-or-create-input[value=''] {
  border-radius: 10px;
}

/* highlight around search box */
#find-or-create-input:focus {
  box-shadow: 0 0 0 1px var(--color-primary-highlight),
    0 0 0 3px var(--color-primary-highlight),
    inset 0 1px 1px rgba(16, 22, 26, 0.2);
}

/* styling dropdown menu*/
.rm-find-or-create-wrapper .bp3-popover {
  border-radius: 0px 0px 10px 10px;
  overflow: hidden;
  background: var(--page-color);
  backdrop-filter: blur(5px);
}

/* prevent coloured menu */
.rm-find-or-create-wrapper .bp3-popover-content,
.rm-find-or-create-wrapper .bp3-menu {
  background-color: transparent !important;
}

/* properly position search menu overlay */
.rm-find-or-create-wrapper .bp3-overlay {
  top: 142px;
  width: 580px;
  left: calc(50% - 308px);
  z-index: 999999;
}

/* new page text */
.rm-find-or-create-wrapper .rm-new-page {
  color: rgb(var(--color-primary)) !important;
}

/* selected search result */
.rm-find-or-create-wrapper .rm-menu-item[style*='background'] {
  background-color: rgba(0, 0, 0, 0.1) !important;
}

/* search results highlighted words */
.rm-find-or-create-wrapper
  .rm-menu-item
  .rm-search-list-item
  span[style*='yellow'],
.rm-pages-title-col span[style*='yellow'] {
  background-color: var(--color-primary-highlight) !important;
  color: var(--text-color);
}

.bp3-input {
  background-color: var(--page-color) !important;
  color: var(--text-color) !important;
}
.bp3-input::placeholder {
  background-color: var(--page-color) !important;
  color: var(--text-color) !important;
  opacity: 0.3;
}

/* -------------------------- */
/*          DIAGRAM           */
/* -------------------------- */

.rm-block-text svg {
  background-color: var(--page-color) !important;
  border: none !important;
}
.bp3-button,
.roam-block div[style*='100vh'] > button {
  background-image: none !important;
  padding: 0px 10px !important;
  border: none !important;
  border-radius: 5px !important;
}
.roam-block div[style*='100vh'] > button {
  background-color: var(--bg-color) !important;
}

.bp3-button:hover,
.roam-block div[style*='100vh'] > button:hover {
  background-color: var(--color-primary) !important;
}
.roam-block div[style*='100vh'] div[style*='background-color: white'] {
  background-color: var(--page-color) !important;
  border-color: var(--bg-color) !important;
}

.roam-center svg > g > rect:first-child,
#roam-right-sidebar-content > div svg > g > rect:first-child {
  display: none;
}

.roam-center svg > g > foreignObject,
#roam-right-sidebar-content > div svg > g > foreignObject {
  background-color: var(--page-color);
  border-radius: 8px;
  filter: drop-shadow(0px 4px 6px rgba(0, 0, 0, 0.05));
  border: 1px solid transparent;
}

/* SELECTION */

.roam-center svg > g > rect[stroke='red'] + foreignObject,
#roam-right-sidebar-content > div svg > g > rect[stroke='red'] + foreignObject {
  border-color: var(--color-primary-highlight);
}

.roam-center svg > g > rect[style*='stroke: red'] + foreignObject,
#roam-right-sidebar-content
  > div
  svg
  > g
  > rect[style*='stroke: red']
  + foreignObject {
  border-color: var(--color-primary-highlight);
}

.roam-center svg > g > rect[style*='rgba'] + foreignObject,
#roam-right-sidebar-content
  > div
  svg
  > g
  > rect[style*='rgba']
  + foreignObject {
  background-color: white;
}

.roam-center svg > g > foreignObject > input:first-child,
#roam-right-sidebar-content > div svg > g > foreignObject > input:first-child {
  background-color: var(--color-primary-highlight) !important;
  color: var(--color-primary-contrast);
  height: 30px;
}

.roam-center svg > line[style*='stroke: red'],
#roam-right-sidebar-content > div svg > line[style*='stroke: red'] {
  stroke: var(--color-secondary) !important;
}

.roam-center svg > rect[style*='fill: rgba(55, 141, 240, 0.5)'],
#roam-right-sidebar-content
  > div
  svg
  > rect[style*='fill: rgba(55, 141, 240, 0.5)'] {
  fill: var(--color-secondary) !important;
  stroke: var(--color-secondary) !important;
}

/* -------------------------- */
/*       SEARCH PAGE          */
/* -------------------------- */

#all-pages-search {
  max-height: calc(100% - 50px);
  overflow-y: auto;
  padding-bottom: 100px !important;
}
#all-pages-search > div {
  padding: 0 !important;
}
.rm-pages-row-header {
  background-color: var(--color-primary) !important;
  color: var(--color-secondary-contrast) !important;
  border: none !important;
}
.rm-pages-row[style] .bp3-icon::before {
  margin-left: 5px;
  color: var(--color-secondary-contrast) !important;
}
.rm-pages-row-highlight {
  background-color: var(--page-color);
}
.rm-pages-row[style] .rm-pages-action-col {
  color: transparent !important;
}
/* use wrench icon for actions header rather than "AC..." */
.rm-pages-row[style] .rm-pages-action-col::before {
  font-family: 'Icons16';
  content: '';
  color: var(--color-secondary-contrast);
  position: absolute;
  margin-left: 10px;
}

/* style new page button */
.bp3-intent-success {
  color: rgb(var(--color-primary)) !important;
}
.bp3-intent-success:hover {
  background-color: rgba(73, 197, 91, 0.2) !important;
}
.bp3-intent-success:active {
  background-color: rgba(73, 197, 91, 0.4) !important;
}

/* new search page */

.bp3-control-indicator {
  background-color: var(--page-color) !important;
  background-image: none !important;
  border: 1px solid var(--color-primary) !important;
}

.bp3-control input:checked ~ .bp3-control-indicator {
  background-color: var(--color-primary) !important;
  box-shadow: none !important; /* sliders */
}
.bp3-checkbox > input:checked ~ .bp3-control-indicator::before {
  width: 0.9em !important;
  height: 0.9em !important;
}

.rm-clickable-pill {
  background-color: var(--color-primary) !important;
}
.rm-clickable-pill.empty-pill {
  background-color: var(--page-color) !important;
}

.rm-pages-col-word-count > div > span:first-child,
.rm-pages-col-word-count + div > div > span:first-child {
  display: none;
}
/*.rm-pages-col-word-count > div > .sorting-button-group::before {
    content: "WORDS";
    font-size: 0.8em;
}
.rm-pages-col-word-count + div > div > .sorting-button-group::before {
    content: "REFS";
    font-size: 0.8em;
}*/
.sorted-header-text {
  color: var(--text-color) !important;
}

.rm-pages-row .rm-pages-col {
  flex: 0 0 60px !important;
}
.rm-pages-row .rm-pages-col:nth-last-child(1),
.rm-pages-row .rm-pages-col:nth-last-child(2) {
  flex: 0 0 140px !important;
}
.rm-all-pages .table > div {
  max-width: 580px !important;
  min-width: 580px !important;
}

.sort-button::before {
  color: var(--text-color) !important;
}
.sort-button.focused::before {
  color: rgb(var(--color-primary)) !important;
}

.rm-pages-row {
  border-bottom: none !important;
}
.rm-pages-row:nth-child(2n + 1) {
  background-color: var(--color-primary);
  border-radius: 3px;
}

/* fix width change on border */
.rm-all-pages .bp3-input {
  border: 1px solid transparent;
}

.rm-all-pages .bp3-input.focused {
  border: 1px solid rgb(var(--color-primary)) !important;
}

/* ------------ Custom data tags ------------ */

span.rm-page-ref[data-tag='Tweet'] {
  background: #81d5ed !important;
  color: white !important;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}

span.rm-page-ref[data-tag='Literature Notes'] {
  background: #9769ff !important;
  color: white !important;
  padding: 3px 7px;
  font-weight: 500;
  line-height: 2em;
}

span.rm-page-ref[data-tag='Evergreens'] {
  background: #0dbac6 !important;
  color: #fff !important;
  padding: 3px 8px;
  line-height: 2em;
  font-weight: 500;
}

span.rm-page-ref[data-tag='Seedling'] {
  color: #0dbac6 !important;
  padding: 3px 3px;
  font-weight: 600;
  line-height: 1.4em;
}

span.rm-page-ref[data-tag='Idea Bank'] {
  color: #fcb815 !important;
  padding: 3px 4px;
  font-weight: 700;
  line-height: 1.4em;
}

span.rm-page-ref[data-tag='Idea Bank']:before {
  content: '✦ ';
}

span.rm-page-ref[data-tag='Illustrated Notes'] {
  color: #7172fc;
  padding: 3px 4px;
  font-weight: 700;
  line-height: 1.4em;
}

span.rm-page-ref[data-tag='Garden Notes'] {
  color: #9dbc13;
  padding: 3px 4px;
  font-weight: 700;
  line-height: 1.4em;
}

span.rm-page-ref[data-tag='Video Tutorial'] {
  color: #db3b8d;
  padding: 3px 4px;
  line-height: 1.4em;
  font-weight: 700;
}

span.rm-page-ref[data-tag='Essay'] {
  background: #adcb2a;
  color: #fff;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}

span.rm-page-ref[data-tag='Livestream'] {
  color: #b979cf;
  padding: 3px 4px;
  line-height: 1.4em;
  font-weight: 700;
}

span.rm-page-ref[data-tag='Talk'] {
  background: #7172fc;
  color: #fff;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}

span.rm-page-ref[data-tag='Waiting'] {
  background: #f9c866;
  color: #fff;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}

span.rm-page-ref[data-tag='Researching'] {
  background: #ff9d66 !important;
  color: #fff;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}

span.rm-page-ref[data-tag='Synthesising'] {
  background: #fc766f !important;
  color: #fff !important;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}

span.rm-page-ref[data-tag='Alive'] {
  background: #ee5f85 !important;
  color: #fff !important;
  padding: 3px 7px;
  line-height: 2em;
  font-weight: 500;
}

span.rm-page-ref[data-tag^='SR: '] {
  background: #f3ecff !important;
  color: #8b53bf !important;
  border: 1px solid #c5a8e0;
  border-radius: 3px;
  padding: 3px 8px;
  line-height: 2em;
  font-weight: 500;
}
```

- Theme - Night Owl Ish
	 - https://github.com/theianjones/roam-research-themes/blob/master/night-owl-ish.css

	 - {{[[roam/css]]}}
		 - 
```css
/*  Make sure you have the fonts Lato and Dank Mono installed locally on your machine.
Lato is free to download from Google:
https://fonts.google.com/specimen/Lato

Dank Mono is available for purchase:
https://dank.sh/  

I reccomend Open Sans if you dont want to purchase Dank Mono:
https://fonts.google.com/specimen/Open+Sans
*/

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Lato';
}
div,
textarea {
  font-family: 'Dank Mono';
}

.roam-block-container {
  max-width: 1000px;
}
.roam-block, .rm-block-text {
  max-width: 850px;
}

.bp3-button.bp3-minimal {
  color: #ffa7c4;
}

.bp3-button.bp3-minimal:hover {
  color: #ffa7c4;
}

.bp3-elevation-3 {
  background-color: #697098 !important;
}

.bp3-elevation-3 > div:hover {
  background-color: #011627;
}

.kanban-board {
  background-color: #fff;
}

.kanban-card {
  background-color: white;
  margin: 8px;
  box-shadow: 0px 1px 2px #9eb3c0;
  padding: 10px;
  border-radius: 2px;
  line-height: 1.3em;
}

.kanban-title {
  text-align: center;
  font-weight: bold;
  padding-top: 6px;
}

.kanban-column {
  background-color: #e4edf2;
  margin: 0px 4px 0px 4px;
  padding: 4px;
  min-width: 200px;
  border-radius: 3px;
}


.rm-block-ref {
  border-bottom: none;
  font-size: 1em;
  padding: 4px;
  color: #697098;
}

.rm-block-ref:hover {
  background-color: #697098;
  color: #011627;
}

.checkmark {
  background: #fff;
}
.check-container input:checked ~ .checkmark {
  background: #2db4eb;
}
.check-container input:checked ~ .checkmark:after {
  border-color: #fff;
}

.rm-level3 {
  color: #8390b2;
}

.rm-page-ref {
  color: #7e57c2cc;
}

.rm-page-ref-link-color {
  color: #ffa7c4;
}

a {
  color: #64b5f6 !important;
}

.intercom-app,
.intercom-launcher-frame,
#intercom-container {
  display: none !important;
}

.rm-reference-item div {
      background-color: #2e3250;

}

#right-sidebar div .rm-reference-item div,
.roam-topbar,
.roam-body {
  background-color: #011627;
}

.roam-body-main {
  background-color: #011627;
  color: #fff;
}

.roam-body .roam-app h1 {
  color: #fff;
}

#right-sidebar div {
  background-color: #2e3250;
}

.roam-body .roam-app .roam-sidebar-container {
  background-color: #2e3250;
  border-right: 1px #051e33 solid;
}

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button,
.roam-body
  .roam-app
  .roam-sidebar-container
  .roam-sidebar-content
  .starred-pages-wrapper,
.roam-body
  .roam-app
  .roam-sidebar-container
  .roam-sidebar-content
  .starred-pages-wrapper
  .starred-pages
  .page,
.roam-body .roam-app .roam-sidebar-container > * {
  opacity: 0.9;
  color: #fff;
}
.roam-body
  .roam-app
  .roam-sidebar-container
  .roam-sidebar-content
  .starred-pages-wrapper
  .starred-pages
  .page:hover,
.roam-body
  .roam-app
  .roam-sidebar-container
  .roam-sidebar-content
  .log-button:hover {
  background: #011627;
  color: white;
  opacity: 0.9;
}
#buffer.tall {
  height: calc(100vh - 50px) !important;
}
.check-container {
  padding-right: 4px;
}

.rm-reference-item {
  background-color: #011627;
}

.block-highlight-blue,
#roam-right-sidebar-content div .block-highlight-blue div {
  background-color: #a599e9;
}

.kanban-board {
    background: #011627;
    color: white;
}

.kanban-column {
    background-color: #2e3250;

}
.kanban-card{
    color: #011627;
}

/* highlights */

.roam-highlight {
    background-color: #a599e9;
}

/* reactions */

.rm-emoji-button {
    background-color: #697098 !important;
}

/* rows */
.rm-pages-row:first-of-type,
.rm-pages-row-highlight {
    background-color: #2e3250 !important;
}



.CodeMirror{
    font-family: 'Dank Mono' !important;
    height:auto;
    color:white;
    direction:ltr;
    background: #182026 !important;
    border-radius: 5px;
}
.CodeMirror-lines{
    padding:4px 0
}
.CodeMirror pre{
    padding:0 4px;
    margin-left: 5px;
}
.CodeMirror-scrollbar-filler,.CodeMirror-gutter-filler{
    background-color:white
}
.CodeMirror-gutters{
    border-right:0px solid #ddd;
    background-color:#242F38;
    white-space:nowrap;
    width: 30px;
}
.CodeMirror-linenumber{
    padding:0 3px 0 5px;
    min-width:20px;
    text-align:right;
    color:#999;
    white-space:nowrap;
    font-family:'Dank Mono';
}
.CodeMirror-guttermarker{
    color:black
}
.CodeMirror-guttermarker-subtle{
    color:#999
}
.CodeMirror-cursor{
    border-left:2px solid #394D6C;
    border-right:0;
    margin-left: 0px;
    width:0
}
.CodeMirror div.CodeMirror-secondarycursor{
    border-left:1px solid silver
}
.cm-fat-cursor .CodeMirror-cursor{
    width:auto;
    border:0 !important;
    background:#7e7
}
.cm-fat-cursor div.CodeMirror-cursors{
    z-index:1
}
.cm-fat-cursor-mark{
    background-color:rgba(20,255,20,0.5);
    -webkit-animation:blink 1.06s steps(1) infinite;
    -moz-animation:blink 1.06s steps(1) infinite;
    animation:blink 1.06s steps(1) infinite
}
.cm-animate-fat-cursor{
    width:auto;
    border:0;
    -webkit-animation:blink 1.06s steps(1) infinite;
    -moz-animation:blink 1.06s steps(1) infinite;
    animation:blink 1.06s steps(1) infinite;
    background-color:#7e7
}
@-moz-keyframes blink{
    50%{
        background-color:transparent
    }
}
@-webkit-keyframes blink{
    50%{
        background-color:transparent
    }
}
@keyframes blink{
    50%{
        background-color:transparent
    }
}
.cm-tab{
    display:inline-block;
    text-decoration:inherit
}
.CodeMirror-rulers{
    position:absolute;
    left:0;
    right:0;
    top:-50px;
    bottom:-20px;
    overflow:hidden
}
.CodeMirror-ruler{
    border-left:1px solid #ccc;
    top:0;
    bottom:0;
    position:absolute
}
.cm-s-default .cm-header{
    color:blue
}
.cm-s-default .cm-quote{
    color:#090
}
.cm-negative{
    color:#d44
}
.cm-positive{
    color:#292
}
.cm-header,.cm-strong{
    font-weight:bold
}
.cm-em{
    font-style:italic
}
.cm-link{
    text-decoration:underline
}
.cm-strikethrough{
    text-decoration:line-through
}
.cm-s-default .cm-keyword{
    color:#f19dfd
}
.cm-s-default .cm-atom{
    color:#219
}
.cm-s-default .cm-number{
    color:#164
}
.cm-s-default .cm-def{
    color:#00f
}

.cm-variable {
    color: rgb(214, 222, 235);
}

.cm-s-default .cm-variable-2{
    color: rgb(214, 222, 235);
}
.cm-s-default .cm-variable-3,.cm-s-default .cm-type{
    color: rgb(214, 222, 235);
}
.cm-s-default .cm-comment{
    color:#a50
}
.cm-s-default .cm-string{
    color:#fff
}
.cm-s-default .cm-string-2{
    color:#f50
}
.cm-s-default .cm-meta{
    color:#ffbaba
}
.cm-s-default .cm-qualifier{
    color:#555
}
.cm-s-default .cm-builtin{
    color:#3dc0ff
}
.cm-s-default .cm-bracket{
    color:#997
}
.cm-s-default .cm-tag{
    color:#170
}
.cm-s-default .cm-attribute{
    color:#00c
}
.cm-s-default .cm-hr{
    color:#999
}
.cm-s-default .cm-link{
    color:#00c
}
.cm-s-default .cm-error{
    color:red
}
.cm-invalidchar{
    color:red
}
.CodeMirror-composing{
    border-bottom:2px solid
}
div.CodeMirror span.CodeMirror-matchingbracket{
    color:#0b0
}
div.CodeMirror span.CodeMirror-nonmatchingbracket{
    color:#a22
}
.CodeMirror-matchingtag{
    background:rgba(255,150,0,.3)
}
.CodeMirror-activeline-background{
    background:#242F38;
}
.CodeMirror{
    position:relative;
    overflow:hidden;
    background:white
}
.CodeMirror-scroll{
    overflow:scroll !important;
    margin-bottom:-30px;
    margin-right:-30px;
    padding-bottom:30px;
    height:100%;
    outline:0;
    position:relative
}
.CodeMirror-sizer{
    position:relative;
    border-right:30px solid transparent
}
.CodeMirror-vscrollbar,.CodeMirror-hscrollbar,.CodeMirror-scrollbar-filler,.CodeMirror-gutter-filler{
    position:absolute;
    z-index:6;
    display:none
}
.CodeMirror-vscrollbar{
    right:0;
    top:0;
    overflow-x:hidden;
    overflow-y:scroll
}
.CodeMirror-hscrollbar{
    bottom:0;
    left:0;
    overflow-y:hidden;
    overflow-x:scroll
}
.CodeMirror-scrollbar-filler{
    right:0;
    bottom:0
}
.CodeMirror-gutter-filler{
    left:0;
    bottom:0
}
.CodeMirror-gutters{
    position:absolute;
    left:0;
    top:0;
    min-height:100%;
    z-index:3
}
.CodeMirror-gutter{
    white-space:normal;
    height:100%;
    display:inline-block;
    vertical-align:top;
    margin-bottom:-30px
}
.CodeMirror-gutter-wrapper{
    position:absolute;
    z-index:4;
    background:none !important;
    border:none !important
}
.CodeMirror-gutter-background{
    position:absolute;
    top:0;
    bottom:0;
    z-index:4
}
.CodeMirror-gutter-elt{
    position:absolute;
    cursor:default;
    z-index:4
}
.CodeMirror-gutter-wrapper ::selection{
    background-color:transparent
}
.CodeMirror-gutter-wrapper ::-moz-selection{
    background-color:transparent
}
.CodeMirror-lines{
    cursor:text;
    min-height:1px
}
.CodeMirror pre{
    -moz-border-radius:0;
    -webkit-border-radius:0;
    border-radius:0;
    border-width:0;
    background:transparent;
    font-family:'Dank Mono' !important;
    font-size:inherit;
    margin:0;
    white-space:pre;
    word-wrap:normal;
    line-height:inherit;
    color:inherit;
    z-index:2;
    position:relative;
    overflow:visible;
    -webkit-tap-highlight-color:transparent;
    -webkit-font-variant-ligatures:contextual;
    font-variant-ligatures:contextual
}
.CodeMirror-wrap pre{
    word-wrap:break-word;
    white-space:pre-wrap;
    word-break:normal
}
.CodeMirror-linebackground{
    position:absolute;
    left:0;
    right:0;
    top:0;
    bottom:0;
    z-index:0
}
.CodeMirror-linewidget{
    position:relative;
    z-index:2;
    padding:.1px
}
.CodeMirror-rtl pre{
    direction:rtl
}
.CodeMirror-code{
    outline:0
}
.CodeMirror-scroll,.CodeMirror-sizer,.CodeMirror-gutter,.CodeMirror-gutters,.CodeMirror-linenumber{
    -moz-box-sizing:content-box;
    box-sizing:content-box
}
.CodeMirror-measure{
    position:absolute;
    width:100%;
    height:0;
    overflow:hidden;
    visibility:hidden
}
.CodeMirror-cursor{
    position:absolute;
    pointer-events:none
}
.CodeMirror-measure pre{
    position:static
}
div.CodeMirror-cursors{
    visibility:hidden;
    position:relative;
    z-index:3
}
div.CodeMirror-dragcursors{
    visibility:visible
}
.CodeMirror-focused div.CodeMirror-cursors{
    visibility:visible
}
.CodeMirror-selected{
    background:#d9d9d9
}
.CodeMirror-focused .CodeMirror-selected{
    background:#d7d4f0
}
.CodeMirror-crosshair{
    cursor:crosshair
}
.CodeMirror-line::selection,.CodeMirror-line>span::selection,.CodeMirror-line>span>span::selection{
    background:#d7d4f0
}
.CodeMirror-line::-moz-selection,.CodeMirror-line>span::-moz-selection,.CodeMirror-line>span>span::-moz-selection{
    background:#d7d4f0
}
.cm-searching{
    background-color:#ffa;
    background-color:rgba(255,255,0,.4)
}
.cm-force-border{
    padding-right:.1px
}
@media print{
    .CodeMirror div.CodeMirror-cursors{
        visibility:hidden
    }
}
.cm-tab-wrap-hack:after{
    content:''
}
span.CodeMirror-selectedtext{
    background:0
}
```

- Theme - Darcula
	 - https://draculatheme.com/roam-research

	 - {{[[roam/css]]}}
		 - 
```css
/*
Dracula Theme for Roam Research v0.7.2.
Install with the Stylus extension for Chrome or Firefox.
*/

:root {
  /* Dracula color palette */
  --blue:   #8be9fd;
  --green:  #50fa7b; 
  --orange: #ffb86c;
  --pink:   #ff79c6;
  --purple: #bd93f9;
  --red:    #ff5555;
  --yellow: #f1fa8c;

  /* Dracula black & white colors */
  --background:   #282a36;
  --current-line: #44475a;
  --foreground:   #f8f8f2;
  --comment:      #6272a4;

  /* Other UI colors */
  --dark-blue:    #29454B;
  --dark-yellow:  #606438;
  --background2:  #333545;
  --foreground2:  #BDCAD4;
  --search-input: #e4e9ed;
  --search-hover: #d5dadf;
  --bullet-outer: #6c6f75;
  --bullet-inner: #D8DEE9;
  --column-title: #818D9B;
}


/* Body, topbar, sidebar */

.roam-topbar {
  background-color: var(--background);
}

.roam-body-main {
  background-color: var(--background);
  color: var(--foreground);
}

.roam-body .roam-app h1 {
  color: var(--foreground);
}

.roam-app {
  background-color: var(--background);
}

.roam-body .roam-app .roam-sidebar-container {
  background-color: var(--background2);
}

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page,
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button,
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper,
.roam-body .roam-app .roam-sidebar-container > * {
  color: var(--foreground2);
  opacity: 0.9;
}

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page:hover,
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button:hover {
  background: var(--current-line);
  color: var(--foreground);
  opacity: 0.9;
}

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button .bp3-button:hover {
  background-color: var(--foreground);
}

.roam-block-container button {
  background-color: var(--current-line);
  color: var(--foreground);
  border-color: var(--background2);
}


/* Button */

.bp3-button.bp3-minimal.bp3-small {
  color: var(--comment); 
}

.roam-block .bp3-button {
  background-color: var(--background2);
  color: var(--foreground2);
  background-image: none;
}

.roam-block .bp3-button:hover {
  background-color: var(--current-line);
  color: var(--foreground);
}

.dont-focus-block.bp3-button {
  background-color: var(--background2);
  color: var(--foreground2);
  background-image: none;
}

.dont-focus-block.bp3-button:hover {
  background-color: var(--current-line);
  color: var(--foreground);
}

/* Heading */

.rm-level3 {
  color: var(--foreground2);
}


/* Right sidebar */

#right-sidebar > div {
  background-color: var(--background2);
  color: var(--foreground)
}


/* Buffer (the help window in the bottom right corner) */

#buffer {
  background-color: var(--current-line) !important;
  color: var(--foreground) !important;
}


/* Highlights */

.roam-highlight {
  background-color: var(--dark-yellow);
}

.block-highlight-yellow {
  background-color: var(--dark-yellow);
}

.block-highlight-blue {
  background-color: var(--dark-blue);
}

.block-highlight-grey {
  background-color: var(--dark-blue);
}

/* Toast messages */

.bp3-toast.bp3-intent-success {
  background-color: var(--green);
}

.bp3-toast.bp3-intent-warning {
  background-color: var(--orange);
}


/* Sync icon */

.rm-saving-inner-icon.rm-synced {
  background-color: var(--green);
  opacity: 1;
}

.rm-saving-inner-icon.rm-saving-remote {
  background-color: var(--orange);
  opacity: 1;
}


/* External links */

a {
  color: var(--blue);
}

a:hover {
  color: var(--blue);
}


/* Reference links */

.rm-block-ref {
  border-bottom: 0.5px solid var(--current-line);
}

.rm-block-ref:hover {
  background-color: var(--background2);
}

.rm-page-ref {  
  color: var(--comment);
}

.rm-page-ref-link-color {
  color: var(--purple);
}

.rm-page-ref-brackets {
  color: var(--comment);
}


/* Reference pages */

.rm-ref-page-view-title span {
  color: var(--pink);
}

.rm-reference-item {
  background-color: var(--current-line);
}

.parent-path-wrapper {
  color: var(--foreground2);
}

.bp3-icon-standard {
  color: var(--foreground2);
}


/* Bullet points & indent lines */

.controls .simple-bullet-outer .simple-bullet-inner {
  background-color: var(--bullet-inner);
}

.roam-bullet-closed {
  background-color: var(--bullet-outer); 
}

#right-sidebar .roam-bullet-closed {
  background-color: var(--bullet-outer); 
}

.block-border-left {
  border-left: 1px solid var(--comment);
}


/* All Pages table */

.rm-pages-title-text {
  color: var(--foreground);
}

.rm-all-pages .table .rm-pages-row.rm-pages-row-header {
  background-color: var(--background2);
}

.rm-all-pages .table .rm-pages-row {
  border-bottom: 1px solid var(--background2); 
}

.rm-pages-title-col span {
  color: var(--column-title);
}

.rm-pages-col span {
  color: var(--column-title);
}

.rm-pages-title-col span.sorted-header-text {
  color: var(--foreground2);
}

.rm-pages-col span.sorted-header-text {
  color: var(--foreground2);
}

.sorting-button-group .focused::before {
  color: var(--foreground2);
}

.rm-pages-title-col a.rm-pages-title-text:hover {
  color: var(--foreground2);
}

.rm-pages-title-col span.title-children-text {
  color: var(--comment); 
}


/* All Pages checkmarks */

.bp3-control.bp3-checkbox .bp3-control-indicator {
  background-color: var(--current-line);
  border-color: var(--background2);
  background-image: none;
} 

.bp3-control.bp3-checkbox input:active ~ .bp3-control-indicator {
  background-color: var(--bullet-outer);
}

.bp3-control.bp3-checkbox input:not(:disabled):active:checked ~ .bp3-control-indicator {
  background-color: var(--bullet-outer);
}

.bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator {
  background-color: var(--dark-yellow);
} 

/* Mentions in All Pages */

.rm-clickable-pill.empty-pill {
  color: var(--foreground);
  background-color: var(--background);
}

.rm-clickable-pill {
  color: var(--background);
  background-color: var(--blue);
  opacity: 0.7;
}

.rm-clickable-pill.level1-pill {
  color: var(--background);
  background-color: var(--blue);
  opacity: 0.8;
}

.rm-clickable-pill.level2-pill {
  color: var(--background);
  background-color: var(--blue);
  opacity: 0.9;
}

.rm-clickable-pill.level3-pill {
  color: var(--background);
  background-color: var(--blue);
  opacity: 1;
}


/* Find or Create Page search box */

.bp3-input {
  background-color: var(--search-input);
  color: var(--background);
}

.bp3-menu {
  background-color: var(--search-input) !important;
  color: var(--current-line) !important;
}

.bp3-menu div:hover {
  background-color: var(--search-hover);
}

.rm-find-or-create-wrapper .rm-menu-item .rm-search-title .rm-new-page {
  color: var(--pink); 
}

.rm-find-or-create-wrapper .rm-menu-item .rm-search-list-item {
  color: var(--comment); 
}

.rm-find-or-create-wrapper .rm-menu-item ul {
  color: var(--comment);
}


/* Hover window triggered by autocompletion */

.bp3-elevation-3 {
  background-color: var(--current-line) !important;
}

.bp3-elevation-3 .dont-unfocus-block[style~="background-color:"] {
  background-color: var(--comment) !important;
}


/* Date picker */

.bp3-datepicker{
  background-color: var(--current-line);
  color: var(--foreground2);
}

.bp3-html-select.bp3-minimal.bp3-datepicker-month-select > select,
.bp3-html-select.bp3-minimal.bp3-datepicker-year-select > select {
  color: var(--foreground2);
}


/* Kanban board */

.kanban-board {
  background-color: #6c6f75;
}

.kanban-title {
  border-bottom: 1px solid var(--foreground);
}

.kanban-column {
  background-color: var(--background2);
}

.kanban-card {
  background-color: var(--background);
}


/* Filter tooltip */

.bp3-tooltip .bp3-popover-content {
  background-color: var(--current-line);
  color: var(--foreground);
}

.bp3-popover .bp3-popover-content {
  background-color: var(--current-line);
  color: var(--foreground);
}

.bp3-popover-arrow {
  color: var(--current-line);
}

.bp3-popover .bp3-popover-content .bp3-button {
  background-color: var(--background2) !important;
  color: var(--foreground) !important;
  background-image: none;
  box-shadow: none;
}


/* Embed containers */

.rm-embed-container{
  background-color: var(--background2);
}

.rm-embed-container .rm-embed-container {
  background-color: var(--current-line);
}


/* Checkmarks */

.checkmark {
  background-color: var(--current-line);
  border-color: var(--background2);
}

.check-container input:active ~ .bp3-control-indicator {
  background-color: var(--bullet-outer);
}

.check-container input:not(:disabled):active:checked ~ .bp3-control-indicator {
  background-color: var(--bullet-outer);
}

.check-container input:checked ~ .checkmark {
  background-color: var(--dark-yellow);
}


/* Sliders */

.bp3-slider-progress.bp3-intent-primary {
  background-color: var(--yellow);
}

.bp3-slider-handle {
  background-color: var(--bullet-outer);
  background-image: none;
}

.bp3-slider-handle .bp3-slider-label {
  background-color: var(--bullet-inner);
  color: var(--background2);
}


/* Inline code blocks with ` */

code {
  color: var(--orange);
  background-color: var(--current-line);
  border-color: var(--current-line);
}


/* Multiline code blocks with 
``` */

.bp3-popover-text {
  color: var(--foreground);
}

.CodeMirror {
  background-color: var(--background);
  color: var(--foreground);
  border: 2px solid var(--background2);
}

.CodeMirror-scrollbar-filler,
.CodeMirror-gutter-filler {
  background-color: var(--background);
}

.CodeMirror-gutters {
  border-right: 1px solid var(--background);
  background-color: var(--background);
}

.CodeMirror-linenumber {
  color: var(--comment);
}

.CodeMirror-guttermarker {
  color: var(--background);
}

.CodeMirror-guttermarker-subtle {
  color: var(--comment);
}

.CodeMirror-cursor {
  border-left: 1px solid var(--foreground);
}

.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid var(--current-line);
}

.cm-fat-cursor .CodeMirror-cursor {
  background: var(--bullet-inner);  /* best guess */
  color: var(--bullet-outer);       /* best guess */
}

.CodeMirror-ruler {
  border-left: 1px solid var(--current-line);
}

.cm-s-default .cm-header {
  color: var(--blue);
}

.cm-s-default .cm-quote {
  color: var(--green);  /* best guess */
}

.cm-negative {
  color: var(--red);  /* best guess */
}

.cm-positive {
  color: var(--green);  /* best guess */
}

.cm-s-default .cm-keyword {
  color: var(--pink);
}

.cm-s-default .cm-atom {
  color: var(--purple);
}

.cm-s-default .cm-number {
 color: var(--purple);
}

.cm-s-default .cm-def {
 color: var(--blue);
}

.cm-s-default .cm-variable-2 {
 color: var(--orange);
}

.cm-s-default .cm-variable-3,
.cm-s-default .cm-type {
 color: var(--green);
}

.cm-s-default .cm-comment {
  color: var(--comment);
}

.cm-s-default .cm-string {
  color: var(--yellow);
}

.cm-s-default .cm-string-2 {
  color: var(--yellow);  /* best guess */
}

.cm-s-default .cm-meta {
  color: var(--bullet-outer);  /* best guess */
}

.cm-s-default .cm-qualifier {
  color: var(--green);
}

.cm-s-default .cm-builtin {
  color: var(--green);
}

.cm-s-default .cm-bracket {
  color: var(--bullet-inner);  /* best guess */
}

.cm-s-default .cm-tag {
  color: var(--pink);
}

.cm-s-default .cm-attribute {
  color: var(--green);
}

.cm-s-default .cm-hr {
  color: var(--bullet-inner);  /* best guess */
}

.cm-s-default .cm-link {
  color: var(--blue);
}

.cm-s-default .cm-error {
  color: var(--foreground);
}

.cm-invalidchar {
  color: var(--red);
}

div.CodeMirror span.CodeMirror-matchingbracket {
  color: var(--foreground);
}

div.CodeMirror span.CodeMirror-nonmatchingbracket {
  color: var(--red);
}

.CodeMirror-matchingtag {
 background: var(--orange);  /* best guess */
}

.CodeMirror-activeline-background {
 background: var(--current-line);
}

.CodeMirror-selected {
  background: var(--current-line);
}

.CodeMirror-focused .CodeMirror-selected {
  background: var(--current-line);
}

.CodeMirror-line::selection,
.CodeMirror-line>span::selection,
.CodeMirror-line>span>span::selection {
  background: var(--current-line);
}

.CodeMirror-line::-moz-selection,
.CodeMirror-line>span::-moz-selection,
.CodeMirror-line>span>span::-moz-selection {
  background: var(--current-line);
}

.cm-searching {
  background-color: var(--dark-yellow);  /* best guess */
}
 

/* Intercom app */

.intercom-app,
.intercom-launcher-frame,
#intercom-container {
  display: none !important;
}
```

- Theme - Tags
	 - 自定义 Tag 的样式

	 - {{[[roam/css]]}}
		 - 
```css
span.rm-page-ref[data-tag="Ideas"],
span[data-link-title^="Tweet"] .rm-page-ref {
 color: #FCB815;
 padding: 3px 4px;
 font-weight: 700;
 line-height: 1.4em;
}
```

- 

- 