# Zoho Sustainability Manager  
*A end-to-end Zoho solution for small businesses to track, analyze, and offset their carbon footprint, with integrated project management workflows.*

## 📌 Overview  
**Problem Statement**: Small businesses lack affordable tools to measure sustainability metrics, comply with ESG regulations, and engage customers in carbon offset programs.  
**Solution**: A Zoho-driven platform that automates carbon footprint calculation, generates auditable reports, and integrates carbon credit marketplaces, paired with a customer-facing portal for offset participation.  

---

## 🛠️ **Zoho Tech Stack**    
1. **Zoho Creator**: Core app for carbon data collection & calculations.   
2. **Zoho Analytics**: Real-time dashboards for emissions KPIs.  
3. **Zoho CRM**: Customer engagement & offset program management.  
4. **Zoho Projects**: Agile workflows for implementation.  
5. **Zoho Flow**: API integrations with external carbon credit APIs (e.g., Cloverly).  

---

## 📂 **Project Structure**  
### Phase 1: Market Research & Scope Baseline (Zoho Analytics)  
- **Dataset**: Mock survey data from 100 SMBs on sustainability challenges.  
- **Analysis**:  
  - Zoho Analytics report showing 68% lack tools to track Scope 3 emissions.  
  - Pareto chart identifying top pain points: data fragmentation (45%), compliance complexity (30%).  
- **Scope Document**:  
  - **Inclusions**: Automated Scope 1-3 emission calculators, supplier scorecards, CSR report generator.  
  - **Exclusions**: Hardware IoT integration (phased rollout).  

### Phase 2: Solution Design (Zoho Creator & Flow)  
- **App Architecture**:  
  - **Tables**:  
    - `Emissions_Data` (fields: Activity Type, CO2e, Date, Supplier_ID).  
    - `Offset_Projects` (fields: Credit Cost, Vendor, Certification Status).  
  - **Deluge Scripts**:  
    - Auto-calculation of CO2e using industry-specific emission factors.  
    ```javascript
    // Sample Deluge script for transportation emissions
    input Distance = 150; // km  
    input FuelType = "Diesel";  
    emissionFactor = MapHelper.get(emissionFactorMap, FuelType);  
    totalCO2e = Distance * emissionFactor;  
    ```  
  - **API Workflows**:  
    - Zoho Flow automates carbon credit purchases via Cloverly API when thresholds are breached.  

### Phase 3: Project Management (Zoho Projects)  
- **Milestones**:  
  - Sprint 1: Core calculator MVP (2 weeks).  
  - Sprint 2: Supplier portal (3 weeks).  
- **Gantt Chart**:  
  - Dependency mapping for CRM-Creator data sync.  
- **Risk Log**:  
  - **Risk**: Supplier data granularity → **Mitigation**: Fallback to industry-average factors.  

### Phase 4: Customer Portal (Zoho CRM & Sites)  
- **Features**:  
  - Customers redeem loyalty points for carbon offsets.  
  - Zoho Sites page displays real-time offset impact (e.g., "Your purchase saved 50kg CO2e").  
- **Journey Automation**:  
  - CRM campaigns trigger educational emails when customers reach offset milestones.  

---

## 📊 **Mock Results**  
- **Metrics**:  
  - 40% reduction in manual data entry time.  
  - 25% increase in customer participation for green loyalty programs.  
- **Sample Analytics Dashboard**:  
  - Heatmap of emission hotspots (e.g., logistics vs. office energy).  
  - Trendline comparing emissions pre/post-implementation.  

---

## 🚀 **Setup & Deployment**  
1. **Import Templates**:  
   - Clone the `Emissions_Data` table schema from [Zoho Creator Template Library](link).  
2. **API Keys**:  
   - Add Cloverly API keys to Zoho Flow.  
3. **Permissions**:  
   - Assign roles in Zoho CRM: Supplier (read-only), Auditor (full access).  

---

## 📈 **Business Impact**  
- **Cost Savings**: Eliminated $12k/yr in manual reporting costs for a 50-employee retailer.  
- **Compliance**: Automated SECR (UK) and CSRD (EU) audit trails.  

---

## 📝 **Lessons Learned**  
- **Technical Debt**: Legacy supplier data required custom Deluge parsing.  
- **Stakeholder Alignment**: Monthly sprint reviews with client sustainability teams.  

---

## 📸 **Screenshots**  
1. `analytics_dashboard.png`: Emissions by category.  
2. `creator_app.png`: Supplier data entry form.  
3. `crm_portal.png`: Customer offset redemption flow.  

---

**⭐ Star this repo** if you’d like more Zoho case studies!  
**🔗 Connect with me on LinkedIn** for project collabs.  

---

This project demonstrates your ability to:  
- Design scalable Zoho architectures.  
- Implement Deluge scripts for complex business logic.  
- Align analytics with stakeholder KPIs.  
- Manage cross-app integrations and Agile workflows.  
