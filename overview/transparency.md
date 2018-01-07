# Transparency

We aim to make Peerex platform as much transparent as possible. We do not want you to trust us, but to be able to verify everything what's happening inside.

## Open-source

First of all, 100% of the client-side code is open-sourced and available at our Github: [github.com/peerex](https://github.com/peerex). Even the book you're currently reading is open-sourced too.

Next, back-end. The truth is that even if we're publishing the source code, there is no way one can verify whether is it the same on our servers or not. Moreover, some elements have sensitive information stored on the servers, which could make the system less stable in some way. For example, Anchor server must have spend keys stored on it so we can process Upgrades automatically, and attacker could send some assets to himself - nobody wants it.

However, other elements, such as Local Exchange, do not store any harmful secrets, and in the case of breach the system will stay stable. So we could publish its code. Maybe someday it will be possible to run publicly open servers where users can log in and see what's going on inside.

We will eventually publish the back-end source code for the most of the elements, but there are some other reasons preventing us of doing it right now.

But as we're open organization, we will encourage free folks to share their back-end (as well as front-end) implementations of the elements.

## Operations transparency

<div class="note warn">
  Remember that the whole history of a particular Stellar account can be seen!
</div>

**Transparency in brief by element:**

* <i class="fa fa-check success"></i> **Wallet** - no back-end, contacting with Stellar network only
* <i class="fa fa-exclamation-triangle warn"></i> **Anchor** - each Stellar transaction is bound to a particular Upgrade. You can see the whole history of the anchor and verify that no asset is transferred without corresponding crypto-transaction. Also each Upgrade is revealing the source IP address ([read more](anchor/transparency.md))
* <i class="fa fa-check success"></i> **Asset Exchange** - no back-end, contacting with Stellar network only
* <i class="fa fa-exclamation-triangle warn"></i> **Local Exchange** - each Offer created has an origin IP address and Stellar public key of the creator. Furthermore, each WebRTC end-to-end session initialization attempt is listed too with peers' IP addresses ([read more](local_exchange/transparency.md))
* <i class="fa fa-exclamation-triangle warn"></i> **Payments Platform** - basically, a merchant is a programmatic user of Asset and Local Exchanges, so the same rule are applied to it
