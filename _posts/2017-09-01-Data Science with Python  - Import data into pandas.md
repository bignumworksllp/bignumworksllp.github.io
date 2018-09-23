---
layout: post
title: Data Science with Python - Import data into pandas
author: Harish Garg
categories: Python, DataScience
tags: [Python, Pandas, Data Analysis, Data Science]
published: true
---
## Introduction ### 
In this article, I will walk you through on how to import csv data into pandas and start exploring it.

## import pandas module
We start with importing the pandas module.

```python
import pandas as pd
```
## Introudce dataset
Next, we will read a csv file using pandas. It’s a csv file containing columns as Rank, country, gold, silver, bronze and total medals 

![Data](/assets/images/Screenshot-Data-Olympics-CSV.png)

This is the data we are going to be using for this lesson.
The data we are using is from Rio Olympics
The data is a list of countries and the medals they won.

## Import dataset
To read csv data into pandas, we will use pandas read_csv method
The read data will be read in a pandas dataframe object. 

```python
df = pd.read_csv('olympics.csv')
```
DataFrame is a 2-dimensional labeled data structure with columns of potentially different types. You can think of it like a spreadsheet or SQL table. 
It is the most commonly used pandas object. 

To print the data inside the dataframe, we just call it’s name, like this


```python
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Country</th>
      <th>Gold</th>
      <th>Silver</th>
      <th>Bronze</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>United States (USA)</td>
      <td>46</td>
      <td>37</td>
      <td>38</td>
      <td>121</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Great Britain (GBR)</td>
      <td>27</td>
      <td>23</td>
      <td>17</td>
      <td>67</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>China (CHN)</td>
      <td>26</td>
      <td>18</td>
      <td>26</td>
      <td>70</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Russia (RUS)</td>
      <td>19</td>
      <td>17</td>
      <td>19</td>
      <td>55</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Germany (GER)</td>
      <td>17</td>
      <td>10</td>
      <td>15</td>
      <td>42</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Japan (JPN)</td>
      <td>12</td>
      <td>8</td>
      <td>21</td>
      <td>41</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>France (FRA)</td>
      <td>10</td>
      <td>18</td>
      <td>14</td>
      <td>42</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>South Korea (KOR)</td>
      <td>9</td>
      <td>3</td>
      <td>9</td>
      <td>21</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Italy (ITA)</td>
      <td>8</td>
      <td>12</td>
      <td>8</td>
      <td>28</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Australia (AUS)</td>
      <td>8</td>
      <td>11</td>
      <td>10</td>
      <td>29</td>
    </tr>
    <tr>
      <th>10</th>
      <td>11</td>
      <td>Netherlands (NED)</td>
      <td>8</td>
      <td>7</td>
      <td>4</td>
      <td>19</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12</td>
      <td>Hungary (HUN)</td>
      <td>8</td>
      <td>3</td>
      <td>4</td>
      <td>15</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13</td>
      <td>Brazil (BRA)*</td>
      <td>7</td>
      <td>6</td>
      <td>6</td>
      <td>19</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14</td>
      <td>Spain (ESP)</td>
      <td>7</td>
      <td>4</td>
      <td>6</td>
      <td>17</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15</td>
      <td>Kenya (KEN)</td>
      <td>6</td>
      <td>6</td>
      <td>1</td>
      <td>13</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16</td>
      <td>Jamaica (JAM)</td>
      <td>6</td>
      <td>3</td>
      <td>2</td>
      <td>11</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17</td>
      <td>Croatia (CRO)</td>
      <td>5</td>
      <td>3</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18</td>
      <td>Cuba (CUB)</td>
      <td>5</td>
      <td>2</td>
      <td>4</td>
      <td>11</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19</td>
      <td>New Zealand (NZL)</td>
      <td>4</td>
      <td>9</td>
      <td>5</td>
      <td>18</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20</td>
      <td>Canada (CAN)</td>
      <td>4</td>
      <td>3</td>
      <td>15</td>
      <td>22</td>
    </tr>
    <tr>
      <th>20</th>
      <td>21</td>
      <td>Uzbekistan (UZB)</td>
      <td>4</td>
      <td>2</td>
      <td>7</td>
      <td>13</td>
    </tr>
    <tr>
      <th>21</th>
      <td>22</td>
      <td>Kazakhstan (KAZ)</td>
      <td>3</td>
      <td>5</td>
      <td>9</td>
      <td>17</td>
    </tr>
    <tr>
      <th>22</th>
      <td>23</td>
      <td>Colombia (COL)</td>
      <td>3</td>
      <td>2</td>
      <td>3</td>
      <td>8</td>
    </tr>
    <tr>
      <th>23</th>
      <td>24</td>
      <td>Switzerland (SUI)</td>
      <td>3</td>
      <td>2</td>
      <td>2</td>
      <td>7</td>
    </tr>
    <tr>
      <th>24</th>
      <td>25</td>
      <td>Iran (IRI)</td>
      <td>3</td>
      <td>1</td>
      <td>4</td>
      <td>8</td>
    </tr>
    <tr>
      <th>25</th>
      <td>26</td>
      <td>Greece (GRE)</td>
      <td>3</td>
      <td>1</td>
      <td>2</td>
      <td>6</td>
    </tr>
    <tr>
      <th>26</th>
      <td>27</td>
      <td>Argentina (ARG)</td>
      <td>3</td>
      <td>1</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <th>27</th>
      <td>28</td>
      <td>Denmark (DEN)</td>
      <td>2</td>
      <td>6</td>
      <td>7</td>
      <td>15</td>
    </tr>
    <tr>
      <th>28</th>
      <td>29</td>
      <td>Sweden (SWE)</td>
      <td>2</td>
      <td>6</td>
      <td>3</td>
      <td>11</td>
    </tr>
    <tr>
      <th>29</th>
      <td>30</td>
      <td>South Africa (RSA)</td>
      <td>2</td>
      <td>6</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>57</th>
      <td>54</td>
      <td>Singapore (SIN)</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>58</th>
      <td>54</td>
      <td>Tajikistan (TJK)</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>59</th>
      <td>60</td>
      <td>Malaysia (MAS)</td>
      <td>0</td>
      <td>4</td>
      <td>1</td>
      <td>5</td>
    </tr>
    <tr>
      <th>60</th>
      <td>61</td>
      <td>Mexico (MEX)</td>
      <td>0</td>
      <td>3</td>
      <td>2</td>
      <td>5</td>
    </tr>
    <tr>
      <th>61</th>
      <td>62</td>
      <td>Algeria (ALG)</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>62</th>
      <td>62</td>
      <td>Ireland (IRL)</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>63</th>
      <td>64</td>
      <td>Lithuania (LTU)</td>
      <td>0</td>
      <td>1</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>64</th>
      <td>65</td>
      <td>Bulgaria (BUL)</td>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>65</th>
      <td>65</td>
      <td>Venezuela (VEN)</td>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>66</th>
      <td>67</td>
      <td>India (IND)</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>67</th>
      <td>67</td>
      <td>Mongolia (MGL)</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>68</th>
      <td>69</td>
      <td>Burundi (BDI)</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>69</th>
      <td>69</td>
      <td>Grenada (GRN)</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>70</th>
      <td>69</td>
      <td>Niger (NIG)</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>71</th>
      <td>69</td>
      <td>Philippines (PHI)</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>72</th>
      <td>69</td>
      <td>Qatar (QAT)</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>73</th>
      <td>74</td>
      <td>Norway (NOR)</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>4</td>
    </tr>
    <tr>
      <th>74</th>
      <td>75</td>
      <td>Egypt (EGY)</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>75</th>
      <td>75</td>
      <td>Tunisia (TUN)</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>76</th>
      <td>77</td>
      <td>Israel (ISR)</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>77</th>
      <td>78</td>
      <td>Austria (AUT)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>78</th>
      <td>78</td>
      <td>Dominican Republic (DOM)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>79</th>
      <td>78</td>
      <td>Estonia (EST)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>80</th>
      <td>78</td>
      <td>Finland (FIN)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>81</th>
      <td>78</td>
      <td>Morocco (MAR)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>82</th>
      <td>78</td>
      <td>Moldova (MDA)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>83</th>
      <td>78</td>
      <td>Nigeria (NGR)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>84</th>
      <td>78</td>
      <td>Portugal (POR)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>85</th>
      <td>78</td>
      <td>Trinidad and Tobago (TTO)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>86</th>
      <td>78</td>
      <td>United Arab Emirates (UAE)</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>87 rows × 6 columns</p>
</div>

As you can see, our csv data is now a 2D data structure and each individual element can be accessed directly

If no index is specified, pandas automatically assigns a index, starting from 0. 
However, in our case, we may want to specify country as the index. In that case we have to pass a extra option to the read_csv table like this.

```python
df = pd.read_csv('olympics.csv', index_col='Country')
```


```python
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Gold</th>
      <th>Silver</th>
      <th>Bronze</th>
      <th>Total</th>
    </tr>
    <tr>
      <th>Country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>United States (USA)</th>
      <td>1</td>
      <td>46</td>
      <td>37</td>
      <td>38</td>
      <td>121</td>
    </tr>
    <tr>
      <th>Great Britain (GBR)</th>
      <td>2</td>
      <td>27</td>
      <td>23</td>
      <td>17</td>
      <td>67</td>
    </tr>
    <tr>
      <th>China (CHN)</th>
      <td>3</td>
      <td>26</td>
      <td>18</td>
      <td>26</td>
      <td>70</td>
    </tr>
    <tr>
      <th>Russia (RUS)</th>
      <td>4</td>
      <td>19</td>
      <td>17</td>
      <td>19</td>
      <td>55</td>
    </tr>
    <tr>
      <th>Germany (GER)</th>
      <td>5</td>
      <td>17</td>
      <td>10</td>
      <td>15</td>
      <td>42</td>
    </tr>
    <tr>
      <th>Japan (JPN)</th>
      <td>6</td>
      <td>12</td>
      <td>8</td>
      <td>21</td>
      <td>41</td>
    </tr>
    <tr>
      <th>France (FRA)</th>
      <td>7</td>
      <td>10</td>
      <td>18</td>
      <td>14</td>
      <td>42</td>
    </tr>
    <tr>
      <th>South Korea (KOR)</th>
      <td>8</td>
      <td>9</td>
      <td>3</td>
      <td>9</td>
      <td>21</td>
    </tr>
    <tr>
      <th>Italy (ITA)</th>
      <td>9</td>
      <td>8</td>
      <td>12</td>
      <td>8</td>
      <td>28</td>
    </tr>
    <tr>
      <th>Australia (AUS)</th>
      <td>10</td>
      <td>8</td>
      <td>11</td>
      <td>10</td>
      <td>29</td>
    </tr>
    <tr>
      <th>Netherlands (NED)</th>
      <td>11</td>
      <td>8</td>
      <td>7</td>
      <td>4</td>
      <td>19</td>
    </tr>
    <tr>
      <th>Hungary (HUN)</th>
      <td>12</td>
      <td>8</td>
      <td>3</td>
      <td>4</td>
      <td>15</td>
    </tr>
    <tr>
      <th>Brazil (BRA)*</th>
      <td>13</td>
      <td>7</td>
      <td>6</td>
      <td>6</td>
      <td>19</td>
    </tr>
    <tr>
      <th>Spain (ESP)</th>
      <td>14</td>
      <td>7</td>
      <td>4</td>
      <td>6</td>
      <td>17</td>
    </tr>
    <tr>
      <th>Kenya (KEN)</th>
      <td>15</td>
      <td>6</td>
      <td>6</td>
      <td>1</td>
      <td>13</td>
    </tr>
    <tr>
      <th>Jamaica (JAM)</th>
      <td>16</td>
      <td>6</td>
      <td>3</td>
      <td>2</td>
      <td>11</td>
    </tr>
    <tr>
      <th>Croatia (CRO)</th>
      <td>17</td>
      <td>5</td>
      <td>3</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <th>Cuba (CUB)</th>
      <td>18</td>
      <td>5</td>
      <td>2</td>
      <td>4</td>
      <td>11</td>
    </tr>
    <tr>
      <th>New Zealand (NZL)</th>
      <td>19</td>
      <td>4</td>
      <td>9</td>
      <td>5</td>
      <td>18</td>
    </tr>
    <tr>
      <th>Canada (CAN)</th>
      <td>20</td>
      <td>4</td>
      <td>3</td>
      <td>15</td>
      <td>22</td>
    </tr>
    <tr>
      <th>Uzbekistan (UZB)</th>
      <td>21</td>
      <td>4</td>
      <td>2</td>
      <td>7</td>
      <td>13</td>
    </tr>
    <tr>
      <th>Kazakhstan (KAZ)</th>
      <td>22</td>
      <td>3</td>
      <td>5</td>
      <td>9</td>
      <td>17</td>
    </tr>
    <tr>
      <th>Colombia (COL)</th>
      <td>23</td>
      <td>3</td>
      <td>2</td>
      <td>3</td>
      <td>8</td>
    </tr>
    <tr>
      <th>Switzerland (SUI)</th>
      <td>24</td>
      <td>3</td>
      <td>2</td>
      <td>2</td>
      <td>7</td>
    </tr>
    <tr>
      <th>Iran (IRI)</th>
      <td>25</td>
      <td>3</td>
      <td>1</td>
      <td>4</td>
      <td>8</td>
    </tr>
    <tr>
      <th>Greece (GRE)</th>
      <td>26</td>
      <td>3</td>
      <td>1</td>
      <td>2</td>
      <td>6</td>
    </tr>
    <tr>
      <th>Argentina (ARG)</th>
      <td>27</td>
      <td>3</td>
      <td>1</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <th>Denmark (DEN)</th>
      <td>28</td>
      <td>2</td>
      <td>6</td>
      <td>7</td>
      <td>15</td>
    </tr>
    <tr>
      <th>Sweden (SWE)</th>
      <td>29</td>
      <td>2</td>
      <td>6</td>
      <td>3</td>
      <td>11</td>
    </tr>
    <tr>
      <th>South Africa (RSA)</th>
      <td>30</td>
      <td>2</td>
      <td>6</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>Singapore (SIN)</th>
      <td>54</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Tajikistan (TJK)</th>
      <td>54</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Malaysia (MAS)</th>
      <td>60</td>
      <td>0</td>
      <td>4</td>
      <td>1</td>
      <td>5</td>
    </tr>
    <tr>
      <th>Mexico (MEX)</th>
      <td>61</td>
      <td>0</td>
      <td>3</td>
      <td>2</td>
      <td>5</td>
    </tr>
    <tr>
      <th>Algeria (ALG)</th>
      <td>62</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Ireland (IRL)</th>
      <td>62</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Lithuania (LTU)</th>
      <td>64</td>
      <td>0</td>
      <td>1</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>Bulgaria (BUL)</th>
      <td>65</td>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Venezuela (VEN)</th>
      <td>65</td>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>India (IND)</th>
      <td>67</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Mongolia (MGL)</th>
      <td>67</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Burundi (BDI)</th>
      <td>69</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Grenada (GRN)</th>
      <td>69</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Niger (NIG)</th>
      <td>69</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Philippines (PHI)</th>
      <td>69</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Qatar (QAT)</th>
      <td>69</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Norway (NOR)</th>
      <td>74</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>4</td>
    </tr>
    <tr>
      <th>Egypt (EGY)</th>
      <td>75</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Tunisia (TUN)</th>
      <td>75</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Israel (ISR)</th>
      <td>77</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Austria (AUT)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Dominican Republic (DOM)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Estonia (EST)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Finland (FIN)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Morocco (MAR)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Moldova (MDA)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Nigeria (NGR)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Portugal (POR)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Trinidad and Tobago (TTO)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>United Arab Emirates (UAE)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>87 rows × 5 columns</p>
</div>

Now, we have Country name as index for our dataframe.

To check, what are the datatypes of the various columns, we can call dtypes on the dataframe we just created

```python
df.dtypes
```




    Rank      int64
    Gold      int64
    Silver    int64
    Bronze    int64
    Total     int64
    dtype: object

To see the top rows of the dataframe, use the head method


```python
df.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Gold</th>
      <th>Silver</th>
      <th>Bronze</th>
      <th>Total</th>
    </tr>
    <tr>
      <th>Country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>United States (USA)</th>
      <td>1</td>
      <td>46</td>
      <td>37</td>
      <td>38</td>
      <td>121</td>
    </tr>
    <tr>
      <th>Great Britain (GBR)</th>
      <td>2</td>
      <td>27</td>
      <td>23</td>
      <td>17</td>
      <td>67</td>
    </tr>
    <tr>
      <th>China (CHN)</th>
      <td>3</td>
      <td>26</td>
      <td>18</td>
      <td>26</td>
      <td>70</td>
    </tr>
    <tr>
      <th>Russia (RUS)</th>
      <td>4</td>
      <td>19</td>
      <td>17</td>
      <td>19</td>
      <td>55</td>
    </tr>
    <tr>
      <th>Germany (GER)</th>
      <td>5</td>
      <td>17</td>
      <td>10</td>
      <td>15</td>
      <td>42</td>
    </tr>
  </tbody>
</table>
</div>

To see the bottom rows of the dataframe, use tail method


```python
df.tail()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Gold</th>
      <th>Silver</th>
      <th>Bronze</th>
      <th>Total</th>
    </tr>
    <tr>
      <th>Country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Moldova (MDA)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Nigeria (NGR)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Portugal (POR)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Trinidad and Tobago (TTO)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>United Arab Emirates (UAE)</th>
      <td>78</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>


Calling columns method on the dataframe will print just the column names

```python
df.columns
```




    Index(['Rank', 'Gold', 'Silver', 'Bronze', 'Total'], dtype='object')


To see a quick statistical summary of the your data, you can call describe method.

```python
df.describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Gold</th>
      <th>Silver</th>
      <th>Bronze</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>87.000000</td>
      <td>87.000000</td>
      <td>87.000000</td>
      <td>87.000000</td>
      <td>87.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>43.091954</td>
      <td>3.528736</td>
      <td>3.517241</td>
      <td>4.126437</td>
      <td>11.172414</td>
    </tr>
    <tr>
      <th>std</th>
      <td>24.193326</td>
      <td>6.867245</td>
      <td>5.726036</td>
      <td>6.263227</td>
      <td>18.213340</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>22.500000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>44.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>65.000000</td>
      <td>3.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>11.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>78.000000</td>
      <td>46.000000</td>
      <td>37.000000</td>
      <td>38.000000</td>
      <td>121.000000</td>
    </tr>
  </tbody>
</table>
</div>


To get a single column of data or a subset of data, you need to pass on that column to the dataframe
For example, to print just country names, we will say df and pass Country in square brackets


```python
df['Total']
```




    Country
    United States (USA)           121
    Great Britain (GBR)            67
    China (CHN)                    70
    Russia (RUS)                   55
    Germany (GER)                  42
    Japan (JPN)                    41
    France (FRA)                   42
    South Korea (KOR)              21
    Italy (ITA)                    28
    Australia (AUS)                29
    Netherlands (NED)              19
    Hungary (HUN)                  15
    Brazil (BRA)*                  19
    Spain (ESP)                    17
    Kenya (KEN)                    13
    Jamaica (JAM)                  11
    Croatia (CRO)                  10
    Cuba (CUB)                     11
    New Zealand (NZL)              18
    Canada (CAN)                   22
    Uzbekistan (UZB)               13
    Kazakhstan (KAZ)               17
    Colombia (COL)                  8
    Switzerland (SUI)               7
    Iran (IRI)                      8
    Greece (GRE)                    6
    Argentina (ARG)                 4
    Denmark (DEN)                  15
    Sweden (SWE)                   11
    South Africa (RSA)             10
                                 ... 
    Singapore (SIN)                 1
    Tajikistan (TJK)                1
    Malaysia (MAS)                  5
    Mexico (MEX)                    5
    Algeria (ALG)                   2
    Ireland (IRL)                   2
    Lithuania (LTU)                 4
    Bulgaria (BUL)                  3
    Venezuela (VEN)                 3
    India (IND)                     2
    Mongolia (MGL)                  2
    Burundi (BDI)                   1
    Grenada (GRN)                   1
    Niger (NIG)                     1
    Philippines (PHI)               1
    Qatar (QAT)                     1
    Norway (NOR)                    4
    Egypt (EGY)                     3
    Tunisia (TUN)                   3
    Israel (ISR)                    2
    Austria (AUT)                   1
    Dominican Republic (DOM)        1
    Estonia (EST)                   1
    Finland (FIN)                   1
    Morocco (MAR)                   1
    Moldova (MDA)                   1
    Nigeria (NGR)                   1
    Portugal (POR)                  1
    Trinidad and Tobago (TTO)       1
    United Arab Emirates (UAE)      1
    Name: Total, dtype: int64


To select only a certain rows, you have pass the index of those rows to the dataframe

```python
df[2:6]
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Gold</th>
      <th>Silver</th>
      <th>Bronze</th>
      <th>Total</th>
    </tr>
    <tr>
      <th>Country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>China (CHN)</th>
      <td>3</td>
      <td>26</td>
      <td>18</td>
      <td>26</td>
      <td>70</td>
    </tr>
    <tr>
      <th>Russia (RUS)</th>
      <td>4</td>
      <td>19</td>
      <td>17</td>
      <td>19</td>
      <td>55</td>
    </tr>
    <tr>
      <th>Germany (GER)</th>
      <td>5</td>
      <td>17</td>
      <td>10</td>
      <td>15</td>
      <td>42</td>
    </tr>
    <tr>
      <th>Japan (JPN)</th>
      <td>6</td>
      <td>12</td>
      <td>8</td>
      <td>21</td>
      <td>41</td>
    </tr>
  </tbody>
</table>
</div>


Or if you need to select a particular row where you know the value of certain column

```python
df[df.Rank == 1]
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Gold</th>
      <th>Silver</th>
      <th>Bronze</th>
      <th>Total</th>
    </tr>
    <tr>
      <th>Country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>United States (USA)</th>
      <td>1</td>
      <td>46</td>
      <td>37</td>
      <td>38</td>
      <td>121</td>
    </tr>
  </tbody>
</table>
</div>


Or if you want to get all the data for a particular country, you can call loc method and pass country as parameter.

```python
df.loc['China (CHN)']
```




    Rank       3
    Gold      26
    Silver    18
    Bronze    26
    Total     70
    Name: China (CHN), dtype: int64

## Conclusion
In this article We learned how to import csv data and start exploring it in Python pandas. I have published a whole video course on [Learning Pandas](https://www.packtpub.com/big-data-and-business-intelligence/learning-pandas-video) for Data Analysis, if you want to check it out.


