    1  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    2  ln -s /opt/conda/pkgs/*/bin/* /bin
    3  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
    4  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
    5  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
    6  /opt/conda/bin/pip install bash_kernel
    7  /opt/conda/bin/pip install ipykernel
    8  /opt/conda/bin/python3 -m bash_kernel.install
    9  /opt/conda/bin/conda install -y ipykernel
   10  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   11  mkdir /scratch/reproducibility-tutorial
   12  mkdir /scratch/reproducibility-tutorial
   13  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   14  /opt/conda/bin/conda search -c bioconda snakemake
   15  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   16  ln -s /opt/conda/bin/* /bin
   17  ln -s /opt/conda/lib/* /usr/lib
   18  snakemake --version
   19  sudo apt-get update
   20  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   21  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   22  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   23  sudo apt-get update
   24  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   25  docker run hello-world
   26  cd /scratch/reproducibility-tutorial/
   27  history >>README.md
