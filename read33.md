# JSON Web Token
JWT stand for JSON Web Token and it is an authentication strategy used by client/server applications where the client is a Web application using JavaScript and some frontend framework like Angular, React or VueJS.
  
- A JSON Web Token looks like this (newlines inserted for readability):
```eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.
eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWV9.
TJVA95OrM7E2cBab30RMHrHDcEfxjoYZgeFONFh7HgQ

```
- While this looks like gibberish, it is actually a very compact, printable representation of a series
of claims, along with a signature to verify its authenticity

- Claims are definitions or assertions made about a certain party or object. Some of these claims
and their meaning are defined as part of the JWT spec. Others are user defined. The magic
behind JWTs is that they standardize certain claims that are useful in the context of some common
operations 
## What problem does it solve?
- Although the main purpose of JWTs is to transfer claims between two parties, arguably the most
important aspect of this is the standardization effort in the form of a simple, optionally validated
and/or encrypted, container format. Ad hoc solutions to this same problem have been implemented
both privately and publicly in the past. Older standards8
for establishing claims about certain
parties are also available. What JWT brings to the table is a simple, useful, standard container
format.

- practical applications
    - • Authentication
    - • Authorization
    - • Federated identity
    - • Client-side sessions (“stateless” sessions)
    - • Client-side secrets