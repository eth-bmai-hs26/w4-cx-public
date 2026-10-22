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

The exercise: the same network tells the time of the day. You do five tasks, each marked with a target
sign, eight lines in all: the two convolution blocks of the network, the head that gives one number, the
optimizer, the loss, and the three calls of one training step. Every task has a hint, folded until you
click it, that points at the matching lines of the worked example:
[`sunrise-cnn/sunrise_time_regression.ipynb`](sunrise-cnn/sunrise_time_regression.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/sunrise-cnn/sunrise_time_regression.ipynb

## Two grasshoppers fit a line (Friday 08:15)

An exercise in one Colab notebook, nothing to install. Two grasshoppers learn the line that predicts the
hour of three sunrise photos from where the sun stands, by gradient descent: each hops a little to measure
the slope of the average loss under its feet, and jumps against it, until the ground is flat under both.
You do three tasks, each marked with a target sign, ten short lines in all: the average loss of a line,
a function that measures the two slopes, the gradient, and the loop that calls it and makes the two
jumps. Every task has a hint, folded until you click it, and a cell below it that checks your lines and
prints PASS or NOT YET. The loop takes well under a second and prints the same numbers as the lecture's
click-through page, and the last cell says in large letters whether your grasshoppers found the line.
The exercise:
[`grasshopper-gradient-descent/grasshopper_gradient_descent.ipynb`](grasshopper-gradient-descent/grasshopper_gradient_descent.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/grasshopper-gradient-descent/grasshopper_gradient_descent.ipynb

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

After the exercise, and only then: the same fish trained as a variational autoencoder, a complete coding
example whose three sliders, in most runs, each do one thing: move the fish sideways, move it up and
down, or puff it up. Its code gives the exercise's answers away, as a warning at its top says:
[`pufferfish-vae/pufferfish_vae.ipynb`](pufferfish-vae/pufferfish_vae.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/pufferfish-vae/pufferfish_vae.ipynb

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

After the exercise, and only then: the extension, a complete coding example with a third face, surprised, and a
sentence as the prompt, read by BERT, which picks the face to draw. Its code gives the exercise's answers away:
[`happy-sad-diffusion/happy_sad_diffusion_extension.ipynb`](happy-sad-diffusion/happy_sad_diffusion_extension.ipynb),
in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/happy-sad-diffusion/happy_sad_diffusion_extension.ipynb

## Text embeddings from scratch (beside the happy and sad extension)

An exercise in one Colab notebook, nothing to install:
[`text-embeddings/text_embeddings.ipynb`](text-embeddings/text_embeddings.ipynb), or open it straight in Colab:

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/text-embeddings/text_embeddings.ipynb

The extension of the happy and sad notebook reads a sentence with BERT. This notebook builds a tiny text
embedder of its own from the same thirty made-up sentences: every word gets two numbers of its own, a sentence
gets the average of its words' numbers, and a wide network turns that average into three numbers, how happy,
sad and surprised the sentence is. Training finds all of these numbers in a few seconds. Then the notebook
draws where the words landed and every sentence as a point in 3D, and places your own sentences among them.
You do three tasks, each marked with a target sign, six lines in all: the two layers of the wide network, the
average of the words' numbers, and the three calls of one training step. Every task has a hint, folded until
you click it.

## A tiny stable diffusion (Friday 14:00, after the exercises)

After both exercises above, and only then: a complete coding example whose code gives their answers away, as a
warning at its top says:
[`tiny-stable-diffusion/tiny_stable_diffusion.ipynb`](tiny-stable-diffusion/tiny_stable_diffusion.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/tiny-stable-diffusion/tiny_stable_diffusion.ipynb

It puts the two notebooks together the way Stable Diffusion is built. The text embedder of the text embeddings
notebook is trained first and then frozen; the denoiser of the happy and sad extension then learns from the faces,
each with a caption, a sentence that describes its expression, read through the frozen text embedder as three
numbers. Then a word or a sentence of your own, "happy" or "a smiling child", becomes a face. Training takes well
under a minute.

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
