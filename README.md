# Bank Account

A simple Java console program that manages a bank account. It reads the account data and performs a withdrawal, showing the new balance after the operation.

## How it works

1. The user enters the account data: **number**, **holder**, **initial balance** and **withdraw limit**.
2. The user enters the **amount to withdraw**.
3. The program performs the withdrawal and displays the new balance.

### Validation rules

A withdrawal is **rejected** if:
- The amount exceeds the account's **withdraw limit**.
- There isn't **enough balance** in the account to cover the withdrawal.

If any rule is violated, the program shows an error message instead of performing the withdrawal.

## Class diagram

```
Account
-----------------------------------
- number       : Integer
- holder       : String
- balance      : Double
- withdrawLimit: Double
-----------------------------------
+ deposit(amount : Double) : void
+ withdraw(amount : Double) : void
```

## Examples

**Successful withdrawal**

```
Enter account data
Number: 8021
Holder: Bob Brown
Initial balance: 500.00
Withdraw limit: 300.00

Enter amount for withdraw: 100.00
New balance: 400.00
```

**Amount exceeds withdraw limit**

```
Enter account data
Number: 8021
Holder: Bob Brown
Initial balance: 500.00
Withdraw limit: 300.00

Enter amount for withdraw: 400.00
Withdraw error: The amount exceeds withdraw limit
```

**Not enough balance**

```
Enter account data
Number: 8021
Holder: Bob Brown
Initial balance: 200.00
Withdraw limit: 300.00

Enter amount for withdraw: 250.00
Withdraw error: Not enough balance
```

## How to run

```bash
javac Main.java
java Main
```

## Technologies

- Java
