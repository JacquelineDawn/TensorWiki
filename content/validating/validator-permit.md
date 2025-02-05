---
title: Validator Permit
---
Only the largest 128 validators, in terms of stake, on any particular subnetwork are considered to have `validator permit`. Validators with permit are considered active within Bittensor's mining mechanism, Yuma Consensus, can validate the network, and get `dividends`.

### How do I check to see if my validator has permit?
The amount can be pulled from the metagraph based on your uid.
```python numbered dark
import bittensor as bt
subnet = bt.metagraph(1)
wallet = bt.wallet( name = 'my_wallet_name', hotkey = 'my_validator_hotkey_name' )
my_uid = subnet.hotkeys.index( wallet.hotkey.ss58_address )
print ('validator permit', subnet.validator_permit[ my_uid ])
```

### How much TAO is required to attain a validator permit?
The amount of TAO required is depends on how the other largest 128 wallets distribute TAO across themselves. You can calculate the minimum using `bt.metagraph`:
```python numbered dark
import bittensor as bt
subnet = bt.metagraph(1)
stake_requirement = subnet.S.sort()[0][-128:]
print ('validator permit requirement', stake_requirement)
```