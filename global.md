# 目录
+ [Global Objects](./global.md#1)
    - [global](./global.md#2)
    - [process](./global.md#3)
    - [console](./global.md#4)
    - [Class:Buffer](./global.md#5)
    - [require()](./global.md#6)
        + [require.resolve()](./global.md#7)
        + [require.cache](./global.md#8)
        + [require.extensiions](./global.md#9)
    - [__filename](./global.md#10)
    - [__dirname](./global.md#11)
    - [module](./global.md#12)
    - [exports](./global.md#13)
    - [setTimeout(cb,ms)](./global.md#14)
    - [clearTimeout(t)](./global.md#15)
    - [setInterval(cb,ms)](./global.md#16)
    - [clearInterval(t)](./global.md#17)
    
# <a name="1">Global Objects
这些模块在所有的模块中都可以使用，需要注意的是其中一些并不是全局范围的，二是模块范围的

## <a name="2">global 
  + {Object}全局命名空间对象  
在浏览器中，最顶层的作用范围就是全局范围。也就意味着在浏览器中在全局范围<small>var something</small>将会定义一个全局变量。而在Node中则不同，最顶层的作用范围不是全局范围，在Node模块中<small>var something</small>只会定位到那个模块

## <a name="3">process
 + {Object}  
process对象，参考[process objec](#)板块

## console
 + {Object}  
用于打印到标准输出和标准错误输出，参考[console](../console.md)模块

## Class:Buffer
 + {Function}  
用于处理二进制数据，参考[buffer](#)模块

## require()
 + {Function}  
用于加载模块，参考[Modules]模块。