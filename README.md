# af_cubic_docking

This repository contains data available and explanations of them for the article: 

**Accurate prediction of protein assembly structure by combining AlphaFold and symmetrical docking, Mads Jeppesen and Ingemar André**

Larger files are deposited on [Zenodo](https://zenodo.org/record/8047514) and referenced correspondingly here.  

The repository for EvoDOCK (The software used to run all the simulations) are found on: https://github.com/Andre-lab/evodock.  

The repository also explains how to set up all the necessary input files as well as how to run the simulations as done in the article. 

## Analysis of 111 cubic sequences by AF/AFM

The file `111_cubic_sequence_analysis.csv` contains the results of the AF/AFM analysis. 
It contains the following entries:

* `pdbid`: The PDB id.
* `symmetry`: The symmetry of the PDB.
* `fold`: The fold type that was analysed and run with AF/AFM. "hf" stands for the **h**igheset **f**old. That is the symmetric fold with the highest number.
Two 2-folds were analyzed and are called 2_1 and 2_2 respectively. 
* `multimer`: If the row values come from an AFM run. 
* `best RMSD`: The best RMSD found among all the AF/AFM predictions compared to all native folds.  
* `best avg plddt`: best average plddt found from all AF/AFM predictions.
* `best iptm+ptm`: best ipTM+pTM found from all AFM predictions.
* `best ptm`: best pTM found from all AFM predictions.
* `best iptm`: best ipTM found from all AFM predictions.
* `best RMSD comes from mer`: Which native fold the matches the prediction the best and gives rise to the value in `best RMSD`.
* `symmetrizable`: If the prediction is symmetrizable with Rosetta 
* `sym best total rmsd`: The RMSD of the Rosetta symmetrized structure compared to the prediction. 

## All metric values for Reassembly docking and Complete assembly docking using an EvoDOCK ensemble 

The file `complete_assembly_and_reassembly_metric_data.csv` contains all metric values from the Reassembly and Complete assembly docking simulations.


It contains the following entries:

* `Symmetry`: The symmetry of the structure
* `pdbid`: The PDB id of the structrure. 
* `docking type`: If the simulation was Reassembly or Complete assembly docking. 
* `TMscore`: The TM-score of the structure
* `DockQ`: The DockQ score of the structure
* `RMSD`: The RMSD of the structure
* `type`: if the values come from the Best Ranked or the Best Cluster

## Initial structure lists from the RCSB

The initial list of homomeric I/O/T PDB files downloaded from RCSB is deposited [here](https://zenodo.org/record/8047514) and is called `initial_rcsb_list.tar.gz` 

## Predicted structures from the method

The PDB files of the predicted structures for the Reassembly docking is deposited [here](https://zenodo.org/record/8047514) and is called `reassembly.tar.gz` 

The PDB files of the predicted structures for the Complete assembly docking is deposited [here](https://zenodo.org/record/8047514) and is called `complete_assembly.tar.gz` 
