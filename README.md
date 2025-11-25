# **MixITup Customer Segmentation Using Clustering Analysis**

## **Overview**

This project performs customer segmentation for MixITup, a dessert and beverage brand with branches in Jakarta, Depok, and Tangerang. Using demographic, economic, and behavioral variables, the analysis identifies distinct customer groups to support data-driven marketing strategies. The workflow includes preprocessing, exploratory data analysis (EDA), feature scaling, categorical encoding, clustering with K-Means++ and K-Medoids, and insight generation.

---

## **Dataset Description**

The dataset contains the following attributes:

* **ID**: Unique customer identifier
* **Gender**
* **Age**
* **Monthly Income**
* **Spending Score** (0–100)
* **Married** (0 = No, 1 = Yes)
* **City** (Jakarta, Depok, Tangerang)
* **Promo** (frequency of promo usage)
* **FavDay** (favorite day to visit)
* **FavFlavor** (preferred flavor)

---

## **Preprocessing**

Preprocessing follows the same steps as the previous MixITup project, including:

* Handling missing values
* Cleaning inconsistent entries
* Formatting numeric variables
* Encoding categorical features using Label Encoding
* Standardizing numerical columns (Age, Monthly Income, Spending Score) to ensure comparable scales

Standardization produces mean = 0 and standard deviation = 1, improving model performance on scale-sensitive algorithms, especially clustering.

---

## **Exploratory Data Analysis**

### **Numerical Variables**

* **Age** is symmetrically distributed around a mean of **37.18**, with most customers between 30–40 years.
* **Monthly Income** is right-skewed, with most individuals earning lower income and a few high-income outliers (mean ≈ 18.4M IDR).
* **Spending Score** shows a **bimodal pattern**, indicating two distinct spending behaviors, with mean ≈ 50.88.

These results indicate strong demographic and economic diversity across customers.

---

### **Categorical Variables**

Findings include:

* **Gender**: 93 women and 80 men.
* **Marital Status**: 149 not married, 24 married.
* **City**: Jakarta dominates (76), followed by Depok (54) and Tangerang (43).
* **Promo Usage**: Promo "1.0" is most used (82 occurrences), while Promo "5.0" is unused.

These characteristics help identify demographic patterns and city-based marketing opportunities.

---

## **Clustering Analysis**

Two clustering methods were applied: **K-Means++** (with optimal k selected via Elbow Method) and **K-Medoids** for robust segmentation due to the presence of outliers.

---

## **Segmentation Results (Initial Boxplot and Barplot)**

### **Cluster 0: Medium-Spending Regular Customers**

* **73 customers**
* Mixed gender, wide age range
* Many married, primarily from Jakarta
* Not highly responsive to promotions
* Prefer weekdays (especially Monday)
* Favor classic mixed flavors (2–3 flavor combinations)
* Stable and loyal group

### **Cluster 1: High-Spending Loyal Customers**

* **62 customers**
* Mostly young adult women (~30 years old)
* Many married
* Reside in Depok, Jakarta, Tangerang
* Not promo-sensitive but consistent buyers
* Visit on Monday and Saturday
* Prefer vanilla, strawberry, or mixed flavors
* Strong potential for premium targeting

### **Cluster 2: New or Infrequent Visitors**

* **36 customers**
* Older demographic (~45 years old)
* Mostly married
* From Jakarta and Tangerang
* Highly responsive to promotions
* Prefer weekend visits
* Prefer sweeter/unique flavors: chocolate, blueberry, bubble gum

---

## **K-Means++ Segmentation**

### **Cluster 0**

* **71 customers**
* Older age group, mostly married
* Medium to high income
* From Depok and Jakarta
* Rare promo users
* Favor Monday and Sunday
* Prefer mix 2 and mix 3 flavors
* Medium to high spending behavior

### **Cluster 1**

* **44 customers**
* Age 26–34, mostly married
* Low to high income range
* From Depok
* Rare promo usage
* Prefer Monday and Tuesday
* Favor vanilla and strawberry
* Highest spending per customer

### **Cluster 2**

* **54 customers**
* Mostly 42–53 years old
* Balanced gender ratio
* From Tangerang and Jakarta
* Frequent promo users
* Prefer Saturday and Sunday
* Favor chocolate and blueberry
* Low to medium spending

---

## **Final Segmentation Using K-Medoids**

K-Medoids is selected due to robustness against outliers.
The final insights and recommendations are based on this method.

---

## **Insights**

### **Cluster 0: Stable, Low-Promo Users**

* Consistent spending and strong loyalty
* Prefer Monday and Sunday
* Prefer mixed flavors
* Promo is not a key motivator

### **Cluster 1: High-Value Loyal Customers**

* Highest spending among all clusters
* Prefer classic flavors like vanilla and strawberry
* Visit mainly Monday and Saturday
* Ideal for personalized campaigns

### **Cluster 2: Promo-Sensitive Customers**

* Highly responsive to promotions
* Prefer weekends
* Prefer unique and sweet flavors
* Good target for discount-based campaigns

---

## **Recommendations**

### **Cluster-Based Marketing Strategy**

* **Cluster 0**:
  Enhance loyalty programs and offer exclusive benefits on Monday and Sunday. Focus on quality-driven campaigns.

* **Cluster 1**:
  Personalize offers based on favorite flavors. Promote premium products on Monday and Saturday.

* **Cluster 2**:
  Use aggressive promotions, especially on weekends. Offer bundle deals for chocolate, blueberry, and bubble-gum flavors.

### **Flavor Optimization**

* Promote mixed flavors for Cluster 0
* Promote classic flavors for Cluster 1
* Promote unique and creative flavors for Cluster 2

### **Loyalty and Promo Development**

* Strengthen loyalty programs for Cluster 0 and 1
* Create targeted promo campaigns for Cluster 2
* Consider flavor-based seasonal campaigns per segment

---

## **Conclusion**

Customer segmentation using K-Medoids reveals three main customer groups:

1. Medium-Spending Regular Customers
2. High-Spending Loyal Customers
3. Promo-Sensitive New or Infrequent Visitors

Each cluster has distinct demographic patterns, flavor preferences, promotion responsiveness, and visit behaviors. By applying targeted marketing strategies, MixITup can increase purchase frequency, improve customer retention, and enhance overall business performance.
