# Renewable Energy Project

![Renewable Energy Project](https://github.com/daistarr/Renewable_Energy_Project/blob/3d20d9e459848fd468fe8ec3a55a1b8109bf3d0a/Banner.png)

---

### 1. Problem Statement 

The paradigm shift towards renewable energy is palpable worldwide with diversified energy sources such as hydropower, wind, solar, biofuel, and geothermal energy becoming increasingly pivotal. This shift is not only fundamental for environmental sustainability but also vital for the strategic planning of policymakers, energy corporations, and investors, especially in the context of the United States, where energy demands are incessantly increasing.

---

### 2. Dataset

* [Raw dataset](0_data)

Historical record ranging from 1965 to 2022 from the This site was built using ["Renewable Energy World Wide"](https://www.kaggle.com/datasets/belayethossainds/renewable-energy-world-wide-19652022) dataset from Kaggle.

---

### 3. Data Wrangling

* [Data Wrangling Notebook](1_Wrangling/Capstone2_wrangling.ipynb)
* [Clean dataset](1_Wrangling/merged_usa_dataset.csv)

During data preprocessing, I merged all these datasets based on the year and country name. In case the observation was split in more than one row for a given year and country, the rows were cumulatively summed and the parameters coalesced. This strategy facilitated the formulation of a consolidated dataset. Subsequently the data was filtered to exclusively encompass the United States, which is the focus of the report. Rows with absent values were removed to assure data integrity.

The final dataset contains 57 rows, representing data from 1965 to 2022, and 21 columns containing the year feature as well as renewable power sources types: geo biomass, wind, solar, hydro electricity, biofuels electricity generation (TWh) as well as percentage of electricity produced from the same sources.

![Data](https://github.com/daistarr/Renewable_Energy_Project/blob/fc387f02635a7b58a980e8c8eac4e4bd85e89d1d/1_Wrangling/data.png)

---

### 4. Exploration Data Analysis (EDA)

* [EDA Notebook](2_EDA/Capstone2_EDA.ipynb)
* [Pre-processing Notebook](3_Preprocessing/Capstone2_Preprocessing.ipynb)

![Line Plot](https://github.com/daistarr/Renewable_Energy_Project/blob/fc387f02635a7b58a980e8c8eac4e4bd85e89d1d/2_EDA/EDA_figures/year.png)

The line plots give us a temporal perspective on the evolution of various energy sources:

* Solar generation has witnessed a significant uptick, especially in the latter years, indicating a growing adoption and utilization of solar energy. This could be due to advancements in solar technology, decreases in the cost of solar installations, and possibly due to policy initiatives promoting renewable energy sources.

* Wind generation has experienced a consistent and significant upward trend. Similar to solar energy, advancements in technology and supportive policies might have contributed to this upward trajectory. The growing global emphasis on renewable energy sources to mitigate climate change could also be a key factor.

* Geo Biomass generation shows an overall increase but with noticeable fluctuations. This might suggest that the production is influenced by various factors, such as biomass availability, technological applications, or policy changes that might impact its adoption.

* Biofuels show a consistent increase over the years. This might be associated with a rise in the adoption of biofuels as an alternative to fossil fuels, particularly in sectors like transportation. The development of biofuel technology and possibly incentives for cleaner fuel alternatives might drive this growth.

* Hydro generation seems to be stable and doesn’t exhibit the same growth trend as wind and solar energy. This could be due to geographical or environmental limitations, as hydroelectric power generation often requires substantial water bodies and specific geographical conditions. Also, existing hydroelectric facilities might have reached their production capacities.

---

### 5. Modeling

* [Modeling Notebook](4_Modeling/Capstone2_Modeling.ipynb)

The objective of this stage involves employing Time Series Forecasting to formulate predictive models using ARIMA and LSTM, aimed at forecasting the growth of various renewable energy sources over the subsequent decade. 

A variety of approaches and models were explored for a methodological comparison, being compared based on the Mean Absolute Error (MAE), Root Mean Square Error (RMSE), the latest recorded value, the predicted value, growth percentage, Compound Annual Growth Rate (CAGR), and Sum of Squared Residuals (SSR). 

Also, to validate and evaluate the model, data were analyzed utilizing machine learning, allocating 80% of the dataset to the training set and the remaining 20% to the testing set. 

Furthermore, all model plots feature solid lines representing the actual observed data, dashed lines indicating the forecasted values for the test set period (model validation period), and dotted lines projecting forecasted values for the next decade (2022-2031).

Here is the example of the Non-Stationary ARIMA (AutoRegressive Integrated Moving Average), a prominent model known for its proficiency in analyzing and forecasting time series data, particularly due to its capability to handle data with a trend. In this second approach, I decided not to check the stationarity of the data:

![ARIMA](https://github.com/daistarr/Renewable_Energy_Project/blob/a61d325991ead32fb731e7cb342cbebd6bf711c4/4_Modeling/Modeling_Figures/ARIMA2.png)

---

### 6. Modeling Selection

* [Modeling Notebook](4_Modeling/Capstone2_Modeling.ipynb)

In determining the optimal model for predicting the most rapidly growing renewable energy source over the next decade, I assessed various error metrics—Mean Absolute Error (MAE), Root Mean Square Error (RMSE), and Sum of Squared Residuals (SSR)—across several models, namely Linear Regression, Non-Stationary ARIMA, Stationary ARIMA, and LSTM, each employed to forecast energy generation for each source.

Based on this approach, Non-Stationary ARIMA performed the best, with the lowest MAE and RMSE as well as the second lowest SSR.

<img src="https://github.com/daistarr/Renewable_Energy_Project/blob/8a1b9fce22ab3f79cad79bffb131feb46c99b389/4_Modeling/Modeling_Figures/model_eval.png" width="320">

---

### 7. Takeaways

* [Report](4_Modeling/5_Report/Report.pdf)

* **Optimal Predictive Model**: The ARIMA Non-Stationary model stands out as the most suitable for this dataset.

* **Foremost in Future Growth**: Solar energy is forecasted to witness the most substantial growth in the next decade.

<img src="https://github.com/daistarr/Renewable_Energy_Project/blob/228056c919da13d6fc047b5dfb0148a7e4e48dc4/4_Modeling/Modeling_Figures/renewable_energy.png" width="600">

* **Navigating Towards Renewables**: A discernible upward trend in several renewable sources, notably solar, wind, and biofuels, signals a pivot towards enhanced sustainable energy practices. The pronounced rises in solar and wind generation may be indicative of periods where policies or incentives were introduced to promote renewable energies.
  
* **Influence of Technological Progress**: Technological advancements and diminishing production costs, especially in the realms of solar and wind energy, are likely driving factors in their increased adoption and development.


