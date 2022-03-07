# How to build a simple website with HTML

Individual HTML elements are not enough to create a website. So let's see what more we need to build a simple website from scratch.

How to create an HTML document
First, let's open Visual Studio Code (or your favorite code editor). In the folder of your choice, create a new file and name it index.html.

In the index.html file, type ! (exclamation mark) and press enter. You will see something like this:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

This is the minimal code that an HTML document should have to make up a website. And here we have:

1. `<!DOCTYPE html>`: First we have Doctype. For some weird historical reason in HTML we have to include the doctype for everything to work correctly.
2. `<html lang="en"></html>`: The `<html>` element wraps all the content on the page, also known as the root element. And we should always include the `lang` attribute to declare the language of the page.
3. `<head></head>`: The `<head>` element is a container for everything you want to include, but not content that you show to your users.
4. `<meta charset="UTF-8" />`: The first meta element is used to set the character set to be UTF-8, which includes most characters from written languages.
5. `<meta name="viewport" content="width=device-width, initial-scale=1.0" />`: The second meta element specifies the browser viewport. This setting is for a mobile-optimized site.
6. `<title>Document</title>`: This is the `<title>` element. It sets the title of the page.
7. `<body></body>`: The `<body>` element contains all the content on the page.

## How to build a pancake recipe page

Alright, now that we have the starter code, let's build a beer recipe page.

First, let's give the `<title>` element content of the pancakes recipe. You will see the text on the web page tab change. In the `<body>` element, let's create 3 elements: `<header>`, `<main>` and `<footer>` representing 3 sections.

## 1. Build the header section

In the header, we want to have the logo and the navigation. Therefore, let's create a div with the content ALL RECIPE for the logo.
For the navigation, let's use the `<nav>` element. Within the `<nav>` element, we can use `<ul>` to create an unordered list.
We want to have 3 `<li>` elements for 3 links: Ingredients, Steps, and Subscribe. The header code looks like this:

```
<header>
<div>BEER RECIPE</div>
  <nav>
    <ul>
      <li><a href="#ingredients">Ingredients</a></li>
      <li><a href="#steps">Steps</a></li>
      <li><a href="#subscribe">Subscribe</a></li>
    </ul>
  </nav>
</header>
```

## 2. Build the Main Section

In the main section, first, we want to have a title and an image. We can use `h1` for the title and `<img>` for the image (we can use an image from Unsplash for free):

```
<main>
    <h1>Another Zombie Dust Clone
</h1>
    <img
        src="https://untappd.akamaized.net/photos/2018_08_18/9a3d698621a81b29bfd26b2df99446ff_raw.jpeg"
        alt="beer"
        width="250"
    />
</main>
```

Next, we want to list all the ingredients. We can use `<ol>` to create an ordered list and `<input type="checkbox" />` to create a checkbox.

But before that, we can use `<h2>` to start a new content block. We also want to add the id attribute for `<h2>` so that the link in the navigation knows where to go:

```
...
<main>
  ...
  <h2 id="ingredients">Ingredients</h2>
  <ol>
    <li>
      <span>6 lbs Extra Light DME</span>
    </li>
    <li>
      <span>1 lb American – Munich – Light 10L</span>
    </li>
    <li>
      <span>.5 lb German – CaraFoam</span>
    </li>
    <li>
      <span>.5 lb American Caramel / Crystal 60L</span>
    </li>
    <li>
      <span>.5 lb German – Melanoidin</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 10 Mins left during steep</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 15 Mins</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 10 Mins</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 05 Mins</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 01 Mins</span>
    </li>
    <li>
      <span
        >3 oz Citra – Pellet (11AA) Dry Hop (start day 2 through day 7)</span
      >
    </li>
    <li>
      <span>2 pkgs Safale – English Ale S-04</span>
    </li>
  </ol>
</main>
...
```

After the ingredients, we want to list all the steps. We can use `<h4>` for the step heading and `<p>` for the step content:

```
...
    <main>
    ...
      <h2 id="steps">Steps</h2>
      <h4>Additional Instructions</h4>
    <ol>
    <li>
      <span>Boil: 60 Minutes</span>
    </li>
    <li>
      <span>Primary Ferment: 10 days</span>
    </li>
    <li>
      <span
        >Secondary Ferment: 12 days</span
      >
    </li>
  </ol>
      <h4>Procedure</h4>
      <p>
       Nothing really out of the ordinary. I steeped the grains at 150 and fermented between 60 & 65 degrees.
       Jump started the yeast with a cup cooled wort.
       After 10 days I dumped trub in the conical and gave it another 12 days to clarify then bottled in 22oz bottles.
      </p>
    </main>
...
```

Alright, now that we are done with the main section, let's move on to the footer section.

## 3. Build the Footer Section

In the footer, we want to have a subscribe form and copyright text.

For the subscribe form, we can use the `<form>` element. Inside it, we can have an `<input type="text">` for text input and a `<button>` for the submit button.

For the copyright text, we can simply use a `<div>`. Notice here, we can use the HTML entity $copy; for the copyright symbol.

We can add `<br>` to add some space between the subscribe form and the copyright text:

```
...
    <footer>
      <h6 id="subscribe">Subscribe</h6>
      <form onsubmit="alert('Subscribed')">
        <input type="text" placeholder="Enter Email Address" />
        <button>Submit</button>
      </form>
      <br />
      <div>&copy; Beer 4 you </div>
    </footer>
...
```

Alright now we are done!

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Beer Recipe</title>
  </head>
  <body>
    <header>
      <div>BEER RECIPE</div>
      <nav>
        <ul>
          <li><a href="#ingredients">Ingredients</a></li>
          <li><a href="#steps">Steps</a></li>
          <li><a href="#subsribe">Subscribe</a></li>
        </ul>
      </nav>
    </header>
    <main>
   <main>
    <h1>Another Zombie Dust Clone
</h1>
    <img
        src="https://untappd.akamaized.net/photos/2018_08_18/9a3d698621a81b29bfd26b2df99446ff_raw.jpeg"
        alt="beer"
        width="250"
    />
<h2 id="ingredients">Ingredients</h2>
  <ol>
    <li>
      <span>6 lbs Extra Light DME</span>
    </li>
    <li>
      <span>1 lb American – Munich – Light 10L</span>
    </li>
    <li>
      <span>.5 lb German – CaraFoam</span>
    </li>
    <li>
      <span>.5 lb American Caramel / Crystal 60L</span>
    </li>
    <li>
      <span>.5 lb German – Melanoidin</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 10 Mins left during steep</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 15 Mins</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 10 Mins</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 05 Mins</span>
    </li>
    <li>
      <span>1 oz Citra – Pellet (11AA) 01 Mins</span>
    </li>
    <li>
      <span
        >3 oz Citra – Pellet (11AA) Dry Hop (start day 2 through day 7)</span
      >
    </li>
    <li>
      <span>2 pkgs Safale – English Ale S-04</span>
    </li>
  </ol>
      <h2 id="steps">Steps</h2>
      <h4>Additional Instructions</h4>
    <ol>
    <li>
      <span>Boil: 60 Minutes</span>
    </li>
    <li>
      <span>Primary Ferment: 10 days</span>
    </li>
    <li>
      <span
        >Secondary Ferment: 12 days</span
      >
    </li>
  </ol>
      <h4>Procedure</h4>
      <p>
       Nothing really out of the ordinary. I steeped the grains at 150 and fermented between 60 & 65 degrees.
       Jump started the yeast with a cup cooled wort.
       After 10 days I dumped trub in the conical and gave it another 12 days to clarify then bottled in 22oz bottles.
      </p>
    </main>
    <hr />
    <footer>
      <h6 id="subscribe">Subscribe</h6>
      <form onsubmit="alert('Subscribed')">
        <input type="text" placeholder="Enter Email Address" />
        <button>Submit</button>
      </form>
      <br />
       <div>&copy; Beer 4 you </div>
    </footer>
  </body>
</html>
