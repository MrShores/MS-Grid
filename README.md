# MS Grid

**MS Grid** is a fluid CSS, configurable via SASS, and sweet. It's my own attempt to reverse engineer the Boostrap grid. Why? One, to learn how it all works, and two, I no longer need Boostrap for most builds.

## The Markup

```
<div class="container">
    <div class="row">
        <div class="col_4">
            Content goes here...
        </div>
        <div class="col_4">
            Content goes here...
        </div>
        <div class="col_4">
            Content goes here...
        </div>
    </div>
</div>
```

## Settings

```
// Grid widths, columns, spacing
$max_width:             1000px; // width of the container
$container_padding:     15px;   // padding outside of the container
$gutter:                15px;   // space between the columns
$columns:               12;     // number of columns

// Media query breakpoints
$breakpoint_small:       560px; // smallest breakpoint
$breakpoint_medium:      780px; // medium breakpoint
```

## Helper Classes

`.col_hide`

Hide for the desktop grid above `$breakpoint_medium`

`.col_m_hide`

Hide for the medium grid between `$breakpoint_small` and `$breakpoint_medium`

`.col_s_hide`

Hide for the small grid below `$breakpoint_small`

`.col_pad`

Adds the same padding to an element as used by the columns. Convenient for aligning headers without having to include them in a `.row` and `.col_12` markup.