<!-- PROJECT BANNER -->
<p align="center">
  <img src="https://img.shields.io/badge/Data%20Warehouse-PostgreSQL-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Architecture-Medallion-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/ETL-Pipeline-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Power%20BI-Ready-orange?style=for-the-badge" />
</p>

<h1 align="center">📦 Data Warehouse Project (PostgreSQL + Medallion Architecture)</h1>

<p align="center">
End-to-end SQL-driven Data Warehouse using Bronze → Silver → Gold layers, with dimensional modelling and BI-ready outputs.
</p>

---

# 📑 Table of Contents
- [Overview](#overview)
- [Medallion Architecture](#medallion-architecture)
- [Star Schema Model](#star-schema-model)
- [Bronze Layer](#bronze-layer--raw-ingestion)
- [Silver Layer](#silver-layer--cleansing--standardisation)
- [Gold Layer](#gold-layer--dimensional-modelling)
- [Key SQL Techniques](#🧠-key-sql-techniques-used)
- [Final Outputs](#📊-final-output)

---

# Overview

This project demonstrates an **end-to-end Data Warehouse** built in **PostgreSQL** using the **Medallion Architecture (Bronze → Silver → Gold)**.

It integrates:
- CRM Data  
- ERP Product & Category Data  
- ERP Customer & Location Data  
- Sales Transactions  

Outputs include clean **fact & dimension views** used for **Power BI analytics**.

---

# Medallion Architecture

