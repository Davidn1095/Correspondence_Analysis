# Correspondence_Analysis

## Statistical Analysis using CA and MCA

### Part 1: Correspondence Analysis (CA)
1. **Loading Data:**
   - `datos <- read.table("correspondencias.txt", header = TRUE)`: Reads data from "correspondencias.txt" into `datos`. The file's first row has column names.

2. **Chi-Squared Test:**
   - `chisq.test(datos)`: Performs a Chi-squared test of independence on the `datos` dataset.

3. **Performing Correspondence Analysis:**
   - `acs <- dudi.coa(datos)`: Conducts Correspondence Analysis on `datos`.

4. **Scree Plot Visualization:**
   - `fviz_screeplot(acs, addlabels = TRUE, ylim = c(0, 70))`: Displays a scree plot showing eigenvalues/inertia from the CA.

5. **Accessing CA Results:**
   - Access various CA results such as row weights (`acs$lw`), column weights (`acs$cw`), and coordinates (`acs$li`, `acs$co`).

6. **Biplot Visualization:**
   - `fviz_ca_biplot` functions: Create biplots in different styles to visualize relationships from the CA.

### Part 2: Multiple Correspondence Analysis (MCA)
1. **Loading Dog Breeds Data:**
   - `data("DogBreeds")`: Loads `DogBreeds` dataset.
   - `DogBreeds`: Displays the dataset.

2. **Data Preparation:**
   - `Datosrazas <- DogBreeds[, -7]`: Selects columns from `DogBreeds` for MCA.

3. **Summary of Data:**
   - `summary(Datosrazas)`: Provides a summary of the `Datosrazas` dataset.

4. **MCA Preparation:**
   - Calculation of `Intotal` using predefined `p` and `s` values.

5. **Conducting MCA:**
   - `acm <- dudi.acm(Datosrazas, nf = 10, scannf = FALSE)`: Performs MCA on `Datosrazas`.

6. **Scree Plot for MCA:**
   - `fviz_screeplot(acm, addlabels = TRUE, ylim = c(0, 35))`: Shows a scree plot for the MCA eigenvalues.

7. **Accessing MCA Results:**
   - `acm$li` and `acm$co`: Retrieve row and column coordinates from MCA.

8. **Visualization of MCA Results:**
   - Utilize `fviz_mca_*` functions to create visualizations for MCA results, including biplots and variable contributions.

This analysis helps in understanding the relationships in the data, with visualizations enhancing interpretability.
