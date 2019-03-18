# Flexbute CSS Grid

A simple mobile first and flexbox based Grid system controlled by HTML attributes. (version: 1.0)

## Installation

### Without building

1. Download or fork the repository
2. Embed the flexbute.css file inside the dist folder into your HTML

### With building

1. Download or fork the repository
2. Install [SASS](https://sass-lang.com)
3. Build the flexbute.scss file inside the dist folder
4. Embed the flexbute.css file inside the dist folder into your HTML

Building the flexbute.scss file with SASS

```bash
sass --watch src/flexbute.scss:dist/flexbute.css
```

Embedding the flexbute.css file

```html
<link rel="stylesheet" href="path/to/flexbute.css">
```

## Documentation

The grid is controlled by HTML attributes. There are two different attributes (default values).

| Level  | Attribute | Description                                     |
|--------|-----------|-------------------------------------------------|
| Grid   | data-grid | used on the wrapper element that defines a grid |
| Column | data-col  | used on the column element to control it        |

All attribute values shown beneath are separated by spaces and can be combined freely.

### Defining a basic grid

```html
<div data-grid>
    <div data-col>...</div>
    <div data-col>...</div>
    <div data-col>...</div>
</div>
```

### Grid control over the grid attribute

Every column uses 4 spaces of the grid (12 by default)

```html
<div data-grid="4">
    <div data-col>...</div>
    <div data-col>...</div>
    <div data-col>...</div>
</div>
```

### Grid control over the column attribute

Every column now again uses 4 spaces of the grid (12 by default).

Column width definitions inside the data-grid attribute will be overridden by the
data-col attribute by default, this makes it possible to use both controll types at the same time.

```html
<div data-grid>
    <div data-col="4">...</div>
    <div data-col="4">...</div>
    <div data-col="4">...</div>
</div>
```

### Grid breakpoints over the grid attribute

```html
<div data-grid="12 sm-6 md-4 lg-2">
    <div data-col>...</div>
    <div data-col>...</div>
    <div data-col>...</div>
</div>
```

### Grid breakpoints over the column attribute

```html
<div data-grid>
    <div data-col="12 sm-6 md-4 lg-2">...</div>
    <div data-col="12 sm-6 md-4 lg-2">...</div>
    <div data-col="12 sm-6 md-4 lg-2">...</div>
</div>
```

### Column offset

```html
<div data-grid>
    <div data-col="12 left-3">...</div>
    <div data-col="12 right-3">...</div>
</div>
```

### Column offset with breakpoints

```html
<div data-grid>
    <div data-col="12 left-0 left-md-2 left-lg-4">...</div>
    <div data-col="12 right-0 right-md-2 right-lg-4">...</div>
</div>
```

### Nested grids

```html
<div data-grid>
    <div data-col="6">
            <div data-grid>
                <div data-col="6">...</div>
                <div data-col="6">...</div>
            </div>
        </div>
    </div>
    <div data-col="6">...</div>
</div>
```

### Column alignment

```html
<div data-grid="[alignment-value]">
    <div data-col="2">...</div>
    <div data-col="2">...</div>
</div>
```

Alignment values (horizontal):

| alignment value | css flex value css: justify-content |
|-----------------|-------------------------------------|
| hCenter         | center                              |
| hStart          | flex-start                          |
| hEnd            | flex-end                            |
| hSpaceBetween   | space-between                       |
| hSpaceAround    | space-around                        |
| hSpaceEvenly    | space-evenly                        |

Alignment values (vertical):

| alignment value | css flex value css: align-items |
|-----------------|---------------------------------|
| vCenter         | center                          |
| vStart          | flex-start                      |
| vEnd            | flex-end                        |
| vStretch        | stretch                         |
| vBaseline       | baseline                        |

### Default grid breakpoints

| Breakpoint  | Screen width |
|-------------|--------------|
| xs          | 448px        |
| sm          | 576px        |
| md          | 768px        |
| lg          | 1024px       |
| xl          | 1280px       |

### Special attribute values

No gutter

Used to turn off the gutter.

```html
<div data-grid="no-gutter">
    <div data-col="2">...</div>
    <div data-col="2">...</div>
</div>
```

No spill

No negative margin on the grid level, used to turn off the left and right compensation of the gutter.

```html
<div data-grid="no-spill">
    <div data-col="2">...</div>
    <div data-col="2">...</div>
</div>
```

### SASS Variables

Further documentation can be found inside the flexbute.scss file.

| Variable name       | Description |
|---------------------|-------------|
| $GRID_TYPE          | Defines the if the grid is mobile or desktop first                    |
| $COLUMN_GUTTER      | Defines the gutter size of the grid                                   |
| $COLUMN_COUNT       | Defines the base column count of the grid (max width of one column)   |
| $COLUMN_GROW        | Defines if a single column without fixed with should dynamically grow |
| $COLUMN_BREAKPOINTS | A collection that defines the breakpoints for the columns             |
| $GRID_ATTRIBUTE     | The attribute that defines a grid                                     |
| $COLUMN_ATTRIBUTE   | The attribute that defines a column                                   |

## Recommendations or questions

If you have any ideas that would make the grid even greater, feel free to contact me:
[mailto](Mailto:wag96niklas@gmail.com)

Thank you for downloading, made with ❤️ and 🍺 in Munich
