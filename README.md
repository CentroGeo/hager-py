# Hager python



![example workflow](https://github.com/CentroGeo/hager_py/actions/workflows/main.yml/badge.svg)

## Difusión espacial

En este taller vamos a trabajar con una implementación en Python del modelo de difusión espacial de <a href ="http://en.wikipedia.org/wiki/Torsten_H%C3%A4gerstrand" target="_blank">Torsten Hägerstrand</a>. Este modelo es una simulación tipo [Monte Carlo](http://en.wikipedia.org/wiki/Monte_Carlo_method) del proceso de difusión de innovaciones concebido originalmente por Hagerstrand en 1953.
Para este taller vamos a trabajar con la versión más simple del modelo, las suposiciones básicas son las siguientes:

1. Una sola persona tiene el *mensaje* al principio
2. La innovación es adoptada en cuanto se tiene contacto con ella
3. El mensaje se comunica *unicamente* en encuentros cara a cara
4. El mensaje se transmite en intervalos discretos en los que **todos** los adoptantes transmiten el mensaje a otra persona.
5. El espacio es homogeneo e isotrópico

En escencia, lo que hacemos es considerar al espacio *geográfico* como una retícula en la que cada elemento tiene el mismo número de habitantes. A partir de aquí, la probabilidad de que un habitante de una retícula contacte a otro habitante es función únicamente de la distancia.

La simulación Monte Carlo ocurre en dos etapas, para cada portador del mensaje:

1. Se selecciona al azar (de acuerdo a una función de probabilidad que decae con la distancia) la celda a la cual se transmite el mensaje.
2. Se selecciona otro número al azar para elegir el habitante de la celda que recibe el mensaje. Si este habitante es también portador de la innovación, queda inalterado.

Vamos ahora a jugar un poco con la implementación del modelo de Hagerstrand que está en esta misma carpeta.

## Install

`pip install your_project_name`

## How to use

Fill me in please! Don't forget code examples:

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
