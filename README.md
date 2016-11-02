# -computational-method.
In the book 'the Art of Computer Programming' the author Knuth describes the definition of a computational method.
I just started reading this book (volume 1) and I had trouble understanding the style.

Knuth mentions a computational method to be a quadruple (Q,I, Omega, f) -- but I had trouble understanding what each of these is intended to be. 
Knuth's definiton: Let us formally define a computational method to be a Quadruple (Q, I ,Ω, f), in which Q is a set containing subsets I and Ω, and f is a function from Q into itself. Furthermore f should leave Ω pointwise fixed; that if f(q) should equal q for all elements q of Ω. The four quantities Q, I, Ω, f are intended to represent respectively the states of the computation, the input, the output, and the computational rule. Each input x in the set I defines a computational sequence, x0, x1, x2,..., as follows: x0 = x and xk+1 = f(xk) for k>=0. The computational sequence is said to teminate in k steps if k is the smallest integer for which xk is in Ω, and in this case it is said to pr, so is Xk+1, produce the output xk from x,(Note that if xk is in Ω, so is Xk+1, because xk+1 = Xk in such a case.) some computational sequence never terminates in finitely many steps for all x in I.

Here's my explanation (not sure if it's right):

Remember we are defining a 'computational method' and not an algorithm. what is a computational method naively?

a "procedure" that has all characteristics of an algorithm except that it possibly lacks finiteness, may be called a computational method.
simply put the quadruple is the computational method.

Q = {all possible states of computations, I, Ω}
I = {all possible inputs}
Ω = {all possible outputs}
f = computational rule

f is a function from Q into itself.

f: Q  --->  Q
  [I]      [Ω]
f should leave Ω pointwise fixed which means:

f(q) = q, ∀ q ∈ Ω (note it is not any different function but the same computational rule just seperated to Ω)

Now a procedure will have a sequence. And obviously, a computational method must also have a sequence. Hence,

Each input x in the set I defines a computational sequence x0, x1, x2, ..., as follows: x0 = x and xk+1 = f(xk) for k ≥ 0.
How x0 = x? Don't forget the input x is a sequence and so the initial input sequence would be x0. As we are dealing with a sequence, and when we are concerning about 'k' states, the order and the position of elements in the sequence matters. And so, the computational rule f is such that the position or more precise word 'state' of the kth element would be k+1th state. that way, we can seperately apply the function to each new state to get the state that follows.

if xk+1 is not in Ω, then it makes no sense by definition of a function. Hence the wording of Knuth.

The computational sequence is said to terminate in k steps if k is the smallest integer for which xk is in Ω and in this case, it is said to produce the output xk from x.
Thus this is the definition of a computational method. the computational rule f  is an algorithm.
