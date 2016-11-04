---
layout: post
title: Interpreting PCA results
---
<div class="message">
  After reading up on the theory and application of PCA (principle component analysis) for the last few weeks, I feel that one of the most difficult component of this entire process isn't how to preprocess your data and extract the eigenvectors from your correlation matrix, rather it is everything that comes afterwards. Interpreting PCA requires domain knowledge, but there are tools available to help you along the way.
</div>

## PCA outputs

Let's begin by getting some jargons out of the way. After running your PCA code, you should obtain the following output (standard output from most statistical packages). Imagine we have a $m$ x $n$ matrix, where the rows represent the entities (neurons, proteins, etc.) and the columns represent variables

- **Scores**: (or factor score) projection of your data onto a specific dimension
- **Loadings**: the weight assigned to each variable for a specific dimension (a.k.a the eigenvectors)
    - it is worth noting that *loadings* can have multiple meaning, make sure to read the meaning specified by the author
    - don't worry if you can't find an explanation, you can usual interpret the different meanings in the same way, because they usually only differ by their *type of normalization*
        - loading as *correlation of variables with components*: normalized so the sum of the squared correlations of a *single given* variable is 1. (I will use this definition here)
        - loading as *eigenvectors*: column vectors of the projection matrix (loadings) are normalized such that sum of the squared elements of a given component is 1
- **Eigenvalues**: each eigenvector has a corresponding eigenvalue which represents its variance, this is the variance of the data that results from projecting the original data onto a specific eigenvector
- **Inertia**: this is just a fancy term for the proportion of variance "explained" by a component with respect to all variance in the dataset. Think of this as a reflection of how important a component is.
- **Contribution**: typically referred to the contribution of an observation to a component, the contribution of observation $i$ to component $l$ is:
<p align="center">
$ctr_{i,l} = \frac{f^{2}_{i,l}}{\sum_{i}f^{2}_{i,l}}$

  For example, say you have 200 neurons, each neuron would have a value for this component (think of it has its coordinate when plotted in these dimensions, also called its **factor score**), square the factor score and divide by the eigenvalue (which is the sum o)
</p>
- **Squared cosine**: *squared cosine* shows the importance of a component for a given observation by indicating the cosine of the angle from the right triangle made with the origin
<p align="center">
$\cos^{2}_{i,l} = \frac{f^{2}_{i,l}}{\sum_{l}f^{2}_{i,l}}$

  the denominator is the squared distance of the point to the origin. For each observation, there are $n$ $\cos^{2}$ values corresponding to the $n$ components. The larger the cosine, the more important the component for the given observation.
</p>

### Visualizing PCA results

When you have 20 dimensions, PCA results are a vomit of numbers, a headache to look at and an even bigger pain to make meaning out of. The power of data visualization lies in its ability **to reveal meaningful patterns**. This process is as much of an art as it is a science, so be patient and practice, practice, practice!

Two of the most basic plots are the plot of **observations** and the plot of **variables**.

- observations are represented by their *projections*, where the coordinates for each dimension is the projection of data onto that dimension
    - significance:
- variables are represented by their *correlations*, where the coordinates for each dimension is the correlation of the variable with that dimension
    - significance:

####Plotting correlations of the variables with the component

- recall that the sum of squared correlation/loadings = 1.
- if there are only two components, the two correlations (with the first and second components) of each variable can be used to plot the variable on a cartesian plane and all points would rest on the perimeter of a unit circle
- but you will most likely need more than two components, in which case the variable will be positioned inside the unit circle.
    - the closer a variable is to the perimeter, the more important those components are to explaining variance in that variable

## Clustering gene expression data

Two questions associated with clustering gene expression data are:

- What similarity criterions to use for clustering?
- How to use those criterions to cluster?

In answering the first question, there are two common similarity measures: **Euclidean distance** and **Pearson correlation coefficient**.
- Euclidean distance is sensitive to scaling and difference in average expression






### Code

Cum sociis natoque penatibus et magnis dis `code element` montes, nascetur ridiculus mus.

{% highlight js %}
// Example can be run directly in your JavaScript console

// Create a function that takes two arguments and returns the sum of those arguments
var adder = new Function("a", "b", "return a + b");

// Call the function
adder(2, 6);
// > 8
{% endhighlight %}

Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa.

Aenean eu leo quam. Pellentesque ornare sem lacinia quam venenatis vestibulum. Nullam quis risus eget urna mollis ornare vel eu leo. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec sed odio dui. Vestibulum id ligula porta felis euismod semper.

### Lists

Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.

* Praesent commodo cursus magna, vel scelerisque nisl consectetur et.
* Donec id elit non mi porta gravida at eget metus.
* Nulla vitae elit libero, a pharetra augue.

Donec ullamcorper nulla non metus auctor fringilla. Nulla vitae elit libero, a pharetra augue.

1. Vestibulum id ligula porta felis euismod semper.
2. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
3. Maecenas sed diam eget risus varius blandit sit amet non magna.

Cras mattis consectetur purus sit amet fermentum. Sed posuere consectetur est at lobortis.

<dl>
  <dt>HyperText Markup Language (HTML)</dt>
  <dd>The language used to describe and define the content of a Web page</dd>

  <dt>Cascading Style Sheets (CSS)</dt>
  <dd>Used to describe the appearance of Web content</dd>

  <dt>JavaScript (JS)</dt>
  <dd>The programming language used to build advanced Web sites and applications</dd>
</dl>

Integer posuere erat a ante venenatis dapibus posuere velit aliquet. Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Nullam quis risus eget urna mollis ornare vel eu leo.

### Images

Quisque consequat sapien eget quam rhoncus, sit amet laoreet diam tempus. Aliquam aliquam metus erat, a pulvinar turpis suscipit at.

![placeholder](http://placehold.it/800x400 "Large example image")
![placeholder](http://placehold.it/400x200 "Medium example image")
![placeholder](http://placehold.it/200x200 "Small example image")

### Tables

Aenean lacinia bibendum nulla sed consectetur. Lorem ipsum dolor sit amet, consectetur adipiscing elit.

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Upvotes</th>
      <th>Downvotes</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Totals</td>
      <td>21</td>
      <td>23</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <td>Charlie</td>
      <td>7</td>
      <td>9</td>
    </tr>
  </tbody>
</table>

Nullam id dolor id nibh ultricies vehicula ut id elit. Sed posuere consectetur est at lobortis. Nullam quis risus eget urna mollis ornare vel eu leo.

-----

Want to see something else added? <a href="https://github.com/poole/poole/issues/new">Open an issue.</a>
