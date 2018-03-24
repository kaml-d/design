<div style="text-align:right; margin-bottom:50px;" width="90%">
  <a href="motivation">Motivation</a> &#12288;
  &#10143; Use Cases &#12288;
  <a href="https://github.com/kaml-d/design/issues/new">Leave a comment</a>
</div>

## Use Cases

`KAML-D` is mainly useful in the area of collaboratively developing and running cloud native Machine Learning (ML) apps, for example:

- As a *data scientist*, iterate on ML-based features faster and consequently ship them faster. Share models (incl. datasets and parameters) with team colleagues in a simple and intuitive way.
- As a *data engineer* or *developer*, you can benefit from the unified way of handling both datasets and models to more smoothly transition an app to production and interact with your fellow data scientists on the team.
- In an *ops* role, you can get the insights necessary to provide guidance to run the app (incl. the ML features) optimally.

### Faster machine learning iterations

Before an ML feature can be integrated into an app, a data scientist needs to, for example:

1. come up with a model by choosing an approach and algorithm, for example, supervised learning with a [CNN](https://en.wikipedia.org/wiki/Convolutional_neural_network) like the one available in [habrman/FaceRecognition](https://github.com/habrman/FaceRecognition), and
2. figure out how good the model performs using, say, a [cost function](https://towardsdatascience.com/machine-learning-fundamentals-via-linear-regression-41a5d11f5220).

In each of the steps the data scientist might perform many iterations, trying out a number of different approaches and/or using different test and training datasets. With KAML-D, rather than manually creating new versions of datasets and models, you can quickly generate new versions and also go back in time. 

### Ship ML-based features faster

As we've discussed in the [motivation](../motivation), there's a double divide (data scientists/developers/ops) and KAML-D is written with mitigating this in mind. By providing a unified way of handling both datasets and models across different roles, you can expect to more smoothly transition an app to production. With KAML-D, everyone involved can focus on their role while benefiting from a common language and environment, from experimentation to prod.

### Unified handling of datasets and models

Datasets and models are often handled separately, by different people and/or roles and using different methods, from no versioning to purely manual versioning to proprietary methods. With KAML-D, you get a unified way for different roles such as data scientists or developers to handle datasets and models in a unified manner, based on industry-leader [Dotmesh](https://dotmesh.com/).