# vault-door-training
- **picoGym - picoCTF 2019**
- **Category: Reverse Engineering**
- **Points: 50**

## Challenge Description
Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility. The source code for the training vault is here: [VaultDoorTraining.java](https://jupiter.challenges.picoctf.org/static/1afdf83322ee9c0040f8e3a3c047e18b/VaultDoorTraining.java)

## Solution Steps
I downloaded the file to see what was in it, and opened it up. It's java source code, and reading through it, it appears to take in a password, and then tell the user "Access granted." or "Access denied!". The password is written as part of the checkPassword method, and is the content of the flag.
