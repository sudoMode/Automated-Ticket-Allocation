# Automated Ticket Allocation

---

This project aims to provide an effective solution to the mundane task of assigning user
tickets to relevant support groups. This is supposed to be a generic solution that can be
applied to custom datasets from different platforms such as ZenDesk, AzureDesk or 
ServiceNow.

## Get Started
- Sample dataset(incidents.csv) given in the "data" directory can be used to understand the
flow of the code and test pre-trained model(available in the "data" directory).
- Project is divided into 3 Jupyter notebooks to allow for user customisation, these should
be used in a specific sequence:

### EDA
    - This file provides code for data exploration, helps us spot key features from in the
      data.
    - Idea is to feed the dataset as an input to this file and observe common patterns as
      well anamolies in the data.

### Feature Engineering
    - Use the insights gained after EDA and then trigger this file to extract features
      from the dataset against which the model can be trained.
    - Specify any acronyms or words explicitly as reserved keywords, if you wish to
      emphasise on them(should be discovered in EDA).

### Incident Allocation
    - Once a feature set has been generated, this file will help us train and generated
      models that will be capable of predicting a target "Assignment Group".
    - Validate your results based on your training & testing set and improvise as needed.


## An exception
    - A simple rule based approach can also be taken to further simplify the process in
      some special cases, to be able to do that refer to the fourth file called
      "deterministic_rules.ipynb"

