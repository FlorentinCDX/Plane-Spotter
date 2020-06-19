# Plane-Spotter

As part of the MSc at the ENSAI, I had to carry out a mission for the company Vinci Airport. 
Using online sources such as planespotters.com, the goal is to build a model able to classify airplanes according their manufacturer and their type (e.g. A320, B777, etc.)

## The mission

The objective of the mission was to detect and classify the aircraft present in the airport based on the video stream from the cameras. 
My job was to scrappe a set of images of labelled aircraft (brand, model, airline) in order to train a CNN model.Once the model was trained, I deployed it as an REST API.
In order to facilitate the use of the model and to realize a POC, I have deployed the API in a Docker container.

For more information you can consult the document report.pdf.

## Tech/framework used

* Model : TensorFlow, Keras
* Web Scrapping : rvest
* REST API : Plumber
* Docker

## Usage

To build our image, open a terminal in the project folder and run :

```bash
docker build -t r-tensorflow-api-plane-spotter
```

And in order to run the container :

```bash
docker run --rm -it -p 80:80 r-tensorflow-api-plane-spotter
```
Great, now we can see the result of the output by going to http://127.0.0.1:6974/names in your browser.
