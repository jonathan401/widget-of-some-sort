# toolbar
Trying to create a clickable tooltip or toolbar (I'd be using these interchangeably) that can be customized to appear at specific positions. This could come-in handy when working on my react projects. For example
clicking on an avatar to reveal some information about the user. The contents can be passed to the tooltip component using `props.children`. 
I built this project to test typescript skills and increase my problem solving skills

# Notes
1. For the toolbar to work properly, you'd have to position it relative to the parent. i.e. 

``` 
.toolbar-parent {
  position: relative;
}

.toolbar {
  position: absolute;
}

```

This is because since the toolbar has to be inside a container (in this case, the element that would be used to toggle the visibility of the tooltip).

2. Tooltips usually have little arrows pointing to the element that encloses them. I tried implementing this but couldn't figure out how to make sure the arrow inherited the color of it's parent (i.e the tooltip) :). So I decided not to include it in the tooltip.

3. For now, the only positions the tooltip can be customized to 
appear in are the:
- bottom left,
- center,
- bottom right.


# Props
The tootip accepts the following props:
- width (required) - of type number that will be used to customize the width of the tooltip in pixels.
- height (required) - of type number that will be used to customize the height of the tooltip in pixels.
- color - this is an optional prop that will be used to customize the background colour of the tooltip. If none is specified, 
a default of white is used
