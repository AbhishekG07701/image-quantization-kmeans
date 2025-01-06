# Image Quantization Using K-Means Clustering

This repository provides Python functions to perform image quantization using the K-Means clustering algorithm. Image quantization reduces the number of unique colors in an image while attempting to maintain its overall appearance. This technique is particularly useful for compressing images and simplifying their color schemes.

## What is Image Quantization?

Image quantization is the process of reducing the number of unique colors in an image while trying to preserve its overall appearance. Instead of using a large variety of colors, quantization maps similar colors together into clusters, simplifying the image. This process can help reduce the image size and make it easier to process, while still keeping the visual characteristics intact.

## Functions

### `display_color_palette(cluster_centroids, num_clusters)`

This function displays the color palette for the quantized image clusters.

#### Parameters:
- `cluster_centroids` (numpy array): The RGB color codes representing the center of each cluster.
- `num_clusters` (int): The number of clusters (or colors) used for quantization.

#### Description:
- Reshapes the `cluster_centroids` and visualizes them as a palette of colors.
- Displays `num_clusters` colors as a horizontal strip in the plot.

---

### `quantize_image(image_path, num_clusters)`

This function performs image quantization using the K-Means clustering algorithm.

#### Parameters:
- `image_path` (str): The file path to the image you want to quantize.
- `num_clusters` (int): The number of clusters (i.e., the number of unique colors you want to reduce the image to).

#### Description:
- Loads the image from the specified path and reshapes it into a 2D array where each row represents a pixel with RGB values.
- Applies the K-Means algorithm to group similar pixels into `num_clusters` clusters.
- Displays the color palette representing the centroids of these clusters.
- Reconstructs the image by mapping each pixel to its closest cluster centroid.
- Displays the quantized image with reduced colors.

---

## Requirements

To run this code, you will need the following Python libraries:

- `numpy`
- `matplotlib`
- `sklearn`

You can install the required libraries using `pip`:

```bash
pip install numpy matplotlib scikit-learn
