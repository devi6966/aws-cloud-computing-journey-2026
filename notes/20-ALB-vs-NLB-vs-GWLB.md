# ALB vs NLB vs GWLB

## Types of Elastic Load Balancer (ELB)

### 1. Application Load Balancer (ALB)

**Works On:** Layer 7 (Application Layer)

**Purpose:** Routes HTTP/HTTPS requests based on URL, Hostname, Headers, and Cookies.

**Best For:**

* Web Applications
* REST APIs
* Microservices

**Real World Example:**

Amazon, Flipkart, Swiggy, Zomato, Netflix Login

**Remember:**

ALB = Smart Routing

---

### 2. Network Load Balancer (NLB)

**Works On:** Layer 4 (Transport Layer)

**Purpose:** Routes TCP/UDP traffic using IP Address and Port with ultra-low latency.

**Best For:**

* Online Gaming
* Stock Trading
* VoIP
* Live Streaming

**Real World Example:**

PUBG/BGMI, Valorant, Zerodha, Groww

**Remember:**

NLB = Fast Routing

---

### 3. Gateway Load Balancer (GWLB)

**Purpose:** Routes traffic through security appliances before reaching the application.

**Best For:**

* Firewalls
* Intrusion Detection Systems (IDS)
* Intrusion Prevention Systems (IPS)
* Enterprise Security

**Real World Example:**

Banks, Government Organizations, Enterprise Data Centers

**Remember:**

GWLB = Security Routing

---

## Difference

| Feature | ALB | NLB | GWLB |
|---------|-----|-----|------|
| Layer | 7 | 4 | Security |
| Traffic | HTTP/HTTPS | TCP/UDP | Security Traffic |
| Routing | URL, Hostname | IP & Port | Firewall/IDS/IPS |
| Speed | High | Very High | Security Focus |
| Best For | Web Apps | Gaming & Trading | Enterprise Security |

---

## Quick Revision

* ALB → Smart Routing for Web Applications
* NLB → High-Speed Routing for TCP/UDP Traffic
* GWLB → Security Inspection using Firewalls and IDS/IPS

---

## Interview Question

**Q. Why did AWS create three different Load Balancers?**

**Answer:**

Different applications have different requirements. ALB provides intelligent routing for web applications, NLB provides ultra-low latency for high-performance network applications, and GWLB provides centralized security by routing traffic through security appliances.
