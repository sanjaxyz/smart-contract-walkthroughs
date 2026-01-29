# ERC-20 Walkthrough (OpenZeppelin Reference)

This document provides a high-level walkthrough of the OpenZeppelin ERC-20 reference implementation.
OpenZeppelin’s ERC-20 contract is widely used as a base for fungible tokens on Ethereum.

The goal of this walkthrough is to explain the structure and behavior of the contract, not to analyze security or performance.

## Overview
The ERC-20 contract manages balances, token transfers, and allowances.
It follows the ERC-20 interface defined in the Ethereum Improvement Proposal.

## State Tracking
The contract maintains internal records of:
- Token balances for each address
- Allowances that permit one address to spend tokens on behalf of another

These records are updated whenever tokens are transferred or allowances are changed.

## Token Supply
The total token supply represents the number of tokens in existence.
Changes to the total supply typically occur during token creation or destruction.

## Transfers
Token transfers move balances from one address to another.
Transfers require that the sender has a sufficient balance before the state is updated.

## Allowances
Allowances enable delegated token spending.
An address can approve another address to transfer tokens up to a specified amount.

## Events
The contract emits events when transfers and approvals occur.
These events allow external applications to track token activity.
