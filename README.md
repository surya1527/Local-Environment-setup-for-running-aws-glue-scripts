# docker
</br>
</br>
<h2>The main object of this Environmental setup is to run aws services free through Docker.</h2>


 
 
 
Docker: Docker is a software platform that simplifies the process of building, running, managing and distributing applications.</br>

Docker Container: containers are runnable instance of an image. You can create, start, stop, move, or delete a container using Docker API or CLI.</br>

Docker Image: A Docker image is a read-only template that contains a set of instructions for creating a container that can run on the Docker platform.</br>

Jupyter Notebook: The Jupyter Notebook is an open-source web application that allows data scientists to create and share documents that integrate live code, equations, computational output, visualizations, and other multimedia resources, along with explanatory text in a single document.</br>

Aws Glue: AWS Glue is a fully managed ETL (extract, transform, and load) service that makes it simple to categorise your data, clean it, enrich it, and move it reliably between various data stores and data streams.</br>


In order to make a connection firstly it is required to install docker desktop [click here to download Docker Desktop](https://www.docker.com/products/docker-desktop)</br>

 

After the successful installation open cmd on windows or terminal on Mac and type </br>
</br>
```
docker --version
```
</br>

<img width="631" alt="Screenshot 2022-02-08 at 17 41 53" src="https://user-images.githubusercontent.com/58841159/152985799-8c3468a0-0ce9-418e-a53c-ef2a38510a44.png"></br>
</br>
As shown in the picture you need to get your installed version.</br>
</br>


After sucessfull installation of docker open the docker desktop in your system and then check the images section.</br>
You can that there will not be any images present.</br>
</br>
</br>
Open cmd on Windows or terminal on Mac and run the following command:
</br>
```
docker pull amazon/aws-glue-libs:glue_libs_1.0.0_image_01
```
Depending on your internet speed the image will be installed into your docker.</br>
Then after Sucessful installation, goto images section in docker and check weatehr the image which is installed is visible or not.</br>
You can see the installed image.</br>
Then again go to terminal and type: </br>
```
docker run -itd -p 8888:8888 -p 4040:4040 -v ~/.aws:/root/.aws:ro --name glue_jupyter amazon/aws-glue-libs:glue_libs_1.0.0_image_01 /home/jupyter/jupyter_start.sh
```



















