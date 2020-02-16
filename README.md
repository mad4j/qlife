# Q Life
Notes and examples regarding Quantum Computing

* [RNG1](#RNG1)
* [RNG4](#RNG4)
* [Entaglement](#Entaglement)

## RNG1
Perfect single-bit random generator.

### Circuit
![PRNG1](prng1.png)


### Code
```
OPENQASM 2.0;
include "qelib1.inc";

qreg q[1];
creg c[1];

h q[0];
measure q[0] -> c[0];
```

### Results
![PRNG1](prng1-results.png)

## RNG4
Perfect 4-bits random generator.

### Circuit
![PRNG4](rng4.png)


### Code
```
OPENQASM 2.0;
include "qelib1.inc";

qreg q[4];
creg c[4];

h q[0];
h q[1];
h q[2];
h q[3];

measure q[0] -> c[0];
measure q[1] -> c[1];
measure q[2] -> c[2];
measure q[3] -> c[3];
```

### Results
![PRNG1](rng4-results.png)


## Entaglement

### Circuit
![Entaglement](entaglement.png)


### Code
```
OPENQASM 2.0;
include "qelib1.inc";

qreg q[2];
creg c[2];

h q[0];
cx q[0],q[1];
measure q[0] -> c[0];
measure q[1] -> c[1];
```

### Results
![Entaglement](entaglement-results.png)


## References
* https://quantum-computing.ibm.com/
