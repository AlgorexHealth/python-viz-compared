# python-viz-compared
Example Notebooks that compare various python visualization libraries. Each notebook recreates the same visualization in as many python libraries as we can find. 

The following comparasions are available: 

* Heatmaps in 10 Libraries: *Heatmaps.ipynb*


##Installation Discussion

These notebooks rely on a myriad of different libraries many of which may conflict. It is absolutely essential that you use a virtual environment AND be careful about modifying certain Jupyter configuration environments that exist outside the virtual environment. 

*Clone the repo*:

```
git clone https://github.com/AlgorexHealth/python-viz-compared.git
cd python-viz-compared
```

*Initialize a new virtual environment:*

```
python3 -m venv venv
source venv/bin/activate
```
*Install the requirements.txt file:*

```
pip install -r requirements.txt
```

*Install Jupyter Notebook Extensions to support certain Plots:*
Certain libraries use the Jupyter notebook extensions framework and thus require an extra step to register extensions with jupyter. 
The sys-prefix ensures that only links to the files are used so that your core jupyter installation is not corrupted. 

```
jupyter nbextension enable --py --sys-prefix bqplot 
jupyter nbextension install --sys-prefix --py vega
```

I've found that these occasions can occasionally conflict. If that is occurring after your run these notebooks a few times, try clearing the widget state from the notebook menu (widgest > Clear Widget State).

*Run Notebook Server and Open in Browser:*

```
jupyter notebook 
```






