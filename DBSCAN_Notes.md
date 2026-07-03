# DBSCAN & HDBSCAN Clustering Notes

## What is DBSCAN?

DBSCAN stands for:

**Density-Based Spatial Clustering of Applications with Noise**

It is an **Unsupervised Machine Learning** algorithm that groups data based on **density** instead of centroids.

Unlike K-Means, DBSCAN does **not** require the number of clusters (K) beforehand.

---

# Key Concepts

## 1. Core Point

A point that has enough neighboring points within a specified radius (epsilon).

Think of it as a crowded place.

Example:

Many customers standing together.

---

## 2. Border Point

A point that is close to a core point but does not have enough neighbors to become a core point.

It belongs to a cluster.

---

## 3. Noise Point

A point that is far from every cluster.

It does not belong to any group.

Also called an **Outlier**.

---

# Important Parameters

## Epsilon (eps)

The maximum distance used to search for neighboring points.

Small eps → More clusters and more noise.

Large eps → Fewer clusters.

---

## Min Samples (MinPts)

Minimum number of nearby points required to become a Core Point.

Example:

If MinPts = 5

A point must have at least 5 nearby neighbors to become a Core Point.

---

# How DBSCAN Works

Step 1

Pick a point.

↓

Step 2

Find all nearby points within epsilon.

↓

Step 3

If nearby points ≥ MinPts

→ Make it a Core Point.

↓

Step 4

Expand the cluster by checking neighboring Core Points.

↓

Step 5

Repeat until all points are processed.

↓

Step 6

Points that don't belong anywhere become Noise.

---

# Advantages

✔ No need to choose K

✔ Finds clusters of any shape

✔ Detects outliers automatically

✔ Works well with noisy datasets

---

# Limitations

✖ Choosing eps is difficult

✖ Doesn't work well if cluster densities vary a lot

✖ Slower than K-Means on very large datasets

---

# What is HDBSCAN?

HDBSCAN stands for:

**Hierarchical Density-Based Spatial Clustering of Applications with Noise**

It is an improved version of DBSCAN.

Instead of using one fixed density, HDBSCAN works with **multiple density levels**.

It can detect clusters with different densities automatically.

---

# Advantages of HDBSCAN

✔ Better than DBSCAN

✔ Handles varying densities

✔ More robust

✔ Finds meaningful clusters

✔ Less parameter tuning

---

# DBSCAN vs HDBSCAN

| DBSCAN | HDBSCAN |
|---------|----------|
| Uses one density | Uses multiple densities |
| Needs eps | No fixed eps required |
| Less flexible | More flexible |
| Good | Better |

---

# DBSCAN vs K-Means

| K-Means | DBSCAN |
|----------|---------|
| Needs K | No K required |
| Uses Centroids | Uses Density |
| Every point belongs to a cluster | Noise is allowed |
| Best for round clusters | Best for irregular clusters |

---

# Real-World Applications

- Crime Hotspot Detection
- GPS Location Analysis
- Museum Clustering
- Earthquake Detection
- Disease Outbreak Analysis
- Traffic Monitoring
- Smart Cities
- Delivery Zones
- Fraud Detection

---

# IBM Lab Summary

In this lab I learned to:

- Import Python libraries
- Load real-world museum data
- Prepare geographical coordinates
- Scale latitude and longitude
- Build a DBSCAN model
- Detect noise points
- Visualize clusters on a map of Canada
- Build an HDBSCAN model
- Compare DBSCAN with HDBSCAN
- Understand density-based clustering

---

# My Learning

After completing this project, I can now:

✔ Explain DBSCAN

✔ Explain HDBSCAN

✔ Differentiate between K-Means and DBSCAN

✔ Detect outliers

✔ Build clustering models using Scikit-learn

✔ Visualize clustering results

✔ Apply density-based clustering to real-world datasets

---

**Author**

Hamza

Learning Artificial Intelligence & Machine Learning one project at a time.
