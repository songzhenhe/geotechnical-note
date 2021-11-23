# Shear Strength

## Soil Elasticity and Plasticity

For given applied stress components, the resulting strains can be written in matrix form:

$$\begin{align}
\left(
    \begin{array}{c}
    \epsilon_{xx}
    \\
    \epsilon_{yy}
    \\
    \epsilon_{zz}
    \\
    \epsilon_{xy}
    \\
    \epsilon_{yz}
    \\
    \epsilon_{xz}
    \end{array}
\right)
=
\frac{1}{E}
\left(
    \begin{array}{cccccc}
    1 & -\nu & -\nu & 0 & 0 & 0
    \\
    -\nu & 1 & -\nu & 0 & 0 & 0
    \\
    -\nu & -\nu & 1 & 0 & 0 & 0
    \\
    0 & 0 & 0 & 1 + \nu & 0 & 0
    \\
    0 & 0 & 0 & 0 & 1 + \nu & 0
    \\
    0 & 0 & 0 & 0 & 0 & 1 + \nu
    \end{array}
\right)
\left(
    \begin{array}{c}
    \Delta \sigma_{xx}'
    \\
    \Delta \sigma_{yy}'
    \\
    \Delta \sigma_{zz}'
    \\
    \Delta \sigma_{xy}'
    \\
    \Delta \sigma_{yz}'
    \\
    \Delta \sigma_{xz}'
    \end{array}
\right)
\end{align}$$

or in stiffness matrix format 

$$\begin{align}
\left(
    \begin{array}{c}
    \Delta \sigma_{xx}'
    \\
    \Delta \sigma_{yy}'
    \\
    \Delta \sigma_{zz}'
    \\
    \Delta \sigma_{xy}'
    \\
    \Delta \sigma_{yz}'
    \\
    \Delta \sigma_{xz}'
    \end{array}
\right)
=
\frac{E}{(1+\nu) (1-2\nu)}
\left(
    \begin{array}{cccccc}
    1 -\nu & \nu & \nu & 0 & 0 & 0
    \\
    \nu & 1 - \nu & \nu & 0 & 0 & 0
    \\
    \nu & \nu & 1 - \nu & 0 & 0 & 0
    \\
    0 & 0 & 0 & 1 - 2\nu & 0 & 0
    \\
    0 & 0 & 0 & 0 & 1 - 2\nu & 0
    \\
    0 & 0 & 0 & 0 & 0 & 1 - 2\nu
    \end{array}
\right)
\left(
    \begin{array}{c}
    \epsilon_{xx}
    \\
    \epsilon_{yy}
    \\
    \epsilon_{zz}
    \\
    \epsilon_{xy}
    \\
    \epsilon_{yz}
    \\
    \epsilon_{xz}
    \end{array}
\right)
\end{align}$$

Some literatures may have a factor 1/2 multiplying the shear modulii in the stiffness matrix resulting from the difference between shear strain and engineering shear strain, where $\gamma_{xy}=\epsilon_{xy}+\epsilon_{yx}=2\epsilon_{xy}$, etc.

For plane strain condtion, where $\epsilon_{xy}=\epsilon_{yy}=\epsilon_{yz}=0$

$$
\left[\begin{array}{c}
\epsilon_{xx} \\
\epsilon_{zz} \\
\epsilon_{xz}
\end{array}\right]=\frac{1}{E}\left[\begin{array}{ccc}
1 & -v & 0 \\
-v & 1 & 0 \\
0 & 0 & 1+v
\end{array}\right]\left[\begin{array}{c}
\Delta \sigma_{xx}' \\
\Delta \sigma_{zz}' \\
\Delta \sigma_{xz}'
\end{array}\right]
$$

or as a fuction of shear strain $\gamma_{xy}$

$$
\left[\begin{array}{c}
\epsilon_{xx} \\
\epsilon_{zz} \\
\gamma_{xz}
\end{array}\right]=\frac{1}{E}\left[\begin{array}{ccc}
1 & -v & 0 \\
-v & 1 & 0 \\
0 & 0 & 2(1+v)
\end{array}\right]\left[\begin{array}{c}
\Delta \sigma_{xx}' \\
\Delta \sigma_{zz}' \\
\Delta \sigma_{xz}'
\end{array}\right]
$$

## Elastic Settlement
The vertical displacement at the ground surface is the result of the vertical strain accumulating over the depth:

$$
    s(x,y) = u_z(x,y)|_{z=0} = \int \limits_{z=0}^{z=\infty} \epsilon_{zz} \text{d}z
$$

The vertical strain is a function of the vertical stress

$$
    \epsilon_{zz} = \frac{1}{E} \left[ \Delta \sigma'_{zz} - \nu (\Delta \sigma'_{xx} + \Delta \sigma'_{yy})  \right]
$$

In the oedometer test, soil strains in the z- direction under drained conditions, but the lateral strains $\epsilon_{yy}$ and $\epsilon_{xx}$ are zero. 

$$
    \epsilon_{yy} = \frac{1}{E} \left[ \Delta \sigma'_{yy} - \nu (\Delta \sigma'_{xx} + \Delta \sigma'_{zz})  \right] =0
$$

$$
    \epsilon_{xx} = \frac{1}{E} \left[ \Delta \sigma'_{xx} - \nu (\Delta \sigma'_{yy} + \Delta \sigma'_{zz})  \right] =0
$$

solving the above two equations and we could get 

$$
    \Delta \sigma'_{xx} = \Delta \sigma'_{yy} = \frac{E \nu }{(1+\nu) (1-2\nu)} \epsilon_{zz}
$$

$$
    \epsilon_{zz} = \frac{\Delta \sigma'_{zz}}{E_\text{s}} \quad \text{so} \quad  E_\text{s} = \frac{E(1-\nu)}{(1+\nu) (1-2\nu)}
$$


## Stresses beneath shallow foundations
Under typical working loads, the applied vertical bearing pressure applied by a shallow foundation to the underlying soil will be much less than the bearing capacity (so that the foundation is safe from collapse). Under these conditions, the soil will be in a state of elastic rather than plastic equilibrium. The constitutive behaviour of the soil is approximated as linear elastic (see Equation 5.4), though the stiffness (G) may vary with the confining stress (i.e. depth) or between soil layers. If the stresses beneath the founda-
tion are known for an applied bearing pressure (q), then the induced strains (and hence movements of the foundation) can be determined from the elastic material properties (G, ν). A range of solutions, suitable for determining the stresses below foundations, is given in this section.

### Point load
The stresses within a semi- infinite, homogeneous, isotropic mass, with a linear stress–strain relationship, due to a point load on the surface, were determined by Boussinesq in 1885. The vertical, radial, circumferential and shear stresses at a depth z and a horizontal distance r from the point of application of the
load were given. Referring to Figure 8.19(a), the stresses induced at X due to a point load Q on the surface are as follows:

$$\begin{align}
    r &= \sqrt{x^2 + y^2}
    \\
    R &= \sqrt{r^2 + z^2}
\end{align}$$

According to Boussinesq's analytical solution:

$$\begin{align}
    \Delta \sigma_{xx} &= \frac{3F_z}{2\pi R^2} \left[ \frac{x^2 z}{R^3} - \frac{1-2\nu}{3} \left( \frac{(x^2 - y^2) R}{r^2 (R + z)} + \frac{y^2 z}{R r^2}\right) \right]
    \\
    \Delta \sigma_{yy} &= \frac{3F_z}{2\pi R^2} \left[ \frac{y^2 z}{R^3} - \frac{1-2\nu}{3} \left( \frac{(y^2 - x^2) R}{r^2 (R + z)} + \frac{x^2 z}{R r^2}\right) \right]
    \\
    \Delta \sigma_{zz} &= \frac{3F_z}{2\pi R^2} \frac{z^3}{R^3}
\end{align}$$

the sum of the two horizontal normal stresses results in:  
$$
    \Delta \sigma_{xx} + \Delta \sigma_{yy} = \frac{3F_z}{2\pi R^2} \left[ \frac{r^2 z}{R^3} - \frac{1-2\nu}{3} \frac{z}{R} \right]
$$

$$\begin{align}
    \epsilon_{zz} &= \frac{1}{E} \left[ \Delta \sigma'_{zz} - \nu (\Delta \sigma'_{xx} + \Delta \sigma'_{yy})  \right]
    \\
    &= \frac{3F_z}{2\pi R^2 E} \left[ \frac{z^3}{R^3} - \nu \left( \frac{r^2 z}{R^3} - \frac{1-2\nu}{3} \frac{z}{R} \right) \right]
\end{align}$$

We now calculate the integral over $\epsilon_{zz}$ from $z=\infty$ to a depth $\bar{z}$, so:

$$
    u_z(r,\bar{z}) = \frac{3F_z}{2\pi E} \int \limits_{\bar{z}}^{\infty} \frac{1}{R^2} \left[ \frac{z^3}{R^3} - \nu \left( \frac{r^2 z}{R^3} - \frac{1-2\nu}{3} \frac{z}{R} \right) \right] \text{d}z
$$

To do this, we define in \texttt{sympy} the integrand \text{eps} (without constant prefactor) and the radius R:

$$
\frac{-v\left(\frac{r^{2} z}{\left(r^{2}+z^{2}\right)^{\frac{3}{2}}}-\frac{z\left(\frac{1}{3}-\frac{2 v}{3}\right)}{\sqrt{r^{2}+z^{2}}}\right)+\frac{z^{3}}{\left(r^{2}+z^{2}\right)^{\frac{3}{2}}}}{r^{2}+z^{2}}
$$

