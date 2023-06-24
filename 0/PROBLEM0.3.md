# Einstein

Even if you haven’t studied physics (recently or ever!), you might have heard that E = mc<sup>2</sup>, wherein E represents energy (measured in Joules), E represents mass (measured in kilograms), and represents the speed of light (measured approximately as 300000000 meters per second), per Albert Einstein et al. Essentially, the formula means that mass and energy are equivalent.

In a file called `einstein.py`, implement a program in Python that prompts the user for mass as an integer (in kilograms) and then outputs the equivalent number of Joules as an integer. Assume that the user will input an integer.

## Hints
1. Recall that input returns a `str`, per <https://docs.python.org/3/library/functions.html#input>.
2. Recall that int can convert a `str` to an `int`, per <https://docs.python.org/3/library/functions.html#int>.
3. Recall that Python comes with several built-in functions, per <https://docs.python.org/3/library/functions.html>.

## Before You Begin
Execute `cd` by itself in your terminal window. You should find that your terminal window’s prompt resembles the below:

		$
Next execute

		mkdir einstein
to make a folder called einstein in your codespace.

Then execute

		cd einstein
to change directories into that folder. You should now see your terminal prompt as einstein/ $. You can now execute

		code einstein.py
to make a file called einstein.py where you’ll write your program.

# How to Test
Here’s how to test your code manually. At the `einstein/ $` prompt in your terminal: :

1. Run your program with `python einstein.py`. Type `1` and press Enter. Your program should output: `90000000000000000`
2. Run your program with `python einstein.py`. Type `14` and press Enter. Your program should output: `1260000000000000000`
3. Run your program with `python einstein.py`. Type `50` and press Enter. Your program should output: `4500000000000000000`

# Commit your progran to GITHUB
At the `einstein/ $` prompt in your terminal:

		git add einstein.py
Add einstein.py to the changes to be committed

		git commit -m “Upload completed einstein.py“
Commit all changes in the REPO with the comment “Upload completed einstein.py“
*note: If the file is not complete, adjust the comment to describes what is being commited*

		git push 
Push all changes to the REPO
