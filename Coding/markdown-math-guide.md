# Displaying Math Formulas in GitHub Markdown

## Problem
GitHub's markdown renderer doesn't natively support LaTeX math expressions (unlike platforms like Jupyter Notebook or VS Code). When you write LaTeX formulas directly in markdown, they appear as raw text, making mathematical documentation difficult to read.

## Solution
Use an online LaTeX renderer (like CodeCogs) to convert mathematical expressions into images that can be embedded in markdown.

## Method

### Basic Syntax
Replace LaTeX expressions like this:
```
$\int_0^\infty f(t)e^{-st}dt$
```
or
```
\[ \int_0^\infty f(t)e^{-st}dt \]
```

With an HTML image tag using CodeCogs:
```
<img src="https://latex.codecogs.com/svg.latex?\int_0^\infty%20f(t)e^{-st}dt"/>
```

### URL Encoding Rules
When using CodeCogs URL:
1. Replace spaces with `%20`
2. Replace `{` and `}` with their actual characters (no encoding needed)
3. Special characters like `\`, `_`, `^` can be used directly in the formula
4. For complex formulas, test the URL in a browser first

### Examples

1. Simple inline formula:
   ```markdown
   <img src="https://latex.codecogs.com/svg.latex?x^2+y^2=r^2"/>
   ```

2. Fraction and integration:
   ```markdown
   <img src="https://latex.codecogs.com/svg.latex?\frac{d}{dx}\int_0^x%20f(t)dt"/>
   ```

3. Matrix:
   ```markdown
   <img src="https://latex.codecogs.com/svg.latex?\begin{bmatrix}a&b\\c&d\end{bmatrix}"/>
   ```

### Best Practices

1. **Tables**: When using formulas in tables, make sure to:
   - Use the HTML image tag syntax
   - Test the alignment
   ```markdown
   | Expression | Value |
   |------------|-------|
   | <img src="https://latex.codecogs.com/svg.latex?x^2"/> | 4 |
   ```

2. **Long Equations**: For complex equations:
   - Break them into smaller parts
   - Use multiple lines for readability
   - Consider adding explanatory text between parts

3. **Documentation Structure**:
   - Keep a clear hierarchy
   - Use headers for different sections
   - Include examples and explanations

## Advantages
1. Universal compatibility - works on all platforms
2. SVG format ensures clear rendering
3. No need for special plugins or extensions
4. Formulas look professional

## Disadvantages
1. Requires internet connection to render
2. Cannot be easily edited (need to modify URL)
3. No real-time preview while editing
4. Slightly more verbose syntax

## Tips
1. Keep a reference of commonly used formulas
2. Test complex formulas before committing
3. Consider using a script to automate the conversion
4. Maintain consistent styling throughout the document

## Example Repository Structure
```
project/
├── docs/
│   ├── math/
│   │   ├── equations.md
│   │   └── symbols.md
│   └── README.md
└── scripts/
    └── latex2img.py  # Optional conversion script
```

## References
1. [CodeCogs Equation Editor](https://www.codecogs.com/latex/eqneditor.php)
2. [GitHub Markdown Guide](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) 