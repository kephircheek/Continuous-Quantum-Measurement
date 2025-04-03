# Continuous Quantum Measurement
 
## Getting started    

### Load sub-modules 

*This project depends on external code hosted in another repository.*

```shell
git submodule update --init 
```

### Set up Jupyter Notebook Kernel

Create special user kernel with

```shell
python3.10 -m venv <venv-name>
source <venv-name>/bin/activate
pip install ipykernel
python -m ipykernel install --name <kernel-name> --user
pip install $(cat **/requirements.txt) 
```

Or install dependencies in notebook cell with default kernel with

```text
from pathlib import Path
_requirements = " ".join(
    p.read_text().replace("\n", " ") 
    for p in Path.cwd().parent.glob("**/requirements.txt")
)
%pip install {_requirements}
```

*If the kernel is no longer needed, you can remove it later with*

```shell
jupyter kernelspec remove <kernel-name>
```

