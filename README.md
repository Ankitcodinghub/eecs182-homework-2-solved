# eecs182-homework-2-solved
**TO GET THIS SOLUTION VISIT:** [EECS182 Homework 2 Solved](https://www.ankitcodinghub.com/product/eecs182-solved-14/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;116541&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EECS182 Homework 2  Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
1. Why Learning Rates Cannot be Too Big

To understand the role of the learning rate, it is useful to understand it in the context of the simplest possible problem first.

Suppose that we want to solve the scalar equation

σw = y (1)

where we know that σ &gt; 0. We proceed with an initial condition w0 = 0 by using gradient descent to minimize the squared loss

L(w) = (y − σw)2 (2)

which has a derivative with respect to the parameter w of −2σ(y − σw).

Gradient descent with a learning rate of η follows the recurrence-relation or discrete-time state evolution of:

wt+1 = wt + 2ησ(y − σwt)

= (1 − 2ησ2)wt + 2ησy. (3)

(a) For what values of learning rate η &gt; 0 is the recurrence (3) stable?

(HINT: Remember the role of the unit circle in determining the stability or instability of such recurrences. If you keep taking higher and higher positive integer powers of a number, what does that number has to be like for this to converge?)

(b) The previous part gives you an upper bound for the learning rate η that depends on σ beyond which we cannot safely go. If η is below that upper bound, how fast does wt converge to its final solution

? i.e. if we wanted to get within a factor (1 − ϵ) of w∗, how many iterations t would we need?’=

(HINT: The absolute value of the error of current w to the optimality might help.)

(c) Suppose that we now have a vector problem where we have two parameters w[1],w[2]. One with a large σℓ and the other with a tiny σs. i.e. σℓ ≫ σs and we have the vector equation we want to solve:

. (4)

We use gradient descent with a single learning rate η to solve this problem starting from an initial condition of w = 0.

For what learning rates η &gt; 0 will we converge? Which of the two σi is limiting our learning rate?

(d) For the previous problem, depending on η,σℓ,σs, which of the two dimensions is converging faster and which is converging slower?

(e) The speed of convergence overall will be dominated by the slower of the two. For what value of η will we get the fastest overall convergence to the solution?

(f) Comment on what would happen if we had more parallel problems with σi that all were in between σℓ and σs? Would they influence the choice of possible learning rates or the learning rate with the fastest convergence?

(g) Using what you know about the SVD, how is the simple scalar and parallel scalar problem analysis above relevant to solving general least-squares problems of the form Xw ≈ y using gradient descent?

2. Accelerating Gradient Descent with Momentum

Consider the problem of finding the minimizer of the following objective:

(5)

In the previous homework, we proved that gradient descent (GD) algorithm can converge and derive the convergence rate. In this homework, we will add the momentum term and how it affects to the convergence rate. The optimization procedure of gradient descent+momentum is given below:

wt+1 = wt − ηzt+1

zt+1 = (1 − β)zt + βgt, (6)

where gt = ∇L(wt), η is learning rate and β defines how much averaging we want for the gradient. Note that when β = 1, the above procedure is just the original gradient descent.

Let’s investigate the effect of this change. We’ll see that this modification can actually ’accelerate’ the convergence by allowing larger learning rates.

(a) Recall that the gradient descent update of 5 is

(7)

and the minimizer is

w∗ = (XTX)−1XTy (8)

The geometric convergence rate (in the sense of what base is there for convergence as ratet) of this procedure is

rate = max|1 − 2ησi2| (9)

i

You saw on the last homework that if we choose the learning rate that maximizes Eq. 9, the optimal learning rate, η∗ is

, (10)

where σmax and σmin are the maximum and minimum singular value of the matrix X. The corresponding optimal convergence rate is

optimal rate (11)

Therefore, how fast ordinary gradient descent converges is determined by the ratio between the maximum singular value and the minimum singular value as above.

Now, let’s consider using momentum to smooth the gradients before taking a step in Eq.6.

wt+1 = wt − ηzt+1

zt+1 = (1 − β)zt + β(2XTXwt − 2XTy) (12)

We can use the SVD of the matrix X = UΣV T, where Σ = diag(σmax,σ2,…,σmin) with the same (potentially rectangular) shape as X. This allows us to reparameterize the parameters wt and averaged gradients zt as below:

xt = V T(wt − w∗)

at = V Tzt. (13)

Please rewrite Eq. 12 with the reparameterized variables, xt[i] and at[i]. (xt[i] and at[i] are i-th components of xt and at respectively.)

(b) Notice that the above 2 × 2 vector/matrix recurrence has no external input. We can derive the 2 × 2 system matrix Ri from above such that

(14)

Derive Ri.

(c) Use the computer to symbolically find the eigenvalues of the matrix Ri.

When are they purely real? When are they repeated and purely real? When are they complex?

(d) For the case when they are repeated, what is the condition on η,β,σi that keeps them stable (strictly inside the unit circle)? What is the highest learning rate η as a function of β and σi that results in repeated eigenvalues?

(e) For the case when the eigenvalues are real, what is the condition on η,β,σi that keeps them stable (strictly inside the unit circle)? What is the upper bound of learning rate? Express with β,σi

(f) For the case when the eigenvalues are complex, what is the condition on η,β,σi that keeps them stable (strictly inside the unit circle)? What is the highest learning rate η as a function of β and σi that results in complex eigenvalues?

(g) Now, apply what you have learned to the following problem. Assume that β = 0.1 and we have a problem with two singular values and . What learning rate η should we choose to get the fastest convergence for gradient descent with momentum? Compare how many iterations it will take to get within 99.9% of the optimal solution (starting at 0) using this learning rate and momentum with what it would take using ordinary gradient descent.

(h) The 2 questions below are based on the Jupyter Notebook given in this url. Please open the corresponding notebook and follow the instructions to answer the following questions. You don’t need to submit the ipynb file.

How does σi (the eigenvalues) influence the gradients and paramters updates?

(i) Question: Comparing gradient descent and gradient descent with momentums, which one converges faster for this task? Why?

3. Regularization and Instance Noise

Say we have m labeled data points , where each xi ∈ Rn and each yi ∈ R. We perform data augmentation by adding some noise to each vector every time we use it in SGD. This means for all points i, we have a true input xi and add noise Ni to get the effective random input seen by SGD:

Xˇi = xi + Ni

The i.i.d. random noise vectors Ni are distributed as Ni ∼ N(0,σ2In).

We can conceptually arrange these noise-augmented data points into a random matrix Xˇ ∈ Rm×n, where row Xˇ⊤i represents one augmented datapoint. Similarly we arrange the labels yi into a vector y.

  y1

Xˇ = Xˇ⊤2  ˇ ∈ Rn , and y y2 m

, where Xi

 …  ˇ⊤ Xm

One way of thinking about what SGD might do is to consider learning weights that minimize the expected least squares objective for the noisy data matrix:

argminE[∥Xˇw − y∥2] w

(a) Show that this problem (15) is equivalent to a regularized least squares problem: (15)

argmin(16) w

You will need to determine the value of λ.

Hint: write the squared norm of a vector as an inner product, expand, and apply linearity of expectation.

Now consider a simplified example where we only have a single scalar datapoint x ∈ R and its corresponding label y ∈ R. We are going to analyze this in the context of gradient descent. For the t-th step of gradient descent, we use a noisy datapoint Xˇt = x + Nt which is generated by adding different random noise values Nt ∼ N(0,σ2) to our underlying data point x. The noise values for each iteration of gradient descent are i.i.d. We want to learn a weight w such that the squared-loss function is minimized. We initialize our weight to be w0 = 0.

(b) Let wt be the weight learned after the t-th iteration of gradient descent with data augmentation. Write the gradient descent recurrence relation between E[wt+1] and E[wt] in terms of x, σ2, y, and learning rate η.

(c) For what values of learning rate η do we expect the expectation of the learned weight to converge using gradient descent?

(d) Assuming that we are in the range of η for which gradient-descent converges, what would we expect E[wt] to converge to as t → ∞? How does this differ from the optimal value of w if there were no noise being used to augment the data?

(HINT: You can also use this to help check your work for part (a).)

4. An Alternate MAP Interpretation of Ridge Regression

Consider the Ridge Regression estimator,

argmin w

We know this is solved by

wˆ = (XTX + λI)−1XTy (17)

An alternate form of the Ridge Regression solution (often called the Kernel Ridge form) is given by

wˆ = XT(XXT + λI)−1y. (18)

We know that Ridge Regression can be viewed as finding the MAP estimate when we apply a prior on the (now viewed as random parameters) W. In particular, we can think of the prior for√ W as being N(0,I)

and view the random Y as being generated using Y = xTW + λN where the noise√ N is distributed iid

(across training samples) as N(0,1). At the vector level, we have Y = XW + λN, and then we know that when we try to maximize the log likelihood we end up minimizing

argmin = argmin . w λ w

The underlying probability space is that defined by the d iid standard normals that define the W and the n iid standard normals that give the n different Ni on the training points. Note that the X matrix whose rows consist of the n different inputs for the n different training points are not random.

Based on what we know about joint normality, it is clear that the random Gaussian vectors W and Y are jointly normal. Use the following facts to show that the two forms of solution are identical.

• (17) is the MAP estimate for W given an observation Y = y (We showed this in HW1 last week, and in discussion section)

• For jointly normal random variables, when you condition one set of variables on the values for the others, the resulting conditional distribution is still normal.

• A normal random variable has its density maximized at its mean.

• For jointly normal random vectors that are zero mean, the formula for conditional expectation is

E[W|Y = y] = ΣWY Σ−YY1 y (19)

where the ΣYY is the covariance E[YYT] of Y and ΣWY = E[WYT] is the appropriate crosscovariance of W and Y.

5. Coding Question: Initialization and Optimizers

In this question, you’ll implement He Initialization and Different Optimizers. You will have the choice between two options:

Use Google Colab (Recommended). Open this url and follow the instructions in the notebook.

For this question, please submit a .zip file your completed work to the Gradescope assignment titled “HW 2 (Code)”.

For this question, please submit a .zip file your completed work to the Gradescope assignment titled “Homework 2 (Code)”. Please answer the following question in your submission of the written assignment:

(a) What you observe in the mean of gradient norm plot above in the above plots? Try to give an explanation.

6. Visualizing Features from Local Linearization of Neural Nets (Part II)

This question is a sequel to the question about local linearization of the network in the neighborhood of the parameters. In this part, We will now compare shallow and deep networks, examine the effects of different initialization strategies, and investigate the consequences of training a neural network on a mismatched training data distribution.

We provide you with some starter code on Google Colab. For this question, please do not submit your code to Gradescope. Instead, just include the answers to the questions in your submission of the written assignment.

(a) What are the gradient norms of each layer when the init weight scale is small (-0.03 to 0.03)?

(b) Describe the performance of the model initialized with the small weight scale.

(c) Record and explain your observation of the singular values and principal features of the local linearization gradient matrix of the model initialized with the small weight scale before and after training.

(d) What are the gradient norms of each layer when the init weight scale is large (-3.0 to 3.0)?

(e) What happened when we try to train the model initialized with the large weight scale?

(f) What are the gradient norms of each layer when the neural network is initialize with your implemented method?

(g) Based on your observation of the singular values and principal features of the local linearization gradient matrix, compare the properly-initialized neural network with the neural network initialized with a very large weight scale. (before training)

(h) Describe the performance of the model initialized with your implemented method.

(i) Based on your observation of the singular values and principal features of the local linearization gradient matrix, compare the trained shallow neural network (1 hidden layer) with the trained deep neural network (4 hidden layers).

(j) Describe the performance of the model when the x values of training data range from -1.0 to 0.4

(k) Based on your observation of the singular values and principal features of the local linearization gradient matrix, compare the model trained with mismatched training data with models (both shallow and deep model) trained with matched training data.

7. Homework Process and Study Group

We also want to understand what resources you find helpful and how much time homework is taking, so we can change things in the future if possible.

(a) What sources (if any) did you use as you worked through the homework?

(b) If you worked with someone on this homework, who did you work with?

List names and student ID’s. (In case of homework party, you can also just describe the group.)

(c) Roughly how many total hours did you work on this homework? Write it down here where you’ll need to remember it for the self-grade form.

Contributors:

• Anant Sahai.

• Sheng Shen.

• Suhong Moon.

• Gabriel Goh.

• Peter Wang.

• Saagar Sanghavi.

• Hao Liu.

• Andrew Ng.

• Linyuan Gong.
