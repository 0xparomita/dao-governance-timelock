# DAO Governance Timelock

A robust, modular framework for decentralized autonomous organizations. This repository provides the essential smart contracts to implement on-chain voting and secure treasury management.

## Components
* **GovernanceToken**: An ERC-20 token with built-in snapshot and delegation capabilities.
* **GovernorContract**: Manages the lifecycle of a proposal (Proposing, Voting, Succeeded, Queued, Executed).
* **TimelockController**: Acts as a safety buffer, delaying the execution of passed proposals to allow stakeholders to exit if they disagree with the outcome.

## Governance Parameters
* **Voting Delay**: The delay between a proposal being created and voting starting (usually 1 block).
* **Voting Period**: Duration for which the voting remains open.
* **Proposal Threshold**: Minimum tokens required to create a proposal.
* **Quorum**: Minimum percentage of total supply required for a vote to be valid.

## Setup
1. Deploy the Governance Token.
2. Deploy the Timelock with a specified delay (e.g., 2 days).
3. Deploy the Governor contract, linking it to the Token and Timelock.
4. Transfer ownership of the Timelock (and treasury) to the Governor contract.
