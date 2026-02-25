This code download SDF files of molecules in batch when provided SMILES files. 
The code background is: Frontend colleagues need molecular files with geometry information stored in their database. They used JavaScript library [3Dmol.js](https://3dmol.org/doc/index.html ) to visualize 3D molecular structrues on web application when provided sdf or pdf format files. 
Example SMILES txt file can be checked [here](https://github.com/JianyuZhao612/jianyuzhao612.github.io/blob/master/docs/scripts/attachments/SMILES.txt). All codes mentioned in `Scripts` section are placed in [this folder](https://github.com/JianyuZhao612/jianyuzhao612.github.io/tree/master/docs/scripts/codes).

```python
import requests,os
import numpy as np
from pathlib import Path
import zipfile

def download_sdf_files(smiles,path):
    # request data from pubchem
    # url_2d = f"https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/smiles/{smiles}/SDF"
​    url_3d = f"https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/smiles/{smiles}/SDF?record_type=3d"
​    response = requests.get(url_3d)
​    
    # If the requests succeed, obtain the content
​    if response.status_code == 200:
​        sdf_content = response.content
​        
        # save 3D SDF files
​        with open(path/f'3d_{smiles}.sdf', 'wb') as f:
​            f.write(sdf_content)
​        
​        print("SDF files downloaded successfully.")
​    else:
​        print(f"Failed to download SDF files. Status code: {response.status_code}")


if __name__=="__main__":

​    dirpath = r'C:\Users\YOUR\DESTINATION\DIRECTORY\FOLDER'
​    if os.getcwd() != dirpath:
​        os.chdir(dirpath)
​    output_head = Path.cwd()/'files'
​    if not os.path.exists(output_head):
​        os.mkdir(output_head)
​    
​    
    # ex1：given single smiles, download the 3D SDF file
​    smiles = "C1=CC=C(C=C1)C=O"
​    download_sdf_files(smiles,output_head)
​    
    # ex2：download 3D SDF file in SMILES txt file
​    mols = np.loadtxt(Path.cwd()/'SMILES.txt',dtype=str)
​    for mol in mols:
​        download_sdf_files(mol,output_head)

    # compress files into one file:files.zip
​    with zipfile.ZipFile(Path.cwd()/'files.zip', 'w', zipfile.ZIP_DEFLATED) as myzip:
​        print(os.listdir(output_head))
​        for file in os.listdir(output_head):
​            myzip.write(Path('./files')/file) # Relative path
```