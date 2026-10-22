# w4-cx-public

Public material for the coding exercises of BMAI weekend 4 (23–24 October 2026).

## Pufferfish autoencoder (Friday 08:15)

An exercise in one Colab notebook, nothing to install:
[`pufferfish-autoencoder/pufferfish_autoencoder.ipynb`](pufferfish-autoencoder/pufferfish_autoencoder.ipynb),
or open it straight in Colab:

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/pufferfish-autoencoder/pufferfish_autoencoder.ipynb

It draws 5000 made-up pufferfish pictures, each from three numbers (where the fish sits, x and y, and how
puffed up it is, m), trains a plain autoencoder that squeezes every picture into three numbers of its own,
and ends with a cell where you pick a fish, change its three numbers with sliders, and watch the decoder
draw the new fish. You fill in three gaps, each marked with a target sign: one line of the decoder, the
optimizer, and the three calls of one training step. Training takes about a minute and a half on Colab.

Stuck on how to write a line? A short worked example trains a small network on made-up ice cream sales,
with the same three kinds of lines:
[`pufferfish-autoencoder/pytorch_example.ipynb`](pufferfish-autoencoder/pytorch_example.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/pufferfish-autoencoder/pytorch_example.ipynb

## Manifold games (Friday 09:00)

Two browser apps, no installation needed. Open them from the course page, or locally with any static file server:

| app | folder | what you do |
|---|---|---|
| **Sunrise Machine** | [`manifold-games/sunrise-machine/`](manifold-games/sunrise-machine/) | Scroll through how a variational autoencoder learns 2000 synthetic sunrises: the image manifold in 3072-D pixel space, the encoder that unrolls it, the decoder, interpolation, sampling and β. Ends with a game: guess where the encoder puts a sunrise. |
| **Manifold Chart Explorer** | [`manifold-games/manifold-explorer/`](manifold-games/manifold-explorer/) | Explore 2-D manifolds (cylinder, Möbius band, sphere, torus, Klein bottle, RP²) through their charts and identifications: drag a dot across a glued edge and watch where it comes back. On the cylinder, torus, Klein bottle and projective plane tabs, "Fold the chart" (key F) folds the chart step by step into the surface, until its glued edges meet. |

```bash
cd manifold-games
python3 -m http.server 8000
# http://localhost:8000/sunrise-machine/  and  http://localhost:8000/manifold-explorer/
```

Both pages need an internet connection for their fonts and, for the Sunrise Machine, the JavaScript libraries (TensorFlow.js, GSAP, D3, KaTeX) loaded from a CDN.
