This is no longer needed because firefox 121 introduced an option to disable the debugger statement: https://www.mozilla.org/en-US/firefox/121.0/releasenotes/#note-789917

# {Anti {{Anti Debugging} Debugger}} Firefox

[![Build Firefox on All Platforms](https://github.com/Sec-ant/a2d2-firefox/actions/workflows/build.yml/badge.svg)](https://github.com/Sec-ant/a2d2-firefox/actions/workflows/build.yml)

<img alt="a2d2-firefox-demo" src="https://user-images.githubusercontent.com/10386119/234786387-dede6c9e-57d1-4ee1-80c8-adfc65276df1.gif" width=75% >

The Firefox build that evades JavaScript anti-debugging `debugger` mechanisms.

## Introduction

This repository provides GitHub Workflows to build Firefox browsers that replace the [JavaScript `debugger`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/debugger) with custom keywords. This bypasses the [`debugProtection`](https://github.com/javascript-obfuscator/javascript-obfuscator#debugprotection) used by websites like [weread](https://weread.qq.com/) and [mycloud](http://mcloud.to/) to secure their JavaScript code. Using these browser builds, developers can debug protected code without `debugProtection` constraints. The default keyword is `debugger[%Y%m%d%H%M%S]`, where `[%Y%m%d%H%M%S]` is a build-time timestamp, e.g., `20230427040458`. The workflow also allows for the customization of the `debugger` keyword.

## Download & Install

You can download the Firefox installer from [Github Actions](https://github.com/Sec-ant/a2d2-firefox/actions/workflows/build.yml) artifacts (look for `firefox-artifacts`), or from the [releases](https://github.com/Sec-ant/a2d2-firefox/releases).

## References

[Evading JavaScript Anti-Debugging Mechanisms by nullptrs](https://web.archive.org/web/20211031140141/https://nullpt.rs/evading-anti-debugging-techniques/)
