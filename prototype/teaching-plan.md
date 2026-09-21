# Teaching Plan

## Audience
Upper-undergraduate students who have taken calculus and basic ODEs. They know what derivatives are but have not seen PDEs before.

## Goal
After this presentation, the learner should be able to:
1. Explain what a PDE is and why it's different from an ODE
2. Name the three classical PDEs and describe the physical phenomenon each describes
3. Explain why PDE classification matters (not just as naming, but as physics)
4. Describe the basic idea behind solution methods (separation of variables, numerical approximation)

## Teaching Sequence

### Slide 1: Frame — Why This Matters
- **Purpose:** Establish relevance before any content
- **Teaching move:** Frame
- **Key idea:** PDEs are the mathematical language for describing how things change in space and time. Without them, we cannot predict weather, design aircraft, or model climate.
- **Visual:** Image of weather system / wave / heat pattern — something that screams "this changes in space AND time"
- **Speaker notes:** Don't start with equations. Start with the world. "Every time you check the weather, you're looking at the output of a PDE solver."

### Slide 2: Context — From ODE to PDE
- **Purpose:** Bridge from what learners know (ODEs) to what they don't (PDEs)
- **Teaching move:** Distinguish
- **Key idea:** ODEs describe change in one variable. PDEs describe change in multiple variables simultaneously.
- **Visual:** Side-by-side comparison: ODE (ball on a line) vs. PDE (temperature on a plate)
- **Speaker notes:** "You already know derivatives. A partial derivative is just a derivative where you hold some variables fixed. The jump from ODE to PDE is not about new math — it's about new geometry."

### Slide 3: Key Idea — What a PDE Looks Like
- **Purpose:** Show the general form and explain what each piece means
- **Teaching move:** Introduce
- **Key idea:** A PDE is an equation involving an unknown function of several variables and its partial derivatives.
- **Visual:** The general PDE form with labeled parts: unknown function, independent variables, derivatives
- **Speaker notes:** Walk through each symbol. Don't rush. "The u is what we're trying to find. The x's are the independent variables. The partial derivatives tell us how u changes."

### Slide 4: Key Idea — The Three Classical PDEs
- **Purpose:** Introduce the three types and their physical meanings
- **Teaching move:** Introduce
- **Key idea:** Three equations appear everywhere: Heat (parabolic), Wave (hyperbolic), Laplace (elliptic).
- **Visual:** Three-column layout: equation, name, physical meaning
- **Speaker notes:** Don't derive. Just introduce. "These three equations are the atoms of PDE theory. Everything else is built from them."

### Slide 5: Evidence — Heat Equation in Action
- **Purpose:** Show the heat equation as a concrete example
- **Teaching move:** Demonstrate
- **Key idea:** The heat equation describes how temperature spreads. Sharp gradients smooth out over time.
- **Visual:** Animation or sequence showing a temperature profile smoothing over time (initial spike → bell curve → flat)
- **Speaker notes:** "Imagine you touch a cold metal rod with a hot finger. The heat spreads. That's the heat equation. Notice how the sharp spike becomes smooth — that's diffusion."

### Slide 6: Evidence — Wave Equation in Action
- **Purpose:** Show the wave equation as a concrete example
- **Teaching move:** Demonstrate
- **Key idea:** The wave equation describes propagation. Disturbances travel at speed c without dissipating.
- **Visual:** Animation or sequence showing a pulse traveling along a string (initial bump → traveling bump → reflected bump)
- **Speaker notes:** "Now imagine plucking a guitar string. The pulse travels. It doesn't smooth out like heat — it PRESERVES its shape. That's the fundamental difference between parabolic and hyperbolic."

### Slide 7: Distinguish — Classification Matters
- **Purpose:** Explain WHY classification is not just bookkeeping
- **Teaching move:** Distinguish
- **Key idea:** The classification (B²-AC) determines: what BCs are needed, what solution methods work, what the solutions look like, whether information propagates finitely or infinitely.
- **Visual:** Decision tree or table: Classification → Properties → Solution methods
- **Speaker notes:** "This is not just naming. If I tell you the equation is hyperbolic, you already know: waves travel at finite speed, you need initial AND boundary conditions, and you should use methods that respect propagation."

### Slide 8: Explain — Why Boundary Conditions Matter
- **Purpose:** Explain why a PDE alone is not enough
- **Teaching move:** Explain
- **Key idea:** A PDE describes a FAMILY of solutions. Boundary conditions pick the specific solution for YOUR problem.
- **Visual:** Same PDE with different BCs → different solutions (e.g., Laplace equation on a square with different boundary temperatures)
- **Speaker notes:** "The PDE is the rule. The boundary conditions are the specific situation. Same rule, different situation, different answer. Without BCs, the PDE is incomplete."

### Slide 9: Demonstrate — How We Solve PDEs
- **Purpose:** Show the basic idea of separation of variables
- **Teaching move:** Demonstrate
- **Key idea:** Assume u(x,t) = X(x)·T(t). The PDE splits into two ODEs. Each is easy to solve. Combine the solutions.
- **Visual:** Step-by-step: PDE → assume product → two ODEs → solve each → combine
- **Speaker notes:** "This is the key trick. One hard PDE becomes two easy ODEs. You've already solved ODEs. This is why separation of variables is so powerful."

### Slide 10: Synthesize — The Big Picture
- **Purpose:** Connect everything into a coherent framework
- **Teaching move:** Synthesize
- **Key idea:** PDEs are the bridge between mathematical structure and physical behavior. Classification tells you the physics. Solution methods let you compute. Numerical methods let you solve real problems.
- **Visual:** Overview diagram connecting: Classification → Physics → Solution methods → Applications
- **Speaker notes:** "The deep insight is that the equation itself tells you the physics. Elliptic = equilibrium. Parabolic = diffusion. Hyperbolic = waves. And we have tools to solve all three."

## Notes on This Plan

This plan follows our teaching grammar:
- Frame → Context → Key Idea → Evidence → Distinguish → Explain → Demonstrate → Synthesize

It deliberately:
- Starts with relevance, not equations
- Bridges from ODEs (known) to PDEs (unknown)
- Shows concrete examples BEFORE classification
- Explains WHY classification matters, not just WHAT it is
- Ends with synthesis, not just coverage

It deliberately does NOT:
- Derive equations (too advanced for this audience)
- Cover numerical methods in detail (out of scope)
- Cover nonlinear PDEs (out of scope)
- Include exercises (this is a presentation, not a lesson)
