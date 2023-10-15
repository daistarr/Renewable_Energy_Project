# Renewable Energy Project

![Renewable Energy Project](https://github.com/daistarr/Renewable_Energy_Project/blob/3d20d9e459848fd468fe8ec3a55a1b8109bf3d0a/Banner.png)

---

### 1. Problem Statement 
The paradigm shift towards renewable energy is palpable worldwide with diversified energy sources such as hydropower, wind, solar, biofuel, and geothermal energy becoming increasingly pivotal. This shift is not only fundamental for environmental sustainability but also vital for the strategic planning of policymakers, energy corporations, and investors, especially in the context of the United States, where energy demands are incessantly burgeoning.

### 2. Dataset

Historical record ranging from 1965 to 2022 from the "Renewable Energy World Wide" dataset from Kaggle.

### 3. Data Wrangling

During data preprocessing, I merged all these datasets based on the year and country name. In case the observation was split in more than one row for a given year and country, the rows were cumulatively summed and the parameters coalesced. This strategy facilitated the formulation of a consolidated dataset. Subsequently the data was filtered to exclusively encompass the United States, which is the focus of the report. Rows with absent values were removed to assure data integrity.

The final dataset contains 57 rows, representing data from 1965 to 2022, and 21 columns containing the year feature as well as renewable power sources types: geo biomass, wind, solar, hydro electricity, biofuels electricity generation (TWh) as well as percentage of electricity produced from the same sources.

### 4. Exploration Data Analysis (EDA)

The line plots give us a temporal perspective on the evolution of various energy sources:

* Solar generation has witnessed a significant uptick, especially in the latter years, indicating a growing adoption and utilization of solar energy. This could be due to advancements in solar technology, decreases in the cost of solar installations, and possibly due to policy initiatives promoting renewable energy sources.

* Wind generation has experienced a consistent and significant upward trend. Similar to solar energy, advancements in technology and supportive policies might have contributed to this upward trajectory. The growing global emphasis on renewable energy sources to mitigate climate change could also be a key factor.

* Geo Biomass generation shows an overall increase but with noticeable fluctuations. This might suggest that the production is influenced by various factors, such as biomass availability, technological applications, or policy changes that might impact its adoption.

* Biofuels show a consistent increase over the years. This might be associated with a rise in the adoption of biofuels as an alternative to fossil fuels, particularly in sectors like transportation. The development of biofuel technology and possibly incentives for cleaner fuel alternatives might drive this growth.

* Hydro generation seems to be stable and doesn’t exhibit the same growth trend as wind and solar energy. This could be due to geographical or environmental limitations, as hydroelectric power generation often requires substantial water bodies and specific geographical conditions. Also, existing hydroelectric facilities might have reached their production capacities.

* **Summary**: The line plots depict the varied evolution of energy sources, with solar and wind seeing recent sharp rises, hydro and geothermal remaining consistent, and an overall increase in renewable contributions.


### 5. Modeling

