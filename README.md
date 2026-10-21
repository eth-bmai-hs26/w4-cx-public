# w4-cx-public

Public material for the coding exercises of BMAI weekend 4 (23–24 October 2026).

## Manifold games (Friday 09:00)

Two browser apps, no installation needed. Open them from the course page, or locally with any static file server:

| app | folder | what you do |
|---|---|---|
| **Sunrise Machine** | [`manifold-games/sunrise-machine/`](manifold-games/sunrise-machine/) | Scroll through how a variational autoencoder learns 2000 synthetic sunrises: the image manifold in 3072-D pixel space, the encoder that unrolls it, the decoder, interpolation, sampling and β. Ends with a game: guess where the encoder puts a sunrise. |
| **Manifold Chart Explorer** | [`manifold-games/manifold-explorer/`](manifold-games/manifold-explorer/) | Explore 2-D manifolds (cylinder, Möbius band, sphere, torus, Klein bottle, RP²) through their charts and identifications, then see the same sunrises encoded by VAEs whose latent space has each of these shapes. |

```bash
cd manifold-games
python3 -m http.server 8000
# http://localhost:8000/sunrise-machine/  and  http://localhost:8000/manifold-explorer/
```

Both pages need an internet connection for their fonts and, for the Sunrise Machine, the JavaScript libraries (TensorFlow.js, GSAP, D3, KaTeX) loaded from a CDN.
