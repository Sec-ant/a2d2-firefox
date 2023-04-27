# <img alt="firefox" src="https://user-images.githubusercontent.com/10386119/234802229-84233a0d-bcc5-4d4a-ad13-ec0a1be46510.png" width=64px > {anti-{{anti-debugging}-debugger}}-firefox 



<img alt="anti-anti-debugging-debugger-firefox-demo" src="https://user-images.githubusercontent.com/10386119/234786387-dede6c9e-57d1-4ee1-80c8-adfc65276df1.gif" width=50% >

The Firefox build that evades JavaScript anti-debugging `debugger` mechanisms.

## Introduction

This repository maintains GitHub Workflows for building Firefox browsers (in Windows only, as of now) that support replacing the [JavaScript keyword `debugger`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/debugger) with custom keywords. This customization is an efficient way to circumvent the [`debugProtection`](https://github.com/javascript-obfuscator/javascript-obfuscator#debugprotection) anti-debugging mechanism utilized by many websites, such as [weread](https://weread.qq.com/) and [mycloud](http://mcloud.to/), to protect their client-side JavaScript code. By using the browser builds provided in this repository, developers can freely debug protected JavaScript code without worrying about the limitations brought by `debugProtection`. By default, the custom keyword is set to `debugger[%Y%m%d%H%M%S]`, where `[%Y%m%d%H%M%S]` is a timestamp acquired during the build process, e.g. `20230427040458`.

## Download & Install

You can download the Firefox installer from [Github Actions](https://github.com/Sec-ant/anti-anti-debugging-debugger-firefox/actions/workflows/build.yml) artifacts (look for `firefox-artifacts`), or from the [releases](https://github.com/Sec-ant/anti-anti-debugging-debugger-firefox/releases).

## Fork

If you would like to fork this repo and run the actions under your account, please be aware that you need to create a [personal access token](https://github.com/settings/tokens?type=beta) (follow the [instructions here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)) and grant it permissions of **Read and Write access to code** in your repo. And add this access token to your repo secrets (`https://github.com/{OWNER}/{REPO}/settings/secrets/actions`) with the name `ACTIONS_TRIGGER_PAT` (this name is used in the workflow files). You'll also have to grant **Read and write permissions** to your workflow (`https://github.com/{OWNER}/{REPO}/settings/actions`). All the hassle here is to automatically trigger build at least once a day upon new commit in the Firefox source code.

## References

[Evading JavaScript Anti-Debugging Mechanisms by nullptrs](https://web.archive.org/web/20211031140141/https://nullpt.rs/evading-anti-debugging-techniques/)

