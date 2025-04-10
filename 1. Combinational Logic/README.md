## 1. Combinational Logic

### 1.1. Digital Logic

- Digital logic is a subfield of electronics where voltages are interpreted as either 1 or 0, and the output information is also 1's or 0's.
- There are two broad types of digital logic:
    1. **Functions:**  
       $$ f(x_0, x_1, x_2) $$
       - Digital functions are stateless (i.e., the current output depends only on the current inputs, meaning the output is not a function of time).
    2. **Storage:**  
       $$ Q(t) = f(Q(t-1), x(t)) $$
       - The current output depends on past inputs.

### 1.2. Digital Functions

- A digital function is a mapping from \( \mathbb{B} \rightarrow \mathbb{B} \), which can be expressed using Boolean algebra:
    - \( \mathbb{B} = \{ 0, 1 \} \).
    - Operations are:
        1. \( a \mid b \) (logical OR),
        2. \( \neg a \) (logical NOT),
        3. \( a \land b \) (logical AND).
- Digital functions can be represented graphically as truth tables.
- We can reduce all high-level operations to combinations of simple logical operations (like AND, OR, NOT, XOR), a process known as logical reduction.
- These gates actually perform specific tasks! All high-level algorithms must be broken down into these fundamental functions. For example:
    1. If 0 and 1 are numbers, XOR performs base-2 addition.
    2. If 0 represents positive and 1 represents negative, XOR determines the sign of multiplication.
    3. XOR represents the if/else check (if A equals 1, then the output is not B; otherwise, the output is B).
    4. XOR checks if A is not equal to B.
    5. And many more.
- In general, there are \( 2^{2^n} \) possible \( n \)-bit digital functions.
- In practice, we aim to find a digital function that describes the desired logical behavior. One way to specify a digital function in algebraic form is through sum-of-products:
    1. Create the truth table.
    2. Write each row where the output is 1 as a product of inputs (using AND).
    3. Combine them as a sum (using OR) to get the final expression.
    - Example:  
    ![SOP Example](../_img/sop.png)  
    Then, $$ f(x, y, z) = \overline{x} \overline{y} \overline{z} + \overline{x} y \overline{z} + x \overline{y} \overline{z} + x y \overline{z} $$  