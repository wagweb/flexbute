# Flexbute CSS Grid

A simple mobile first and Flexbox based grid system controlled by HTML attributes. (version: 2.0)

## Documentation

The Flexbute grid is controlled via HTML attributes, this means it wont collide with any classes inside your project and the HTML has an overall cleaner look.

| Level  | Attribute | Description                                     |
|--------|-----------|-------------------------------------------------|
| Grid   | data-grid | used on the wrapper element that defines a grid |
| Column | data-col  | used on the column element to control it        |

All attribute values shown beneath are separated by spaces and can be combined freely.

### Defining the most basic grid

```html
<div data-grid>
    <div data-col>...</div>
    <div data-col>...</div>
    <div data-col>...</div>
</div>
```

### Controlling the column size with the grid level attribute

```html
<div data-grid="4">
    <div data-col>...</div>
    <div data-col>...</div>
    <div data-col>...</div>
</div>
```

### Controlling the column size with the column level attribute

```html
<div data-grid>
    <div data-col="4">...</div>
    <div data-col="4">...</div>
    <div data-col="4">...</div>
</div>
```

### Defining breakpoints with the grid level attribute

```html
<div data-grid="12 xs-12 sm-8 md-6 lg-4 xl-2">
    <div data-col>...</div>
    <div data-col>...</div>
    <div data-col>...</div>
</div>
```

### Defining breakpoints with the column level attribute

```html
<div data-grid>
    <div data-col="12 xs-12 sm-8 md-6 lg-4 xl-2">...</div>
    <div data-col="12 xs-12 sm-8 md-6 lg-4 xl-2">...</div>
    <div data-col="12 xs-12 sm-8 md-6 lg-4 xl-2">...</div>
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

### Column alignment

```html
<div data-grid="[alignment-value]">
    <div data-col="2">...</div>
    <div data-col="2">...</div>
</div>
```

Alignment values (horizontal):

| alignment value | corresponding css flex value (justify-content) |
|-----------------|------------------------------------------------|
| h-center        | center                                         |
| h-start         | flex-start                                     |
| h-end           | flex-end                                       |
| h-space-between | space-between                                  |
| h-space-around  | space-around                                   |
| h-space-evenly  | space-evenly                                   |

Alignment values (vertical):

| alignment value | corresponding css flex value (align-items) |
|-----------------|--------------------------------------------|
| v-center        | center                                     |
| v-start         | flex-start                                 |
| v-end           | flex-end                                   |
| v-stretch       | stretch                                    |
| v-baseline      | baseline                                   |

### Default grid breakpoints

| Breakpoint  | Screen width |
|-------------|--------------|
| xs          | 448px        |
| sm          | 576px        |
| md          | 768px        |
| lg          | 1024px       |
| xl          | 1280px       |

### Special grid level attributes

No gutter

Used to turn off the gutter.

```html
<div data-grid="no-gutter">
    <div data-col="2">...</div>
    <div data-col="2">...</div>
</div>
```

No spill

No negative margin on the grid level, used to turn off the left and right compensation for the gutter.

```html
<div data-grid="no-spill">
    <div data-col="2">...</div>
    <div data-col="2">...</div>
</div>
```

### SASS Variables

Further documentation can be found inside the src/flexbute.scss file.

| Variable name           | Description                                                             |
|-------------------------|-------------------------------------------------------------------------|
| $FLB_GRID_TYPE          | Defines the if the grid is mobile or desktop first                      |
| $FLB_COLUMN_GUTTER      | Defines the gutter size of the grid                                     |
| $FLB_COLUMN_COUNT       | Defines the base column count of the grid (max combined width in a row) |
| $FLB_COLUMN_GROW        | Defines if a single column without fixed with should dynamically grow   |
| $FLB_COLUMN_BREAKPOINTS | A collection that defines the breakpoints for the columns               |
| $FLB_GRID_ATTRIBUTE     | The attribute name used to define a grid                                |
| $FLB_COLUMN_ATTRIBUTE   | The attribute name used to define a column                              |

## Recommendations or questions

If you have any ideas that would make the grid even greater, feel free to contact me:
[mailto](Mailto:niklas@wagweb.de)

Thank you for downloading, made with ❤️ and 🍺 in Munich
