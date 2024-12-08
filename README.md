# Ques4
[22CA682DR.pdf](https://github.com/user-attachments/files/18053199/22CA682DR.pdf)




### **Question 1**

**(i) Describe the shape of the histogram below in terms of the modality. [2 marks]**
![image](https://github.com/user-attachments/assets/7780fd76-207d-4ca8-9f6c-0d6a2adacb99)

Answer: The histogram is **unimodal**, as it has a single peak or mode.

---

**(ii) If I'm creating a frequency table from a discrete variable (e.g., the count of current primary toothbrush colours for CA682 students), what could the values in the first column be? [2 marks]**  
Fig ? Frequency
? 100
? 52
? 23
? 40

Answer: The values in the first column could be **categories of toothbrush colours** (e.g., Blue, Red, Green, Yellow, etc.).

---

**(iii) Which of the following histograms (A-D) displays positive skewness? [3 marks]**

Answer: Histogram **D** displays positive skewness, as it has a longer tail on the right side.
![image](https://github.com/user-attachments/assets/e258a02c-f05f-49d3-8475-6ce9d78e9573)

---

**
![image](https://github.com/user-attachments/assets/394e18cc-168d-414e-b814-40a149dffce1)
The figure above was created to show the distribution of patients with a particular
long term medical condition that is being treated with three different therapies (A, B &
C) according the county where the therapy is administered. The median age of
patients in each county is also included.

(i) What type of visualisation is this (specific name)? What are the marks and attributes used to encode the data? [3 marks]**

Answer: The visualisation is a **bubble chart**.  
- **Marks:** Circles (bubbles).  
- **Attributes:** Size of bubbles represents frequency; position encodes counties; color represents therapy type.

---

**(ii) Identify any issues with preserving the privacy of patients that this graph may raise? [3 marks]**

Answer: Privacy issues include potential identification of patients based on small sample sizes in specific counties, especially when combined with other demographic data like median age.

---

**(iii) The graph is released in a report that also includes further aggregated information such as the date of diagnosis, blood type, gender, and ethnicity of the patient by county. Comment on the likely risks associated with this report and suggest two methods that may be used to reduce the privacy risks. [4 marks]**

Answer:  
- **Risks:** Combining multiple datasets increases re-identification risk. Sensitive data like blood type and ethnicity can make individuals identifiable.  
- **Methods to reduce risks:**  
  1. Aggregate data further (e.g., group counties or age ranges).  
  2. Apply differential privacy techniques to anonymize data.

---

**You are asked to create a visualisation to show 120 first-year students so they can understand their comparative performance across all modules. Suggest a method for communicating the information that would be privacy-preserving and discuss any potential risks that should be considered.**

Student ID Student Name CA100 CA105 CA121 CA167
123456789 Alex Smith 64% 72% 56% 85%


Answer: Use a **box plot** for each module to show performance distributions without revealing individual scores.  
- **Risks:** Outliers may reveal individual performance if scores are unique or extreme. Ensure anonymization by grouping or removing outliers.

---

### **Question 2**

<img width="1470" alt="Screenshot 2024-12-08 at 10 20 50 PM" src="https://github.com/user-attachments/assets/aee41adc-12f5-48e9-b089-bacd24577c21">


2(a) Given the following brief to design a system for a data collection and storage
(preservation) task:
“Your client runs a chain of 10 gift shops across the UK and Ireland and
wants to integrate the inventory and sales data from all stores to a central
system. This includes data such as product id, description, unit price, etc.
and daily sales transactions from each shop.”

**(i) List three (3) important questions you would ask your client about their data storage requirements.**

Answer:  
1. What is the expected volume of data, both current and future?  
2. Are there specific compliance requirements like GDPR?  
3. How frequently will data need to be accessed or updated?

---

**(ii) Suggest a type of data storage approach to use for this project, giving a reason for your choice.**

Answer: Use a **relational database management system (RDBMS)** like MySQL or PostgreSQL for structured inventory and sales data due to its reliability and ability to handle transactions efficiently.

---

**(iii) The client now wants to include website logs and social media content interactions to work on future promotions. Would this change your recommendation? Why/Why not?**

Answer: Yes, this changes the recommendation. A **NoSQL database** like MongoDB or Elasticsearch would be better suited for unstructured data like logs and social media interactions due to its scalability and flexibility.

---

2(b)**(i) Give three (3) examples of simple metadata describing your favourite item of clothing.**

Answer:  
1. Color: Blue (Descriptive).  
2. Material: Cotton (Descriptive).  
3. Size: Medium (Structural).

---

**(ii) For each metadata element, identify if it is Descriptive, Administrative or Structural and briefly explain why.**

Answer:  
1. Color - Descriptive: Provides information about physical appearance.  
2. Material - Descriptive: Describes what it is made of.  
3. Size - Structural: Defines how it fits within categories like Small/Medium/Large.

---

**(iii) If I was to collect and integrate data about the favourite item of clothing of all CA682 students then, in your own words, how would using a standard specifically change the quality of metadata? Identify one potential difficulty with enforcing a metadata standard.**

Answer: Using a standard improves consistency, interoperability, and accuracy in metadata collection across datasets. However, enforcing standards can be difficult due to varied interpretations or lack of adherence by contributors.

---

**Q 2(c): Given the information in your brief in Q2(a), including social media data, identify any possible data that may need to be handled differently due to European GDPR requirements. Explain why or why not. [6 Marks]**

Answer: Social media interactions may include personal identifiers like usernames or comments linked to individuals, which fall under GDPR’s definition of personal data requiring consent for processing.

---
### **Question 3**
<img width="1470" alt="Screenshot 2024-12-08 at 10 19 32 PM" src="https://github.com/user-attachments/assets/2ca8f18e-d1a8-4ce6-8049-b32af7b2aa7a">

#### **(a) Identify four (4) different possible errors or artefacts in the dataset linked above, giving the column name and cell reference if appropriate.**

Answer:  
1. **Missing Data**: Some cells in the "Production (Tonnes)" column may have blank values (e.g., Row 15, Column 3).  
2. **Outliers**: Extremely high or low values in the "Production (Tonnes)" column that deviate significantly from the average (e.g., a value of 1,000,000 for a small country).  
3. **Inconsistent Formatting**: Dates in the "Year" column might be in different formats (e.g., '2020' vs. '20/20').  
4. **Duplicate Entries**: Repeated rows for the same country and year combination.

Tool: Microsoft Excel or Python's Pandas library.

---

#### **(b) Identify how each error or artefact in Q3(a) is most likely to have been introduced, specifying the phase from the generic data analytics pipeline. State any assumptions.**

Answer:  
1. **Missing Data** - Introduced during the *Gathering* phase due to incomplete data collection from sources.  
2. **Outliers** - Introduced during the *Processing* phase due to errors in manual data entry or system glitches.  
3. **Inconsistent Formatting** - Introduced during the *Gathering* phase when data is collected from multiple sources with varying formats.  
4. **Duplicate Entries** - Introduced during the *Processing* phase due to merging datasets without proper deduplication.

---

#### **(c) What data quality methods would you suggest using to either avoid or mitigate the errors or artefacts in this dataset? Why would your suggestion improve overall data quality?**

Answer:  
1. **Missing Data**: Use imputation techniques (e.g., replacing missing values with averages or medians) to fill gaps and maintain dataset integrity.  
2. **Outliers**: Perform outlier detection using statistical methods like Z-scores or interquartile range (IQR) and either remove or verify them for accuracy.  
3. **Inconsistent Formatting**: Apply standardization tools (e.g., Python's datetime library) to ensure uniform date formats across all entries.  
4. **Duplicate Entries**: Use deduplication algorithms to identify and remove repeated rows.

These methods improve data quality by ensuring consistency, completeness, and reliability of the dataset.

---

### **Question 4**
4(a)You are asked to plan a data analytics project to analyse student feedback
to DCU in relation to online teaching in 2020 and 2021. Using the Generic
Data Analytics Pipeline discussed in CA682, assign each of the following
activities to one of the 5 main categories: Gathering, Processing,
Analysing, Presenting and Preserving and identify a tool or application that
you might use (same one can be used for multiple tasks).

**(i): Assign activities to Generic Data Analytics Pipeline categories and tools used:**

| Activity | Category | Tool |
|----------|----------|------|
| Documenting formats | Preserving | Excel |
| Removing incorrect entries | Processing | Python |
| Liaising with Registry | Gathering | Email |
| Calculating averages | Analysing | R |
| Anonymising comments | Processing | Python |
| Converting words into sentiment ratings | Analysing | NLP Toolkit |
| Conducting surveys | Gathering | Google Forms |
| Creating summary documents | Presenting | PowerPoint |


**(ii): Identify a weakness with Generic Data Analytics Pipeline.**

Answer: It does not explicitly include feedback loops for iterative improvements during analysis phases.

4(b) For each of the following data attributes (A-D), choose all descriptions that apply (Qualitative, Quantitative, Discrete, Continuous, Nominal, Ordinal, Interval, Ratio):**

| Attribute | Descriptions |
|-----------|--------------|
| A: Rating of temperature comfort in offices | Qualitative, Ordinal |
| B: Number of times a character's name is used in a TV show episode | Quantitative, Discrete |
| C: Names of pets owned by all CA682 students | Qualitative, Nominal |
| D: All winning times (in seconds) for men's 100m sprint at the Olympic Games | Quantitative, Continuous, Ratio |

---

4 (c) Choose one scenario and explain why it is/is not a good example of "big" data according to classical characteristics (Volume, Velocity, Variety):**

**Scenario A: Customer account, purchasing data and engagement data from a supermarket chain's loyalty card programme**

Answer: This is a good example of "big" data because:  
- **Volume**: The dataset involves large-scale customer transactions and engagement logs across multiple stores over time.  
- **Velocity**: Data is generated continuously as customers make purchases and interact with loyalty programs in real time.  
- **Variety**: It includes structured transactional data (e.g., purchase history), semi-structured engagement logs (e.g., clickstream), and unstructured feedback/comments.

Assumption: The supermarket chain operates on a large scale with numerous customers.

---

### **Question 5**

#### **(a) Identify three possible improvements to the graph below and justify your choices referencing design rules/theories:**
![image](https://github.com/user-attachments/assets/c806aaba-2cdb-4d21-b3dc-98fcc00a8e0e)


1. **Improve Labeling**: Add clear axis labels for better understanding of what each axis represents (e.g., "Time" on X-axis and "Expenditure (€)" on Y-axis). This follows Tufte's principle of clarity.
2. **Use Color Coding or Grouping**: Differentiate categories using distinct colors or patterns to improve visual distinction and accessibility.
3. **Simplify Design**: Remove unnecessary gridlines or visual clutter to focus attention on key trends/data points.

---

#### **(b) Suggest an appropriate graph type for each visualisation task and justify your choice:**

| Task | Graph Type | CHRTS Category | Justification |
|------|------------|----------------|---------------|
| A: Compare performance of stocks in Microsoft, Apple, and Samsung over 5 years | Line Chart | Trend | Line charts are ideal for showing changes over time across multiple series. |
| B: Explore movie commercial performance for IMDB top 50 by director based on cost to make and ticket sales | Scatter Plot with Bubble Size | Relationship | A scatter plot can show relationships between cost and sales while bubble size represents additional metrics like profit margin.|

---

5 (c) Answer questions relating to the graphic shown below:**  
![image](https://github.com/user-attachments/assets/ad32d145-7d75-46d6-9453-6e582cebfb2b)

1. **What is the main communication purpose and why?**  
   Answer: The main purpose is to compare categories visually through size differences in shapes (e.g., bars or bubbles). This helps highlight disparities effectively.

2. **What design choices or guidelines have been used to support this purpose?**  
   Answer: The use of distinct colors for categories enhances differentiation; proportional sizing ensures accurate representation of values.





