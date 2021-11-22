# XCADDEX-API

API server for XCAD DEX

The web service exposes these end points.
You can find the sample data for each end point here

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
To be implemented

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
To be implemented

