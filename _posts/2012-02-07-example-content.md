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




- *To italicize text*, use `<em>`.
- Abbreviations, like <abbr title="HyperText Markup Langage">HTML</abbr> should use `<abbr>`, with an optional `title` attribute for the full phrase.
- Citations, like <cite>&mdash; Mark otto</cite>, should use `<cite>`.
- <del>Deleted</del> text should use `<del>` and <ins>inserted</ins> text should use `<ins>`.
- Superscript <sup>text</sup> uses `<sup>` and subscript <sub>text</sub> uses `<sub>`.



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
