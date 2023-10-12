# INFO6150-assignment5

Freya is a vegan, environmental friendly makeup-skincare website. It has 2 web pages currently, which are Home and About.
Both these pages contain a navigation bar and a footer.
1. The navigation bar contains a set if links to travel to different web pages. The logo and items are aligned in flexbox layout. The font used for these is taken from the variable $primary-font-stack.
2. The next section in the home page has a cover picture with a heading and description. There is also a button which redirects us to the About page.
3. Below that is a div which is another flexbox. the right div of the box contains an image, and the left div has content with a button.
4. The 3rd section is a grid layout, and has images randomly arranged in grid cells, with different dimensions for an abstract display. The center part of the grid layout has some text, with a button.
5. Below that, is a grid column layout displaying different products available.
6. The last section is the footer, which is a flex layout. It has an input text field for email id and a Submit button. The right box has a list of all external links from this page, in an inline block layout.

The following SASS/SCSS features are used -
1. Variables like $primary-font-stack, $primary-bg-color, $btn-bg-color with initiated values are declared in the _config.scss file, and are used directly in style.scss file and also in various mixins.
2. Custom Properties, also known as CSS variables are declared in root component in style.scss class. Example used is --primary, which takes the $primary-font-stack and is used for section 2 background color.
3. Nesting is used all over the style.scss file between html elements and their classes. Nesting is also used when property attributes are separated by hyphen(-) and have a common string, like margin-left and margin-right. One example of this usage is for nav bar declaration of margins.
4. Interpolation is used to embed the result of a SassScript expression into a chunk of CSS. It is used in a mixin set-btn-hover which passes the $property variable and a background color and color of the button are set.
5. Placeholder Selectors used to set css styles, which can be extended and reused. It is used to declare css properties for all the buttons and is present in _buttons.scss file.
6. Mixins are a language concept that allows us to inject some code into a class. We have used 3 mixins in config file and is declared for reusability. It can pass variables and assign them to css variables. Its used to set intro text color and set font size for responsive environment.
7. Functions can take variables, do calculations and return the result to a css attribute. We have used function set-text-color to take evenOrOdd variable and return appropriate color. It is used on the text field in product grid.
8. Parent selector can be used in nested selectors to refer to the outer selector. Its is used in various parts, one example is for footer. 
9. @debug is at-rule used to show the style sheet variables while developing. Used in set-btn-hover mixin.
10. The equality operators return whether or not two values are the same. Its used in set-text-color function.
11. @if and @else are used to check values and execute the block of code in their respective parantheses. Used in set-text-color function.