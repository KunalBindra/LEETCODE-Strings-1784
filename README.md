# LEETCODE-Strings-1784
### Idea of the Code

The function checks whether the string has **only one continuous segment of '1's**.

If `"01"` appears, it means:

* A **0 appears after 1**, and later **1 appears again** → meaning **multiple segments of 1s**.

So the code simply checks:

```
Does the string contain "01" ?
```

* If **YES → return false**
* If **NO → return true**

---

# Dry Run for `s = "110"`

### Step 1

`s = "110"`

### Step 2

Check:

```
s.contains("01")
```

Look for `"01"` inside `"110"`.

Check substrings:

| Position | Substring |
| -------- | --------- |
| 0-1      | "11"      |
| 1-2      | "10"      |

We **do not find "01"**.

So:

```
s.contains("01") = false
```

---

### Step 3

The function returns:

```
!false
```

which becomes

```
true
```

---

# Final Output

```
true
```

### Why?

The **1s appear in only one segment**:

```
110
^^
```

After `0`, **no more 1s appear**, so the condition is satisfied.

---

✅ **Rule to remember**

| String | Contains "01"? | Result |
| ------ | -------------- | ------ |
| 111000 | ❌              | true   |
| 110    | ❌              | true   |
| 101    | ✅              | false  |
| 110011 | ✅              | false  |

---
