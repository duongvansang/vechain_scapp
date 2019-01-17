Morpheus Examples Project
====


## 安装NPM依赖

    npm install


## Truffle集成使用

开发工具调用栈图如下，

![develop-stack](images/development-stack.jpg)


使用`Ethereum Truffle`要求开发者安装和运行`Web3-Gear`程序，该程序是一层`VeChainThor Network`的透明代理程序，可以将以太坊JSON-RPC调用转换成`VeChainThor Network`的`RESTful API`协议。

`Web3-Gear`的安装过程这里就不再赘述，最关键的地方就是`truffle-config.js`配置文件要连接`Web3-Gear`节点。

    vim truffle-config.js

    networks: {
        development: {
            host: "localhost", // web3-gear host
            port: 8545,        // web3-gear port
            network_id: "*"    // Match any network id
        }
    }


以上，便可以使用Truffle提供的全部工具。

### 编译合约

    ./node_modules/.bin/truffle compile

### 部署合约

    ./node_modules/.bin/truffle migrate


### 执行测试用例

    ./node_modules/.bin/truffle test
    

## Thorify使用演示

详细请见`web3-thorify-example.js`文件，演示内容包括：

+ VET转账
+ 合约部署
+ 合约调用
+ 合约交易
+ 使用外部签名工具签名交易

# vechain_scapp
