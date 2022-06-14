# Nova Froala Field

### :warning: This is a fork of the original [Nova Froala Field](https://github.com/froala/nova-froala-field) which has been archived! :warning

## Installation

```bash
composer require wimski/nova-froala-field
```

## Usage

See original [README.md](https://github.com/froala/nova-froala-field/blob/master/README.md#usage).

### Custom Elements

To add custom elements like buttons, icons or plugins, you can create separate scripts and load them in the editor.
<br>See also the documentation: https://froala.com/wysiwyg-editor/docs/concepts/custom/button/

```php
// config/froala-field.php
return [
    'options' => [
        'custom_elements' => [
            'froala/custom-elements/buttons/my-custom-button.js',
        ],
    ],
];
```

```js
// public/froala/custom-elements/buttons/my-custom-button.js
(function (FroalaEditor) {
    FroalaEditor.RegisterCommand('MyCustomButton', {
        // ...
    });
});
```
