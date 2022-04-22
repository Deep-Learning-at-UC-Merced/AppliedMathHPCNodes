# Applied Math HPC Nodes

UC Merced's Applied Mathematics (AM) hosts dedicated nodes on both MERCED and Pinnacles clusters, which can be utilized by AM faculty and graduate students (or those who have been granted permission). 

## Pinnacles Nodes
The AM department has a dedicated partition, `dept.appliedmath`, which hosts 6 nodes, with 2 being GPU nodes (one A100 GPU). The walltime limit on all nodes is 7 days. 

### Submitting Jobs to `dept.appliedmath` Generic Nodes
To submit your jobs to the normal AM nodes (without others being able to join the queue), your Slurm bash script must include:

````bash
#SBATCH -p dept.appliedmath
#SBATCH --constraint=6330
````

### Submitting Jobs to GPU Nodes on `dept.appliedmath`:
Similar to the generic AM nodes, your script must first specify the `dept.appliedmath` partition, followed by adding the constraint to include GPUs. 
Just as in submitting your GPU jobs to the other nodes, you must also specify which GPU(s) you are requsting. This can be done as the follwing:

````bash
#SBATCH -p dept.appliedmath
#SBATCH --constraint=a100
#SBATCH --gres=gpu:<ReplaceWithGPUNumber(s)>
````


## MERCED Nodes
Coming soon.
