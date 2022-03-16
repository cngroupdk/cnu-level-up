# CSS

While [HTML](../HTML/) is the fundamental structure of every web page, it can be visually unappealing on its own. **Cascading Style Sheets** or `CSS` is a language web developers use to style the `HTML` content on a web page. If you’re interested in modifying colors, font types, font sizes, images, element positioning, and more, `CSS` is the tool for the job!

- [CSS Anatomy](#css-anatomy)
  - [Ruleset Terms](#ruleset-terms)
  - [Inline Style Terms](#inline-style-terms)
  - [Internal Stylesheet](#internal-stylesheet)
  - [External Stylesheet](#external-stylesheet)
- [Usefull resources](#usefull-resources)

## CSS Anatomy

Understanding that a declaration is used to style a selected element is key to learning how to style HTML documents with CSS! The terms below explain each of the labels in the diagram on the right.

Form more info check [Codecademy Docs: CSS Anatomy](https://www.codecademy.com/resources/docs/css/anatomy).

### Ruleset Terms

```css
p {
  color: blue;
}
```

- `Selector` — The beginning of the ruleset used to target the element that will be styled.

  - ```
    p
    ```

- `Declaration Block` — The code in-between (and including) the curly braces ({ }) that contains the CSS declaration(s).
  - ```css
    p {
      color: blue;
    }
    ```
- `Declaration` — The group name for a property and value pair that applies a style to the selected element.

  - ```
    color: blue;
    ```

- `Property` — The first part of the declaration that signifies what visual characteristic of the element is to be modified.
  - ```css
    color
    ```
- `Value` — The second part of the declaration that signifies the value of the property.
  - ```css
    blue
    ```

### Inline Style Terms

Although CSS is a different language than HTML, it’s possible to write CSS code directly within HTML code using inline styles.

To style an HTML element, you can add the style attribute directly to the opening tag. After you add the attribute, you can set it equal to the CSS style(s) you’d like applied to that element.

```html
<p style="color: blue; font-size: 20px;">Hello World!</p>
```

- `Opening Tag` — The start of an HTML element. This is the element that will be styled.
- `Attribute` — The style attribute is used to add CSS inline styles to an HTML element.
- `Declaration` — The group name for a property and value pair that applies a style to the selected element.
- `Property` — The first part of the declaration that signifies what visual characteristic of the element is to be modified.
- `Value` — The second part of the declaration that signifies the value of the property.

It’s important to know that inline styles are a quick way of directly styling an HTML element, but are rarely used when creating websites. But you may encounter circumstances where inline styling is necessary, so understanding how it works, and recognizing it in HTML code is good knowledge to have.

### Internal Stylesheet

`HTML` allows you to write `CSS` code in its own dedicated section with a [`<style>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style) nested inside of the `<head>` element. The CSS code inside the `<style>` element is often referred to as an _internal stylesheet_.

```html
<head>
  <style>
    p {
      color: red;
      font-size: 20px;
    }
  </style>
</head>
```

An `internal stylesheet` has certain benefits and use cases over inlines styles, but once again, it’s not best practice (we’ll get there, we promise). Understanding how to use `internal stylesheets` is nonetheless helpful knowledge to have.

### External Stylesheet

Developers avoid mixing code by storing `HTML` and `CSS` code in separate files (HTML files contain only HTML code, and CSS files contain only CSS code).

You can create an _external stylesheet_ by using the `.css` file name extension, like so: `style.css`

With an _external stylesheet_, you can write all the CSS code needed to style a page without sacrificing the readability and maintainability of your HTML file.

You can use the `<link>` element to link `HTML` and `CSS` files together. The `<link>` element must be placed within the head of the `HTML` file.

```html
<link href="./style.css" rel="stylesheet" />
```

Don’t worry about memorizing all of these—you will get acquainted with them more and more as you learn!

## Usefull resources

- [Codecademy Docs: CSS](https://www.codecademy.com/resources/docs/css)
- [Codecademy Docs: CSS Anatomy](https://www.codecademy.com/resources/docs/css/anatomy)
- [Codecademy Docs: Selectors](https://www.codecademy.com/resources/docs/css/selectors)
- [Codecademy Docs: Box Model](https://www.codecademy.com/resources/docs/css/box-model)
- [Codecademy Docs: Position](https://www.codecademy.com/resources/docs/css/position)
- [Codecademy Docs: Colors](https://www.codecademy.com/resources/docs/css/colors)
- [Codecademy Docs: Typography](https://www.codecademy.com/resources/docs/css/typography)

## Games to practice `flex-box`

- [flexboxfroggy](http://flexboxfroggy.com/)
- [flexboxdefense](http://www.flexboxdefense.com/)
