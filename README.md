Steps Performed

 1. **Importing Dataset**
- Loaded Titanic dataset and displayed initial rows.
- Checked data types and null values using `.info()` and `.isnull().sum()`.

 2. **Handling Missing Values**
- Filled missing values:
  - `Age` → replaced with **median**
  - `Embarked` → replaced with **mode**
  - `Cabin` → created a new binary column `HasCabin` to indicate presence

 3. **Feature Extraction & Encoding**
- Extracted **Title** (Mr, Mrs, Miss, etc.) from the `Name` column.
- Grouped rare titles into 'Other'.
- One-hot encoded categorical columns:
  - `Sex`, `Embarked`, `Title`, and `Ticket_Prefix`

 4. **Ticket Prefix Feature**
- Extracted the prefix from the `Ticket` column (e.g., `PC`, `A/5`, etc.).
- Created a new feature `Ticket_Prefix` and applied one-hot encoding.
- Dropped the original `Ticket` and `Name` columns after extraction.

 5. **Feature Scaling**
- Standardized the `Age` and `Fare` columns using `StandardScaler` from `sklearn`.

 6. **Outlier Detection & Removal**
- Used **boxplots** to visualize outliers in `Age` and `Fare`.
- Applied the **IQR method** to filter out extreme outliers from both columns.

 7. **Boolean Conversion**
- Converted all boolean values (`True`/`False`) to binary (`1`/`0`).

  
