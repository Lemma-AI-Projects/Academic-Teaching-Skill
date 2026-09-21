# Source: Partial Differential Equations — A Brief Introduction

## What is a PDE?

A partial differential equation (PDE) is an equation that involves an unknown function of several independent variables and its partial derivatives with respect to those variables. PDEs are used to formulate problems involving functions of several variables, and they are either solved by hand or used to create a relevant computer model.

A PDE typically looks like:

```
F(x₁, x₂, ..., xₙ, u, ∂u/∂x₁, ∂u/∂x₂, ..., ∂²u/∂x₁∂x₂, ...) = 0
```

where u is the unknown function (the dependent variable), and x₁, x₂, ..., xₙ are the independent variables.

## Why PDEs Matter

PDEs are the mathematical language for describing how things change in space and time. Almost every physical phenomenon — heat flowing through a metal rod, waves traveling through water, the motion of air over an airplane wing, the spread of a disease through a population — is governed by PDEs.

Without PDEs, we cannot:
- Predict weather
- Design aircraft
- Model climate change
- Understand how heat distributes in a building
- Simulate how electrical signals propagate in the brain

## The Three Classical PDEs

### 1. The Heat Equation (Parabolic)

```
∂u/∂t = α ∇²u
```

or in one dimension:

```
∂u/∂t = α ∂²u/∂x²
```

This describes how temperature u(x,t) evolves over time in a conducting medium. The parameter α is the thermal diffusivity.

**Physical meaning:** Temperature spreads out from hot regions to cold regions. The rate of spreading is proportional to the "curvature" of the temperature profile.

**Key behavior:** Solutions smooth out over time. Sharp temperature differences gradually equalize.

### 2. The Wave Equation (Hyperbolic)

```
∂²u/∂t² = c² ∇²u
```

or in one dimension:

```
∂²u/∂t² = c² ∂²u/∂x²
```

This describes waves — sound waves, light waves, water waves, seismic waves. The parameter c is the wave speed.

**Physical meaning:** A disturbance at one point propagates to neighboring points at speed c. The second time derivative means the equation describes acceleration, not just velocity.

**Key behavior:** Solutions preserve their shape (in the simple case). Waves travel without dissipating.

### 3. The Laplace/Poisson Equation (Elliptic)

```
∇²u = 0       (Laplace)
∇²u = f(x,y)  (Poisson)
```

In two dimensions:

```
∂²u/∂x² + ∂²u/∂y² = 0
```

This describes steady-state phenomena: the equilibrium temperature distribution, the shape of a membrane at rest, the electric potential in a region without charge.

**Physical meaning:** At every point, the value of u equals the average of its neighbors. This is the "balance" condition.

**Key behavior:** Solutions are infinitely smooth (even if boundary conditions are rough). No time dependence — this is a snapshot of equilibrium.

## Classification

Every second-order linear PDE in two variables can be written as:

```
A ∂²u/∂x² + 2B ∂²u/∂x∂y + C ∂²u/∂y² + D ∂u/∂x + E ∂u/∂y + Fu = G
```

The classification depends on the discriminant B² - AC:

| Condition | Type | Example | Character |
|-----------|------|---------|-----------|
| B² - AC < 0 | Elliptic | Laplace equation | Smooth, equilibrium |
| B² - AC = 0 | Parabolic | Heat equation | Diffusion, smoothing |
| B² - AC > 0 | Hyperbolic | Wave equation | Propagation, waves |

This classification is not just naming — it determines:
- What boundary conditions are needed
- What solution methods work
- What the solutions look like physically
- Whether information propagates finitely or instantaneously

## Boundary and Initial Conditions

A PDE alone does not determine a unique solution. You need:

**For the heat/wave equation (time-dependent):**
- Initial conditions: u(x, 0) = f(x) — the initial state
- Boundary conditions: u(0, t) and u(L, t) — what happens at the edges

**Common boundary conditions:**
- Dirichlet: u is specified on the boundary (fixed temperature)
- Neumann: ∂u/∂n is specified on the boundary (insulated)
- Robin: a combination of u and ∂u/∂n

**For the Laplace equation (steady-state):**
- Boundary conditions only (no time evolution)

## Solution Methods

### Separation of Variables

Assume u(x,t) = X(x)·T(t). Substitute into the PDE. This converts the PDE into two ODEs, which are easier to solve.

**Example:** For the heat equation on [0, L]:

```
u(x,t) = Σ Bₙ sin(nπx/L) e^{-α(nπ/L)²t}
```

where Bₙ are Fourier coefficients determined by the initial condition.

### Fourier Analysis

Any reasonable function can be decomposed into sines and cosines. This is the foundation for solving PDEs on bounded domains.

The Fourier transform converts the PDE in the spatial domain to an ODE in the frequency domain, which is easier to solve.

### Numerical Methods

When analytical solutions are impossible (most real problems), we use:

- **Finite Difference Methods (FDM):** Replace derivatives with differences on a grid
- **Finite Element Methods (FEM):** Approximate the solution using piecewise polynomials on a mesh
- **Finite Volume Methods (FVM):** Conservation laws on control volumes

## The Big Picture

PDEs are:
1. A language for describing continuous change in space and time
2. Classified by their mathematical character (elliptic, parabolic, hyperbolic)
3. Solved by reducing to simpler problems (separation of variables, Fourier analysis)
4. In practice, solved numerically (FDM, FEM, FVM)
5. The foundation of computational science and engineering

The deep insight: **the type of PDE determines the type of physics.** Elliptic = equilibrium. Parabolic = diffusion. Hyperbolic = wave propagation. This classification is not arbitrary — it reflects fundamental differences in how information travels through space.
