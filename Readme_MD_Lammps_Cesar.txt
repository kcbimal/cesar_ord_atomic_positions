1: running LAMMPS using supercell:
      a) Files: FeV_supercell_lammps_input_file.in, .meam, .conf, POSCAR
      b) "directories.py" >> modify: vol, temp, and, paths
      c) "dispersion_generator.py" >> modify: first part, paths, and, 
                                      range for 1st and 2nd species
      d) "bVK_alat_temp.py" >> modify: Example, paths, positions, & force
      e) Run "LAMMPS"
      f) use ideal file to create "...ideal_unit.txt" from excel.
      g) Run "BvK code" followed by "dispersion generator code"
      h) Run "heatmap creator" to create directory "heatmap"
      i) Run dispersion aggretator followed by aggregator analysis
         (these files must have temp-label in file name)
      

2: running LAMMPS using "atomic_positions":
     a) Run "lammps script ordered simulation 0.5.py" to create
                   "atoms_positions.data"
       NOTE: pick up correct ".data: file from respective T & volume dir.
     b) Run "sort_atom_position.py" and replace 2nd part of 
        "atomic_positions.data" by "sorted_atomic_positions.data"
     c) Files: FeV_external_positions_lammps_input_file.in, 
                   .meam, .conf, POSCAR, atoms_positions.data
     d)follow: b)...i) from part 1.
     