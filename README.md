# \<spine-tags\>

This element represents an editable list of labels.

It produces the `spine-tags-change` event upon list change.

Example:
```
<spine-tags on-spine-tags-change='handleChange'>
  <spine-tag text="TAG 1"></spine-tag>
  <spine-tag text="TAG 2"></spine-tag>
  <spine-tag text="TAG 3"></spine-tag>
</spine-tags>
```

### Controlled content

The `controlled` attribute is used to define that the element content is controlled from outside.
In that scenario, adding or removing tags does not affect the content
but only causes the `spine-tags-change` event to be fired.

For example, if it's required to bind the content to the `tags` array, use `controlled`
attribute in conjunction with `tags` array updating in the `spine-tags-change` event handler.

Example:
```
<spine-tags on-spine-tags-change='handleChange' controlled>
  <template is="dom-repeat" items="[[tags]]">
    <spine-tag text="{{item}}"></spine-tag>
  </template>
</spine-tags>
```

### Styling

The following custom mixins is available for styling:

Custom property                | Description                                   | Default
-------------------------------|-----------------------------------------------|--------
`--spine-tags-add-button`      | Mixin applied to the <paper-icon-button>      | `{}`
`--spine-tags-add-button-text` | Mixin applied to the <paper-icon-button> text | `{}`
`--spine-tags-add-button-icon` | Mixin applied to the <paper-icon-button> icon | `{}`
