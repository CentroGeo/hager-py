# Hager python



![example workflow](https://github.com/CentroGeo/hager_py/actions/workflows/main.yml/badge.svg)

## Difusi�n espacial

En este taller vamos a trabajar con una implementaci�n en Python del modelo de difusi�n espacial de [Torsten H�gerstrand](http://en.wikipedia.org/wiki/Torsten_H%C3%A4gerstrand). Este modelo es una simulaci�n tipo [Monte Carlo](http://en.wikipedia.org/wiki/Monte_Carlo_method) del proceso de difusi�n de innovaciones concebido originalmente por Hagerstrand en 1953.
Para este taller vamos a trabajar con la versi�n m�s simple del modelo, las suposiciones b�sicas son las siguientes:

1. Una sola persona tiene el *mensaje* al principio
2. La innovaci�n es adoptada en cuanto se tiene contacto con ella
3. El mensaje se comunica *unicamente* en encuentros cara a cara
4. El mensaje se transmite en intervalos discretos en los que **todos** los adoptantes transmiten el mensaje a otra persona.
5. El espacio es homogeneo e isotr�pico

En escencia, lo que hacemos es considerar al espacio *geogr�fico* como una ret�cula en la que cada elemento tiene el mismo n�mero de habitantes. A partir de aqu�, la probabilidad de que un habitante de una ret�cula contacte a otro habitante es funci�n �nicamente de la distancia.

La simulaci�n Monte Carlo ocurre en dos etapas, para cada portador del mensaje:

1. Se selecciona al azar (de acuerdo a una funci�n de probabilidad que decae con la distancia) la celda a la cual se transmite el mensaje.
2. Se selecciona otro n�mero al azar para elegir el habitante de la celda que recibe el mensaje. Si este habitante es tambi�n portador de la innovaci�n, queda inalterado.

Vamos ahora a jugar un poco con la implementaci�n del modelo de Hagerstrand que est� en esta misma carpeta.

## Install

`pip install your_project_name`

## How to use

Fill me in please! Don't forget code examples:

## Data analysis

In this part of the workshop we are going to analyze, using ESDA (Exploratory Spatial Data Analysis) tools, the data generated with the Hagerstrand model. The goal is to begin to understand the relationship between spatial statistics and the processes that give rise to the distributions that we observe.

To analyze the data we are going to use the [pysal](https://pysal.readthedocs.org/en/latest/) analysis library, which is the Python equivalent of the OpenGeoda software.

As you know, [Moran's Index](http://en.wikipedia.org/wiki/Moran%27s_I) measures the spatial autocorrelation of spatial distributions. Let's use this measure to analyze the results of the model, let's start with random diffusion:

```
1+1
```




    2



```
s= SimpleDiffusion(100,100,5,20,[(20,20)],0.2,20)
```

```
s.mixed_diffusion(0.7)
```
