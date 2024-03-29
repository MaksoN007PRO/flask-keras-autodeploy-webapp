
# Auto-deployment of a web application based on Keras and Flask.

Web application based on Keras and Flask for image classification.

## Application Features :fire:

- Enhanced, mobile-friendly UI;
- Support drag-and-drop for images;
- Developed in vanilla JS, HTML and CSS;
- Using TensorFlow 2.x and [tf.keras](https://www.tensorflow.org/guide/keras) by default;
- The application is adapted for deployment in docker.

## Run with Docker


#### Build locally

```shell
# 1. First, clone the repo
$ git clone https://gitlab.com/crazyminerecovery/flask-keras-autodeploy-webapp
$ cd flask-keras-autodeploy-webapp

# 2. Build Docker image
$ docker build -t keras_flask_webapp .

# 3. Run Docker Container
$ docker run -it --rm -p 5000:5000 keras_flask_webapp
```

Open http://localhost:5000 and wait till the webpage is loaded.

## Local Installation

It's easy to install and run application on your computer.

```shell
# 1. First, clone the repo
$ git clone https://gitlab.com/crazyminerecovery/flask-keras-autodeploy-webapp
$ cd flask-keras-autodeploy-webapp

# 2. Install Python packages
$ pip install -r requirements.txt

# 3. Run!
$ python app.py
```

Open http://localhost:5000 and have fun. :smiley:

![2_-Image-Classifier-Commit_-918390df-_-Яндекс-Браузер-2024-03-29-13-04-55-_online-video-cutter.com_](/uploads/193a9d2221f770be007490d361179d11/2_-Image-Classifier-Commit_-918390df-_-Яндекс-Браузер-2024-03-29-13-04-55-_online-video-cutter.com_.gif)

------------------

## Customization

It's also easy to customize and include your models in this app.

> **Note**
> Also consider [gradio](https://github.com/gradio-app/gradio) or [streamlit](https://github.com/streamlit/streamlit) to create complicated web apps for ML models.

<details>
 <summary>Details</summary>

### Use your own model

Place your trained `.h5` file saved by `model.save()` under models directory.

Check the [commented code](https://github.com/mtobeiyf/keras-flask-deploy-webapp/blob/master/app.py#L37) in app.py.

### Use other pre-trained model

See [Keras applications](https://keras.io/applications/) for more available models such as DenseNet, MobilNet, NASNet, etc.

Check [this section](https://github.com/mtobeiyf/keras-flask-deploy-webapp/blob/master/app.py#L26) in app.py.

### UI Modification

Modify files in `templates` and `static` directory.

`index.html` for the UI and `main.js` for all the behaviors.

</details>