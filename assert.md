# 目录
+ [Assert]()
 - [assert.fail(actual,expected,message,operator)]()
 - [assert(value[,message]),assert.ok(value[,message])]()
 - [assert.equal(actual,expected[,message])]()
 - [assert.notEqual(actual,expected(,message))]()
 - [assert.deepEqual(actual,expected[,message])]()
 - [assert.strictEqual(actual,expected[,message])]()
 - [assert.notStrictEqual(actual,expected[,message])]()
 - [assert.throws(block[,errot][,message])]()
 - [assert.doesNotThrow(block[,message])]()
 - [assert.ifError(value)]()

# Assert
    稳定性：5 - 锁定状态
该模块用于单元测试，可以通过require('assert')引入
## asser.fail(actual,expected,message,operator)
抛出一个异常，用提供的operator来分开真实值和期望值
##assert(value[,message]),assert.ok(value[,message])
测试值是否为真，和assert.equal(true, !!value, message)等效
## assert.equal(actual,expected[,message])
测试相等，和==比较操作符一样
## assert.notEqual(actual,expected[,message])