# Pandora-WhiteMatterAtlas

## Pandora white matter atlas
Pandora is a new population-based collection of white matter atlases, represented in both volumetric and surface coordinates in a standard space. These atlases are based on 2443 subjects, and include 216 white matter fascicles derived from 6 different state-of-the-art tractography techniques: AFQ, AFQclipped, Recobundles, TractSeg, Tracula, and Xtract. Because these pathways may overlap, these atlases are represented as 4D volumes where each probabalistic segmentation is seperated across the 4th dimension.

These subjects scans are of all healthy adults and were drawn from three datasets: Human Connectome Project (HCP), Baltimore Longitudinal Study of Aging (BLSA), and Vanderbilt University (VU). 

<p align="center">
    <img src="https://github.com/MASILab/Pandora-WhiteMatterAtlas/blob/master/figures/pipeline.png?raw=true")
</p>
    
## Organization
A directory exists for each of the 6 methods. Within each are the corresponding 4D probablistic atlas created using all datasets, a csv file which describes the bundles within the atlas, and a supplementary folder which contains three similar atlas which were created using data from only one of the datasets (HCP, BLSA, VU). Additionally, a similar directory exists for template T1 images which are created from the same subject data as the corresponding atlases. 

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

## Reference
A manuscript is currently in preparation, and will be submitted shortly. 
