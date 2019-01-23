---
description: Representacion de un punto 
visible: true
title: node
categories: [documentation, CT00]
layout: class
type: constructor
properties:
   r: 
        type: "double"
        default: "none"
        description: This property is a array 1x3 that contains the [x y z].
      
   walls: 
        type: "Functional"
        default: "none"
        description: This property contains the walls which this node is children.
      
methods:
   times:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5
        url: /documentation/ct00/node/times
   plus:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5    
        url: /documentation/ct00/node/plus
   minus:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5   
        url: /documentation/ct00/node/minus
   eq:
        description: This method comprobe that the two nodes have the same r property
        MandatoryInputs:   
          lobj2: 
              description: second node
              class: ControlParameterDependent
              dimension: [1xN]
          lobj1: 
              description: first node
              class: double
              dimension: [1xM]
        Outputs:
          result:
              description: Boolean that indicate if lobj1==lobj2
              class: logical
              dimension: [NxM]       
        url: /documentation/ct00/node/eq
   node:
        description: The node constructor need a array double of 3 dimension. 
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
        url: /documentation/ct00/node/node
   zeros:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5
          beta:
           description: This number is the power of the control, is define by follow expresion $$J = \min_{u \in L^2(0,T)} \frac{1}{2} \left[ \frac{1}{|\mathcal{K}|} \sum_{\nu \in \mathcal{K}} x \left( T, \nu \right) - \bar{x} \right]^2  + \frac{\beta}{2} \int_0^T u^2 \mathrm{d}t, \quad \beta \in \mathbb{R}^+ $$ 
           class: double
           dimension: [1x1]
           default:   1e-1
          MaxIter:
           description: Maximun of iterations of this method
           class: double
           dimension: [1x1]
           default:   100
        url: /documentation/ct00/node/zeros
   DeleteSelect:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5
        url: /documentation/ct00/node/DeleteSelect
   line:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5
        url: /documentation/ct00/node/line
   line3:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5
        url: /documentation/ct00/node/line3
   mustBeDiff:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5
        url: /documentation/ct00/node/mustBeDiff
   select:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5
        url: /documentation/ct00/node/select
   unselect:
        description: This function solve a particular optimal control problem using
          the stochastic gradient descent algorithm. The restriction of the optimization 
          problem is a parameter-dependent finite dimensional linear system. Then, the 
          resulting states depend on a certain parameter. Therefore, the functional is
          constructed to control the average of the states with respect to this parameter.
          See Also in AverageClassicalGradient
        autor: AnaN
        MandatoryInputs:   
          iCPD: 
           description: Control Parameter Dependent Problem 
           class: ControlParameterDependent
           dimension: [1x1]
          xt: 
           description: The target vector where you want the system to go
           class: double
           dimension: [iCPD.Nx1]
        OptionalInputs:
          tol:
           description: tolerance of algorithm, this number is compare with $J(k)-J(k-1)$
           class: double
           dimension: [1x1]
           default:   1e-5
        url: /documentation/ct00/node/unselect

---
```matlab
% Existen distintas formas de crear un punto
n1 = node([1 1 1]);

line(n1,'Marker','*')
```


![]({{site.url}}/{{site.baseurl}}/assets/imgs/CT00/class/main/node/copiaRM_01.png)

