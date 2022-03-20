_Please stick to the headings and their order. Don't modify the words in bold. Your input is required at each occurrence of "e.g." and "..."._<br>
_You may use https://tex-image-link-generator.herokuapp.com/ to render math formulas in Markdown, see the examples below._

## Physics

### PDEs

Black oil equations with CO2 represented by gas phase/component and water represented by oil phase. CO2 can dissolve in water. 


### Constitutive relations

#### Fluid-matrix interaction

* **Capillary pressure:** 

![p_c(S_{l}) = p_\text{entry}S_{le}^{-1/\lambda}](https://render.githubusercontent.com/render/math?math=%5Cdisplaystyle+p_c%28S_%7Bl%7D%29+%3D+p_%5Ctext%7Bentry%7DS_%7Ble%7D%5E%7B-1%2F%5Clambda%7D%0A)
  Pentry=[1471., 294, 98, 30, 30, 30] for ESF, C, D, E, F, G sands.
  Lambda=1

* **Relative permeability:** 

![\begin{align*}
k_{r\alpha} =k_{r\alpha}^{max}S_{e\alpha}^{n_\alpha}
\end{align*}
](https://render.githubusercontent.com/render/math?math=%5Ccolor%7Bblack%7D%5Cdisplaystyle+%5Cbegin%7Balign%2A%7D%0Ak_%7Br%5Calpha%7D+%3Dk_%7Br%5Calpha%7D%5E%7Bmax%7DS_%7Be%5Calpha%7D%5E%7Bn_%5Calpha%7D%0A%5Cend%7Balign%2A%7D%0A)

![\begin{align*}
S_{e\alpha}=max\left(0, \frac{S_\alpha-S_{r\alpha}} {1-S_{rCO_2}-S_{rWater}}\right)
\end{align*}
](https://render.githubusercontent.com/render/math?math=%5Ccolor%7Bblack%7D%5Cdisplaystyle+%5Cbegin%7Balign%2A%7D%0AS_%7Be%5Calpha%7D%3Dmax%5Cleft%280%2C+%5Cfrac%7BS_%5Calpha-S_%7Br%5Calpha%7D%7D+%7B1-S_%7BrCO_2%7D-S_%7BrWater%7D%7D%5Cright%29%0A%5Cend%7Balign%2A%7D%0A)

*** Parameters ***
S_rW=[0.32, 0.14, 0.12, 0.12, 0.12, 0.10];
k_rC^max= [0.09, 0.05, 0.02, 0.1, 0.11, 0.16];
s_rC= [0.14, 0.1, 0.08, 0.06, 0.13, 0.06];
k_rW^max= [0.71,0.93,      0.95,     0.93,    0.72,      0.75, 1];
    

#### Phase composition: Applied equations of state

* **CO2 in liquid phase:** ...

* **Water in gas phase:** ...

#### Density

* **Liquid phase:** ...

* **Gas phase:** ...

#### Solubility limit

_Please provide the assumed solubility limit of CO2 in liquid phase at the tank bottom in kg/m<sup>3</sup>._

### Temperature

_Please provide the assumed temperature inside the computational domain in °C._

### Domain volume

_Please provide the assumed total volume of the computational domain in m<sup>3</sup>._

### Spatial parameters

_Please provide the relevant facies parameters as a csv file._<br>
_E.g._ The parameters ![p_\text{entry}, \lambda, S_{lr}, S_{gr}](https://render.githubusercontent.com/render/math?math=%5Cdisplaystyle+p_%5Ctext%7Bentry%7D%2C+%5Clambda%2C+S_%7Blr%7D%2C+S_%7Bgr%7D%0A) for the different facies are given in [spatial_parameters.csv](spatial_parameters.csv).<br>
_Obviously, the number and type of parameters for your model might differ from the ones in the provided template._

## Numerics

### Coupling of flow and transport, temporal and spatial discretization

_E.g._ Fully coupled, fully implicit, cell-centered FV with TPFA.

### Linearization and Solvers

_E.g._ Newton with line search, AMG-preconditioned BiCGSTAB for the linear systems.

### Primary Variables

_E.g._ Dependent on local phase composition:
* Both phases present:
  ![p_l, S_g](https://render.githubusercontent.com/render/math?math=%5Ctextstyle+p_l%2C+S_g%0A)...

### Computational Grid

_Please provide the number and shape of grid elements._

### Performance

| Indicator                            |  Average |      Min |      Max |
|:-------------------------------------|---------:|---------:|---------:|
| time step size [s]                   | 1.23e+56 | 1.23e+56 | 1.23e+56 |
| # nonlinear iterations per time step |      123 |      123 |      123 |
| # linear iterations per solve        |      123 |      123 |      123 |
