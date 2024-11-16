flowchart LR
    %% Define nodes with IDs for styling
    subgraph Bitcoin_System[System Dynamics of Bitcoin]
A[Belief in Bitcoin's Value]
B[Limited Supply of Bitcoin]
C[Scarcity of Bitcoin]
D[Increased Demand for Bitcoin]
E[Rising Bitcoin Prices]
F[Early Adopters and Holders]
G[Promotion and Evangelism]
H[Media and Influencer Attention]
I[Adoption by Influential Figures]
J[Legitimacy and Wider Acceptance]
K[Network Effect Strengthens]
L[Bitcoin Halving Events]
M[Loss of Bitcoin Lost Keys]
end

    %% Define relationships
A-- >| Increases | D
D-- >| Leads to | E
E-- >| Benefits | F
F-- >| Promote to Gain More | G
G-- >| Spreads | A
E-- >| Attracts | H
H-- >| Amplifies | A
I-- >| Endorse | J
J-- >| Boosts | A
B-- >| Contributes to | C
C-- >| Drives | D
L-- >| Reduces Supply | B
M-- >| Decreases | B
K-- >| Enhances | D
D-- >| Expands | K

    %% Reinforcing Loop Labels
E-- >| Reinforcing Loop | F
D-- >| Network Effect Loop | K

    %% Comparison to Religion
    subgraph Religion_System[Comparison to Religion]
R1[Religious Belief]
R2[Religious Practices]
R3[Evangelism]
R4[Growth of Followers]
R5[Religious Authority Endorsement]
R6[Legitimacy of Religion]
end

    %% Relationships in Religion
R1-- >| Leads to | R4
R4-- >| Expands | R1
R1-- >| Encourages | R3
R3-- >| Spreads | R1
R5-- >| Supports | R6
R6-- >| Strengthens | R1

    %% Difference Highlight
B -.->| Less Built -in Growth Loops | R2
L -.->| Halving and Scarcity Mechanics | R2
K -.->| Stronger Network Effects | R4

    %% Styles for Nodes
    classDef bitcoin fill: #E6F7FF, stroke:#333, stroke - width: 2px, color:#000
    classDef religion fill: #FFF0F0, stroke:#333, stroke - width: 2px, color:#000

    %% Assign Classes to Nodes
class A, B, C, D, E, F, G, H, I, J, K, L, M bitcoin
class R1, R2, R3, R4, R5, R6 religion