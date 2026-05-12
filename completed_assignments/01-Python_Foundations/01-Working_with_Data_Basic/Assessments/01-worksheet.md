# 📝 Worksheet: 02 - Working with Data

Use this worksheet to review and reinforce your understanding of Python data containers.

---

## 🧠 Section 1: Lists

1. What method adds an item to the end of a list?  
   `Answer:` append

2. How can you remove an item from a list by value?  
   `Answer:` remove

3. What’s the result of this code?

```python
nums = [2, 4, 6]
nums.append(8)
print(nums)
```

   `Answer:` 2 4 6 8

---

### ✏️ Task: List Practice

```python
# Create a list of your top 3 favorite foods.
# Add another food to the list.
# Remove one item and print the list.
```
foods = ["pizza", "popcorn", "pasta"]
foods.append("porkchop")
foods.remove("popcorn")
print(foods)
---

## 🔒 Section 2: Tuples

4. What is a key difference between a list and a tuple?  
   `Answer:` tuples cannot be changed after creation

5. Can you change the contents of a tuple once it is created? Why or why not?  
   `Answer:` No, the immuntability of a tuple makes it a safer and more constant place to store info. It also allows it to be hashable and thus much quicker to access than a list.

---

### ✏️ Task: Tuple Practice

```python
# Create a tuple with your favorite 3 numbers.
# Unpack it into three variables and print each.
```
nums = (1,4,7)
x,y,z = nums
print('X:', x)
print('Y:', y)
print('Z:', z)
---

## 🔑 Section 3: Dictionaries

6. What does the `.get()` method do differently from accessing a key directly?  
   `Answer:` 

7. How do you loop through both keys and values in a dictionary?  
   `Answer:` ____________________________

---

### ✏️ Task: Dictionary Practice

```python
# Create a dictionary with keys: 'name', 'age', and 'hobby'.
# Print each key and value in the format "key: value".
```

---

## 🧾 Submit Checklist

- [ ] I practiced creating and modifying lists.
- [ ] I understand how tuples are different from lists.
- [ ] I accessed and looped through dictionary items.
