1. open jupyter notebook.
2. run the command --> pwd in jupyter notebook to know your current working directory.
3. Put all the attached file in mail into the working directory.( I took the liberty to convert the file to .csv)
4. Run the dataweave-assignment.ipynb using jupyter notebook. run(shift + enter) each cell, ordered by question number.
5. the files which were supposed to be created in question #6 is also attached with the mail. (normalize_mrp_t.csv, normalize_mrp_y.csv)
6. In case of malfunctioning of the code please feel free to contact me.

NOTE- THOUGH PANDAS HAS BEEN IMPORTED. NO PRE-DEFINED FUNCTIONS OF IT HAS BEEN USED. Each question i have treated as another project, that is why some code repetition is there instead of making a def function for it.

LOGIC-
#1 in first question they were asking the overlapping urlh. so i created 2 lists. one to store urlh for file_1 and second to store urlh for file_2. with the help of iteration i counted the number of urlh which are overlapping.

#2 for overlapping urlh we had to calculate price difference. the logic i have used in #1, same i used here also, just for every overlapping urlh i calculated the price difference and stored it into another list.

#3 for this problem i took an empty list. i traversed through the category of both files. with help of 'in' i checked if category is there or not. if not, iadded it into the list.

#4 for list of categories which are not overlapping, i created 2 different lists to store categories from 2 different files. using iteration i checked if they are equal or not, for every category which was not equal i added that in not_overlapping_category list.

#5 i created a list to store concatenated value of category and subcategory. then i converted that list to set which does not allow repeated items. i put all set value to dictionary key and set all of values to 0. with iteration i went through the concatenated list and for every thing repeating the value of dictionary was updated to +1. thats how we got the stats of count for all taxonomies. then that dictionary was converted to simple bar graph using matplotlib.

#6 in this question we had to generate new files with normalized mrp. i used the formula to change the value between 0 and 1( 1 - (x/xmax)). i created empty lists and went through mrp column. for every 0 or empty cell i appended "NA" to the list and normalized the value where it was possible. a new file was created with 'w' permission. with help of loop i put the list info into .csv file.