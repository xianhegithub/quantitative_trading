# quantitative_trading

some useful websites:

https://www.quora.com/What-are-good-online-tutorials-on-beginning-algorithmic-trading
https://quantiacs.com/Home.aspx

To run the tutorial_altrading.ipynb smoothly, one can download the docker images file using docker or singularity.
You first need a docker hub account and login in in the command line.

$ docker login
errors might occur at login, most of them can be fixed by typing in the command
$sudo chmod 666 /var/run/docker.sock

Once login, pull the container image
$ docker pull xianhedocker/quant_trading:1.1. or
$ singularity pull docker//:xianhedocker/quant_trading:1.1

To run the container image, forward the port
$ docker run -p 8888:8888 xianhedocker/quant_trading:1.1 jupyter lab

To mount local files to the container image
$ docker run -v /local_folder/:/home/jovyan/work/ -p 8888:8888 xianhedocker/quant_trading:1.1 jupyter lab

replace /local_folder/ with your files' path.
/home/jovyan/work/ is the mounted directory inside the container instance.

You can then open your web browser and type http://localhost:8888/
