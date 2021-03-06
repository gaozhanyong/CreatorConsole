# CreatorConsole 游戏内置控制台

**CreatorConsole**是一款支持在CocosCretor游戏运行时启动控制台的插件，该插件具有以下特性：
 
- **内置输出** ：虽然WEB的浏览器控制台很方便，但原生输出的话，开发者是无法直观地看到调试输出的，因此，直接在游戏内部可视化输出日志就相当方便了；
- **支持命令** ：除了日志输出外，`CreatorConsole`还支持自定义命令，就跟shell一样，你可以实时输入命令来控制程序，例如键入`'cl'`，可实现清屏；
- **开放源码** ：由于是开放源码的，因此你可以自由地拓展功能，例如定义更多的命令等。

-------------

## 使用说明

> - 安装
> - 在场景中使用
> - 在代码中使用
> - 命令

### 安装
    从[GitHub](https://github.com/jeason1997/CreatorConsole)上下载Zip文件，解压，覆盖到你的项目目录下。

### 在场景中使用
    打开项目，将Asset/Plugins/CreatorConsole/Console.prefab拖入到场景中
> 注意：`Console.prefab` 拖入场景后一定要至于节点层级的最顶层，确保`console.js`最先被加载。

![Scene](http://cdn.cocimg.com/bbs/attachment/Fid_71/71_412843_840a55f61031574.png)

### 在代码中使用
``` javascript
// 像平常一样直接输出即可
cc.log('Hello World');
cc.warn('Warning!');
cc.error('Fucking!');
```

### 命令
| Command               | Describe |
| :--------             | --------:|
| Help                  | 显示帮助，列出所有命令 |
| Cl                    | 清空屏幕|
| E [script]            | 执行脚本，例如`'E var i = 10;'`|
| Q                     | 退出控制台 |
![Command](http://cdn.cocimg.com/bbs/attachment/Fid_71/71_412843_36b3e0133ee3a8a.png)