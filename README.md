# ServiceNow-CustomerRequestProject
ServiceNow mini-project: Customer Request Table with automated priority calculation, unique request numbering, UI policy and client/server scripts.
# ServiceNow - Customer Request Project

## **Project Overview**
This is a ServiceNow mini-project that demonstrates hands-on experience with custom tables, Business Rules, Client Scripts, Script Includes, and UI Policies.  

The project simulates a **Customer Request system** where each request automatically calculates priority based on impact and urgency, assigns a unique request number, and validates user input on form submission.

---

## **Table Created**
**`u_customer_table_min`** with the following fields:  
- **u_full_name** (String)  
- **u_email** (String)  
- **u_phone** (String, 10 digits)  
- **u_impact** (Choice: High, Medium, Low)  
- **u_urgency** (Choice: High, Medium, Low)  
- **u_priority** (Choice: Critical, High, Moderate, Low, Planning)  
- **u_request_number** (String, auto-generated, e.g., CR001)

---

## **Features Implemented**

### **1. Business Rule**
- Automatically assigns a **unique request number** (`CR001`, `CR002`, …) for every new record.  
- Ensures the request number is read-only via a **UI Policy**.  

### **2. Client Scripts**
- Validates **Full Name**, **Email**, and **Phone Number** before form submission.  
- Dynamically updates the **Priority** field when `Impact` or `Urgency` changes.  

### **3. Script Include**
- Global `CalculatePriority` Script Include used by client scripts to calculate priority based on **Impact** and **Urgency**.  
- Demonstrates **client-server communication** using `GlideAjax`.  

### **4. UI Policy**
- Makes `u_request_number` **read-only** to prevent manual editing.  

---

## **Technologies Used**
- ServiceNow Platform  
- GlideRecord, GlideAggregate  
- Business Rules  
- Client Scripts  
- Script Include (Global)  
- UI Policy  

---

## **How to Use**
1. Import the **Update Set XML** file (`sys_remote_update_set_*.xml`) into your ServiceNow instance.  
2. Preview and commit the Update Set.  
3. Open the **Customer Request** table.  
4. Create a new request to see:
   - Automatic request numbering (`CR001`, `CR002`, …)  
   - Dynamic priority calculation  
   - Form validation for name, email, and phone  
   - Read-only request number  

---

## **Outcome**
- Gain practical experience with **ServiceNow customizations**.  
- Demonstrates **ITSM best practices** for request management.  
- Shows **hands-on knowledge of client-server scripting** in ServiceNow.  

---

**GitHub Repository:** [https://github.com/Shahjad12/ServiceNow-CustomerRequestProject).
