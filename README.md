# Questioning the influence of roots: A soil fauna perspective on rhizosphere space

This repository contains the R scripts associated with the publication "*Questioning the influence of roots: A soil fauna perspective on rhizosphere space*" currently being written. This study uses high-resolution in situ imaging combined with resource selection function framework to quantify how soil invertebrates organise their activity around roots at the microscopic scale.

## Analytical approach

To answer the question about the fine scale root - fauna spatial relations, we developed an analytical approach that begins with image analysis using deep learning models. For roots analysis, we used a convolutional neural network-based software names RootPainter models (Smith et al. 2022). For invertebrate analysis, we developed a pipeline analysis based on a mathematical detection tool and a deep learning classification tool (Belaud et al., in prep; Hendrikx et al., in prep). We were thus able to generate binary images reflecting root structures and the fauna database, including their taxonomic range and location on the image. For roots, we distinct two functionnal parts - the growing part and the mature parts - by a substraction calcul. Thus, for each roots parts image masks, we generate distance maps (i.e., each pixels of the maps represent the minimum Euclidean distance to a root). We then projected the faunal occurrences on these distance maps to compute distances from each invertebrate to the nearest root. Distance to root was interpreted as habitat use under a Resource Selection Function (RSF) framework (Calenge et al. 2005). Habitat availability was quantified by projecting 50 random points per image onto root distance maps, yielding a null expectation of distances to the nearer root available within each image. Expected mean distances were computed from these random samples. For every image, we compared the observed invertebrate – root distances to this expectation to quantify marginality – a measure of departure from random spatial use of the root environment by inverterbrates. Marginality values wereas averaged per image to control for sampling heterogeneity, and computed independently for Acari, Collembola, Gastropoda, and for all taxa combined.

![Figure illustrating the conceptual and methodological approach](images/analytical-approach.png)

## Data

The data required to generate the results can be downloaded at the following link: [dataverse repository](https://entrepot.recherche.data.gouv.fr/dataset.xhtml?persistentId=doi:10.57745/9VMCNE).
