# MarketMake Aave Fluid Delegate

A depositor/sender is able to delegate fluidly (continuous | instant) to a borrower/receiver.

## Context

At a high level, I want to explore the possibility of building a **SuperApp** that enables a `depositor` to stream money to a `borrower`.

To make this happen, I have chosen to protocols:
**Superfluid** for its streaming money feature.
**Aave** for its credit delgation feature.

## Userflow
1. One depositor streaming money to One borrower
2. Many depositor(s) streaming money to One borrower
3. Many depositor(s) streaming money to Many borrower(s)

### Functions

After reviewing the documenation for Superfluid and Aave, I am at the understanding that the following functions will be required to construct.

#### Superfluid Continuous Flow Agreement (CFA)
- user()
- flow()
- createFlow()
- getNetFlow()
- deleteFlow()

#### Superfluid Instant Distribution Agreement (IDA)
- createPool()
- giveShares()
- distributeToPool()

#### Aave Credit Delegation (CD)
- approve Delegation()
- borrow()
- repay()
- borrowAllowance()

### Reference
[CFA](https://docs.superfluid.finance/superfluid/protocol-tutorials/create-a-superfluid-flow)

[IDA](https://docs.superfluid.finance/superfluid/protocol-tutorials/perform-an-instant-distribution)

[CD](https://docs.aave.com/developers/guides/credit-delegation)
