# Collateralized Loan Smart Contract

## Overview
This Solidity smart contract facilitates a collateralized loan system where a lender provides a loan to a borrower against collateral. The contract ensures repayment with interest and enables the lender to claim collateral in case of default.

## Features
- **Set Loan Details**: Lender defines loan amount, collateral, interest rate, and due date.
- **Collateral Deposit**: Borrower deposits collateral before withdrawing the loan.
- **Loan Withdrawal**: Borrower withdraws the loan amount after depositing collateral.
- **Repayment with Interest**: Borrower repays the loan plus interest before the due date.
- **Collateral Claim**: If repayment is not made before the due date, the lender can claim the collateral.

## Smart Contract Functions
### `setLoanDetails`
- Initializes loan details such as loan amount, collateral, interest rate, and due date.
- Can only be set once by the lender.

### `depositCollateral`
- Allows the borrower to deposit collateral equivalent to the required amount.
- Ensures only the borrower can deposit.

### `withdrawLoan`
- Enables the borrower to withdraw the loan amount after depositing collateral.

### `repayLoan`
- Allows the borrower to repay the loan along with interest before the due date.
- Refunds the collateral upon successful repayment.

### `claimCollateral`
- Allows the lender to claim the collateral if the borrower fails to repay by the due date.

## Deployment Instructions
1. Deploy the contract on an Ethereum-compatible blockchain.
2. The lender initializes the loan using `setLoanDetails`.
3. The borrower deposits collateral via `depositCollateral`.
4. The borrower withdraws the loan using `withdrawLoan`.
5. The borrower repays the loan via `repayLoan` before the due date.
6. If the loan is not repaid, the lender can call `claimCollateral` to seize the collateral.

## License
This project is licensed under the MIT License.
