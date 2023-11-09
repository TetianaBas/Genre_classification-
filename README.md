# TV Show Genre Prediction Project

This project focuses on predicting the genre of TV shows based on their descriptions. The workflow includes data scraping from IMDb using BeautifulSoup, building a classification model using machine learning techniques, and iteratively improving the model for better performance.

## Data Scraping

The data was scraped from IMDb using BeautifulSoup and includes information such as TV show name, release year, ratings, and genre. The IMDb search page [link](https://www.imdb.com/search/title/?title_type=tv_series&num_votes=100000,&sort=release_date,asc) was used for scraping.

## Classification

### Initial Model: Multinomial Naive Bayes
The initial model was built using a Multinomial Naive Bayes classifier with TF-IDF vectorization. However, the model's performance was suboptimal, with an accuracy of 0.4. The classification report revealed low precision, recall, and F1-score values across various genres.

### Hyperparameter Tuning: GridSearchCV
To enhance model performance, a GridSearchCV approach was employed to explore different hyperparameter combinations for the TF-IDF vectorizer and Multinomial Naive Bayes classifier. The tuned model resulted in an accuracy of 0.8, indicating significant improvement. The classification report showed higher precision, recall, and F1-score values across genres.

### Model Improvement: Random Forest
Identifying the limitations of the initial model, a switch to a Random Forest classifier was made. The Random Forest model demonstrated superior performance over the Multinomial Naive Bayes model. The accuracy remained at 0.8, but the macro and weighted average F1-scores improved, indicating better overall precision and recall.

## Model Evaluation

The confusion matrices provided insights into the models' performances. The Random Forest model, with its ensemble learning, exhibited higher values on the diagonal, indicating correct predictions for various genres. In contrast, the Multinomial Naive Bayes model, despite the same accuracy, showed lower values on the diagonal, suggesting less robust performance.

## Conclusion

The final Random Forest model, implemented after iterative improvements, is the preferred choice due to its better overall performance. The decision to switch models was justified by the need to handle non-linear relationships and improve the accuracy and precision of genre predictions.

## Next Steps

The model's misclassifications were analyzed to identify potential patterns and areas for further improvement. Continuous evaluation and refinement are essential for adapting to diverse TV show descriptions and ensuring accurate genre predictions.
