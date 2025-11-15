**Dataset Source**
The dataset used for this analysis is the "Movies" dataset, sourced from Kaggle: 
[Kaggle: Movies Dataset](https://www.kaggle.com/datasets/danielgrijalvas/movies)

**Key Skills and Techniques Demonstrated**

**1. Data Wrangling and Preprocessing**

*Handling Missing Data*: Identified columns with missing values (e.g., 'budget' at 28%, 'gross' at 2%) and subsequently managed them by dropping incomplete rows to ensure the integrity of financial analysis (df.dropna()).

*Data Type Conversion*: Converted relevant columns, including 'budget', 'gross', 'runtime', and 'votes', to the integer type (.astype('int64')) to facilitate accurate numerical calculations.

*Data Normalization*: Cleaned categorical variables, specifically re-labeling inconsistent entries (e.g., changing 'Unrated' to 'Not Rated' in the 'rating' column).

*Feature Engineering*: Created a new financial metric, 'profit', calculated as the difference between 'gross' revenue and 'budget'.

*Duplicate Handling*: Ensured data uniqueness by identifying and removing potential duplicate entries (df.drop_duplicates(inplace=True)).

**2. Data Analysis and Insights**

*Correlation Analysis* (df.corr(numeric_only=True)): Generated a correlation matrix to quantitatively assess relationships between all numerical features.

*Finding Strong Correlations*: Identified pairs of features with high correlation coefficients, such as gross revenue and profit (correlation ~0.9844) and budget and gross revenue (correlation ~0.7402).

*Visualization of Correlation*: The relationship between budget and gross earnings is visually presented here .

*Performance Metrics*: Analyzed and sorted data to determine top-performing entities, including the top 5 highest-grossing films and the directors associated with the highest single-movie profit.

*Genre Analysis*: Explored genre data to understand central tendencies by calculating the mean and median gross revenue grouped by film genre.

**Technologies and Libraries**

This project leverages the following Python libraries:

pandas: Core library for data structures and data analysis tools.

numpy: Provides support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions.

matplotlib.pyplot: Used for creating static, interactive, and animated visualizations, including scatter plots.

seaborn: (Imported) A library for making attractive and informative statistical graphics.

matplotlib.ticker: Utilized for precise axis labeling, including formatting tick labels into millions (M) and billions (B) for enhanced readability (e.g., mticker.FuncFormatter).

plt.style.use('ggplot'): Applied to enhance the aesthetic appearance of visualizations.
