# TailwindCSS

This is a reposity based on a tutorial created by Brad Traversy on mastering tailwindCSS and all it's utility classes.

Covered...
- [x] colours
    > Colours come in interesting varieties i.e white, black, red, green, blue, orange, yellow, purple, lime, emerald, teal, cyan, indigo, violet, fuchsia, pink, rose, sky, gray, slate, zinc, neutral, stone, amber,  -->

    ### css utility classes
    - text-[color]-[shade]
        The colour can be any from the list above. However, notably black and white don't have shades. Shades can be anything from 50 - 900
        example:
        `<p class="text-cyan-400">This text will have a colour cyan shade of 400</p>`

        
    - bg-[colour]-shade
        Works more of less like the text-color-shade but instead sets the background of the html element.

        example:
        `<div class="bg-fuchsia-400"><p>The div will have a background color of fuchsia with shade 400</p></div>`
    
    - text underline
        Sets the underline colour on an element.
        The class must be preceded by an underline class, then proceed to add decoration-colour-shade to set it.
        example:
        `<p class="underline decoration-red-500">Tailwind is awesome</p>`
    
    - border colour
        The first border class adds a border to your element and then followed by the border-color-shade tweaks it to the preferred colour profile.
        example:
        `<p class="border border-red-500">Tailwind is awesome</p>`

    - divide colour
        Applied to a parent element that would ideally contain children elements. The divide class adds divides in your preferred axis x / y in the your preferred colour shade.
        The first class `divide-y` adds a divider rule to each child element's y axis ideally underneath it.
        `divide-x` would set it to the left left side of the element.
        The followup class `divide-lime-300` goes ahead to set the followup colour profile of your now set up divider.

        example:
        `<div class="divide-y divide-lime-300"><div>item 1</div><div>item 2</div><div>item 3</div><div>item 4</div><div>item 5</div></div>`

    - outline colour
        Resembles a border but with a thicker stroke size. 
        First class `outline` sets out the outline then the followup class `outline-red-500` sets the colour shade.
        example:
        `<p class="outline outline-red-500">Tailwind is awesome</p>`
    - box shadow colour
        This will add a shadow to your html element. The first class has to be `shadow-` with a sizing to it i.e `shadow-xl` `shadow-l` etc.
        Followup class is the shadow colour shade itself i.e `shadow-cyan-300` you can also set the opacity of this by adding a `/percent` suffix to the shade making `shadow-cyan-300/20` to add an opacity of 20% to the shadow.
        example:
        `<button class="shadow-lg shadow-cyan-300">Subscribe</button>`
    - accent colour
        Want to tweak colours on elements such as checkboxes? Add an accent colour to it to end up bedazzling it.
        This goes as simply as a single class i.e `accent-colour-shade`
        example:
        `<input type="checkbox" checked class="accent-lime-500">`

    - arbitrary colour
        Want to use your very own custom colours?
        Simple.
        You can add your preferred colour as either as an rgb or hexcode as seen below.

        colour code example:
        `<div class="bg-[#427fab]">Hex Code</div> <div class="bg-[rgb(255,0,0)]">RGB colour code</div>`

colours can also be added in a myriad of ways adding the customization ability of all this.