![Visitor](https://visitor-badge.laobi.icu/badge?page_id=PineAppleGrits.liveworksheets-script)
# liveworksheets-script
Script to get the answer into liveworksheets excercises

### Scripts
```js
function rtas(contenidojson) {
    var c = JSON.parse(contenidojson)
    for (let i = 0; i < c.length; i++) {
        var r = c[i][0]
        if (r.includes('/')) {
            r = r.replace('choose:', '')
            if (r.includes('/*')) {
                r = r.split("/*").pop();
            } else {
                r = r.split('/')[0];
                r = r.replace('*', '')
            }

        }
        console.log(`${i} ${r}\n`)
    }
}
rtas(contenidojson)
```

### Como usar?
* Abrir la consola de inspeccionar pagina con F12
* Insertar el codigo y presionar enter.
Informacion:
Cuando haya una lista de select:yes/no va dependiendo el orden de los botones leyendo de izquierda a derecha y de abajo hacia arriba en order de aparicion.

Por ejemplo `select:no select:yes` (En este caso la correcta seria la 2)

opcion1/**opcion2**
