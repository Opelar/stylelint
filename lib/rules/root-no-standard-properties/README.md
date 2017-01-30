# root-no-standard-properties

***Deprecated: this rule is outside the scope of stylelint's functionality. See [the release planning docs](https://stylelint.io/user-guide/release-planning/) for details.***

Disallow standard properties inside `:root` rules.

```css
    :root { color: #333 }
/** ↑       ↑
 * This selector and these types of standard properties */
```

This rule ignores `$sass` and `@less` variables.

## Options

### `true`

The following patterns are considered warnings:

```css
:root { color: pink; }
```

```css
a, :root { top: 0; }
```

The following patterns are *not* considered warnings:

```css
:root { --foo: 0; }
```

```css
a, :root { --foo: 0; }
```