

# Foreward
Beginning in the spring of 2000, a series of four one-semester courses were taught at Princeton University whose purpose was to present, in an integrated manner, the core areas of analysis. The objective was to make plain the organic unity that exists between the various parts of the subject, and to illustrate the wide applicability of ideas of analysis to other fields of mathematics and science. The present series of books is an elaboration of the lectures that were given.

While there are a number of excellent texts dealing with individual parts of what we cover, our exposition aims at a different goal: presenting the various sub-areas of analysis not as separate disciplines, but rather as highly interconnected. It is our view that seeing these relations and their resulting synergies will motivate the reader to attain a better understanding of the subject as a whole. With this outcome in mind, we have concentrated on the main ideas and theorems that have shaped the field (sometimes sacrificing a more systematic approach), and we have been sensitive to the historical order in which the logic of the subject developed.

We have organized our exposition into four volumes, each reflecting the material covered in a semester. Their contents may be broadly summarized as follows:

I. Fourier series and integrals.
II. Complex analysis.
III. Measure theory, Lebesgue integration, and Hilbert spaces.
IV. A selection of further topics, including functional analysis, distributions, and elements of probability theory.

However, this listing does not by itself give a complete picture of the many interconnections that are presented, nor of the applications to other branches that are highlighted. To give a few examples: the elements of (finite) Fourier series studied in Book I, which lead to Dirichlet characters, and from there to the infinitude of primes in an arithmetic progression; the X-ray and Radon transforms, which arise in a number of problems in Book I, and reappear in Book III to play an important role in understanding Besicovitch-like sets in two and three dimensions; Fatou’s theorem, which guarantees the existence of boundary values of bounded holomorphic functions in the disc, and whose proof relies on ideas developed in each of the first three books; and the theta function, which first occurs in Book I in the solution of the heat equation, and is then used in Book II to find the number of ways an integer can be represented as the sum of two or four squares, and in the analytic continuation of the zeta function.

A few further words about the books and the courses on which they were based. These courses where given at a rather intensive pace, with 48 lecture-hours a semester. The weekly problem sets played an indispensable part, and as a result exercises and problems have a similarly important role in our books. Each chapter has a series of “Exercises” that are tied directly to the text, and while some are easy, others may require more effort. However, the substantial number of hints that are given should enable the reader to attack most exercises. There are also more involved and challenging “Problems”; the ones that are most difficult, or go beyond the scope of the text, are marked with an asterisk.

Despite the substantial connections that exist between the different volumes, enough overlapping material has been provided so that each of the first three books requires only minimal prerequisites: acquaintance with elementary topics in analysis such as limits, series, differentiable functions, and Riemann integration, together with some exposure to linear algebra. This makes these books accessible to students interested in such diverse disciplines as mathematics, physics, engineering, and finance, at both the undergraduate and graduate level.

It is with great pleasure that we express our appreciation to all who have aided in this enterprise. We are particularly grateful to the students who participated in the four courses. Their continuing interest, enthusiasm, and dedication provided the encouragement that made this project possible. We also wish to thank Adrian Banner and José Luis Rodrigo for their special help in running the courses, and their efforts to see that the students got the most from each class. In addition, Adrian Banner also made valuable suggestions that are incorporated in the text.

FOREWORD ix

We wish also to record a note of special thanks for the following individuals: Charles Fefferman, who taught the first week (successfully launching the whole project!); Paul Hagelstein, who in addition to reading part of the manuscript taught several weeks of one of the courses, and has since taken over the teaching of the second round of the series; and Daniel Levine, who gave valuable help in proof-reading. Last but not least, our thanks go to Gerree Pecht, for her consummate skill in type-setting and for the time and energy she spent in the preparation of all aspects of the lectures, such as transparencies, notes, and the manuscript.

We are also happy to acknowledge our indebtedness for the support we received from the 250th Anniversary Fund of Princeton University, and the National Science Foundation’s VIGRE program.

Elias M. Stein
Rami Shakarchi
Princeton, New Jersey
August 2002

### Preface to Book I

Any effort to present an overall view of analysis must at its start deal with the following questions: Where does one begin? What are the initial subjects to be treated, and in what order are the relevant concepts and basic techniques to be developed?

Our answers to these questions are guided by our view of the centrality of Fourier analysis, both in the role it has played in the development of the subject, and in the fact that its ideas permeate much of the present-day analysis. For these reasons we have devoted this first volume to an exposition of some basic facts about Fourier series, taken together with a study of elements of Fourier transforms and finite Fourier analysis. Starting this way allows one to see rather easily certain applications to other sciences, together with the link to such topics as partial differential equations and number theory. In later volumes several of these connections will be taken up from a more systematic point of view, and the ties that exist with complex analysis, real analysis, Hilbert space theory, and other areas will be explored further.

In the same spirit, we have been mindful not to overburden the beginning student with some of the difficulties that are inherent in the subject: a proper appreciation of the subtleties and technical complications that arise can come only after one has mastered some of the initial ideas involved. This point of view has led us to the following choice of material in the present volume:

•   Fourier series. At this early stage it is not appropriate to introduce measure theory and Lebesgue integration. For this reason our treatment of Fourier series in the first four chapters is carried out in the context of Riemann integrable functions. Even with this restriction, a substantial part of the theory can be developed, detailing convergence and summability; also, a variety of connections with other problems in mathematics can be illustrated.

•   Fourier transform. For the same reasons, instead of undertaking the theory in a general setting, we confine ourselves in Chapters 5 and 6 largely to the framework of test functions. Despite these limitations, we can learn a number of basic and interesting facts about Fourier analysis in R^d and its relation to other areas, including the wave equation and the Radon transform.

•   Finite Fourier analysis. This is an introductory subject par excellence, because limits and integrals are not explicitly present. Nevertheless, the subject has several striking applications, including the proof of the infinitude of primes in arithmetic progression.

Taking into account the introductory nature of this first volume, we have kept the prerequisites to a minimum. Although we suppose some acquaintance with the notion of the Riemann integral, we provide an appendix that contains most of the results about integration needed in the text.

We hope that this approach will facilitate the goal that we have set for ourselves: to inspire the interested reader to learn more about this fascinating subject, and to discover how Fourier analysis affects decisively other parts of mathematics and science.

### Introduction II

In effect, if one extends these functions by allowing complex values for the arguments, then there arises a harmony and regularity which without it would remain hidden.

*B. Riemann, 1851*

When we begin the study of complex analysis we enter a marvelous world, full of wonderful insights. We are tempted to use the adjectives magical, or even miraculous when describing the first theorems we learn; and in pursuing the subject, we continue to be astonished by the elegance and sweep of the results.

The starting point of our study is the idea of extending a function initially given for real values of the argument to one that is defined when the argument is complex. Thus, here the central objects are functions from the complex plane to itself

$$f : \mathbb{C} \to \mathbb{C},$$
or more generally, complex-valued functions defined on open subsets of $\mathbb{C}$. At first, one might object that nothing new is gained from this extension; since any complex number $z$ can be written as $z = x + iy$ where $x, y \in \mathbb{R}$ and $z$ is identified with the point $(x, y)$ in $\mathbb{R}^2$.

However, everything changes drastically if we make a natural, but misleadingly simple-looking assumption on $f$: that it is differentiable in the complex sense. This condition is called **holomorphicity**, and it shapes most of the theory discussed in this book.

A function $f : \mathbb{C} \to \mathbb{C}$ is **holomorphic** at the point $z \in \mathbb{C}$ if the limit

$$\lim_{h \to 0} \frac{f(z+h) - f(z)}{h} \quad (h \in \mathbb{C})$$
exists. This is similar to the definition of differentiability in the case of a real argument, except that we allow $h$ to take *complex* values. The reason this assumption is so far-reaching is that, in fact, it encompasses a multiplicity of conditions: so to speak, one for each angle that $h$ can approach zero.


Although one might now be tempted to prove theorems about holomorphic functions in terms of real variables, the reader will soon discover that complex analysis is a new subject, one which supplies proofs to the theorems that are proper to its own nature. In fact, the proofs of the main properties of holomorphic functions which we discuss in the next chapters are generally very short and quite illuminating.

The study of complex analysis proceeds along two paths that often intersect. In following the first way, we seek to understand the universal characteristics of holomorphic functions, without special regard for specific examples. The second approach is the analysis of some particular functions that have proved to be of great interest in other areas of mathematics. Of course, we cannot go too far along either path without having traveled some way along the other. We shall start our study with some general characteristic properties of holomorphic functions, which are subsumed by three rather miraculous facts:

1.  **CONTOUR INTEGRATION:** If $f$ is holomorphic in $\Omega$, then for appropriate closed paths in $\Omega$

    $$\int_{\gamma} f(z)dz = 0.$$
2.  **REGULARITY:** If $f$ is holomorphic, then $f$ is indefinitely differentiable.
3.  **ANALYTIC CONTINUATION:** If $f$ and $g$ are holomorphic functions in $\Omega$ which are equal in an arbitrarily small disc in $\Omega$, then $f = g$ everywhere in $\Omega$.

These three phenomena and other general properties of holomorphic functions are treated in the beginning chapters of this book. Instead of trying to summarize the contents of the rest of this volume, we mention briefly several other highlights of the subject.

*   The zeta function, which is expressed as an infinite series

    $$\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s},$$
    and is initially defined and holomorphic in the half-plane $\text{Re}(s) > 1$, where the convergence of the sum is guaranteed. This function and its variants (the $L$-series) are central in the theory of prime numbers, and have already appeared in Chapter 8 of Book I, where we proved Dirichlet's theorem. Here we will prove that $\zeta$ extends to a meromorphic function with a pole at $s = 1$. We shall see that the behavior of $\zeta(s)$ for $\text{Re}(s) = 1$ (and in particular that $\zeta$ does not vanish on that line) leads to a proof of the prime number theorem.

*   The theta function

    $$\Theta(z|\tau) = \sum_{n=-\infty}^{\infty} e^{\pi in^2\tau} e^{2\pi inz},$$
    which in fact is a function of the two complex variables $z$ and $\tau$, holomorphic for all $z$, but only for $\tau$ in the half-plane $\text{Im}(\tau) > 0$. On the one hand, when we fix $\tau$, and think of $\Theta$ as a function of $z$, it is closely related to the theory of elliptic (doubly-periodic) functions. On the other hand, when $z$ is fixed, $\Theta$ displays features of a modular function in the upper half-plane. The function $\Theta(z|\tau)$ arose in Book I as a fundamental solution of the heat equation on the circle. It will be used again in the study of the zeta function, as well as in the proof of certain results in combinatorics and number theory given in Chapters 6 and 10.

Two additional noteworthy topics that we treat are: the Fourier transform with its elegant connection to complex analysis via contour integration, and the resulting application of the Poisson summation formula; also conformal mappings, with the mappings of polygons whose inverses are realized by the Schwarz-Christoffel formula, and the particular case of the rectangle, which leads to elliptic integrals and elliptic functions.
Here is the complete transcription of the provided images:
### Introduction III
I turn away in fright and horror from this lamentable plague of functions that do not have derivatives.
  C.Hermite. 1893

Starting in about 1870 a revolutionary change in the conceptual framework of analysis began to take shape, one that ultimately led to a vast transformation and generalization of the understanding of such basic objects as functions, and such notions as continuity, differentiability, and integrability.

The earlier view that the relevant functions in analysis were given by formulas or other “analytic” expressions, that these functions were by their nature continuous (or nearly so), that by necessity such functions had derivatives for most points, and moreover these were integrable by the accepted methods of integration – all of these ideas began to give way under the weight of various examples and problems that arose in the subject, which could not be ignored and required new concepts to be understood. Parallel with these developments came new insights that were at once both more geometric and more abstract: a clearer understanding of the nature of curves, their rectifiability and their extent; also the beginnings of the theory of sets, starting with subsets of the line, the plane, etc., and the “measure” that could be assigned to each.

That is not to say that there was not considerable resistance to the change of point-of-view that these advances required. Paradoxically, some of the leading mathematicians of the time, those who should have been best able to appreciate the new departures, were among the ones who were most skeptical. That the new ideas ultimately won out can be understood in terms of the many questions that could now be addressed. We shall describe here, somewhat imprecisely, several of the most significant such problems.


**1 Fourier series: completion**

Whenever $f$ is a (Riemann) integrable function on $[-\pi, \pi]$ we defined in Book I its Fourier series $f \sim \sum a_n e^{inx}$ by
$$a_n = \frac{1}{2\pi} \int_{-\pi}^{\pi} f(x)e^{-inx} dx,$$
and saw then that one had Parseval’s identity,

$$\sum_{n=-\infty}^{\infty} |a_n|^2 = \frac{1}{2\pi} \int_{-\pi}^{\pi} |f(x)|^2 dx.$$

However, the above relationship between functions and their Fourier coefficients is not completely reciprocal when limited to Riemann integrable functions. Thus if we consider the space $\mathcal{R}$ of such functions with its square norm, and the space $\ell^2(\mathbb{Z})$ with its norm, each element $f$ in $\mathcal{R}$ assigns a corresponding element $\{a_n\}$ in $\ell^2(\mathbb{Z})$, and the two norms are identical. However, it is easy to construct elements in $\ell^2(\mathbb{Z})$ that do not correspond to functions in $\mathcal{R}$. Note also that the space $\ell^2(\mathbb{Z})$ is *complete* in its norm, while $\mathcal{R}$ is not.² Thus we are led to two questions:

(i) What are the putative “functions” $f$ that arise when we complete $\mathcal{R}$? In other words: given an arbitrary sequence $\{a_n\} \in \ell^2(\mathbb{Z})$ what is the nature of the (presumed) function $f$ corresponding to these coefficients?

(ii) How do we integrate such functions $f$ (and in particular verify (1))?

**2 Limits of continuous functions**

Suppose $\{f_n\}$ is a sequence of continuous functions on $[0, 1]$. We assume that $\lim_{n \to \infty} f_n(x) = f(x)$ exists for every $x$, and inquire as to the nature of the limiting function $f$.

If we suppose that the convergence is uniform, matters are straightforward and $f$ is then everywhere continuous. However, once we drop the assumption of uniform convergence, things may change radically and the issues that arise can be quite subtle. An example of this is given by the fact that one can construct a sequence of continuous functions $\{f_n\}$ converging everywhere to $f$ so that

$$\int_0^1 f(x) dx = \lim_{n \to \infty} \int_0^1 f_n(x) dx ?$$

It is with Lebesgue integration that we can solve both this problem and the previous one.

**3 Length of curves**

The study of curves in the plane and the calculation of their lengths are among the first issues dealt with when one learns calculus. Suppose we consider a continuous curve $\Gamma$ in the plane, given parametrically by $\Gamma = \{(x(t), y(t))\}$, $a \le t \le b$, with $x$ and $y$ continuous functions of $t$. We define the *length* of $\Gamma$ in the usual way: as the supremum of the lengths of all polygonal lines joining successively finitely many points of $\Gamma$, taken in order of increasing $t$. We say that $\Gamma$ is *rectifiable* if its length $L$ is finite. When $x(t)$ and $y(t)$ are continuously differentiable we have the well-known formula,
$$L = \int_a^b ((x'(t))^2 + (y'(t))^2)^{1/2} dt.$$

The problems we are led to arise when we consider general curves. More specifically, we can ask:
(i) What are the conditions on the functions $x(t)$ and $y(t)$ that guarantee the rectifiability of $\Gamma$?
(ii) When these are satisfied, does the formula (2) hold?

The first question has a complete answer in terms of the notion of functions of “bounded variation.” As to the second, it turns out that if $x$ and $y$ are of bounded variation, the integral (2) is always meaningful; however, the equality fails in general, but can be restored under appropriate reparametrization of the curve $\Gamma$.

³ The limit $f$ can be highly discontinuous. See, for instance, Exercise 10 in Chapter 1.


There are further issues that arise. Rectifiable curves, because they are endowed with length, are genuinely one-dimensional in nature. Are there (non-rectifiable) curves that are two-dimensional? We shall see that, indeed, there are continuous curves in the plane that fill a square, or more generally have any dimension between 1 and 2, if the notion of fractional dimension is appropriately defined.

**4 Differentiation and integration**

The so-called “fundamental theorem of the calculus” expresses the fact that differentiation and integration are inverse operations, and this can be stated in two different ways, which we abbreviate as follows:

$$F(b) - F(a) = \int_a^b F'(x) dx,$$

$$\frac{d}{dx} \int_0^x f(y) dy = f(x).$$

For the first assertion, the existence of continuous functions $F$ that are nowhere differentiable, or for which $F'(x)$ exists for every $x$, but $F'$ is not integrable, leads to the problem of finding a general class of the $F$ for which (3) is valid. As for (4), the question is to formulate properly and establish this assertion for the general class of integrable functions $f$ that arise in the solution of the first two problems considered above. These questions can be answered with the help of certain “covering” arguments, and the notion of absolute continuity.

**5 The problem of measure**

To put matters clearly, the fundamental issue that must be understood in order to try to answer all the questions raised above is the problem of measure. Stated (imprecisely) in its version in two dimensions, it is the problem of assigning to each subset $E$ of $\mathbb{R}^2$ its two-dimensional measure $m_2(E)$, that is, its “area,” extending the standard notion defined for elementary sets. Let us instead state more precisely the analogous problem in one dimension, that of constructing one-dimensional measure $m_1 = m$, which generalizes the notion of length in $\mathbb{R}$.

We are looking for a non-negative function $m$ defined on the family of subsets $E$ of $\mathbb{R}$ that we allow to be extended-valued, that is, to take on the value $+\infty$. We require:

5. The problem of measure
(a) $m(E) = b - a$ if $E$ is the interval $[a, b]$, $a \le b$, of length $b - a$.
(b) $m(E) = \sum_{n=1}^{\infty} m(E_n)$ whenever $E = \bigcup_{n=1}^{\infty} E_n$ and the sets $E_n$ are disjoint.

Condition (b) is the “countable additivity” of the measure $m$. It implies the special case:
(b') $m(E_1 \cup E_2) = m(E_1) + m(E_2)$ if $E_1$ and $E_2$ are disjoint.

However, to apply the many limiting arguments that arise in the theory the general case (b) is indispensable, and (b') by itself would definitely be inadequate.

To the axioms (a) and (b) one adds the translation-invariance of $m$, namely
(c) $m(E+h) = m(E)$, for every $h \in \mathbb{R}$.

A basic result of the theory is the existence (and uniqueness) of such a measure, Lebesgue measure, when one limits oneself to a class of reasonable sets, those which are “measurable.” This class of sets is closed under countable unions, intersections, and complements, and contains the open sets, the closed sets, and so forth.⁴

It is with the construction of this measure that we begin our study. From it will flow the general theory of integration, and in particular the solutions of the problems discussed above.

**A chronology**

We conclude this introduction by listing some of the signal events that marked the early development of the subject.
1872 – Weierstrass’s construction of a nowhere differentiable function.
1881 – Introduction of functions of bounded variation by Jordan and later (1887) connection with rectifiability.
1883 – Cantor’s ternary set.
1890 – Construction of a space-filling curve by Peano.
1898 – Borel’s measurable sets.
1902 – Lebesgue’s theory of measure and integration.
1905 – Construction of non-measurable sets by Vitali.
1906 – Fatou’s application of Lebesgue theory to complex analysis.

⁴ There is no such measure on the class of all subsets, since there exist non-measurable sets. See the construction of such a set at the end of Section 3, Chapter 1.
