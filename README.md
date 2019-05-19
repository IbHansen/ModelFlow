# ModelFlow
A Python toolkit to manage models

The easy way to start is here [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/IbHansen/modelflow/master). This will start **ModelFlow** as an online Jupyter notebook. Select one of the notebooks (files with the extension .ipynb). You can also look at the python files of the system. Located at the **modelflow/** folder

Alternative look at the *getting started* section later in this file. It explains how to run ModelFlow localy. 

The **Pandas** library is a great library to handle all kinds of datamanipulation and transformations. 

However when it comes to models which contains lags or models which requires solving simultanous equations, Pandas is not quite helpful. 

ModelFlow extends Pandas to handle a range of such models. And they can be large.  

It requires you to specify the *model* specified as equations (the **business logic**) and place the *data* in a Pandas  **DataFrame**.  ModelFlow allows the model to meet the data and return the result as a new DataFrame. 

A number of **analytical tools for model and result analytic** helps to understand the model and its results.

The user can **extend and modify the tools** to her or his needs.

**Onboarding models and combining models from different sources**. Creating a Macro prudential model often entails recycling several models specified in different ways: Excel, Latex, Dynare, Python or other languages. Python's ecosystem makes it possible to transform many different models into ModelFlow models or to wrap them into functions which can be called from ModelFlow models.

**Models can be specified in a high level Business logic language (a Domain Specific language)**. This allows the formulation of a model in a concise and expressive language which is close to the economic of the model. The user can concentrate on the economic or financial content - not the coding of the solution. The code for solving the model is generated by the tool. Then you can *solve the
simultaneous* (or *non-simultaneous* model) in an efficient way. 

## Introduction 

**ModelFlow is written in Python**. Python comes "batteries included" and is
the basis of a very rich ecosystem, which consists of a wide array of
libraries. ModelFlow is just another library. It supplements the existing
libraries regarding modeling language and solving and allows the use of
Python as a model management framework.

**Data handling and wrangling is done in the Pandas library**. This
library is the Swiss army knife of data science in Python. It can import and export data to most systems and it is very powerful in manipulating and transforming data.
The core
element of Pandas is the *Dataframe*. A Dataframe is a two-dimensional
tabular data structure. Each *column* consists of cells of the same type
-- it can be a number, a string, a matrix or another Python data object.This includes matrices and other dataframes. Each *row is indexed.* The index can basically be any type of variable
including dates, which is especially relevant for economic and financial models.

**ModelFlow gives the user tools for more than solving models**. This
includes:

-   *Visualization* and comparison of results

-   *Integration* of models from different sources

-   *Analyze the logical structure of a model*. By applying graph theory, 
    ModelFlow can find data lineage, find a suitable calculating sequence and trace 
    causes of changes through the calculations.

-   *Inverting* the model to calculating the necessary instruments to
    achieve a desired target.

-   Calculating the *attributions* from input to the results of a model.

-   Calculating the *attribution* from input to the result of each
    formula.

-   Finding and calculating partial *derivatives* of formulas

-   *Integrating user defined python functions* in the Business logic
    language (like optimization, calculating risk weights or to make a matrices consistent with the RAS algorithm  )

-   *Wrap matlab* models so they can be used in the Business logic
    language.

-   *Speed up* solving using "Just in time compilation"

-   Analyze the model structure through tools from graph theory

-   Handle *large models.* 1,000,000 formulas is not a problem.

-   Integrate model management in Jupyter notebooks for *agile and user
    friendly model use*


**The core code of ModelFlow is small and
documented.** Thus it can easily be modified and expanded to the specific need of the user. *ModelFlow is a toolset*. It can handle models, which conform to the tools.

If you need a feature or have a model which can't be handled in ModelFlow,
you are encouraged to improve ModelFlow. Please share the
improvement, other users may have the same need, or can be inspired by
your work.

Also bear in mind that ModelFlow is experimental. It is provided ”as is”, without any representation or warranty of any kind either express or implied.   

## Getting started

You need Python 3.6+ with asssociated libraries. The easy way is to install Anaconda Python [https://www.anaconda.com/distribution](https://www.anaconda.com/distribution)

In addition to the standard packagdes in the Anaconda distribution you need: **Graphviz** and **cvxopt**: they can be installed by running a command window from the Anaconda prompt and execute theese commands 
```
conda install graphviz
conda install cvxopt
```
You will find the anaconda prompt by searching "anaconda" in the start menu search field

Now you want to download the modelflow repo. This can be done either using git or by downloading the repo as a zip file and unzip the content in your local drive. you can use any location but one suggestion could be c:\modelflow.

Now you want the PYTHONPATH enviroment variable to point to the location of the model flow library. In this case c:modelflow\src. This is most easily done through the Spyder editor:tools>PYTHONPATH manager. Add the pahth and press the syncrize buttom to syncronize the spyder PYTHONPATH with the environment variable.

Now you are in business. Try out one of the workbooks. to do this you
```
click on the Adaconda prompth in the Anaconda folder
cd <The location you have downloaded the workbooks>
jupyter notebook
```
