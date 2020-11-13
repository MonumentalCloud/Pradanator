# Pradanator
This is an experiment to see if Neural Network can design a convincing garment.

41 images of the most recent Spring 2021 Ready-to-wear shows were used to train the Network.
I only wanted to use one collection of images since bringing in other collections, while increasing the data pool, would introduce higher variance in data.

Two big approaches were taken: GAN and VAE.

After hours of training, GAN and VAE both had its pros and cons.

![Sample Result](https://github.com/MonumentalCloud/Pradanator/blob/main/Sample%20Results/download-12.png)
![Sample Result](https://github.com/MonumentalCloud/Pradanator/blob/main/Sample%20Results/download-14.png)
![Sample Result](https://github.com/MonumentalCloud/Pradanator/blob/main/Sample%20Results/download-11.png)
![Sample Result](https://github.com/MonumentalCloud/Pradanator/blob/main/Sample%20Results/download-10.png)


Deep Convolutional GAN, while higher definition than the VAE approach, failed to reproduce design variance in the images.
The discriminator network, instead of training itself to recognize differnt types of clothing, have instead fit itself to the grand average of the entire collection.
THe result is a unrecognizable patches of colors on a humanoid figure, as seen below. No matter how random the seed input was, the image never changed. It seems that the generater overfitted to a overgeneralized discriminator network


On the other hand, VAE's were successful in reproducing variable garments when given the approapriate inputs. However, when the decoder was separated from encoder and was given a random seed input, it failed to create anything resembling the original images.

**THE PROJECT IS STILL IN PROGRESS**
