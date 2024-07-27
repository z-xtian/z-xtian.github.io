# Fork 网络

?> 本质是创建目标网络的分叉链，注意这不会拉取所有数据，而是要用到什么数据就拉取哪部分数据。


完成这个事情共2步骤
- 1. 节点配置

在 `hardhat.config.js` 配置
```js
networks: {
  hardhat: {
    forking: {
      url: "https://mainnet.infura.io/v3/<key>",
    }
  }
}
```

默认情况下将从最近的主网区块中分叉。但是我们建议从特定的块号进行分叉（防止出现奇奇怪怪的结果）。

```js
networks: {
  hardhat: {
    forking: {
      url: "https://mainnet.infura.io/v3/<key>",
      blockNumber: 14390000
    }
  }
}
```

或者通过命令行启动节点

```cmd
npx hardhat node --fork https://goerli.infura.io/v3/<key>
```

输出

```cmd
Started HTTP and WebSocket JSON-RPC server at http://127.0.0.1:8545/

Accounts
========

WARNING: These accounts, and their private keys, are publicly known.
Any funds sent to them on Mainnet or any other live network WILL BE LOST.

Account #0: 0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266 (10000 ETH)
Private Key: 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80

Account #1: 0x70997970C51812dc3A010C7d01b50e0d17dc79C8 (10000 ETH)
Private Key: 0x59c6995e998f97a5a0044966f0945389dc9e86dae88c7a8412f4603b6b78690d

Account #2: 0x3C44CdDdB6a900fa2b585dd299e03d12FA4293BC (10000 ETH)
Private Key: 0x5de4111afa1a4b94908f83103eb1f1706367c2e68ca870fc3fb9a804cdab365a

Account #3: 0x90F79bf6EB2c4f870365E785982E1f101E93b906 (10000 ETH)
Private Key: 0x7c852118294e51e653712a81e05800f419141751be58f605c371e15141b007a6

Account #4: 0x15d34AAf54267DB7D7c367839AAf71A00a2C6A65 (10000 ETH)
Private Key: 0x47e179ec197488593b187f80a00eb0da91f1b9d0b13f8733639f19c30a34926a

Account #5: 0x9965507D1a55bcC2695C58ba16FB37d819B0A4dc (10000 ETH)
Private Key: 0x8b3a350cf5c34c9194ca85829a2df0ec3153be0318b5e2d3348e872092edffba

Account #6: 0x976EA74026E726554dB657fA54763abd0C3a0aa9 (10000 ETH)
Private Key: 0x92db14e403b83dfe3df233f83dfa3a0d7096f21ca9b0d6d6b8d88b2b4ec1564e

Account #7: 0x14dC79964da2C08b23698B3D3cc7Ca32193d9955 (10000 ETH)
Private Key: 0x4bbbf85ce3377467afe5d46f804f221813b2bb87f24d81f60f1fcdbf7cbf4356

Account #8: 0x23618e81E3f5cdF7f54C3d65f7FBc0aBf5B21E8f (10000 ETH)
Private Key: 0xdbda1821b80551c9d65939329250298aa3472ba22feea921c0cf5d620ea67b97

Account #9: 0xa0Ee7A142d267C1f36714E4a8F75612F20a79720 (10000 ETH)
Private Key: 0x2a871d0798f97d79848a013d4936a73bf4cc922c825d33c1cf7073dff6d409c6

Account #10: 0xBcd4042DE499D14e55001CcbB24a551F3b954096 (10000 ETH)
Private Key: 0xf214f2b2cd398c806f84e317254e0f0b801d0643303237d97a22a48e01628897

Account #11: 0x71bE63f3384f5fb98995898A86B02Fb2426c5788 (10000 ETH)
Private Key: 0x701b615bbdfb9de65240bc28bd21bbc0d996645a3dd57e7b12bc2bdf6f192c82

Account #12: 0xFABB0ac9d68B0B445fB7357272Ff202C5651694a (10000 ETH)
Private Key: 0xa267530f49f8280200edf313ee7af6b827f2a8bce2897751d06a843f644967b1

Account #13: 0x1CBd3b2770909D4e10f157cABC84C7264073C9Ec (10000 ETH)
Private Key: 0x47c99abed3324a2707c28affff1267e45918ec8c3f20b8aa892e8b065d2942dd

Account #14: 0xdF3e18d64BC6A983f673Ab319CCaE4f1a57C7097 (10000 ETH)
Private Key: 0xc526ee95bf44d8fc405a158bb884d9d1238d99f0612e9f33d006bb0789009aaa

Account #15: 0xcd3B766CCDd6AE721141F452C550Ca635964ce71 (10000 ETH)
Private Key: 0x8166f546bab6da521a8369cab06c5d2b9e46670292d85c875ee9ec20e84ffb61

Account #16: 0x2546BcD3c84621e976D8185a91A922aE77ECEc30 (10000 ETH)
Private Key: 0xea6c44ac03bff858b476bba40716402b03e41b8e97e276d1baec7c37d42484a0

Account #17: 0xbDA5747bFD65F08deb54cb465eB87D40e51B197E (10000 ETH)
Private Key: 0x689af8efa8c651a91ad287602527f3af2fe9f6501a7ac4b061667b5a93e037fd

Account #18: 0xdD2FD4581271e230360230F9337D5c0430Bf44C0 (10000 ETH)
Private Key: 0xde9be858da4a475276426320d5e9262ecfc3ba460bfac56360bfa6c4c28b4ee0

Account #19: 0x8626f6940E2eb28930eFb4CeF49B2d1F2C9C1199 (10000 ETH)
Private Key: 0xdf57089febbacf7ba0bc227dafbffa9fc08a93fdc68e1e42411a14efcf23656e

WARNING: These accounts, and their private keys, are publicly known.
Any funds sent to them on Mainnet or any other live network WILL BE LOST.
```

- 2. 代码应用

#### 模拟账户
Hardhat Network 允许您模拟任何地址。即使您无权访问其私钥，这也可以让您从该帐户发送交易。

下面是根据在 `hardhat.config.js`配置 fork 后的代码示例:

- 合约部分

```solidity
pragma solidity ^0.8.9;
contract Fork {
    address immutable public owner;

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner {
        require(msg.sender == owner, "Only the owner can call this function.");
        _;
    }

    function test(uint a, uint b) public onlyOwner view returns(uint) {
        return a+b;
    }
}
```
作者已在 goerli 部署该合约，地址:  `0x1BC902734C51711301aee8D78a37CdAbF4123c57`


- 脚本部分`scripts/fork.js`

```js
const { ethers } = require("hardhat");
async function transfer() {
    const [sender] = await ethers.getSigners();
    const recipientAddress = "0x05421c943Db220a71531fD76E0267813a15cAB05"; 
    const amount = BigInt("1000000000000000000");
    const tx = await sender.sendTransaction({
        to: recipientAddress,
        value: amount,
    });
    await tx.wait();
    console.log("转账完成！");
}
(async () => {
    // 冒充所有者地址
  await hre.network.provider.request({
    method: "hardhat_impersonateAccount",
    params: ["0x05421c943Db220a71531fD76E0267813a15cAB05"]
  });

  // 让签名者冒充所有者地址
  const ownerSigner = await ethers.getSigner("0x05421c943Db220a71531fD76E0267813a15cAB05");

  // 获取部署的合约实例
  const contractAddress = "0x1BC902734C51711301aee8D78a37CdAbF4123c57";
  
  // 作者账户余额不足才需要这样，如果你够的话可以不用管这步骤
  await transfer()

  const Fork = await ethers.getContractFactory("Fork");
  const fork = await Fork.attach(contractAddress);

  // 使用所有者签名者连接到已部署的合约
  const connectedContract = fork.connect(ownerSigner);

  // 函数调用
  const result = await connectedContract.test(1, 21111);

  console.log('执行成功！')
})()
```

- 执行
```cmd
npx hardhat run .\scripts\fork.js --network hardhat
```

- 输出
```cmd
转账完成！
执行成功！
```