# XCADDEX-API

API server for XCAD DEX

The web service exposes these end points.
You can find the sample data for each end point here

Where the result consists of multiple pages ( i.e. where total_pages > 1)
use query parameter ?page=n  where n = page number e.g. 2

# [get("/")]
http://localhost:3010/
Returns a string to indicate that the webservice is running
Hello xcaddex!

#[get("/swaps")]

# [get("/liquidity_changes")]
http://localhost:3010/liquidity_changes

```json{
  "records": [
    {
      "id": "89f6d1fc-64cf-420f-b5ef-58eebbd3e8b9",
      "transaction_hash": "0x118e022d1c65530d902d807d89adb552fb6e444adb58b039f3998b367afe6f3b",
      "event_sequence": 0,
      "block_height": 3504704,
      "block_timestamp": "2021-11-18T17:58:26",
      "initiator_address": "zil150uv303w8ttzcml8w200ptzq957637wel8p8ev",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "change_amount": "250058346",
      "token_amount": "208486200",
      "zil_amount": "300000000"
    },
    {
      "id": "af9c9286-b1a6-4af8-a4ed-b554351019ce",
      "transaction_hash": "0x97f4db1f15c5b558c7db9295988444c85b6a4f4b486f00db3caac1ffee5b1059",
      "event_sequence": 0,
      "block_height": 3491896,
      "block_timestamp": "2021-11-15T12:32:04",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "change_amount": "1000000000",
      "token_amount": "1000000000",
      "zil_amount": "1000000000"
    },
    {
      "id": "6b8cc6a4-c2ae-4323-aeea-74fc37864818",
      "transaction_hash": "0x27921c38b3563dbe38039500b62ede860a9b6cddf6861a58bf3ba7c8143b3979",
      "event_sequence": 0,
      "block_height": 3491883,
      "block_timestamp": "2021-11-15T12:27:31",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "change_amount": "-1476952902",
      "token_amount": "1363655832",
      "zil_amount": "1599860000"
    },
    {
      "id": "c26831ef-024e-4225-9925-4576e7bf3f5c",
      "transaction_hash": "0xf5071ab9900a89dd2c442cce8e5cff3d517f2a37f0a8178c105de4678adc5b41",
      "event_sequence": 0,
      "block_height": 3491848,
      "block_timestamp": "2021-11-15T12:15:16",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "change_amount": "276952902",
      "token_amount": "255707843",
      "zil_amount": "300000000"
    },
    {
      "id": "8d10b15e-5c02-46da-bdb1-b9835f16d66a",
      "transaction_hash": "0x856c5d8cec4b07cce0a71ee4b6814de43f63ca35b20d5ecd171712ff9c488159",
      "event_sequence": 0,
      "block_height": 3491838,
      "block_timestamp": "2021-11-15T12:11:46",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "change_amount": "200000000",
      "token_amount": "200000001",
      "zil_amount": "200000000"
    },
    {
      "id": "6c4d36ee-de7c-4bc8-8587-5a25ded3332e",
      "transaction_hash": "0xca6735cb3b3445ea7c4528eb848a5e90fcaa488e5812798609c6d2324b03a68a",
      "event_sequence": 0,
      "block_height": 3491831,
      "block_timestamp": "2021-11-15T12:09:19",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "change_amount": "1000000000",
      "token_amount": "1000000000",
      "zil_amount": "1000000000"
    }
  ],
  "total_pages": 1
}
```

# [get("/liquidity")]
http://localhost:3010/liquidity
```json
[
  {
    "pool": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
    "amount": "1250058346"
  }
]
```

# [get("/weighted_liquidity")]
http://localhost:3010/weighted_liquidity
```json
[
  {
    "pool": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
    "amount": "98813779912"
  }
]
```

#[get("/transactions")]
http://localhost:3010/transactions
```json
{
  "records": [
    {
      "id": "89f6d1fc-64cf-420f-b5ef-58eebbd3e8b9",
      "transaction_hash": "0x118e022d1c65530d902d807d89adb552fb6e444adb58b039f3998b367afe6f3b",
      "block_height": 3504704,
      "block_timestamp": "2021-11-18T17:58:26",
      "initiator_address": "zil150uv303w8ttzcml8w200ptzq957637wel8p8ev",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "token_amount": "208486200",
      "zil_amount": "300000000",
      "tx_type": "liquidity",
      "swap0_is_sending_zil": null,
      "swap1_token_address": null,
      "swap1_token_amount": null,
      "swap1_zil_amount": null,
      "swap1_is_sending_zil": null,
      "change_amount": "250058346"
    },
    {
      "id": "af9c9286-b1a6-4af8-a4ed-b554351019ce",
      "transaction_hash": "0x97f4db1f15c5b558c7db9295988444c85b6a4f4b486f00db3caac1ffee5b1059",
      "block_height": 3491896,
      "block_timestamp": "2021-11-15T12:32:04",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "token_amount": "1000000000",
      "zil_amount": "1000000000",
      "tx_type": "liquidity",
      "swap0_is_sending_zil": null,
      "swap1_token_address": null,
      "swap1_token_amount": null,
      "swap1_zil_amount": null,
      "swap1_is_sending_zil": null,
      "change_amount": "1000000000"
    },
    {
      "id": "6b8cc6a4-c2ae-4323-aeea-74fc37864818",
      "transaction_hash": "0x27921c38b3563dbe38039500b62ede860a9b6cddf6861a58bf3ba7c8143b3979",
      "block_height": 3491883,
      "block_timestamp": "2021-11-15T12:27:31",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "token_amount": "1363655832",
      "zil_amount": "1599860000",
      "tx_type": "liquidity",
      "swap0_is_sending_zil": null,
      "swap1_token_address": null,
      "swap1_token_amount": null,
      "swap1_zil_amount": null,
      "swap1_is_sending_zil": null,
      "change_amount": "-1476952902"
    },
    {
      "id": "c26831ef-024e-4225-9925-4576e7bf3f5c",
      "transaction_hash": "0xf5071ab9900a89dd2c442cce8e5cff3d517f2a37f0a8178c105de4678adc5b41",
      "block_height": 3491848,
      "block_timestamp": "2021-11-15T12:15:16",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "token_amount": "255707843",
      "zil_amount": "300000000",
      "tx_type": "liquidity",
      "swap0_is_sending_zil": null,
      "swap1_token_address": null,
      "swap1_token_amount": null,
      "swap1_zil_amount": null,
      "swap1_is_sending_zil": null,
      "change_amount": "276952902"
    },
    {
      "id": "8d10b15e-5c02-46da-bdb1-b9835f16d66a",
      "transaction_hash": "0x856c5d8cec4b07cce0a71ee4b6814de43f63ca35b20d5ecd171712ff9c488159",
      "block_height": 3491838,
      "block_timestamp": "2021-11-15T12:11:46",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "token_amount": "200000001",
      "zil_amount": "200000000",
      "tx_type": "liquidity",
      "swap0_is_sending_zil": null,
      "swap1_token_address": null,
      "swap1_token_amount": null,
      "swap1_zil_amount": null,
      "swap1_is_sending_zil": null,
      "change_amount": "200000000"
    },
    {
      "id": "6c4d36ee-de7c-4bc8-8587-5a25ded3332e",
      "transaction_hash": "0xca6735cb3b3445ea7c4528eb848a5e90fcaa488e5812798609c6d2324b03a68a",
      "block_height": 3491831,
      "block_timestamp": "2021-11-15T12:09:19",
      "initiator_address": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
      "token_address": "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10",
      "token_amount": "1000000000",
      "zil_amount": "1000000000",
      "tx_type": "liquidity",
      "swap0_is_sending_zil": null,
      "swap1_token_address": null,
      "swap1_token_amount": null,
      "swap1_zil_amount": null,
      "swap1_is_sending_zil": null,
      "change_amount": "1000000000"
    }
  ],
  "total_pages": 1
}
```

#[get("/volume")]
To be implemented

# [get("/distribution/info")]
http://localhost:3010/distribution/info
This is the info from the config.yml
```json
[
  {
    "name": "dXCAD Rewards",
    "reward_token_symbol": "dXCAD",
    "reward_token_address_hex": "0x17c81253b9de207c98381c0ca3c84f2d151928c7",
    "distributor_name": "XcadDEXDistributor",
    "distributor_address_hex": "0x4a28a0b3d3fc98a52fc128e3cd40c77a88da696e",
    "developer_address": "zil1ytk3ykwlc2vy8fyp7wqp492zjassj5mxzgscv6",
    "emission_info": {
      "epoch_period": 60,
      "tokens_per_epoch": "1000000000",
      "tokens_for_retroactive_distribution": "0",
      "retroactive_distribution_cutoff_time": 0,
      "distribution_start_time": 1637136000,
      "total_number_of_epochs": 43200,
      "initial_epoch_number": 0,
      "developer_token_ratio_bps": 0,
      "trader_token_ratio_bps": 0
    },
    "incentivized_pools": {
      "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10": 1
    }
  }
]
```
# [get("distribution/generate/{id}")]
http://localhost:3010/distribution/generate/0
id: is the index into the list of configurations in the config.yml file
it is 0 indexed - first config is number 0

# [get("/distribution/estimated_amounts/{user_address}")]
Given a user address return list of Pools and Estimated reward amount for current epoch
Return data format:
{ 
    TokenDistributorContractHash: {
        PoolKey: EstinatedRewardAmount,        
        PoolKey: EstinatedRewardAmount,        
        PoolKey: EstinatedRewardAmount,        
    }
}
http://localhost:3010/distribution/estimated_amounts/zil150uv303w8ttzcml8w200ptzq957637wel8p8ev
```json
{
  "0x4a28a0b3d3fc98a52fc128e3cd40c77a88da696e": {
    "0x17c81253b9de207c98381c0ca3c84f2d151928c7,0x25430edb4fb51d6082d3410ade9f214d1a03ab10": "200037321"
  }
}
```

# [get("/distribution/claimable_data/{user_address}")]
Return data required for making reward claim.

http://localhost:3010/distribution/claimable_data/zil150uv303w8ttzcml8w200ptzq957637wel8p8ev
```json
[
  {
    "id": "b00668f9-6396-48ea-a2af-a44c45fab440",
    "distributor_address": "0x4a28a0b3d3fc98a52fc128e3cd40c77a88da696e",
    "epoch_number": 2234,
    "address_bech32": "zil150uv303w8ttzcml8w200ptzq957637wel8p8ev",
    "address_hex": "a3f8c8be2e3ad62c6fe7729ef0ac402d3da8f9d9",
    "amount": "196646889",
    "proof": "0a2c29922304883accb6e0222d7d75e5055e8323eea06504edb5a2352349c387 ddf9fc4e8f35b3246cedeb7d5db9f9e95176d94879828d36d770a8135bda7341 2b2443add7dce1c67617a289a3f4c1657747681f2f08bed331b137fc033245b7"
  }
]
```

# [get("/distribution/data/{distributor_address}/{epoch_number}")]
http://localhost:3010/distribution/data/0x4a28a0b3d3fc98a52fc128e3cd40c77a88da696e/2234
```json
[
  {
    "id": "b00668f9-6396-48ea-a2af-a44c45fab440",
    "distributor_address": "0x4a28a0b3d3fc98a52fc128e3cd40c77a88da696e",
    "epoch_number": 2234,
    "address_bech32": "zil150uv303w8ttzcml8w200ptzq957637wel8p8ev",
    "address_hex": "a3f8c8be2e3ad62c6fe7729ef0ac402d3da8f9d9",
    "amount": "196646889",
    "proof": "0a2c29922304883accb6e0222d7d75e5055e8323eea06504edb5a2352349c387 ddf9fc4e8f35b3246cedeb7d5db9f9e95176d94879828d36d770a8135bda7341 2b2443add7dce1c67617a289a3f4c1657747681f2f08bed331b137fc033245b7"
  },
  {
    "id": "691f4506-4c46-4d9c-9974-bf4577cafcb5",
    "distributor_address": "0x4a28a0b3d3fc98a52fc128e3cd40c77a88da696e",
    "epoch_number": 2234,
    "address_bech32": "zil1eym5x5vxpd2v5ltq0uu5sz4dy2aaw5gps9qhzs",
    "address_hex": "c9374351860b54ca7d607f39480aad22bbd75101",
    "amount": "786403978",
    "proof": "ddf9fc4e8f35b3246cedeb7d5db9f9e95176d94879828d36d770a8135bda7341 0a2c29922304883accb6e0222d7d75e5055e8323eea06504edb5a2352349c387 2b2443add7dce1c67617a289a3f4c1657747681f2f08bed331b137fc033245b7"
  }
]
```

# [get("/claims")]
http://localhost:3010/claims
```json
{
  "records": [
    {
      "id": "eedcde21-9b1e-40db-aef7-9880759a01da",
      "transaction_hash": "0x4edc0f97ed16a83022d55866039a8f85301f9f6609b18b34b164c065c04eaebe",
      "event_sequence": 2,
      "block_height": 1594212,
      "block_timestamp": "2021-11-18T02:17:29",
      "initiator_address": "zil18p32qmf79yrtsk9nt4rff3gk03ea85t438zpat",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "1546970453567343342"
    },
    {
      "id": "96b62eb2-ebab-43b3-bc8e-d5df30593267",
      "transaction_hash": "0x8ca5c63b7b2dfa59383ce841bef82cb279b2ec4daad308b182a644cc573d85b0",
      "event_sequence": 2,
      "block_height": 1592500,
      "block_timestamp": "2021-11-17T09:58:46",
      "initiator_address": "zil1ny48m9jangd4wlmra6438ncjkxcs7gm0wzd7q5",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "431060488986859467125"
    },
    {
      "id": "cd5c027d-d3bd-40a8-870f-e0d5c0387aae",
      "transaction_hash": "0x9451f571d7a75afdea9954915634983bb9a64f06426d5d4697612b7fd27f9785",
      "event_sequence": 2,
      "block_height": 1592500,
      "block_timestamp": "2021-11-17T09:58:46",
      "initiator_address": "zil1mdtcs5ryzqytzfz23j9y2plgu9twc7gp4ffrls",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "377005326183808270420"
    },
    {
      "id": "5bf5d86d-54e0-493b-8db2-65117f03deeb",
      "transaction_hash": "0x958e85ad26cdba9d95ef78b8288e2f43900ddf362e063b795a6c3e569229f0a6",
      "event_sequence": 2,
      "block_height": 1592501,
      "block_timestamp": "2021-11-17T09:59:17",
      "initiator_address": "zil1v54sjxeu2jejv6ufk7tr0g7rtx9awvy9pjld2y",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "73965576008131548517"
    },
    {
      "id": "e9f34bf6-056e-42aa-aadd-baa031558ff8",
      "transaction_hash": "0x9f86ef351641becb580590b77862a13df8beab331cd47a74543cccc7aef2242a",
      "event_sequence": 2,
      "block_height": 1592501,
      "block_timestamp": "2021-11-17T09:59:17",
      "initiator_address": "zil17k0fs30hy52pev2ctucrk939kmc6apjkxz5raz",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "762576798388827101"
    },
    {
      "id": "01cf39cd-c523-4a0d-aaaa-ffc0168f1a03",
      "transaction_hash": "0xef46cb283e90a82657b3fd33427beb686fb880ebaa637a2ba8fdf2881f230586",
      "event_sequence": 2,
      "block_height": 1592501,
      "block_timestamp": "2021-11-17T09:59:17",
      "initiator_address": "zil1cy8eyw84rqkamwv8y0cfh8c9zmc84x8l04rsqj",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "1647518612644636807"
    },
    {
      "id": "012751f0-c316-4935-82a8-50a5c1d2012d",
      "transaction_hash": "0xe1db6256d67f9000c639f0d8d3ae22920ec801c0d4e78d4c0c4a61a3be19cd35",
      "event_sequence": 2,
      "block_height": 1592504,
      "block_timestamp": "2021-11-17T10:00:57",
      "initiator_address": "zil1tpjzy759jtl3njwx35hqhs90vc2xftps4nz3me",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "6561006879626856362"
    },
    {
      "id": "32dd7c12-b2c6-4dbe-8602-aac2c02ef717",
      "transaction_hash": "0x02c60444be9a576941b1b0f3d6a56ab2fb40fc266fa75f330b1cbd38066c444e",
      "event_sequence": 4,
      "block_height": 1592514,
      "block_timestamp": "2021-11-17T10:06:17",
      "initiator_address": "zil162z07d7lvjecx8p0ryy4u58sn3hvffygh30m0t",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "7505935796245750761"
    },
    {
      "id": "b80ec854-2d5d-4636-befd-d5caeb66f0a9",
      "transaction_hash": "0xe270014c41640407e7b867cf996b94e17852b37392f884b4469861c5e1708c72",
      "event_sequence": 0,
      "block_height": 1612958,
      "block_timestamp": "2021-11-25T11:53:55",
      "initiator_address": "zil1mamaztmnd0ykl2rkghxs5utpx7dpvu57tfwuc8",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "4553536695825218754"
    },
    {
      "id": "dc73c8e2-9198-4aa5-9be2-d3dcab78c2fa",
      "transaction_hash": "0x77466b0b4f7ea4bcdf81453224c6fca80ff11b436e470e1dc039510162cf0082",
      "event_sequence": 0,
      "block_height": 1592531,
      "block_timestamp": "2021-11-17T10:15:14",
      "initiator_address": "zil1syj07m7rjwa94myzsq9lcjre24lega933ftt67",
      "distributor_address": "0xad48b1c421b7b55e03f91b74681d97f5701c1060",
      "epoch_number": 0,
      "amount": "13446791182759431671"
    }
  ],
  "total_pages": 62
}
```

