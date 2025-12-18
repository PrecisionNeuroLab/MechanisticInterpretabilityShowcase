# Mechanistic Interpretability Showcase

A research showcase page demonstrating mechanistic interpretability tools developed by the Precision Neuro Lab.

## Customization

### Adding New Research Cards

Edit `index.html` and add new cards in the `research-section`:

```html
<div class="research-card">
    <h3>Your Research Title</h3>
    <p>Description of your research.</p>
</div>
```

### Adding Interactive Demos

Add demo cards in the `demos-section` of `index.html`:

```html
<div class="demo-card">
    <h3>Demo Title</h3>
    <p>Demo description.</p>
    <a href="demo-link.html" class="btn btn-primary">Try Demo</a>
</div>
```

### Styling

Modify colors and styles in `styles.css`. Key CSS variables are defined at the top:

```css
:root {
    --primary-color: #2563eb;
    --secondary-color: #7c3aed;
    /* Add more custom variables */
}
```