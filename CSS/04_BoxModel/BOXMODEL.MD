# CSS Box Model and Margin Collapse

## 1. CSS Box Model

The **CSS Box Model** describes the rectangular boxes generated for elements in a document. It defines how the size, spacing, and layout of elements are calculated.

Every element in the box model consists of four main components (from the innermost part outward):

1. **Content**  
   - The area where text, images, or other elements appear.  
   - Defined by `width` and `height`.

2. **Padding**  
   - The space between the content and the border.  
   - It is transparent and takes the background color of the element.

3. **Border**  
   - A boundary around the padding.  
   - Controlled using `border-width`, `border-style`, and `border-color`.

4. **Margin**  
   - The outermost space that separates an element from its neighbors.  
   - It is always transparent.

---

### CSS Box Model Diagram

```plaintext
                     Margin
    +---------------------------------------+
    |                                       |
    |            Border                     |
    |   +-------------------------------+   |
    |   |                               |   |
    |   |          Padding              |   |
    |   |   +-----------------------+   |   |
    |   |   |    Content Area       |   |   |
    |   |   +-----------------------+   |   |
    |   |                               |   |
    |   +-------------------------------+   |
    |                                       |
    +---------------------------------------+
```

# Margin Collapse in CSS

Margin collapse occurs when the vertical margins of elements combine into a **single margin** rather than adding up. This behavior simplifies spacing but requires understanding specific scenarios.

---

## When Margins Collapse

**Adjacent Sibling Elements**:  
When two sibling elements have vertical margins, the **larger margin** is applied.

   **Example**:
   ```html
   <div class="box1"></div>
   <div class="box2"></div>
