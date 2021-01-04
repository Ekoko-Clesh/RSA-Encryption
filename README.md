# RSA-Encryption

The implementation of RSA makes heavy use of modular arithmetic, Euler's theorem, and Euler's totient function. Notice that each step of the algorithm only involves multiplication, so it is easy for a computer to perform:

First, the receiver chooses two large prime numbers pp and qq. Their product, n=pqn=pq, will be half of the public key.
The receiver calculates \phi(pq)=(p-1)(q-1)ϕ(pq)=(p−1)(q−1) and chooses a number ee relatively prime to \phi(pq)ϕ(pq). In practice, ee is often chosen to be 2^{16}+1=655372 
16
 +1=65537, though it can be as small as 33 in some cases. ee will be the other half of the public key.
The receiver calculates the modular inverse dd of ee modulo \phi(n)ϕ(n). In other words, de \equiv 1 \pmod{{\small\phi(n)}}de≡1(modϕ(n)). dd is the private key.
The receiver distributes both parts of the public key: nn and ee. dd is kept secret.



