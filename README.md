# vue3-draggable

simple drag&drop component for vue 3.x, with no dependencies

![vue3-drag2](https://user-images.githubusercontent.com/59331444/104086030-774ce700-5297-11eb-9f5a-211bd4b7c01f.gif)

# Features

- support v-model
- support transition
- customizable draggable component

# Installation

```
npm i vue3-draggable
```

# Usage

import component:

```javascript
import Draggable from 'vue3-draggable';

export default {
  components: {
    Draggable,
  },
};
```

template:

```vue
<draggable v-model="items" dropZoneId="1" class="drop-zone">
    <template v-slot:item="{item}">
        <!-- example -->
        <div class="draggable-item">
            {{item.title}}
        </div>
        <!-- or your own template -->
    </template>
</draggable>
```

### Props

| Name       | Required     | Type       | Description                                        |
| :--------- | :----------- | :--------- | :------------------------------------------------- |
| modelValue | REQUIRED | ARRAY  | v-model value, items to be bound <br> **each item in array should have 'id' property** <br> ex) [{id:1, title:item1}, {id:2, title: item2}]            |
| dropZoneId | REQUIRED | STRING | unique id is required for each draggable component |
| transition | OPTIONAL | STRING | transition delay in ms |
