# Speaker Notes — Version B (Foundation-Informed)

## Slide 1: Frame — Why This Matters
Don't start with equations. Start with the world. "Every time you check the weather, you're looking at the output of a PDE solver. Every time an engineer designs an aircraft, they solve PDEs. Every time a doctor models how a drug spreads through tissue, they use PDEs. Today we'll see what these equations are and why they work."

## Slide 2: Context — From ODE to PDE
Bridge from known to unknown. "You already know derivatives. A partial derivative is just a derivative where you hold some variables fixed. The jump from ODE to PDE is not about new math — it's about new geometry. We're no longer moving along a line. We're moving through space."

Show the ODE: dy/dt = f(t,y) — one variable, one direction.
Show the PDE: ∂u/∂t = α ∂²u/∂x² — two variables, change in space AND time.

The visual comparison should make the leap feel small, not terrifying.

## Slide 3: Key Idea — What a PDE Looks Like
Walk through each symbol. Don't rush. "The u is what we're trying to find — it might be temperature, pressure, displacement. The x's tell us WHERE. The partial derivatives tell us HOW it changes. The equation itself is the RULE that governs the change."

Label the three parts clearly: unknown function, independent variables, derivatives. The learner should be able to point to each part and say what it means.

## Slide 4: Three Equations, Three Kinds of Change
Don't derive. Just introduce. "These three equations are the atoms of PDE theory."

Point out the structural difference: heat equation has ONE time derivative (first order in time), wave equation has TWO (second order in time). This is not a minor detail — it's the reason one diffuses and the other propagates.

The color-coded tags (Parabolic, Hyperbolic, Elliptic) should help the learner start building associations.

## Slide 5: Heat Equation in Action
"Imagine you touch a cold metal rod with a hot finger. The heat spreads. That's the heat equation."

Walk through the time sequence: sharp spike → bell curve → flat. The learner should see the SMOOTHING happening.

Key insight: "The rate of smoothing is proportional to the CURVATURE. Where the profile is sharpest, diffusion is fastest."

This is the moment where the equation becomes physical. Don't rush it.

## Slide 6: Wave Equation in Action
"Now imagine plucking a guitar string. The pulse travels. It doesn't smooth out like heat — it PRESERVES its shape."

Walk through the time sequence: pulse at left → moving right → near boundary. The learner should see the PERSISTENCE.

Key insight: "The second time derivative means acceleration — the pulse has momentum. It bounces off boundaries."

The contrast with Slide 5 is the whole point. The learner should feel the difference between diffusion and propagation.

## Slide 7: Why Classification Is Not Just Naming
"This is not just naming."

Walk through each column:
- Elliptic: no time, instant equilibrium, steady state
- Parabolic: first time derivative, infinite speed diffusion, smoothing
- Hyperbolic: second time derivative, finite speed propagation, persistence

Then connect: "If I tell you the equation is hyperbolic, you already know: waves travel at finite speed, you need initial AND boundary conditions, and you should use methods that respect propagation."

The learner should understand that classification is a SHORTCUT to understanding the physics.

## Slide 8: Why a PDE Alone Is Not Enough
"The PDE is the rule. Boundary conditions are the specific situation."

Show three squares with different boundary conditions and different resulting temperature distributions. Same equation, different answers.

"The PDE says 'at every point, the value equals the average of its neighbors.' But that rule alone doesn't tell you the temperature分布. The boundary conditions — what's happening at the edges — determine the specific solution."

The learner should understand why boundary conditions are not optional.

## Slide 9: The Key Trick — Separation of Variables
"This is the key trick."

Walk through the process flow: Hard PDE → Assume product → Split into ODEs → Solve each → Combine.

"We assume the solution is a product of a function of x only and a function of t only. When we substitute into the PDE, the x-parts and t-parts separate — we get two ODEs instead of one PDE. ODEs we know how to solve."

Show the solution formula. Point out that each term is a product: spatial part × temporal part.

The learner should understand the STRATEGY, not just the formula.

## Slide 10: The Big Picture
"We've seen the full arc."

Connect: Classify → Understand → Solve

"The deepest insight is that the equation itself tells you the physics. Elliptic = equilibrium. Parabolic = diffusion. Hyperbolic = waves."

"This is what makes PDEs powerful — they're not just symbols, they're a window into how the world works."

End with the key insight panel. The learner should leave with this as their lasting impression.
