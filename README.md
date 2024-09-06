# Governance
The overarching governance channel for all current and future sub-groups/special interest groups

## Overall Summary
As DeFiChain is preparing to move to the next era of decentralization with governance powered by the community, the goal moving forward is to grant extra executive authority and power to execute commands that alters the chain parameters and other governance-related variables.



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
Minting of tokens (Manual process from vault by Finance Team)
Adding of Initial Pool Liquidity (DUSD price taken as 0.31 as its dStocks-DUSD)
Validation of pool.



