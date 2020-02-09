# quantitative_trading

some useful websites:

https://www.quora.com/What-are-good-online-tutorials-on-beginning-algorithmic-trading
https://quantiacs.com/Home.aspx

To run the tutorial_altrading.ipynb smoothly, one can download the docker images file using docker or singularity.

$ docker pull xianhedocker/quant_trading:1.0

or

$ singularity pull docker//:xianhedocker/quant_trading:1.0

To run the container image, forward the port

$ docker run -p 8890:8888 xianhedocker/quant_trading:1.0 jupyter lab

To mount local files to the container image

$ docker run -v /local_folder/:/home/jovyan/work/ -p 8890:8888 xianhedocker/quant_trading:1.0 jupyter lab
replace /local_folder/ with your files' path.
/home/jovyan/work/ is the mounted directory inside the container instance.

You can then open your web browser and type http://localhost:8890/
