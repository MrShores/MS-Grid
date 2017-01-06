# MS Grid

**MS Grid** is a fluid CSS, configurable via SASS, and sweet. It's my own attempt to reverse engineer the Boostrap grid. Why? One, to learn how it all works, and two, I no longer need Boostrap for most builds.

[View the demo &raquo;](http://michaelshores.com/ms-grid)

**Jump To**

1. [The Markup](#markup)
2. [Settings](#settings)
3. [Helper Classes](#helper)

## <a name="markup"></a>The Markup

```
// Standard grid layout

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

// Full width container

<div class="container-full">
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

## <a name="settings"></a>Settings

**MS Grid** is configurable using SASS variables. Just change values and recompile the SASS to CSS.

```
// Grid widths, columns, spacing

$max_width:             1000px; // width of the container
$container_padding:     15px;   // padding outside of the container
$gutter:                15px;   // space between the columns
$columns:               12;     // number of columns

// Media query settings

$breakpoint_small:      560px;  // smallest breakpoint
$breakpoint_medium:     780px;  // medium breakpoint
```

## <a name="helper"></a>Helper Classes

<dl>
    <dt><code>.col_hide</code></dt>
    <dd>Hide for the desktop grid above <code>$breakpoint_medium</code></dd>

    <dt><code>.col_m_hide</code></dt>
    <dd>Hide for the medium grid between <code>$breakpoint_small</code> and <code>$breakpoint_medium</code></dd>

    <dt><code>.col_s_hide</code></dt>
    <dd>Hide for the small grid below <code>$breakpoint_small</code></dd>

    <dt><code>.col_pad</code></dt>
    <dd>Adds the same padding to an element as used by the columns. Convenient for aligning headers without having to include them in a <code>.row</code> and <code>.col_12</code> markup</dd>
</dl>