# Pixel-CLIP Image Search

A Python-based image processing and retrieval system that converts a normal input image into a pixel-style image and uses the CLIP model to retrieve visually and semantically matching pixel images from a dataset based on a text query.

## Project Overview

This project combines **image pixelation** and **CLIP-based image retrieval**.

The system takes a normal image as input and creates a pixel-style version of the image. The user then provides a text query, such as `"aeroplane"`, `"dog"`, or `"car"`. The CLIP model converts the text query and dataset images into embeddings and calculates their similarity to identify the most relevant pixel images.

## Project Workflow

```text
User uploads a normal image
          ↓
Image is converted into pixel-style image
          ↓
User enters a text query
          ↓
CLIP converts the text query into an embedding
          ↓
CLIP compares the query with dataset image embeddings
          ↓
Top matching pixel images are retrieved
          ↓
Results are displayed
```

## Input Requirements

The user needs to provide:

### 1. Input Image

The user must upload a normal image in a supported image format such as:

* PNG
* JPG
* JPEG

Example:

```text
Input Image → Aeroplane.jpg
```

The system processes this image and creates a pixel-style version.

### 2. Text Query

The user must enter a text description for image retrieval.

Example:

```text
Enter your image search query: aeroplane
```

Other examples:

```text
dog
car
leaf
```

## Dataset

This project uses a pixel-image dataset stored in the **`input1`** dataset folder.

The dataset contains pixel-style images that are used for CLIP-based image retrieval.

The dataset should be available to the project before running the retrieval process.

### Dataset Setup

The dataset is provided as a ZIP file:

```text
input1.zip
```

extract it into the project directory so that the project can access the `input1` folder.

Example structure:

```text
project/
├── main.py
├── requirements.txt
├── README.md
├── .gitignore
└── input1/
    ├── image1.png
    ├── image2.png
    ├── image3.png
    └── ...
```

> **Note:** The `input1` dataset should only
