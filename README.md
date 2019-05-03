# tfrecords compiler

## Introduction

For this to work the compiler will need a config file at the top of the folder tree, and this readme will be dedicated
to explaning what to put into the json file and how the compiler will use it.

## The Structure Array

The most important object in the json file will be under the structure key. This will be the driver for how the compiler traverses the folder tree.


This is an array where each entry can be one of three numbers 0, .5,1. Each entry in the array designates a
level of the folder tree. If the number is zero then there is no data on that level(Here we note that when we say data we mean that there are two folders in each folder on this layer. One called domain, and one called targets. It is these folders that have the data in them.) If the number is .5 that layer is a mixed layer with some of the folders containing data and some of the layers containing sub-layers. A number of 1 is obvously a layer full of data.


We will note that the first index will designate the root of the tree. ie. [root, first layer, second layer, third layer, ...]