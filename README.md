# -quantum-computational-project-GNN-
R &amp; D project of quantum computational chemistry project using GNN
# this set of code contains solutions for only 2nd and third questions.

# step wise explantion
1. Imports
![image](https://github.com/user-attachments/assets/4c18b75b-5d97-40ee-9638-cf380f24ea76)
Purpose: Importing necessary libraries for handling molecular data, performing machine learning, and visualization.
Explanation: Libraries include RDKit for chemical informatics, Mordred for descriptor calculation, Coulomb Matrix for feature extraction, and TensorFlow/Keras for building neural networks.
2. Check Number of XYZ Files:
   ![image](https://github.com/user-attachments/assets/eabf96a1-105f-4598-802e-0b7099d3db60)
Purpose: Verify the number of XYZ files available for processing.
Explanation: Lists the files in the specified directory and counts them.
3.Read XYZ Files Function:
![image](https://github.com/user-attachments/assets/5b48f5c2-2e26-4f37-a3b3-c5953a764e9c)
We then defined a function read_xyz to parse XYZ files. This function extracts atomic symbols, Cartesian coordinates, SMILES strings, and molecular properties. This process helps in converting raw data into a structured format suitable for further analysis.
4.Read and Extract Data from XYZ Files:
![image](https://github.com/user-attachments/assets/1581c2e4-4396-48e6-bc8f-9de2b00462a6)
Purpose: Collect data from all XYZ files.
Explanation: Reads each file and stores extracted information in lists.

5.Create DataFrame from Properties:
![image](https://github.com/user-attachments/assets/91eb0371-5bee-41b2-858c-d429e8e79127)
Purpose: Create a DataFrame to organize properties and SMILES.
Explanation: Assigns column names and adds SMILES strings.

6. Convert SMILES to Molecule Objects:
   ![image](https://github.com/user-attachments/assets/37dda98f-c80a-49f6-b6d6-234c5b673e94)
Purpose: Convert SMILES strings to RDKit molecule objects.
Explanation: Facilitates further molecular manipulations.

7. Check for Null Molecules:
   ![image](https://github.com/user-attachments/assets/1a293906-0e0f-4db4-86b6-38e987855097)
Purpose: Identify any invalid SMILES that failed to convert.
Explanation: Ensures data integrity by checking for null values.
8. Visualize Molecules:
   ![image](https://github.com/user-attachments/assets/a03a0882-d82c-40c7-b4a2-e4ad8b477390)
Purpose: Draw the first 20 molecules.
Explanation: Provides a visual confirmation of the molecular structures.
9. Get Number of Atoms in a Molecule:
    ![image](https://github.com/user-attachments/assets/471c144d-a5c7-4853-8414-70a7eefa2891)
Purpose: Check the number of atoms in the first molecule.
Explanation: Demonstrates how to extract specific information from molecule objects.
10. Accessing First Entry Data:
    ![image](https://github.com/user-attachments/assets/40a4c670-75b2-4847-abbb-3106f0c4ca2f)
Purpose: View the atoms and coordinates of the first molecule.
Explanation: Provides a quick check on the structure of the stored data.
11. Add Hydrogen Atoms:
    ![image](https://github.com/user-attachments/assets/bb437c75-dc05-4dd5-a6b7-c82afabbdf9f)
Purpose: Ensure all molecules have explicit hydrogen atoms.
Explanation: Adds hydrogen atoms to the molecular structures.
12. Calculate Atom Counts:
    ![image](https://github.com/user-attachments/assets/15731045-a020-4440-b13c-a4a6b30147e5)
Purpose: Calculate the number of atoms and heavy atoms in each molecule.
Explanation: Adds these counts as new columns in the DataFrame.
13. Display Updated DataFrame:
    ![image](https://github.com/user-attachments/assets/e0698700-695c-482e-a2a6-7a74d4684506)
Purpose: Preview the updated DataFrame.
Explanation: Ensures the new columns were added correctly.
14. Canonicalize SMILES:
    ![image](https://github.com/user-attachments/assets/0c61a39f-8250-49f6-acdd-7d058468e131)
Purpose: Generate canonical SMILES for consistency.
Explanation: Standardizes the SMILES strings.
15. Display Updated DataFrame:
    ![image](https://github.com/user-attachments/assets/9a4e3097-dc77-4f16-a3e1-b283cfa99e73)
Purpose: Preview the DataFrame with canonical SMILES.
Explanation: Ensures the new column was added correctly.
16. Convert Specific SMILES to Molecule:
    ![image](https://github.com/user-attachments/assets/f3a463aa-79bc-4a1a-b6ae-256b27232e73)
Purpose: Test conversion of a specific SMILES string.
Explanation: Demonstrates the conversion process.
17. Identify Duplicate Canonical SMILES:
    ![image](https://github.com/user-attachments/assets/7a5c0ada-f9eb-4a7c-bace-c353818c3c71)
Purpose: Identify duplicated canonical SMILES.
Explanation: Checks for duplicate entries in the DataFrame.
18.Locate Specific Canonical SMILES:
![image](https://github.com/user-attachments/assets/1dbcfa46-a168-4e9e-9b05-95d2a738b4c4)
Purpose: Find entries matching a specific canonical SMILES.
Explanation: Provides a way to locate specific molecules.
19. Convert Another SMILES to Molecule:
    ![image](https://github.com/user-attachments/assets/0e228385-dd7b-400b-8bb3-e3340b6f6923)
Purpose: Test conversion of another specific SMILES string.
Explanation: Demonstrates the conversion process.
20. Remove Duplicate Entries:
    ![image](https://github.com/user-attachments/assets/a3e4de09-49e3-4e9d-88a6-95d2466d8584)
Purpose: Remove duplicate entries based on canonical SMILES.
Explanation: Ensures each molecule is unique.
21. Update Molecule Column:
    ![image](https://github.com/user-attachments/assets/95b811f3-4641-4f16-82d3-52b7f8e3b75e)
Purpose: Update the molecule objects with canonical SMILES.
Explanation: Ensures consistency in the DataFrame.
22.   Plot Property Distributions:
![image](https://github.com/user-attachments/assets/fffa02e2-1395-4fda-9a80-cfd466d93308)
Purpose: Visualize the distribution of molecular properties.
Explanation: Plots histograms for each property to understand their distributions.
23. Repeat Property Distributions Plot:
![image](https://github.com/user-attachments/assets/170bd581-ec70-4cf4-9dc1-8ce34f7bbf8b)
Purpose: Repeated plot to ensure completeness.
Explanation: Confirms the distributions are correctly visualized.
24. Save Final DataFrame:
    ![image](https://github.com/user-attachments/assets/ed57d500-4bf8-4c45-a34a-ef119402124e)
Purpose: Save the processed DataFrame to a CSV file.
Explanation: Preserves the data for future use.
25. Check DataFrame Shape:
    ![image](https://github.com/user-attachments/assets/73619fd1-c19c-43a0-bba4-e21f6ee4d793)
Purpose: Verify the dimensions of the DataFrame.
Explanation: Ensures the DataFrame has the expected number of rows and columns.
26. Plot Atom Count Frequency:
   ![image](https://github.com/user-attachments/assets/9ac07e68-3fb7-4908-a8d6-a3d8b541f1f1)
Purpose: Visualize the distribution of molecules by their atom count.
Explanation: Provides insight into the dataset composition.
27. Scatter Plot of Properties vs. Atom Count:
    ![image](https://github.com/user-attachments/assets/defa2d4b-3827-475e-9b5c-b543c277fb68)
Purpose: Analyze the relationship between atom count and molecular properties.
Explanation: Uses scatter plots to visualize correlations and trends.
28. Plot Heavy Atom Count Frequency:
    ![image](https://github.com/user-attachments/assets/655f7e3a-801a-4dd9-9648-e7ccdc5f7e29)
Purpose: Visualize the distribution of molecules by their heavy atom count.
Explanation: Provides additional insight into the dataset composition.
29. Scatter Plot of Properties vs. Heavy Atom Count:
    ![image](https://github.com/user-attachments/assets/d0248774-987e-41da-b082-b759745f1189)
Purpose: Analyze the relationship between heavy atom count and molecular properties.
Explanation: Uses scatter plots to visualize correlations and trends.
30. Calculate Descriptors for Molecules with 19 Atoms:
    ![image](https://github.com/user-attachments/assets/2075d494-e746-47ff-af37-aedcc5656ea1)
Purpose: Calculate molecular descriptors for molecules with 19 atoms.
Explanation: Uses Mordred to generate descriptors and saves the results.
31. Inspect Descriptor DataFrame:
    ![image](https://github.com/user-attachments/assets/40f2d426-f432-4674-8d17-899d0ac1034a)
Purpose: Check the structure and types of the descriptor DataFrame.
Explanation: Ensures the data is correctly formatted.
32. Select Numeric Descriptors:
    ![image](https://github.com/user-attachments/assets/c61024b2-520a-4992-a212-3bef0def7d99)
Purpose: Filter the DataFrame to include only numeric descriptors.
Explanation: Prepares the data for machine learning.
33. Remove Zero-Variance Columns:
     ![image](https://github.com/user-attachments/assets/3aa49d6e-40af-4957-8597-e798467eded8)
Purpose: Remove columns with zero variance.
Explanation: Ensures all features contribute to the model.
34. Normalize Descriptors:
    ![image](https://github.com/user-attachments/assets/f44fc121-1521-447f-ada2-c54252737a73)
Purpose: Normalize the descriptor values.
Explanation: Scales features to a common range for better model performance.
35. Select Properties for Molecules with 19 Atoms:
    ![image](https://github.com/user-attachments/assets/5a1ad865-44fe-400e-9827-dd376a6a57be)
Purpose: Create a subset of the DataFrame with only molecules containing 19 atoms.
Explanation: Prepares the data for machine learning.
36. Split Data for Model Training:
    ![image](https://github.com/user-attachments/assets/23d3b535-b0cd-4c93-99e5-bc98c98a891e)
Purpose: Split the data into training and testing sets.
Explanation: Ensures a fair evaluation of the model.
37. Define Neural Network Model:
  ![image](https://github.com/user-attachments/assets/d8e3eeb0-f194-41ec-bbe0-86089dd5f08f)
Purpose: Define a function to create and train a neural network model.
Explanation: Uses Keras to build and evaluate a neural network
38. Train Neural Network Model:
   ![image](https://github.com/user-attachments/assets/9c16879a-ab51-4fb4-8ec8-13cf12e273fa)
Purpose: Train the neural network on the training data.
Explanation: Uses the defined function to train the model.
39. Print Model Performance:
    ![image](https://github.com/user-attachments/assets/2fa1facd-5a37-4f19-8408-35e01e9255ab)
Purpose: Display the model's mean squared error.
Explanation: Provides a measure of the model's performance.
40. Select Molecules with 19 Atoms:
   ![image](https://github.com/user-attachments/assets/b1f49c42-5fc4-4a5f-afd9-ca43b05f03ef)
Purpose: Filter the data to include only molecules with 19 atoms.
Explanation: Prepares the data for Coulomb matrix calculation.
41. Calculate Coulomb Matrix Eigenvalues:
    ![image](https://github.com/user-attachments/assets/5c198845-616a-4641-a157-4715f6d44175)
Purpose: Calculate Coulomb matrix eigenvalues for feature extraction.
Explanation: Uses molml to compute the features and stores them in a DataFrame.
42. Normalize Coulomb Matrix Features:
    ![image](https://github.com/user-attachments/assets/177a8649-6476-4e8c-a5d9-cc8e00795553)
Purpose: Normalize the Coulomb matrix features.
Explanation: Scales features to a common range for better model performance.
43. Split Coulomb Matrix Data for Model Training:
      ![image](https://github.com/user-attachments/assets/291744df-cf8f-4f3d-a77f-a81daa1dc28f)
Purpose: Split the data into training and testing sets.
Explanation: Ensures a fair evaluation of the model.
44. Train Neural Network on Coulomb Matrix Data:
      ![image](https://github.com/user-attachments/assets/b8d29983-f4a3-4ab2-abbd-cc630c7276c2)
Purpose: Train a neural network on the Coulomb matrix features.
Explanation: Uses the defined function to train the model on new features.
45. Print Coulomb Matrix Model Performance:
     ![image](https://github.com/user-attachments/assets/c1884d17-f5db-473f-a4b9-401d984dddb6)
Purpose: Display the model's mean squared error for Coulomb matrix features.
Explanation: Provides a measure of the model's performance.


    
