### Income Estimator Database Creation Exercise

#### Overview:
In this exercise, we'll create a database for a monetary income estimation model. We'll utilize data from the National Household Survey for the years 2018 and 2019. The database will focus on household members as the unit of analysis.

#### Steps:
1. **Data Download**
   - Access the [link](https://proyectos.inei.gob.pe/microdatos/) to download the National Household Survey (ENAHO) data for 2018 and 2019.
   - Download modules 1 (Housing and Household Characteristics), 2 (Characteristics of Household Members), 3 (Education), 4 (Health), and 5 (Employment and Income), and organize them in your working directory.

2. **Module 1 Processing - Housing and Household Characteristics**
   - Create new variables:
     - Department as a string variable from UBIGEO.
     - water_supply: a dummy variable (1 if household has potable water, 0 otherwise).
     - electricity: a dummy variable (1 if household has electric lighting, 0 otherwise).
     - phone: a dummy variable (1 if household has a landline, 0 otherwise).
     - cellphone: a dummy variable (1 if household has a cellphone, 0 otherwise).
     - tv: a dummy variable (1 if household has a TV, 0 otherwise).
     - internet: a dummy variable (1 if household has internet, 0 otherwise).
   - Save the file in your preferred format as "module_1_preprocessed_year" for each year.

3. **Module 2 Processing - Characteristics of Household Members **
   - Create new variables:
     - male: a dummy variable (1 if reported sex is male, 0 if female).
     - age: a numeric variable reporting the age of household members in years.
     - married: a dummy variable (1 if household member is married, 0 otherwise).
   - Save the file in your preferred format as "module_2_preprocessed_year" for each year.

4. **Module 3 Processing - Education **
   - Create new variable:
     - education: an ordered categorical variable (1 for no education, 2 for basic education, 3 for higher education, 4 for master's/doctorate).
   - Save the file in your preferred format as "module_3_preprocessed_year" for each year.

5. **Module 4 Processing - Health **
   - Create new variables:
     - chronic_disease: a dummy variable (1 if household member has a chronic disease, 0 otherwise).
     - essalud_insurance: a dummy variable (1 if household member is affiliated with EsSalud, 0 otherwise).
     - private_insurance: a dummy variable (1 if household member is affiliated with private insurance, 0 otherwise).
     - eps_insurance: a dummy variable (1 if household member is affiliated with an EPS, 0 otherwise).
     - police_insurance: a dummy variable (1 if household member is affiliated with police insurance, 0 otherwise).
     - sis_insurance: a dummy variable (1 if household member is affiliated with SIS, 0 otherwise).
   - Save the file in your preferred format as "module_4_preprocessed_year" for each year.

6. **Module 5 Processing - Employment **
   - Create new variables:
     - company_size: an ordered categorical variable (1 for companies with 0-50 employees, 2 for 51-100 employees, 3 for 101-500 employees, 4 for over 500 employees).
     - formality: a dummy variable (1 if member is formally employed, 0 otherwise).
     - monthly_income: a continuous numeric variable constructed from specified variables and adjusted to 2019 inflation.
   - Save the file in your preferred format as "module_5_preprocessed_year" for each year.

7. **Data Merging **
   - Merge datasets by year, starting with household member data, then merge household member data with household-level data (module 1).
   - Concatenate the files for the years 2018 and 2019.
   - Export the file in your preferred format as "enaho_processed_18_19".

8. **Statistics and Deliverables **
   - Variable dictionary (name and description) in a PDF file.
   - Summary statistics table of variables in the final database, exported as an Excel file.
   - Additional tables in Excel files:
     - Average, minimum, and maximum income per year.
     - Average, minimum, and maximum income per year and sex.
     - Average income by informality status and sex.
     - Average age by informality status.

Enjoy the exercise!
