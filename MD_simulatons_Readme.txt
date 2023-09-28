MD_simulatons
   |
   |-MD_simulations_300K
           |-Random_compositions
           |       |-Fe0.5V0.75
           |            |-Simulation 1   >>> files: 2 .meam, 1 lammps .in, 1 .py
           |            |    | (Run .py code using play button in spyder to create 39 dir's)
           |            |    |-Simulation_lattice_a0(39 lattices)
           |            |    |       :
           |            |    |-Simulation_lattice_a39
           |            |
           |            |-Simulation 2  >>> files: 2 .meam, 1 lammps .in, 1 .py
           |            |-Simulation 3  >>> files: 2 .meam, 1 lammps .in, 1 .py
           |            |-Simulation 4  >>> files: 2 .meam, 1 lammps .in, 1 .py
           |            |-Simulation 5  >>> files: 2 .meam, 1 lammps .in, 1 .py
           |
           |-Ordered_compositions 
                   |-Fe0.5V0.75  >>> files: 2 .meam, 1 lammps .in, 1 .py
                       |    (Run .py code using play button in spyder to create 39 dir's)
                       |-Simulation_lattice_a0(39 lattices) 
                       |     :
                       |-Simulation_lattice_a39

#############################################################################################
#detail : : : 1000-ts and 250 dump; 2000 atomic configuration, total FeV atoms = 16 

#############################################################################################

1: Create dir       :    MD_Simulations
   Create subdir    :    MD_simulations_300K
   Create subsubdir :    Ordered_compositions 
                         >>> need 4 files: 2 .meam, 1 lammps .in, 1 .py
   Create subsubdir :    Random_compositions  with 5 subsubsubdir's 
                         (Simulation 1, 2,3, 4, 5)  
                         >>> need 4 files: 2 .meam, 1 lammps .in, 1 .py
2: Run .py code using play button in spyder to create 39 dir's to create 39 "Simulation_lattice_" directories.
3: Run lammps code using "atoms_positions.data" and command:
                         "mpiexec -np 2 lmp_mpi -in FeV_external_positions_input_file.in -e screen"
                   or, 
                         "multirun.sh"
