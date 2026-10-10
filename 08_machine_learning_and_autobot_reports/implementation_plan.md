# Autonomous Work Plan: Project Audits, LinkedIn Series, Commercial Packages & 20 Kaggle Educational Notebooks

## Overview
This multi-phase plan addresses all requested tasks autonomously during the 5+ hour overnight period:
1. **Screen / Sleep Daemon Verification**: Ensure `keep_awake.ps1` runs continuously to prevent screen/system sleep.
2. **Project Inspection & Documentation Discovery**: Audit `rlpcb`, `rlcad`, `autobot`, `proq`, and other projects in `personal projects` to locate existing documentation, architecture summaries, benchmark outputs, and visual assets.
3. **LinkedIn 4-Part Article Series**:
   - **Article 1: RLPCB** (Reinforcement Learning for PCB Component Placement & Trace Routing).
   - **Article 2: RLCAD** (Autonomous CAD Geometry & Parametric Constraint Synthesis).
   - **Article 3: AutoBot in the Wild (12 Hours on Kaggle)**: Plain English, zero AI-slop narrative of what actually happened, what the competitions are, what scores were reached, and what it means.
   - **Article 4: AutoBot as the Unified Autonomous Engineering Controller** (Bridging RLPCB, RLCAD, and ML workflows under one agentic architecture).
4. **Commercial Project Audit & Outbound Outreach Masterfile**:
   - Inspect all 42 personal project directories (e.g. `proq`, `care-connect-network`, `transitika`, `uniNest`, `kenya-camera-ai`, `kahawaconnect`, `gemfin`, `edureach`, etc.).
   - Identify commercializable / high-value saleable projects.
   - Create one comprehensive master file (`commercial_projects_and_outreach.md`) containing project overviews, target customer personas/industries, contact emails/leads, ready-to-send email pitches, LinkedIn/Instagram DM templates, and demo asset links.
5. **20 Foundational Educational Kaggle Notebooks**:
   - Create 20 clean, modular, teachable notebooks using competition data and core machine learning fundamentals.
   - Each notebook includes rich visual image printing, clear intuitive explanations, and focused code covering essential techniques (EDA, augmentations, slice extraction, attention maps, tabular embeddings, metric evaluation, etc.).

---

## Detailed Execution Phases

### Phase 1: Keep-Screen-Awake Verification
- Verify running daemon `keep_awake.ps1` (`task-22117`).

### Phase 2: Codebase & Asset Deep Dive
- Inspect `rlpcb/` and `rlcad/` for existing docs, reports, evaluation plots, and images.
- Inspect `autobot/` telemetry and run history for empirical 12-hour Kaggle data.
- Survey all projects in `personal projects/` (`proq`, `transitika`, `care-connect-network`, `uniNest`, `kenya-camera-ai`, `kahawaconnect`, `gemfin`, `edureach`, etc.) to catalog status, features, and target markets.

### Phase 3: Writing the 4 LinkedIn Articles
- Formatted in clean markdown with human, clear, non-slop engineering voice.
- Direct technical and practical breakdown with image references.
- Articles saved in `content/linkedin_articles/`.

### Phase 4: Commercial Audit & Outbound Master Document
- Written to `commercial_projects_and_outreach.md`.
- Includes elevator pitch, market fit, target decision makers, outbound email sequences, and social media copy for each saleable project.

### Phase 5: Generating the 20 Educational Kaggle Notebooks
- Create directory `educational_notebooks/`.
- Generate 20 complete, standalone, runnable Jupyter Notebooks (`.ipynb`) with markdown commentary and code:
  1. `01_medical_mri_3plane_visualizer.ipynb` (Loading and viewing Sagittal, Coronal, Axial DICOMs)
  2. `02_mass_spec_peak_processing.ipynb` (Peak centroiding, m/z binning, spectral plotting)
  3. `03_arc_grid_transformations_visualized.ipynb` (Color palettes, geometric rotations, symmetry checks)
  4. `04_dicom_windowing_and_hu_scaling.ipynb` (Bone vs soft tissue windowing)
  5. `05_medical_image_augmentations.ipynb` (Albumentations: elastic transforms, affine, noise)
  6. `06_multilabel_class_imbalance_strategies.ipynb` (Asymmetric loss, focal loss, positive weights)
  7. `07_attention_map_visualizer.ipynb` (Grad-CAM / ViT attention rollout on knee MRIs)
  8. `08_molecular_fingerprinting_rdkit.ipynb` (Morgan fingerprints, MACCS keys, Tanimoto similarity)
  9. `09_mri_2p5d_slice_stacking.ipynb` (Grouping adjacent slices into 3-channel representations)
  10. `10_confusion_matrix_and_roc_auc_deep_dive.ipynb` (Threshold sweeps, ROC curves, Macro AUC)
  11. `11_out_of_fold_cross_validation_mastery.ipynb` (GroupKFold vs StratifiedKFold implementation)
  12. `12_feature_importance_and_shap_analysis.ipynb` (SHAP summary plots for tabular and spectroscopy)
  13. `13_image_patching_and_vision_transformer_basics.ipynb` (Breaking 2D slices into patches)
  14. `14_text_report_clinical_negex_parser.ipynb` (Clinical negation windowing on medical reports)
  15. `15_test_time_augmentation_tta_visualizer.ipynb` (Flip/shift TTA impact on prediction confidence)
  16. `16_hierarchical_clustering_chemical_spectra.ipynb` (Dendrograms and spectral clustering)
  17. `17_contrastive_learning_simclr_concepts.ipynb` (Augmentation pair visualization for self-supervised learning)
  18. `18_metric_learning_and_embeddings_tsne.ipynb` (t-SNE and UMAP feature projections)
  19. `19_learning_rate_schedulers_in_practice.ipynb` (Cosine annealing vs OneCycleLR visual comparison)
  20. `20_model_ensembling_and_rank_averaging.ipynb` (Probability calibration, rank blending, voting)
