# Count Words
### This code reads the content of a file presumably a text file containing some paragraphs. After reading, it counts the occurence of each word in the file and then store it into a csv file in Decsending Order.

### Import libraries

 
    import pandas as pd
    import string
    from operator import itemgetter

### Code start by reading a file named "input.txt" (you can change the file according to your use):
    with open("input.txt", "r") as file:
    paragraph=file.read()

### To remove punctuations:
    paragraph= remove_punctuations(paragraph.lower())


### Count the words in the para:
    count_words(paragraph)


### Sort the list in descending Order:
    final_paragraph = sort_paragraph(count_words(paragraph))


### Run to make a csv file of the output:
    df=pd.DataFrame(final_paragraph)
    df.to_csv("sorted_paragraph.csv", index=False)

### Print the Output:
     for word,count in final_paragraph:
        print(f'{word}: {count}')