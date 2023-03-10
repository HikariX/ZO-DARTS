#  ZO-DARTS

## Basic Info

This code repository is prepared for *ZO-DARTS: DIFFERENTIABLE ARCHITECTURE SEARCH WITH ZEROTH-ORDER APPROXIMATION*, which will be published in ICASSP 2023 soon. We implement our algorithm and other algorithms used for comparison on NAS-Bench-201 based on the repository https://github.com/D-X-Y. We express our gratitude to the owner of this repository.

## Modified & added files

**ZO-DARTS/exps/NAS-Bench-201-algos/:**

ZO-DARTS.py

iDARTS.py

MiLeNAS.py

PCDARTS.py

PCDARTS-OURS.py

DARTS+.py

**ZO-DARTS/xautodl/models/cell_searchs:**

search_cells_pcdarts.py

search_model_pcdarts.py

## Main body of ZO-DARTS

We implement our ZO-DARTS in ZO-DARTS/exps/NAS-Bench-201-algos/ZO-DARTS.py based on DARTS-V2.py. Important functions are listed as below.

1. _generate_z

   This function is used for generating direction vector (u) in line 2 of Algorithm 1 from our paper.

2. _prepare_distrubance

   This function is used to generate the disturbed model weights and architecture parameters. Plz refer to line 3 of Algorithm 1 from our paper.

3. _backward_step_ours

   This function is defined for calculating approximated gradients of $\alpha$, as stated in line 9 of Algorithm1 from our paper.

4. search_func_ours_F

   This function forms the framework of the searching process defined in Algorithm 1 adn invokes functions mentioned above.

## How to execute

Use the command below can start the search process of ZO-DARTS:

```
python ZO-DARTS/exps/NAS-Bench-201-algos/ZO-DARTS.py
```

Running this command starts ZO-DARTS, but you can change 'ZO-DARTS.py' to other files to reproduce search process of different algorithms. You can also refer to https://github.com/D-X-Y for some implementation and execution details.
