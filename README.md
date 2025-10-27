# shell_script

---
### Review: Key Shell Scripting Points
echo: --outputs text.

read: --grabs user input and stores it.

if/else/elif: --tests conditions and runs code based on them.

for: --repeats actions for each item in a list or set.

---
1. Starting a Script (Shebang)
Shebang tells the computer which shell to use. Add this at the very top of your script:

bash
```
#!/bin/bash
Why? It ensures your script uses Bash for command interpretation.​
```
---

2. Printing Text: echo
echo outputs (prints) text to the terminal.

bash
```
echo "Hello, world!"
```
What happens:

When you run this script, it prints: Hello, world!

Now you try: What do you think happens if you run echo "My first shell script."?

---

3. Reading User Input: read
read takes input from the user and stores it in a variable.

bash
```
read name
echo "Hello, $name"
```
What happens:

Script waits for you to type something. If you type Amit, it prints: Hello, Amit.

Quick check: In this script, what does $name represent?

---

4. Conditional Statements: if, else, elif
These control script decisions. Here's a simple test for numbers:

bash
```
read num
if [ "$num" -gt 10 ]; then
    echo "Number is greater than 10"
elif [ "$num" -eq 10 ]; then
    echo "Number is exactly 10"
else
    echo "Number is less than 10"
fi
```
What happens:

After you enter a number, the script tells if the number is greater than, equal to, or less than 10.

Can you explain what happens if you enter 10?

---

5. Loops: Repeating Actions (for loop)
for loop let you create directories

bash
```
for ((i=1;i<=5;i++))
do
    mkdir "dir$i"
done
```
script create the dir1,...dir5

---

for loops let you process lists. Example printing fruit names:

bash
```
fruits=("apple" "banana" "cherry")
for fruit in "${fruits[@]}"; do
    echo "Current fruit: $fruit"
done
```
What happens:

Script prints each fruit, one per line:

Current fruit: apple

Current fruit: banana

Current fruit: cherry



