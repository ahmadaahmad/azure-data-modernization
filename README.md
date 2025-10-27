
## **⚙️ Pipeline Description**
1. **Source Dataset**  
   - Reads a CSV file from **Blob Storage** (e.g., `rawdata/SalesData.csv`).  
   - Connection defined via **Linked Service** to your blob container.  

2. **Mapping Data Flow**  
   - Performs data transformations such as:  
     - Adding additional columns (Cost,  Unit Price)
     - Add **parameterization** for dynamic file paths
     - Split source file by Category column (Technology, Others)
       
3. **Sink Dataset**  
   - Writes the cleansed output file to:  
     ```
     /salesdatacontainer/Sample - Superstore_Others.csv',
     /salesdatacontainer/Sample - Superstore_Technology.csv',
     ```
   - Stored in the same container as the source file.  

---

## **🖼️ Screenshots**
**ADF Pipeline Overview**  
![image](https://github.com/user-attachments/assets/fd20ab76-1081-4ba8-a813-a4ceb5fe8c7e)


**Data Flow Transformations**  
<img width="2193" height="1108" alt="image" src="https://github.com/user-attachments/assets/f95a862a-fe29-4f52-9b39-4c2b3c13ae20" />


**Blob Storage Output**  
<img width="2388" height="732" alt="image" src="https://github.com/user-attachments/assets/71ce1155-1a87-48d7-9296-fa31c6e4b864" />


---

## **🚀 Outcome**
- Raw CSV files are automatically cleaned and standardized.  
- Output is uniquely named under the same directory as source file in Blob Storage.  
- The pipeline can easily scale to process multiple files or be scheduled for daily automation.  

---

## **📄 Key Learnings**
- How to integrate **Blob Storage** with **ADF pipelines**  
- How to use **Mapping Data Flows** for visual, code-free data transformations  


---

