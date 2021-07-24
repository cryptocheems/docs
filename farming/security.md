---
description: Details about the audits and security measures used
---

# Security

Since the [CheemscoinFarm](https://github.com/cryptocheems/farm-contracts/blob/master/contracts/CheemscoinFarm.sol) contract is a fork of the [HoneyFarm](https://github.com/1Hive/honeyswap-farm/blob/master/contracts/HoneyFarm.sol) contract, the [audits](https://wiki.1hive.org/projects/honeyswap/audits-and-security) done by CertiK and 1Hive mostly apply. Note that no audit has been done of the CheemscoinFarm contract directly so the changes have not been audited. You can see all of the changes [here](technical-details.md).

The contract has been extensively tested on the Rinkeby test network and a live test run was done with 140 actual Cheemscoin as rewards on the xDai Chain for a week. The only issue found was that the `getExpiredDepositIds`function would also return already downgraded deposits. This only affected the UI and none of the functionality and it has now been fixed. One of the testers also requested withdraw-all functionality and that has now been added too. 

Although these measures have been used, it's still possible for there to be vulnerabilities. If you find any, report them to a mod in the discord and you will be rewarded with Cheemscoin. 

