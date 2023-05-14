# Sequence-of-treatments

Project Description:  
 
This project focuses on adapting the SurviTE machine learning technique for survival analysis to handle sequences of treatments, specifically in the context of cancer patients. Survival analysis models the time to an event, such as patient mortality. The goal is to predict the effect of treatment sequences on survival outcomes for cancer patients while addressing time-dependent confounding. Time-dependent confounding arises from treatment assignment being influenced by previous treatments. The project aims to integrate techniques for handling time-dependent confounding into SurvITE and empirically evaluate its ability to accurately predict treatment effects and address confounding issues. An LSTM model is utilized to predict the binary variable 'recovery_flags' for cancer patients in the context of survival analysis. 
 
Dependencies:  
 
This model was implemented in Pyhton 3.9.16. The following packages are 	needed for running this model:  
NumPy version: 1.24.3 
Pandas version: 2.0.1 
TensorFlow version: 2.11.0 
 
Usage Guide: 

This repository contains the code for an LSTM model that predicts the binary variable ‘recovery_flags’ where 1 stand for ‘recovered’ and 0 stand for ‘not recovered’. To obtain the results from the model, simply run the provided script. 
This repository also includes the script that predicts hazard functions for a specific patient, which can be chosen by the user. This functionality is implemented in the file ‘Collect_probs.ipynb’.  
This repository also contains ‘cancer_simulation’ file that was used to generate dataset used in the analysis. This file was retrieved from 8.b. That means that you might need some extra adjustments to your libraries in order to be able to simulate the data set. Additionally, we changed the seed value in ‘cancer_simulation’ file from 100 to 200 in order to create more positive recovery flags. This variable was highly unbalanced.  
The last file in the repository is ‘Time-depending confounder' which contains the code attempting to address time-dependent confounding.
 
Contribution Guidelines:  

Time Dependent Confoundig: this repository contains a code that attempts to address the problem of time-dependent confounding; however, the results are not promising. Therefore, any suggestions for possible solution to this problem are highly welcome. 
Censoring: this repository does not contain any code that addresses the problem of censoring. Therefore, any suggestion on how to deal with censoring are also welcome. Eventueel nog verder uitschrijven: Encourage and guide potential contributors to the project. Describe how they can contribute, including details on how to report issues, suggest improvements, or submit pull requests. 
 
Contact Information:  
 
Chiril Erosenco:  
- Email: kiril.erosenco@yahoo.be 
- LinkedIn: linkedin.com/in/chiril-erosenco-77346a1b2
 
Mehdi Chouachoua Bouali:
- Email: mehdi.chouachoua@gmail.com 
- LinkedIn: https://www.linkedin.com/in/chouachoua/ 
 
Thomas Boonen:  
- Email:  
- LinkedIn 
 
Acknowledgments:  

We would like to thank our supervisor Toon Verschueren and our promotor professor Bart Baesens for guiding us through this project.  
 
Related Projects or References:  

SurvITE: https://github.com/chl8856/survITE 
Learning Heterogeneous Treatment Effects from Time-to-Event Data 
Authors: Alicia Curth*, Changhee Lee*, and Mihaela van der Schaar (* co-first authors) 
 
CRN (Counterfactual Recurrent Network): https://github.com/ioanabica/Counterfactual-Recurrent-Network 
@article{bica2020crn, 
  title={Estimating counterfactual treatment outcomes over time through adversarially balanced representations}, 
  author={Bica, Ioana and Alaa, Ahmed M and Jordon, James and van der Schaar, Mihaela}, 
  journal={International Conference on Learning Representations}, 
  year={2020} 
} 
 
 
