# Hotel Booking



## Dataset Content
This dataset contains over 10,000 rows and 20 columns detailing guest bookings across two hotel types: Resort Hotel and City Hotel. It was sourced from Kaggle and thoroughly cleaned and analyzed using Matplotlib, Seaborn, and Plotly.

Important: Plotly charts are interactive and may not render correctly in GitHub’s notebook preview.
To view them properly, please download the notebook and open it in Jupyter or VS Code.


## Business Requirements
Determine which hotel type (City Hotel vs. Resort Hotel) performs better during the same time periods.  Performance will be evaluated using key metrics such as occupancy rate, average daily rate (ADR),behavior patterns, distribution channel etc.


## Seasonality affects the two hotels differently?
Seasonal patterns drive pricing and staffing decisions.
How to validate:
Group by month and hotel.
Compare ADR, occupancy, and booking volume.
Plot seasonal curves.

![monthly revenue trend](output/charts/monthly_revenue_trend.png)

Even though Resort Hotels hit higher revenue peaks during the summer months compared to City Hotels, their performance shows a steep drop afterward followed by a slow recovery. On the other hand, City Hotels show a more stable and consistent revenue trend, with fluctuations that feel more controlled and less extreme than the Resort Hotel. This suggests that Resort Hotels are more dependent on seasonal tourism, while City Hotels benefit from steadier demand throughout the year.


## High reliance on TA/TO channels reduces net profit due to higher commission fees. 

![Distribution Channel](output/charts/distribution_channel_share.png)
The pie chart gives us a clear picture of how bookings are distributed across different channels. It’s immediately obvious that TA/TO (Travel Agents/Tour Operators) dominate the scene, accounting for over 79% of all bookings. Direct bookings come in second at around 15%, followed by Corporate with just under 6%. GDS and Undefined barely register, making up a tiny fraction of the total.

This tells us that most guests are coming through third-party intermediaries rather than booking directly or through corporate deals.

To increase the bottom line and reduce the commission paid to TA/TO our marketing strategy should focus on promoting more direct or corporate bookings.

in addition our analysis indicates that city hotels generate more revenue throughout the year and has a healthy and stable trend

![Revenue](output/charts/revenue_trend.png)



## Project Plan
Outline the high-level steps taken for the analysis.
The project followed a structured, end‑to‑end data analytics workflow to ensure clarity, reproducibility, and meaningful insights:
* Created a clean folder structure
* Downloaded the Hotel Booking Demand dataset from Kaggle.
* Imported the raw CSV file into the project’s data/raw directory.

### How was the data managed throughout the collection, processing, analysis and interpretation steps?
#### Data Cleaning & Pre‑Processing
Handled missing values, inconsistent formats, and outliers.
Converted date components into a proper datetime column.
Created new engineered features (e.g., stay_length, has_breakfast, is_occupied).
Saved the cleaned dataset into data/processed.

Exploratory Data Analysis (EDA)

Used Matplotlib and Seaborn for static visualizations.
Used Plotly for interactive charts (not visible on GitHub, but viewable locally).
Explored distributions, correlations, seasonal patterns, and hotel performance metrics.

* Why did you choose the research methodologies you used?

Because the goal was to understand patterns, trends, and relationships in hotel booking behavior. 
Seasonal trends
Differences between hotel types
Booking channel performance
Guest behavior patterns
## The rationale to map the business requirements to the Data Visualisations
To compare performance between City Hotel and Resort Hotel, we need visualisations that reveal differences in demand, pricing, cancellations, and guest behaviour over time. Time‑series and comparative charts make these differences visible and measurable.
* Pie Chart
Shows Distribution channel

* Line charts (ADR over time)  
Compares pricing strategies and revenue potential.

* Monthly booking volume bar chart  
Highlights seasonal demand patterns.

## Analysis techniques used
#### List the data analysis methods used and explain limitations or alternative approaches.
* Exploratory Data Analysis (EDA)

 Used descriptive statistics, distribution plots, and summary tables to understand the structure of the dataset.Tools: Pandas, Matplotlib, Seaborn, Plotly.
* Limitations:

EDA is descriptive, not predictive.
It highlights patterns but cannot confirm causation.
Interactive Plotly charts do not render on GitHub, requiring static PNG exports.

* How did you structure the data analysis techniques. Justify your response. Before any modelling or comparison, I explored the dataset to understand distributions, missing values, and data types.Created meaningful variables (e.g., stay length, breakfast indicator) and fixed date formats.
Justification: Raw data rarely answers business questions directly; engineered features unlock deeper insights.
Grouped data by hotel type, month, and booking characteristics.
Justification: The business requirement focuses on comparing hotel performance over time.
Investigated booking channels, lead times, cancellations, and meal types.
Justification: These factors directly influence profitability and operational decisions.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
No revenue column: Revenue must be inferred from ADR × stay length × occupancy.
No cost data: Profitability cannot be calculated precisely.
Limited time range: Only three years of data restrict long‑term trend analysis.
Plotly charts not visible on GitHub: Interactive insights are lost in the online preview.
Categorical variables with many levels: Harder to visualise cleanly.
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?
Generative AI tools were used strategically throughout the project to enhance workflow and creativity:
Helped structure the project into clear business requirements, analytical steps, and insights.
Assisted in designing a clean folder structure and reproducible workflow.
Provided guidance on how to communicate insights effectively for non‑technical stakeholders.
Suggested more efficient Pandas operations (e.g., vectorised feature engineering).
Helped debug issues with date parsing, Plotly exports, and path handling.
Provided cleaner, more readable versions of visualisation code.
Assisted in writing polished explanations, README sections, and insight summaries.
Ensured the narrative remained clear, professional, and business‑focused.
## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data? As soon as the data loaded the personal details such as Name,Email,Phone number and Credit card number were dropped permanently 
* How did you overcome any legal or societal issues? the data was in a public domain however when i produced the data i removed all the personal data and referenced that the data was obtained from Kaggle and who was the publisher.





## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.
Numpy
Pandas
Matlibplot
Seaborn
Plotly

## Conclusion
The analysis of over 10,000 hotel bookings across City Hotel and Resort Hotel reveals distinct patterns in performance, guest behaviour, and revenue drivers. By examining ADR, occupancy, cancellations, booking channels, and seasonal trends, we’ve uncovered insights that directly address the business requirements.

City Hotels consistently maintain higher occupancy rates, especially during business-heavy months, suggesting stronger year-round demand. Resort Hotels, on the other hand, achieve higher ADR during peak seasons, indicating strong pricing power during holidays and summer periods.

A key finding is the dominance of TA/TO channels, which drive a large share of bookings but also incur high commission costs. This reduces net profitability despite strong booking volume. Encouraging more direct or corporate bookings could significantly improve margins.
Seasonality plays a major role: Resort Hotels peak in summer, while City Hotels perform steadily year-round, requiring tailored pricing and staffing strategies.

Additionally, the ADR by Market Segment analysis reveals that:

Online TA and Direct bookings yield the highest ADR, both approaching £120.

Aviation bookings also show strong ADR, around £100.

Complementary bookings generate the lowest ADR, below £10, offering minimal revenue contribution.

Corporate and Offline TA/TO segments fall in the mid-to-low range, suggesting potential for pricing optimization.

This segmentation insight reinforces the importance of channel strategy: not all bookings contribute equally to revenue, and high-volume channels may dilute profitability if ADR is low or commissions are high.

Overall, City Hotels deliver consistent occupancy, while Resort Hotels excel in high-ADR seasonal windows. Profitability is shaped not just by volume, but by channel mix, guest behavior, and pricing strategy. Targeted interventions — such as shifting demand toward higher-yield segments and optimizing seasonal pricing — can significantly enhance performance across both hotel types.
## Credits 

the dataset was collected from Kaggle.from the user (Narges Sedrehneshin)





## Acknowledgements (optional)
* Thank the people who provided support through this project especially Vasi and Mark and Neil.