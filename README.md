# Analysis-of-Urban-Walkability
Conducted a comprehensive study to evaluate the relationship between urban walkability, socioeconomic and urban planning factors using machine learning algorithms, enabling efficient calculation of key urban metrics.

1. Introduction
Walkability, an essential element of urban planning, focuses on making walking safe and convenient in cities, with accessible transportation options nearby. A key aspect of building vibrant, sustainable cities is the comprehension of pedestrian movement and its connection to factors like transit access and destination accessibility. Urban planners, policymakers, and researchers benefit from a walkability index, which quantitatively measures pedestrian-friendliness, for prioritizing investments and informed land use decisions. Our research in this context involves analyzing urban walkability and its determining factors through machine learning methods. Our goal is to offer valuable insights for urban planners and communities seeking to improve walkability and create healthier, pedestrian-friendly spaces by analyzing job-housing balance, land use diversity, traffic measures, demographics, and employment factors.
1.1 Problem and Background
The significance of promoting walking as the main mode of transportation has been accentuated by rapid urbanization, calling for advancements in urban design and transportation infrastructure. Walkable cities require a detailed understanding of the complex relationships between urban factors. We are researching to bridge this gap by examining the intricate nature of urban walkability patterns and their interplay with diverse urban variables.
1.2 Project Goals
Enhancing urban design, sustainable transportation, and pedestrian-friendly environments is the goal of our project. We achieve this by analyzing population
dynamics, job structures, land use, and transit to provide actionable insights for urban planners, legislators, and communities.
1.3 Research Questions
Building upon our investigation of urban walkability factors, our goal is to further explore the intricacies of creating pedestrian-friendly environments. Thus, our research aims to understand the complex connections between these factors and how they affect walkability. Our goal is to provide valuable insights for urban planners, policymakers, and communities seeking to create vibrant, sustainable, and pedestrian-friendly cities by addressing key research questions.
The primary research questions for this project are:
1. Does neighborhood walkability correlate with job-housing balance?
2. What is the impact of combining retail, office, and residential land use on walkability scores?
3. Is it possible to use traffic measures as a predictor for areas with high walkability?
4. Can we find a correlation between demographics, like auto ownership rates, and observed walkability?
5. In what ways do employment variables influence neighborhood walk scores?
   
1.4 Research Problem and Context
Our research problem arises from the necessity of unraveling the intricacies of urban walkability patterns and their relationship to diverse urban factors. While previous tries might have concentrated on factors, a complete comprehension is necessary to enhance urban walkability.

1.5 Stakeholders, Decision-Making, and Predictive Modeling
Walkability’s immense influence on quality of life, health, and economic vibrancy is recognized by key urban planning stakeholders, including legislators, city officials, and residents. Determining the functionality of urban space to enhance walkability is a complex process that requires considering urban planning, transportation, public health, and community development. To effectively analyze future walkability scores and highlight areas for improvement, the use of predictive modeling techniques is essential. Predictive modeling improves urban decision-making and enhances walkability by optimizing resources and strategies.

2. Research Study
Hauer et al. (2021) (Hauer, 2021)presented groundbreaking approaches to natural language processing by exploring sense annotation through translations, both in semi-supervised and unsupervised settings. While it may not be specifically focused on urban walkability, this study showcases how innovative approaches can be used to tackle intricate research challenges, reflecting the demand for creative solutions in urban planning.
2.1 Similar Problems
The literature review by De Vos et al. (2022) introduced a conceptual model and research agenda, aiming to deepen our understanding of perceived walkability. Through the synthesis of existing research and the proposal of future directions, this study presents a roadmap for addressing comparable challenges in urban walkability research. Hijriyah et al. (2023) utilized systematic literature review techniques to examine trends in walkability research, highlighting the significance of comprehensive methodologies in analyzing complex urban phenomena.
2.2 Conclusion
By examining the literature, we uncover the various facets of urban walkability and the potential of machine learning to address challenging real-world problems. This review establishes a foundation for empirical analysis in urban walkability research by integrating insights from urban planning theories, behavioral frameworks, and machine learning methodologies. This review carefully examines biases, limitations, and relevant studies to establish the framework for informed decision-making and future research in urban planning and machine learning integration.

3. Research Methods
The dataset was selected after careful evaluation for its relevance and comprehensiveness. The dataset from Data.gov provides comprehensive information on urban variables essential for analyzing pedestrian activity patterns. The dataset considers multiple indicators, such as administration, demographics, employment, density, diversity, design, transit access, and destination accessibility, to provide a well-rounded view of urban environments. The wide range of information makes it perfect for studying the complex connection between urban features and pedestrian behavior.
3.1 Data and Procedures
The dataset contains 117 variables, providing detailed information on urban characteristics such as population, housing, employment, land use, transportation, and accessibility. The analysis incorporates one dependent variable that reflects pedestrian activity levels and multiple independent variables. Geographic representation in diverse urban areas is ensured with the dataset covering all 50 states, Puerto Rico, and other territories. By utilizing this dataset, the research methodology aimed to streamline the analysis process and implement rigorous analytical techniques to address the research questions and extract meaningful insights effectively.

3.2 Analysis
The research employed a methodical analytical approach to derive useful findings from the data. The analysis process consisted of multiple important steps.
1. Data Pre-processing: The first step consisted of cleaning the dataset, removing inconsistencies, handling missing values, and ensuring data quality. Methods like imputation and outlier detection have been used to improve the dataset’s reliability.
2. Exploratory Data Analysis (EDA): Preliminary insights into the dataset’s characteristics were obtained through descriptive and visual analyses. This involved summarizing variable distribution, identifying patterns and trends, exploring correlations among variables, and visualizing spatial relationships through GIS tools.
3. Feature Engineering: We identified numeric features from the dataset and applied PCA to optimize the predictive modeling process by dealing with the multicollinearity problem faced above. The goal of PCA is to reduce the dimensionality of the dataset from 117 columns to 25 Principal components.
4. Model Selection: The choice of machine learning algorithms, including linear regression and artificial neural networks (ANN), was made considering the research objectives and dataset properties. Their proficiency influenced the choice of models in capturing and predicting pedestrian activity levels based on the independent variables. There is significant multicollinearity in the data, which we are going to deal with by using PCA.
5. Model Training: The prepared dataset was used to train the selected models to understand the connections between urban variables and pedestrian activity levels. To optimize performance, the training process involves fitting the models to the data and fine-tuning their parameters.
6. Model Evaluation: Evaluation of trained models involved the use of appropriate metrics, including Mean Squared Error (MSE) for regression tasks. The purpose of model evaluation is to ensure reliable and accurate analysis results by measuring predictive performance and identifying areas for improvement. The figure has Average Natwalkind and CBSA Names on the X and Y axis respectively.
7. Interpretation and Insights: The interpretation of the analysis results provided valuable insights into urban walkability and pedestrian behavior factors. The knowledge gained from these insights influenced efforts to create pedestrian-friendly environments through urban planning and policymaking. Furthermore, the researchers examined the implications of the findings within the context of existing literature and theoretical frameworks to ensure a thorough comprehension of the research outcomes.
The study aimed to provide valuable insights for urban planning, promoting informed decisions to improve walkability and create sustainable communities.
3.3 Methods used
1. Imputation: we have used imputation to deal with null values in our dataset. The nulls in all the numeric variables have been imputed with mean and categorical variables with mode. We have found that more than 90% of the values in "D4A", "D4C", "D4D", "D4E", "D5BR", "D5BE", "D5DR", "D5DRI", "D5DE", "D5DEI" are “-0.99999” which has been used as a place holder value in these columns. So, they have been dropped.
2. Correlation: We have checked for correlations in the independent variable to check for any interesting correlations and found some very interesting things like how as populations grow, so does the infrastructure to support job commuting by car and how as total employment raises, the workers earning more than $3333 also increases disproportionately which indicates a high influx of high paying jobs.
3. PCA: Since we have 117 variables originally, we needed to do some dimensionality reduction. We have considered Forward selection, Backward selection and Principle component analysis among which we ended up choosing PCA as it reduces the data leakage and deals with the multicollinearity problem we had with the dataset.
"PCA is a practical and valuable statistical technique that transforms large correlated data into small uncorrelated data using principal components (PCs) (Shang et al., 2017). PCs can be expressed as linear combinations of the original input variables, which retain the complete information of the original data."(Fan et al., 2024). Using PCA we have reduced our dataset to 25 columns.
Standard Scaling: Machine learning algorithms tend to give higher weightage to bigger numbers in the dataset no matter how insignificant they are so, to deal with this problem, we have scaled the entire dataset Using standardscaler() function from python which does the standardization by using the mean and standard deviation of each variable.
4. Linear Regression
We have chosen Linear regression as a baseline model for our analysis which fits a linear equation to the data and estimate coefficients to each variable depending on how much influence that independent variable has on the dependent variable.
5. Artificial Neural Networks
Building a shallow neural network to compare the performances of various activation functions has always been the core of our project. A neural network is a kind of model that is created to simulate the functioning of human brain consisting of neurons and nodes organized in layers.
For our analysis we have decided to use a shallow neural network because of the computational constraints with 1 hidden layer on which we will apply different activation functions and an output layer with one node with linear activation function which predicts the outcome.
6. Activation Functions used:
ReLU (Rectified Linear Unit):
Definition: If the input is positive, it comes from the input itself; If the input is negative, zero is the output.
LeakyReLU:
Definition: It is comparable to ReLU, but allows a slight, non-zero overhead when the input is less than zero and the unit is not operating.
PReLU (Parametric ReLU):
Definition: A variant of LeakyReLU where the leak coefficient are determined by training rather than by default.
RReLU (Randomized ReLU):
Definition: It is comparable to LeakyReLU, but with a random negative part slope during training and a fixed slope during testing.
SReLU (S-shaped ReLU):
Definition: Combining several blockwise linear functions yields an S-shaped function.
ELU (Exponential Linear Unit):
Definition: If the input is negative, negative gives an exponential decay to infinity; If input is positive, it generates only input.
PeLU (Parametric ELU):
Definition: ELU variant with parameters specifying the size of the output.
Selu (Scaled Exponential Linear Unit):
Definition: The ELU is scaled using a fixed scale factor to maintain accuracy.
Maxout:
Definition: It efficiently uses several affine functions to generalize ReLU without requiring a special method for nonlinearity.
ELiSH (Exponential Linear Sigmoid SquasHing):
Definition: Sigmoid-like output combined with ELU based on the range of inputs.
HardELiSH:
Definition: A piecewise linear approximation of ELiSH that sacrifices smoothness in order to be faster.
4. Data Analysis
Our data analysis is specifically focused on descriptive statistics and correlation analysis results, and we evaluated the performances using different activation functions in the Neural networks.
4.1 Descriptive Statistics
Descriptive Statistics provided an understanding of the size, structure, and data types. Used data.describe() for understanding the statistical details such as mean, minimum value, maximum value, and standard deviation.
The key components are count, mean, standard deviation, minimum, maximum values, and percentiles:
1. The count showed the number of non-null values per variable, this indicates that there are no missing values and the missing values have been filled up using the mode value.
2. Mean provided the information of the average value of each variable and this information gave he central tendency insights.
3. Standard deviation suggests the number of variations happening around the mean values. The data points are spared out in a wide range as we have a high range of std.
4. The minimum and maximum values helped us understand the range within the data variers and this has been calculated for each column.
5. The 25th, 50th, and 75th percentile of each column helped in understanding the data distribution. And median which is the 50th percentile provided the midpoint information. Overall, this information gave insights into the first quartile, median, and third quartile.
4.2 Analysis based on the Descriptive Statistics
1. Urban Planning and Economical Analysis, here we compared the demographical and economic variables for understanding urban planning and policymaking. Some of the variables used are TotPop, Workers, and R_LowWageWk.
2. Socio-economic research factors helped to analyze the correlation between the economic and demographic factors to identify the trends and potential area trends. Some of the variables used are AutoOwn0, Shape_Length, Shape_Area and D2A_JPHH
3. Geographical Analysis helped us understand the patterns related to development, land density, population, and employment distribution. Some of the variables used are GEOID10 and STATEFP.
4.3 Correlation Analysis
Correlation Analysis is a critical part of our analysis. It provided insights into how the different variables in the walk wise are related to each other. Overall, we have strong correlations in terms of the target variable for predicting the model. The stronger correlations are identified by seeing the red blocks which are directly related to each other, more populations and employment variables showed up in this area. The negative correlation is seen in the blue area of the graph, and we can see no correlation or weaker correlation on the white or light blue part of the graph.
In the overall analysis, we can see a strong correlation with the target variable which is the net walkability index which we used for prediction. This heatmap also identified that multicollinearity can be shown as a problem.
The limitation of Correlation analysis is the graph only showed the linear relationship of the model, which can show us how strong that matrix is and how the positive pattern is shown in the graph. The major con is, that overall can identify the variable which indicates that the graph is clumsy and messy as we have a larger dataset.
4.4 Visualization
After EDA we have included a few scatter plots, which determined the relationship between variables, and we have given the threshold of 0.6 we got about 160 graphs showing the different relations and analyses among all we have a few interesting scatter plots that are listed below.
1. Relation between CBSA_POP and D5AR - Total population in CBSA.
The scatter plots show the relation between the Total population in CBSA and Jobs within 45 minutes of auto travel time. We can see that they are highly correlated with 0.794, by this we can explain the accessibility of jobs with 45 minutes of travel time is good and This indicates that as the population increases the infrastructure for the travel or commute is also growing.
2. Relation between Ac_Total and Ac_Land - Total geometric area of the CBG and Total land area.
The relation between the Total geometric area of the CBG and the Total land area has a correlation of 0.986 which is good enough to explain the area measures and the proportion of land and non-land areas.
3. Relation between TotPop and Workers - Count of low-wage workers and Count of high-wage.
The relation between Total Population and Count of workers in CBG has an interesting plot with 0.874 as a correlation, this highlights the economic activity of the population.
4. Relation between R_LowWageWk and R_HiWageWk - Total Population and Count of workers in CBG.
The Count of low-wage workers and Count of high-wage workers relation explains the geographic area wage differences, this shows the mixed economic structure for development and the correlation is 0.751. 
5. Relation between TotEmp and E_HiWageWk - Total Employment and the number of workers earning.
The relation between Total Employment and the number of workers earning $3333/month or more is highly correlated with 0.9605 which indicates that high-paying jobs are on the rise.
6. Relation between D2B_E5MIX and D2B_E8MIX - complexity of job markets in the different locations.
The 5-tier employment entropy and 8-tier employment entropy correlate 0.882 which explains the complexity of job markets in the different locations.
Research Question 1: Does neighborhood walkability correlate with job-housing balance?
7. Scatter plot of NatWalkInd vs. D2R_JOBPOP
From the scatter plot of NatWalkInd vs. D2R_JOBPOP, the two variables have a slightly positive to no correlation. In other words, it means that when the ratio of jobs to population is high, the walkability score is likely to be high. Areas in which they have more jobs than people living in them could possibly have better walkability due to amenities supporting workers and residents in this regard.
Research Question 2: What is the impact of combining retail, office, and residential land use on walkability scores?
D3BMM3 versus NatWalkInd:
There is a positive correlation between D3BMM3 and NatWalkInd. As D3BMM3 increases, indicating a denser mix of residential, multifamily, and commercial uses, the NatWalkInd score also tends to increase. This suggests that areas with a higher mix of residential and commercial functions are more likely to have better walkability, probably due to the availability of various amenities and services close to dwellings.
D3BMM4 versus NatWalkInd:
Similar to D3BMM3, D3BMM4 shows a positive correlation with NatWalkInd. As D3BMM4 increases, which indicates a higher mix of office and commercial uses, the NatWalkInd score also tends to increase. This indicates that areas zoned with a combination of office and commercial uses are likely to be more walkable, due to the presence of workplaces, shops, and services that attract foot traffic.
D3BPO3 versus NatWalkInd:
Unlike the first two plots, there is no clear correlation between D3BPO3 and NatWalkInd. The scatterplot shows a more dispersed pattern, suggesting that the mix of public open space and recreation areas does not consistently impact walkability scores. This implies that other factors,
such as the quality and accessibility of public spaces, may play a more significant role in determining walkability.
Research Question 3: Is it possible to use traffic measures as a predictor for areas with high walkability?
Traffic Measure 1 vs. NatWalkInd:
- Traffic Measure 1 has a positive correlation with NatWalkInd.
- As Traffic Measure 1 increases, the NatWalkInd score also tends to increase. This suggests that areas with higher traffic measurements, such as traffic volume or density, are likely to have better walkability. This could be due to more transportation options available, including public transit and bike lanes, making walking a preferred option.
Traffic Measure 2 vs. NatWalkInd:
- Similarly, NatWalkInd shows a positive relationship with Traffic Measure 2.
- As Traffic Measure 2 increases, the NatWalkInd score also increases. This suggests that areas with higher traffic measures, such as greater traffic congestion or delay, may have better walkability. In these areas, the presence of mixed-use development and pedestrian-friendly infrastructure likely makes walking more convenient and enjoyable.
Research Question 4: Can we find a correlation between demographics, like auto ownership rates, and observed walkability? Correlation between demographics
There is no clear correlation between auto correlation rates and walkability. This would suggest that factors like accessibility to public transportation and a quality built environment may be very strong determinants in walkability for regions with greater auto ownership rates.

Research Question 5: How does the usage of various activation functions affect metrics such as error(MSE and MAE), R-Squared, Adj R-Squared when applied on a shallow neural network. 
The activation function of neural networks determines the output of a node in the neural network. It plays a crucial role in setting the smoothness of the fitting curve that predicts the output. Metrics such as mean square error (MSE), mean absolute error (MAE), R-square error (R2), adjusted R-square can be used to evaluate the efficiency of the neural network model when using different activation functions. We analyzed the impact of the implementation of these functions using the metrics provided:
Mean Squared Error (MSE):
In the model we can see that the MSE is low which indicates that its shows a smaller average squared error while comparing the actual and predicted values. Based on the graphs, we can say that ReLU, LeakyReLU, PReLU, RReLU, SReLU are performing well, where ad RRelu is showing the lower values of MSE. Thus, RRelu is on average and closer to the true value.
Mean Absolute Error (MAE):
The MAE value is also low, which indicates that the predicted values are closer to the actual values. The RRelu function performs the best metrics with few errors on average without deviations squaring.
R-Squared (R²):
The R-Squared shows the proportion of variances for the dependent variables which explains the independent variables in regression model. The higher the R-Squared the more variance which gives us a desirable model. In most activation functions R-Squared is mostly similar and in RRelu we can see a slight edge. Overall, we can say that different activation functions are relatively comparable.
Adjusted R-Squared:
This will modify the R-Squared values to predict the model. The higher the better measures which gives us a good model. Here we can again see that RRelu has the higher value which indicated the predicted values and perform robust.
In summary, the RReLU activation function appears to perform well for shallow neural networks in all given metrics, based on the given data if the adjusted R2 shows a larger percentage of captures it is a variance that is not too normal, thus balancing the bias-variance trade-off. Variants such as ReLU also perform well, consistent with the literature. This is because ReLU-type functions, due to their computational efficiency and gradient propagation properties, are well known to train effective deep correlations.

5. Conclusions and Recommendations
Conclusions:
In Conclusion, our study investigates the intricate relationship between urban walkability and various socioeconomic and urban planning factors with the help of machine learning. We have identified the main features of the scrutinized dataset that reveal the most relevant information related to pedestrian behaviour and determinants of walkability in urban areas. The major correlations our findings pointed out are related to the factors of job-housing balance, land use diversity, traffic measures, demographics, and employment variables; they thus influence walkability scores. To use descriptive statistics, correlation analysis, and visualization techniques to tease out patterns and trends within urban data with the intent of providing subtle perspectives back to the urban planner and policymaker. Besides, the model was used to generate a predictive model analysis framework, which is improving the understanding of pedestrian activity levels in making urban planning decisions. Our results strive to contribute toward the search for vibrant, sustainable, pedestrian-friendly cities by trying to bridge the gap between theoretical and practical application. Thus, based on these insights, the current discussion moves forward to provide a guide for designing interventions and policies that foster walkable urban environments in the name of healthier and more livable communities for all residents.
