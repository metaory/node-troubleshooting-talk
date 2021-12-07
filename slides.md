---
theme: unicorn
background: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
highlighter: shiki
lineNumbers: true
handle: 'metaory'
website: 'github.com/metaory'
# gradientColors: ['#001CAF', '#5B21B6']
drawings:
  persist: false
---

# Web Troubleshooting

Tips and Tricks

---

# Hi, there!

<br>
<br>

- 😀 My name: **Pou Yan**
- 🧠 I'm a: **Solution Architect**
- ⛏  My hobby: **Hacking and Writing**
- 🏢 Currently working for: **[HelloGold.com](https://hellogold.com)**

<br>
<br>

Follow me on [Github](https://github.com/metaory) 👋

---
src: ./intro.md
---

---

# Terminology

<div v-click class="text-xl p-2"><b>Debugger</b> – A debugging tool that allows you to see internal variable states by running code line by line</div>
<div v-click class="text-xl p-2"><b>Frequency</b> – How frequently or under what circumstances a bug will appear</div>
<div v-click class="text-xl p-2"><b>Logic error</b> – The program works, but it doesn't do what it's supposed to do</div>
<div v-click class="text-xl p-2"><b>Race condition</b> – Bugs that are difficult to track are those that are reliant on the sequence or timing of uncontrollable events</div>
<div v-click class="text-xl p-2"><b>Regression</b> – A previously repaired bug reappears, possibly as a result of other updates</div>
<div v-click class="text-xl p-2"><b>Stack trace</b> – The list of all methods that were called before the error</div>

<br>

---
layout: cover-logos
logos: [
  'https://cdn1.iconfinder.com/data/icons/aami-web-internet/64/aami2-90-512.png',
  'https://cdn1.iconfinder.com/data/icons/aami-web-internet/64/aami2-100-512.png',
  'https://cdn3.iconfinder.com/data/icons/aami-web-internet/64/aami5-44-256.png',
]
---


|                     |                                |
| ---                 | ---                            |
| <kbd>PREVENT</kbd>  | Linters, git Hooks, Unit tests |
| <kbd>INSPECT</kbd>  | Logs, CLI, Browser, Editor     |
| <kbd>IDENTIFY</kbd> | Sentry, Rollbar, TrackJs       |


---
layout: new-section
sectionImage: 'https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/section-illustration.svg'
---
<h1>Prevent</h1>

---
layout: intro
introImage: https://miro.medium.com/max/398/1*TPkhIqPgVzFSSpwdlVwhVw.png
---
# Use a Linter

### Find and fix problems in your JavaScript code.

---
layout: intro
introImage: https://miro.medium.com/max/1400/1*Rj3iVwEKZMiRhcEsjh45Kg.png
# introImage: https://pbs.twimg.com/media/EbHalBQXYAE1XwD.jpg
---

# Use Unit tests

### Tests can't fail if you don't run any.

---
layout: intro
introImage: https://dev-to-uploads.s3.amazonaws.com/i/96jxo85imhaa25xhi44k.png
---
# Use Git hooks

### Husky improves your commits and more!

#### woof!

---
layout: new-section
sectionImage: 'https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/section-illustration.svg'
---
# Logs

---

# console.group
[console.group() - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/console/group)

<div grid="~ cols-2 gap-2" m="-t-2">
  <img v-click border="rounded" width="500" src="https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/carbon-console-group-1.png">
  <img v-click border="rounded" width="500" src="https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/carbon-console-group-2.png">
</div>

---

# console.table
[console.table() - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/console/table)

<div grid="~ cols-2 gap-2" m="-t-2">
  <img v-click border="rounded" width="500" src="https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/carbon-console-table-1.png">
  <img v-click border="rounded" width="500" src="https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/carbon-console-table-2.png">
</div>
---

# colorful console

```js
console.log('%c Oh my heavens! ', 'background: #222; color: #bada55');
```
<br>

<div grid="~ cols-2 gap-2" m="-t-2">
  <img v-click border="rounded" width="500" src="https://i.stack.imgur.com/gvpgF.png">
  <img v-click border="rounded" width="500" src="https://i.stack.imgur.com/DFJBd.png">
</div>
---

```bash
python -0 assert.py
```

<div grid="~ cols-2 gap-2" m="-t-2">
  <img v-click border="rounded" width="500" src="https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/carbon-python-assert.png">
</div>

## Python’s build-in assert method can raise an AssertionError if its statement is False .
---
layout: intro
introImage: https://png.pngtree.com/png-clipart/20190516/original/pngtree-log-file-document-icon-png-image_4180597.jpg
---

# Distributed Logging and Tracing

### As systems grows bigger, the visibility gap grows.

---
layout: new-section
sectionImage: 'https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/section-illustration.svg'
---
# Inspect

---

# CLI Options

|                                    |                                                             |
| ---                                | ---                                                         |
| <code>-\-enable-source-maps</code> | enable source maps                                          |
| <code>-\-throw-deprecation</code>  | throw on deprecated features                                |
| <code>-\-inspect</code>            | activate the V8 inspector                                   |
| <code>-\-inspect-brk</code>        | activate the V8 inspector and break on first statement      |
| <code>inspect</code>               | starts with CLI client                                      |
| <code>debug</code>                 | The legacy debugger has been deprecated as of Node.js 7.7.0 |

---

# CLI Inspect

[Full Debugger Specification](https://nodejs.org/api/debugger.html)
```bash {none|all}
node inspect script.js
```

```bash {none|1|all}
import pdb; pdb.set_trace()
python3 -m pdb script.py
```

```yaml {none|1-4|6-7|9-10|12-15|all}
  cont, c               # Resume execution
  next, n               # Continue to next line in current file
  step, s               # Step into, potentially entering a function
  out, o                # Step out, leaving the current function

  backtrace, bt         # Print the current backtrace
  list                  # Print the source around the current line where execution

  setBreakpoint, sb     # Set a breakpoint
  clearBreakpoint, cb   # Clear a breakpoint

  breakpoints           # List all known breakpoints
  breakOnException      # Pause execution whenever an exception is thrown
  breakOnUncaught       # Pause execution whenever an exception isn't caught
  breakOnNone           # Don't pause on exceptions (this is the default)
```

---
layout: cover-logos
logos: [
  'https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Chrome_icon_%28September_2014%29.svg/2048px-Google_Chrome_icon_%28September_2014%29.svg.png',
  'https://upload.wikimedia.org/wikipedia/commons/thumb/f/fe/Chromium_Material_Icon.svg/1200px-Chromium_Material_Icon.svg.png',
  'https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/Firefox_logo%2C_2019.svg/1200px-Firefox_logo%2C_2019.svg.png',
]
---
# Nodejs Browser Inspect

[Chrome DevTools Protocol](https://chromedevtools.github.io/devtools-protocol/)
```bash {none|all}
node --inspect-brk script.js
```

```bash {none|all}
chrome://inspect
```

<p v-click> by default Debugger will start listening on <b>ws://127.0.0.1:9229</b> </p>

---

# Remote Browser Inspect

<div v-click><h3>ssh to remote machine</h3></div>
```bash {none|all}
ssh -i KEYFILE SERVER-USER@SERVER-IP
```

<div v-click><h3>start application inspector flag </h3></div>

```bash {none|all}
node --inspect-brk server.js
```
<br>

<div v-click><h4>start ssh tunnel session where a connection to port 9221 on your local machine will be forwarded to port 9229</h4></div>
```bash {none|all}
ssh -N -L 9221:127.0.0.1:9229 -i KEYFILE SERVER-USER@SERVER-IP
```


```bash {none|all}
ssh -N -L 9221:localhost:9229 -i ~/.ssh/mykey.pem ec2-user@22.222.222.22
```


---
layout: new-section
sectionImage: 'https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/section-illustration.svg'
---
# Identify

---

# Exception Monitoring tools
[stackshare.io/exception-monitoring](https://stackshare.io/exception-monitoring)

<div grid="~ cols-3 gap-2" m="-t-2">
  <img v-click border="rounded" width="260" src="https://mms.businesswire.com/media/20210216005484/en/859303/23/New_Rollbar_LOGO.jpg">
  <img v-click border="rounded" width="150" src="https://res.cloudinary.com/crunchbase-production/image/upload/c_lpad,f_auto,q_auto:eco,dpr_1/uq1w4cehiz1z09tdedjl">
  <img v-click border="rounded" width="260" src="https://vectorlogoseek.com/wp-content/uploads/2020/02/sentry-io-vector-logo.png">
</div>

---

# Application Performance Monitoring tools (APM)
[stackshare.io/application-performance-monitoring](https://stackshare.io/stacks/application-performance-monitoring)

<div grid="~ cols-4 gap-2" m="-t-2">
  <img v-click border="rounded" width="260" src="https://img.favpng.com/3/22/15/new-relic-web-development-business-amazon-web-services-png-favpng-cayg8S5dWEsDCvectkcw4YxzH.jpg">
  <img  v-click border="rounded" width="150" src="https://ms-f7-sites-01-cdn.azureedge.net/docs/stories/1408635292023828373-dynatrace-other-azure-en-united-states/resources/6c48e916-5bc8-438d-b3b1-a952dc66cfe9/1408638336458751638_1408638336458751638">
  <img v-click border="rounded" width="200" src="https://dv-website.s3.amazonaws.com/uploads/2017/06/ns.png">
  <img v-click border="rounded" width="260" src="https://vectorlogoseek.com/wp-content/uploads/2020/02/sentry-io-vector-logo.png">
</div>

---
layout: image-center
image: 'https://www.nodesource.com/assets/nsolid/hero-nsolid-home.png'
---
# NODESOURCE NSolid

---
layout: new-section
sectionImage: 'https://raw.githubusercontent.com/metaory/node-troubleshooting-talk/master/public/section-illustration.svg'
---
## [Self-Hosted Sentry](https://develop.sentry.dev/self-hosted/)

<br>
<br>

## [Self-Hosted NSolid](https://docs.nodesource.com/nsolid)


---
layout: center
website: 'github.com/metaory'
class: text-center
---

# Thank You

---
layout: image-center
image: 'https://miro.medium.com/max/1500/1*Tnkk12VxGlyvx_7LBbpnOw.jpeg'
---
