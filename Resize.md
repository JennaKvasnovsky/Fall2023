# Resize Image

# This Python code snippet demonstrates how to use the matplotlib, numpy, and scikit-image libraries to download an image from a URL, resize it, and display it using matplotlib.pyplot.

      # This imports the matplotlib library under the alias plt, which is commonly used for creating plots and displaying images.
      import matplotlib.pyplot as plt 

      # This imports the numpy library under the alias np, which is used for numerical operations and array manipulations.
       import numpy as np 

       # This imports the imread function from the skimage.io module, which is part of the scikit-image library and is used to read images.
      from skimage.io import imread 

      # This imports the resize function from the skimage.transform module, which is used for resizing images.
      from skimage.transform import resize 

      # Defines the URL
      url = 'https://upload.wikimedia.org/wikipedia/commons/thumb/d/da/Claude_Monet%2C_Saint-Georges_majeur_au_cr%C3%A9puscule.jpg/800px-Claude_Monet%2C_Saint-Georges_majeur_au_cr%C3%A9puscule.jpg' 

      # This line reads the image from the specified URL using the imread function and stores it in the variable im.      
      im = imread(url)

      # This line displays the original image using plt.imshow. This is a quick way to visualize the image.
      plt.imshow(im); 

       # This line resizes the im image to have dimensions 512x512 pixels using the resize function. The result is stored back in the im variable.
      im = resize(im,(512,512))

      # This line displays the resized image. The second call to plt.imshow replaces the original image displayed with the resized one, allowing you to visualize the resized image.
      plt.imshow(im); 
