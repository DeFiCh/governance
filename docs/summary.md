# Governance Summary

## Evolution

- Genesis: 
  - Critical operations: Foundation keys (eg: DAT creation and minting)
  - DFIP, CFP: GitHub
- Bayfront: DEX and Liquidity pools.
  - Critical operations: Foundation keys (eg: Past + DEX, pool)
  - DFIP, CFP: GitHub
- Fort Canning+: Oracles, Vaults, Loans + economy with operations.
  - Highlight: Introduction of on-chain attributes to handle parameters on-chain.
  - Critical operations: Foundation keys (eg: Past + Loan, vaults, Oracles appoints)
  - DFIP, CFP: GitHub
- Grand Central Upgrade:
  - Critical operations: Foundation keys
  - DFIP, CFP: On-chain
- DF24: 
  - Highlight: Phase-out foundation, first blocks to de-centralize governance.
  - Critical operations: 
    - Collaboration: GitHub
    - Execution: Governance SIG
  - DFIP, CFP: On-chain
- Later:
  - Highlight: Phase-out execution SIG.
  - Required feature: Extend `AuthManager` to SIGs. 


## Governance - High-level details

- General governance continues to be through on-chain voting. 
- The centralized part of governance that's been entrusted to a few to operate so far is now being phased out.
- The existing foundation rights are being downsized.
  - The old system continues to remain in handi-capped mode, but start to unused only as emergency fallback after upgrade.
  - To be eventually be removed once the new governance stable and mature.
- Governance is broken up into several Special Interest Groups (SIGs). 
- First set of governance is being bootstrapped by the core team to accelerate the process. 
  - Each SIG creation, removal, etc goes through DFIP there-after.
  - Each SIG shall have it's own system of governance on how to appoint / rotate / remove members.
  - All SIGs co-ordinate the final execution transparently in the GitHub repo dedicated for governance (until SIG specific auth is available on-chain). 
- Any changes that utilizes the governance SIGs must always be executed only after being acknowledged on GitHub. 
- Each SIG will maintain it's own directory on the GitHub repo on it's key operations with one dedicated file with the rules of execution for Execution SIG.

### Key Special Interest Groups

- Execution SIG (Taking over from past Foundation)
- Node SIG
- Token Economy SIG
- Oracle SIG
- Explorer Infra SIG
- Wallet / Ecosystem SIG


### Basic How To

- Create an issue on governance repo that's addressed to a specific SIG with the exact commands to be executed.
- SIG members now provide their ACK / NACK through GitHub comments.
- When each SIG has reached consensus (through it's own governance on M/N ACK required), one of the SIG members will tag the issue to be executed by a member of the Execution SIG.
- An Execution SIG member to verify the rules of confirmation proposed by the SIG and if consensus has reached, is now ready to execute it.
- Execution SIG Member Actions:
  - Validate.
  - Execute.
  - Document the execution and TX in the issue.
  - Close issue on completion, re-assign to SIG otherwise.
 
