# Local Exchange / Privacy

Local exchange is a sensitive operation when your digital funds may turn into government-controlled fiat money and vice versa. That's why privacy is a big concern in this case.

<div class="note danger">
  Always use VPN if you want to hide your IP!
</div>

<i class="fa fa-book"></i> *Please read our [Privacy Policy](/overview/privacy.md) before.*

## Offers

Any Offer created will have the creator's IP address stored.

Also, according to [Peerex Privacy Policy](/overview/privacy.md#ip-logging), we will log all search queries with their IPs and they will be publicly seen as well:

```
10.20.30.40: buy 1000.0 "USD" in ["gb"] with "paypal" at 01/01/17 14:55:47.005
11.22.33.44: buy 5000.0 "EUR" in ["gb"] with "wire transfer" at 01/01/17 14:56:47.005
```

## Communication

With initial Local Exchange design, no private information is either stored on-chain or goes through our servers. All sensitive details like where to send bucks from PayPal to are never seen by us because we have only two methods of communication:

* End-to-end encrypted WebRTC channel
* End-to-end encrypted messages

Here goes an explanation of each of these methods:

### WebRTC

[WebRTC](https://webrtc.org) means Web Real-Time Communication, and it's often called Peer To Peer connection.

> That where PeerEx naming comes from! <i class="fa fa-child"></i>

WebRTC technology allows you to securely communicate with other parties of the exchange directly avoiding Peerex servers. Such connection is [MITM](https://en.wikipedia.org/wiki/Man-in-the-middle_attack)-resistant.

However, to *initiate* a connection, you'll have to reveal your IP to our servers. Then, the parties will see your IP while the connection is active. And again, according to our [Privacy Policy](/overview/privacy.md#ip-logging), we will record the act of WebRTC session initialization and it result in both yours and other side's IP addresses logged publicly.

Note that you're communicating explicitly with an owner of an address and we don't know which offer does a particular session belongs to.

### Encrypted messages

This is an old-school method involving encryption with your public key and decryption with the private one. You are the only one who can ever read a message encrypted with your public key, so it can be safely transmitted via our Servers. However, we also do publicly log all transmitted messages at their initially encrypted state.

You must understand that decryption possibility grows as the time goes by and eventually anyone with enough capabilities can decrypt a message.

Also note that you're communicating explicitly with an owner of an address and we don't know which offer does a particular session belongs to.

### Third-Party messaging

You're not limited to those two communication methods only; a seller could provide a generic communication method like Jabber or Telegram which is secure in his mind and it's up to you and him to decide what to use.
