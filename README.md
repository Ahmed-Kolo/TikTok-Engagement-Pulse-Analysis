### Project Summary: TikTok Engagement Pulse - Time Series Analysis

This project aimed to perform a Time Series Analysis on TikTok view count data within a Discovery-to-Action (DTA) framework to understand engagement patterns and inform content scheduling strategies. Due to the unavailability of the original dataset, a synthetic dataset reflecting typical TikTok view patterns (with trend, weekly seasonality, and noise) was generated for this analysis.

### Key Findings:

*   **Discovery Phase (Data Loading, Preprocessing & Decomposition):**
    *   The synthetic `tiktok_views.csv` dataset was successfully loaded, preprocessed (date conversion, indexed, resampled to daily frequency), and decomposed into its constituent trend, seasonal, and residual components.
    *   Visualization of these components clearly showed an increasing **trend** in views over the analysis period and strong **weekly seasonality**.

*   **Technical Phase (Stationarity Testing with ADF Test):**
    *   The Augmented Dickey-Fuller (ADF) test was performed on the daily view data.
    *   **Conclusion:** The p-value (0.986) was greater than the significance level (0.05), leading to a failure to reject the null hypothesis. This indicates that the time series is **non-stationary** and will likely require differencing (the 'I' component in ARIMA) for future forecasting models.

*   **Action Phase (Strategic Recommendations & Next Steps):**
    *   **Peak Engagement Days:** Analysis of the seasonal component identified **Saturday** as the peak engagement day.
    *   **Lowest Engagement Days:** **Tuesday** was identified as the day with the lowest average seasonal effect.
    *   **Content Scheduling Recommendation:** Content creators are advised to focus on publishing high-impact content on **Saturdays** to maximize visibility, and consider less critical activities or content repurposing on **Tuesdays**.
    *   **Forecasting Foundation:** This analysis established a strong foundation for developing predictive models. The identified non-stationarity, clear seasonality, and observed trend are crucial inputs for selecting and configuring ARIMA/SARIMA models (e.g., determining differencing orders and seasonal components) for future TikTok engagement forecasting.

## Resources

*   **Python:** The primary programming language used for this analysis.
*   **Pandas:** Utilized for data manipulation, cleaning, and time series specific operations.
*   **Numpy:** Used for numerical operations, especially during synthetic data generation.
*   **Matplotlib & Seaborn:** Employed for data visualization and plotting the time series components and insights.
*   **Statsmodels:** Essential for time series decomposition (`seasonal_decompose`) and statistical tests like the Augmented Dickey-Fuller (ADF) test.
