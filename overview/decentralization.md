# Decentralization

> No system is safe.

> *-- Chinese Hacker*

*We assume that you're familiar with the concept of crypto currency and its advantages over fiat money. If not so, please google it before.*

Thanks to [Stellar Consensus Protocol](https://www.stellar.org/papers/stellar-consensus-protocol.pdf) (or better read this [awesome comic](https://www.stellar.org/stories/adventures-in-galactic-consensus-chapter-1/)), Peerex transactions are fast, cheap and trusted.

In addition to the fact that your assets are stored on the crypto-verified Stellar blockchain, Peerex is designed the way that even if it gets hacked or taken down by a government, no harm is made to its users and the system. This is achieved with following techniques:

## Takedown in mind

When developing Peerex, we think of it as of ephemeral system which servers or domain name could be gone at any moment - be it a hack, government seizure or just us running away.

### Open-source code

If our website and/or server is down, any person or even company can run the code locally and get absolutely the same experience. Just imagine you could have run BTC-e locally with all your funds safe when it's been [taken down](https://btc-e.com)!

### No account access data is stored on servers

Peerex never has access to your private keys, so even if an attacker gets an access over the database, they can't gain control over your account; and you can continue using the system.

**Counter-example:** most of exchanges (e.g. Poloniex or Bittrex) have full control over your funds on it, so do hackers.

### No obligations to buy assets back

<div class="note rfc">
  <i class="fa fa-exclamation-triangle"></i> This could be frustrating at the first glance, because no exchanges currently have such a practice, but hold on
</div>

[Peerex Anchor](/anchor/README.md) is one-way - when you convert your crypto currency into Peerex asset, it's irreversible. As a result **you lose nothing** in the case of security breach on our side. Assets can still be exchangeable both on [Asset](/asset_exchange/README.md) and [Local](/local_exchange/README.md) Exchanges. Please read more at [Anchor Overview](/anchor/README.md).

**Counter-examples:**

* Recent [Youbit hack](http://money.cnn.com/2017/12/20/technology/south-korea-bitcoin-exchange-closes/index.html) lead to price drop.
* [BTC-e](https://btc-e.com) has been taken by FBI, resulting in colossal loses for all its users.

---

You can continue reading deeper explanations of decentralization by particular element at their according pages:

* <i class="fa fa-book"></i> [Anchor Decentralization](/anchor/decentralization.md)
* <i class="fa fa-book"></i> [Asset Exchange Decentralization](/asset_exchange/decentralization.md)
* <i class="fa fa-book"></i> [Local Exchange Decentralization](/local_exchange/decentralization.md)
* <i class="fa fa-book"></i> [Payments Platform Decentralization](/payments/decentralization.md)
