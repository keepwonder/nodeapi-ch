# 概要

用Node编写web服务器，打印出Hello World。

    var http = require('http');

    http.createServer(function (request,response) {
        response.writeHead(200,{'Content-Type':'text/plain'});
        reponse.end('hello world\n');
        }).listen(8127);

        console.log('Sercer running at http://127.0.0.1:8127');

怎样运行服务呢？把上述代码保存在example.js文件中，并运行下面node程序  
                
        >node exmaple.js
        Server running at http://127.0.0.1:8127;

文档中的所有示例的运行都与此类似

