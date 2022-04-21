# MobSF Enhancement Requests

Enhancement and feature requests for _[MobSF](https://mobsf.github.io/docs/)_ are listed here, and community can pick the ones they want to complete and be rewarded for completing them.

## Index

1. [Code Enhancement/Feature Requests](#code-enhancementfeature-requests)
   - [CSS file loading fail in China](#1-css-file-loading-fail-in-china)
   - [Find API keys/secrets by matching regex](#2-find-api-keyssecrets-by-matching-regex)
   - [browse all files](#3-browse-all-files)
   - [Split settings.py](#4-split-settingspy)
   - [Sticky horizontal scrollbar in code/xml views](#5-sticky-horizontal-scrollbar-in-codexml-views)

## Code Enhancement/Feature Requests

---

### **1. CSS file loading fail in China**

the page loading time is more than 15 seconds.
Because live-in China users do not access `fonts.googleapi.com` site.
Could we put the font file in the code repository or use CDN?

- **Posted by**: _[@magaofei](https://github.com/magaofei)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmobsf%2F1870">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/MobSF/Mobile-Security-Framework-MobSF/issues/1870)**

---

### **2. Find API keys/secrets by matching regex**

**If you're requesting a new feature/enhancement, explain why you'd like it to be added and it's importance.**

We currently have a feature which find possible hardcoded secrets. But there could be false positives. So I am suggesting a feature which will use regex to find API keys. I currently have a command line program called dora which does exactly this. But would of course be very nice if this was implemented into this program so we'd get exact matches to those API keys/secrets.

**Is your feature request related to a problem? Please describe.**
It is not a problem.

**Describe the solution you'd like**
Use a list of regex that match certain API keys/secrets so they will be found without any false positives. I am willing to provide the regex patterns if needed.

**Describe alternatives you've considered**
I currently use my program called dora but if MobSF had this inbuilt, it would be ease my workflow.

- **Posted by**: _[@sdushantha](https://github.com/sdushantha)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmobsf%2F1843">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/MobSF/Mobile-Security-Framework-MobSF/issues/1843)**

---

### **3. browse all files**

**Is your feature request related to a problem? Please describe**.
I would like to see the source code for other files besides java and smali, i.e. html. Or download binary files (images, shared objects and so on).

**Describe the solution you'd like**
Allow the browser access all sorts of files

- **Posted by**: _[@elig0n](https://github.com/elig0n)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmobsf%2F1724">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/MobSF/Mobile-Security-Framework-MobSF/issues/1724)**

---

### **4. Split settings.py**

**If you're requesting a new feature/enhancement, explain why you'd like it to be added and it's importance.**

**Is your feature request related to a problem? Please describe.**
`settings.py` hosts both required MobSF/Django config and local config.
Each time MobSF version is updated, need to merge local settings (e.g., `USE_HOME`, DB config, `ALLOWED_HOSTS`) into the updated `settings.py`

~/MobSF/config.py allows for customizing some values, but can't host Django settings.

**Describe the solution you'd like**
Split the file into settings.py and local_settings.py (ideally loaded from `~/.MobSF`).

**Describe alternatives you've considered**
Manual merge

**Additional context**
Django wiki about splitting settings: https://code.djangoproject.com/wiki/SplitSettings

- **Posted by**: _[@nelenkov](https://github.com/nelenkov)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmobsf%2F1697">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/MobSF/Mobile-Security-Framework-MobSF/issues/1697)**

---

### **5. Sticky horizontal scrollbar in code/xml views**

**Is your feature request related to a problem? Please describe.**
When some lines exceed the viewport width inside the source and smali code views or the Manifest XML view, a horizontal scrollbar is shown.
The problem is, it's all at the bottom of the view which forces the user to scroll all way down to adjust the horizontal scroll.
This interrupts the workflow and is distracting because you have to guess what width is needed to view a specific part of the line.

**Describe the solution you'd like**
The horizontal scrollbar might be set to stick at the page bottom if it would be outside the viewport otherwise.

- **Posted by**: _[@serkonda7](https://github.com/serkonda7)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmobsf%2F1693">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/MobSF/Mobile-Security-Framework-MobSF/issues/1693)**

---
