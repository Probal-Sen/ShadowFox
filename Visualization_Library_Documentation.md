# Visualization Library Documentation  
**Libraries Chosen:** Matplotlib and Seaborn  

---

## 1. Library Overview  

### Matplotlib  
Matplotlib is a comprehensive and widely used Python library for creating static, animated, and interactive visualizations.  
- **Unique Features:** Highly customizable, supports low-level control of plot elements.  
- **Typical Use Cases:** Scientific publications, educational plots, and data exploration.  

### Seaborn  
Seaborn is a high-level data visualization library built on top of Matplotlib.  
- **Unique Features:** Simplifies complex plots, offers beautiful default styles and themes.  
- **Typical Use Cases:** Statistical visualizations, quick exploratory data analysis.  

---

## 2. Graph Types  

### A. Line Plot  
**Description:** Shows trends or changes over continuous data.  
**Use Case:** Visualizing stock prices over time.  

**Matplotlib Example:**  
```python
import matplotlib.pyplot as plt
x = [1,2,3,4,5]
y = [2,3,5,7,11]
plt.plot(x, y, marker='o')
plt.title("Matplotlib Line Plot")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```
**Seaborn Example:**
```python
import seaborn as sns
import matplotlib.pyplot as plt
data = {'x':[1,2,3,4,5], 'y':[2,3,5,7,11]}
sns.lineplot(x='x', y='y', data=data, marker='o')
plt.title("Seaborn Line Plot")
plt.show()
```
## B. Scatter Plot:
**Description:** Displays individual data points to show relationships or patterns.
**Use Case:** Analyzing correlation between two variables.

**Matplotlib Example:**

```python
plt.scatter([5,7,8,7,2,17,2,9,4,11],[99,86,87,88,100,86,103,87,94,78])
plt.title("Matplotlib Scatter Plot")
plt.show()
```

**Seaborn Example:**
```python
sns.scatterplot(x=[5,7,8,7,2,17,2,9,4,11], y=[99,86,87,88,100,86,103,87,94,78])
plt.title("Seaborn Scatter Plot")
plt.show()
```

## C. Bar Chart:

**Description:** Represents categorical data with rectangular bars.  
**Use Case:** Comparing product sales.  

**Matplotlib Example:**
```python
import matplotlib.pyplot as plt

x = ['A','B','C','D']
y = [3,7,8,5]
plt.bar(x, y)
plt.title("Matplotlib Bar Chart")
plt.show()
```

**Seaborn Example:**  
```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

df = pd.DataFrame({'Category': ['A','B','C','D'], 'Values': [3,7,8,5]})
sns.barplot(x='Category', y='Values', data=df)
plt.title("Seaborn Bar Chart")
plt.show()
```

## D. Histogram  

**Description:** Displays the distribution of a dataset.  
**Use Case:** Understanding data distribution.  

**Matplotlib Example:**  
```python
import matplotlib.pyplot as plt

data = [7,8,5,6,8,6,7,5,6,8,6,7,8,5,6]
plt.hist(data, bins=5)
plt.title("Matplotlib Histogram")
plt.show()
```
**Seaborn Example:**  
```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.histplot([7,8,5,6,8,6,7,5,6,8,6,7,8,5,6], bins=5, kde=True)
plt.title("Seaborn Histogram")
plt.show()
```

## 3. Comparison  

| Feature         | Matplotlib                                  | Seaborn                                           |
|-----------------|---------------------------------------------|-------------------------------------------------|
| **Ease of Use** | More verbose, requires manual styling.       | High-level API with simple syntax.               |
| **Customization**| Extremely customizable at low level.        | Less customizable but inherits Matplotlib control.|
| **Interactivity**| Basic interactivity.                        | Limited interactivity (depends on Matplotlib).    |
| **Performance**  | Handles large datasets well.                | Slightly slower due to additional abstraction.    |
| **Best For**     | Complex, highly customized visualizations.  | Quick, aesthetically pleasing statistical plots.  |

---

## 4. Resources  

- [Matplotlib Quick Start](https://matplotlib.org/stable/users/explain/quick_start.html#quick-start)  
- [Seaborn Introduction](https://seaborn.pydata.org/tutorial/introduction.html)  
