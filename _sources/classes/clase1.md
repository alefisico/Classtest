---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
markdown_extensions:
      - admonition
---

# Clase Demostrativa

## Técnicas de simulación de sistemas dinámicos: Runge Kutta con paso adaptivo.

``````{admonition} Qué vamos a ver en esta clase?
:class: seealso
Vamos a aprender formas analíticas de resolver sistemas de ecuaciones en sistemas dinámicos.
``````

``````{admonition} Objetivos
:class: tip
Conocer el método de Runge Kutta para resolver ecuaciones diferenciales en sistemas dinámicos.
``````

### Quick recap

Vamos a recordar algunas definiciones que serán útiles en esta clase:

``````{admonition} Sistemas No lineales
:class: note

Son sistemas que no pueden ser descritos por sistemas de ecuaciones lineales. Para sistemas no lineales, no siempre se puede encontrar una solución explicita a un problema con cualquier condición inicial. Es por eso que encontrar una solución analítica a estos problemas no es posible.
``````

``````{admonition} Linearidad
:class: note

Para que una función satisfaga el principio de linealidad debe tener las siguientes propiedades:
 * Aditividad: $\textstyle f(x + y) = f(x) + f(y)$
 * Homogeneidad: $f(\alpha x) = \alpha f(x)$

Un sistema descrito por ecuaciones diferenciales no es *lineal* si no es un sistema de ecuaciones que cumplan los requisitos previos.
``````


``````{admonition} Sistema dinámico
:class: note

Son formas de describir el *paso del tiempo* en todos los puntos del espacio $\mathcal S$, que puede ser por ejemplo el espacio de estados de un sistema físico.
``````


### Métodos de Runge Kutta

Estos son una familia de métodos *iterativos* en análisis numérico que nos permiten resolver de forma numérica ecuaciones diferenciales. A pesar de su simplicidad, estos métodos son muy precisos y se ha demostrado que se tienen un buen comportamiento en muchos problemas.

La idea general en todos estos métodos es aproximar el resultado de una función/curva desconocida conociendo las condiciones iniciales. Empecemos con el método más sencillo de resolver ecuaciones diferenciales, conocido como el método de Euler.

#### Método de Euler

La idea del método de Euler es simple. Cuando la forma específica del resultado no es conocida, su condición inicial si lo es ($A_0$). Así, la pendiente de la curva puede ser calculada en el punto $A_0$ de la ecuación diferencial, y de esta manera su línea tangente. Si nos movemos un *paso* por esta tangente podemos encontrar un punto $A_1$ desde donde volvemos a calcular la pendiente.

Notese que la precisión de este método depende del tamaño de este paso. 

![Euler method simple demostration](../images/clase1/Euler_method.svg)

Empecemos con un ejemplo simple:

\begingroup
\fontfamily{ppl}\fontsize{20}{22}\selectfont
$$ \frac{dx}{dz} $$
\endgroup


```{note}
My directive content
```
