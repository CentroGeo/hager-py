# Hager python 



![example workflow](https://github.com/CentroGeo/hager_py/actions/workflows/main.yml/badge.svg)

## Spatial Diffusion


In this workshop we are going to work with a Python implementation of the [Torsten Hägerstrand](http://en.wikipedia.org/wiki/Torsten_H%C3%A4gerstrand) spatial diffusion model. This model is a [Monte Carlo](http://en.wikipedia.org/wiki/Monte_Carlo_method) simulation of the innovation diffusion process originally conceived by Hagerstrand in 1953. For this workshop we are going to work with the simplest version of the model, the basic assumptions are the following:

1. Just one person has the message at the beginning
2. Innovation is adopted as soon as it is contacted
3. The message is only communicated in face-to-face meetings
4. The message is transmitted in discrete intervals in which all the adopters transmit the message to another person.
5. Space is homogeneous and isotropic

In essence, what we do is consider geographic space as a grid in which each element has the same number of inhabitants. From here, the probability that an inhabitant of a grid contacts another inhabitant is a function of distance only.

The Monte Carlo simulation occurs in two stages, for each carrier of the message:

1. The cell which transmits the message is randomly selected (according to a probability function that decays with distance).
2. Another number is selected randomly to choose the inhabitant of the cell that receives the message. If this inhabitant is also the bearer of innovation, it remains unaltered.

We are now going to work a bit with the implementation of the Hagerstrand model that is in this same folder.

## Install

`pip install git+https://github.com/CentroGeo/hager_py`

## How to use

Fill me in please! Don't forget code examples:

```
s= SimpleDiffusion(100,100,5,20,[(20,20)],0.2,20)
```

```
s.mixed_diffusion(0.7)
```

    finished
    There are 175693 adopters out of a total of 200000 inhabitants
    The total number of iterations performed is: 20

