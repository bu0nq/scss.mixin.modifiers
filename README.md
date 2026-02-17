# SCSS.Mixin.Modifiers

Package for integrating `SCSS.Mixins.Modifiers` in a web environment.

![npm](https://img.shields.io/npm/v/@bu0nq/scss.mixin.modifiers?style=for-the-badge)
![npm](https://img.shields.io/npm/dt/@bu0nq/scss.mixin.modifiers?style=for-the-badge)
___

## Installation

This package can be deployed automatically using NPM:

```
npm i @bu0nq/scss.mixin.modifiers
```

## Usage

```scss
@use "@bu0nq/scss.mixin.modifiers/modifiers";
```

or

```scss
@use "@bu0nq/scss.mixin.modifiers/variables" with (
  $is-modifier: true,
  $is-class-modifier: true,
  $is-class-modifier-rounded: true,
  $is-class-modifier-size: true,
  $is-class-modifier-type: true,
  $is-data-modifier: true,
  $is-data-modifier-rounded: true,
  $is-data-modifier-size: true,
  $is-data-modifier-type: true
);

@use "@bu0nq/scss.mixin.modifiers/modifiers";
```

### Rounded

Modifiers for changing the rounding of a block or element.

| Mixin Name   | Additional mixins                        | Class Modifier | Data Modifier (Optional)      |
|--------------|------------------------------------------|----------------|-------------------------------|
| rounded-auto | class-rounded-auto<br/>data-rounded-auto | _rounded-auto  | data-modifier-rounded="auto"  |
| rounded-none | class-rounded-none<br/>data-rounded-none | _rounded-none  | data-modifier-rounded="none"  |
| rounded-xs   | class-rounded-xs<br/>data-rounded-xs     | _rounded-xs    | data-modifier-rounded="xs"    |
| rounded-sm   | class-rounded-sm<br/>data-rounded-sm     | _rounded-sm    | data-modifier-rounded="sm"    |
| rounded-md   | class-rounded-md<br/>data-rounded-md     | _rounded-md    | data-modifier-rounded="md"    |
| rounded-base | class-rounded-base<br/>data-rounded-base | _rounded-base  | data-modifier-rounded="base"  |
| rounded-lg   | class-rounded-lg<br/>data-rounded-lg     | _rounded-lg    | data-modifier-rounded="lg"    |
| rounded-xl   | class-rounded-xl<br/>data-rounded-xl     | _rounded-xl    | data-modifier-rounded="xl"    |
| rounded-xxl  | class-rounded-xxl<br/>data-rounded-xxl   | _rounded-xxl   | data-modifier-rounded="xxl"   |

```scss
.example {
    @include modifiers.rounded-base {
        border-radius: 12px;
    }
    
    @include modifiers.rounded-lg {
        border-radius: 16px;
    }
}

// Result

.example_rounded-base {
    border-radius: 12px;
}

.example[data-modifier-rounded="base"] {
    border-radius: 12px;
}

.example_rounded-lg {
    border-radius: 16px;
}

.example[data-modifier-rounded="lg"] {
    border-radius: 16px;
}
```

### Size

Modifiers for changing the size of a block or element.

| Mixin Name | Additional mixins                  | Class Modifier | Data Modifier (Optional)  |
|------------|------------------------------------|----------------|---------------------------|
| size-xs    | class-size-xs<br/>data-size-xs     | _size-xs       | data-modifier-size="xs"   |
| size-sm    | class-size-sm<br/>data-size-sm     | _size-sm       | data-modifier-size="sm"   |
| size-md    | class-size-md<br/>data-size-md     | _size-md       | data-modifier-size="md"   |
| size-base  | class-size-base<br/>data-size-base | _size-base     | data-modifier-size="base" |
| size-lg    | class-size-lg<br/>data-size-lg     | _size-lg       | data-modifier-size="lg"   |
| size-xl    | class-size-xl<br/>data-size-xl     | _size-xl       | data-modifier-size="xl"   |
| size-xxl   | class-size-xxl<br/>data-size-xxl   | _size-xxl      | data-modifier-size="xxl"  |

```scss
.example {
    @include modifiers.size-base {
        height: 40px;
        line-height: 20px;
        font-size: 14px;
    }
    
    @include modifiers.size-lg {
        height: 48px;
        line-height: 24px;
        font-size: 16px;
    }
}

// Result

.example_size-base {
    height: 40px;
    line-height: 20px;
    font-size: 14px;
}

.example[data-modifier-size="base"] {
    height: 40px;
    line-height: 20px;
    font-size: 14px;
}

.example_size-lg {
    height: 48px;
    line-height: 24px;
    font-size: 16px;
}

.example[data-modifier-size="lg"] {
    height: 48px;
    line-height: 24px;
    font-size: 16px;
}
```

### Type

Modifiers for changing the type of block or element.

| Mixin Name   | Additional mixins                        | Class Modifier | Data Modifier (Optional)     |
|--------------|------------------------------------------|----------------|------------------------------|
| type-base    | class-type-base<br/>data-type-base       | _type-base     | data-modifier-type="base"    |
| type-fill    | class-type-fill<br/>data-type-fill       | _type-fill     | data-modifier-type="fill"    |
| type-icon    | class-type-icon<br/>data-type-icon       | _type-icon     | data-modifier-type="icon"    |
| type-outline | class-type-outline<br/>data-type-outline | _type-outline  | data-modifier-type="outline" |
| type-text    | class-type-text<br/>data-type-text       | _type-text     | data-modifier-type="text"    |

```scss
.example {
    @include modifiers.type-base {
        background-color: hsl(0, 0%, 5%);
        border-color: transparent;
    }

    @include modifiers.type-outline {
        background-color: transparent;
        border-color: hsl(0, 0%, 5%);
    }
}

// Result

.example_type-base {
    background-color: hsl(0, 0%, 5%);
    border-color: transparent;
}

.example[data-modifier-type="base"] {
    background-color: hsl(0, 0%, 5%);
    border-color: transparent;
}

.example_type-outline {
    background-color: transparent;
    border-color: hsl(0, 0%, 5%);
}

.example[data-modifier-type="outline"] {
    background-color: transparent;
    border-color: hsl(0, 0%, 5%);
}
```
### State

Modifiers for changing the state of a block or element.

| Mixin Name  | Class Modifier |
|-------------|----------------|
| is-active   | _is-active     |
| is-current  | _is-current    |
| is-disabled | _is-disabled   |
| is-hidden   | _is-hidden     |
| is-hide     | _is-hide       |
| is-invalid  | _is-invalid    |
| is-open     | _is-open       |
