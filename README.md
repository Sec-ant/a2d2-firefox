# reggubed-firefox

The Firefox build that evades JavaScript anti-debugging mechanisms

## Introduction

This repository maintains a GitHub Workflow for building Firefox browsers that support replacing the [JavaScript keyword `debugger`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/debugger) with custom keywords. This customization is an efficient way to circumvent the [`debugProtection`](https://github.com/javascript-obfuscator/javascript-obfuscator#debugprotection) anti-debugging mechanism utilized by many websites, such as [weread](https://weread.qq.com/) and [mycloud](http://mcloud.to/), to protect the JavaScript code running on the client-side. By using the browser builds provided in this repository, developers can freely debug protected JavaScript code without worrying about the limitations of anti-debugging mechanisms. By default, the custom keyword is set to `reggubed`, which is the reverse spelling of `debugger`.

## References

[Evading JavaScript Anti-Debugging Mechanisms by nullptrs](https://web.archive.org/web/20211031140141/https://nullpt.rs/evading-anti-debugging-techniques/)
