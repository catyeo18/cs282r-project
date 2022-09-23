# Segmentation as Auxiliary Information for Reducing Spurious Correlations

Harvard CS 282r Final Project: Catherine Yeo & Zev Nicolai-Scanio

Deliverables:
- [Project paper](CS_282r_Project_Paper.pdf)
- [Project poster](CS_282r_Project_Poster.pdf)
- [Initial project proposal](CS_282r_Project_Proposal.pdf)

Brief runthrough of the notebooks in `notebooks/`:
- `data_read.ipynb`: Super quick exploration of the Waterbirds data.
- `data_generation.ipynb`: Generate a Waterbirds dataset with a train/val/test split and a specified correlation for the confounder (i.e. the correlation between background and bird type). Can be set to do various augmentations such as applying noise to the backgrounds, adding segmentations masks as a 4th input channel, or adding segmentation masks as a secondary label. Also generates example images and calculate distance metrics between noise types.
- `finetuning.ipynb`: We finetuned Resnet50 on our augmented datasets.
- `segmentation_as_input.ipynb`: The code is similar to `finetuning.ipynb`, but with 1 more image channel added.
- `segmentation_as_output.ipynb`:  Incomplete progress, we never got around to finishing building this successfully. Idea more fleshed out in Project Proposal.
- `data_visualization.ipynb`: Our notebook for generating a few Seaborn visualizations. (Uses CSV files that we compiled our experimental results into.) 
