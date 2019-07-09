# DTI-CDF
Drug-target interactions play a crucial role in target-based drug discovery and exploitation. Computational prediction of DTIs has become a popular alternative strategy to the experimental methods for identification of DTIs of which are both time and resource consuming. However, the performances of the current DTIs prediction approaches suffer from a problem of low precision and high false positive rate. In this study, we aimed to develop a novel DTIs prediction method, named DTI-CDF, for improving the prediction precision based on a cascade deep forest model which integrates hybrid features, including multiple similarity-based features extracted from the heterogeneous graph, fingerprints of drugs, and evolution information of target protein sequences. In the experiments, we built five replicates of 10 fold cross-validations under three different experimental settings of data sets, namely, corresponding DTIs values of certain drugs (S_D), targets (S_T), or drug-target pairs (S_P) in the training set are missed but existed in the test set. The experimental results show that our proposed approach DTI-CDF achieves significantly higher performance than the state-of-the-art methods.

#-----------------------------------------------------------------------------------------------------------------------------
run processes: Python2.7 environment (NR dataset)
1. pip install -r DTI-CDF_requirements.txt
2. install DTI-CDF/gcforest
3. download data from folder 1_original_data
4. fill the file path in python file (eg. 2_generate_dataset_NR.py and 3_training&test_NR_DTI-CDF.py)
5. python 2_generate_dataset_NR.py
6. python 3_training&test_NR_DTI-CDF.py
 
#-----------------------------------------------------------------------------------------------------------------------------

Note: When installing gcforest, use the code provided by this page, dir：DTI-CDF/gcforest, because the source code has been modified. Also, note that the first line {#y_pred = np.argmax(y_pred_proba, axis=1)} in the xgb_eval_accuracy(y_pred_proba, y_true) function in the DTI-CDF/gcforest/exp_utils.py file is used for tunable parameters, you need to add or remove comments. 
