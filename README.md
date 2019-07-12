
# css-naming-conventions
[!!] WIP

Using BEM with a component approach to maximize understanding at simple view of what the code does.
The idea is to amost know how the component is going to be with just a glance to the css


`.ComponentName`
  Also `.componentName` or `.component-name` That is up to you.

`.ComponentName__element`

`.ComponentName--modifier`

`.ComponentName.is-stateOfComponent` (ex: .is-selected)

`.ComponentName.not-stateOfComponent` (ex: not-visible, is recommended to use .is-stateOf..)



Note: not be afraid to use **UPPERCASE** to add more readability and emphasis to important words, and use a lodash to see more separation between names

Ex:

`.ButtonFancy.is-focus` (regular)

`.ButtonFancy.is_FOCUS` (super_SIZE)

> fun documentary https://en.wikipedia.org/wiki/Super_Size_Me ☺




# Writing
Is easier to read and understand if we can picture the style in our mind, like a composition, structuring along reading.
Also is useful to break apart in case of wanting code splitting.

ComponentName
   - Layout
   
      position, dimensions, space, aligment...
   - Styling
   
      fonts, colors, borders, background, gradients...
   - Others
   
      uncommond use properties.

Ex:

~~~
.ComponentName{
  position,
  display,
  with,
  height,
  margin,
  padding,
  z-index,
  ...
  
  border,
  font,
  color,
  background,
  ...
  
  clip-path,
  transtion,
  transform,
  ... 
}
~~~

# Global scope
In case of using some class with global scope, let's call them helpers, because they help :p
like a prefix

`.helper__hidden{}`
` .H__hidden{}` Shorten version

**Layout**

in case of layout, if we need to add specific code to the layout composition

`.layout__section{}`
`.L__section{}`

**Media Queries**

`.break-point__small{}`
`.BP__sm{}`



# BEM
Is a way to name your elements with some relation and meaning
http://getbem.com/naming/

**Block**

Represent a meaningful thing in our web. It's an awareful tag, it know that he is important a represent something.
Ex: 
`.header{}`

**Element**

Is a part of a block, alone it has little or none meaning of this own.

Ex: 
`.header__logo{}`

The logo has to be somewhere, that's why we need a block to contain it.


**Modifier**

They say people can't change, but HTML can!

Flags on blocks or elements. Use them to change appearance, behavior or state.

Ex: 
~~~
.header{}
.header.header--dark{}
.header__logo{}
.header__logo.header__logo--small{}
~~~

# State
Is used for the possible variations of a block or element (ex: selected, active, inactive, expanded)
They are prefixed with is-, ex: is-selected

