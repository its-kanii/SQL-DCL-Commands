# **📜 README: SQL DCL Commands**  

## **📌 Introduction**  
Data Control Language (DCL) commands in SQL are used to manage user privileges in a database. The two primary DCL commands are:  

- **🔑 GRANT** – Gives specific privileges to users or roles.  
- **🚫 REVOKE** – Removes previously granted privileges.  

---

## **📝 1. GRANT Command**  
**Purpose:** Allows users to perform specific actions on database objects.  

### **✅ Syntax:**  
```sql
GRANT privilege_name ON object_name TO user_name;
```

### **📊 Example:**  
Granting `SELECT` access on the `employees` table to user `john`:  
```sql
GRANT SELECT ON employees TO john;
```

### **💼 Real-Time Use Case:**  
The HR department needs access to view employee records but should not modify them.  
```sql
GRANT SELECT ON payroll_db.employees TO hr_team;
```

---

## **📝 2. REVOKE Command**  
**Purpose:** Removes previously granted privileges from users.  

### **🚨 Syntax:**  
```sql
REVOKE privilege_name ON object_name FROM user_name;
```

### **📊 Example:**  
Revoking `SELECT` access from user `john`:  
```sql
REVOKE SELECT ON employees FROM john;
```

### **💼 Real-Time Use Case:**  
An employee moves to a different department and should no longer have access to payroll data.  
```sql
REVOKE SELECT ON payroll_db.employees FROM hr_team;
```

---

## **🔍 Advanced Example**  
Grant multiple privileges (`SELECT`, `INSERT`) to user `mike`:  
```sql
GRANT SELECT, INSERT ON orders TO mike;
```
Revoke only `INSERT` permission:  
```sql
REVOKE INSERT ON orders FROM mike;
```

---

## **⚠️ Best Practices**  
✔️ Grant only **necessary** permissions.  
✔️ Regularly **review and revoke** unused privileges.  
✔️ Use **roles** instead of individual user grants for easier management.  

---

## **📌 Conclusion**  
DCL commands help maintain **data security** by controlling user access. Always ensure permissions align with business needs!  
