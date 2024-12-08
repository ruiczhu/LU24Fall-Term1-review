# CDS535 DataMining
- The exam has 9 Questions
- Data contains value and knowledge

## 1. What is Data Mining?

### 1. Definition of Data Mining
- Non-trivial extraction of implicit, previously unknown and potentially useful information from data
- Exploration & analysis, by automatic or semi-automatic  means, of large quantities of data in order to discover  meaningful patterns
- ![image.png](image.png)

### 2. Data Science compared to Data Mining
**Business Understanding**
- Seldom pre-packaged as clear data science problems.
- Creative problem formulation is needed to consider the  business problem as one or more data science problems.
- High-level knowledge of the domains helps creative Data
- Scientists/Business Analysts see novel formulations.
- The design team should think carefully about the problem to  be solved and about the user scenario.

**Data Understanding**
- Understand the strengths and limitations of the data.
- Historical data often are collected for other purposes unrelated  to the current data science problem.

**Data Preparation**
- Many data science/data mining algorithms require data to be in a specific form (e.g. Table format).
- Some conversion will be necessary.
- Missing values should be handled.
- 
**Modeling**
- Apply data science/data mining algorithms to create  models/data science results from the data

**Evaluation**
- Assess the data science results.
- Gain confidence that they are correct and reliable.
- Test the results (models) in a controlled laboratory setting.
- Ensure that the model satisfies the original business goals.

**Deployment**
- The data science results (models) are used in real problems  (e.g. fake detections).
- Implement it in some information system or business process.
- Deploy a model into a production system typically requires  that the model be re-coded for the production environment  (e.g. program in Windows environment).

![image_2.png](image_2.png)

### 3. Data Mining Process
![image_3.png](image_3.png)

## 2. Data Mining Tasks
**Prediction Methods**
- Use some variables to predict unknown or  future values of other variables.

**Description Methods**
- Find human-interpretable patterns that  describe the data.

二、过程与步骤
- Prediction Methods（预测方法）
- 数据收集：收集与预测目标相关的历史数据。 
- 数据预处理：清洗数据、处理缺失值、标准化等。 
- 特征选择：选择对预测目标有影响的特征。 
- 模型训练：使用训练数据集训练预测模型。 
- 模型验证：使用验证数据集验证模型的准确性。 
- 预测：使用训练好的模型对未知数据进行预测。


- Description Methods（描述方法） 
- 数据收集：收集与目标问题相关的数据。 
- 数据探索：通过可视化、统计等方法初步了解数据。 
- 模式发现：运用数据挖掘技术发现数据中的模式、关联和异常等。 
- 模式解释：以人类可理解的方式解释发现的模式。 
- 结果呈现：通过图表、报告等形式呈现描述结果。

三、应用实例
- Prediction Methods（预测方法） 
- 金融领域：预测股票价格、汇率、信用风险等。 
- 销售领域：预测销售额、市场份额、客户行为等。 
- 医疗领域：预测疾病发生率、治疗效果、患者预后等。

- Description Methods（描述方法） 
- 市场研究：描述消费者行为、市场趋势等。 
- 社会科学：描述社会现象、人类行为等。 
- 生物信息学：描述基因表达、蛋白质结构等。

- Classification [Predictive]
- Clustering [Descriptive]
- Association Rule Discovery [Descriptive]  
- Sequential Pattern Discovery [Descriptive]  
- Regression [Predictive]
- Deviation Detection [Predictive]

![image_4.png](image_4.png)

## 3. Predictive Modeling

### 1. predictive modeling: classification
- Find a model	for class attribute as a function of the values of other attributes

### 2. predictive modeling: regression
- Predict a value of a given continuous valued variable based on the values of other variables, assuming a linear or nonlinear model of dependency. 
- Extensively studied in statistics, neural network fields.

### 3. predictive modeling: clustering
- Finding groups of objects such that the objects in a
group will be similar (or related) to one another and
different from (or unrelated to) the objects in other
groups

#### 1. K-means Clustering
- Partitional clustering approach 
- Number of clusters, K, must be specified 
- Each cluster is associated with a centroid (center point) 
- Each point is assigned to the cluster with the closest
centroid 
- The basic algorithm is very simple
![image_5.png](image_5.png)

#### 2. Two different K-means Clusterings
- Optimal Clustering（最优聚类）
- Sub-optimal Clustering（次优聚类）

#### 3. Importance of Choosing Initial Centroids 


### 4. Association Rule Discovery: Definition
- Given a set of records each of which contain
some number of items from a given collection
– Produce dependency rules which will predict
occurrence of an item based on occurrences of other
items.

#### 1. Association Analysis: Applications

- Market-basket analysis 
  - Rules are used for sales promotion, shelf management, and inventory management

- Telecommunication alarm diagnosis 
  - Rules are used to find combination of alarms that  occur together frequently in the same time period

- Medical Informatics 
  - Rules are used to find combination of patient  symptoms and test results associated with certain  diseases

## 4. Data Preprocessing

### 1. Outliers
### 2. Missing Values
### 3. Duplicate Data

<note>本章具体内容见以下链接</note>

[](#8-data-quality)

[](#9-data-preprocessing)

## 5. Decision Trees

### 1. Test Condition for Nominal Attributes
- Multi-way split:
- Use as many partitions as distinct values.

- Binary split:
- Divides values into two subsets

![image_6.png](image_6.png)

### 2. Test Condition for Ordinal Attributes
- Multi-way split:
- Use as many partitions as distinct values

- Binary split:
- Divides values into two subsets
- Preserve order property among attribute values

![image_7.png](image_7.png)


### 3. Test Condition for Continuous Attributes
![image_8.png](image_8.png)

## 6. Model Evaluation

### 1. Metrics for Performance Evaluation
<tip>IMPORTANT!!!</tip>

![image_9.png](image_9.png)

### Confusion Matrix 混淆矩阵
|                 | Predicted Positive  | Predicted Negative  |
|-----------------|---------------------|---------------------|
| Actual Positive | True Positive (TP)  | False Negative (FN) |
| Actual Negative | False Positive (FP) | True Negative (TN)  |

#### 1. Accuracy 准确率
Accuracy表示分类器正确分类的样本比例。

$
\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
$

#### 2. Precision 精确率
Precision表示被预测为正类的样本中实际为正类的比例。

$
\text{Precision} = \frac{TP}{TP + FP}
$

#### 3. Recall (Sensitivity) 召回率（灵敏度）
Recall表示实际为正类的样本中被正确预测为正类的比例。

$
\text{Recall} = \frac{TP}{TP + FN}
$

#### 4. F-measure (F1-score)
F-measure是Precision和Recall的调和平均值。

$
\text{F-measure} = 2 \times\frac{ \text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
$

#### 5. Specificity 特异性
Specificity表示实际为负类的样本中被正确预测为负类的比例。

$
\text{Specificity} = \frac{TN}{TN + FP}
$

#### 6. Sensitivity (Recall) 灵敏度（召回率）
Sensitivity与Recall相同，表示实际为正类的样本中被正确预测为正类的比例。

$
\text{Sensitivity} = \frac{TP}{TP + FN}
$

#### 7. False Positive Rate (FPR) 假阳性率
FPR表示实际为负类的样本中被错误预测为正类的比例。

$
\text{False Positive Rate} = \frac{FP}{TN + FP}
$

### 2. Limitation of Accuracy

### 3. Computing Cost of Classification

## 7. Data
- **Data:** Collection of data objects and their attributes
- **Attribute Values:** Attribute values are numbers or symbols assigned
  to an attribute
  - Distinction between attributes and attribute values
    - Same attribute can be mapped to different attribute
      values
    - Different attributes can be mapped to the same set of
      values 

### 1. Types of Attributes

| Property       | Symbol | Nominal | Ordinal | Interval | Ratio |
|----------------|--------|---------|---------|----------|-------|
| Distinctness   | = !=   | ✅       | ✅       | ✅        | ✅     |
| Order          | < >    |         | ✅       | ✅        | ✅️    |
| Addition       | + -    |         |         | ✅        | ✅️    |
| Multiplication | * /    |         |         |          | ✅     |

| Attribute Type  | Description                                                                | Examples                                                                       | Operations                                                     | Transformation                                                                                      | Comments                                                                                                                               |
|-----------------|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Categorical** |                                                                            |                                                                                |                                                                |                                                                                                     |                                                                                                                                        |
| Nominal         | Nominal attribute values only distinguish. (=, ≠)                          | zip codes, employee ID numbers, eye color, sex: {male, female}                 | mode, entropy, contingency correlation, χ² test                | Any permutation of values                                                                           | If all employee ID numbers were reassigned, would it make any difference?                                                              |
| Ordinal         | Ordinal attribute values also order objects. (<, >)                        | hardness of minerals, {good, better, best}, grades, street numbers             | median, percentiles, rank correlation, run tests, sign tests   | An order preserving change of values, i.e.,new_value = f(old_value) where f is a monotonic function | An attribute encompassing the notion of good, better, best can be represented equally well by the values {1, 2, 3} or by {0.5, 1, 10}. |
| **Numeric**     |                                                                            |                                                                                |                                                                |                                                                                                     |                                                                                                                                        |
| Interval        | For interval attributes, differences between values are meaningful. (+, -) | calendar dates, temperature in Celsius or Fahrenheit                           | mean, standard deviation, Pearson's correlation, t and F tests | new_value = a * old_value + b where a and b are constants                                           | Thus, the Fahrenheit and Celsius temperature scales differ in terms of where their zero value is and the size of a unit (degree).      |
| Ratio           | For ratio variables, both differences and ratios are meaningful. (*, /)    | temperature in Kelvin, monetary quantities, counts, age, mass, length, current | geometric mean, harmonic mean, percent variation               | new_value = a * old_value                                                                           | Length can be measured in meters or feet.                                                                                              |

### 2. Discrete and Continuous Attributes

#### Discrete Attribute 离散属性
- Has only a finite or countably infinite set of values
- Examples: zip codes, counts, or the set of words in a collection of documents
- Often represented as integer variables
- Note: binary attributes are a special case of discrete attributes

#### Continuous Attribute 连续属性
- Has real numbers as attribute values
- Examples: temperature, height, or weight
- Practically, real values can only be measured and represented using a finite number of digits
- Continuous attributes are typically represented as floating-point variables

### 3. Asymmetric Attributes
- Only presence (a non-zero attribute value) is regarded as
  important.

### 4. Critiques of the Attribute Categorization

#### Incomplete
- Asymmetric binary
- Cyclical (e.g., position on the surface of the Earth, Time)
- Multivariate (e.g., set of movies seen)
- Partially ordered
- Partial membership
- Relationships between the data

#### Real Data is Approximate and Noisy
- This can complicate recognition of the proper attribute type.
- Treating one attribute type as another may be approximately correct.

### 5. Key Messages for Attribute Types

#### Meaningful Operations
- The types of operations you choose should be "meaningful" for the type of data you have.
  - Distinctness, order, meaningful intervals, and meaningful ratios are only four (among many possible) properties of data.
  - The data type you see—often numbers or strings—may not capture all the properties or may suggest properties that are not present.
  - Analysis may depend on these other properties of the data.
    - Many statistical analyses depend only on the distribution.
  - In the end, what is meaningful can be specific to the domain.

### 6. Important Characteristics of Data

- **Dimensionality (number of attributes)**
  - High dimensional data brings a number of challenges

- **Sparsity**
  - Only presence counts

- **Resolution**
  - Patterns depend on the scale

- **Size**
  - Type of analysis may depend on size of data

### 7. Types of Data Sets

<tip>详情见 Data_Mining_week2_slides.pdf</tip>

#### Record
- **Data Matrix**
- **Document Data**
- **Transaction Data**

#### Graph
- **World Wide Web**
- **Molecular Structures**

#### Ordered
- **Spatial Data**
- **Temporal Data**
- **Sequential Data**
- **Genetic Sequence Data**

### 8. Data Quality
- Poor data quality negatively affects many data processing
  efforts
- Quality issues include:
  - Noise
    - For objects, noise is an extraneous (無關) object
    - For attributes, noise refers to modification of original values
  - Outliers
    - Outliers are data objects with characteristics that
      are considerably different than most of the other
      data objects in the data set
  - Wrong data
  - Fake data
  - Missing values
    - Reasons for missing values
      - Information is not collected
      - Attributes may not be applicable to all cases
    -  Handling missing values
        - Eliminate data objects or variables
        - Estimate missing values
        - Ignore the missing value during analysis
  - Duplicate data
    - Data set may include data objects that are
      duplicates, or almost duplicates of one another

### 9. Data Preprocessing
#### 1. Aggregation
  - Combining two or more attributes (or objects) into a single
    attribute (or object)
  - Purpose
    - Data reduction - reduce the number of attributes or objects
    - Change of scale
      - Cities aggregated into regions, states, countries, etc.
      - Days aggregated into weeks, months, or years
    - More “stable” data - aggregated data tends to have less variability
#### 2. Sampling 
  - Sampling is the main technique employed for data
    reduction.
    - It is often used for both the preliminary investigation of
      the data and the final data analysis.
  - Statisticians often sample because obtaining the
      entire set of data of interest is too expensive or
      time consuming.
  - Sampling is typically used in data mining because
      processing the entire set of data of interest is too
      expensive or time consuming.
  - The **key principle** for effective sampling is the
    following:
    - Using a sample will work almost as well as using the
    entire data set, if the sample is representative
    - A sample is representative if it has approximately the
    same properties (of interest) as the original set of data

    - **Simple Random Sampling**
    - There is an equal probability of selecting any particular item.

      - **Sampling without replacement**
      - As each item is selected, it is removed from the population.

      - **Sampling with replacement**
      - Objects are not removed from the population as they are selected for the sample.
      - In sampling with replacement, the same object can be picked up more than once.

    - **Stratified sampling**
    - Split the data into several partitions; then draw random samples from each partition.


#### 3. Discretization 
- Discretization is the process of converting a
continuous attribute into an ordinal attribute
  - A potentially infinite number of values are mapped into
  a small number of categories
  - Discretization is used in both unsupervised and
  supervised settings
- Unsupervised Discretization
  - Equal interval width (distance) partitioning
  - Equal-frequency (frequency) partitioning
  - K-means
- Supervised Discretization
  - Discretization is based on class labels
  - The goal is to find partitions that minimize the
  entropy (or maximize the purity) of the classes in
  each partition

#### 4. Binarization
- Binarization maps a continuous or categorical
  attribute into one or more binary variables

#### 5. Attribute Transformation 
- An attribute transform is a function that maps the
  entire set of values of a given attribute to a new
  set of replacement values such that each old
  value can be identified with one of the new values

- Simple Functions

  - Power Function (幂函数):
  $x^k$
  - Logarithmic Function (对数函数):
  $log(x)$
  - Exponential Function (指数函数):
  $ e^x $
  - Absolute Value Function (绝对值函数):
  $|x|$

- Normalization
  - Refers to various techniques to adjust to
  differences among attributes in terms of frequency
  of occurrence, mean, variance, range
  - Take out unwanted, common signal, e.g.,
  seasonality
- In statistics, standardization refers to subtracting off
the means and dividing by the standard deviation

#### 5. Dimensionality Reduction 

- Curse of Dimensionality
  - Many types of data analysis become significantly harder as
    the dimensionality of the data increases
  - When dimensionality increases, data becomes increasingly
  sparse in the space that it occupies
  - Definitions of density and distance between points, which
  are critical for clustering and outlier detection, become less
  meaningful

- Purpose of Dimensionality Reduction:
  - Avoid curse of dimensionality
  - Reduce amount of time and memory required by data
  mining algorithms
  - Allow data to be more easily visualized
  - May help to eliminate irrelevant features or reduce
  noise
- Techniques
  - Principal Components Analysis (PCA)
  - Singular Value Decomposition
  - Others: supervised and non-linear techniques

#### 6. Feature subset selection 
- Another way to reduce dimensionality of data 
- Redundant features 
  - Duplicate much or all of the information contained in
  one or more other attributes 
  - Example: purchase price of a product and the amount
  of sales tax paid 
- Irrelevant features 
  - Contain no information that is useful for the data
  mining task at hand 
  - Example: students' ID is often irrelevant to the task of
  predicting students' GPA 
- Many techniques developed, especially for
classification

#### 7. Feature creation
- Create new attributes that can capture the
  important information in a data set much more
  efficiently than the original attributes
- Three general methodologies:
  - Feature extraction
  - Feature construction
  - Mapping data to new space



