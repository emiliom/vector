---
title: "Introduction"
teaching: 5
exercises: 0
---

## Tutorial provided by Emilio Mayorga, with help from Don Setiawan

## Student Prerequesites
* Python **conda**
  * To install conda and learn more about it, see the [GeoHackWeek conda tutorial](https://geohackweek.github.io/Introductory/00-conda-tutorial/)
  * A **conda** environment for the vector tutorial has been set up. It includes `geopandas` and its dependencies, which include (for vector-handling packages) `shapely`, `fiona`, `pyproj`, `descartes` and `pysal`, in addition to `pandas`, `numpy`, etc. These will be handled automatically by the conda environment. Additional conda packages available in the environment include `geojson`, `folium` (for interactive maps in Jupyter notebooks), `cartopy` and `mplleaflet`,`rasterstats` for simplified raster-vector analysis, and `psycopg2` for access to vector data stored in PostGIS. This environment will be available in the Docker image. It may be created independently with this command (once you understand how to work with conda): `conda create -c conda-forge -n vectorenv python=2.7 geopandas geojson pysal rasterstats seaborn mplleaflet folium cartopy jupyter`
* Ideally some familiarity with GIS concepts regarding vector spatial objects (points, lines, polygons, etc).


## Docker Instruction to follow along

Docker image is located on this link: [geohackweek2016/vectortutorial](https://hub.docker.com/r/geohackweek2016/vectortutorial/)

Here are the steps to create a docker container that runs the ipython notebook within the docker container:

**Linux/OS X**

Pull the docker image
  
~~~
$ docker pull geohackweek2016/vectortutorial
~~~
{: .bash}

Create docker container

~~~
$ docker run -i -t -p 8888:8888 --name vector_tutorial geohackweek2016/vectortutorial
~~~
{: .bash}

Activate `vectorenv` conda environment

~~~
# source activate vectorenv
~~~
{: .bash}

Run jupyter notebook

~~~
# jupyter notebook --notebook-dir=/notebooks --ip="*" --port=8888 --no-browser
~~~
{: .bash}

Open web browser on your local host machine and put `localhost:8888` on your address bar to view notebook.

**Windows**

In the docker prompt:

~~~
$ docker-machine ip default
~~~
{: .bash}

*let's call the returned values the "IPaddress"*

Pull the image

~~~
$ docker pull geohackweek2016/vectortutorial
~~~
{: .bash}

Create docker container

~~~
$ docker run -i -t -p 8888:8888 --name vector_tutorial geohackweek2016/vectortutorial
~~~
{: .bash}

Activate `vectorenv` conda environment

~~~
# source activate vectorenv
~~~
{: .bash}

Run jupyter notebook

~~~
# jupyter notebook --notebook-dir=/notebooks --ip="*" --port=8888 --no-browser
~~~
{: .bash}

Open web browser on your local host machine and put `IPaddress:8888` on your address bar to view notebook.

## Overview
1. Geospatial Concepts
2. Encodings, Formats and Libraries
3. GeoPandas Introduction
4. GeoPandas Advanced Topics

