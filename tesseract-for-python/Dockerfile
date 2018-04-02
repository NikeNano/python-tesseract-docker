FROM ubuntu:16.04
MAINTAINER nikenano
RUN apt-get update && apt-get install -y software-properties-common && add-apt-repository -y ppa:alex-p/tesseract-ocr
RUN apt-get update && apt-get install -y tesseract-ocr-swe 
RUN apt-get update 
RUN apt-get -y upgrade
RUN apt-get install python-pip -y
RUN pip install pytesseract
RUN pip install pillow
RUN pip install jupyter
RUN pip install opencv-python
COPY . /notebooks
CMD jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
