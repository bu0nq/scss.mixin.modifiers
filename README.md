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
  $is-data-modifier: true
);

@use "@bu0nq/scss.mixin.modifiers/modifiers";
```

### Examples

```scss
.example {
    @include modifiers.rounded-base {
        border-radius: 12px;
    }
}

.example_rounded-base {
    border-radius: 12px;
}
```

```scss
.example {
    @include modifiers.rounded-base(true) {
        border-radius: 12px;
    }
}

.example_rounded-base {
    border-radius: 12px;
}

.example[data-modifier-rounded="base"] {
    border-radius: 12px;
}
```

### Rounded


| Name         | BEM Modifier  | Data Modifier (Optional)     |
|--------------|---------------|------------------------------|
| rounded-xs   | _rounded-xs   | data-modifier-rounded="xs"   |
| rounded-sm   | _rounded-sm   | data-modifier-rounded="sm"   |
| rounded-md   | _rounded-md   | data-modifier-rounded="md"   |
| rounded-base | _rounded-base | data-modifier-rounded="base" |
| rounded-lg   | _rounded-lg   | data-modifier-rounded="lg"   |
| rounded-xl   | _rounded-xl   | data-modifier-rounded="xl"   |
| rounded-xxl  | _rounded-xxl  | data-modifier-rounded="xxl"  |

### Size

| Name      | BEM Modifier | Data Modifier (Optional)  |
|-----------|--------------|---------------------------|
| size-xs   | _size-xs     | data-modifier-size="xs"   |
| size-sm   | _size-sm     | data-modifier-size="sm"   |
| size-md   | _size-md     | data-modifier-size="md"   |
| size-base | _size-base   | data-modifier-size="base" |
| size-lg   | _size-lg     | data-modifier-size="lg"   |
| size-xl   | _size-xl     | data-modifier-size="xl"   |
| size-xxl  | _size-xxl    | data-modifier-size="xxl"  |
