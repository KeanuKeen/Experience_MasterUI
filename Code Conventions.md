#CONVENTIONS:

#####Order
1. Positioning
2. Box model
3. Typographic
4. Visual

Naming: BEM & Functional
--------------------------

###Functional: Modified
  **o**: Objects

    Structure of the document.
    {Ommitted for BEM usage of block_name-element_name}

  **c**: Components

    Element blocks.
    {Ommitted for BEM usage of block_name-element_name if
    element is adhered only to its Block parent}

  **u**: Utilies

    Margins, alignment, positioning, etc.

  **v**: Visual

    Visual styles of a component.

---

###BEM: Modified

*{Swapped seperators ("-" & " _ ") }*

**Block**


    - Functionally independent, reusable component.
    - "what is it?" -- menu, button
    - A Molecule.

**Element**  

    Part of the block that cannot be seperated from it.
    "what is it?" -- menu item, button text.
    A atom.

**Modifier**  

    Determines the appearance, state or behavior of a block or an element
    "what size?", "what theme?" -- 2rem, limegreen color
    {Ommitted for Functional usage of "v: Visual"}


---

###Container vs. Wrapper


When multiples elements are to be handled specifically and for layout positioning, they'll be contained as a group. Whereas a wrapper is to wrap multiple related containers for seamless user or code identification of a wrapped container.
> You should only wrap containers and not element themselves.

E.G.: *We'll be creating a row for category titles.*

Assuming:
`o-table--skeleton`, `c-table-row`

Category titles table:

`category-cntr`
<br>
    &nbsp;&nbsp;&nbsp;`o-table-skeleton`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`c-row` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`category_row-item` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`category_row-item` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`category_row-item`
