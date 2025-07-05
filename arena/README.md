# Arena 🕹️
**Arena** is a Clarity smart contract enabling fractional ownership, governance, and prize distribution for professional esports teams. Fans can buy stakes in teams, vote on tournament strategies, and claim a proportional share of winnings based on their stake ownership.

## 🚀 Features

- **Team Registration**  
  League commissioners can register new teams with predefined stakes and captains.

- **Fan Participation**  
  Fans can buy fractional stakes in their favorite esports teams and earn rewards.

- **Tournament Governance**  
  Fans vote on proposed tournament strategies based on their stake weight.

- **Automated Prize Distribution**  
  Winnings are distributed proportionally to all fans who hold team stakes.

- **Secure Voting & Claims**  
  Fans can’t double vote or claim prizes multiple times per season.

---

## 🛠️ Functions

### 📦 Team Management

- `register-team` – Register a new team (admin only)
- `buy-stakes` – Fans buy stakes in a team

### 🏆 Tournament Interaction

- `create-tournament` – Fans propose a strategy for an upcoming tournament
- `vote-tournament` – Fans vote on the strategy proposal
- `distribute-prizes` – Team captains initiate prize distribution
- `claim-prizes` – Fans claim their share of tournament winnings

### 📚 Read-Only Queries

- `get-team` – Get team details
- `get-stake-balance` – Get fan's stake in a team
- `get-tournament` – View tournament proposal
- `calculate-prize-share` – View potential prize share for a fan

---

## 🔐 Roles & Permissions

- **League Commissioner**: The deploying account; can register teams.
- **Team Captain**: Controls prize distribution for the team.
- **Fans**: Buy stakes, propose/vote on strategies, and claim winnings.

---

## ❗ Error Codes

| Code   | Meaning                          |
|--------|----------------------------------|
| 600    | Unauthorized fan action          |
| 601    | Insufficient stake balance       |
| 602    | Team not found                   |
| 603    | Invalid amount supplied          |
| 604    | Tournament not found             |
| 605    | Already voted in tournament      |
