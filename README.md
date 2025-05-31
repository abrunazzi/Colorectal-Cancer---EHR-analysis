# Colorectal-Cancer---EHR-analysis

## DESCRIZIONE PROGETTO
Questo progetto analizza un dattaset di 999 pazienti affetti da cancro colorettale in stadio IV. Sono stati applicati metodi di machine learning supervisionato, modelli di sopravvivenza (Cox, Aalen), clustering (UMAP, t-SNE, k-means, HAC) e visualizzazioni per identificare fattori clinici e perioperatori associati alla sopravvivenza.



##  per eseguire il codice in RStudio 

Caricamento delle librerie utilizzate nel progetto
* library(glmnet)
* library(survival)library(Matrix)
* library(factoextra)
* library(dplyr)
* library(cluster)
* library(clusterSim)
* library(Rtsne)
* library(umap)
* library(ggplot2)
* library(mice)
* library(performanceEstimation)
* library(pacman)

### PER SCARICARE TUTTE LE LIBRERIE NECESSARIE:

packages <- c("glmnet", "survival", "Matrix", "factoextra", "dplyr", 
              "cluster", "clusterSim", "Rtsne", "umap", "ggplot2", 
              "mice", "performanceEstimation", "pacman")

install_if_missing <- function(pkg) {
  if (!require(pkg, character.only = TRUE)) {
    install.packages(pkg, dependencies = TRUE)
    library(pkg, character.only = TRUE)
  }
}

lapply(packages, install_if_missing)

- glmnet= Per regressioni penalizzate (ridge, lasso) nel modello di Cox per gestire multicollinearità.
- survival = Modelli di sopravvivenza (Kaplan-Meier, Cox) e test log-rank.
- Matrix = Supporto a strutture di dati sparsi richieste da glmnet.
- factoextra = Visualizzazione dei risultati di clustering (ad es. dendrogrammi).
- dplyr = Manipolazione dati e pipe (%>%) per preparare il dataset.
- cluster = Calcolo del silhouette score per valutare la qualità dei cluster.
- clusterSim = Calcolo del Davies-Bouldin index per misurare la qualità del clustering.
- Rtsne = Riduzione dimensionale t-SNE per esplorare la struttura latente dei dati.
- umap = Riduzione dimensionale UMAP per visualizzare le relazioni tra variabili.
- ggplot2 = Creazione di grafici (es. boxplot, istogrammi, scatter plot) per l’esplorazione dei dati.
- mice = Imputazione multipla dei dati mancanti per garantire completezza nel dataset.
- performanceEstimation = Valutazione delle performance dei modelli e gestione degli squilibri nel dataset (es. oversampling).
- pacman = Facilita il caricamento e installazione di più pacchetti con un unico comando.


##   OUTPUT
- `output_dataset.csv`: Cleaned dataset ready for analysis
- Graphical outputs: Kaplan-Meier plots, clustering visualizations, correlation heatmaps
- Model summaries and performance reports, analyzed in my report if needed



#  Citation
Chang, Y.C., et al. (2018). "The effect of epidural analgesia on cancer progression in patients with stage IV colorectal cancer after primary tumor resection: A retrospective cohort study." PLoS ONE 13(7): e0200893.
