# CELLECT-MAGMA-ANALYSIS
Repository for hosting the web application I developed during my Master's thesis at Lundbeck.  

## Explanation of the Application's Purpose
The application has been developed to investigate the output of another computational toolkit named [**CELLECT**](https://github.com/perslab/CELLECT). In short, CELLECT takes as input GWAS data (e.g. for a particular disease of interest) and integrates it with gene expression specificity data (generated by another related toolkit, [**CELLEX**](https://github.com/perslab/CELLEX)) to identify and prioritize likely cell types involved in the etiology of the disease in question. CELLECT can achieve this prioritization of likely disease-related cell types by using one of two genetic prioritization models. One of these models, **MAGMA**, is the basis of the output generated to be used with the web application in this repository.  

The application was developed and tested in R (version 4.x.x), using the Shiny framework.  

## Getting the Required Input Data
For more info on getting the necessary input data for the application, please see either the **Help** tab when running the application or the Wiki pages of this repository.  
**NB:** The Wiki pages have not been created yet - will be updated soon.

## Running the Application  
This section describes what you need to run the application.  

### Prerequisites  
- **R version:** 4.x.x
- **Shiny:** Install using this command: `install.packages("shiny")`
- **Bioconductor packages:**  
First, install the _BiocManager_ package: `install.packages("BiocManager")`  
Then, install the _biomaRt_ package: `BiocManager::install("biomaRt")`  
- **Other packages:** Will be downloaded as necessary when running the application.

### Running the Application Locally
To run the application locally, you just need to run the following command:  
```R
runGitHub("cellect-magma-analysis", "Mporse")
```
The first time you're running this, R will automatically download the required packages used by the application (except for the _biomaRt_ package, since it is part of Bioconductor - see the **Prerequisites** part above for more info).

### Running the Application as an Online Service  
**FYI:** As described above, this application was designed to be run locally, however it is also possible to host the application online. Some of the more direct solutions are the following:
- [**Shinyapps.io**](https://www.shinyapps.io/): Easy deployment in a few minutes, easily shareable with others, and with free tiers available, however limited in terms of scaling.
- [**Shiny Server**](https://www.rstudio.com/products/shiny/shiny-server/): Open source, however requires you to use your own server for hosting.
- [**RStudio Connect**](https://www.rstudio.com/products/connect/): Easy deployment, easily shareable with others, good for collaboration, and supports other programming languages and database systems, however is pricy and mostly intended for organizations.

## Disclaimer
The application is still very much a prototype, and if you try to run the analysis without providing the proper input, it will likely freeze up.  
In any case, if the application locks up, try to refresh the page or restart application.

## Credits
The tool makes use of ESµ values from the CELLEX tool, as well as output from the CELLECT tool:
- **GitHub:** https://github.com/perslab/CELLEX & https://github.com/perslab/CELLECT
- **Journal article (P. N. Timshel, J. J. Thompson, and T. H. Pers):** https://elifesciences.org/articles/55851
