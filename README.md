📘 README.md — Around the World AR Project (Unity + Vuforia)
1. Overview

This project is an Augmented Reality (AR) application developed in Unity 2021.3.6f1 using Vuforia Engine 10.9.
The application displays virtual "souvenirs" mapped onto physical AR cubes (Merge Cube and Class Cube).
Each souvenir represents a real-world attraction and displays:

3D models

Local time

Weather information

Ambient audio

Dynamic lighting when rotating the cube

This project was created for the Around the World AR Assignment.

2. Features
✔ Souvenir 1 — Merge Cube (Eiffel Tower, Paris)

3 models imported from the web

2 custom models created manually

Ambient sound

Real-time weather (°F)

Local time (12-hour AM/PM)

Attraction name

Extra side with relevant information

Lighting changes when the cube is flipped

✔ Souvenir 2 — Class Cube (Same attraction used for demonstration)

Weather in °C

Time in 24-hour format

Same behavior but adapted for the Class Cube

Works simultaneously with the Merge Cube

✔ General

Uses OpenWeather API

Uses WorldTimeAPI

Works with webcam (or smartphone when built for Android)

Scene supports both cubes visible at the same time

3. Requirements
Component	Version
Unity	2021.3.6f1
Vuforia Engine	10.9.x
Android Build Support	Optional
OpenWeather API Key	Required
Vuforia License Key	Required
4. Project Setup
1. Install Unity 2021.3.6f1

Download from:
https://unity.com/releases/editor/archive

Include modules:

Android Build Support

WebGL Support (optional)

2. Add Vuforia to the Project

In Unity:

Window → Vuforia Configuration → Add License


Paste your Vuforia App License Key.

3. Configure Webcam

If using DroidCam:

Start DroidCam on your phone

Select DroidCam as webcam inside Unity

5. API Configuration
Weather Script

Open:

Assets/Scripts/WeatherAPIScript.cs


Add your API key:

private string apiKey = "SUA_CHAVE_AQUI";

Time Script

Open:

Assets/Scripts/TimeAPIScript.cs


Set timezone:

private string timezone = "Europe/Paris";

6. Running the Project
Unity Editor

Connect webcam

Open the Scene

Press Play

Point Merge Cube or Class Cube at the camera

Android Build
File → Build Settings → Android → Switch Platform
Player Settings → XR → Enable Vuforia
Build & Run

7. Project Structure
/Assets
    /Models
    /Scripts
    /Textures
    /Sounds
    /Scenes
        EiffelScene.unity
        ClassCubeScene.unity
        CombinedScene.unity
