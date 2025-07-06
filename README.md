# Dynamic Printing Service (DPS)

## 🧩 Overview

**Dynamic Printing Service (DPS)** is a high-performance, scalable web service built with **Node.js**, leveraging the **Carbone.io** engine to generate dynamic documents (PDF, DOCX, XLSX, etc.) from structured **JSON** data and pre-designed templates.

DPS is designed for enterprise environments with integration flexibility, load balancing support, and business continuity in mind.

---

## 🚀 Key Features

- ✅ **Standalone Web API**: Lightweight RESTful service, deployable on multiple ports or nodes.
- 🔄 **JSON Compatible**: Accepts data from any source capable of sending JSON (APIs, databases, microservices).
- 🧾 **Template-based Output**: Uses ODT, DOCX templates processed by Carbone.
- 🖨️ **Multiple Output Targets**:
  - HTTP response (Base64 encoded)
  - Direct printing via CUPS
  - File system (PDF/Word export)
- 🌐 **Encoding Support**: Converts `cp1256` (Arabic Windows) to `UTF-8`.
- 📦 **Linux Native**: Built and tested for Linux only, with required dependencies.
- 📈 **Scalable**: Supports multiple instances, load balancing, and Docker deployments.

---

## 📐 High-Level Architecture

### Data Sources:
- **Replica Databases**
- **Production Systems**
- **External APIs / Systems**

These systems send JSON payloads to DPS.

### DPS Core:
Each instance:
- Loads a document template
- Merges data with Carbone
- Produces output document

### Output Targets:
- **HTTP Response** (Base64 string)
- **Printing Service** (CUPS integration)
- **File System / Archiving**

