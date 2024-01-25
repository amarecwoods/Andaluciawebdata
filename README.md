# Andalucía Web Pages Dataset

This repository contains a dataset of web pages related to Andalucía, a region in Spain. The dataset provides information about various websites, including their titles, URLs, status, update frequency, size, keywords, and subject matter.

## Table of Contents
1. [Description](#description)
2. [Data Source](#data-source)
3. [Data Analysis](#data-analysis)
4. [Visualization](#visualization)

## Description
The dataset consists of web pages related to Andalucía, covering a wide range of subjects such as medicine, food industry, education, media, religion, and arts. Each entry includes details such as the title of the web page, URL, status (active or inactive), update frequency, size, keywords, and subject matter.

## Data Source
The dataset was obtained from [Kaggle](https://www.kaggle.com/datasets/isabelocastillo/pginas-web-de-andaluca?rvi=1), a platform for data science and machine learning enthusiasts.

## Data Analysis
The dataset was analyzed using Python and various libraries such as pandas, seaborn, and matplotlib. Here is a snippet of the Python code used for analysis:

```python
import pandas as pd

# Read the dataset
df = pd.read_csv("/Volumes/Data SSD/Kaggle/Unclean/webs_andalucia.csv", encoding='UTF-8')

# Display the first 20 rows
df.head(20)

# Check for missing values
df.isnull().sum()

# Count duplicated entries
df.count().duplicated()

# Filter data based on specific keywords
mask = df['Título'].str.contains('Cádiz', na=False)
df2 = df[mask]

# Analyze keyword counts
keywordcounts = df2['Palabras_clave'].value_counts()

# Analyze content counts
Content_counts = df2['Materia'].value_counts()

# Analyze visit frequency
Visitfrequency = df2['Frecuencia'].value_counts()

# Export cleaned datasets of active and inactive sites
Active_Sitesmask = df2['Estado'].str.contains('Activa', na=False)
ActiveSites = df2[Active_Sitesmask]
ActiveSites.to_csv('Activesitesclean', sep=',', index=False, encoding='utf-8')

Passive_Sitemask = df2['Estado'].str.contains('Inactiva', na=False)
PassiveSites = df2[Passive_Sitemask]
PassiveSites.to_csv('PassiveSitessitesclean', sep=',', index=False, encoding='utf-8')
```markdown
# Andalucía Web Pages Dataset

This repository contains a dataset of web pages related to Andalucía, a region in Spain. The dataset provides information about various websites, including their titles, URLs, status, update frequency, size, keywords, and subject matter.

## Table of Contents
1. [Description](#description)
2. [Data Source](#data-source)
3. [Data Analysis](#data-analysis)
4. [Visualization](#visualization)

## Description
The dataset consists of web pages related to Andalucía, covering a wide range of subjects such as medicine, food industry, education, media, religion, and arts. Each entry includes details such as the title of the web page, URL, status (active or inactive), update frequency, size, keywords, and subject matter.

## Data Source
The dataset was obtained from [Kaggle](https://www.kaggle.com/datasets/isabelocastillo/pginas-web-de-andaluca?rvi=1), a platform for data science and machine learning enthusiasts.

## Data Analysis
The dataset was analyzed using Python and various libraries such as pandas, seaborn, and matplotlib. Here is a snippet of the Python code used for analysis:

```python
import pandas as pd

# Read the dataset
df = pd.read_csv("/Volumes/Data SSD/Kaggle/Unclean/webs_andalucia.csv", encoding='UTF-8')

# Display the first 20 rows
df.head(20)

# Check for missing values
df.isnull().sum()

# Count duplicated entries
df.count().duplicated()

# Filter data based on specific keywords
mask = df['Título'].str.contains('Cádiz', na=False)
df2 = df[mask]

# Analyze keyword counts
keywordcounts = df2['Palabras_clave'].value_counts()

# Analyze content counts
Content_counts = df2['Materia'].value_counts()

# Analyze visit frequency
Visitfrequency = df2['Frecuencia'].value_counts()

# Export cleaned datasets of active and inactive sites
Active_Sitesmask = df2['Estado'].str.contains('Activa', na=False)
ActiveSites = df2[Active_Sitesmask]
ActiveSites.to_csv('Activesitesclean', sep=',', index=False, encoding='utf-8')

Passive_Sitemask = df2['Estado'].str.contains('Inactiva', na=False)
PassiveSites = df2[Passive_Sitemask]
PassiveSites.to_csv('PassiveSitessitesclean', sep=',', index=False, encoding='utf-8')
```

## Visualization
For visualization of the analyzed data, you can refer to the [Tableau page](https://public.tableau.com/views/CdizInternetSearchExplorer/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link) created using the data from this dataset.

```

Please note that the content provided here is a summary of the dataset and its analysis. You may need to provide more detailed information or additional sections based on your specific requirements or audience.
