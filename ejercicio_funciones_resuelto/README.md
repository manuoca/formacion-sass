# FUNCIONES - SASS

### Vamos a crear una función para poder escribir nuestos line-height en porcentajes sabiendo las medidas en píxeles de line-height y font-size. Supongamos que tenemos un párrafo con la fuente a 18px y 24px de alto de línea.

```scss
@function lh($lineHeight, $fontSize) {
  @return ($lineHeight * 100% / $fontSize);
}
p {
  font-size: 18px;
  line-height: lh(24, 18);
}
```

#### Y generará:

```scss
p {
  font-size: 18px;
  line-height: 133.33%;
}
```
