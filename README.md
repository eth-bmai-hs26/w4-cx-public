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

After the exercise: its extension, an exercise of its own, with a third face, surprised, and a sentence as the
prompt, read by BERT, which picks the face to draw. Its folded cells reuse the first exercise's code, answers
included, so do that one first:
[`happy-sad-diffusion/happy_sad_diffusion_extension.ipynb`](happy-sad-diffusion/happy_sad_diffusion_extension.ipynb),
in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/happy-sad-diffusion/happy_sad_diffusion_extension.ipynb

You do five tasks, one line each: the denoiser's first layer, which now reads three more numbers, the vector of
`[CLS]` that stands for the whole sentence, the classifier, its loss, and the one-hot of the best score. Tasks 3
and 4 have the same kinds of lines as the sunrise season classifier above.

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

## A tiny stable diffusion (Friday 14:00, after the exercises above)

An exercise to do after the happy and sad faces, their extension and the text embeddings: its folded cells reuse
their code, answers included, as its first cell says:
[`tiny-stable-diffusion/tiny_stable_diffusion.ipynb`](tiny-stable-diffusion/tiny_stable_diffusion.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/tiny-stable-diffusion/tiny_stable_diffusion.ipynb

It puts the two notebooks together the way Stable Diffusion is built. The text embedder of the text embeddings
notebook is trained first and then frozen; the denoiser of the happy and sad extension then learns from the faces,
each with a caption, a sentence that describes its expression, read through the frozen text embedder as three
numbers. Then a word or a sentence of your own, "happy" or "a smiling child", becomes a face. You do four tasks,
five lines in all, the lines that make it Stable Diffusion: the cut of the prompt to between 0 and 1, the frozen
text embedder reading the captions once, a caption of its own expression for each face, and the text embedder's
step in front of the generation. Training takes well under a minute.

## Stable Diffusion: your own sampling loop (Friday 14:00)

An exercise in one Colab notebook, written by Sofi Mousia:
[`cx4_stable_diffusion.ipynb`](cx4_stable_diffusion.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/cx4_stable_diffusion.ipynb

The notebooks above build diffusion models small enough to train in under a minute. This one uses the real
one, Stable Diffusion 1.5 with its pretrained weights, through the `diffusers` library, and takes its pipeline
apart: the text encoder turns the prompt into embeddings, the UNet predicts the noise in a latent of
4 x 64 x 64 numbers, the scheduler takes one step, and the VAE decodes the last latent into a picture of
512 x 512 pixels. You write the sampling loop yourself, ten one-line gaps, each marked with a target sign and
most with a hint: the text embeddings, the starting noise, classifier-free guidance, the scheduler's step and
the decoding, then a sweep over the guidance scale and over the number of steps, a check of your loop against
the official pipeline, and a bonus that shows the picture appearing step by step. It needs a GPU runtime (the
notebook asks Colab for a T4) and downloads 4.3 GB of weights; after that a picture takes a few seconds.

## Face aging (Friday 11:00)

An exercise in one Colab notebook. You lead product at a photo app that wants a "show me at 70" button. A photo is
196,608 numbers, and faces sit on a thin manifold among them. You squeeze faces through the VAE of Stable Diffusion
and decode them back, blend two faces in pixels and in codes, and see that a random code decodes to stained glass.
You fill in four one-line gaps, each marked with a target sign and each with a folded hint: the encoder, the decoder,
the blend of two codes, and the edit that ages a face. The last part, optional, ages a real face with FADING; it needs
a GPU with more than 4 GB and about 4.6 GB of downloads. Parts 1 to 3 run on a free Colab CPU.
[`aging/face_aging.ipynb`](aging/face_aging.ipynb), in Colab at

    https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/aging/face_aging.ipynb

## Face aging with your own VAE (Friday 14:30)

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
