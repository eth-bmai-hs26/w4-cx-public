# Solutions of the weekend 4 notebooks

Every notebook of weekend 4 (23 and 24 October 2026) with its solution, in the order of the Friday
programme. Each address opens the notebook in Colab, straight from this repository; the same path under
https://github.com/eth-bmai-hs26/w4-cx-public/blob/main/ shows it on GitHub. The course site links the
exercises, not these solutions.

## Pufferfish autoencoder (Friday 08:15)

The solution, the complete notebook:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/pufferfish-autoencoder/pufferfish_autoencoder_solutions.ipynb

The exercise, three gaps:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/pufferfish-autoencoder/pufferfish_autoencoder.ipynb

The worked example beside it, complete, with no solution of its own:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/pufferfish-autoencoder/pytorch_example.ipynb

## Pufferfish variational autoencoder (Friday 08:15)

Complete, nothing to fill in: the same fish as the pufferfish exercise, trained as a variational
autoencoder, ending in the same sliders. A coding example for after the exercise, whose answers its code
gives away (a warning at its top says so); the course site links it as a demo, after the exercise.

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/pufferfish-vae/pufferfish_vae.ipynb

## Sunrise CNN (Friday 08:15)

The solution, the complete notebook:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/sunrise-cnn/sunrise_time_regression_solutions.ipynb

The exercise, the time of day of a sunrise, five tasks:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/sunrise-cnn/sunrise_time_regression.ipynb

The worked example, the season of a sunrise, complete, with no solution of its own:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/sunrise-cnn/sunrise_season_classifier.ipynb

## Two grasshoppers fit a line (Friday 08:15)

The solution, the complete notebook:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/grasshopper-gradient-descent/grasshopper_gradient_descent_solutions.ipynb

The exercise, three tasks:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/grasshopper-gradient-descent/grasshopper_gradient_descent.ipynb

## Apples and oranges, a conditional autoencoder (Friday 10:00)

Complete, with nothing to fill in: the notebook is its own solution.

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/apple-orange-autoencoder/apple_orange_autoencoder.ipynb

## Happy and sad faces from noise (Friday 14:00)

The solution, the complete notebook:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/happy-sad-diffusion/happy_sad_diffusion_solutions.ipynb

The exercise, five tasks:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/happy-sad-diffusion/happy_sad_diffusion.ipynb

## Three faces and BERT, the extension (Friday 14:00, after the happy and sad exercise)

A third face, a one-hot prompt, and a sentence read by BERT. The solution, the complete notebook, which also
holds the first exercise's answers:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/happy-sad-diffusion/happy_sad_diffusion_extension_solutions.ipynb

The exercise, five tasks:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/happy-sad-diffusion/happy_sad_diffusion_extension.ipynb

## Text embeddings from scratch (beside the happy and sad extension)

Every word of the extension's thirty sentences gets two numbers of its own, a sentence gets their average,
and a wide network turns it into three numbers; the words land in three groups and the sentences in three
clusters.

The solution, the complete notebook:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/text-embeddings/text_embeddings_solutions.ipynb

The exercise, three tasks:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/text-embeddings/text_embeddings.ipynb

## A tiny stable diffusion (Friday 14:00, after the three exercises above)

The text embedder of the text embeddings notebook and the denoiser of the happy and sad extension, put
together as Stable Diffusion is: a word or a sentence becomes a face. The solution, the complete notebook,
which also holds answers of the three exercises it builds on:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/tiny-stable-diffusion/tiny_stable_diffusion_solutions.ipynb

The exercise, four tasks:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/tiny-stable-diffusion/tiny_stable_diffusion.ipynb

## Face aging with your own VAE (Friday 14:30)

The solution, the complete notebook:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/face-aging-vae/face_aging_vae_solutions.ipynb

The exercise, eight gaps in the four layers of the VAE:

https://colab.research.google.com/github/eth-bmai-hs26/w4-cx-public/blob/main/face-aging-vae/face_aging_vae.ipynb

Not at the same path in the private repository: the masters are `aging/exercise_solution.ipynb` and
`aging/exercise.ipynb`, both built by `aging/scripts/build_exercise_notebooks.py`, and `pipeline.gif` is
`aging/figures/pipeline.gif`, drawn by `aging/scripts/draw_pipeline_doodle.py`.

## Keeping this list true

Every notebook here is a byte-for-byte copy of its master in the course's private repository, at the same
path. After a change to a master, copy it here again; when a notebook or a solution is added, add it to
this list.
