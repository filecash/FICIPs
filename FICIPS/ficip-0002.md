# Support 4G sector



### Brief intro

- Support 4G sector

### Summary

- Filecash is an IPFS-based distributed storage network, dedicated to building Web 3.0 storage infrastructure based on IPFS, hoping to make use of idle storage space and build cloud storage market for everyone.

- Filecash lowers the threshold for storage providers by upgrading current AMD-centric algorithms to support Intel processors to reduce submission time.

- Token reward mechanism is based on effective storage, where miners receive satisfying token reward, and the release time is shorter compared to other products in the market.

- Excessive punishment in Window-post proof algorithms only hinders miner motivation and participation, Filecash therefore seeks to balance between network stability and miner loss.

- As a community-driven project, Filecash encourages and adopts suggestions from communities, developers and miners to achieve a truly autonomous market balance.

### Why 4G sector

Large sectors such as 64G and 32G impose high entry limit for participants. Filecash embraces more participants with the much lowered entry threshold - 4 G sectors added.

Large sectors have high requirements for equipment memory and performance, and it is difficult for ordinary miners to meet the hardware requirements. 4G sectors meet the needs of most miners in the market.

### Technical specifications

Note: github does not support formulas, search and install MathJax Plugin for Github in Google Store

https://chrome.google.com/webstore/detail/mathjax-3-plugin-for-gith/peoghobgdhejhcmgoppjpjcidngdfkod

##### Support 4G sector
- Precommit pre-pledge
$$
collateralpre = 20 \times \frac{SectorPower}{NetworkPower} \times CurrEpochReward \times Epochslnday \times \frac{110}{100}
$$

- Commit2 pledge
$$
ipBase = 20 \times \frac{SectorPower}{NetworkPower} \times CurrEpochReward\times Epochslnday
$$

$$
additionalIP = \frac{30}{100} \times CircSupply \times \frac{SectorPower}{NetworkPower}
$$

$$
initialPledge=Min (ipBase + additionalIP , SpaceRaceInitialPledgeMaxPerByte \times 4G) \times  \frac{110}{100}
$$

- Refund

$$
Refund = collateralpre - initialPledge
$$
