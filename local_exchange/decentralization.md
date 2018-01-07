# Local Exchange / Decentralization

Peerex is a platform and our mission is to provide *tools* for successful financial communications. Peerex is also decentralized, so no party should be dependent on it.

The Local Exchange is an essential element of Peerex platform, that's why it's so important to make it as much decentralized as possible.

## Human relations problem

Human relations often involve lying and so we can not just trust a stranger about money. Bitcoin, the First Crypto Currency, has resolved a part of this problem by introducing mathematical algorithms which confirm the ownership of funds and terminate the possibility of coin duplication.

But the problem of trustlessness of off-chain exchanges still exists. How would you trust anyone to exchange your 3 BTC to real-world USD? It's a big amount of money and a person can trick you stealing the coins.

One factor which could increase your confidence in another party is reputation. A well-known exchanger with solid reputation would trick you with lesser probability, because they value their reputation more than your money.

Nevertheless, if the sum is big enough (say, 100 BTC) and they have a chanсe to steal sacrificing their reputation only, would they do it? Much likely.

So what we see here is a value of reputation. It is real and can be measured in terms of funds. And what we need is to introduce some kind of material reputation which one would be afraid to lose. What can that be?

## TRUST token?

It could be a frozen asset called `TRUST` which only *Peerex TrustBot* could send to a user, but it would have reduced the decentralization.

## On-chain reputation

So we've come up with a more elegant solution. Every account has reputation points based on an amount of transactions they've ever made with `"localExchange"` memo with unique active accounts (each of which costs at least 20 XLM). A successful exchange results in a positive reputation gain, a negative one - with a penalty to both parties.

This algorithm motivates users to gain more reputation to exchange bigger sums and prevents them from fraudulent behavior.

Moreover, the whole history is on-chain, so even if Peerex Local Exchange is gone, users still will be able to see others' reputation and decide whether it worths to exchange with them because the algorithm is eventually open-sourced as well.
