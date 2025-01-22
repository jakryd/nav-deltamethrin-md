The data includes the results of molecular dynamics trajectories and docking, as described in the upcoming paper:

*Cytochrome P450 inhibition impedes pyrethroid effect through Nav channel regulation*

by Beata Niklas, Eléonore Moreau, Caroline Deshayes, Jakub Rydzewski, Milena Jankowska, Jacek Kęsy, Ademir J. Martins, Pie Müller, Vincent Corbel, Wieslaw Nowak & Bruno Lapied.

All simulations are calculated using Gromacs patched with the PLUMED plugin.

___

In the `docking` directory, there are the lowest-energy poses of deltamethrin found in the open and inactivated state PaNav1 models.

The `wtm-simulations` directory contains the following results of well-tempered metadynamics (WTM) simulations to study the dissociation of Nav channel and deltamethrin:

- The trajectories are initiated from the deep and shallow binding pose in `deep-bind-pocket` and `shallow-bind-pocket`, respectively. In each subdirectory, the inputs for Gromacs are named `wtm.*` and for PLUMED `plumed.dat`. The results are saved in `colvar.dat`.

- For each binding pose, `unbinding-traj` contains 15 short WTM simulations to find dissociation pathways of deltamethrin from the protein.

- In the `fes-in-traj` and `fes-out-traj` directories, there are the results from 300-ns WTM simulations conducted to estimate free-energy profiles. In `fes-in-traj`, the free energy profile is estimated from the shallow binding pose to the center of mass of the protein. In `fes-out-traj`, the free energy profile is calculated from the shallow binding pose toward the protein exterior.
___

Directory structure:
```bash
❯ tree
.
├── README.md
├── docking
│   ├── inactivated-deep.pdb
│   ├── open-deep.pdb
│   └── open-shallow.pdb
└── wtm-simulations
    ├── deep-bind-pocket
    │   ├── unbinding-traj
    │   │   ├── colvar-1.dat
    │   │   ├── colvar-10.dat
    │   │   ├── colvar-11.dat
    │   │   ├── colvar-12.dat
    │   │   ├── colvar-13.dat
    │   │   ├── colvar-14.dat
    │   │   ├── colvar-15.dat
    │   │   ├── colvar-2.dat
    │   │   ├── colvar-3.dat
    │   │   ├── colvar-4.dat
    │   │   ├── colvar-5.dat
    │   │   ├── colvar-6.dat
    │   │   ├── colvar-7.dat
    │   │   ├── colvar-8.dat
    │   │   ├── colvar-9.dat
    │   │   ├── plumed.dat
    │   │   ├── wtm.gro
    │   │   ├── wtm.mdp
    │   │   └── wtm.tpr
    │   └── wtm-index.ndx
    └── shallow-bind-pocket
        ├── fes-in-traj
        │   ├── colvar.dat
        │   ├── plumed.dat
        │   ├── wtm.gro
        │   ├── wtm.mdp
        │   └── wtm.tpr
        ├── fes-out-traj
        │   ├── colvar.dat
        │   ├── plumed.dat
        │   ├── wtm.gro
        │   ├── wtm.mdp
        │   └── wtm.tpr
        ├── unbinding-traj
        │   ├── colvar-1.dat
        │   ├── colvar-10.dat
        │   ├── colvar-11.dat
        │   ├── colvar-12.dat
        │   ├── colvar-13.dat
        │   ├── colvar-14.dat
        │   ├── colvar-2.dat
        │   ├── colvar-3.dat
        │   ├── colvar-4.dat
        │   ├── colvar-5.dat
        │   ├── colvar-6.dat
        │   ├── colvar-7.dat
        │   ├── colvar-8.dat
        │   ├── colvar-9.dat
        │   ├── plumed.dat
        │   ├── wtm.gro
        │   ├── wtm.mdp
        │   └── wtm.tpr
        └── wtm-index.ndx

9 directories, 53 files
```

___

For further information about the data, contact Jakub Rydzewski (<jr@fizyka.umk.pl>).