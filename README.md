# blockchain

## sol
```
//SPIX-License-Identifier:MIT

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

contract New{
    string name;
    function setName(string memory _name) public {
        name=_name;
    }
    function getName() public view returns(string memory){
            return name;
    }
    
}
```

code 1:
```
bootnode -nodekey { KEY_NAME } -verbosity 7 -addr "127.0.0.1:30301"
```
```
geth --datadir "./data"  --port 30304 --bootnodes enode://4736e5b9fd42f9b9ffa31af62ef8ea458437d7a6272f940088039744be72fa485fdff4c2acd47851bd3d7f548af8ad8f64eaf8c6b0ab05a0b4b2dded6dd97936@127.0.0.1:0?discport=30301 --authrpc.port 8547 --ipcdisable --allow-insecure-unlock  --http --http.corsdomain="https://remix.ethereum.org" --http.api web3,eth,debug,personal,net --networkid 1234567 --unlock 0x98d4a95e1CED107f85396d3dcD5E7195C500734c  --password ./data/password.txt  --mine --miner.etherbase= 0x98d4a95e1CED107f85396d3dcD5E7195C500734c

```
```
geth --datadir "./data"  --port 30306 --bootnodes enode://4736e5b9fd42f9b9ffa31af62ef8ea458437d7a6272f940088039744be72fa485fdff4c2acd47851bd3d7f548af8ad8f64eaf8c6b0ab05a0b4b2dded6dd97936@127.0.0.1:0?discport=30301  -authrpc.port 8546 --networkid 1234567 --unlock 0xB33A5F2114EC80c468A7907356F88F7a34B93249 --password ./data/password.txt

```
