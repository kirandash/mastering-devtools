# MASTERING DEV TOOLS

## 1 Intro
### 1.1 Resources
- Slides: https://slides.com/jkup/devtools/
- Tutorial: http://masteringdevtools.com/
- Official docs: https://developer.chrome.com/docs/devtools/

### 1.2 History of debugging
- Live DOM Viewer (https://software.hixie.ch/utilities/js/live-dom-viewer/)
- Firebug (Firefux extension)

### 1.3 Developer tool panels
- To open dev tools: `Cmd + Optn  + I`
- The panels are draggable and can be re positioned
- To expand all child of a DOM node: `Option + left Click`
- Panels: Element, console, sources, network, performance, memory, application, security, lighthouse(audits)
- Additional drawer: press `esc` on any tab other than console tab

## 2 Editing
-  You can use Chrome DevTools as a full time IDE
-  It can do a bunch of amazing things, such as:
    - Edit HTML and CSS

### 2.1 Elements Styles
- Chrome shows google **material ui palette** and also** page palette**
- on elements screen, to go to a specific element: click: **"Scroll into view"**
- **Hide  and how elements**: press `H` key or click: **Hide element** by right click

### 2.2 Specificity and DOM nodes
- Styles, Computed, Event Listeners
    - in styles: for colors: we can change b/w rgb and hsl etc by clicking "**Shift + Click"** or manually change by left clicking

### 2.3 DOM breakpoints
- Select element
    - Right click and choose **"break on"**
        - subtree modifications
        - attribute modifications
        - node removal
- Ex: Choose **attribute modifications** to set a breakpoint on class change. it will auto open the file as well which is causing the class change.

### 2.4 Saving changes in Workspace
- We can add our source code folder to chrome source file system workspace. And chrome will try to sync source code with the files loaded by the website. And I can change content from dev tools and it will save changes in workspace.
- Sources ---> **"File System"** tab --->** "Add folder to workspace"** ---> Click and choose the folder of our project
- Once added, the files that are synced will have a **green dot** to indicate that the file is in sync with disk.
- Now if I edit file content from dev tools, **it will change file content on your disk**.
- Note: Changes in element tab won't persist. Only changes in sources tab and in Styles tab for mapped files will persist.
- Support: Currently it supports css,html, sass.
    - not good support for build tools like webpack and cra etc

### 2.5 Recent Selection History
- Element tab: Select a DOM element
- Click escape to open console or manually move to console tab
- Enter **`$0`** iin console.
- It will move the recent selection element to console.
- The history goes up to 3 like `$1`, `$2`, `$3`

### 2.5.1 jQuery like selectors built in Chrome
- DOM also provides jQuery like selectors in console ex: `$(".nav")`

## 3 Debugging
