# SuperKart-Sales-Forecasting-Platform
End-to-end sales forecasting system with serialized model, REST API, and Streamlit frontend deployed on Hugging Face.

Frontend (Streamlit): https://dwidrich-superkart-frontend.hf.space/
Backend (Flask API): https://dwidrich-superkart-backend.hf.space/

*This project demonstrates end-to-end machine learning deployment, including model serialization, containerized APIs, and a web-based prediction interface.*

## Business Problem

SuperKart operates a network of supermarkets and food marts across multiple city tiers. Accurate sales forecasting is critical for inventory planning, regional strategy, and supply chain coordination. While predictive modeling provides value, its impact depends on the ability to operationalize forecasts across the organization.

This project goes beyond model development to deliver a **production-ready sales forecasting system**, enabling SuperKart to generate real-time and batch predictions through deployed services that integrate directly into business workflows.

---

## System Architecture Overview

The solution is implemented as a two-tier deployment:

- **Backend**: Flask-based REST API serving a serialized Random Forest model
- **Frontend**: Streamlit application for interactive, user-facing predictions
- **Deployment**: Both services containerized and deployed on Hugging Face Spaces

### Live Deployment
- **Frontend (Streamlit)**: https://dwidrich-superkart-frontend.hf.space  
- **Backend (Flask API)**: https://dwidrich-superkart-backend.hf.space  

---

## Forensic Research & Key Insights

- **Product pricing and weight are the strongest revenue drivers**  
  Product_MRP and Product_Weight show strong positive relationships with sales.

- **Store maturity has a modest positive effect**  
  Older stores tend to generate higher sales, likely due to brand familiarity and operational stability.

- **Sales vary by product category and store format**  
  Categories such as Snack Foods, Fruits & Vegetables, and Dairy consistently outperform others.

- **Allocated display area alone does not drive revenue**  
  Shelf space must be paired with demand and pricing strategy to be effective.

- **The forecasting model generalizes well**  
  The selected Random Forest model demonstrated strong test performance, supporting production use.

---

## Modeling & Deployment

- Trained a Random Forest regression model for product–store level sales forecasting.
- Serialized the trained pipeline for reuse in production environments.
- Exposed predictions via a REST API for system-to-system integration.
- Built a Streamlit frontend for exploratory and ad hoc forecasting use.
- Containerized and deployed both services to ensure environment consistency.

---

## Business Recommendations

- Use forecast outputs to **optimize inventory replenishment** and reduce stock-outs.
- Tailor product assortments and pricing strategies by **store type and city tier**.
- Integrate the backend API into planning and analytics pipelines for automated forecasting.
- Leverage older stores as **performance benchmarks** when evaluating new locations.

---

## Repository Structure

- `Full_Code_SuperKart_Model_Deployment_Notebook.ipynb`  
  End-to-end workflow including EDA, model training, serialization, API integration, and deployment logic.

---

## Tools & Technologies

- Python
- scikit-learn
- Flask (REST API)
- Streamlit (Frontend)
- Model serialization
- Docker
- Hugging Face Spaces
