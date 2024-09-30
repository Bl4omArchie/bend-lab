# How to install the massively parallel language Bend 

Bend is a new language with a very interesting specificity: it parallezize every single computation.
With such capability, you don't have no more to worry about locks, mutexes or atomics. 
This language is very similar to python.



# Installation

Install Bend for linux and every dependencies by running [bend_installation.sh](bend_installation.sh)

# Running

Now, try a Hello World program: 
```
def main() -> IO(u24):
  with IO:
    * <- IO/print("Hello, world!\n")
    return wrap(0)
```

And run it:
- bend run    <file.bend> - Uses the C interpreter by default (parallel)
- bend run-rs <file.bend>  - Uses the Rust interpreter (sequential)
- bend run-c  <file.bend> - Uses the C interpreter (parallel)
- bend run-cu <file.bend> - Uses the CUDA interpreter (massively parallel)