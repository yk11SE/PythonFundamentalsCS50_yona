# Tip Calculator

In the United States, it’s customary to leave a tip for your server after dining in a restaurant, typically an amount equal to 15% or more of your meal’s cost. Not to worry, though, we’ve written a tip calculator for you, below!

		def main():
			dollars = dollars_to_float(input("How much was the meal? "))
			percent = percent_to_float(input("What percentage would you like to tip? "))
			tip = dollars * percent
			print(f"Leave ${tip:.2f}")


		def dollars_to_float(d):
			# TODO


		def percent_to_float(p):
			# TODO


		main()

Well, we’ve written most of a tip calculator for you. Unfortunately, we didn’t have time to implement two functions:

- `dollars_to_float`, which should accept a `str` as input (formatted as `$##.##`, wherein each `#` is a decimal digit), remove the leading `$`, and return the amount as a `float`. For instance, given `$50.00` as input, it should return `50.0`.
- `percent_to_float`, which should accept a `str` as input (formatted as `##%`, wherein each `#` is a decimal digit), remove the trailing `%`, and return the percentage as a `float`. For instance, given `15%` as input, it should return `0.15`.

Assume that the user will input values in the expected formats.

## Hints

- Recall that `input` returns a `str`, per <https://docs.python.org/3/library/functions.html#input>.
- Recall that `float` can convert a `str` to a `float`, per <https://docs.python.org/3/library/functions.html#float>.
- Recall that a `str` comes with quite a few methods, per <https://docs.python.org/3/library/stdtypes.html#string-methods>.
Demo

## Before You Begin
Execute `cd` by itself in your terminal window. You should find that your terminal window’s prompt resembles the below:

		$
Next execute

		mkdir tip
to make a folder called tip in your codespace.

Then execute

		cd tip
to change directories into that folder. You should now see your terminal prompt as tip/ $. You can now execute

		code tip.py
to make a file called tip.py where you’ll write your program.

# How to Test
Here’s how to test your code manually. At the `tip/ $` prompt in your terminal: :

1. Run your program with `python tip.py`. Type `$50.00` and press Enter. Then, type `15%` and press Enter. Your program should output: `Leave $7.50`  
2. Run your program with `python tip.py`. Type `$100.00` and press Enter. Then, type `18%` and press Enter. Your program should output: `Leave $18.00`
3. Run your program with `python tip.py`. Type `$15.00` and press Enter. Then, type `25%` and press Enter. Your program should output: `Leave $3.75`

# Commit your progran to GITHUB
At the `tip/ $` prompt in your terminal:

		git add tip.py
Add tip.py to the changes to be committed

		git commit -m “Upload completed tip.py“
Commit all changes in the REPO with the comment “Upload completed tip.py“
*note: If the file is not complete, adjust the comment to describes what is being commited*

		git push 
Push all changes to the REPO