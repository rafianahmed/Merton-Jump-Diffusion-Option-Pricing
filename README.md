# Merton Jump-Diffusion Option Pricing Simulator

This project implements the **Merton Jump-Diffusion model** for pricing European call options entirely in **JavaScript**, so it can run in any browser and be hosted on **GitHub Pages**.

## Model

Stock price dynamics:

dS_t = (μ - λk) S_t dt + σ S_t dW_t + (J-1) S_{t-} dN_t

- S_t: Stock price
- μ: Drift
- σ: Volatility
- W_t: Brownian motion
- N_t: Poisson jump process (jump intensity λ)
- J: Jump size (lognormal distribution)
- k: Mean jump size = E[J-1]

Option price computed via Monte Carlo simulation:
1. Simulate stock paths with jumps.
2. Compute payoff max(S_T - K, 0) for call option.
3. Discount average payoff at risk-free rate.

## Deployment

1. Push this repository to GitHub.
2. Go to **Settings → Pages** in the repository.
3. Set branch to `main` and folder to `/root` or `/docs`.
4. Your app will be live at `https://<username>.github.io/<repo>/`.
