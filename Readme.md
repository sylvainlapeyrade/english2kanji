# English to Kanji Diffusion

## Overview
This project provides tools to convert English meanings into corresponding Kanji characters, generate their SVG representations, convert these to other image formats, and utilize these images within a machine learning framework for further processing and application.
<p align="center">
  <img src="https://huggingface.co/sylvainlapeyrade/kanji2english/resolve/main/generated_kanji_examples.jpg" width="350" title="Generated Kanji examples">
</p>

<i>These Kanji images were generated on only one epoch on Google Colab free version for proof of concepts purpose. A bigger training would result in much better images.</i>

## Features
- **Kanji Data Parsing:** Parses XML data sources for Kanji characters and their descriptions.
- **SVG Generation:** Generates SVG files for each Kanji character.
- **Image Conversion:** Converts SVG files to PNG and subsequently to JPG format.
- **Dataset Preparation:** Structures the processed images into a format suitable for machine learning applications.
- **Model Training:** Utilizes the Hugging Face Diffusers library to train a model on the Google Colab platform.
- **Image Generation:** Queries a trained model to generate images based on Kanji meanings.

## Resources

- [An XML dictionary file from the KANJIDIC project](http://www.edrdg.org/wiki/index.php/KANJIDIC_Project)
- `kanjidic2.xml` can be [downloaded here](http://www.edrdg.org/kanjidic/kanjidic2.xml.gz)
- [An XML file from the Kanji Vector Graphics project](https://github.com/KanjiVG/)
- [KanjiVG format explanation](https://kanjivg.tagaini.net/svg-format.html)
- `kanjivg.xml` can be [downloaded here](https://github.com/KanjiVG/kanjivg/releases/)

## Hugging Face Resources

The dataset generated and the model trained using this repository have been uploaded on Hugging Face:
- **Dataset:** [Kanji English Meaning Dataset on Hugging Face](https://huggingface.co/datasets/sylvainlapeyrade/kanji_english_meaning)
- **Model:** [Kanji to English Translation Model on Hugging Face](https://huggingface.co/sylvainlapeyrade/kanji2english)

## Usage
Follow the steps outlined in each cell to set up the environment, parse XML data, generate and convert images, and finally, train and utilize the model for Kanji image generation.

### Setting up the Environment
Make sure to install all required libraries using `pip install` for Python packages mentioned in the dependencies section.

### Running the Notebook
Execute each cell in sequence, from XML parsing to model querying. Ensure that appropriate files and directories are accessible as per the scripts.

### Model Query
To query the trained model, ensure you have a valid API key for the Hugging Face Inference API.

## Project Structure
1. **Kanjidic XML Parsing:** Extracts Kanji details from the `kanjidic2.xml` file.
2. **KanjiVG SVG Processing:** Generates SVG images from `kanjivg.xml`.
3. **SVG to Image Conversion:** Converts SVG files to PNG and JPG formats.
4. **Dataset Creation and Push to Hugging Face Hub:** Creates an image dataset and pushes it to the Hugging Face Hub.
5. **Model Training on Google Colab:** Sets up and runs training using a text-to-image model from the Diffusers library.
6. **Image Querying:** Demonstrates how to query the model to generate images based on text prompts.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
