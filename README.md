# w4-cx-public

Public material for the coding exercises of BMAI weekend 4 (23–24 October 2026).

## What time is it? A CNN reads a sunrise (Friday 08:15)

An exercise and its worked example, two Colab notebooks, nothing to install. Both draw 3000 synthetic
sunrises with the generator of the Sunrise Machine (Friday 09:00), written by Frederick Puls, each from
two numbers, where the sun stands (the time of the year) and how high (the time of the day), and train a
small convolutional network on them.

The worked example, complete: the network tells the season of a sunrise, winter, spring or autumn, or
summer. Only the network and its training show their code:
[`sunrise-cnn/sunrise_season_classifier.ipynb`](sunrise-cnn/sunrise_season_classifier.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/sunrise-cnn/sunrise_season_classifier.ipynb

The exercise: the same network tells the time of the day. You do four tasks, each marked with a target
sign, seven lines in all: the two convolution blocks of the network, the head that gives one number, the
loss, and the three calls of one training step. Every task has a hint, folded until you click it, that
points at the matching lines of the worked example:
[`sunrise-cnn/sunrise_time_regression.ipynb`](sunrise-cnn/sunrise_time_regression.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/sunrise-cnn/sunrise_time_regression.ipynb

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

## Apples and oranges, a conditional autoencoder (Friday 10:00)

One Colab notebook, nothing to install:
[`apple-orange-autoencoder/apple_orange_autoencoder.ipynb`](apple-orange-autoencoder/apple_orange_autoencoder.ipynb),
or open it straight in Colab:

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/apple-orange-autoencoder/apple_orange_autoencoder.ipynb

Every picture is an apple (a red circle) or an orange (an orange circle) somewhere in the frame, and a label,
0 or 1, says which. The encoder squeezes a picture and its label into 16 numbers, and the decoder rebuilds the
picture from those numbers and the label, so flipping the label should turn an apple into an orange in the
same place. The notebook trains the same autoencoder twice, without and with a penalty on the length of the
code that stands in for the KL term of a variational autoencoder, counts how many of 5000 flips work with
each, and ends with a cell where you flip any fruit yourself. The two trainings together take about 20
seconds on a laptop, and longer on Colab.

## Happy and sad faces from noise (Friday 14:00)

A tiny diffusion model in one Colab notebook, nothing to install:
[`happy-sad-diffusion/happy_sad_diffusion.ipynb`](happy-sad-diffusion/happy_sad_diffusion.ipynb),
or open it straight in Colab:

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/happy-sad-diffusion/happy_sad_diffusion.ipynb

Every picture is a face of 9 x 9 pixels, happy or sad, and the prompt is a single bit: 0 asks for a happy
face, 1 for a sad one. The notebook blends faces into noise, trains a small network to estimate the picture
one step earlier, and then generates new faces from pure noise, step by step, as on the slides. You do five
tasks, each marked with a target sign, seven lines in all: the forward process, the network's missing layer,
the true previous picture that training compares with, the three calls of one training step, and one step
of the generation. Training takes well under a minute.

## Face aging with your own VAE

One Colab notebook, nothing to install:
[`face-aging-vae/face_aging_vae.ipynb`](face-aging-vae/face_aging_vae.ipynb),
or open it straight in Colab:

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/face-aging-vae/face_aging_vae.ipynb

Stable Diffusion never works on pixels: its VAE turns a 512 x 512 photo into a 64 x 64 x 4 latent and back.
You write the four layers that VAE is built from, eight gaps marked TODO: the residual block, the down- and
upsampling, and the self-attention. A check cell tests each layer. The notebook then builds the whole VAE from
your layers, loads the official Stable Diffusion v1.5 weights into it, and checks that it computes the same
numbers as the original, to within 1e-4. The last part ages a face with FADING, a face-aging model built on
Stable Diffusion, using your VAE to go between pixels and latents, on a demo face or a photo you upload. It
needs a GPU runtime (an A100) and downloads 4.6 GB of weights, and its slow step takes about 4 minutes.

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
