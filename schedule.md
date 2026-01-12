# Day by day schedule for APPM 4600 Numerical Methods and Scientific Computing

Spring 2026, Instructor: Mark Hoefer (Applied Math dept)

See also the [syllabus](./syllabus.md) for a high-level description

# High-level list of topics
Here's the plan for Spring 2026. Note that things may change slightly,
so see the "Detailed list" below for what we actually covered, which
will be updated during the semester.

[Planned schedule](./APPM%204600%20Spring%202026%20schedule.pdf)

# Detailed list of topics
i.e., what we actually covered.  Topics listed for dates in the future are just estimates,  and will be revised later.

References are to Burden and Faires, 10th edition, unless otherwise noted

#### Week 1, Chapter 1 (preliminaries, floating pt numbers)

- Fri, Jan 9
  - Refs: ch 1.1, 1.2, and other sources.
  - Calc Review and Floating Point Numbers. 
  - Mixed precision computing is being used to speed up computations,
    e.g., on GPUs.  See [Carson, Mary, "Mixed-precision Computing:
    High Accuracy with Low Precision", SIAM News, v 58, Nov 2025](https://www.siam.org/publications/siam-news/articles/mixed-precision-computing-high-accuracy-with-low-precision/).

#### Week 2, Chapter 1 (floating pt numbers, scientific computing)

- Mon, Jan 12
  - Finish Floating Point Numbers
  - Conditioning
  - Refs: mostly from Driscoll and Braun, some ch 1.2. 
  <!-- - Demos: [Ch1_SymbolicTaylorSeries](Demos/Ch1_SymbolicTaylorSeries.ipynb), [Ch1_DataTypes](Demos/Ch1_DataTypes.ipynb), [Ch1_ExponentialSummation](Demos/Ch1_ExponentialSummation.ipynb) -->
- Tue, Jan 13
  - Lab 1
  - Setup Python locally and on cloud
- Wed, Jan 14
  - Debrief from lab
  - Finish Stability and Big-O notation.
  - Demos: <!-- [Ch1_Stability_simple](Demos/Ch1_Stability_simple.ipynb).  -->
  - Optional:
    <!--   [Ch1_Extra_Conditioning](Demos/Ch1_Extra_Conditioning.ipynb) is a -->
    <!-- summary of ch 1 material from Jed Brown's course (didn't cover in -->
    <!-- class) -->
- Fri, Jan 16
  - Rates of convergence, from ch 2.4.
  - Demos: <!-- [Ch1_QuadraticFormula](Demos/Ch1_QuadraticFormula.ipynb), -->
    <!-- [Ch1_RatesOfConvergence](Demos/Ch1_RatesOfConvergence.ipynb) -->

#### Week 3, Chapter 2 (1D root-finding)

- Mon, Jan 19.  No class (Martin Luther King Jr. Day)
- Tues, Jan 20, 
  - Lab 2
- Wed, Jan 21
  - Debrief lab
  - Condition number of a quadratic root-finding problem, and Horner's
    Rule, partly from Driscoll and Braun; and Memory on a computer;
    sparse matrix format; HDF5
- Fri, Jan 23 
  - Finish Memory on a computer; sparse matrix format; HDF5
  - Intro to multivariate calculus
  - Demos: <!-- [Sparse Matrices](Demos/Ch1_SparseMatrices.ipynb) -->

#### Week 4, more Chapter 2 (1D root-finding)

- Mon, Jan 26
  - Finish Intro to multivariate calculus
  - Start Automatic Differentiation
- Tue, Jan 27
  - Lab 3
- Wed, Jan 28 
  - Debrief from lab
  - Finish Automatic Differentiation
  - Discussed computational complexity of multiplying two $n\times n$
    square matrices (and brief mention of Strassen)
  - Demo: <!-- [AutoDiff](Demos/Ch1_AutoDiff.ipynb) with both PyTorch and JAX -->
- Fri, Jan 30
  - Intro to scalar root-finding
  - Intro to scalar optimization
  - Condition number of root-finding

#### Week 5, more Chapter 2 (1D root-finding)
- Mon, Feb 2 
  - multiple roots
  - Bisection Method, from ch 2.1
  - Start Fixed Point Iteration, from ch 2.2.
  - Demo: <!-- [Ch2_IntroToBisection.ipynb](Demos/Ch2_IntroToBisection.ipynb) -->
- Tue, Feb 3
  - Lab 4
- Wed, Feb 4 
  - Debrief lab
  - Finish Fixed Point Iteration, from ch 2.2. Includes convergence
    analysis / contraction-mapping-theorem (aka Banach fixed point
    theorem)
- Fri, Feb 6 
  - Newton's Method, from ch 2.3
  - Newton's Method Variants (secant method, etc.)
  - Demo: <!-- finish [Ch2_IntroToBisection.ipynb](Demos/Ch2_IntroToBisection.ipynb) -->
 <!-- - Demos -->
 <!--    - [Ch2_Intersection_GraphingCalculator.ipynb](Demos/Ch2_Intersection_GraphingCalculator.ipynb) -->
 <!--    - [Ch2_FixedPointPlots.ipynb](Demos/Ch2_FixedPointPlots.ipynb) -->
 <!--      which uses a nice [geogebra online cobweb plotting -->
 <!--      app](https://www.geogebra.org/m/uvsfvNDt) -->
 <!--    - [Ch2_NewtonsMethod.ipynb](Demos/Ch2_NewtonsMethod.ipynb) -->
 <!--    - [HowToCheckYourAnswerUsingExtendedPrecision.ipynb](Demos/HowToCheckYourAnswerUsingExtendedPrecision.ipynb) -->
 <!--      (Python) or -->
 <!--      [HowToCheckYourAnswerUsingExtendedPrecision.m](Demos/HowToCheckYourAnswerUsingExtendedPrecision.m) -->
 <!--      (Matlab) -->
  - Aitken Extrapolation and Zeros of Polynomials and Muller's Method,
    from ch 2.5 and 2.6
    - Demo: <!-- [Ch2_AitkenExtrapolation.ipynb](Demos/Ch2_AitkenExtrapolation.ipynb) -->


#### Week 6, Chapter 10 (nonlinear systems of equations)
- Mon, Feb 9 
  - Ch 10.1, multivariate fixed pt equations and the contraction mapping theorem
- Tue, Feb 10
  - Lab 5
- Wed, Feb 11 
  - Debrief lab
  - Finish example (as in-class exercise, on $g(x)=x+e^{-x}$) from
    Fixed Point Iteration
  - Ch 10.2, Newton's method for systems
  - Demo:
    <!-- [Ch10_NewtonForSystems.ipynb](Demos/Ch10_NewtonForSystems.ipynb) -->
    which also is an example of using JAX for the AutoDiff
- Fri, Feb 13
  - Example of multivariate contraction mapping theorem

#### Week 7, Chapter 10 (nonlinear systems of equations)
- Mon, Feb 16
  - Linear algebra: how to think about matrix multiplication
  - Linear algebra: Sherman-Morrison-Woodbury (as in-class exercise)
  - Start Ch 10.3, Quasi-Newton methods (see 2.3 notes for more
    details on the sectant method, i.e., Newton's Method Variants
    (secant method, etc.))
- Tue, Feb 17
  - Lab 6: multivariate systems of equations and GNSS/GPS
- Wed, Feb 18
  - Debrief lab
  - Finish Ch 10.3, Quasi-Newton methods
  - Optimization problems; Ch 10.4, Steepest-descent (aka
    Gradient-descent), differences/similarities between root-finding
    and optimization; pros-cons of different methods
- Fri, Feb 20 
  - Finish 10.4
  - Non-linear least square, Gauss-Newton, Levenberg-Marquardt

#### Week 8, Chapter 3 (interpolation)
- Mon, Feb 23
  - Intro to Interpolation from ch 3.1
  - Demo: <!-- [Gradient descent vs Newton on nonconvex problem in -->
    <!-- 2D](Demos/Ch10_nonconvex_example_2D.ipynb) -->
- Tue, Feb 24
  - Lab 7
- Wed, Feb 25
  - In-class review
  <!-- - Review: pros and cons of different rootfinding/fixed-pt/optimization methods -->
  <!--   - See the 2025 Midterm 1 template for what the midterm will look like -->
    <!-- - Didn't have time to cover 2025 review of Ch 1 and scientific computing -->
    <!-- - Study material from years past is at [Exams/StudyMaterials](Exams/StudyMaterials), with some solutions on Canvas -->
  - Evening **midterm exam**, TBD
- Fri, Feb 27 
  - Lagrange (and Barycentric) interpolation from ch 3.1
  - "Barycentric Interpolation formula" same notes as before from
    Driscoll and Braun;
    - cf. [Berrut and Trefethen's 2004 SIAM Review
      article](https://people.maths.ox.ac.uk/trefethen/barycentric.pdf);
  - "Lagrange Interpolation Error Bounds" (10 min video; same notes as
    before) ch 3.2;
  - Further resources on Lagrange interpolation:
    - [8 min youtube
      video](https://www.youtube.com/watch?v=_zK_KhHW6og) (nice
      handwriting)
    - [42 min youtube
      video](https://www.youtube.com/watch?v=M8hF7QChkSY) (with
      Vandermonde matrix and divided differences) -- this is a
      standard classroom blackboard lecture from Wen Shen at Penn
      State (textbook author, nice handwriting)
    - [13 min youtube
      video](https://www.youtube.com/watch?v=C1Jijw3VaI0)

#### Week 9, more Chapter 3 (interpolation)
- Mon, Mar 2 
  - Divided Differences from ch 3.3
- Tue, Mar 3
  - Lab 8
- Wed, Mar 4 
  - Debrief lab
  - Interpolation: supplemental notes on how to think about it i.e.,
    different bases, and solving linear systems
  - Demos:
    <!-- [Ch3_PolynomialInterpolation.ipynb](Demos/Ch3_PolynomialInterpolation.ipynb), -->
    which also links to other demos
- Fri, Mar 6 
  - Hermite Interpolation from ch 3.4
  - Intro to Splines from ch 3.5 (we'll skip ch 3.6)
  - Demo: <!-- [splines](Demos/Ch3_Splines.ipynb) -->

#### Week 10, Chapter 8 (approximation theory)
- Mon, Mar 9 
  - Finish Splines
  - Demo: <!-- [Misc_speedExamples](Demos/Misc_speedExamples.ipynb) on -->
    <!-- vectorizing code, avoiding `if` statements in inner `for` loops, -->
    <!-- etc. -->
- Tue, Mar 10
  - Lab 9
- Wed, Mar 11
  - Debrief lab
  - Ch 8.1: discrete l2 and intro to approximation theory
- Fri, Mar 13
  - Start Ch 8.2: continuous L2, up until Chebyshev polynomials

#### Thanksgiving break, no class

#### Week 11, Chapter 4 (numerical integration)
- Mon, Mar 23
  - Finish 8.2
  - Demos: 
    <!-- - [Approximation in L^2](Demos/Ch8_ContinuousL2.ipynb) -->
    <!-- - [Common Python pitfalls](Demos/Misc_CommonPythonPitfalls.ipynb) -->
    <!--   relevant to numerical analysys -->
- Tue, Mar 24
  - Lab 10
- Wed, Mar 25
  - Debrief lab
  - Trigonometric polynomial approximation/interpolation and DFT/FFT
    <!-- - see Supplementary notes on four variations of Fourier operators -->
    <!--   if you're interested (these specific notes will not be on exams) -->
  <!-- - In 2025, we're skipping: -->
  <!--   - ~~8.4, Rational function approximation~~ -->
  <!--       - ~~[The first five years of the AAA algorithm](https://people.maths.ox.ac.uk/trefethen/nak_sete_tref_revised.pdf) by Y. Nakatsukasa, O. Sete, L. N. Trefethen~~ -->
  <!--   - ~~[LOESS and other smoothing techniques](https://en.wikipedia.org/wiki/Local_regression)~~ -->
- Fri, Mar 27 
  - Finish DFT/FFT notes, deriving the FFT and its complexity
  - Start Intro to quadrature
  - Note: 
    - We will **not** cover the first parts of this chapter (on
      *differentiation*), as that is now covered 2nd semester along
      with Ch 5.  For reference, we have some old notes: Intro to
      numerical differentiation and Finite differences on ch 4.1; <!-- with -->
      <!-- a [finite differences demo](Demos/Ch4_FiniteDifferences.ipynb); -->
      <!-- and Richardson extrapolation on ch 4.2 along with the -->
      <!-- [Ch4_RichardsonExtrapolation.ipynb -->
      <!-- demo](Demos/Ch4_RichardsonExtrapolation.ipynb) -->
    - For integration, we are *not* covering Gregory's method; if
      you're interested, see (CU professor) Bengt Fornberg's talk
      [Gregory formulas and improving on the Trapezoidal
      rule](https://www.colorado.edu/amath/sites/default/files/attached-files/2019_unm_0.pdf)

#### Week 12, more Chapter 4 (numerical integration)
- Mon, Mar 30 
  - Finish Intro to quadrature
  - Newton Cotes formula from ch 4.3
  <!-- - If we have time: -->
  <!--   - ~~Romberg integration from ch 4.5~~ -->
  - Demo: <!-- [Ch4_RombergIntegration.ipynb](Demos/Ch4_RombergIntegration.ipynb) -->
- Tue, Mar 31
  - Lab 11
- Wed, Apr 1
  - Debrief lab
  - In-class review
  <!-- - Review_2025_Midterm2.pdf -->
  - Evening **midterm exam**, TBD
- Fri, Apr 3 
  - Finish Newton cotes
  - Demo: <!-- [Ch4_integration.ipynb](Demos/Ch4_integration.ipynb) -->
    <!-- - Look at [Tai's -->
    <!--   method](https://en.wikipedia.org/wiki/Tai%27s_model) which -->
    <!--   reinvented the trapezoidal rule -->

#### Week 13, Chapter 6 (finish integration, start direct methods for linear algebra)
- Mon, Apr 6
  - Composite quadrature from ch 4.4
  - Adaptive integration from ch 4.6
- Tue, Apr 7
  - Lab 12
- Wed, Apr 8 
  - Debrief from lab
  - Demo: <!-- [Ch4_CompositeIntegration.ipynb](Demos/Ch4_CompositeIntegration.ipynb) -->
  <!-- - Demo: [Ch4_AdaptiveIntegration.ipynb](Demos/Ch4_AdaptiveIntegration.ipynb) -->
  - Briefly start Gaussian quadrature from ch 4.7 and also from the
    Driscoll and Braun supplementary text (saving the demo for Friday)
  - Further resources on Gaussian quadrature:
    - a 4 part youtube video series:
          1. [Preview](https://www.youtube.com/watch?v=k-yUdqRXijo)
          2. [Part 1: Legendre
             polynomials](https://www.youtube.com/watch?v=65zwMgGZnUs)
          3. [Part 2: Determining the
             weights](https://www.youtube.com/watch?v=nQZYBWB6q_k)
          4. [Part 3:
             Explanation](https://www.youtube.com/watch?v=cKKrGr93f6c)
    - Lloyd Trefethen, "[Is Gauss Quadrature Better than
      Clenshaw–Curtis?](https://epubs.siam.org/doi/10.1137/060659831)",
      SIAM Review 50(1), pp. 67–87 (2008)
    - Topics in our class: Gauss-Legendre, Gauss-Laguerre,
      Gauss-Hermite; *skip* Chebyshev-Gauss. Note that we are *not*
      covering Clenshaw-Curtis
  <!-- - We didn't have time to cover the following interesting topics -->
  <!--   (though we'll explore multiple dimensions in the lab) -->
  <!--   - ~~Multiple Integrals, from ch 4.8, with demo -->
  <!--     [Ch4_MultidimensionalIntegrals.ipynb](Demos/Ch4_MultidimensionalIntegrals.ipynb)~~ -->
  <!--   - ~~Improper Integrals from ch 4.9, with demo -->
  <!--     [Ch4_ImproperIntegrals.ipynb](Demos/Ch4_ImproperIntegrals.ipynb)~~ -->
- Fri, Apr 10 
  - Finish Gaussian quadrature
    - Demo: <!-- [Ch4_GaussianQuadrature.ipynb](Demos/Ch4_GaussianQuadrature.ipynb) -->
  - Start our last two units on **linear algebra** (ch 6 and ch 9)
    - In chapter 6, we're roughly covering the material from the book,
      but adding more (conditioning, more details on LAPACK/BLAS), and
      doing it in a different order; we're also moving fast, since
      APPM 3310 "Matrix Methods" is a prereq for this class and these
      topics were covered in that class
    - We have a basic Ch6_LinearAlgebraIntro note which is a review of
      some concepts covered in matrix methods. We won't explicitly
      cover this in class, but please review on your own if you feel
      rusty on matrix methods.
  - Complexity of Matrix Multiplication and Systems of Linear
    Equations and Gaussian Elimination; we discuss some BLAS
  - Start LU factorization

#### Week 14, Chapter 9 (Eigenvalues)
- Mon, Apr 13 
  - Finish basic LU factorization from last time, talking about the
    flop count.
  - Do LU factorization details: pivoting, and block factorization,
    and special types of matrices
  - Start Conditioning of solving linear systems
- Tue, Apr 14
  - Lab 13
  <!-- - some day we'll do a lab involving -->
  <!--   [chebfun](https://www.chebfun.org/) (which has to main Python -->
  <!--   offshoots) -->
- Wed, Apr 15
  - Debrief lab
  - Finished conditioning of solving linear systems
  - Least Squares which looks at stability of QR vs normal equations
  - Ch6_QR_and_Householder.pdf
  - Demos:
    <!-- - Short demo on -->
    <!--   [Ch6_Conditioning_solvingEquations.ipynb](Demos/Ch6_Conditioning_solvingEquations.ipynb) -->
    <!-- - Did part of -->
    <!--   [Ch6_LU_vs_Cholesky.ipynb](Demos/Ch6_LU_vs_Cholesky.ipynb) to -->
    <!--   demonstrate why we want to pivot. We didn't cover the rest of -->
    <!--   this demo -->
    <!-- - Did *not* cover ~~[Ch6_conditioning_LeastSquares.ipynb](Demos/Ch6_conditioning_LeastSquares.ipynb) (long!)~~, nor ~~[Ch6_RepeatedSolves.ipynb](Demos/Ch6_RepeatedSolves.ipynb) (short)~~, nor ~~[Ch6_MatrixMultiplication.ipynb](Demos/Ch6_MatrixMultiplication.ipynb), talk about BLAS and LAPACK~~ -->
- Fri, Apr 17 
  <!-- - If you're rusty on eigenvalues and determinants, see all of -->
  <!--   Ch9_EigenvalueBackground.pdf, but we didn't cover all of this -->
  <!--   systematically in class. We focused on just parts of it and an -->
  <!--   in-class exercise to see if we can use the characteristic equation -->
  <!--   to find eigenvalues -->
  - Demo:
    <!-- [Ch9_EigenvaluesTheBadWay.ipynb](Demos/Ch9_EigenvaluesTheBadWay.ipynb), -->
    <!-- though this also has information on how to compute the determinant -->
    <!-- *the good way* -->

#### Week 15, iterative methods (Ch 9, possibly Ch 7)
- Mon, Apr 20 
  - Ch 9.3, Power method
  <!-- - See Ch9_Powermethod_part1.pdf for basic power method -->
- Tue, Apr 21
  - Final review
- Wed, Apr 22 
  - Debrief from lab
  - <!-- Ch9_Powermethod_part2.pdf --> Power method part 2: how to
    accelerate convergence and find more than one eigenvalue (i.e.,
    shift-and-invert, deflation, orthogonal iteration and the QR
    Iteration)
  - Demo: <!-- [Ch 9 power method demo](Demos/Ch9_PowerMethod.ipynb) -->
- Fri, Apr 24 
  - Ch 9.4, Householder reflections, reduction to tridiagonal or upper
    Hessenberg
  - Ch 9.5, QR iteration for eigenvalues
  <!-- - Both these sections are in the notes Ch9_HouseholderHessenberg.pdf -->

#### Final exam
- Wed, Apr 29 
  - 7:30-10 PM Final exam
