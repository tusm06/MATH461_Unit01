# MATH461_Unit01

<img src="data/image.png" height="500" width="700">

## Problem description

_Discribe, in words, the situation you would lile to model._

**Statement**:
We want to figure out what happend when we introduce a new specie, like suckermouth fish, to an existing simplified food chain with two species, and letting the suckermouth fish to break the steadystate of the system. Then, we want to find the new steady-state of the three species. The Food chain contain a prey and a predator, and the invasive specie only consume the same food type of prey.

## Question formulation

_What question(s) would you like to answer about your setup above?_

- What will happend if a invasive specie is introduced in a exsiting food chain?
- How the steady state will change over time?
- What is the population change for each specie?
- Whether the invasive species will blend in the food chain or eliminate the food chain?
- Is it good or bad for the invasive species to eliminate or blend in the food chain?

## Mathematical model

_Identify variables, parameters, equations. List your assumptions._

### Variables and Parameters

|    Symbol     | Description                                                          |         Type         |                Unit                | Dimensions |
| :-----------: | -------------------------------------------------------------------- | :------------------: | :--------------------------------: | :---: |
|      $x$      | The population of species X (prey)                                   |  Dependent Variable  |                prey                | N  |
|      $y$      | The population of species Y (predator)                               |  Dependent Variable  |                pred                | N |
|      $z$      | The population of species Z (invasive species)                       |  Dependent Variable  |                inv                 | N |
|      $t$      | Time                                                                 | independent variable |                year                | T |
|     $x_0$     | The initial population of species X (prey)                           |      Parameter       |                prey                | N |
|     $y_0$     | The initial population of species Y (predator)                       |      Parameter       |                pred                | N |
|     $z_0$     | The initial population of invasive species Z (invasive species)      |      Parameter       |                inv                 | N |
|   $\alpha$    | The growth rate of prey (X) in the absence of a predator (Y)         |      Parameter       |         year<sup>-1</sup>          | T<sup>-1</sup> |
|    $\beta$    | The death rate of prey (X) due to the predation                      |      Parameter       | pred<sup>-1</sup>year<sup>-1</sup> | N<sup>-1</sup> T<sup>-1</sup>  |
| $\varepsilon$ | The death rate of prey (X) due to food sharing with invasive species |      Parameter       | inv<sup>-1</sup>year<sup>-1</sup>  | N<sup>-1</sup> T<sup>-1</sup> |
|   $\gamma$    | The natural death rate of predator (Y)                               |      Parameter       |         year<sup>-1</sup>          | T<sup>-1</sup> |
|   $\delta$    | The growth rate of the predator (Y) due to predation on the prey     |      Parameter       | prey<sup>-1</sup>year<sup>-1</sup> | N<sup>-1</sup> T<sup>-1</sup> |
|     $\xi$     | The growth rate of invasive species (Z)                              |      Parameter       |         year<sup>-1</sup>          | T<sup>-1</sup> |
|   $\sigma$    | The death rate of invasive species (Z) due to food sharing with prey |      Parameter       | prey<sup>-1</sup>year<sup>-1</sup> | N<sup>-1</sup> T<sup>-1</sup> |

### Equations

**Governing Equation**:

$$
\begin{align}
\frac{dx}{dt} &= \alpha x - \beta xy - \varepsilon xz\\
\frac{dy}{dt} &= -\gamma y + \delta xy\\
\frac{dz}{dt} &= \xi z - \sigma xz
\end{align}
$$

$$
x(0) = x_0, \quad y(0) = y_0, \quad z(0) = z_0
$$

### Assumptions
- The food chain only contains a single preditor, prey, and invasive specie. 
- There are 3 species in total within the food chain.
- The suckermouth fish only consume seawead, and do not hunt the prey or be hunted by the preditor.
- The prey and the invasive species share the common food.
- The death of the preditor can only be due to natural death.
- The death of the prey can only be due to the predation and the lack of food.
- The death of the invasive species can only due to the lack of food.
- The food for the prey and invasive species is not unlimited.
- The birth and death rate of each species is constant.
- All species the the food chain is all grown.
- Before introducing the invasive species, the food chain of prey and preditor is at an equilibrium state.

### Constraint 
- $x, y, z, t \ge 0$

## How will you answer your questions?

_Explain your approach to studying your model, identify a mathematical quantity you will evaluate to answer your question._


- Use python code to visualize the change in population of the 3 species, and find it steady-state.
- Use system of first-order differential equations to model the process for a invasive species take a part in the food chain.
- Use non-dimensionalization to make all variables and parameters we use is in the same scale.
- The final state of our population for 3 species respectively.
