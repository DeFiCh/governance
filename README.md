# Governance
The overarching governance channel for all current and future sub-groups/special interest groups (SIGs)

## Overall Summary
As DeFiChain is preparing to move to the next era of decentralization with governance powered by the community, the goal moving forward is to grant extra executive authority and power to execute commands that alters the chain parameters and other governance-related variables.

## General Structure of Governance

### Governance Execution SIG
The role of the Execution SIG is to take on the responsibility of executing commands on behalf of the other SIGs. This SIG does not have any powers on deciding the chain parameters and is merely an executor

#### Token Economy SIG
Determines which tokens are allowed as Decentralized Asset Tokens (DAT) and which should be deprecated. This SIG also manages DEX prices, vaults, and related components

#### Oracle SIG
Responsible for timely updates and price feed availability for current and future DATs, ensuring that the price does not deviate significantly from the expected range.

#### Explorer SIG
Oversees tools like Blockscout and Defiscan. Its operations are entirely self-contained and do not require on-chain decisions.

#### Wallet SIG
Manages the Light Wallet app, its publishing, and maintenance. It also oversees the desktop wallet, which is optional and in maintenance mode.

## SIG Operations
How SIGs Will Operate
The operational structure of Special Interest Groups (SIGs) within DeFiChain introduces a clear separation between decision-making and execution.
While SIGs are empowered to make crucial decisions within their designated areas, they do not have the authority to execute those decisions on-chain.
Instead, execution powers are reserved for Governance members, a group within DeFiChain's hierarchy responsible solely for implementing decisions, without having influence over the content of those decisions.

Each SIG operates independently, deciding its internal structure.
Whether a SIG chooses to have a lead or not, or how it manages appointments and resignations, is entirely up to the group. These decisions are not dictated by higher authorities in DeFiChain but rather determined within each SIG’s governance.

## Common Rules for SIGs
One of the key procedural elements for all SIGs is the concept of quorum— the number of participants required to validate decisions. Collectively, SIGs will define a universal policy outlining what constitutes quorum (M out of N members), ensuring consistency across the ecosystem.
Once quorum is reached, the SIG can tag an issue for execution by a Governance member on GitHub.
At this point, the Governance member’s role is purely administrative; they execute the decision without influencing or questioning the outcome.

For more: 

- [Summary](./docs/summary.md)
- [Areas of Impact](./docs/areas-of-impact.md)