# Assignment-Module-20

## Purpose

This project creates a joint savings account using a smart contract and the Ethereum blockchain. A user is able to deposit and withdraw ether into the smart contract. Withdrawal is possible to two authorized addresses.

## Process

- In the joint_savings contract two payable addresses were defined : accountOne, accountTwo.
- a variable for a public address that will hold the last to withdraw address.
- a public uint holding the last to withdraw amount.
- a public uint holding the balance for the contract.

---

- a withdraw function was defined with parameters for the amount to withdraw and the address to withdraw to.
- within the function, two require statements:
  - the first, requiring the recipient address for the withdrawal be either accountOne or accounTwo
  - the amount withdrawn be less or equal to the account balance
- the lastToWithdraw address is also set to the recipient address
- the lastWithdrawAmount is set to amount
- the contractBalance is updated

---

### deposit()

- a public payable deposit function is created
- the contract balance is updated upon a deposit transaction

---

### setAccounts()

- a setAccounts function is created allowing for the setting of which two addresses funds can be withdrawn to

---

### fallback function()

- a fallback deposit function of external payable is created

---

## Results

The contract was deployed successfully:

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/deployed_contract.JPG)

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/deployed_contract_log.JPG)

---

Using the setAccounts function, the authorized ethereum addresses were set:

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/setAccounts_function.JPG)

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/setAccounts_function_log.JPG)

---

The deposit functionality of the contract was tested:

Transaction 1:

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/transaction_1.JPG)

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/transaction_1_log.JPG)

Transaction 2:

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/transaction_2.JPG)

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/transaction_2_log.JPG)

Transaction 3:

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/transaction_3.JPG)

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/transaction_3_log.JPG)

---

The contracts withdrawal function was tested:

Withdrawal 1:

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/withdrawal_1.JPG)

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/withdrawal_1_log.JPG)

Withdrawal 2:

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/withdrawal_2.JPG)

![](https://github.com/malrepos/Assignment-Module-20/blob/main/Execution_Results/withdrawal_2_log.JPG)

## Instructions

- Copy and paste, or upload the code to the remix IDE https://remix-project.org/.

- Compile and deploy the contract.
