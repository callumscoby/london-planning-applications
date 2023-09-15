<h1 align="left">Predicting the Success of Planning Applications in London</h1>

<p>This work, produced for my Urban Data Science and Analytics Masters dissertation, scraped over 30,000 planning applications from London planning authorities. It uses the applications to understand how the quantity and success rate of applications vary spatially amongst London LSOA and planning authorities, and whether such variation is associated with geodemographic characteristics. It also identifies the spatial distribution of different application types and ascertains the factors that increase the odds of a successful outcome of a planning application. The insights are discussed in the context of urban challenges and so a light is shone on the role of the planning system in mitigating or compounding urban challenges.

Methods such as KNN spatial clustering, Geographically Weighted Regression, Logistic Binary Regression, SVM, and Random Forests are employed. </p>

## Abstract
<p> Despite the importance of planning permission for development of the built environment and
the mitigation of urban challenges, there is a lack of existing research examining the factors
that predict a successful planning application. Using planning applications submitted to 33
London planning authorities, this project assesses spatial variation within the number of
planning applications and the success rate of planning applications in London LSOA, and
identifies the factors that predict a successful application.
  
Systematic distributions of the number and success rate of planning applications between
LSOA are found, and statistically significant associations between the number and success
rate of planning applications in an LSOA and geodemographic characteristics are identified.
Modal types of planning application in LSOA are visualised, showing spatial variability.
Finally, applications for non-intrusive works such as noise assessments are found to be the
strongest predictors of planning application success. Results indicate that the planning system
has the capacity to compound urban challenges, suggesting the need for standardised
planning policy across London and wider reform and digitalisation to enable the planning
system to mitigate urban challenges.</p>


<p>
<img src="https://raw.githubusercontent.com/callumscoby/london-planning-applications/main/PA_Success_Rate.png" height="258px" />
<img src="https://raw.githubusercontent.com/callumscoby/london-planning-applications/main/PA_Modal_Type.png" height="258px" />



<p>(L-R): London, Beijing, Washington DC</p></p>

<p>Example workflows are available <a href="https://github.com/callumscoby/networkh3/blob/main/examples.ipynb">here</a></p>

## Install

Install the latest version from PyPI:

```sh
pip install networkh3
```

## Import

```sh
from networkh3 import NETWORKH3
```

## Usage

NETWORKH3 requires three parameters: the area of interest, the type of OSMNx network, and the resolution of the returned H3 hexagons:

```sh
from networkh3 import NETWORKH3

NETWORKH3.get_h3('Leeds, United Kingdom', 'drive', 9)
```

Optional style keywords can also be specified:

```sh
from networkh3 import NETWORKH3
import contextily as cx

NETWORKH3.get_h3('Leeds, United Kingdom', 'drive', 9, 
                network_kwargs={
                  'node_size': 1, 
                  'node_color': 'black',
                  'edge_color': 'red',
                  'edge_linewidth': 0.2}, 
                h3_kwargs={
                  'facecolor': 'white', 
                  'alpha': 0.6}, 
                basemap_kwargs={
                  'source': cx.providers.Stamen.TonerLite}
                  )
```
The network and clipped H3 hexagons can then be used in analysis:

```sh
# Calling the network
NETWORKH3.network

# Calling the clipped H3 hexagons
NETWORKH3.h3
```

## Issues and support

<p>Contribute or log issues <a href="https://github.com/callumscoby/networkh3/issues">here</a></p>

## Contact

* Website: <a href="https://callumscoby.com">callumscoby.com</a>
* Twitter: [@ScobyCallum](https://twitter.com/ScobyCallum)
* LinkedIn: [@callumscoby](https://linkedin.com/in/callumscoby)

## Acknowledgements
* <p>⌇ <a href="https://github.com/gboeing/osmnx">OSMnx</a></p>

* <p>🗺 <a href="https://github.com/uber/h3">H3</a></p>
