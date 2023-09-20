### Swan Download
1. Swan Download
cd
mkdir SWAN
cd SWAN
wget https://swanmodel.sourceforge.io/download/zip/swan4145.tar.gz

2. Unzip and install
tar -xvzf swan4145.tar.gz
cd swan4145
make config
make mpi

SWAN is installed swan.exe is present. Type ls | grep swan.exe

3. Change permission
chmod 745 ./swanrun

4. Copy swan files
cp /mnt-storage1/TRAINING/data/swan_fgd/SamuderaHindia_coba2.swn .
cp /mnt-storage1/TRAINING/data/swan_fgd/batimetri_batnas.bot .
cp /mnt-storage1/TRAINING/data/swan_fgd/WindWorking_combined.wnd .

5. Copy job.mpi
cp /opt/ohpc/pub/examples/slurm/job.mpi .
gedit job.mpi

Change into :
====================
#!/bin/bash

#SBATCH -J swan_hindia_belanda               # Job name
#SBATCH -o swan_hindia.out         # Name of stdout output file (%j expands to jobId)
#SBATCH -N 1                  # Total number of nodes requested
#SBATCH -n 32                 # Total number of mpi tasks requested
#SBATCH -t 02:30:00           # Run time (hh:mm:ss) - 2.5 hours

# Launch MPI-based executable

mpirun ./swanrun -input SamuderaHindia_coba2.swn
=============
6. Run swan
sbatch job.mpi

7. Take a coffee break and wait for it to run.
