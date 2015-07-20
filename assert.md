# 目录
+ [Assert](#1)
 - [assert.fail(actual,expected,message,operator)](#2)
 - [assert(value[,message]),assert.ok(value[,message])](#3)
 - [assert.equal(actual,expected[,message])](#4)
 - [assert.notEqual(actual,expected(,message))](#5)
 - [assert.deepEqual(actual,expected[,message])](#6)
 - [assert.notDeepEqual(actual,expected[,message])](#7)
 - [assert.strictEqual(actual,expected[,message])](#8)
 - [assert.notStrictEqual(actual,expected[,message])](#9)
 - [assert.throws(block[,errot][,message])](#10)
 - [assert.doesNotThrow(block[,message])](#11)
 - [assert.ifError(value)](#12)

# Assert(#1)
    稳定性：5 - 锁定状态
该模块用于单元测试，可以通过require('assert')引入
## asser.fail(actual,expected,message,operator)(#2)
抛出一个异常，用提供的operator来分开真实值和期望值
##assert(value[,message]),assert.ok(value[,message])(#3)
测试值是否为真，和assert.equal(true, !!value, message)等效
## assert.equal(actual,expected[,message])(#4)
测试是否相等，和==比较操作符一样
## assert.notEqual(actual,expected[,message])(#5)
测试是否不等，和!=比较操作符一样
## assert.deepEqual(actual,expected[,message])(#6)
测试是否全等
## assert.notDeepEqual(actual,expected[,message])(#7)
测试是否不全等
## assert.strictEqual(actual,expected[,message])(#8)
测试是否严格相等，和===比较操作符一样
## assert.notStrictEqual(actual,expected[,message])(#9)
测试不严格相等，和!==比较操作符一样
## assert.throws(block[,error][,message])(#10)
期待block抛出一个错误，错误可以是构造器，正则表达式或者验证函数

使用构造器验证：

    assert.throws(
        function() {
            throw new Error("Wrong value");
            },
            Error
        );

使用正则验证错误信息：

    assert.throws(
        function() {
            throw new Error("Wrong value");
            },
            /value/
        );

客户端错误验证

    assert.throws(
        function() {
            throw new Error("Wrong value");
            },
            function(err) {
                if( (err instanceof Error) && /value/.test(err) ){
                    return true;
                }
            },
            "unexpected error";
        );

## asset.doesNotThrow(block[,message])(#11)
期望代码块不抛出错误，详见assert.throws
## assert.ifError(value)(#12)
测试值是否不是一个假值，如果是真值则抛出错误，在测试回调函数第一个参数error时非常有用