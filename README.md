# nfts-as-subscriptions

## Preface

NFTs have been used for raising funds by many orgnizations / individuals for altruistic or whatever
reasons. The NFT minting fees are the main source of initial revenue with some royalties on all
subsequent sales on secondary market places which is usually only a minor part of the total revenue.

For sustaining and continuously raising new funds one can opt / try to implement a subscription service
that will require the minters to regularly pay for the NFTs to keep owning them which can be used for
token-gating anything, etc.

## Solution

We can ensure the inactive subscriptions / NFTs are burnt as they should and on time by introducting
incentives to carry out those operations on-chain. Proposed method here is to:
1. Introduce a deposit(e.g. 0.1 ETH) that will be seized if the user fails to cancel their subscription and does 
   not pay for the subsequent period.
2. Allow anyone to carry out the burn operation on any such NFTs that still exist but didn't pay up their subscription
   fee for the period. The users are incentivized to do this because whoever would call this and help the subscription
   service by burning inactive subscriptions would be paid the deposit amount that the user had deposited when they
   started the subscription. 
3. The users are also allowed to cancel their subscriptions by calling `burn` themselves and they'd be refunded their deposits.

With such incentives we can ensure that the protocol's subscriptions / NFTs are always active / valid. No stale subscriptions
that will still remain active, etc.
