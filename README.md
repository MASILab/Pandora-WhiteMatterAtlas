# Pandora-WhiteMatterAtlas

## Abstract
While a few white matter atlases do exist based on diffusion MRI fiber tractography, they are often limited to descriptions of white matter as spatially separate “regions” rather than as white matter “bundles” or fascicles, which are well-known to overlap throughout the brain. 

Pandora is a new population-based collection of white matter atlases represented in both volumetric and surface coordinates in a standard space. These atlases are based on 2443 subjects, and include 216 white matter fascicles derived from 6 different state-of-the-art tractography techniques: AFQ, AFQclipped, Recobundles, TractSeg, Tracula, and Xtract. Because these pathways may overlap, these atlases are represented as 4D volumes where each probabalistic segmentation is seperated across the 4th dimension.

These subjects scans are of all healthy adults and were drawn from three datasets: Human Connectome Project (HCP), Baltimore Longitudinal Study of Aging (BLSA), and Vanderbilt University (VU). 

![Pipeline](https://github.com/MASILab/Pandora-WhiteMatterAtlas/blob/master/figures/pipeline.tif)

## Organization
A directory exists for each of the 6 methods. Within each are the corresponding 4D probablistic atlas created using all datasets, a csv file which describes the bundles within the atlas, and a supplementary folder which contains three similar atlas which were created using data from only one of the datasets (HCP, BLSA, VU).

    .
    ├── ...
    ├── Method                       # One of the 6 tractography methods
    |   ├── Method.nii.gz            # 4D Atlas using all datasets
    │   ├── Method_info.csv          # Description of each bundle in the atlas
    │   ├── supplementary
    |   |   ├── Method_HCP.nii.gz    # 4D Atlas using the HCP datasets
    |   |   ├── Method_BLSA.nii.gz   # 4D Atlas using BLSA datasets
    |   |   ├── Method_VU.nii.gz     # 4D Atlas using VU datasets
    |   |   └── ...   
    |   └── ...   
    └── ...   
