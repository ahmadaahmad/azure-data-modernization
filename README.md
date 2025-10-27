
## **⚙️ Pipeline Description**
1. **Source Dataset**  
   - Reads a CSV file from **Blob Storage** (e.g., `rawdata/SalesData.csv`).  
   - Connection defined via **Linked Service** to your blob container.  

2. **Mapping Data Flow**  
   - Performs data transformations such as:  
     - Trimming spaces  
     - Converting text to **UPPERCASE**  
     - Removing duplicates  
     - Replacing nulls or invalid values  

3. **Sink Dataset**  
   - Writes the cleansed output file to:  
     ```
     cleansed/SalesData_Cleansed.csv
     ```
   - Stored in the same container as the source file.  

---

## **🖼️ Screenshots**
**ADF Pipeline Overview**  
![ADF Pipeline](images/adf_pipeline_overview.png)

**Data Flow Transformations**  
![ADF Data Flow](images/adf_dataflow.png)

**Blob Storage Output**  
![Cleansed Data](images/blob_output.png)

---

## **🚀 Outcome**
- Raw CSV files are automatically cleaned and standardized.  
- Output is organized under a dedicated `cleansed` directory.  
- The pipeline can easily scale to process multiple files or be scheduled for daily automation.  

---

## **📄 Key Learnings**
- How to integrate **Blob Storage** with **ADF pipelines**  
- How to use **Mapping Data Flows** for visual, code-free data transformations  
- How to maintain a clear folder structure for raw and cleansed data  

---

## **💡 Next Steps**
- Add **parameterization** for dynamic file paths  
- Enable **trigger-based automation** for new uploads  
- Extend transformations using **Synapse Serverless SQL** for advanced analytics  
