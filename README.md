# PREDATOR-milestones
Deliverables for PREDATOR project milestones.

The [notebooks](https://github.com/INFN-PREDATOR/PREDATOR-milestones/tree/main/notebooks) folder contains browser-executable Jupyter notebook showcasing
the deliverables planned for the milestone M1 of the project. Specifically:

* Milestone M1 - development of a computational framework for quantitative MR reconstruction.
    - M1a: implementation of data I/O routines. 
    - M1b: implementation of MR encoding operators.
    - M1c: implementation of the main regularizers and solvers for iterative reconstruction.
    - M1d: implementation of a numerical Bloch simulator for synthetic data generation and parameter fitting.

Milestone M2 consisted in the creation of a database of quantitative maps (T1, T2, T2*) of at least 10 subjects
to be used for synthetic data generation for DL-based reconstruction training.

The database was built as follows:

1. Whole-head quantitative data (MP2RAGE-based T1 mapping, MRF-based M0/T2 mapping and multi-echo GRE-based T2* mapping, resolution: 0.8-1.1 mm), together with high-resolution (0.8 mm) anatomical images (T1w and T2*w), were collected for 10 healthy subjects using 3T and 7T MRI scanners (GE HealthCare).
2. Anatomical images were resampled to 0.5mm, and a super-resolution template was built using ANTs (nonlinear registration).
3. Sub-millimetric quantitative parameter distributions were obtained by aligning the parametric maps to the anatomical template space.
4. A 25-subjects 0.5mm isotropic whole head quantitative dataset (PD, T1, T2, T2*) was built by aligning our anatomical template to the [Open Science CBS Neuroimaging](https://www.sciencedirect.com/science/article/pii/S1053811915007612) database and using our parameter distribution to create realistic randomized quantitative maps with different anatomical features.

The database can be freely downloaded on the [PREDATOR project OSF repository](https://osf.io/qkbca/).

