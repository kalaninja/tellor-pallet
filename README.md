# Tellor

[![Check Set-Up & Build](https://github.com/tellor-io/tellor-pallet/actions/workflows/check.yml/badge.svg?branch=main)](https://github.com/tellor-io/tellor-pallet/actions/workflows/check.yml)
[![Run Tests](https://github.com/tellor-io/tellor-pallet/actions/workflows/test.yml/badge.svg?branch=main)](https://github.com/tellor-io/tellor-pallet/actions/workflows/test.yml)

This repo is a clone of this work [here](https://github.com/evilrobot-01/substrate-pallets/tree/tellor).

## Porting Progress

### AutoPay

| Dispatchable Function                  |  Functional Test   | Notes |
|----------------------------------------|:------------------:|-------|
| :white_check_mark: `claim_onetime_tip` | :white_check_mark: |       |
| :white_check_mark: `claim_tip`         | :white_check_mark: |       |
| :white_check_mark: `fund_feed`         | :white_check_mark: |       |
| :white_check_mark: `setup_data_feed`   | :white_check_mark: |       |
| :white_check_mark: `tip`               | :white_check_mark: |       |

| Runtime API                                       |   Functional Test   | Notes              |
|---------------------------------------------------|:-------------------:|--------------------|
| :white_check_mark: `get_current_feeds`            | :white_check_mark:  | No reference test. |
| :white_check_mark: `get_current_tip`              | :white_check_mark:  |                    |
| :white_check_mark: `get_data_feed`                | :white_check_mark:  |                    |
| :white_check_mark: `get_funded_feed_details `     | :white_check_mark:  |                    |
| :white_check_mark: `get_funded_feeds`             | :white_check_mark:  |                    |
| :white_check_mark: `get_funded_query_ids`         | :white_check_mark:  |                    |
| :white_check_mark: `get_funded_single_tips_info`  | :white_check_mark:  |                    |
| :white_check_mark: `get_past_tip_count`           | :white_check_mark:  |                    |
| :white_check_mark: `get_past_tips`                | :white_check_mark:  |                    |
| :white_check_mark: `get_past_tip_by_index`        | :white_check_mark:  |                    |
| :white_check_mark: `get_query_id_from_feed_id`    | :white_check_mark:  |                    |
| :white_check_mark: `get_reward_amount`            | :white_check_mark:  |                    |
| :white_check_mark: `get_reward_claimed_status`    | :white_check_mark:  |                    |
| :white_check_mark: `get_reward_claim_status_list` | :white_check_mark:  |                    |
| :white_check_mark: `get_tips_by_address`          | :white_check_mark:  |                    |

### Oracle (Tellor Flex)

| Dispatchable Function              |   Functional Test   | Notes                                                                                |
|------------------------------------|:-------------------:|--------------------------------------------------------------------------------------|
| :heavy_check_mark: `submit_value`  | :white_check_mark:  | Implemented apart from time-based rewards                                            |

| Runtime API                                                        |    Functional Test    | Notes |
|--------------------------------------------------------------------|:---------------------:|-------|
| :white_check_mark: `get_block_number_by_timestamp`                 |  :white_check_mark:   |       |
| :white_check_mark: `get_current_value`                             |  :white_check_mark:   |       |
| :white_check_mark: `get_data_before`                               |  :white_check_mark:   |       |
| :white_check_mark: `get_new_value_count_by_query_id`               |  :white_check_mark:   |       |
| ~~`get_pending_reward_by_staker`~~                                 |                       |       |
| ~~`get_real_staking_rewards_balance`~~                             |                       |       |
| :white_check_mark: `get_report_details`                            |  :white_check_mark:   |       |
| :white_check_mark: `get_reporter_by_timestamp`                     |  :white_check_mark:   |       |
| :white_check_mark: `get_reporter_last_timestamp`                   |  :white_check_mark:   |       |
| :white_check_mark: `get_reporting_lock`                            |  :white_check_mark:   |       |
| :white_check_mark: `get_reports_submitted_by_address`              |  :white_check_mark:   |       |
| :white_check_mark: `get_reports_submitted_by_address_and_query_id` |  :white_check_mark:   |       |
| :white_check_mark: `get_stake_amount`                              |  :white_check_mark:   |       |
| :white_check_mark: `get_staker_info`                               |  :white_check_mark:   |       |
| :white_check_mark: `get_time_of_last_new_value`                    |  :white_check_mark:   |       |
| :white_check_mark: `get_timestamp_by_query_id_and_index`           |  :white_check_mark:   |       |
| :white_check_mark: `get_index_for_data_before`                     |  :white_check_mark:   |       |
| :white_check_mark: `get_timestamp_index_by_timestamp`              |  :white_check_mark:   |       |
| :white_check_mark: `get_total_stake_amount`                        |  :white_check_mark:   |       |
| :white_check_mark: `get_total_stakers`                             |  :white_check_mark:   |       |
| :white_square_button: `get_total_time_based_rewards_balance`?      | :white_square_button: |       |
| :white_check_mark: `is_in_dispute`                                 |  :white_check_mark:   |       |
| :white_check_mark: `retrieve_data`                                 |  :white_check_mark:   |       |

### Governance

| Dispatchable Function              |   Functional Test   | Notes           |
|------------------------------------|:-------------------:|-----------------|
| :heavy_check_mark: `begin_dispute` | :white_check_mark:  | 98% implemented |
| :white_check_mark: `vote`          | :white_check_mark:  |                 |

| Runtime API                                     |   Functional Test   | Notes |
|-------------------------------------------------|:-------------------:|-------|
| :white_check_mark: `did_vote`                   | :white_check_mark:  |       |
| :white_check_mark: `get_dispute_fee`            | :white_check_mark:  |       |
| :white_check_mark: `get_disputes_by_reporter`   | :white_check_mark:  |       |
| :white_check_mark: `get_dispute_info`           | :white_check_mark:  |       |
| :white_check_mark: `get_open_disputes_on_id`    | :white_check_mark:  |       |
| :white_check_mark: `get_vote_count`             | :white_check_mark:  |       |
| :white_check_mark: `get_vote_info`              | :white_check_mark:  |       |
| :white_check_mark: `get_vote_rounds`            | :white_check_mark:  |       |
| :white_check_mark: `get_vote_tally_by_address`  | :white_check_mark:  |       |

## Controller Contract Integration

| Dispatchable Function                                |    Functional Test    | Notes                                                          |
|------------------------------------------------------|:---------------------:|----------------------------------------------------------------|
| :heavy_check_mark: `register`                        |  :white_check_mark:   | Partially implemented                                          |
| :heavy_check_mark: `report_stake_deposited`          |  :heavy_check_mark:   | Mostly implemented, `depositStake` functional test implemented |
| :heavy_check_mark: `report_staking_withdraw_request` |  :white_check_mark:   | 99% implemented                                                |
| :heavy_check_mark: `report_stake_withdrawal`         |  :white_check_mark:   |                                                                |
| :heavy_check_mark: `report_slash`                    |  :heavy_check_mark:   | 99% implemented                                                |
| :heavy_check_mark: `report_invalid_dispute`          | :white_square_button: |                                                                |
| :heavy_check_mark: `slash_dispute_initiator`         | :white_square_button: | Partially implemented, needs clarification on dispute fee      |
| :heavy_check_mark: `deregister`                      | :white_square_button: |                                                                |
