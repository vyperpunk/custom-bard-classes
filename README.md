# Bard add-on for Statamic 3 for adding a span and class to selected content

![Statamic 3.0+](https://img.shields.io/badge/Statamic-3.0+-FF269E?style=for-the-badge&link=https://statamic.com)

This is an example Bard addon for Statamic 3 that adds a span with a class to selected content.



## Installation

Install it via the composer command

```
composer require brunosubert/custom-bard-classes
```

In your Bard editor instances (note, *not* the configuration view), you'll see the new button added.

Select some text, click the new icon, and select a class type, and voilà!

## Output

When output, the markup will be a span with a class attached.

```html
<p>This is my text with <span class="les-mills-class bodyattack">BodyAttack</span> highlighted using the addon.</p>
```


## Use on the front end

Styles have been included for a handful of programs (the ones I teach, funnily enough), and will style the selected text
within the Statamic administration area.

You will need to add classes to your front end stylesheets to see them come through there too.

Essentially it will add a generic class ``les-mills-class`` followed by the program name - so this way you can target
all class types, and then tweak per program.

A finished class might be ``les-mills-class bodyattack`` for example.

Your CSS for your frontend can then target that specific class.

```scss
.les-mills-class {
    text-transform: uppercase !important;
    font-weight: bold !important;

    &.bodyattack {
        color: #FCC500 !important;
    }

    /* more class types */
}
```

## License

This addon is licensed under the MIT license.

## Les Mils

Les Mills are an awesome company based on New Zealand, who make the best group fitness classes in the world, including
BODYPUMP - I've been trained in 5 of their programs, and teaching Les Mills group fitness classes for over 14 years.
Their "L" letter has been used for the button for this plugin purely for demonstration purposes.