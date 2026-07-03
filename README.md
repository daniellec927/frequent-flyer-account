# Frequent Flyer Account (C++)

A C++ program modeling an airline frequent-flyer rewards account. Flights add
mileage to an account; once enough miles accrue, the account can redeem a free
flight, which deducts the miles.

## Classes
- **PlaneFlight** (`FFA_PlaneFlight.h` / `.cpp`) — a single flight: passenger
  name, from/to cities, cost, and mileage, with getters.
- **FrequentFlyerAccount** (`FFA_FrequentFlyerAccount.h` / `.cpp`) — an account
  tied to a passenger: tracks a mile balance, adds flights (only when the
  passenger name matches), checks eligibility for a free flight, and redeems one.
- `FFA_main.cpp` — assertion-based test driver.

## Build & Run
```bash
g++ -std=c++17 FFA_main.cpp FFA_PlaneFlight.cpp FFA_FrequentFlyerAccount.cpp -o ffa
./ffa
```

## Also included: online payment (separate program)
`FFA_onlinepayment.cpp` is a separate, self-contained exercise — a simple
`payment` class (payer, payee, amount) with its own `main`. Build it on its own:
```bash
g++ -std=c++17 FFA_onlinepayment.cpp -o payment
./payment
```
