Bootstrap: docker
From: poldracklab/mriqc

%runscript

exec /usr/bin/run_mriqc

% post

# Make script executable

chmod +x /usr/bin/run_mriqc

# Make local folders

mkdir /share
mkdir /scratch
mkdir /local-scratch

# add environment variables

echo "
export PATH=/usr/local/miniconda/bin:$PATH
export PYTHONPATH=/usr/local/miniconda/lib/python3.5/site-packages
export PYTHONNOUSERSITE=1
export LANG=C.UTF-8
export LC_ALL=C.UTF-8
. /etc/fsl/fsl.sh
. /etc/afni/afni.sh

" >> /environment
