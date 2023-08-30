# {Anti {{Anti Debugging} Debugger}} Firefox

<img alt="anti-anti-debugging-debugger-firefox-demo" src="https://user-images.githubusercontent.com/10386119/234786387-dede6c9e-57d1-4ee1-80c8-adfc65276df1.gif" width=75% >

The Firefox build that evades JavaScript anti-debugging `debugger` mechanisms.

## Introduction

This repository provides GitHub Workflows to build Firefox browsers that replace the [JavaScript `debugger`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/debugger) with custom keywords. This bypasses the [`debugProtection`](https://github.com/javascript-obfuscator/javascript-obfuscator#debugprotection) used by websites like [weread](https://weread.qq.com/) and [mycloud](http://mcloud.to/) to secure their JavaScript code. Using these browser builds, developers can debug protected code without `debugProtection` constraints. The default keyword is `debugger[%Y%m%d%H%M%S]`, where `[%Y%m%d%H%M%S]` is a build-time timestamp, e.g., `20230427040458`. The workflow also allows for the customization of the `debugger` keyword.

## Download & Install

You can download the Firefox installer from [Github Actions](https://github.com/Sec-ant/anti-anti-debugging-debugger-firefox/actions/workflows/build.yml) artifacts (look for `firefox-artifacts`), or from the [releases](https://github.com/Sec-ant/anti-anti-debugging-debugger-firefox/releases).

## Fork

If you would like to fork this repo and run the actions under your account, please be aware that you need to create a [personal access token](https://github.com/settings/tokens?type=beta) (follow the [instructions here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)) and grant it permissions of **Read and Write access to code** in your repo. And add this access token to your repo secrets (`https://github.com/{OWNER}/{REPO}/settings/secrets/actions`) with the name `ACTIONS_TRIGGER_PAT` (this name is used in the workflow files). You'll also have to grant **Read and write permissions** to your workflow (`https://github.com/{OWNER}/{REPO}/settings/actions`). All the hassle here is to automatically trigger build at least once a day upon new commit in the Firefox source code.

## References

[Evading JavaScript Anti-Debugging Mechanisms by nullptrs](https://web.archive.org/web/20211031140141/https://nullpt.rs/evading-anti-debugging-techniques/)
