In this page, I managed to display some 3Dmol instance using a third-party JavaScript library [3Dmol.js](https://3dmol.org/doc/index.html ) , this is an excellent library for online molecular visualization on webpage. Here I will show some cases of  embedding proteins or molecules via setting 3Dmol parameters within HTML tags.
For practical embedding 3Dmol in your code, check the tutorial  [Using 3Dmol within your code](https://3dmol.org/doc/tutorial-code.html ).

- #### Display PDB proteins from remote database

Here is 2POR protein displayed. After configuration of the class as `viewer_3Dmol js` in `div`, and the parameter `data-pdb` as `2POR`, 3dmol.js will download the corresponding PDB file via an HTTP request from RCSB PDB API（In this case, [https://files.rcsb.org/download/2POR.pdb](https://files.rcsb.org/download/2POR.pdb) ), parse the file and render the final protein on the canvas.  More settings on display style please check  [embedding a 3Dmol Viewer](https://3dmol.org/doc/tutorial-embeddable.html ).

<div style="height: 700px; width: 700px; position: relative;" class='viewer_3Dmoljs' data-pdb='2POR' data-backgroundcolor='0xffffff' data-style='stick' data-ui='true' data-select=></div> 

- #### Display SDF molecules from remote database

Next example is to display a small molecule, the keywords are the same as the above one but replacing the parameter `data-pdb` as `data-cid`. The underlying pinciple is the same but with different database and API. Given the Compound ID, 3dmol.js download the SDF file via an HTTP request from PubChem CID API（[`https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/5280343/record/SDF?record_type=3d`](`https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/5280343/record/SDF?record_type=3d`) )


<div style="height: 400px; width: 650px; position: relative; left: 7%; " class='viewer_3Dmoljs' data-cid='5280343' data-backgroundcolor='0xffffff' data-style='stick' data-ui='true'></div> 

- #### Display PDB/SDF molecules from local database

Apart from displaying remote molecule files, local molecular data file can also be parsed and rendered automatically after loading local file. At present 3dmol support pdb, sdf, xyz, mol2 and cube formats. The following is an example. Parameter `data-href` and `data-type` need to be specified in `div`. 

<div style="height: 700px; width: 700px; position: relative;" class='viewer_3Dmoljs' data-href='../attachments/3hab.pdb' data-type='pdb' data-backgroundcolor='0xffffff' data-style='cartoon' data-ui='true'></div> 

- #### Using rich API  to create, load and style the 3Dmol instance


By using  3dmol API to display molecules,  there are various functions can be configured to interact with the viewer, such as zoom  in/out, adding residue labels,  bond style, adding surfaces... see the official documentation in details: [`https://3dmol.org/doc/AmbientOcclusionStyle.html`](`https://3dmol.org/doc/AmbientOcclusionStyle.html`) )
Here is an example showing the molecular docking result between qurecetin and protein 1R42.

<div id="container_02" style="height: 700px; width: 700px; position: relative;" class="mol-container"></div> 
