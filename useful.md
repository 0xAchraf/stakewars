## Useful Commands

1. Check Proposal List

  - Check all proposals

    ```bash
    near proposals
    ```
    
  - Check specifically proposal

    `xx` change with wallet name
    
    ```bash
    near proposals | grep xx.factory.shardnet.near
    ```
    
2. Check active validators

  - Check all active validators
        
    ```bash
    near validators current
    ```
 - Check specifically active validator

    `xx` change with wallet name
    
    ```bash
    near validators current | grep xx.factory.shardnet.near
    ```
    
3. Check the next Validators

    This command is useful for viewing a list of validators who will become active in the next epoch, and if the proposal has been approved it will be displayed in the next epoch after the previous epoch has been completed
    
    ```bash
    near validators next
    ```
    
    - We can also check the next validator specifically with this command
    
      ```bash
      near validators next | grep xx.factory.shardnet.near
    
4. Change Comission
    
   ```bash
    near call xx.factory.shardnet.near update_reward_fee_fraction '{"reward_fee_fraction": {"numerator": 3, "denominator": 100}}' --accountId xx.shardnet.near --gas=300000000000000
    ```

    Change `numerator` parameter as you want. The command above is to change the commission to 3%, if you want to change it to 5% then you change the `numerator` parameter to be 5

5. Deposit and Stake NEAR

    ```bash
    near call xx.factory.shardnet.near deposit_and_stake --amount your_NEAR --accountId xx.shardnet.near --gas=300000000000000
    ```

    Change `your_NEAR` with the amount of NEAR you want to deposit ( For example: `--amount 10` )


6. How to Unstake

   ```bash
   near call xx.factory.shardnet.near unstake '{"amount": "amount_of_yoctoNEAR"}' --accountId xx.shardnet.near --gas=300000000000000
   ```

   `amount_of_yoctoNEAR` change with amount that you want to unstake in yoctoNEAR ( For example: ``{"amount: "100000000000000000"} ``)

   NB: 1 NEAR = 1000000000000000000000000 yoctoNEAR

   - For Unstake all your NEAR, run this command:

     ```bash
     near call xx.factory.shardnet.near unstake_all --accountId xx.shardnet.near --gas=300000000000000
     ```

7. Withdraw

   Unstaking will take 2 - 3 epoch until it can be withdrawn to the wallet

   ```bash
   near call xx.factory.shardnet.near withdraw '{"amount": "amount_of_yoctoNEAR"}' --accountId xx.shardnet.near --gas=300000000000000
   ```

   - Run this command for withdaw all NEAR:

     ```bash
     near call xx.factory.shardnet.near withdraw_all --accountId xx.shardnet.near --gas=30000000000000    ```
     ```

8. Ping

   Command:

   ```bash
   near call xx.factory.shardnet.near ping '{}' --accountId xx.shardnet.near --gas=300000000000000
   ```

9. Balances Total Balance Command :

   ```bash
   near view xx.factory.shardnet.near get_account_total_balance '{"account_id": "xx.shardnet.near"}'
   ```

10. Staked Balance

    Command:

    ```bash
    near view xx.factory.shardnet.near get_account_staked_balance '{"account_id": "xx.shardnet.near"}'
    ```

11. Unstaked Balance

    Command:

    ```bash
    near view xx.factory.shardnet.near get_account_unstaked_balance '{"account_id": "xx.shardnet.near"}'
    ```

12. Available for Withdrawal

    You only can withdraw your NEAR if the token is unlocked

    Command:

    ```bash
    near view xx.factory.shardnet.near is_account_unstaked_balance_available '{"account_id": "xx.shardnet.near"}'
    ```

13. Pause / Resume Staking

    - Pause
      Command:

      ```bash
       near call xx.factory.shardnet.near pause_staking '{}' --accountId xx.shardnet.near
      ```

    - Resume

      Command:

      ```bash
      near call xx.factory.shardnet.near resume_staking '{}' --accountId xx.shardnet.near
      ```
