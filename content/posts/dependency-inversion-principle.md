---
title: "Dependency Inversion Principle"
date: 2022-04-05T09:05:00+01:00
draft: true
---
High-level classes shouldn’t depend on low-level classes. Both should depend on abstractions. Abstractions shouldn’t depend on details. Details should depend on abstractions.

## Concepts
### Flow of control
When a module calls a function, the flow of control passes from the function calling it to the function it is calling. The function now has the power to get some stuff done and can return something back to caller. Generally we naturally think about the flow of control flowing “downstream”. For example, it starts with an interface where a user presses a button. The interface calls a usecase the next layer down. The usecase coordinates reusable business logic in the domain layer which calls basic CRUD operations in the model layer. The flow of control naturally passes from the high-level classes to the low-level classes.

### Flow of dependency
Different to the flow of control is the flow of dependency. A module depends on another module if changes to the latter could result in changes to the first. In the above example the flow of control mirrors the flow of dependency. The interface depends on the use-case which depends on the domain, which depends on the models. If we change some parameters that the usecase requires, we’ll have to change the interfaces layer to be able to pass them in.
![Dependency and control flow](/dependency-inversion-fig-1.png) 
Fig 1: Model of dependency and control flow.



## Some Real World Examples
When customer goes to a restaurant they don’t just decide what ever they want to eat and tell the chef. That would mean the chef would be completely at the whim of the customer (fig. 2). What if they didn’t have the ingredients in stock? 
![Dependency and control flow chef example](/dependency-inversion-fig-2.png) 
Fig 2: Control and dependency flow from the chef to the customer. 

Instead the chef designs a menu (or interface) for the customer to choose from. The control still flows to the customer who can choose what they want, but the chef is no longer dependent on the customer choice, because the chef decides the menu (fig. 3). The dependency has been inverted.
![Dependency inversion flow chef example](/dependency-inversion-fig-3.png) 
Fig 3: Control still flows to the customer who decides what to eat, but what the customer eats depends on the menu which is decided by the Chef.

## Tech Examples
In code, you can do exactly the same thing. By introducing a high level interface that both high level and low level classes depend on the dependency is inverted and your code becomes much easier to maintain and add to.
In programming we often structure programmes as the interfaces at the top, that call use cases which coordinate reusable business logic modules which manipulate models. The direction of control flows from the high level downwards to the bottom. The principle of dependency inversion says we should avoid this and instead introduce high level abstractions that both high and low level classes depend on in order to reverse the direction of the dependency.
![Dependency inversion shop example](/dependency-inversion-fig-4.png) 

This is the basis for all APIs and frameworks. At KTL, we depend on the Django framework. But Django cannot depend on us. If Django had to change every time we deployed a change to Kraken, then that would be highly unproductive. Likewise, as we’ve been releasing Krakens in different countries, we’ve gradually been adding plugins so that core functionality depends on abstractions instead of the details of individual territories or clients. The result is modular code that lots of different teams can work on independently across multiple timezones.


