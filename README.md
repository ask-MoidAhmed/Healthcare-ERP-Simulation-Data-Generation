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

<img width="330" height="193" alt="image" src="https://github.com/user-attachments/assets/170d2a22-d997-4c55-90ce-33362e081d85" />


---

## 💾 Data Generation Process

The data was **synthetically generated** to simulate real healthcare operations. Two approaches were used:

### 1. Manual Data Generation

Some datasets had to be created manually to ensure authenticity of the data:

#### Department and Allergies Data
- I created Department and Allergies data as shown below.

##### Example Screenshot

<img width="545" height="442" alt="image" src="https://github.com/user-attachments/assets/0ff9422b-4e9f-4444-9bd7-797bea02b7e5" />

#### Equipment Data
- For this I had to be a little creative. So I created an entire equipment schema like shown below.

##### Example Screenshot

<img width="635" height="480" alt="image" src="https://github.com/user-attachments/assets/97e56bf2-a0ea-4c7f-9193-2eb099e19989" />

<img width="629" height="508" alt="image" src="https://github.com/user-attachments/assets/e7fe59fa-f26e-4fd5-a19d-1276217b2367" />

#### Codes & Descriptions
- I created all the codes and decriptions which I then used random.choice to populate the records.

##### Example Screenshot

<img width="532" height="48" alt="image" src="https://github.com/user-attachments/assets/b52665ac-9ab6-4f0a-84eb-fa324b595ad6" />

<img width="455" height="49" alt="image" src="https://github.com/user-attachments/assets/4ac93b50-5c80-4840-bbd7-340fe34afcff" />

#### Medicine Names
- For this, it was a mixture of using python libraries to generate names and then adding specific strings to make it sound more medicine-like.

##### Example Screenshot

<img width="501" height="203" alt="image" src="https://github.com/user-attachments/assets/67269a3e-9236-47a2-84a6-cfee0f8fb2f6" />

<img width="433" height="34" alt="image" src="https://github.com/user-attachments/assets/d283176a-c8f8-4737-ac6b-fb3ba334b826" />

---

### 2. Python-Based Data Generation

Other datasets were generated programmatically using Python libraries to create large-scale synthetic data:

#### Patient & Company Names
- In order to generate synthetic data I used Faker library.
- To populate that generated data I used random, numpy and pandas.

##### Example Screenshot

<img width="761" height="499" alt="image" src="https://github.com/user-attachments/assets/2f5c68bb-4eb1-4d92-8ca7-59132d0c1b91" />

#### Unique Identifiers
- To generate these, I used random.randint to generate random integers and string.ascii to generate alphabets.

##### Example Screenshot

<img width="427" height="155" alt="image" src="https://github.com/user-attachments/assets/cfdc62de-fc42-4456-b054-2fc8ac451aaa" />

---

## 🔗 Relationships & Links
The ERP **mirrors real-world relationships**, such as:

- Patients → Appointments → Visits → Diagnoses → Treatments  
- Medical Teams → Staff → Visits  
- Medicines → TMMD (medicine administration) → Visits  
- Inventory → Supplies → Vendor → Payments  

> A full ERD diagram can be added here in the future.

---

## 📁 Repository Structure

