# ☕ Day 02 — Two Pointers

## 📖 Story

On the second day of coding, Mr. Frost arrives carrying two containers labeled **“COCOA”**.

None of the available cocoa varieties match the exact sweetness level preferred by the team.
Mr. Frost asks you to mix **two cocoa varieties** so that their **average sweetness** is as close
as possible to the desired target.

---

## 🎯 Objective

Determine the **average sweetness level** of two cocoa varieties that is closest to the target value.

📌 If the result is a decimal number, **round it up** to the nearest integer.

---

## 📥 Input Format

Dataset file:

```
Line 1: Target sweetness value (integer)
Line 2: Comma-separated sweetness levels (sorted)
```

---

## 📤 Output Format

```
An integer representing the rounded-up average sweetness.
```

---

## 🧠 Approach

This problem is solved using the **Two Pointers** technique:

- Use two indices from both ends of the sorted list
- Calculate the average of the two values
- Move pointers based on comparison with the target
- Track the closest average found

Time Complexity: **O(n)**  
Space Complexity: **O(1)**

---

## 🧪 Implementation

```python
def find_closest_cocoa_mix(target, sweetness_levels):
    left = 0
    right = len(sweetness_levels) - 1

    closest_avg = None
    min_diff = float('inf')

    while left < right:
        current_avg = (sweetness_levels[left] + sweetness_levels[right]) / 2
        diff = abs(current_avg - target)

        if diff < min_diff:
            min_diff = diff
            closest_avg = current_avg

        if current_avg < target:
            left += 1
        elif current_avg > target:
            right -= 1
        else:
            return math.ceil(current_avg)

    return math.ceil(closest_avg)
```

---

## 🧾 Result

The program successfully finds the cocoa mix whose average sweetness is
closest to the target value and outputs the rounded-up result.

---

## 📂 File Structure

```text
day02_two_pointers/
├── README.md
├── solution.py / solution.ipynb
└── ../datasets/day02/hyperskill-dataset-118984318.txt
```

---

## 🚀 Status

✅ Day 02 completed
