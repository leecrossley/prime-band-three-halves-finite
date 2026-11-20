# The three-halves prime deficit through 100,000

Set $b=3/2$. For every real $0<y\le100{,}000$, $D_b(y)>0$. This is an unconditional finite-range result.

Let $W_b(t)$ equal $b(1-1/t)$ for $1<t\le b$, $b^2/t-1$ for $b<t<b^2$, and zero elsewhere. Define $P_b(y)=\sum_{p\ {\rm prime}}(\log p)W_b(p/y)$ for $y>0$, with natural logarithms. Its expected main term is $b(b-1)y\log b$. Write $B_b=2\sqrt b(\sqrt b-1)^2$ for the asymptotic prime-square contribution, $D_b(y)=b(b-1)y\log b-P_b(y)$ for the deficit and $H_b(s)=(b^s-1)(b^s-b)/(s(s-1))$ for the Mellin transform.

Write $b=a/c$ with $a=3$ and $c=2$, and put $u=a^2y=9y$. For a prime $p$ the continuous weight $W_b(p/y)$ changes slope only at $c^2p$, $acp$ and $a^2p$ in $u$. Its slope changes, after multiplying the weight by $ac^2$, are respectively $a/p$, $-(a+c)/p$ and $c/p$. An integer sieve through $225{,}000$ includes every contributing prime. Coefficients $(\log p)/p$ are rounded upwards with rational log enclosures, before applying the nonnegative tent. The main slope uses a lower enclosure of $(a-c)\log(a/c)$ with the same fixed-point scale. Prefix summation evaluates these affine bounds at every integer $1\le u\le900{,}000$.

Each endpoint upper bound for the prime sum is strictly below the endpoint lower bound for the main term. Both bounds are affine between successive integers. At $u=0$ both vanish, so the strict inequality at $u=1$ covers the first open interval as well. The full assertion follows by interpolation.

## Verification

The executable checks all 900,000 positive endpoints, using integer and rational arithmetic. This covers every real scale in the stated interval.

The recorded run used Python 3.9.6 on arm64 macOS. The verifier requires Python 3.9 or later and uses only the standard library.

```sh
bash verify-release.sh
```

The command checks the release manifest, reruns the arithmetic, and compares its output with the recorded result.

[Recorded verification output](evidence/check.txt) · [SHA-256 manifest](SHA256SUMS) · [Tagged publication](https://github.com/leecrossley/prime-band-three-halves-finite/releases/tag/v1.0.0)

## Related result

[Conditional oscillation at the same dilation](https://github.com/leecrossley/prime-band-three-halves-oscillation/tree/v1.0.0)
