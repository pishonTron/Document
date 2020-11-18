# Pifi(Pishon finance)protocol economic model

## 一. Overview

`PISHON` is a decentralized liquidity finance protocol based on [TRON](https://tron.network)，shaping the two decentralized financial scenarios of `Pishon Finance（PiFi）`and `Magnify Hashrate` ，and synchronized Completed the value shaping of the token `PIS`and the stable coin `PUSD`. In the `PiFi` scenario, the original superconducting mechanism has completed a revolution in the value of digital assets. At the same time, the `PUSD` asset synthesis adopts the mechanism of "exchange and issuance, redemption and destruction", which has subverted the issuance of stablecoins. Through this article, we will introduce the `PISHON` financial model in detail and disassemble each point.

## 二. Introduction to PISHON

### 1. What is PISHON?

`PISHON` is a decentralized financial ecosystem based on `TRON`, covering two innovative decentralized financial scenarios of `Pishon Finance (PiFi)` and `Magnify Hashrate`.

## 2. What does PISHON want to achieve?

`PISHON` will realize the issuance and preliminary consensus of the ecological foundation `PIS` through `Pishon Finance (PiFi)`. And through `PiFi` to realize the basic computing power lending scenario of `Magnify Hashrate`, the `PIS` miners are used to pledge `PUSD` for computing power lending, driving the miners to participate in the completion of the initial `PUSD` asset synthesis, and at the same time, `PI`S And `PUSD` promotes a wide range of digital asset application scenarios and transaction scenarios. Establish the `PIS` superconducting mining pool, drive more communities and miners to participate in the ecological construction of `PiFi`, and drive miners and consensus participants through the `Dao` organization to design and implement more consensus scenarios for `PIS`. Synchronously establish the issuance mechanism of `PUSD`, and gradually broaden the path of `PUSD` asset synthesis in the subsequent `PISHON` ecological operation, so that more valuable digital assets can participate in the `PUSD` asset synthesis, and at the same time gradually expand `PUSD` Participate in more scenarios where stable currencies can participate in addition to `Magnify Hashrate`. In the mid-stage of the development of `PISHON`, it will promote the widespread use of `Magnify Hashrate` throughout the network, by broadening the sequence of loan pledges, and establishing risk control models and basic data penetration management for computing power loans with different risks; In the scenario of power lending, evaluate the `DeFi` projects based on different public chains and release the corresponding lending products; establish a `Magnify Hashrate` lending fund pool to raise and post-investment management of funds corresponding to the lending power. Finally, it realizes the decentralized P2P financial ecology of PISHON, and contributes to the development of decentralized finance.


## 3. System Role

Role | Definition
---|---
Superconducting computing power | Participating in the liquidity of the `Pifi` protocol, and the liquidity provider of the protocol, accounting for 40% of the computing power
Community computing power | Participating in the community promotion and operation of the `Pifi` protocol, is a strong defender of the entire platform, computing power accounts for 20%
Promote computing power | Participate in the early promotion and technical evangelism of the `Pifi` protocol. 15% of computing power
Rushing computing power | It is the backbone of the entire `Pifi` protocol, with computing power accounting for 10%
Dao computing power | is the technical maintenance and community governance of the entire `Pifi` protocol. 15% of computing power
Mortgage lending | It is the fuel of the entire liquidity financial agreement, mortgages the same amount of superconducting liquidity, and superconducting computing power is increased by 3 times

## 4. Protocol data mechanism

The agreement involves the price synthesis mechanism of PUSD, the superconducting exchange mechanism, and the PUSD destruction mechanism. These three mechanisms are all read from the smart contract, and the prices involved are all derived from Tron's oracle price source. such as:

1. USDT or TRX: PUSD synthetic pool, the price of TRX is read from the oracle on the chain and called by the smart contract.
2. PIS: USDT superconducting pool, the price of PIS is only output and called by the smart contract.
3. PUSD: USDT or TRX destruction pool, the price of TRX is obtained from the oracle on the chain, and the smart contract is directly called

## 三、Pishon Finance (PiFi) model interpretation

### 1、PISHON（PIS）Introduction

`PISHON(PIS)` is the token of `PISHON` ecological `Pishon Finance (PiFi` liquidity mining, with a total of `100,000,000` pieces, none of `PIS` is pre-mined, and all output is miners participating in superconductivity The mechanism makes contributions to computing power to obtain incentive rewards of `PIS`. Users who hold `USDT` can purchase computing power in the superconducting pool of the `PiFi` (liquid finance) platform, and 1 USDT can purchase 1 copy (one copy) Hash power is represented by P) Hash power, and the user's purchasing power must not be less than 100USDT. After the hash power is purchased (you can mine after the hash power is purchased, you can't refund after the hash power is purchased, and the funds purchased are entered into the superconducting pool. ), after purchasing computing power, users can mine `PIS (Pishon)` tokens (`PIS` generates 64800 per day, and each block generates 2.2506251764800/28792 = 2.25062517. 40% of the output is superconducting Computing power (the token PIS mined by superconducting computing power is directly transferred to the user’s wallet address, and the user can exchange it in the superconducting pool), 20% of the amount belongs to the promotion computing power, 15% belongs to the community computing power, and 10% belongs to the redemption 15% of the computing power of the ranking belongs to the Dao organization computing power.


### 2、Introduction to Superconducting Mechanism

The original superconducting mechanism of `Pishon Finance (PiFi)` is used for the calculation of the liquidity mining computing power of `PIS` and the redemption and destruction of `PIS`. Users must deposit their USDT into the superconducting pool when conducting `PIS` liquidity mining. This process is irreversible. Once the user deposits, the non-redeemed USDT will not leave the superconducting pool in any form. After the user deposits, `PiFi` starts to calculate the user's computing power contribution and rewards the user `PIS` according to the output distribution rules of `PIS`. All funds that enter the superconducting pool will be used as the standard of `PIS` redemption. After obtaining the PIS, users can perform the `PIS` redemption operation in accordance with the `PIS` redemption rules in the superconducting mechanism. The redemption rules of the superconducting mechanism are:

Exchange formula:

pis price = (current balance of superconducting pool / current circulation of PIS) * (0.2% + (99.8%/(100 million / 2700)) * hour) **Note: ** 1. The circulation of pis refers to the output Subtract the destroyed 2. Hour represents the number of hours the project started 3. The maximum number of hours that the `PiFi` superconducting mechanism operates is: 35088 (1462 days in total, and the first hour is zero)

Derived formula：

```bash
pis price = (current balance of superconducting pool / current circulation of PIS) * (0.002+ (0.998 * 27 * hours) / 1000000)
pis price = (current balance of superconducting pool / current circulation of PIS) * (0.002+ (0.998 * 27 * hours) / 1000000)

pis price = (current balance of superconducting pool / current circulation of PIS) * (0.002+ (26.946 * hours) / 1000000)

pis price = (current balance of superconducting pool / current circulation of PIS) * (2000+ 26.946 * hours) / 1000000)
pis price = current balance of the superconducting pool * (2000+ 26.946 * hours) /PIS current circulation /1000000
```


All `PIS` participating in redemption are directly destroyed after redemption. The superconducting mechanism can ensure that every `PIS` obtained by all `PIS` miners and consensus participants can be exchanged for USDT in the superconducting pool. The absolute gold standard value of PIS is used to ensure that `PIS` does not have to worry about the standard value in both trading and circulation scenarios.

### 3、Introduction to PIS output computing power

The computing power that triggers the distribution of `PIS' is divided into five parts: superconducting computing power, promotion computing power, community computing power, ranking computing power, and Dao organization computing power. The output distribution ratio is 40% of superconducting computing power and promotion computing power. 20% of the computing power in the community, 15% of the computing power in the community, 10% of the computing power in the ranking, 15% of the Dao organization computing power, 100% in total. The algorithm model and acquisition rules for the five parts of computing power are as follows:

#### 1. Superconducting computing power

Superconducting computing power is the basis for mining output rewards after miners invest USDT into the superconducting pool. The minimum user input limit is 100USDT (100P). Users can obtain superconducting computing power after depositing USDT in the superconducting pool. The superconducting computing power reward algorithm rules are:

Personal superconducting computing power reward PIS=(personal P/full network P) * 64800/24 ​​*40%, PIS rewards the output of each block, and the user receives it by himself.

The calculation of superconducting computing power starts after the user deposits it in the superconducting pool, and the initial value of computing power is marked. The computing power will be halved every 180 days until all PIS is output. The halving of the computing power is for the superconducting pool to continue to stay young, and to ensure fairness for the miners who subsequently enter the PIS superconducting mechanism for mining power.


#### 2. Promote computing power

The purpose of the promotion of computing power is to promote the rewards established by the `PIS` miners to expand the superconducting pool capacity and the number of PIS consensus miners. The `PIS` miners can obtain the promotion link after activating their superconducting computing power, and other miners can register through the registration link. After the recommendation relationship is bound, the PIS miner income that can be directly recommended is:

Directly recommend the miner's superconducting computing power to earn 25%

Directly recommend miners to promote 50% of computing power

**Example:**（A-B-C-D-E-F）F static income 100IS, then E gets 25PIS direct promotion reward; D gets 12.5PIS promotion income; D gets 6.25PIS promotion income; C gets 3.125PIS promotion income; B gets promotion income The promotion income of 1.5625PIS; A gets the promotion income of 0.78125PIS. This means that when calculating the user's promotion computing power, we only pay attention to the superconducting computing power income of the directly recommended miners and the promotion computing power income, and directly recommend how much superconducting computing power the miners receive, and the recommender will take 25% of the promotion computing power income. Directly infer how much promotion computing power the member receives, and the recommender will use 50% of his promotion computing power as the promotion computing power.



#### 3. Community computing power

Community computing power is to incentivize community organizers to better serve the PIS miner community and receive rewards as community management contributions. The top 49 in the entire network community can get community computing power rewards, which are distributed once a day. Nodes that receive community computing power rewards must invest ≥3000 USDT (or minimum computing power 3000P). The community computing power rewards obtain algorithm:

Personal community reward = personal community computing power / network-wide community computing power *64800*15%
Personal community computing power = maximum community computing power under the personal umbrella^2/10 + sum of computing power of all communities except the largest community^8/10
The computing power of the entire network community = the addition of the computing power of all 49 individual communities that meet the conditions


**Note:** 

1. If there is only one community, the default is the largest community.
2. If all communities have equal computing power, they will be in the order of registration, with the largest community being the first to register.
3. The community computing power and the ranking computing power are issued simultaneously. The snapshot is completed and calculated at 20:00 UTM every day, and is issued to the user to the user's wallet address.

#### 4. Rushing computing power

Rushing computing power is to encourage `PIS` miners to increase their percentage of computing power as much as possible, while expanding the overall capacity of the superconducting pool, so as to provide more adequate standard support for future `PIS` cashing.

The specific rules for the rewards of computing power are as follows:
Rushing computing power rewards the 200 miners with the largest personal computing power in the entire network, which are divided into 3 sections:

1. Ranking 1-8: 3% of the total output of PIS is divided equally, that is, 1944 PIS;
2. Ranking 9-49: 3% of the total output of PIS is divided equally, which is 1944 PIS;
3. Ranking 50-200: 4% of the total output of PIS is divided equally, or 2592 PIS;

**Note:** A snapshot is taken at 20:00 UTM every day and distributed to the user to the user's wallet address.

#### 5. Dao organization computing power

The `Dao` organization is composed of foundations, technical communities, community alliances, and audit teams. It mainly completes the basic design, technical implementation, and community promotion of the `PISHON` ecology, and provides continuous support for the later development of `PISHON` Continuous planning and management. This part of the computing power will immediately redeem the tokens rewarded by the computing power in the superconducting pool and complete the destruction (the mining is directly exchanged in the superconducting pool, and the hourly output is immediately triggered by the contract to automatically exchange and destroy). It is ensured that the `Dao` organization only promotes revenue and does not have the ability to hold coins will not affect the future market value of `PIS`. Without whales, there will be no waves. If the `Dao` organization gives up holding a large number of `PIS`, there will be no gold standard in the market. Input and output `PIS`.

## 四. Magnify Hashrate model

### 1. PUSD financial model

#### 1. Introduction to PUSD

`PUSD` is a stable currency anchored to the U.S. dollar and the medium of value circulation in the `PISHON` liquid financial project. The full name is `PISHON USD`, and the token symbol is `PUSD`. `PUSD` is an asset synthesized completely based on the contract rules of `TRON`. As the collateral for `Magnify Hashrate` loans, it first appeared in the `PISHON` ecology for initial circulation, and will expand into more scenarios in the future based on consensus. The rules of `PUSD` asset synthesis are designed and executed according to the principle of "Exchange is issued, redeemed and destroyed". It can be simply understood that users who need to use PUSD can use different digital assets for synthesis according to the requirements of PUSD asset synthesis. PUSD` only supports `TRX` and `USDT` for synthetic asset operations.

#### 2. Synthetic Asset Rules

Users can use `TRX` and `USDT` to issue `PUSD` through exchange (the exchanged TRX and USDT enter the fund pool, and the user can manage the fund pool). If the user wants to redeem, convert PUSD into USDT and TRX, exchange PUSD will be destroyed afterwards

```json
Issuance mechanism is: PUSD⇋ α TRX (α=USDT / TRX current price)
                    PUSD⇋USDT (1:1)

The destruction mechanism is: δ TRX⇋PUSD (δ=USDT / TRX current price*0.9)
                      USDT0.95=PUSD
```

### 2. Magnify Hashrate computing power lending rules

Users mortgage `USDT` to borrow `PUSD` to increase their own hashrate (`Magnify Hashrate`), the specific rules are:
Mortgage: Users who have purchased computing power in the `PiFi` superconducting pool can mortgage `USDT` or `TRX` to exchange for `PUSD` (the exchange method is to use `USDT` or `TRX` to exchange for `PUSD` on `JustSwap` , Or exchange directly in the project (refer to the issuance mechanism of `PUSD`).

Borrowing: user mortgage x = (purchasing power: USDT: PUSD=1:1) PUSD, the user's computing power can become 4 times the power invested in the superconducting pool. It is equivalent to borrowing 3 times the computing power on the platform, so as to obtain more superconducting computing power rewards.
In the future, more digital assets will be gradually opened for computing power lending collateral, and more DeFi liquid mining projects will be opened as computing power lending products.

#### 3. Computing power lending syphon

The computing power lending syphon is one of the most important products of `Magnify Hashrate`, and it is also a very important part of the future development of `PISHON`. In the future, the entire traditional financial market must be a transitional development of `DeFi` finance. Any financial market development Inseparable from the support of the leveraged financial market, the `Magnify Hashrate` platform can increase the user's rate of return while reducing the user's investment risk. `PISHON` will gradually build more computing power lending products based on different `DeFi` financial projects at different bottom layers, and design different computing power lending products based on different product risk control models and development potentials. In the future, `Magnify Hashrate` will join hands with all consensus communities and miners of `PISHON` to build a powerful PiFi financial ecosystem.


## 五、PISHON advantage

### 1. The advantages of superconducting mechanism

#### 2. Security: Superconducting mechanism guarantees the investment income of miners participating in PiFi liquidity mining;

The superconducting mechanism adopts a decentralized contract based on `TRON` to execute the calculation power mining of `PIS` and the redemption and destruction process of `PIS` to ensure that every `PIS` output comes from the contribution of calculation power. A `PIS` can be exchanged to `USDT` in the superconducting pool according to the exchange algorithm and will be destroyed immediately after the exchange is completed. This guarantees that every miner participating in `PIS` liquidity mining can obtain corresponding incentives in accordance with the decentralized contract for the contribution of mining power, and abandon the special group that is considered to be caused by the centralized execution and settlement process. Obtaining rewards in the case of investment or low investment also ensures that the tokens obtained from the contribution of computing power are digital assets supported by the gold standard. At the same time, combined with the incentive policy, both the investment computing power contribution and the community promotion computing power contribution are identified as consensus incentive components, assisting miners who are willing to contribute more consensus impetus to ecological construction to more conveniently form communities and form autonomous organizations to provide more ecological development. Great power.

#### 2. Stability: Superconducting mechanism guarantees the market value shaping of PIS;

The market value of `PIS` is established by the total circulation of `PIS` and the total amount of fiat currencies participating in the market. The balance of the superconducting pool in the superconducting mechanism is the total fiat balance of the `PISHON` ecology for the exchange of `PIS`, outside the superconducting exchange mechanism , A centralized (or DEX) `PIS` trading market will be formed, attracting a large number of `PIS` asset holders to conduct transactions in exchange for the corresponding `PIS` value. We can think that the superconducting pool is the maximum buying depth of the `PIS` secondary market, because the actively formed `PIS` secondary market transaction consensus price must be higher than the exchange price of the superconducting pool (lower than the exchange price of the superconducting pool, it cannot be To attract `PIS` miners to trade in the secondary market), the balance of the superconducting pool can be considered as the bottom price part of the buying order depth (the lowest unit price is the largest), the total demand for buying orders in the secondary market + the balance of the superconducting pool = circulating`PIS `Total market value. From this, it can be seen that the superconducting pool is the basis for the formation of the gold standard of the secondary market and subsequent payment scenarios for the `PIS`, and is also the guarantee for the birth of the secondary market and the subsequent `PIS` application scenarios.

#### 3. Reasonability

1. Miners deposit `USDT` in the superconducting pool to participate in the issuance and distribution of `PIS`, and then they will be destroyed after cashing out;
2. 100% of the funds entered into the superconducting pool are used for `PIS` exchange;
3. The proportion of computing power mining income is balanced, and miners are encouraged to participate in the `PISHON` ecological co-construction and `PIS` value shaping;

#### 4. Fairness

1. "Dao" organizes computing power reward output to be destroyed immediately;
2. The mining power of miners will be halved every 180 days;

### 2、PISHON driving force model

#### 1. Market driving force

1. Analysis of the advantages of the popularization algorithm rules

Promotional computing power rewards account for 20% of the total amount of `PIS`, which is the largest part of computing power incentives except for superconducting computing power rewards. The purpose is to attract more participating miners for the `PISHON` ecology and quickly expand the number of addresses held by `PIS`.

The promotion algorithm is simple and clear, and it is completely executed on the chain. Although the level only calculates the rewards for the direct recommendation miners, because of the algorithmic correlation direct recommendation miners' promotion computing power income, it is actually a very deep correlation income. The distribution accuracy is 4 digits after the decimal point (ie 0.0001PIS), so the associated promotion computing power gains are very market driving force.

Most decentralized financial models are not good at building community stickiness, and focus more on the autonomy reached by the consensus of the community. Obviously, through the twelve years of centralized financial development in the blockchain area, this community autonomy atmosphere and drive The power is insufficient. The community has no service source power triggered by human nature, and more depends on human consciousness. Interests are never directly linked but long-term development of the same direction to drive all consensus participants to maintain ecological value, which is not solid. When `PISHON` constructs the `PIS` liquidity mining superconducting mechanism, it pays more attention to the relevance of every miner in the community. It drives the service of the overall community from short-term benefit management to realize the long-term consensus building and enhances the community’s sense of collaborative development. Although the promotion of computing power is not a decentralized thinking, it is an indispensable part of a decentralized financial ecosystem.

The linear transmission of the miner ontology consensus becomes the consensus of small organizations. The vested interests who promote computing power rewards are the firm supporters of consensus evangelism. Small organizations form a high-quality community horizontally, and the community builds a stable and rapidly developing ecology. The essence of decentralized finance is a revolution at the bottom, a revolution in financial models, not a revolution in human nature. A high-quality decentralized financial ecosystem must fully consider human needs. The ultimate vision of `PISHON` is to build a decentralized financial commercial bank that everyone can use, and the essence of the bank is to manage wealth for the wealthy with assets and finance for those who need funds. To realize such a financial ecology, we must first build a sufficiently large consensus group, and this group will gradually evolve into the role of both parties in the ecology of `P2P` finance. Promoting the growth of the miner community is not only to promote the scale of the `PISHON` ecology, but also to simultaneously accumulate the capital of a bargain-hunting decentralized financial world, and this capital is the appeal and influence. Drive common direction with interests, drive consensus with value, and drive co-creation with the future. The decentralized financial world that `PISHON` wants to build must be shared by all `PIS` miners and participants of `PISHON` consensus. Consensus. Co-creation .shared.

2. Analysis of the advantages of community computing power algorithm rules

Community computing power rewards accounted for 15% of the PIS computing power output, and a stable daily distribution of 9,720 PIS rewards was given to the top 49 in the community computing power rankings. The design of community computing power is to encourage the autonomy of community organizations and the enthusiasm of consensus evangelism. Community computing power rewards are issued in the form of a fixed level to allow all communities to form a healthy competition, to better promote ecological development, and to promote the emergence of more high-quality communities.

The algorithm of community computing power is very scientific, and it uses the whole network to screen high-quality driving communities for ranking. Among them, the parameter participating in the ranking is the personal community computing power, and the personal community computing power algorithm adopts a very scientific calculation method. The algorithm is: personal community computing power = maximum community superconducting computing power under the umbrella ^ 0.2 + total computing power of other communities under the umbrella ^0.8. First, compare the self-sustained superconducting computing power of the miners directly recommended under the umbrella and the superconducting computing power of all miners under the directly recommended miner umbrella to sum up, and then compare the summed computing power of several directly recommended miners to rank, and the largest total computing power is the largest Community, then the result is obtained by raising this community to the power of 0.2, and the sum of the computing power of the remaining communities is raised to the power of 0.8. The logarithmic formula is more familiar and may be understood. The 0.2 power calculation is equivalent to erasing this data. We observe from the actual community contribution. The largest community under the umbrella is often the result of multi-layer shared community computing power. It is also commonly known as "skewered candied haws." The purpose of the largest community under the umbrella for low computing power contribution is to distribute community computing power rewards more fairly to miners who truly continue to grow the community.

Before the calculation of the community computing power reward algorithm, the contract will take a snapshot of the personal superconducting computing power of the miners participating in the ranking. The prerequisite for participating in the community computing power reward ranking is that the personal superconducting computing power is not less than 3000P, and the personal superconducting computing power Miners below 3000P will not be eligible for community computing power rankings. This is to reduce the amount of concurrency in the calculation of the community's computing power reward contract, and too much calculation data will cause difficulty in contract execution. The core of decentralized finance is driven by decentralized communities, and high-quality communities will promote the diversity and sustainability of the financial ecology. Encouraging high-quality communities to gain greater development through competition can promote the overall development of the `PISHON` ecology. In the future, we will empower high-quality communities with more diversified rights and encourage more miners to promote the establishment of communities to participate in the construction and evangelism of the `PISHON` ecology.

#### 2. Capital driving force

1. Analysis of the driving force of rushing computing power for market capital access

Rushing computing power rewards accounted for 10% of `PIS` computing power output, and a stable daily distribution of 6,480 `PIS` rewards to the top 200 superconducting computing power. In the development process of `PiFi` liquid mining, as more and more miners participate in liquid mining, the funds and total computing power in the superconducting pool are increasing, and personal computing power continues to increase in the entire network. Continue to decrease in the large process, PIS will complete value shaping along with this process, and will not affect the actual income of participating miners, but the addition of the hashrate rewards will indeed promote the entire `PISHON` ecology. , Which is equivalent to taking out 25% of the superconducting computing power reward and weighting it among 200 miner addresses. If there are more than 10,000 addresses of miners participating in the entire superconducting pool, then the rewards for the miners who can enter the list of 200 people will be far greater than the rewards of their own superconducting power. The result of the incentive is to deepen the capital depth of the superconducting pool and provide a larger amount of funds for PIS to cash out.

`PISHON` Eco-Liquidity Mining Construction Hashing Power Award is to encourage large miners and institutional users to enter the market and jointly build the `PISHON` ecology. Most of the decentralized financial ecosystems insist on breaking up, denying the entry of large investors to avoid the uncontrollable secondary market, and `PISHON` does not agree with this. Whether it is centralized finance or decentralized finance, the essence is to build a free asset exchange market. The essence of finance is supply and demand. The so-called breakup is only for the dealer to control the secondary market more conveniently and avoid the formation of confrontation with big players. The `PISHON` ecological `Dao` organization does not hold any `PIS`, and all the `Dao` organization computing power rewards will immediately enter the superconducting pool for exchange and destruction. The existence of the `Dao` organization has no effect on the execution of the `PiFi` liquidity mining contract, nor can it affect the results of any execution. Therefore, driving big players into the `PISHON` ecology is to better build the follow-up financial scene of `Magnify Hashrate`. Encouraging miners and financial institutions to enter the `PISHON` ecology is actually to integrate traditional financial forces for a decentralized financial transformation.

2. Analysis of the driving force of the halving rule for market capital access

The miners participating in the `PISHON` ecological liquidity mining start from the moment they buy the superconducting pool to obtain the computing power, and the contract will halve the mining power of the miners every 180 days. For example, a miner buys 1000USDT computing power in the first hour of the first day, and obtains 1000P computing power without borrowing computing power. Then after the liquidity mining of `PISHON` advances to 180 days, the mining power of the miner will be It will be halved to 500P, after 360 days it will be halved to 250P, after 540 days it will be halved to 125P, and so on, until the end of liquidity mining of `PISHON`.

`PISHON`ecology halved the mining power of miners in order to keep the superconducting mechanism younger. From the superconducting mechanism itself, we can analyze that with the operation of the superconducting mechanism, the proportion of subsequent miners’ investment income continues to decline. However, the miners who occupied the top mines and opportunities in the front have always maintained a continuous percentage of computing power. The final result is that no miners are willing to enter the superconducting pool for liquid mining when a certain critical point is reached. `PIS` is an important proof of work for `PISHON` ecology, and it is also an important way to encourage more consensus to enter `PISHON`. `PISHON` opens superconducting pool contract for liquidity mining in order to incentivize more miners and communities to enter` PISHON`Ecology creates the future together. Ultimately, the value of `PIS` is derived from the superconducting mechanism’s redemption algorithm and also from the consensus of the secondary market promoted by a large number of miners. We know that only more `PIS` holders participate Only by shaping the value of `PIS` can the value of `PIS` be pushed higher. In the end, the harvest of every `PIS` miner in the `PISHON` ecology will consist of two parts, the number of `PIS` obtained, and the final value of `PIS` together determine this result. The most reasonable way to shape the value of `PIS` miners is to increase the influence of `PISHON` ecology. Therefore, the `PISHON` ecology used the calculation power halving rule when the superconducting contract was first constructed to continuously reduce the proportion of the calculation power of the superconducting pool, so that the miners who later participate in the superconducting mechanism liquid mining can obtain higher calculation power. Accounted for and jointly participated in promoting the development of the `PISHON` ecology.

### 3. Consensus driving force

#### 1. PIS Miner Driving Force Analysis

The `PISHON` ecology promotes the two important sectors `Pishon Finance (PiFi)` and `Magnify Hashrate` at the same time. The purpose is to allow everyone who participates in the `PISHON` consensus to quickly add value through the two major services of `PISHON` There are many ways to drive users to become `PISHON` miners with their own assets. We have done some analysis and expressions earlier. Whether it is driven by market motivation or personal computing power, it can satisfy most users' interests in becoming `PISHON` miners. demand. However, the consensus required to create an ecosystem is not only the calculation of the input-output ratio and the profit rate of return, but also whether the future development of the ecosystem is relevant to the miners’ future plans for decentralized finance on the blockchain. We hope to complete A revolution at the bottom of the decentralized financial world, starting from the nature of financial supply and demand to build a decentralized financial service provider's supply and demand scenario, it is bound to generate the needs and services of both supply and demand parties rooted in the `PISHON` ecology to build their own financial service scenarios . The current role of every `PISHON` miner is to participate in value verification through hash power mining `PIS`. With the development of `PISHON` ecology, especially the business deepening and scenario expansion of `Magnify Hashrate` service, more and more Many `PISHON` miners are inspired to root in `Magnify Hashrate` to build their own `DeFi` financial scene, and use the leverage property of `Magnify Hashrate` to quickly absorb users from the entire market. This will be a brand-new cooperation model. `PISHON` can give all miners participating in the `PISHON` ecological consensus not only an investment in simply calculating the input-output ratio, but also for all miners in the near future. Consensus provides a high-quality leverage tool for financial entrepreneurship. We all know that it is not a few top companies (payments, social networking, games, e-commerce, new media, etc.) that have really bought the dividends of Internet development over the past decade, but the capital that has supported the ups and downs of hundreds of thousands of startups over the past decade mechanism. Without basic financial support, no industry can obtain the possibility of rapid development. Hot money is a necessary factor to promote the development of the industry. What the `PISHON` ecology wants to shape is the "garage coffee" for the development of decentralized finance in the future. `PISHON` will use the financial advantages of `Magnify Hashrate` in the community to urge more individuals and organizations to carry out wide-area, multi-scenario decentralized financial projects. In the future, the relationship between `PISHON` and `PIS` miners is more inclined to the relationship between GP and LP. `PISHON` provides the financial bottom layer, and `PISHON` miners and the community make more financial innovative application projects.

#### 2. Analysis of the driving force of PIS circulation holding (non-cash-out realization)

All the output methods of `PIS` are liquid mining. The output methods and proportions of `PIS` have been introduced in detail, so I won't repeat them here. When we try to analyze the final liquidity results of PIS, we may come to three completely different conclusions:

Ⅰ. The output of `PIS` has not participated in the redemption and destruction except for the output of `Dao` organization's calculation power which is immediately exchanged and destroyed in the superconducting pool;
Ⅱ. The output of `PIS`, except for the output of `Dao` organization, will be exchanged and destroyed immediately in the superconducting pool, and the rest of the output will participate in the redemption and destruction;
Ⅲ. The output of `PIS`, except for the output of `Dao` organization, will be exchanged and destroyed in the superconducting pool immediately, the rest of the output will be redeemed and destroyed;

Among them, the first and third results belong to two extreme cases, and the most likely result is the second result. So what are the factors that affect the second result, and what are the decision-making factors for the final circulation of `PIS`, and then we will make as detailed analysis as possible.

First of all, the circulation of `PIS` is affected by the output of computing power rewards and the exchange and destruction of miners. The output of computing power rewards is basically equivalent to the total issuance of `PIS` when the promotion of computing power rewards has little effect. (Promotional computing power reward `PIS` output is affected by the rules of distribution accuracy and promotion depth and will not be fully rewarded, and the unrewarded part is directly destroyed.) Then the variable locked in the miner exchange and destruction will determine the final PIS circulation. We try to analyze all factors and miners will actively exchange `USDT` and destroy `PIS` in the superconducting pool after obtaining PIS. The summary is as follows:

Ⅰ. The exchange price of `PIS` continues to rise to meet the psychological price of `PIS` miners, triggering miners to exchange `USDT` in the superconducting pool;
Ⅱ. The exchange price of `PIS` continued to drop below the psychological reserve price of `PIS` miners, triggering miners to exchange `USDT` in the superconducting pool;
Ⅲ. Normal exchange;

It is obviously incomplete to analyze the exchange and destruction of `PIS` from the superconducting pool to determine the final circulation of `PIS`. It is foreseeable that when the number of `PISHON` ecological liquidity mining miners reaches a certain value ( That is, the `PIS` holding address reaches a certain value), the market will take the initiative to open the secondary market for `PIS` (according to the status quo of most `DeFi` projects, it can be known that most centralized exchanges will After the number of asset holding addresses reaches a certain amount, the digital asset will be forced to the exchange to attract holders to trade). What we can know is that the transaction price of `PIS` in the secondary market opened for `PIS` must be higher than the exchange price of the superconducting pool `PIS` (if it is lower than the exchange price, it will not be able to induce currency holders to trade in the secondary market ), then miners have different ways of realizing value after receiving computing power rewards. Not only can they redeem `PIS` in the superconducting pool and trigger the destruction of `PIS`, they can also trade `PIS` in the secondary market for higher returns Return.

After increasing the transaction scale of `PIS` in the secondary market, based on the above analysis, we can easily draw a conclusion that a large amount of `PIS` will flow into the secondary market instead of being exchanged in the superconducting pool. This leads to another problem. The circulation of `PIS` will not be subject to centralized exchange and destruction due to the exchange price of the superconducting pool, or even exchange destruction. The first result of the circulation of `PIS` we analyzed appears. In the first case, except for the calculation power output of the `Dao` organization, which was immediately exchanged and destroyed in the superconducting pool, the rest of the calculation power output did not participate in the redemption and destruction; finally, after the execution of the `PISHON` liquidity mining contract, theoretically Circulating `PIS` and superconducting pool balance are fully corresponded, `PIS` becomes a stable digital asset, but because the actual transaction price of the secondary market formed in advance and the exchange price of the superconducting pool deviate, the superconducting pool will become `PIS `The depth of buying orders in the secondary market. Part of the transaction matching consensus formed in conjunction with the secondary market supports the future value of `PIS`.


Therefore, whether `PIS` is exchanged and destroyed in large quantities in the process does not affect the ultimate benefit of `PISHON` liquidity miners. Broadening the number of `PIS` holders and forming a larger consensus group determines the final value of `PIS` The only influencing factor.

### 4. Sustainable Development

#### 1. Analysis of the advantages of the halving rule for the continued rejuvenation of the PISHON superconducting pool

In "Analysis of the Driving Force of the Hash Rate Halving Rule on Market Capital Access", we made some simple analysis of the PISHON ecological liquidity mining miners' hash rate halving every 180 days. The purpose is to drive more miners. Participate in the ecological construction process of `PISHON` with the community, continue to maintain the surging power provided by the superconducting pool for the `PISHON` ecology, and drive the ecological development faster and more steadily. The following is a simple analysis of why halving the computing power can maintain the continuous fairness of the superconducting mechanism:

To achieve relative fairness, an algorithmic mechanism must guarantee two foundations:

Ⅰ. The algorithm guarantees fairness in the calculation method of all participants.
Ⅱ. The algorithm guarantees fairness for the calculation sequence of all participants.

`PISHON` tries to break the so-called first opportunity and break the imbalance of value distribution caused by news asymmetry. `PISHON` believes that as long as it is a consensus person who contributes to ecological development, any contribution made under any circumstances should obtain a corresponding fair consensus incentive. We have repeatedly analyzed the factors that ultimately determine the value of `PIS`. In the twelve years of digital asset development, we have also seen many ways to increase the market value of digital assets. Although the forms are ever-changing and the scenarios are complicated, we summarize the fundamentals. It's just one-expanding the consensus group. Therefore, the basis for allowing BTC to reach more than $15,000 today is not because of the secondary market or more and more miners, but more and more users have a consensus to hold BTC. The halving of computing power can be executed up to 8 times in a total of 1543 days in `PISHON`, which means that every PIS can perform halving of computing power up to 8 times even if participating in PIS liquidity mining in the first hour. The remaining computing power after 8 halving of computing power is:


It can be seen that from the initial saturation of computing power to participate in the liquidity mining computing power output reward distribution for the `PIS` miners, the computing power that can participate in the liquidity mining will be deflated sharply. The squeezed part is the future `PIS` miners. Participating in liquid mining can be allocated more proportions, so the entire superconducting mechanism will remain attractive to new miners as the hash rate of the previous `PIS` miners involved in mining deflates. Stimulate more and more miners to enter the `PIS` superconducting pool for liquid mining, increase the fund balance of the superconducting pool and increase the value of `PIS`. In the end, the more the total amount of the superconducting pool, the greater the redemption value of `PIS`, the more the number of `PIS` miners, and the greater the ecological value of `PISHON`, the more the formed `PIS` secondary market will deviate from superconductivity. The pool exchanges the price to form a higher consensus price for PIS transactions, allowing all `PIS` miners to obtain greater returns of ecological value.

#### 2. Analysis of the advantages of Dao organization's immediate destruction of computing power for the sustainable development of PISHON

The `PISHON` Ecology `Dao` organization is the original consensus promotion agency of the entire `PISHON` ecology and the design team of the `PISHON` financial model. Different from the previous operation teams and foundations of decentralized financial projects, the `PISHON` ecological `Dao` organization has completed the task of building a decentralized financial model after promoting the establishment of `PISHON`, and more is to pass on PISHON To assume the role of an evangelist in the operation of consensus, there is no strong decision-making power, and there is no need for strong decision-making. What we know is that the `PISHON` ecology covers the two ecological scenarios of `Pishon Finance (PiFi)` and `Magnify Hashrate`, which are to improve the `PISHON` ecology from the two directions of promoting the development of consensus groups and building decentralized financial basic services. Sustainable development. It is the latter that the Dao organization really needs to continuously provide impetus. The construction of a decentralized financial service requires continuous improvement of the technology supply system and financial risk control model from the bottom to the application. Therefore, when designing the `PISHON` ecological liquidity mining `Dao` to organize computing power rewards, in order to prevent the `Dao` organization from becoming a giant whale account from having a huge impact on the future value of `PIS`, therefore, the `Dao` organization computing power rewards were completely organized For immediate destruction. The `Dao` organization needs to continuously invest energy and funds in the process of promoting the ecological development of `PISHON`. Participating in part of the `PIS` computing power output reward is to obtain some funds in the superconducting pool for the follow-up promotion of `PISHON` ecology and `PUSD. `The value building. The immediate destruction of the output of the `Dao` organization's computing power reward has a decisive impact on the exchange price of `PIS`. We can roughly regard the superconducting pool as a simplified version of the `C2C` transaction pair, and users buy in the superconducting pool. Force is equivalent to increasing the depth of buying orders, and the circulation `PIS` can be regarded as the depth of selling orders. If the bilateral depth continues to increase without triggering the transaction, the final price continues to fall. The “Dao” organization’s immediate exchange and destruction of computing power reward output is to continuously adjust the circulation of the “PIS” margin and the superconducting pool margin, so that the exchange price of the superconducting pool is in a process of dynamic growth, leading to more trading possibilities.

The members of the `Dao` organization are not only the initiators. In the process of the continuous development of the `PISHON` ecology, high-quality communities and large computing power miners will successively participate in the `Dao` organization to participate in the planning and consensus transmission work promoted by the `PISHON` ecological development Come in.

#### 3. Analysis of the advantages of computing power lending provided by PUSD for the sustainable development of PISHON liquid mining

`Magnify Hashrate` provides the `PIS` miners with a hashrate loan of 3 times the existing hashrate after the miners pledge `PUSD`. This behavior is undoubtedly a hugely attractive one for participating in the `PISHON` liquidity mining miners. Services. Allows `PIS` miners to obtain `PISHON` computing power rewards with a lower and more flexible input method, thereby obtaining a higher return on investment return, and the pledged `PUSD` can be released after two weeks (computing power) Return to the initial value).

The advantage of computing power lending compared with direct investment is obvious. In the development process of PISHON, we hope to shape the two major financial service sectors in the ecology at the same time. PiFi will use the help of Magnify Hashrate in the development process. The advantage is for participating miners to lower the threshold of participation and enhance investment flexibility. At the same time, it provides huge scene support for the popularization and application of PUSD and value shaping. However, the `PIS` mining work is a pump of digital assets and is in the process of embracing the decentralized digital financial world. Will definitely participate in a large number of high-quality `DeFi` projects, and at the same time promote `Magnify Hashrate` to develop diversified computing power mortgage lending services for more `DeFi` projects, and gradually expand the service scenarios and service content of the `PISHON` ecology.

#### 4. The number of PIS miners has increased, and the advantages of PISHON's sustainable development after the opening of the PIS secondary market

Above we have analyzed the significance of the value shaping of `PIS` after the passive opening of the `PIS` secondary market. A detailed analysis shows that when the `PIS` opens the secondary market, the price of `PIS` will follow `PISHON` The increase in the liquidity mining community, the increase in `PIS` miners, and the increase in the secondary market transaction volume have gradually occurred. The gap between the secondary market price and the exchange price of the superconducting pool `PIS` continues to widen. The greatest impact of the existence of the secondary market is that miners are unwilling to exchange money in the superconducting pool at a low price after obtaining the `PIS`, but are realized through the secondary market transaction. The essence of the transaction is circulation, not like superconducting. Destroyed like the pool exchange, according to the model we analyzed above, the larger the amount of circulating `PIS`, the lower the exchange price of the superconducting pool (when the superconducting pool balance increase cannot exceed the increase of circulating `PIS`). The larger and more frequent the transaction volume in the secondary market, the faster the value of digital assets is filled. This will cause a centrifugal force between the secondary market price and the exchange price of the superconducting pool, and the gap will become larger and larger. When the gap is dozens or even hundreds of times, `PIS` will completely decouple the value standard of superconducting pools and form a digital asset value system based on transaction and circulation needs. But the superconducting pool is still the last line of defense for the final `PIS` miners and the `PIS` consensus holders. We hope that PIS can play a greater role in transaction circulation in different scenarios, thereby expanding the impact of the `PISHON` ecology on the entire decentralized financial world.

### 3. Complementary and closed loop of PISHON dual financial ecosystem

#### 1. Pishon Finance（PiFi）

1. Drive the market to become a `PISHON` miner, and then become a part of the ecological drive
2. Complete the first show of `Magnify Hashrate` to deepen the market's understanding of the value of PUSD. To pave the way for `PISHON` to develop a decentralized traditional financial lending business.

#### 2. Magnify Hashrate

1. The most important part of the `PISHON` ecology, to build the `P2P` of the decentralized financial world.
2. Bring the community of miners attracted by the superconducting mechanism in `PISHON` to the bottom world of `DeFi` finance and become the leader and revolutionary of the new financial order.

## 六、PISHON Development Plan

### 1、Time node

#### 1. 2020 Q4

1. Complete the overall contract design and development of the `PISHON` ecology, and pass the contract audit.
2. The `Pishon Finance (PiFi)` contract is listed on `TRON` and the superconducting pool is opened for `PIS` liquidity mining and `PIS` exchange.
3. Release the `PUSD` asset synthesis contract on `TRON`.

Ⅰ. Open the asset synthesis contract of `USDT&TRX`.
Ⅱ. The asset synthesis contracts of other digital assets have been opened successively, and the contract audit and launch of no less than 5 digital assets have been completed this quarter

4. `Magnify Hashrate` opens hashrate lending for `PiFi` superconducting liquidity mining

Ⅰ. Opening of the channel for computing power lending with `PUSD` as collateral
Ⅱ. Opening of the computing power lending channel for other digital assets as pledges

#### 2. 2021 Q1

1. Promote the development of the `PIS` miner community
2. Create a new scenario for the `PISHON` ecological `PiFi` financial model

Ⅰ. Application scenarios and transaction scenarios for `PIS` circulation
Ⅱ. Application scenarios for `PUSD` circulation and other financial use scenarios

3. Establish the evaluation standard and risk control model of the `Magnify Hashrate` computing power lending access project

#### 3. 2021 Q2

1. Preliminarily establish a computing power lending experiment scenario for `Magnify Hashrate` except `PiFi`, and test and improve the risk control model
2. Import `PUSD` into more trading scenarios as legal currency circulation, increasing the circulation demand of `PUSD`

#### 4. 2021 Q3

1. Officially launched the `Magnify Hashrate` to multiple `DeFi` project, the multi-collateral computing power lending scene

#### 5. 2021 Q4

1. Steadily build the `PIS` secondary market, accelerate the filling of the transaction market value of `PIS`, and build more consensus scenarios for `PIS` to become the mainstream currency.

### 2、Advance steps

#### 1. Establish PIS superconducting mining pool

1. Drive more community participation in `PIFI`
2. Design and implement more consensus scenarios for `PIS`

#### 2. Establish PUSD issuance mechanism

1. Gradually broaden the path of `PUSD` asset synthesis, so that more effective digital assets can participate in the `PUSD` asset synthesis
2. Gradually broaden the consensus scenario of `PUSD` and participate in more scenarios where stablecoins other than `Magnify Hashrate` can participate

#### 3. The first scene of establishing Magnify Hashrate in PIFI

1. Lending computing power to `PIS` miners by pledge of `PUSD`
2.  Preliminary test of `PUSD` asset synthesis

#### 4. Promote the widespread use of PUSD in Magnify Hashrate

1. Broaden the sequence of loan pledges, and establish risk control models and basic data penetration management for computing power loans with different risks
2. Broaden the scenarios where computing power can be borrowed, evaluate the `DeFi` projects based on different public chains, and release corresponding loan products.
3. Establish the `Magnify Hashrate` loan fund pool to raise and post-investment management of the funds corresponding to the lending power

#### 5. Promote the secondary market of PIS

1. Promote the establishment of a multi-transaction scenario of `PIS`, prompting PIS to build a transaction volume in addition to the superconducting redemption mechanism
2. Promote the scene shaping of PIS by the `PIS` miner community, and expand the non-miner coin holding addresses of `PIS`

## 七、PISHON future

### 1、Pishon Finance value

The purpose of the `PISHON` ecological establishment of the `Pishon Finance` financial scene is to broaden the `PISHON` consensus and drive more users who are interested in digital assets investment and have entrepreneurial ideas on decentralized finance to enter the `PISHON` ecological co-construction and sharing a brand new Decentralized financial scenarios. The foundation of an ecological future lies in the future of a group of people. To shape an ecology is to convey a belief to a group of people who have the ability to advance the revolution to a consensus. `PISHON` provides a sufficiently fair and brand-new digital asset holding and monetization rules through the `Pishon Finance` superconducting mechanism, and promotes the ecological system through the promotion of computing power rewards, community computing power rewards, and computing power rewards. The relationship between each miner in the development is related, driving ecological development in many ways. If the PISHON ecology is assumed to be a country, then `Pishon Finance` will be a driving policy to increase the number of citizens. The development of an ecology is the same as the prosperity of a country. It requires the support of a large number of consensus, and only a large number of ecological supporters can There are more talents in the cluster who are willing to make suggestions for ecological development, provide wisdom and suggestions for the broadening of the ecological service boundary of `PISHON`, and contribute more.

### 2、Magnify Hashrate value

`Magnify Hashrate` can be infinitely extended in the `PIAHON` ecology, and determines whether the `PISHON` ecology can become an indispensable `DeFi` financial derivative service scenario in the decentralized financial world in the future. In the future, the risk control system and post-loan management rules established based on the computing power mortgage lending brought by `PiFi` will serve more and more complex `DeFi` financial products, and build a service system based on computing power lending. Through the combination of the `PISHON` ecological community, more high-quality `DeFi` projects are spawned and incubated. Gradually broaden the sequence of collateral, use the risk control model to gradually broaden the collateral from `PUSD` to most mainstream digital assets that can become collateral for the `Magnify Hashrate` computing power lending, and gradually open up `Magnify Hashrate` through cross-chain technology. The computing power lending service of the `DeFi` project built on other public chains other than `TRON` is not limited to only lending `USDT` as the general equivalent of lending computing power.

### 3、 PIS value

`PIS`, as the only proof of work of `PISHON` ecological `Pishon Finance`, bears the consensus of `PISHON` ecological value. The future value of `PIS` is equal to the total value of the ecological future value of `PISHON`. Until the end of the liquidity mining of `Pifi`, the circulating `PIS` will stimulate a huge secondary market transaction volume and a wide threshold `PIS. `Usage scenarios, by then will give birth to more decentralized financial services based on the `PISHON` ecology and the general equivalent of `PIS` and the value of digital assets.

#### 4、PUSD value

`PUSD` is a stable digital asset spawned by the `PISHON` ecology. The unique mechanism of “exchange is issued and redeemed and destroyed” determines that `PUSD` is a stable digital asset with a full gold standard, independent of any other centralized exchanges and public chains. Other stable digital assets issued based on the consensus demand of circulation. In the process of `Magnify Hashrate` being gradually applied to `PiFi` liquid mining computing power lending and more `DeFi` liquid financial projects, the issuance volume of `PUSD` which surged due to the pledge demand was finally brought about by the all-gold standard issuance mechanism. The incoming gold content will definitely be used by most scenarios that require stable digital assets. `PISHON` hopes to promote `PUSD` to replace consensus-based stable digital assets to become the legal currency of more centralized exchanges and the general equivalent in decentralized payment scenarios. Bring the `PISHON` ecology rooted in `TRON` into more financial scenarios.

## 八、Conclusion

The original intention of the design of `PISHON` ecology is to contribute to the establishment of a decentralized financial order in the future. All contract rules are designed in one piece, and the promotion steps are clear and clear, and the decentralized design and ecological development governance from the underlying technology are realized. Decentralized design. In the near future, `PISHON` will surely become one of the indispensable financial service scenarios in the decentralized financial world. All miners, communities and organizations participating in the `PISHON` ecological consensus will witness and share the `PISHON` ecological presence Great consensus value created in the future.







