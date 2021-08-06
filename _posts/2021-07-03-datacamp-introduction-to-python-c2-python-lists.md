---
layout: post
title: "DataCamp - Introduction to Python"
subtitle: "Chapter 2 - Python Lists"
background: "/img/posts/datacamp-introduction-to-python/datacamp-bg.jpg"
---

# Chapter 2 - Python Lists

> Learn to store, access, and manipulate data in lists: the first step toward efficiently working with huge amounts of data.

---

### 2-1 Create a list

---

#### Exercise

Create a list
As opposed to `int`, `bool` etc., a list is a compound data type; you can group values together:

```python
a = "is"
b = "nice"
my_list = ["my", "list", a, b]
```

After measuring the height of your family, you decide to collect some information on the house you're living in. The areas of the different parts of your house are stored in separate variables for now, as shown in the script.

#### Instructions

- Create a list, areas, that contains the area of the hallway (hall), kitchen (kit), living room (liv), bedroom (bed) and bathroom (bath), in this order. Use the predefined variables.
- Print `areas` with the `print()` function.

```python
# area variables (in square meters)
hall = 11.25
kit = 18.0
liv = 20.0
bed = 10.75
bath = 9.50

# Create list areas
areas = [hall, kit, liv, bed, bath]

# Print areas
print(areas)

```

---

### 2-2 Create list with different types

---

#### Exercise

A list can contain any Python type. Although it's not really common, a list can also contain a mix of Python types including strings, floats, booleans, etc.

The printout of the previous exercise wasn't really satisfying. It's just a list of numbers representing the areas, but you can't tell which area corresponds to which part of your house.

The code in the editor is the start of a solution. For some of the areas, the name of the corresponding room is already placed in front. Pay attention here! "bathroom" is a string, while bath is a variable that represents the float 9.50 you specified earlier.

#### Instructions

- Finish the code that creates the `areas` list. Build the list so that the list first contains the name of each room as a string and then its area. In other words, add the strings "hallway", "kitchen" and "bedroom" at the appropriate locations.
- Print `areas` again; is the printout more informative this time?

```python
# area variables (in square meters)
hall = 11.25
kit = 18.0
liv = 20.0
bed = 10.75
bath = 9.50

# Adapt list areas
areas = ["hallway", hall, "kitchen", kit, "living room", liv, "bedroom", bed, "bathroom", bath]

# Print areas
print(areas)
```

---

### 2-3 Select the valid list

---

#### Exercise

A list can contain any Python type. But a list itself is also a Python type. That means that a list can also contain a list! Python is getting funkier by the minute, but fear not, just remember the list syntax:

```python
my_list = [el1, el2, el3]
```

A. `[1, 3, 4, 2]` B. `[[1, 2, 3], [4, 5, 7]]` C. `[1 + 2, "a" * 5, 3]`

#### Instructions

Possible Answers

- ✅ A, B and C
- 🔲 B
- 🔲 B and C
- 🔲 C

---

### 2-4 List of lists

---

#### Exercise

As a data scientist, you'll often be dealing with a lot of data, and it will make sense to group some of this data.

Instead of creating a flat list containing strings and floats, representing the names and areas of the rooms in your house, you can create a list of lists. The script in the editor can already give you an idea.

Don't get confused here: `"hallway"` is a string, while `hall` is a variable that represents the float `11.25` you specified earlier.

#### Instructions

- Finish the list of lists so that it also contains the bedroom and bathroom data. Make sure you enter these in order!
- Print out house; does this way of structuring your data make more sense?
- Print out the type of house. Are you still dealing with a list?

```python
# area variables (in square meters)
hall = 11.25
kit = 18.0
liv = 20.0
bed = 10.75
bath = 9.50

# house information as list of lists
house = [["hallway", hall],
         ["kitchen", kit],
         ["living room", liv], ["bedroom", bed], ["bathroom", bath]]

# Print out house
print(house)

# Print out the type of house
print(type(house))
```

---

### 2-5 Subset and conquer

---

#### Exercise

Subsetting Python lists is a piece of cake. Take the code sample below, which creates a list `x` and then selects "b" from it. Remember that this is the second element, so it has index 1. You can also use negative indexing.

```python
x = ["a", "b", "c", "d"]
x[1]
x[-3] # same result!
```

Remember the `areas` list from before, containing both strings and floats? Its definition is already in the script. Can you add the correct code to do some Python subsetting?

#### Instructions

- Print out the second element from the `areas` list (it has the value `11.25`).
- Subset and print out the last element of `areas`, being `9.50`. Using a negative index makes sense here!
- Select the number representing the area of the living room (`20.0`) and print it out.

```python
# Create the areas list
areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

# Print out second element from areas
print(areas[1])

# Print out last element from areas
print(areas[-1])

# Print out the area of the living room
print(areas[5])
```

---

### 2-6 Subset and conquer

---

#### Exercise

After you've extracted values from a list, you can use them to perform additional calculations. Take this example, where the second and fourth element of a list x are extracted. The strings that result are pasted together using the + operator:

```python
x = ["a", "b", "c", "d"]
print(x[1] + x[3])
```

#### Instructions

- Using a combination of list subsetting and variable assignment, create a new variable, `eat_sleep_area`, that contains the sum of the area of the kitchen and the area of the bedroom.
- Print the new variable `eat_sleep_area`.

```python
# Create the areas list
areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

# Sum of kitchen and bedroom area: eat_sleep_area
eat_sleep_area = areas[3]  + areas[7]

# Print the variable eat_sleep_area
print(eat_sleep_area)
```

---

### 2-7 Slicing and dicing

---

#### Exercise

Selecting single values from a list is just one part of the story. It's also possible to slice your list, which means selecting multiple elements from your list. Use the following syntax:

```python
my_list[start:end]
```

The `start` index will be included, while the `end` index is not.

The code sample below shows an example. A list with `"b"` and `"c"`, corresponding to indexes 1 and 2, are selected from a list `x`:

```python
x = ["a", "b", "c", "d"]
x[1:3]
```

The elements with index 1 and 2 are included, while the element with index 3 is not.

#### Instructions

- Use slicing to create a list, `downstairs`, that contains the first 6 elements of `areas`.
- Do a similar thing to create a new variable, `upstairs`, that contains the last 4 elements of `areas`.
- Print both `downstairs` and `upstairs` using `print()`.

```python
# Create the areas list
areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

# Use slicing to create downstairs
downstairs = areas[:6]

# Use slicing to create upstairs
upstairs = areas[6:]

# Print out downstairs and upstairs
print(downstairs)
print(upstairs)
```

---

### 2-8 Slicing and dicing (2)

---

#### Exercise

In the video, Hugo first discussed the syntax where you specify both where to begin and end the slice of your list:

```python
my_list[begin:end]
```

However, it's also possible not to specify these indexes. If you don't specify the `begin` index, Python figures out that you want to start your slice at the beginning of your list. If you don't specify the `end` index, the slice will go all the way to the last element of your list. To experiment with this, try the following commands in the IPython Shell:

```python
x = ["a", "b", "c", "d"]
x[:2]
x[2:]
x[:]
```

The elements with index 1 and 2 are included, while the element with index 3 is not.

#### Instructions

- Create `downstairs` again, as the first `6` elements of `areas`. This time, simplify the slicing by omitting the `begin` index.
- Create `upstairs` again, as the last `4` elements of `areas`. This time, simplify the slicing by omitting the `end` index.

```python
# Create the areas list
areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

# Alternative slicing to create downstairs
downstairs = areas[:6]

# Alternative slicing to create upstairs
upstairs = areas[6:]
```

---

### 2-9 Subsetting lists of lists

---

#### Exercise

You saw before that a Python list can contain practically anything; even other lists! To subset lists of lists, you can use the same technique as before: square brackets. Try out the commands in the following code sample in the IPython Shell:

```python
x = [["a", "b", "c"],
     ["d", "e", "f"],
     ["g", "h", "i"]]
x[2][0]
x[2][:2]
```

`x[2]` results in a list, that you can subset again by adding additional square brackets.

What will `house[-1][1]` return? `house`, the list of lists that you created before, is already defined for you in the workspace. You can experiment with it in the IPython Shell.

The elements with index 1 and 2 are included, while the element with index 3 is not.

#### Instructions

Possible Answers

- 🔲A float: the kitchen area
- 🔲A string: "kitchen"
- ✅ A float: the bathroom area
- 🔲 A string: "bathroom"

---

### 2-10 Replace list elements

---

#### Exercise

Replacing list elements is pretty easy. Simply subset the list and assign new values to the subset. You can select single elements or you can change entire list slices at once.

Use the IPython Shell to experiment with the commands below. Can you tell what's happening and why?

```python
x = ["a", "b", "c", "d"]
x[1] = "r"
x[2:] = ["s", "t"]
```

For this and the following exercises, you'll continue working on the `areas` list that contains the names and areas of different rooms in a house.

#### Instructions

- Update the area of the bathroom area to be 10.50 square meters instead of 9.50.
- Make the `areas` list more trendy! Change `"living room"` to `"chill zone"`.

```python
# Create the areas list
areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

# Correct the bathroom area
areas[-1] = 10.50

# Change "living room" to "chill zone"
areas[4] = "chill zone"
```

---

### 2-11 Extend a list

---

#### Exercise

If you can change elements in a list, you sure want to be able to add elements to it, right? You can use the + operator:

```python
x = ["a", "b", "c", "d"]
y = x + ["e", "f"]
```

You just won the lottery, awesome! You decide to build a poolhouse and a garage. Can you add the information to the `areas` list?

#### Instructions

- Use the `+` operator to paste the list `["poolhouse", 24.5]` to the end of the `areas` list. Store the resulting list as `areas_1`.
- Further extend `areas_1` by adding data on your garage. Add the string `"garage"` and float `15.45`. Name the resulting list `areas_2`.

```python
# Create the areas list and make some changes
areas = ["hallway", 11.25, "kitchen", 18.0, "chill zone", 20.0,
         "bedroom", 10.75, "bathroom", 10.50]

# Add poolhouse data to areas, new list is areas_1
areas_1 = areas + ["poolhouse", 24.5]

# Add garage data to areas_1, new list is areas_2
areas_2 = areas_1 + ["garage", 15.45]
```

---

### 2-12 Delete list elements

---

#### Exercise

Finally, you can also remove elements from your list. You can do this with the `del` statement:

```python
x = ["a", "b", "c", "d"]
del(x[1])
```

Pay attention here: as soon as you remove an element from a list, the indexes of the elements that come after the deleted element all change!

The updated and extended version of `areas` that you've built in the previous exercises is coded below. You can copy and paste this into the IPython Shell to play around with the result.

```python
areas = ["hallway", 11.25, "kitchen", 18.0,
        "chill zone", 20.0, "bedroom", 10.75,
         "bathroom", 10.50, "poolhouse", 24.5,
         "garage", 15.45]
```

There was a mistake! The amount you won with the lottery is not that big after all and it looks like the poolhouse isn't going to happen. You decide to remove the corresponding string and float from the `areas` list.

The `;` sign is used to place commands on the same line. The following two code chunks are equivalent:

```python
# Same line
command1; command2

# Separate lines
command1
command2
```

#### Instructions

Possible Answers

- 🔲 del(areas[10]); del(areas[11])
- 🔲 del(areas[10:11])
- ✅ del(areas[-4:-2])
- 🔲 del(areas[-3]); del(areas[-4])

---

### 2-13 Inner workings of lists

---

#### Exercise

At the end of the video, Hugo explained how Python lists work behind the scenes. In this exercise you'll get some hands-on experience with this.

The Python code in the script already creates a list with the name `areas` and a copy named `areas_copy`. Next, the first element in the `areas_copy` list is changed and the `areas` list is printed out. If you hit Run Code you'll see that, although you've changed `areas_copy`, the change also takes effect in the `areas` list. That's because areas and `areas_copy` point to the same list.

If you want to prevent changes in `areas_copy` from also taking effect in `areas`, you'll have to do a more explicit copy of the `areas` list. You can do this with `list()` or by using `[:]`.

#### Instructions

- Change the second command, that creates the variable `areas_copy`, such that `areas_copy` is an explicit copy of `areas`. After your edit, changes made to `areas_copy` shouldn't affect `areas`. Submit the answer to check this.

```python
# Create list areas
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Create areas_copy
areas_copy = list(areas)

# Change areas_copy
areas_copy[0] = 5.0

# Print areas
print(areas)
```
