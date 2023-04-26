# reggubed-firefox

The Firefox build that evades JavaScript anti-debugging mechanisms

## Introduction

This repo holds a workflow to build Firefox browsers in which the [JavaScript keyword `debugger`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/debugger) can be replaced with custom words (default to `reggubed`, `debugger` in reverse order). This is by far the most efficient way to evade JavaScript [debugger loops](https://github.com/javascript-obfuscator/javascript-obfuscator#debugprotection), the anti-debugging mechanism that is utilized in many websites, e.g. [weread](https://weread.qq.com/), [mycloud](http://mcloud.to/), to prevent people from debugging their clientside protected code.

## References

[Evading JavaScript Anti-Debugging Mechanisms by nullptrs](https://web.archive.org/web/20211031140141/https://nullpt.rs/evading-anti-debugging-techniques/)
