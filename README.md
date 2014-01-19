## tl,dr;

$.serializeJSON(), when called on a selection of inputs, returns a JavaScript object.  `name` attributes become keys and `value` attributes become values.

## examples

```
<input type="text" name="work" value="320 3rd St">
<input type="text" name="home" value="95 Lansing St">
```
```
$('input').serializeJSON() => { work: "320 3rd St", home: "95 Lansing St" }
```

serializeJSON also supports nesting:

```
<input type="text" name="work.street" value="320 3rd St">
<input type="text" name="work.city" value="San Fran">
<input type="text" name="work.state" value="CA">
```
```
$('input').serializeJSON() => { work: { street: "320 3rd St", city: "San Fran", state: "CA" } }
```

## installation
Download the plugin with `curl -O https://raw.github.com/JasonBenn/jquery-serializeJSON/master/serialize-json.js`, and throw it in a `<script>` tag after jQuery and before your source code.
