# Iris-flower-Dataset-
pip install pandas matplotlib seaborn
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
# Load the iris dataset
iris = sns.load_dataset("iris")
# Print the shape of the dataset
print("Shape:", iris.shape)

# Print column names
print("Columns:", iris.columns.tolist())

# Show the first few rows
print(iris.head())

# Show info (data types, non-null counts)
print(iris.info())

# Show summary statistics
print(iris.describe())
# Print the shape of the dataset
print("Shape:", iris.shape)

# Print column names
print("Columns:", iris.columns.tolist())

# Show the first few rows
print(iris.head())

# Show info (data types, non-null counts)
print(iris.info())

# Show summary statistics
print(iris.describe())
# Scatter plot of sepal_length vs sepal_width, colored by species
sns.scatterplot(data=iris, x="sepal_length", y="sepal_width", hue="species")
plt.title("Sepal Length vs Sepal Width")
plt.show()
sns.pairplot(iris, hue="species")
plt.show()
# Histogram for all numerical features
iris.hist(figsize=(10, 8), bins=15)
plt.suptitle("Histograms of Iris Features")
plt.tight_layout()
plt.show()
sns.histplot(data=iris, x="petal_length", kde=True)
plt.title("Distribution of Petal Length")
plt.show()
# Boxplot for one feature
sns.boxplot(x=iris["sepal_length"])
plt.title("Boxplot of Sepal Length")
plt.show()

# Boxplots for each feature by species
plt.figure(figsize=(10,6))
sns.boxplot(data=iris, x="species", y="petal_length")
plt.title("Petal Length by Species")
plt.show()
