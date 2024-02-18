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

## How to

This is a single-file static website that implements an L-system fractal as a web component. CodeMirror is used as an external dependency for a code editor. To use the website, open `index.html` in a browser.

Web Component example:

```
    <web-fractal
        data-name="H-indexing"
        data-creator="oneearedrabbit"
        data-creation-date="2024-02-12"
        data-description="A new two-dimensional (2-D) indexing scheme called H-indexing, which has superior (possibly optimal) locality in comparison with the well-known Hilbert indexings. H-indexings form a Hamiltonian cycle and we prove that they are optimally locality-preserving among all cyclic indexings."
    >
        order = 4
        angle = 90

        A => BF-F-BFFFC-F-FC+F+BF-F-BFFFC-F-FC
        B => BFFFC-F-FC+F+B
        C => C+F+BF-F-BFFFC
    </web-fractal>
```

## Screenshot

![image](https://github.com/oneearedrabbit/l-sys-playground/assets/198995/6d4809fd-9e81-4004-a8c7-f5182cd9dd65)
