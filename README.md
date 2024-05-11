Count Words
This code reads the content of a file presumably a text file containing some paragraphs. After reading, it counts the occurence of each word in the file and then store it into a csv file in Decsending Order.
First, we started by importing libraries that we will use in our code following which comes 3 important functions.
Code start by reading a file named "input.txt" (you can change the file according to your use) and passing it to remove_punctuation fumction to get rid of punctuations while converting the text into lowercase to avoid matchcase problem.
count_words function seperates words on the basis of white spaces using split(), Initialized a dictionary and stored each word as a key while iterating it's value by 1 each time it appears and then return the final dictionary.
sort_paragraph takes the value of the keys and sort them in decsending order.sorted by default sort the values in ascending order so we use reverse=True to change them into descending order
Finally we converted the sorted list into a csv file with word and it's total count.
