# Recommendations with IBM
Practice using different recommendation techniques using user interaction with articles. Please not that the content based recommendation portion has not been completed.

## Running the project
This project is coded in an ipynb file, as such it will require Jupyter Notebook to run. Run all cells in order to avoid variables or imports not being set, initialized, and avoid other general issues.

## File Descriptions
### /data
* articles_community - contains data pertaining to actual article, including the content.
* user-item-interactions - contains data on each user and the articles they have interacted with

### Recommendations_with_IBM.ipynb
Since this file contains all of the code since it hasn't been split up into their own packages, classes, and so forth, I'll provide a short description of the functions here.
* get_top_articles -  creates a rank based list of article names. Rank based on the number of the article's interactions by users
* get_top_article_ids - creates a rank based list of article ids. Rank based on the number of the article's interactions by users
* create_user_item_matrix - Return a matrix with user ids as rows and article ids on the columns with 1 values where a user interacted with an article and a 0 otherwise.
* find_similar_users - Computes the similarity of every pair of users based on the dot product Returns an ordered
* get_article_names - returns a list of article names given their associated id's.
* get_user_articles - Provides a list of the article_ids and article titles that have been seen by a user
* user_user_recs - recommends articles based on users most similar to the user. Similarity determined by find_similar_users function.
* find_similar_users2 - fairly similar to find_similar_users, but returns a dataframe with both the user id and the similarity score.
* get_user_article_count - a count of how many unique articles the user has interacted with
* get_top_sorted_users - uses find_similar_users2 and get_user_article_count to build a dataframe combining values from each function.
* user_user_recs_part2 - recommends articles based on users most similar to the user as well as how many articles those users have interacted with. Similarity determined by find_similar_users function.
* create_test_and_train_user_item - creates our train and test data for use with matrix factorization and predicting which articles a user will choose.

### Resources
Help was provided through Udacity mentors. Aid in displaying the descriptive and visual data as well as coding the prediction.
* https://knowledge.udacity.com/questions/201430
* https://knowledge.udacity.com/questions/114505
