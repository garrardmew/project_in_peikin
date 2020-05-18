This is the dorectory including data and code.
data:
	3374_samples_1000_estimators_selected_snp_1000gene_from_19708_57753.csv: training data before gege seleciton
	merged_label_of_cancer.csv:  lable of training data
	rf--max_features_auto--n_estimators_1000_first500_intersected_500.genes: selected 500 genes
code:
	ChooseMostImportantGenes.py: code for gene selection
	ClassifyBySklearn.py: code for classificaiton

feature selection:Using the code as follows. -N,where N represents the number of genes that you wanna choose.  You can also use code :python ChooseMostImportantGenes.py -h (for more informaiton of usage)
python ChooseMostImportantGenes.py -t 3374_samples_1000_estimators_selected_snp_1000gene_from_19708_57753.csv -G merged_label_of_cancer.csv -m rf -N 100 -c 100  -n 1000 -v 10 




classifying: Using the code as follows. You can also use code :pythonClassifyBySklearn.py -h (for more informaiton of usage)
python ClassifyBySklearn.py -G merged_label_of_cancer.csv -t 3374_samples_1000_estimators_selected_snp_1000gene_from_19708_57753.csv -V 10 -v 10 -g rf--max_features_auto--n_estimators_1000_first500_intersected_500.genes -m logistic -C 10000 -c 100 -n 2000