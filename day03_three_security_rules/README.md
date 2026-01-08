# 🔐 Day 03 — Three Security Rules

## 📖 Story

On the third day of coding, Mr. Frost is quite upset.
The reindeer authentication system was hacked because someone used
**“rednose”** as a password.

To prevent this from happening again, the cybersecurity team requires
each reindeer to submit **50 candidate passwords**.
Your task is to evaluate them and choose the **most secure password**
based on **three strict security rules**.

---

## 🎯 Objective

Given a list of passwords, determine the one with the **highest security score**.
If two passwords have the same score, the **earlier password in the file wins**.

---

## 🔐 Security Rules

1. **Base score** = length of the password
2. Password must contain:

   - at least one lowercase letter
   - at least one uppercase letter
   - at least one digit
   - at least one special symbol (`!@#$%^&*`)

   ❗ For each missing category, multiply the score by **0.75**

3. If **30% or more** of the password consists of the **same character**,
   subtract the number of occurrences of that character from the score

---

## 📥 Input Format

Dataset file:
Each line contains one password
(Total: 50 passwords)

---

## 📤 Output Format

---

## 🧠 Approach

- Iterate through each password in the dataset
- Calculate its score based on the three rules
- Track the password with the highest score
- Resolve ties by keeping the first occurrence

This solution uses:

- Regular expressions (`re`)
- Frequency analysis (`collections.Counter`)

---

## 🧾 Result

The program successfully evaluates all candidate passwords and selects
the most secure one based on the defined rules.

---

## 📂 File Structure

```text
day03_three_security_rules/
├── README.md
├── solution.py / solution.ipynb
└── ../datasets/day03/hyperskill-dataset-119011491.txt
```
