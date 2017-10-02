## Face generation
In this project, you'll use generative adversarial networks to generate new images of faces.

### Get the Data

You'll be using two datasets in this project:

- MNIST
- CelebA

Since the celebA dataset is complex and you're doing GANs in a project for the first time, we want you to test your neural network on MNIST before CelebA. Running the GANs on MNIST will allow you to see how well your model trains sooner.

If you're using FloydHub, set data_dir to "/input" and use the FloydHub data ID "R5KrjnANiKVhLWAkpXhNBe".

## Explore the Data

### MNIST

As you're aware, the MNIST dataset contains images of handwritten digits. You can view the first number of examples by changing show_n_images.

### CelebA

The CelebFaces Attributes Dataset (CelebA) dataset contains over 200,000 celebrity images with annotations. Since you're going to be generating faces, you won't need the annotations. You can view the first number of examples by changing show_n_images.

## Preprocess the Data

Since the project's main focus is on building the GANs, we'll preprocess the data for you. The values of the MNIST and CelebA dataset will be in the range of -0.5 to 0.5 of 28x28 dimensional images. The CelebA images will be cropped to remove parts of the image that don't include a face, then resized down to 28x28.

The MNIST images are black and white images with a single color channel while the CelebA images have 3 color channels (RGB color channel).

## Build the Neural Network

You'll build the components necessary to build a GANs by implementing the following functions below:
- model_inputs
- discriminator
- generator
- model_loss
- model_opt
- train

### Check the Version of TensorFlow and Access to GPU

This will check to make sure you have the correct version of TensorFlow and access to a GPU

### Input
Implement the model_inputs function to create TF Placeholders for the Neural Network. It should create the following placeholders:


- Real input images placeholder with rank 4 using image_width, image_height, and image_channels.
- Z input placeholder with rank 2 using z_dim.
- Learning rate placeholder with rank 0.


Return the placeholders in the following the tuple (tensor of real input images, tensor of z data)

