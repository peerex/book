# Anchor / Transparency

We don't want a user to have to trust Peerex. That's why each Upgrade has a record of the source transaction (say, Bitcoin payment) and the resulting Stellar transaction. It allows to verify that an Upgrade is real and real coins are spent, reducing a possibility of fraud on our side.

However, we are able to use a VPN, take the same coins you've sent to Peerex, wash them in a laundry and repeat an Upgrade process forever and you can do nothing with it. In this scenario we only will be richer and you lose nothing, because those "fake" assets will be indistinguishable from the "real" ones, so no user would suspect anything.

We could claim that all coins are burnt irreversibly, but would you believe us deleting those private keys? We wouldn't.

<div class="note">
  <i class="fa fa-user-secret"></i> Dear attackers, it is impossible for you to grab those "real" coins, because we don't store coin spend keys on Peerex servers ¯\_(ツ)_/¯
</div>

### Stealing Assets

If an attacker had an access to our servers, they would try to send themselves some Peerex Assets. However, they would not be able to find a proper coin transaction with our address as a target one and therefore it would result in marking this Upgrade as invalid.

Thanks to `AUTHORIZATION REVOCABLE` flag ([read more](https://www.stellar.org/developers/guides/concepts/assets.html#revoking-access)), we will be able to freeze such a fraud account.

<div class="note rfc">
  <i class="fa fa-lightbulb-o"></i> Revoking access is a tough topic and we encourage you to share your opinion on Reddit, Twitter or Telegram Chat.
</div>

## IP addresses

Each Upgrade holds a record of originating IP address. See <i class="fa fa-book"></i> [Peerex Privacy Page](/overview/privacy.md#ip-logging).
