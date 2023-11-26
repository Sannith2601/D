# GuideSync

> Bring the future to your eyes :eyeglasses:

This initiative aims to assist individuals with visual impairments by enabling them to read text, access information from the internet, recognize faces, and receive descriptive information about images through the generation of meaningful sentences.


##  Matriels
Raspberry Pi
Camera
Battery
Aurdino nano 3 
wireless bluetooth
Dsiplay for aurdino

##  Usage

command options :
 - -t : task
 - -m : mode (opencv_haar, dlib_hog, dlib_cnn, mtcnn, mobilenet_ssd)
 - -i : input object (image path)
 - -l : language (en / fr)
 
#### 1) Face detection

```
python gmg.py -t face_detection -m opencv_haar -i image.png -l en
```
#### 2) Face recognition
Recognise person
```
python gmg.py -t face_recognition -i image.png -l en
```
Add person face to dataset
```
python gmg.py -t add_face -i image.png -l fr
```
Initialise dataset with the existing images
```
python gmg.py -t face_init
```

#### 3) Wiki api
Get informations about anything
```
python gmg.py -t wiki -i obama -l fr
```

#### 4) News api

Get latest 10 articles from CNN
```
python gmg.py -t news_latest -l en
```

Get by number (between 1 and 10) article from the latest articles published by CNN

```
python gmg.py -t news_article -i 3 -l en
```

#### 5) Weather api

Get the weather description for a specified city
```
python gmg.py -t weather -country canada -city vancouver -l en
```

#### 6) Time api

Get current date
```
python gmg.py -t date -l en
```

Get current time
```
python gmg.py -t time -l en
```

#### 7) Ocr api

Read text from input image
```
python gmg.py -t ocr -i image_path -l en
```

