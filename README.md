# Baseline Grid Overlay

## Example

[Sebastiaan Beek portfolio (sebastiaanbeek.nl)](https://sebastiaanbeek.nl)

Press `Ctrl + g`

## Code

### SCSS

```css
$baseline: 16px; //Adjust the value to your needs

$baseline-color: rgba(white, 0.06); //The color of the grid

.baseline {
    position: relative;

    &:after {
        position: absolute;
        user-select: none;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        z-index: 999999;
        content: "";
        display: block;
        background: linear-gradient(
            to bottom,
            $baseline-color,
            $baseline-color 8px,
            transparent 1px,
            transparent
        );
        background-size: 100% $baseline;
    }
}
```

### JS

```javascript
const body = document.querySelector("html");
document.onkeyup = function (e) {
    if (e.ctrlKey && e.which == 71) {
        body.classList.toggle("baseline");
    }
};
```
