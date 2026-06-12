# LEFM
remote sensing visual-language foundation model for Open World Land Entity Representation of Earth Observation


## supplementary info
The curation details of Land Entity Representation Paradigm (LERP), the detail inspection of the established 
Contextualized Knowledge Graph (ECKG), the detail configuration of LEFM and its comparison with the state-of-the-art 
visual-language foundation model, the implementation setting of conceptual grounding pretraining and divide-and-conquer 
fine-tuning, the ablation of primary modules of LEFM, and additional experiment results are provided in the [supplementary file]().

## 🔥 How is the Land Entity Representation Paradigm (LERP) established?
🌍 The curation details of Land Entity Representation Paradigm (LERP) can be found in [Curation details of LERP.xlsx](https://pan.baidu.com/s/1zeU1FyLkK4ICRs0sCXSofQ), code=gt5f, including land entity taxonomy, entity existence types, and the scene in which they might appear, as well as the synonym consolidation details and invalid category names removement.

🌍 The established LERP taxonomy as well as the existence type annotation (i.e., object entity/material entity) can be found in [Land Entity Representation Paradigm (LERP).json](https://pan.baidu.com/s/142Jqn7e41bqTJUS9K6gbdQ),code=tfha, as well as the colortable used in our study can be found in [Land Entity Representation Paradigm (LERP)_colortable.json](https://pan.baidu.com/s/1JaL8gAbasH1I5S9kUpJUjg),code=humk

🌍 The annotation principle of "material entity" and "object entity taxonomy" towards the ambiguous categories can be found in [Ambiguous_categories_explanation.docx](https://pan.baidu.com/s/1TjrQU3ioaN7B9rxNzGaYTQ)，code=b23w, we provide the ambiguity reason and the remote sening-contextualized decision of the existence type for each ambiguous category.

🌍 The statistic of the entity instances of SkySA datasets against the 593 LERP categories is provided in [Entity_instances_statistics in SkySA against 593 categories.json](https://pan.baidu.com/s/1WYGhfGYWSIfrWDHnXYizOw),code=2tsx. Statistically, 48.2% of entity instances in top 10% entity categories, which exhibits a significant long-tail distribution.

<img width="2005" height="1137" alt="数据分布可视化" src="https://github.com/user-attachments/assets/cc58b313-8763-4a85-82e7-7473087ddad6" />
Figure 1. The long-tail distribution of the SkySA datasets against the 593 LERP categories.

🌍 To ensure the completeness and representativeness of the LERP category system in characterizing Earth's surface, the Köppen–Geiger climate classification was adopted as a theoretical foundation to guide the category selection. Under this framework, 95 of the 593 LERP categories (16.0%) are climatically specific, the remaining 498 categories (84.0%) are climatically non-diagnostic. The detailed taxonomic coverage of the LERP against the 30 Köppen–Geiger climate subtypes for each entity categories can found in [Taxonomic coverage_of_LERP (based on Köppen–Geiger).txt](https://pan.baidu.com/s/11eccg_pkdpRsswWiAolkIA),code=i9eg.

<img width="901" height="419" alt="image" src="https://github.com/user-attachments/assets/a97818a6-7562-4c5f-956b-c0f7cda19a3e" />
Figure 2. The taxonomic coverage of the established Land Entity Representation Paradigm against the 30 Köppen–Geiger climate subtypes.


## 🔥 How is the Entity Contextualized Knowledge Graph (ECKG) established?
🌍 The established Entity Contextualized Knowledge Graph (ECKG) is provided in [Entity contextualized knowledge graph (ECKG).xlsx](
https://pan.baidu.com/s/1TWOqVlzKo66Aj2k3qSizbw),code=wdey. 

<img width="883" height="679" alt="image" src="https://github.com/user-attachments/assets/216c8673-2ae9-4ced-879d-2dd5e19ec201" />
Figure 3. Overview of the Entity contextualized knowledge graph, with 574 entity nodes and 2237 edges (weight >0.08) displayed, arc width and color transparency is proportional to the Bayes posterior probability of entity co-occurrence.

## 🔥 What is the land entity recognizability boundary in terms of the spatial resolution of the satellite remote sensing images?
While the proposed model is trained and evaluated primarily on sub-meter imagery (~0.5 m), the recognizability of land entities varies across scales. At ~0.5 m resolution, both object entities (e.g., vehicle, tree, airplane) and material entities (e.g., forest, water) can be effectively distinguished. When the resolution decreases to 10 m (e.g., Sentinel-2), only 20.9% entity types remain recognizable, and only 12% entity types remain when the resolution further degraded to 30m resolution (i.e., Landsat-9). The specific curation of the recognizability boundary for each entity is provided in [LERP_Resolution_Recognizability.xlsx](https://pan.baidu.com/s/1gdxDoNEAdx0WO3xRnk-Omg), code=ewbm.
