# 2114. Maximum Number of Words Found in Sentences

**Difficulty:** Easy  
**Topics:** Array, String  
**Link:** [LeetCode Problem 2114](https://leetcode.com/problems/maximum-number-of-words-found-in-sentences/)

---

## 📝 Problem Description
Given an array of strings `sentences`, where each `sentences[i]` represents a single sentence with words separated by a single space, return *the maximum number of words that appear in a single sentence*.

---

## 💡 Examples
* **Example 1:**
  * **Input:** `sentences = ["alice and bob love leetcode", "i think so too", "this is great thanks very much"]`
  * **Output:** `6` (*Third sentence has 6 words*)
* **Example 2:**
  * **Input:** `sentences = ["please wait", "continue to fight", "continue to win"]`
  * **Output:** `3`

---

## 🔒 Constraints
* `1 <= sentences.length <= 100`
* `1 <= sentences[i].length <= 100`
* `sentences[i]` consists only of lowercase English letters and `' '`, with no leading or trailing spaces.

---

## 🚀 Approach & Intuition
Since words are separated by single spaces, the number of words in a sentence is equal to \((\text{number of spaces} + 1)\). We can iterate through each sentence, count the spaces, and track the maximum value.

* **Time Complexity:** \(\mathcal{O}(N \times M)\), where \(N\) is the number of sentences and \(M\) is the maximum length of a sentence.
* **Space Complexity:** \(\mathcal{O}(1)\) auxiliary space.

---

## 💻 Solutions

### Python
```python
class Solution:
    def mostWordsFound(self, sentences: list[str]) -> int:
        return max(sentence.count(' ') + 1 for sentence in sentences)
```

