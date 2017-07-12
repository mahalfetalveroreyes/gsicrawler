![GSICrawler Logo](./front-end/app/images/logo-gsi-crawler.png)

This website is useful to the analysis of comments from external aplications like Yelp, Amazon, Twitter, Youtube, Facebook, TripAdvisor an Foursquare. The user will choose
the type of analysis he wants to carry out (Emotions, Sentiments or Fake Analysis)
and he will also supply, for instance, a direct URL to a Yelp’s Business, the
id of a Facebook’s Fan Page or a YouTube’s Video. GSI Crawler will download the
comments belonging to this element and, later, the pertinent analysis will be run
using the <a href="https://github.com/gsi-upm/senpy">Senpy</a> tool. Once the analysis is finished, a summary of the result will be
shown and the possibility of review each comment one by one will be also offered.

*Note: Facebook and Tripadvisor analysis are not currently available.*

#Requirements
- <a href="https://docs.docker.com/engine/installation/linux/ubuntulinux/">Docker</a>

#Installation
First of all, clone the git project locally and access to gsicrawler directory.
```
git clone https://github.com/gsi-upm/gsicrawler.git

cd gsicrawler
```
Launch docker
```
sudo docker start
```
#Run
Create the project docker image from Dockerfile
```
sudo docker build -t "gsicrawler:dockerfile" .

```

Run your docker image locally in port 8888 and run the *start.py* script to initialize the gsicrawler server
```
sudo docker run -p 8888:8888 -t -i gsicrawler:dockerfile python start.py

```

Access from your browser and execute your analysis
```
http://localhost:8888
```
#User Guide
In this section we will explain the diferent sentiment analysis offered my this framework. We will use Yelp as example platform to analyse in depth. The website offers four different kind of analysis Emotions, Sentiment Fake or all of them. Select the Yelp platform by clicking on the eye button and choose one of the different analysis. Introduce the URL which contains the site you want to process or pick the example one. In this case we will select the Emotion analysis using the example URL.

![img1](./front-end/app/images/readme_img1.png)

A card will be introduced to the main dashboard with the analysis selected. In a few seconds the aplication will show the result. The framework allows to inspect the emotion result of each review of the post analyzed.

![img2](./front-end/app/images/readme_img2.png)



#License
   Copyright 2016 José Emilio Carmona.

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.

#References
<a href="http://www.gsi.dit.upm.es/index.php/es/investigacion/publicaciones?view=publication&task=show&id=394">[1]</a>*"Development of a Social Media Crawler for Sentiment Analysis"*

<a href="https://github.com/gsi-upm/senpy">[2]</a>*"Senpy Documentation"*
