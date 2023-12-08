# Three.js
Biblioteca JavaScript 3D

#### Objetivo ####

O objetivo deste projeto é criar uma biblioteca 3D leve e fácil de usar. A biblioteca oferece renderizadores Canvas 2D, SVG, CSS3D e WebGL.

### Uso ###

Faça o download da [biblioteca minificada](http://threejs.org/build/three.min.js) e inclua-a em seu HTML, ou instale e importe como um [módulo](http://threejs.org/docs/#manual/introduction/Import-via-modules).
Alternativamente, veja [como construir a biblioteca você mesmo](https://github.com/mrdoob/three.js/wiki/Build-instructions).

```html
<script src="js/three.min.js"></script>
```
Este código cria uma cena, uma câmera, e um cubo geométrico, adicionando-o à cena. Em seguida, cria um renderizador `WebGL` para a cena e a câmera, e adiciona essa viewport ao elemento document.body. Por fim, anima o cubo dentro da cena para a câmera.

```javascript
var camera, scene, renderer;
var geometry, material, mesh;

init();
animate();

function init() {

	camera = new THREE.PerspectiveCamera( 70, window.innerWidth / window.innerHeight, 0.01, 10 );
	camera.position.z = 1;

	scene = new THREE.Scene();

	geometry = new THREE.BoxGeometry( 0.2, 0.2, 0.2 );
	material = new THREE.MeshNormalMaterial();

	mesh = new THREE.Mesh( geometry, material );
	scene.add( mesh );

	renderer = new THREE.WebGLRenderer( { antialias: true } );
	renderer.setSize( window.innerWidth, window.innerHeight );
	document.body.appendChild( renderer.domElement );

}
```

## Contato
Se tiver dúvidas ou precisar de mais informações, sinta-se à vontade para entrar em contato:
- Email : [contato@daanrox.com](mailto:contato@daanrox.com)
- LinkedIn: [https://www.linkedin.com/in/daanrox/](Daanrox)

--- 

"Consagre ao Senhor tudo o que você faz, e os seus planos serão bem-sucedidos."

