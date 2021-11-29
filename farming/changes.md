# Changes from HoneyFarm

The [CheemscoinFarm](https://github.com/cryptocheems/farm-contracts/blob/master/contracts/CheemscoinFarm.sol) contract is a fork of the [HoneyFarm](https://github.com/1Hive/honeyswap-farm/blob/master/contracts/HoneyFarm.sol) contract made by [1Hive](https://wiki.1hive.org) for [https://1hive.io/#/farm](https://1hive.io/#/farm).  The core functionality is the same but there are some changes.&#x20;

{% hint style="info" %}
Note that the HoneyFarm contract is owned by a Governance contract whereas the CheemscoinFarm contract is owned by the [developer](https://blockscout.com/xdai/mainnet/address/0xB67D4dd9F0E25760dC0f373d79588Bd0169b2335/transactions).
{% endhint %}

## Changes

* Change formatting and comments
* Allow anyone to call `depositAdditionalRewards`
* Remove referral rewards
  * This would give some extra Cheemscoin to whoever made the frontend the deposit was created from whenever the deposit is harvested from.&#x20;
  * Remove `referrer` from the `DepositInfo` struct
  * Remove `rewardManager`,  `setRewardManager`, `_rewardReferrer`, `Referred` and `RewardManagerSet`
  * Don't require `rewardManager` to exist in `add` function
  * Don't set a referrer in `createDeposit`
  * Don't call `_rewardReferrer` in `closeDeposit` or `withdrawRewards`
* The contract no longer inherits from an interface (`IHoneyFarm`) so `override` is removed from all functions
* Do not allow no-lock deposits (`_unlockTime` of`0`)
* Add `recoverToken` function that only the owner can call.&#x20;
  * The purpose of this is so if a token is accidentally sent to the contract, it can be recovered.
  * When called, it transfers the entire balance of the specified token to the owner
  * The specified token can not be Cheemscoin or any of the LP tokens that you can stake
* Add `multiWithdraw` `external` function
  * calls `withdrawRewards` on all `_depositIds`

### View Functions

* Add `pragma abicoder v2;` (to return structs)
* Add `PoolDetails`, `ExpiredDeposit` and `DepositDetails` structs
* Modify `getPoolByIndex` to return `PoolDetails` and make it `public`
* Add `getAllPools` function
  * Returns an array of `PoolDetails` about each pool
* Add `getAccountDeposits` function
  * Returns an array of `DepositDetails` about each deposit the `_account` owns
* Add `getExpiredDepositIds` function
  * Returns an array of `ExpiredDeposit`
* Make `pendingHsf` `public`

