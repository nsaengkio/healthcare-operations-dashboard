# 📊 **Healthcare Operations Dashboard**  
*A Power BI analytics solution for monitoring encounters, provider performance, and departmental efficiency.*

---

## ⭐ Overview
This project showcases a complete Power BI solution designed for healthcare operational analytics. It includes:

- A custom healthcare‑themed color palette  
- A polished cover page  
- A navigation bar for app‑like usability  
- Executive, provider, and department‑level insights  
- Interactive slicers  
- Conditional formatting using sentiment and divergent color scales  
- Clean layout and UX best practices  

The goal is to demonstrate senior‑level BI development skills across data modeling, DAX, visualization design, and storytelling.

---

## 🏥 Business Problem
Healthcare operations teams need visibility into:

- Encounter volumes  
- Provider performance  
- Department efficiency  
- Readmission and no‑show trends  
- Length of stay  
- Cost patterns  

This dashboard provides a unified view that supports:

- Staffing decisions  
- Provider performance reviews  
- Departmental resource allocation  
- Operational improvement initiatives  

---

## 🧱 Data Model
The solution uses a **star schema** optimized for analytics.

### **Dimensions**
- `DimDate`  
- `DimProvider`  
- `DimDepartment`  
- `DimPatient`  

### **Facts**
- `FactEncounters`  
- `FactProviderPerformance`  
- `FactDepartmentMetrics`  

### **Model Highlights**
- One‑to‑many relationships  
- Proper date table with continuous range  
- Surrogate keys  
- Clean, readable field naming  
- Measures stored in a dedicated **Measures** table  

---

## 🧮 Key DAX Measures
Examples of core measures used in the dashboard:

```DAX
Total Encounters = SUM(FactEncounters[EncounterCount])

Readmission Rate = 
DIVIDE(
    SUM(FactEncounters[Readmissions]),
    SUM(FactEncounters[EncounterCount])
)

Average LOS = AVERAGE(FactEncounters[LengthOfStay])

No Show Rate =
DIVIDE(
    SUM(FactEncounters[NoShows]),
    SUM(FactEncounters[ScheduledVisits])
)
```

All measures follow best practices:

- No implicit measures  
- Consistent naming  
- DIVIDE() for safe division  
- Logical grouping in a Measures table  

---

## 🎨 Custom Theme
The report uses a custom healthcare‑friendly theme with:

### **Primary Palette**
- Primary: `#1F4E79`  
- Secondary: `#2E75B6`  
- Accent: `#70AD47`  
- Neutral Dark: `#333333`  
- Neutral Light: `#F2F2F2`  

### **Sentiment Colors**
- Positive: `#70AD47`  
- Neutral: `#A6A6A6`  
- Negative: `#C00000`  

### **Divergent Scale**
- Low: `#C00000`  
- Middle: `#FFFFFF`  
- High: `#1F4E79`  

This ensures consistent visual language across all pages.

---

## 🧭 Navigation & UX
The dashboard includes:

- A custom navigation bar  
- Hover effects  
- Active‑page highlighting  
- Clean slicer row  
- Consistent spacing and alignment  
- A professional cover page with iconography  

This creates an app‑like experience for users.

---

## 📸 Screenshots  
*(Update these paths after uploading your images to `/screenshots`.)*

```
![Cover Page](screenshots/cover.png)
![Executive Summary](screenshots/page1.png)
![Provider Performance](screenshots/page2.png)
![Department Insights](screenshots/page3.png)
```

---

## 🧭 How to Use This Dashboard
1. Use the slicers at the top to filter by date, department, or provider.  
2. Navigate between pages using the top navigation bar.  
3. Hover over visuals to view tooltips.  
4. Drill through on providers or departments for deeper insights.  
5. Review KPIs with conditional formatting for quick interpretation.  

---

## 🛠️ Tools & Technologies
- Power BI Desktop  
- DAX  
- Power Query  
- Star Schema Modeling  
- Custom Theme JSON  
- GitHub for versioning & documentation  

---

## 📁 Repository Structure
```
/Healthcare-Operations-Dashboard
   /screenshots
       cover.png
       page1.png
       page2.png
       page3.png
   HealthcareDashboard.pbix
   README.md
```

---

## 📌 Key Takeaways
This project demonstrates:

- Strong data modeling fundamentals  
- Clean, readable DAX  
- Professional UI/UX design  
- Healthcare domain understanding  
- Ability to build a polished, end‑to‑end BI solution  

---

## 🙌 Author
**Nancy**  
Senior BI Developer / Data Architect  

