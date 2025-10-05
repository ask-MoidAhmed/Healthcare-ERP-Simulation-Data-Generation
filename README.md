# ProactiveHealth: Healthcare ERP Simulation

👩‍⚕️ **Project Overview**  
ProactiveHealth is a simulated Healthcare ERP designed to emulate a fully structured healthcare system. It includes **patients, staff, appointments, billing, medical teams, medicines, inventory, treatments, and more**. The focus of this project is **creating relational tables and generating realistic synthetic data** to mimic a working ERP system.

> ⚠️ Disclaimer: This is a simulation for learning and demonstration purposes. All data is synthetic and does not represent real patients, staff, or medical information.

---

## 📊 Dataset & Tables
The ERP includes **22 interconnected tables** representing key entities in a healthcare system. Here's a high-level overview:

| Table | Description |
|-------|-------------|
| `STG_EHP__PATN` | Patient information, demographics, and contacts |
| `STG_EHP__STFF` | Staff information including roles and department assignments |
| `STG_EHP__APPT` | Appointments between patients and doctors/staff |
| `STG_EHP__BILL` | Billing details for visits and treatments |
| `STG_EHP__DIAG` | Diagnoses information linked to patient visits |
| `STG_EHP__TRTM` | Treatments administered to patients |
| `STG_EHP__MEDT` | Medical teams assigned to patient visits |
| `STG_EHP__MDCN` | Medicines with type, form, strength, and storage |
| `STG_EHP__TMMD` | Medicine administration during visits |
| `STG_EHP__INSR` | Insurance policies linked to patients |
| `STG_EHP__PMNT` | Payments made by patients |
| `STG_EHP__VIST` | Patient visit records |
| `STG_EHP__ROMS` | Hospital rooms and department links |
| `STG_EHP__DPMT` | Departments in the hospital |
| `STG_EHP__EQPM` | Equipment in departments with status and location |
| `STG_EHP__SPLY` | Supplies and inventory details |
| `STG_EHP__INVN` | Daily inventory tracking and verification |
| `STG_EHP__PTAL` | Patient allergy information |
| `STG_EHP__VNDR` | Vendor information |
| `STG_EHP__VPMT` | Vendor payments |
| `STG_EHP__MDBL` | Medical bills |
| `STG_EHP__ALGY` | Master list of allergies |

> 💡 Each table is **interconnected via primary and foreign keys**, simulating real-world ERP relationships.

---

## 🛠 Tools & Libraries Used

The ERP simulation and data generation were built entirely with **Python**, using the following libraries:

- **Faker**: Generate realistic names, addresses, emails, phone numbers, and other entities.  
- **Random**: Randomized selection for departments, roles, medicine assignments, etc.  
- **NumPy**: Numeric operations and array manipulations.  
- **Pandas**: DataFrames for table creation, manipulation, and CSV export.  
- **String**: Character operations for generating codes and IDs.

---

## 💾 Data Generation Process

The data was **synthetically generated** to simulate real healthcare operations. Two approaches were used:

### 1. Manual Data Generation

Some datasets had to be created manually to ensure authenticity of the data:

#### Department Data
- Department Names
- Department Location
- 

*Screenshot Placeholder:*  
`![Patient Data Sample](screenshots/patient_data.png)`

#### Staff Data
- Staff IDs for doctors, nurses, and administrative staff  
- Departments and roles assigned manually for realism  
- Hire dates and salaries  

*Screenshot Placeholder:*  
`![Staff Data Sample](screenshots/staff_data.png)`

#### Appointments & Visits
- Key appointment schedules and visit records  
- Linked manually to staff and rooms  

*Screenshot Placeholder:*  
`![Appointments Sample](screenshots/appointments.png)`

---

### 2. Python-Based Data Generation

Other datasets were generated programmatically using Python libraries to create large-scale synthetic data:

#### Medicines & Treatments
- Random medicine names using Faker + custom lists  
- Medicine types, forms, and strength values  
- Assigned medicines to visits via medical teams  
- Treatment records linked to diagnoses  

*Screenshot Placeholder:*  
`![Medicine & Treatment Sample](screenshots/medicines_treatments.png)`

#### Billing & Payments
- Generated bills for each patient visit  
- Random payment terms, amounts, and methods  
- Vendor payments for supplies  

*Screenshot Placeholder:*  
`![Billing & Payments Sample](screenshots/billing_payments.png)`

#### Inventory & Supplies
- Medicines and equipment linked to supply records  
- Random batch numbers, quantities, warehouse locations  
- Daily inventory ingestion, receipt, issue, and verification  

*Screenshot Placeholder:*  
`![Inventory Sample](screenshots/inventory.png)`

## 🔗 Relationships & Links
The ERP **mirrors real-world relationships**, such as:

- Patients → Appointments → Visits → Diagnoses → Treatments  
- Medical Teams → Staff → Visits  
- Medicines → TMMD (medicine administration) → Visits  
- Inventory → Supplies → Vendor → Payments  

> A full ERD diagram can be added here in the future.

---

## 📁 Repository Structure

