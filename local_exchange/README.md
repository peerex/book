# Local Exchange / About

Peerex Local Exchange is an essential element of Peerex platform. It allows to exchange your [Stellar Lumens](https://www.stellar.org/lumens/) and [Stellar assets](https://www.stellar.org/developers/guides/concepts/assets.html) off-chain to literally anything and vice versa! It could be crypto-currencies, fiat money or anything else (say, a car).

<i class="fa fa-check success"></i> Peerex does not take any fees from local exchanges made.

**The Local Exchange element consists of two parts:**

* Front-end Javascript Client
* Back-end application on our side having these functions:
  * Storing Offers
  * Connecting users via [secure end-to-end WebRTC connections](/local_exchange/privacy.md#webrtc)
  * Connecting users with [instant end-to-end encrypted messages](/local_exchange/privacy.md#encrypted-messages)

## Local Exchange flow

### Step 1. Create an Offer

For example, you want to sell your `Peerex BTC` for `USD` or `EUR` via PayPal or Wire transfer. That's where you use the Local Exchange. You create a sell Offer, sign it with your Stellar private key and set it up with params like these (simplified draft):

```json
{
  "payload": {
    "sell": {
      "account": "<your Stellar public key>",
      "assets": [{
        "code": "BTC",
        "issuer": "Peerex"
      }]
    },
    "buy": {
      "methods": [{
        "slug": "paypal",
        "name": "PayPal",
        "description": "Gonna sell you Bitcoins with PayPal",
        "countries": null // All countries
      }, {
        "slug": "wire",
        "name": "Wire Transfer",
        "description": "Banks too",
        "countries": ["gb"]
      }],
      "assets": [{
        "code": "USD",
        "description": "United States Dollar"
      }, {
        "code": "EUR",
        "description": "Euro"
      }]
    },
    "description": "Hi there, wanna sell some BTC. My jabber is jabber@jabber.org",
    "accept_webrtc": true, // A buyer would be able to connect to you via WebRTC connection
    "accept_messages": true, // A buyer would be able to send you encrypted messages via Peerex servers
  },
  "signature": "<signature of the payload made with your Stellar private key>"
}
```

### Step 2. Wait for a buyer

Then a buyer uses the Local Exchange Javascript client to find appropriate Offers:

```json
{
  "sell": "USD",
  "buy": {
    "asset": {
      "code": "BTC",
      "issuer": "Peerex"
    },
    "method_query": "paypal"
  },
  "countries": ["gb"]
}
```

Note that a buyer is not necessarily has to have an active Stellar account because you can add `Create Account` operation into the resulting transaction.

### Step 3. Contact the buyer

The system will match the buyer with your Offer and they'll have either to:

* Contact you via Jabber
* Initiate a secure end-to-end WebRTC session (involving Peerex servers)
* Send you a message encrypted with your public key (it will be sent via Peerex servers as well)

A buyer can also be a program, which you will interact via API Protocol with. Moreover, you can be a program too, bloop-blop! <i class="fa fa-android success"></i>

### Step 4. Reach an agreement on the transaction

Whichever communication method is chosen, you'll be building a [Stellar Transaction](https://www.stellar.org/developers/guides/concepts/transactions.html) together. This transaction will describe the algorithm of your future exchange, including amounts, fees, penalties, refunds and so on. It's up to you how to build it, but Peerex provides you with convenient tools which will help you to make a fair and secure exchange.

As Peerex is an open platform, you would also be able to call for a non-affiliated trusted third-party Escrow, which would solve disputes in the case of any issues.

### Step 5. Boost your reputation

If the exchange is successful, you both will gain positive reputation, which will simplify your future exchanges. In case of failure or fraud both yours and the buyer's reputations will be penalized. To reduce the possibility of failure, different techniques are applied.

The reputation system is designed to be on-chain, so even if the Local Exchange is gone, people still would be able to use its advantages.

<i class="fa fa-book"></i> *Continue reading about reputation at [Decentralization Page](/local_exchange/decentralization.md)*.
