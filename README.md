# L-system Playground

An L-system, or Lindenmayer system, is a parallel rewriting system and a type of formal grammar used to model the growth of biological organisms. L-systems can also be used to generate space-filling curves and to describe mathematical processes, such as fractals, through the iteration of production rules.

Here are some L-system rules I gathered from various sources. I apologize for missing attributions; some original sources are lost and I need to recover them. Each curve is interactive and can be modified as needed.

```
    F: Move forward by line length drawing a line
    -: Turn left by turning angle
    +: Turn right by turning angle
    A: An axiom
    A => B: A rule
    setting = value: A configuration setting
```

The intentional decision has been made not to support branching, usually represented by `[` and `]` symbols. I acknowledge that these are powerful operations, yet I prefer to implement them as a fork operation, and I didn't explore this space. 
L-system playground
