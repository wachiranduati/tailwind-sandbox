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
- [x] container-spacing
    adding the container class to the parent div is equivalent to having the container class on bootstrap. It introduces breakpoints within which elements contained in it as it's children abide by.
    More about spacing.
    1. Margin
        - `m-0` - This will add a margin of 0px all around.
            Ideally **m** initializes a margin to the element followed by a unit.
        - `ml-4` - This will add **16px** margin to the left of the element.
        
        > in terms of units *4 units* represents **1 rem** or **16px**

        - `mt-4` - Adds 16px margin to the top
        - `mb-4` - Adds 16px margin to the bottom
        - `mx-4` - Adds 16px margin to the right and left
        - `my-4` - Adds 16px margin to the top and bottom
        - `mt-4` - Adds 16px margin to the top
        - `mt-[20px]` - custom way of adding 20px margin to the top

    2. Padding
        - `p-0` - This will add a padding of 0px all around.
            Ideally **p** initializes a padding to the element followed by a unit.
        - `pl-4` - This will add **16px** padding to the left of the element.
        
        > in terms of units *4 units* represents **1 rem** or **16px**

        - `pt-4` - Adds 16px padding to the top
        - `pb-4` - Adds 16px padding to the bottom
        - `px-4` - Adds 16px padding to the right and left
        - `py-4` - Adds 16px padding to the top and bottom
        - `pt-4` - Adds 16px padding to the top
        - `pt-[20px]` - custom way of adding 20px padding to the top

    3. space between
        You can add space between children elements by adding classes `space-x-4` or `space-y-4`
        i.e 
        `<div class="flex mt-24 space-x-4"><div>item 1</div><div>item 2</div><div>item 3</div><div>item 4</div><div>item 5</div><div>item 6</div><div>item 7</div></div>`

- [x] typpography
    **reference native fonts**
    create a custom script tag i.e
    > <script>
        tailwind.config = {
            theme: {
            fontFamily: {
            'sans': ['ui-sans-serif', 'system-ui'],
            'serif': ['serif', 'Georgia'],
            'mono': ['ui-monospace', 'SFMono-Regular'],
            }
        }
        }
        </script>

    now referencing the fonts can easily be done as so
    `<p class="font-sans">Tailwind is awesome</p>`
    `<p class="font-serif">Tailwind is awesome</p>`
    `<p class="font-mono">Tailwind is awesome</p>`

    **reference external fonts**
    import the custom font via it's cdn link i.e google font links in the header i.e Tapestry font
    then simply add it to the tailwind font family object

    > 'tapestry': ['tapestry', 'Georgia']

    usage falls back to:

    > <p class="font-tapestry">Tailwind is awesome</p>

    **font sizing**
    fonts come in various sizes from:
    > text-xs, text-sm, text-base,text-lg, text-xl

    `<div class="text-9xl">Tailwind is awesome</div>` 

    **font weight**
    font weights can be:
    light, normal, medium, semibold or bold
    example:
    > <div class="font-bold">Tailwind is awesome</div>

    **letter spacing**
    options are: *tracking-tight*, *tracking-normal* or *tracking-wide*
    example:-
    >  <div class="tracking-tight">Tailwind is awesome</div>

    **text alignment**
    options: *text-left*, *text-center*, *text-right*
    example:-
    > <div class="text-left">Tailwind is awesome</div>

    **text decoration**
    like the outline, we can add a text decoration as seen below.
    > <div class="underline decoration-4 decoration-dashed decoration-blue-400">Tailwind is awesome</div>

    Decorations come in various varities i.e
        - dotted
        - dashed
        - wavy
        - double
    
    An offset can be applied to the underline as a class as seen below
    > <div class="underline decoration-4 decoration-blue-400 underline-offset-8">Tailwind is awesome</div>

    **text-transform**
    Under text transform we have 4 classes:
    *normal-case*, *uppercase*, *lowercase*, *capitalize*
    example as:-
    > <div class="normal-case">Tailwind is awesome</div>
