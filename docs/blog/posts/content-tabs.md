---
date: 
  created: 2025-05-29
  update: 2025-05-30
authors: [jianyu]
description: >
  This is a blog demo.
categories:
  - Quantum Computing
pin: true
comments: true
---
## Content Tabs

This is some examples of content tabs.

[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) is the ultimate framework for creating stunning, interactive documentation sites. In this tutorial, we’ll be creating a new documentation portal completely from scratch, and then hosting that on the web for free using [GitHub pages](https://pages.github.com/).

<!-- more -->


Along the way, you'll learn just a handful of the awesome features that Material for MkDocs comes bundled with, such as:

- Setting a **dynamic colour scheme**
- Adding a splash of personality with **emojis**, **icons** and **logos** to make your content visually appealing
- How to create **custom code blocks** that adjust based on the programming language specified
- How to better organise your documentation using **content tabs**
- How to empathize parts of your content using **admonitions** - also known as *callouts*
- And how to bring your ideas to life with **statically rendered diagrams** directly in your docs

???+ tip 

    This is an in-depth tutorial. If this is your first time using Material for MkDocs then you're probably best to just follow it all through from the beginning.

### Generic Content

=== "Plain text"

    This is some plain text

=== "Unordered list"

    * First item
    * Second item
    * Third item

=== "Ordered list"

    1. First item
    2. Second item
    3. Third item





### Code Blocks in Content Tabs

=== "Python"

    ```py
    def main():
        print("Hello world!")
    
    if __name__ == "__main__":
        main()
    ```
    
    There are some explanation about the codes above.

=== "JavaScript"

    ```js
    function main() {
        console.log("Hello world!");
    }
    
    main();
    ```

### Admonitions (aka Callouts)

!!! note "Note"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.


!!! warning "Warning"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

!!! tip "Tip"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

!!! question "Question"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.


Collapsible callout:

??? info "Collapsible callout"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

more examples of admonitions check [official references](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#supported-types).

equations:

$$
\cos x=\sum_{k=0}^{\infty}\frac{(-1)^k}{(2k)!}x^{2k}
$$

