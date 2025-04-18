### 🚀 What is Performance Testing?

**Performance Testing** is a type of software testing that evaluates how a system behaves under different levels of **load**, **stress**, and **usage conditions**.  
It checks the **speed**, **stability**, **scalability**, and **responsiveness** of the application to ensure a smooth user experience.

---

### 🎯 **Main Goals of Performance Testing:**

1. **Measure response time**  
    ➤ How fast does the system respond to user actions?
    
2. **Check system stability**  
    ➤ Does it crash or slow down under pressure?
    
3. **Ensure scalability**  
    ➤ Can the system handle growing numbers of users or data?
    
4. **Identify bottlenecks**  
    ➤ Where does the performance drop happen – server, database, frontend, etc.?

## **Types of Performance testing:**

### 1. **Load Testing**

**Definition:**  
Checks the system's performance under expected user load.

**Goal:**  
To verify how the system behaves when multiple users access it simultaneously under normal conditions.

**API Example:**  
Sending 1000 concurrent requests to a **login API** and measuring response time and error rate.

**Non-API Example:**  
Opening a web page (like a homepage or product list) in 100 browser sessions at once to see if it loads within acceptable time.

---

### 2. **Stress Testing**

**Definition:**  
Tests the system beyond its normal limits to see how it handles extreme conditions.

**Goal:**  
To identify the system’s breaking point and how it recovers from failure.

**API Example:**  
Sending 10,000+ requests per second to an **order placement API** until the server crashes or response time spikes.

**Non-API Example:**  
Opening and using a mobile app simultaneously on hundreds of devices, each doing continuous scrolling or search.

---

### 3. **Spike Testing**

**Definition:**  
Evaluates system behavior when there’s a sudden and sharp increase or decrease in load.

**Goal:**  
To assess if the system can handle unexpected traffic spikes.

**API Example:**  
Suddenly increasing API calls to a **payment API** from 100 to 5000 requests per second, then dropping them.

**Non-API Example:**  
Rapidly opening a live-streaming webpage (like YouTube Live) by thousands of users within seconds.

---

### 4. **Endurance Testing (Soak Testing)**

**Definition:**  
Tests the system under continuous load for a long period of time.

**Goal:**  
To identify memory leaks or performance degradation over time.

**API Example:**  
Running a **user session API** at 200 requests per second for 12 hours.

**Non-API Example:**  
Keeping a mobile app running overnight with active user activity (like chat messages or scrolling feed) to detect slowdowns or crashes.

---

### 5. **Scalability Testing**

**Definition:**  
Checks how well the system scales (in performance) when resources or users increase.

**Goal:**  
To determine the system’s capacity and if performance improves with added resources.

**API Example:**  
Running a **search API** test with gradually increasing load while adding more servers and checking if response time improves.

**Non-API Example:**  
Testing a web-based dashboard with increasing users (10 → 1000) and seeing if UI interactions (like filters, clicks) remain responsive.

---

### 6. **Volume Testing**

**Definition:**  
Evaluates system performance by increasing the volume of data (not users).

**Goal:**  
To ensure the system can handle large data sets efficiently.

**API Example:**  
Uploading a huge dataset (like 10 million records) via a **bulk import API** and measuring processing time.

**Non-API Example:**  
Testing an analytics dashboard that loads reports with millions of rows or logs.


--- 

📌 Example Scenario: Social Media App API

   Let’s say you're testing the /api/v1/feed endpoint (which fetches the home feed).

- Load Testing: Simulate 1000 users hitting /feed API concurrently.  
- Stress Testing: Increase the number to 10,000 requests/sec and see when the server breaks.  
- Spike Testing: Suddenly jump from 100 to 5000 requests and drop again — does the API recover? 
- Endurance Testing: Keep hitting /feed every 5 seconds for 12 hours.  
- Volume Testing: Populate DB with 10 million posts and see how /feed performs.  
