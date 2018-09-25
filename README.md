# core.loader.types

load types from plugin definition

```js
let core = new require('core.constructor')();
 
core.plugin(
    require('core.plugin.type'),
    require('core.loader.types')
);

// plugins can now declare types on the plugin definition object:
core.plugin({
    name: 'test',
    types: [
        {
            name: 'someType',
            schema: [
                {
                    key: 'name',
                    type: 'string',
                    description: 'The name of the instance',
                    isRequired: true
                }
            ]
        }
    ]
});
 
core.types.test;
```
