### ckeditor-releases
---
https://github.com/ckeditor/ckeditor-releases

```js
EditorClass
  .create( {
    toolbar: [ 'bold', 'italic' ],
    image: {
      styles: [
      ]
    }
  } )
  .then()
  .catch();
  
```

```js
( function(){
  var styles = [];
  CKEDITOR.addCss = function( css ){
    styles.push( css );
  };
  CKEDITOR.getCss = function(){
    return styles.join( '\n' );
  };
} )();

CKEDITOR.on( 'instanceDestroyed', function(){
  if( CKEDITOR.tools.is.Empty( this.instances ) )
    CKEDITOR.fire( 'reset' );
} );
CKEDITOR.loader.load( '_bootstrap' );

CKEDITOR.TRISTATE_OFF = 2;

CKEDITOR.TRISTATE_DISABLED = 0;
```

```
```


