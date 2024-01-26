![CellFocus](https://github.com/DynamicBiosystems/CellFocus/blob/main/CellFocus.png)

### CellFocus introduction
---

CellFocus is a visualization software for single-cell transcriptome data on the well-paired-seq (WPS) platform. CellFocus includes many interactive visualization functions, such as displaying cell clustering results, showing differential gene tables, presenting gene expression information, and assisting in manual cell type annotation. It can also export images and table data. In summary, it is convenient to explore personalized data and perform manual cell type identification without programming knowledge.

### Manual

---

Detailed operation documents can be found in [here](https://github.com/DynamicBiosystems/CellFocus/blob/main/docs/CellFocus-v1.0.1_operation_manual.pdf).

#### Load data

---

Files with a suffix of cellfocus, which released by Dynamic Biosystems, can import for visualization.

#### Overview

---

Here you can view the dimensionality reduction graph and the meta data information in the data.

- **Main parameters**: 
The elements in this panel allow you to control what and how results are displayed across the whole tab.
    - **Projection**: Select here which projection you want to see in the scatter plot on the right.
    - **Color cells by**: Select which variable, categorical or continuous, from the meta data should be used to color the cells.

- **Additional parameters**: 
The elements in this panel allow you to control what and how results are displayed across the whole tab.
    - **Point size**: Controls how large the cells should be.
    - **Point opacity**: Controls the transparency of the cells.
    - **Show % of cells**: Using the slider, you can randomly remove a fraction of cells from the plot. This can be useful for large data sets and/or computers with limited resources.

- **Group filters**: 
The elements in this panel allow you to select which cells should be plotted based on the group(s) they belong to. For each grouping variable, you can activate or deactivate group levels. Only cells that are pass all filters (for each grouping variable) are shown in the projection.

- **Selections**: 
The elements in this panel allow you to control what and how results are displayed across the whole tab.
    - **Category**: Controls what selected cells are displayed.
    - **Cluster**: Controls what cluster of selected cells are displayed below.
    - **Delete Selection(s)**: Delete cluster which not select in Cluster.

#### Groups

---

The elements in this panel allow you to view composition of groups

- **Composition by other group**: 
This plot allows to see how cell groups are related to each other. This can be represented as a bar char or a Sankey plot. Optionally, a table can be shown below. To highlight composition in very small cell groups, results can be shown as percentages rather than actual cell counts. Groups can be removed from the plot by clicking on them in the legend.

- **Expression metrics**: 
Violin plots showing the number of transcripts (nUMI/nCounts), the number of expressed genes (nGene/nFeature), as well as the percentage of transcripts coming from mitochondrial and ribosomal genes in each group.

#### Most expressed genes

---

Table of top 100 most expressed genes in each group. For example, if gene XY contributes with 5% to the total expression, that means 5% of all transcripts found in all cells of this sample come from that respective gene. These lists can help to identify/verify the dominant cell types.

#### Marker genes

---

CellFocus performs this analysis with the 'FindAllMarkers()' function by Seurat, which compares each group to all other groups combined. Only genes that pass thresholds for log-fold change, the percentage of cells that express the gene, p-value, and adjusted p-values are reported. 

#### Gene(set) expression

---

The elements in this panel allow you to view expression of genes.

- **Main parameters**: 
The elements in this panel allow you to control what and how results are displayed across the whole tab.
    - **Gene(s) / Gene set**: Select whether you would like to select individual genes or gene sets. In the case of 'Gene(s)', you can select one or multiple genes from the input field below. If you select multiple genes, the mean expression across the selected genes will be calculated for each cell. If you select 'Gene set', you can select a gene set from the MSigDB. Species-specific gene names will be tried to retrieve, otherwise gene name matching is attempted. A list of which genes are present or missing in the data set can be found below the projection.
    - **Projection**: Select here which projection you want to see in the scatter plot on the right.

- **Additional parameters**: 
The elements in this panel allow you to control what and how results are displayed across the whole tab.
    - **Plotting order**: Cells can be plotted in random order or so that cells with highest expression are on top.
    - **Point size**: Controls how large the cells should be.
    - **Point opacity**: Controls the transparency of the cells.
    - **Show % of cells**: Using the slider, you can randomly remove a fraction of cells from the plot. This can be useful for large data sets and/or computers with limited resources.

#### Gene ID conversion

---

Conversion table containing Gencode identifiers, Ensembl identifiers, Havana identifiers, gene symbol and gene type for mouse and human.

#### Color managerment

---

The elements in this panel allow you to view hexadecimal color table.

### About

---

CellFocus is developed by dynamic-biosystems Co., Ltd. The official website is [www.dynamic-biosystems](http://www.dynamic-biosystems.com/).





