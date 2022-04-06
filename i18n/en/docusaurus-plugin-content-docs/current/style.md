---
sidebar_position: 20
---

# Example style
### Custom body width
```html
<style>
  @media screen and (min-width: 62em) {
    .root-box {
      width: 1300px !important;
    }
  }
</style>
```

### No box-shadow
```html
<style>
.chakra-ui-light{
  background-color: #edddfd;
}
.main-box {
  border-radius: 15px !important;
  box-shadow: unset !important;
}
.chakra-ui-light .main-box {
  background-color: rgba(255,255,255,0.9) !important;
}
.chakra-ui-light .readme-box {
  background-color: rgba(255,255,255,0.9) !important;
}
.readme-box {
  border-radius: 15px !important;
  box-shadow: unset !important;
}
</style>
```
### Imitation 大白 style
```html
<style>
.chakra-ui-light{
   background-image: linear-gradient(120deg,#e0c3fc 0%,#8ec5fc 100%) !important;
   background-attachment: fixed;
}
.main-box {
   border-radius: 15px !important;
}
.chakra-ui-light .main-box {
   background-color: white !important;
}
.chakra-ui-light .readme-box {
   background-color: white !important;
}
.readme-box {
   border-radius: 15px !important;
}
</style>
```
:::tip
If you have a good-looking style you want to share, you can click [Edit this page](https://github.com/Xhofe/alist-doc/edit/main/docs/style.md) to initiate a pr to share your The style is added to this page.
:::