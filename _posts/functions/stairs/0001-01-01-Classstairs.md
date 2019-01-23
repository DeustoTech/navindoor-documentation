---
description: Representacion de una escalera. Es una subclase de la clase door. Esto se debe 
             a que dentro del framework las escaleras son mas bien una puerta que te conduce a 
             otra planta
visible: true
title: stairs
categories: [documentation, CT00]
layout: class
type: constructor
properties:
   connections: 
        type: double
        default: none
        description: able connections to stairs
      
methods:
   stairs:
        description: The stairs constructor need a array double of 3 dimension. 
        MandatoryInputs:   
          r: 
           description: Space point where is the node 
           class: double
           dimension: [1x3]
        OptionalInputs:
          obj:
           description: node object
           class: node
           dimension: [1x1]
        url: /documentation/ct00/stairs/stairs
   zeros:
        description:    zeros(N) is an N-by-N matrix of zeros.
                        zeros(M,N) or zeros([M,N]) is an M-by-N matrix of zeros.
                        zeros(M,N,P,...) or zeros([M N P ...]) is an M-by-N-by-P-by-... array of
                        zeros.
                        zeros(SIZE(A)) is the same size as A and all zeros.
                        zeros with no arguments is the scalar 0.
                        zeros(..., CLASSNAME) is an array of zeros of class specified by the
                        string CLASSNAME.
                        zeros(..., 'like', Y) is an array of zeros with the same data type, sparsity,
                        and complexity (real or complex) as the numeric variable Y.
        MandatoryInputs:   
          N: 
           description: Dimension
           class: integer
           dimension: [1x1]
        Outputs:
           z:
              description: List of zeros 
              class: staris
              dimension: [1xN]
        url: /documentation/ct00/stairs/zeros

---

Create a stairs

```matlab
st1 = stairs([10 10 1])
```


```

st1 = 

  stairs with properties:

    connections: []
          width: 0.7500
              r: [10 10 1]
          walls: []


```

```matlab
st2 = stairs([10 20 1]);
st3 = stairs([0 10 1]);
```


Create a node You can initializate memory with this class

```matlab
ListOfStairs = [st1 st2 st3]
```


```

ListOfStairs = 

  1x3 stairs array with properties:

    connections
    width
    r
    walls


```


And you can draw

```matlab
line(ListOfStairs,'Marker','s')
xlim([-5 15])
ylim([0 30])
```


![]({{site.url}}/{{site.baseurl}}/assets/imgs/CT00/class/main/stairs/copiaRM_01.png)

