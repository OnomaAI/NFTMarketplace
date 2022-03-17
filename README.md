## NFT Marketplace w/ Ethereum, Solidity, IPFS, Next.js

### Ref) https://dev.to/edge-and-node/building-scalable-full-stack-apps-on-ethereum-with-polygon-2cfb

### 로컬에서 실행

복사한 후.env 파일 생성하여 다음과 같이 적는다.

```
API_URL = "https://eth-ropsten.alchemyapi.io/v2/E_p2E79a9S3xjV9XNw_p8qUYvr6dHuQW"
PRIVATE_KEY = "YOUR WALLET PRIVATE KEY"
```

PRIVATE_KEY는 메타마스크의 다음 화면에서,
![image](https://user-images.githubusercontent.com/58359639/158768423-ec7096d2-01f2-4671-8f00-97c27df958d9.png)

아래의 버튼을 눌러 복사할 수 있다.

![image](https://user-images.githubusercontent.com/58359639/158768500-4e6edfeb-fe60-4429-8903-03b181b45193.png)

npm 설치 및 컴파일

```
npm install ethers hardhat @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers web3modal @openzeppelin/contracts ipfs-http-client axios

npm install -D tailwindcss@latest postcss@latest autoprefixer@latest

npm hardhat compile

```

컴파일이 끝나면 실행가능.

```
npm run dev
```

### 코드

#### CONTRACT

- greeter.sol: npx hardhat node 실행 시 자동 생성되는 파일
- NFTMarketplace.sol: NFT Marketplace Smart Contract.

#### PAGES

- \_app.js: 메인 페이지
- admin: 지정한 admin wallet address 연결 시에만 접속 가능하게 할 예정
- create-nft: NFT 민팅할 수 있는 페이지
- dash-board: 내가 판매중인 NFT 확인 가능
- index: salefront, 판매하고 있는 모든 NFT 확인 가능
- interact: wallet 연결 함수 포함
- my-nfts.js: 현재 연결된 지갑이 보유하고 있는 NFT 확인 가능
- resell-nft.js: 보유하고 있는 NFT resell 시 가격 설정하는 페이지.

#### SCRIPTS

- deploy.js: smart contract 배포하는 파일

#### TEST

- sample-test.js: smart contract test용 파일
