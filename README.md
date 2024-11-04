## CD Spectroscopy Heatmaps
##### Input Files
Local directory must contain CSV files where:
* Row names are partial sequences TTAXXX (e.g. TTAGGG → GGG)
* Column names are ligand concentrations (μM)
* Contents are relative structural stabilities
<br>
##### Generation
In `cd_spectra_heatmap.ipynb`, navigate to the following cell:
```py
FILENAME = 'CHANGE'
TITLE = 'LIGAND, CATION'
```
Change these values such that:
* `FILENAME` = Input CSV filename
* `TITLE` = Heatmap title
Finally, run the notebook. Generated image will be saved as the file `{FILENAME}.png`.
<br>
<br>
## Docking Score Jitterplots
##### Input Files
Local directory must contain CSV-formatted text files with name format
`dock_{CONF}_{STRUCT}_{sequence}_100_50poses.txt`
* `CONF`: G-quadruplex conformation (parallel, antiparallel, hybrid)
* `STRUCT`: Structure ID
* `Sequence`: Partial sequence TTAXXX (e.g. TTAGGG → GGG)

Binding affinities (kcal/mol) must be included under the heading `S` 
<br>
##### Generation
In `docking_jitterplots.ipynb`, navigate to the following cell:
```py
LIG = 'CHANGE'
CONF = 'CHANGE'
STRUCT = 'CHANGE'
```
Change these values such that:
* `LIG` = Ligand docked
* `CONF` = G-quadruplex conformation (parallel, antiparallel, hybrid)
* `STRUCT`: Structure ID

Finally, run the notebook. Generated image will be saved as the file `{LIG}_{STRUCT}_{CONF}.png`.
