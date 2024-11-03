# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

1. By using the change of base formula, $log_5n$ can be represent as $log_5n=\frac{log_2n}{log_25}=log_2n*\frac{1}{log_25}$, and $log_2n$ can be represent as $log_2n=\frac{log_5n}{log_52}=log_5n*\frac{1}{log_52}$
2. Based on the definition of $O$, assume $c_1=\frac{1}{log_25}$ and $n_0=1$, then $log_5n\leq c_1*log_2n$ for all $n\geq n_0$, therefore, $log_5n\in O(log_2n)$
3. Assum $C_2=\frac{1}{log_52}$ and $n_0=1$, then $log_2n\leq c_2*log_5n$ for all $n\geq n_0$, therefore, $log_2n\in O(log_5n)$
4. Since $log_5n\in O(log_2n)$ and $log_2n\in O(log_5n)$, therefore, $O(\log_{2} n)$ is the same as $O(\log_{5} n)$

“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.” --Doris Yan
