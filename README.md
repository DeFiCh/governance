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







## Areas of Impact
The new governance key has the capability to modify these core areas.

DEX Swap Fees (Commissions)

Process
DEX Swap Fees should ONLY be modified based on DFIPs passed by governance voting round.
After the governance round is cleared and DFIP has passed, evaluate the proposal with the core team and select an appropriate blockheight to target implementation of swap fees update.
Perform setgovheight to change commission if needed.


## Liquidity Pool (LM) Rewards 
Reallocation of LM Rewards based on Ticker_DecentralizedLoans (LM setgov)
and community sheet. List dAssets.xlsx

Sample Command

``` defi-cli setgovheight '{ "LP_LOAN_TOKEN_SPLITS": {"123":0.2,"17":0.05,"102":0.1,"101":0.1,"218":0.05,"114":0.0324,"104":0.0482,"33":0.01518,"100":0.01374,"36":0.01708,"35":0.03468,"90":0.01499,"55":0.0286,"56":0.02484,"61":0.00991,"62":0.00883,"64":0.00922,"71":0.03206,"38":0.01715,"44":0.00313,"53":0.00977,"39":0.01372,"42":0.01274,"40":0.00471,"43":0.00591,"46":0.01309,"45":0.01138,"215":0.01917,"256":0.01251,"276":0.02471,"260":0.02607,"263":0.01816,"265":0.01805}}' 4225921 ```

## DEX “Stabilization” Fees
Sample Command

``` defi-cli setgovheight '{ "ATTRIBUTES": { "v0/poolpairs/17/token_a_fee_pct": "0.8" , "v0/poolpairs/101/token_b_fee_pct": "0.0223" , "v0/poolpairs/102/token_b_fee_pct": "0.0223" , "v0/poolpairs/218/token_b_fee_pct": "0.0223" , "v0/poolpairs/236/token_b_fee_pct": "0.0223" , "v0/token/15/loan_minting_interest": "-11.41" }}' 4191270 ```

Addition of new tokens and setting up of new liquidity pools 
This will be based on the DFIP proposal. For example, to add IBIT, MARA, HOOD, MU, ASML, SMCI into DeFiChain DEX,

Steps to undertake:
Commands for execution on chain: https://github.com/DeFiCh/team/issues/123 
Creation of token & setting it as loan token
Creation of pool pairs
Minting of tokens (Manual process from vault)
Adding of Initial Pool Liquidity (DUSD price taken as 0.31 as its dStocks-DUSD)
Validation of pool.



