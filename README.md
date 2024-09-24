# ML-MAID : ML - Miniature Automatic Installer for Dependencies
- Install dependencies without having to issue a zillion `pip install` commands.
- Re-implement ML-Maid compliant workflows and repositories without a sweat.
- No need to use Conda and Docker unless you really have to.
- Requirement files don't solve the problem.
- Setup CUDA automatically.

## Why ML MAID ?
ML Maid aimed to be a complete and unique tool that aims to automatically install dependencies in Python with specific focus on ML environments. It aims to solve the problem of environment re-creation from old code without the hassle of manually building docker containers unless really required. The idea behind ML-Maid is to implicitly enforce checks to keep the environment setup as simple as possible, so that it is easy to replicate. It also aims to completely automate the environment replication process. It aims to keep the environment simple starting from the production phase of the software life-cycle to save developer time. 

## Is ML-Maid a Replacement for Docker / Conda / Python Venv : NO
ML Maid aims to automate the use of tools like Docker / Conda / Python venv **without adding any additional complexity** so that the developer can focus on writing code.

## Installation
```bash
pip install ml-maid
```

## Usage
In your main Python script add the following to automatically install / check the dependencies before any other code is run:
```python
from mlmaid import install
install(script_path=__file__, python_version='3.10.12', sys_reqs=['cuda==11.8'])
```
(Change Python version and cuda version according to your requirements)

