## Input

Python allows you to take input directly from the user using the `input` function. Let's use it to improve our weather application by asking for the weather before displaying the output.

```
weather = input("What is the weather like today? ")

if weather == "sunny":
    print("Bring your shades")
elif weather == "rainy":
    print("Bring your umbrella")
elif weather == "snowy":
    print("Bring your wooly muffler")
else:
    print("I don't know what you should bring! I'm just a little program...")
```

When you run this program, Python should ask you for some input with the prompt `What is the weather like today?` (The space before the second `"` makes the prompt look more tidy in the console.) It will then return some advice based on the input.

### Asking repeatedly

What if we want Python to keep asking for input instead of exiting after the first question is answered? For that, we can use somethign called a while loop.

Remember our for loop? Instead of iterating through a list like the for loop, our while loop will continue to execute as long as a certain condition is true. Here's a very simple while loop that will run forever until you quit it manually. (Note: if you're using IPython, this may crash your notebook. It's safe to use in your terminal.)

```
while True:
	print("Oh no! I'm stuck...")
```

If you're in the terminal, you can escape from this endless loop by pressing `Control-c` on your keyboard. In IPython, you can stop it by pressing the square `STOP` button in the toolbar.

Let's apply the while loop to our weather app:

```
while True:
    weather = input("What is the weather like today? ")

    if weather == "sunny":
        print("Bring your shades")
    elif weather == "rainy":
        print("Bring your umbrella")
    elif weather == "snowy":
        print("Bring your wooly muffler")
    else:
        print("I don't know what you should bring! I'm just a little program...")
```

Notice that we had to shift everything over one tab to fit it in the `while` block. Now our program will ask us for input again and again, and give us different answers each time.

Let's add one more feature: an `elif` statement that will break us out of the loop and end the program:

```
while True:
    weather = input("What is the weather like today? ")

    if weather == "sunny":
        print("Bring your shades")
    elif weather == "quit":
        break
    elif weather == "rainy":
        print("Bring your umbrella")
    elif weather == "snowy":
        print("Bring your wooly muffler")
    else:
        print("I don't know what you should bring! I'm just a little program...")
```

The `break` command ends the current loop early, ending the program when "quit" is given as input.
