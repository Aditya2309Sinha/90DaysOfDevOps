### Practice Note: File Redirection & Reading in Linux
## Commands Run and What They Did
touch notes.txt
Created an empty file named notes.txt.

echo "Line 1: Practicing Linux redirection" > notes.txt
Wrote the first line to notes.txt, overwriting any existing content.

echo "Line 2: Using append operator" >> notes.txt
Appended a second line to the file without removing existing content.

echo "Line 3: Writing with tee command" | tee -a notes.txt
Displayed the line on the terminal and appended it to notes.txt at the same time.

echo "Line 4: Learning cat, head, and tail" >> notes.txt
echo "Line 5: This is a practice note" >> notes.txt
echo "Line 6: Linux file handling basics" >> notes.txt
echo "Line 7: Redirection is powerful" >> notes.txt
echo "Line 8: End of notes file" >> notes.txt

Added more lines to keep the file concise and within limits.

cat notes.txt
Displayed the entire contents of the file.

head -n 2 notes.txt
Displayed the first 2 lines of the file.

tail -n 2 notes.txt
Displayed the last 2 lines of the file.

# Final File Content (notes.txt)

Total lines: 8
Commands used: >, >>, tee, cat, head, tail
Objective achieved: Practiced writing, appending, and reading files
