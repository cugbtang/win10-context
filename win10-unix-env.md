# Windows 下的类 UNIX 环境

## 时间轴

cygwin ---> mingw ---> mingw-w64 ---> msys ---> msys2---> git

## 详细描述

- Cygwin

  > ​		Cygwin 是一个 Windows 下的类 UNIX 环境。Cygwin 移植了大部分 Linux 下的软件，包括但不局限于 Bash、GCC、Git 和 VIM，甚至 GNOME 和 KDE 这类图形。

  

- [MinGW-w64](https://www.zhihu.com/search?q=MinGW（-w64&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A932543527})

  > ​        在很 久以前，世界上还只有 Cygwin 的 1.3.3（现在已经是 3.0.7 了）。虽然当时 Cygwin 还刚刚开始发展，但是其缺点却已经暴露出来了：它实在太大了！所以，一小撮想搞事情的程序员站了出来，fork 了 Cygwin 的 GCC 和相关库文件，并且将它们魔改了一番，使得 GCC 能使用 Windows 的 Visual C++ API。这就成了 MinGW。后来，因为 MinGW 一直没有发展，所以出现了 TDM-GCC 和 [MinGW-w64](https://www.zhihu.com/search?q=MinGW-w64&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A932543527}) 两个给 MinGW 续命的项目，TDM-GCC 现在也没落了（可见人类的本质是鸽子），而 MinGW-w64 却给 MinGW 续命成功，一直紧跟着官方 GCC 更新到了现在。
  >
  > 

- MSYS（2）

  > ​		当 MinGW 出现之后，程序员们发现光有 GCC 不行啊，面对着如此 naive 的 Windows 命令行也照样不能干活，Cygwin 又太大了。所以 MinGW 的一群人再次 fork 了 Cygwin，把它精简了一番，就成了 MSYS。后来，MinGW 没落了，MSYS 也随之没落了。
  >
  > ​		又一群程序员 fork 了新版本的 Cygwin，精简了一番，给它加上了 Pacman 包管理器（没错就是 Arch Linux 用的那个），最后给 MSYS 的名字后面加了个 2，成了 MSYS2。
  >
  > 

- Git for Windows 

  > ​		随着 Git 的快速完善，将 Git 移植到 Windows 的呼声越来越高，可是 Git 需要很多 Linux 下的命令行工具，所以不想重复造轮子的 Git 开发者们找到了 MSYS2，又将 MSYS2 做了一番精简和针对 Git 的修改，把 Git 放了进去。
  >
  > 

-  WSL

  > ​		WSL 和上述没有任何关系，这是我们的巨硬微软感觉 Linux 的那一套很吼哇，就搞来 Linux 内核进行了一番魔改，在加上了一些针对 Windows 的处理，bling! 的一声，就有了跑在 Windows 下了 Linux。当然因为也有类似 Cygwin 的模拟，所以在磁盘性能方面较慢，比起 Cygwin 差多了。好处在于 它提供了较为原汁原味的 Linux 环境。
  >
  > ​		当然 WSL 也在进步，WSL 2 直接搞了个虚拟机跑原生的 Linux 内核，再加上一些可以较完美地整合 Linux 的修改，这样做性能就可以提高很多。可惜我并不想用 Windows Insider，WSL 2 也暂时没法用。

  

## ref

[在windows下为什么装了git bash等工具后就能执行linux命令?](https://www.zhihu.com/question/65055974/answer/932543527)