# 🐞 Day 1 — A Nasty Bug in a Production Tree

## 📖 Story

On the first day of coding, Mr. Frost asks you to investigate production logs.
One error occurs constantly (background noise), but during **15:00–15:30**
another error spikes and must be identified.

## 🎯 Objective

Find the most common error during the incident window (15:00–15:30),
excluding the error that is most frequent throughout the entire day.

## 📥 Input

Log file with entries:

```
HH:MM ErrorName
```

## 📤 Output

Name of the incident-specific error.

## 🧠 Approach

- Parse logs using `split`
- Filter by time window using `startswith`
- Count frequencies using `collections.Counter`
- Exclude background noise

## ▶️ Run

Open the notebook:
`day01_a_nasty_bug_in_a_production_tree.ipynb`

## 🧾 Result

After analyzing the log file and excluding the background noise error, the following results were obtained:

- **Background noise error:** `SnowballOverflowError`
- **Incident-specific error:** `ChimneyBlockedException`
- **Number of occurrences during incident window (15:00–15:30):** `12`

This confirms that `ChimneyBlockedException` was the error that spiked during the incident
and was hidden beneath the usual background noise in the system logs.
