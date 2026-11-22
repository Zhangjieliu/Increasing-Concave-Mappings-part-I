# Increasing-Concave-Mappings-part-I
# ICM-Based Newton Method for DC Microgrid Power Flow

This repository provides MATLAB codes for the numerical validation of the Increasing-Concave Mapping (ICM)-based Newton method for DC microgrid power flow analysis.

The simulations investigate the existence of feasible power flow equilibria, the convergence properties of different Newton methods, and the relationship between the spectral radius of the ICM mapping Jacobian and high-voltage equilibrium existence.

## Repository Contents

- **A_part.m**: Three-node DC microgrid case study. Calculates positive equilibrium points, identifies the critical CPL loading level, and evaluates the spectral radius along the high- and low-voltage equilibrium branches.

- **B_three_Newton.m**: 123-node DC microgrid case study, consisting of 10 voltage sources, 10 MPPT sources, and 103 constant power loads (CPLs). Compares the Fractional Newton, Quadratic Newton, and ICM-based Newton methods, and investigates the spectral radius under increasing CPL loading.

## Requirements

- MATLAB
- Optimization Toolbox (required for `fsolve` in `B_three_Newton.m`).

## How to Run

Run either script directly in MATLAB:

```matlab
run('A_part.m')
run('B_three_Newton.m')
```

## Generated Outputs

**A_part.m**
- Equilibrium curves under different CPL loading levels, illustrating the merging of two equilibria at the critical load and the loss of feasible equilibria beyond it.
- Spectral radius curves of the high- and low-voltage equilibrium branches, showing their behavior near the critical point.

**B_three_Newton.m**
- Convergence trajectories of the three Newton methods across all 113 unknown-voltage nodes.
- Spectral radius of the ICM mapping Jacobian along the high-voltage equilibrium branch, identifying the critical loading factor at which the spectral radius reaches one.

All figures are generated and displayed automatically upon execution.

