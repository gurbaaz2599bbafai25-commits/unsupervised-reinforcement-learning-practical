# Unsupervised & Reinforcement Learning Practical

A practical exploration of **Unsupervised Learning** and **Reinforcement Learning** using simple business-focused examples in Python.

The project demonstrates how machine learning can be applied to **customer segmentation** and **decision-making based on rewards**.

---

## 📌 Project Overview

This practical is divided into two parts:

### Part A — Customer Segmentation Using K-Means

An online retailer wants to understand different types of customers using two variables:

* Monthly Spending
* App Visits

**K-Means Clustering** is used to divide customers into **3 groups** and identify potential customer behaviour patterns.

### Part B — Introduction to Reinforcement Learning

A delivery company has two possible routes:

* Route A
* Route B

The practical demonstrates how a decision-making system can compare rewards and learn which route performs better.

---

## 🎯 Learning Objectives

By completing this practical, the project demonstrates the ability to:

* Understand customer segmentation using K-Means Clustering.
* Identify groups of similar customers.
* Interpret clusters from a business perspective.
* Understand the basic concept of Reinforcement Learning.
* Identify an Agent, Action, Environment, and Reward.
* Understand Exploration vs Exploitation.
* Connect machine learning concepts with business decision-making.

---

# Part A: Customer Segmentation Using K-Means

## 💼 Business Problem

An online retailer wants to understand different customer types.

The available customer information includes:

* **Monthly Spending**
* **App Visits**

K-Means Clustering is used to divide customers into **3 clusters**.

### Dataset

The practical uses a small example dataset containing 8 customers:

| Customer | Monthly Spending | App Visits |
| -------- | ---------------: | ---------: |
| A        |            9,000 |         20 |
| B        |            8,500 |         18 |
| C        |            1,200 |          3 |
| D        |            1,500 |          4 |
| E        |            5,000 |         10 |
| F        |            5,500 |         12 |
| G        |            8,800 |         19 |
| H        |            1,800 |          5 |

---

## 🧠 K-Means Clustering

The model is configured with:

```python
KMeans(n_clusters=3, random_state=42, n_init=10)
```

The algorithm groups customers based on similarities in:

* Monthly spending
* App activity

The resulting cluster labels are assigned to the dataset as a new **Cluster** column.

> Cluster numbers such as 0, 1, and 2 are simply labels. They do not automatically represent good, average, or bad customers.

---

## 📊 Customer Segmentation

The project visualizes the customer groups using a scatter plot.

The visualization compares:

**Monthly Spending vs App Visits**

This makes it easier to identify customers with similar behavioural patterns.

### Possible Business Segments

Depending on the clustering results, groups may be interpreted as:

* **Premium Customers**
* **Medium-Value Customers**
* **Low-Engagement Customers**

Possible business actions include:

* Loyalty rewards
* Personalized recommendations
* Re-engagement campaigns

The business interpretation should be based on actual customer behaviour rather than the numerical cluster label.

---

# Part B: Reinforcement Learning

## 🚚 Business Scenario

A delivery company has two possible routes:

* Route A
* Route B

The objective is to choose the route that generally provides faster delivery.

For this practical:

* Faster delivery → Higher reward
* Slower delivery → Lower reward

---

## 🎮 Reinforcement Learning Concept

The basic process is:

```text
Take an Action
      ↓
Receive a Reward
      ↓
Learn From the Result
      ↓
Make Better Decisions
```

### Key Components

| Component   | Example                       |
| ----------- | ----------------------------- |
| Agent       | Delivery decision system      |
| Environment | Roads and traffic             |
| Action      | Choose Route A or Route B     |
| Reward      | Delivery performance feedback |

---

## 🏆 Reward Comparison

The example rewards are:

```python
route_rewards = {
    "Route A": [5, 4, 6, 5, 4],
    "Route B": [8, 9, 7, 10, 8]
}
```

The average reward is calculated for each route.

The route with the higher average reward represents the better-performing option in this simplified example.

---

## 🔍 Exploration vs Exploitation

### Exploration

Trying a new or less-used option to collect additional information.

**Example:**
Choosing Route A even when Route B has previously performed better.

### Exploitation

Choosing the option that is already known to perform well.

**Example:**
Choosing Route B because it has previously produced higher rewards.

A practical reinforcement learning system needs to balance both exploration and exploitation.

---

# 🔄 Machine Learning Comparison

| Machine Learning Type  | Main Idea                      | Business Example          |
| ---------------------- | ------------------------------ | ------------------------- |
| Supervised Learning    | Learn from known answers       | Customer churn prediction |
| Unsupervised Learning  | Discover hidden patterns       | Customer segmentation     |
| Reinforcement Learning | Learn from actions and rewards | Route optimization        |

---

# 💼 Business Applications

The concepts demonstrated in this practical can be applied to real business problems.

### Customer Segmentation

Businesses can use clustering to:

* Identify different customer groups
* Create targeted marketing campaigns
* Personalize recommendations
* Develop loyalty programs
* Identify customers requiring re-engagement

### Reinforcement Learning

Reinforcement learning can support:

* Route optimization
* Recommendation systems
* Dynamic decision-making
* Resource allocation
* Automated business processes

---

# 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Scikit-learn**
* **Matplotlib**
* **K-Means Clustering**
* **Reinforcement Learning Concepts**
* **Google Colab / Jupyter Notebook**

---

# 📁 Repository Structure

```text
unsupervised-reinforcement-learning-practical/
│
├── part-a/
│   └── unsupervised-learning/
│       └── Unsupervised_and_Reinforcement_Learning_Practical_Name.ipynb
│
├── screenshots/
│   └── customer-segmentation.png
│
└── README.md
```

---

# 🚀 How to Run

## Google Colab

1. Open the `.ipynb` notebook in Google Colab.
2. Run the cells sequentially.
3. Observe the customer dataset.
4. Run the K-Means clustering model.
5. View the customer segmentation graph.
6. Calculate the average route rewards.
7. Run the exploration and exploitation examples.
8. Complete the reflection questions.

## Jupyter Notebook

Install the required libraries:

```bash
pip install pandas matplotlib scikit-learn
```

Then open the notebook and run the cells.

---

# 📚 Key Learning Outcomes

This practical provides hands-on exposure to:

* Unsupervised Learning
* K-Means Clustering
* Customer Segmentation
* Data Visualization
* Business Interpretation of Clusters
* Reinforcement Learning Fundamentals
* Agent, Action, Environment and Reward
* Exploration and Exploitation
* AI-based Business Decision-Making

---

# ⚠️ Limitations

This practical uses simplified examples for educational purposes.

* The customer dataset contains only a small number of customers.
* Only two customer features are used for clustering.
* The reinforcement learning example uses predefined rewards rather than a trained RL agent.
* Real-world business applications would require larger datasets and more sophisticated models.
* Cluster labels require business interpretation and should not be treated as meaningful categories automatically.

---

# 🎓 Project Information

**Project Type:** Academic Practical
**Domain:** Artificial Intelligence & Machine Learning
**Topics:** Unsupervised Learning, K-Means Clustering & Reinforcement Learning
**Platform:** Google Colab / Jupyter Notebook
**Language:** Python

---

# 📌 Conclusion

This practical demonstrates two different approaches to machine learning.

**K-Means Clustering** helps businesses discover hidden patterns and segment customers based on their behaviour, while **Reinforcement Learning** introduces the idea of learning better decisions through actions and rewards.

Together, these concepts demonstrate how AI and machine learning can support data-driven **business analysis, customer management, and operational decision-making**.
