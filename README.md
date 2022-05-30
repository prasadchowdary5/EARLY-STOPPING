Early stopping requires that you configure your network to be under constrained, meaning that it has more capacity than is required for the problem. When training the network, a larger number of training epochs is used than may normally be required, to give the network plenty of opportunity to fit, then begin to overfit the training dataset.
These early stopping rules work by splitting the original training set into a new training set and a validation set. The error on the validation set is used as a proxy for the generalization error in determining when overfitting has begun. These methods are most commonly employed in the training of neural networks.Overfitting
Main article: Overfitting

This image represents the problem of overfitting in machine learning. The red dots represent training set data. The green line represents the true functional relationship, while the blue line shows the learned function, which has fallen victim to overfitting.
Machine learning algorithms train a model based on a finite set of training data. During this training, the model is evaluated based on how well it predicts the observations contained in the training set. In general, however, the goal of a machine learning scheme is to produce a model that generalizes, that is, that predicts previously unseen observations. Overfitting occurs when a model fits the data in the training set well, while incurring larger generalization error.

Regularization
Main article: Regularization (mathematics)
Regularization, in the context of machine learning, refers to the process of modifying a learning algorithm so as to prevent overfitting. This generally involves imposing some sort of smoothness constraint on the learned model.[1] This smoothness may be enforced explicitly, by fixing the number of parameters in the model, or by augmenting the cost function as in Tikhonov regularization. Tikhonov regularization, along with principal component regression and many other regularization schemes, fall under the umbrella of spectral regularization, regularization characterized by the application of a filter. Early stopping also belongs to this class of methods.

Gradient descent methods
Main article: Gradient descent
Gradient descent methods are first-order, iterative, optimization methods. Each iteration updates an approximate solution to the optimization problem by taking a step in the direction of the negative of the gradient of the objective function. By choosing the step-size appropriately, such a method can be made to converge to a local minimum of the objective function. Gradient descent is used in machine-learning by defining a loss function that reflects the error of the learner on the training set and then minimizing that function.

Early stopping based on analytical results
Early stopping in statistical learning theory
Early-stopping can be used to regularize non-parametric regression problems encountered in machine learning. For a given input space, {\displaystyle X}X, output space, {\displaystyle Y}Y, and samples drawn from an unknown probability measure, {\displaystyle \rho }\rho , on {\displaystyle Z=X\times Y}Z = X \times Y, the goal of such problems is to approximate a regression function, {\displaystyle f_{\rho }}f_{{\rho }}, given by

We want to control the difference between the expected risk of the sample iteration and the minimum expected risk, that is, the expected risk of the regression function:

This difference can be rewritten as the sum of two terms: the difference in expected risk between the sample and population iterations and that between the population iteration and the regression function:

This equation presents a bias-variance tradeoff, which is then solved to give an optimal stopping rule that may depend on the unknown probability distribution. That rule has associated probabilistic bounds on the generalization error. For the analysis leading to the early stopping rule and bounds, the reader is referred to the original article.[3] In practice, data-driven methods, e.g. cross-validation can be used to obtain an adaptive stopping rule.

Early stopping in boosting
Boosting refers to a family of algorithms in which a set of weak learners (learners that are only slightly correlated with the true process) are combined to produce a strong learner. It has been shown, for several boosting algorithms (including AdaBoost), that regularization via early stopping can provide guarantees of consistency, that is, that the result of the algorithm approaches the true solution as the number of samples goes to infinity.[5] [6] [7]

L2-boosting
Boosting methods have close ties to the gradient descent methods described above can be regarded as a boosting method based on the {\displaystyle L_{2}}L_{2} loss: L2Boost.
