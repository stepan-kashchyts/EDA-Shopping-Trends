# Exploratory Data Analysis on Shopping Trends

## Project Overview

This project involves performing exploratory data analysis (EDA) on a dataset of shopping trends. The aim is to uncover actionable insights into consumer behavior, purchasing patterns, and seasonal trends through various statistical and visualization techniques.

## Key Highlights

- **Objective**: Analyze shopping data to understand customer behavior and trends.
- **Dataset**: `shopping_trends.csv`, including customer demographics, purchase details, and product categories.
- **Outcome**: Provided detailed insights into customer preferences, spending habits, and seasonal variations.

## Technologies Used

- **Python**: Used for data manipulation and analysis.
- **Pandas**: For handling and processing data.
- **Matplotlib**: For creating visualizations such as histograms, bar plots, pie charts, scatter plots, and box plots.

## Analysis & Insights

### 1. Customer Demographics

- **Histogram of Age**: The analysis revealed that the majority of customers are middle-aged.
  ```python
  plt.hist(data['Age'], rwidth=0.85)
  plt.title('Histogram of Age')

    Gender Distribution: The data shows a predominantly male customer base.

    python

    data['Gender'].value_counts().plot(kind='bar')
    plt.title('Barplot of Gender Distribution')

2. Purchase Patterns

    Subscription Status: Distribution of subscription statuses among customers.

    python
```
data['Subscription Status'].value_counts().plot(kind='pie', autopct='%1.1f%%')
plt.title('Pie chart of Subscription Status')
```
Purchase Amount by Category: Identified which product categories have the highest average purchase amounts.

python
```
data.groupby('Category')['Purchase Amount (USD)'].mean().sort_values(ascending=False).tail(3)
```
Purchase Trends by Season: Seasonal variations in total purchase amounts.

python
```
    data.groupby('Season')['Purchase Amount (USD)'].sum().plot()
    plt.xlabel('Season')
    plt.title('Sum of Purchase Amount by Season')
```
3. Review Ratings

    Scatter Plot of Previous Purchases vs. Review Rating: Examined the relationship between previous purchases and review ratings.

    python
```
data.head(75).plot(x='Previous Purchases', y='Review Rating', kind='scatter')
plt.title('Scatter Plot - Previous Purchases vs. Review Rating')
```
Review Ratings by Gender: Compared review ratings between male and female customers.

python
```
    data.boxplot(column='Review Rating', by='Gender')
    plt.xlabel('Gender')
    plt.ylabel('Review Rating')
    plt.title('Review Rating Distribution by Gender')
```
4. Additional Insights

    Purchase Amount Distribution: Analyzed the distribution of purchase amounts, revealing a tendency towards both low and high price points.

    python
```
data['Purchase Amount (USD)'].plot(kind='hist', bins=10)
plt.xlabel('USD')
plt.ylabel('Frequency')
plt.title('Histogram of Purchase Amount Distribution')
```
Top Colors by Review Rating: Analyzed mean review ratings for different colors.

python
```
    data.groupby('Color')['Review Rating'].mean().head(5).plot(kind='bar')
    plt.xlabel('Color')
    plt.ylabel('Mean Review Rating')
    plt.title('Mean Review Rating for Each Color')
```
# Visualizations

Below are some of the key visualizations generated from the analysis:

# Conclusion

This project provided valuable insights into shopping trends, including customer demographics, purchasing patterns, and seasonal variations. These findings can help in making data-driven decisions for targeted marketing and business strategies.

For more information, you can visit my portfolio (https://stepan-kashchyts.github.io/stepan_kashchyts.github.io/) or connect with me on LinkedIn. (https://www.linkedin.com/in/stepan-kashchyts/)
