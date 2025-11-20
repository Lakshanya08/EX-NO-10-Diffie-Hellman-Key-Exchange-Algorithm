# EX-NO-10-Diffie-Hellman-Key-Exchange-Algorithm

## AIM:
To Implement Diffie Hellman Key Exchange Algorithm 

## Algorithm:

1. Diffie-Hellman Key Exchange is used for securely sharing a secret key between two parties over an insecure channel.

2. Initialization: Agree on a large prime number \( p \) and a primitive root \( g \) modulo \( p \) (both are public values).

3. Key Exchange Process: 
   - Each party selects a private key and calculates their public key using the formula \( g^{\text{private key}} \mod p \).
   - Each party then shares their public key with the other.

4. Secret Key Computation: 
   - Each party computes the shared secret key using the received public key and their own private key.

5. Security: The difficulty of computing discrete logarithms ensures that the shared key remains secure even if public values are intercepted.

## Program:
```
p = 23   
g = 5  
print("Publicly Shared Values:")
print("Prime (p) =", p)
print("Base  (g) =", g)
a = 6  
b = 15   
A = pow(g, a, p)   
B = pow(g, b, p)   

print("\nPublic Keys Exchanged:")
print("Alice sends A =", A)
print("Bob sends B =", B)
secret_key_alice = pow(B, a, p)
secret_key_bob   = pow(A, b, p)

print("\nSecret Key Computed:")
print("Secret Key (Alice) =", secret_key_alice)
print("Secret Key (Bob)   =", secret_key_bob)
```
## Output:
<img width="577" height="262" alt="image" src="https://github.com/user-attachments/assets/a90a061e-c1c9-40b1-9b2a-751f98c4d431" />

## Result:
The program is executed successfully

