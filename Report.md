# Image Processing and Convolutional Filters Report

## Introduction

This report documents the process of loading and processing an image from a given URL, applying convolutional filters to it, and visualizing the results. The purpose is to demonstrate image processing techniques and their effects.

## Data Loading and Display

We started by downloading an image from the following URL:
![Doberman Image](https://cdn.britannica.com/77/234477-050-DF90E2ED/Doberman-pinscher-dog.jpg)

We used Python and the `requests` library to fetch the image and displayed it in the Jupyter Notebook using the `IPython.display` library.

```python
import requests
from IPython.display import Image, display

# URL of the image you want to load
image_url = "https://cdn.britannica.com/77/234477-050-DF90E2ED/Doberman-pinscher-dog.jpg"

# Download the image
response = requests.get(image_url)

# Check if the request was successful (status code 200)
if response.status_code == 200:
    # Display the image directly in the notebook
    display(Image(data=response.content))
else:
    print("Failed to download the image.")
