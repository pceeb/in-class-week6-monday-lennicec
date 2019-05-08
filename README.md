## In class exercise

1. If you wanted to reuse this program for a file that had 17 headers lines. What line of code
would you change in our program?

        Write the line of code that you will replace here: Line 27; if LineNumber > 0: #skipe first line

        What will be the new code?

        Write the new code here: The new code would be if LineNumber > 17: #skips the first 17 lines

2. What would happen if we don’t included `import sys` in our program?

        Write you answer here: If you dont write 'import sys', then python will not load the sys module, and, thus sys.argv variable will not be accessible to you.

3. Let’s suppose that the third file that the user provides as input
has only one column. What error message will be generated?

        Write you answer here: Therefore the python script that reads:
	for line in Infile:
            if LineNumber > 0
	tells the program to skip the first line of the file and print everything from then on starting with the second line of the file
	Therefore, there will be an error that will probably say that File 3 is empty or does not have line that can be printed

4. Our program split lines of input files (except the first file) into elements
that are tab delimitated. However, data could be split by `,` or many other
characters. In this case is a good idea to define a new variable that takes the delimiter
provide by the user. Using what you learn about `sys.argv` in this class`.
Write a variable that reads a delimiter (e.g ',') provided as the first input file.

        Write your code here:In order to allow the user to ensure that the code can work for any delimter you can make the delimeter another argument 
	For example, at the beginning of the code you can write \t==3:
	And later on, the code for splitting the lines will be:
	else:
                    ElementList = Line.split(3)
                    if len(ElementList) > 0:
                        MasterList[RecordNum] += (3 + ElementList[1]) # += adding instead of replacing
                        RecordNum += 1
