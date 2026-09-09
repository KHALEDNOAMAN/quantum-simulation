# Quantum Simulation - Physics Guide

## The Split-Step Fourier Method
This simulation solves the time-dependent Schrodinger equation:

i * hbar * dPsi/dt = H * Psi

Using the split-operator technique:
1. Apply half-step potential in position space
2. FFT to momentum space
3. Apply full kinetic step
4. IFFT back to position space
5. Apply remaining half-step potential

## Key Parameters
| Parameter | Symbol | Effect |
|-----------|--------|--------|
| Wave number | k0 | Initial momentum |
| Width | sigma | Packet spread |
| Potential height | V0 | Barrier strength |
| Grid points | N | Spatial resolution |
| Time step | dt | Temporal resolution |

## Quantum Phenomena You Can Observe
- **Tunneling**: Particle passes through potential barrier
- **Reflection**: Packet bounces off barrier
- **Dispersion**: Free packet spreads over time
- **Interference**: Split packet recombines

## Running the Simulation
```bash
python simulation.py --potential barrier --energy 0.5 --width 0.1
```

## 3D Visualization
The space-time plot shows probability density |Psi(x,t)|^2
as a 3D surface, revealing the full evolution of the wave packet.