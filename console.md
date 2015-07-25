# 目录
+ [console](./console.md#1)
 - [console.log([data][,...])](./console.md#2)
 - [console.info([data][,...])](./console.md#3)
 - [console.error([data][,...])](./console.md#4)
 - [console.warn([data][,...])](./console.md#5)
 - [console.dir(obj[,options])](./console.md#6)
 - [console.time(label)](./console.md#7)
 - [console.timeEnd(label)](./console.md#8)
 - [console.trace(message[,...])](./console.md#9)
 - [console.assert(value[,message][,...])](./console.md#10)

# <a name="1">console
    稳定性：4 - API冻结状态

 - object 
为了打印标准输出和标准错误输出，和大多数web浏览器提供的console函数类似，这里的输出也是发送的标准输出或者标准错误输出

当目标是一个终端或者一个文件是console函数是同步的(避免提前退出丢失信息)，而以管道形式时则是异步的(避免长时间阻塞)

比如，在下面的例子当中，标准输出是非阻塞的而标准错误输出则是阻塞的

    $ node script.js 2>error.log | tee info.log
平常使用时，如果不是需要记录大量的日志数据，则不需要关心阻塞/非阻塞

## <a name="2">console.log([data][,...])
以新的一行的方式标准输出。像printf()一样可以接受多个参数。例如
    
    var count = 5;
    console.log('count: %d',count);
    //prints 'count: 5'
如果在第一个string参数中没有找到格式化元素，每个参数则会调用util.inspect.更多信息参考[util.format()](#).

## <a name="3">console.info([data][,...])
和console.log用法一样

## <a name="4">console.error([data][,...])
和console.log用法一致，不同的是打印到标准错误输出

## <a name="5">console.warn([data][,...])
和console.error用法一致

## <a name="6">console.dir(obj[,options])
obj使用util.inspect,将结果字符串打印到标准输出.

## <a name="7">console.time(label)
标记一个时间

## <a name="8">console.timeEnd(label)
结束计时器，记录输出，例如：
    
    console.time('100-elements');
    for(var i = 0;i < 100; i++){
        ;
    }
    console.timeEnd('time-elements');
    //prints 100-elements: 262ms

## <a name="9">console.trace(message[,...])
打印到标准错误输出

## <a name="10">console.assert(value[,message][,...])
和console.ok()类似，但是错误信息根据[util.format(message...)](#)格式化了