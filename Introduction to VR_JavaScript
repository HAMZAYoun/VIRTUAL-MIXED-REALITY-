<html>
  <head>
    <title> First scene with Three.js</title>
  	<style>
   		 body{margin:0;}
    	canvas{width:100%;height:100%;}
  	</style>
    </head>
    <body>

    <script src="three.js"></script>  
    <script> 
         
          let scene = new THREE.Scene();
          let camera =new THREE.PerspectiveCamera(75,window.innerWidth/window.innerHeight,0.1,1000);
          let renderer = new THREE.WebGLRenderer();
          renderer.setSize(window.innerWidth,window.innerHeight);
          document.body.appendChild(renderer.domElement);

       // preparing things to display

        const  geometry = new THREE.SphereGeometry( 70, 32, 16 );
        const material = new THREE.MeshLambertMaterial()
       //const  material = new THREE.MeshBasicMaterial( { color: 0xffff00, transparent: true, opacity: 0.5 } );
        const  Sun = new THREE.Mesh( geometry, material );

        const  geometry2 = new THREE.SphereGeometry( 6.5, 32, 16 );
        const  material2 = new THREE.MeshBasicMaterial( { color: 0x00ff00, transparent: true, opacity: 0.5 } );
        const  earth = new THREE.Mesh( geometry2, material2 );

        const  geometry3 = new THREE.SphereGeometry( 1.7, 32, 16 );
        //const  material3 = new THREE.MeshBasicMaterial( { color: 0x808080, transparent: true, opacity: 0.5 } );
        const  material3 = new THREE.MeshLambertMaterial()
        const  moon = new THREE.Mesh( geometry3, material3 );

               // **********************************************************

       const  geometryi = new THREE.SphereGeometry( 70, 32, 16 );
        //const materiali = new THREE.MeshLambertMaterial({fog:false})
       const  materiali = new THREE.MeshBasicMaterial( { color: 0xffff00, transparent: true, visible:true } );
        const  Suni = new THREE.Mesh( geometryi, materiali );

        const  geometry2i = new THREE.SphereGeometry( 6.5, 32, 16 );
        const  material2i = new THREE.MeshBasicMaterial( { color: 0x00ff00, transparent: true, opacity: 0.5} );
        const  earthi = new THREE.Mesh( geometry2i, material2i );

        const  geometry3i = new THREE.SphereGeometry( 1.7, 32, 16 );
        //const  material3 = new THREE.MeshBasicMaterial( { color: 0x808080, transparent: true, opacity: 0.5 } );
        const  material3i = new THREE.MeshLambertMaterial()
        const  mooni = new THREE.Mesh( geometry3i, material3i );
       
	      
       

        // Rotation planets initialization
        const  turningpoint = new THREE.Object3D();
        turningpoint.add(earth);   
        turningpoint.add(moon);
        const  turningpointi = new THREE.Object3D();
        turningpointi.add(earthi);   
        turningpointi.add(mooni);

       // Adding scenes
       scene.add(camera);         // Fixed camera
        scene.add(Sun);            // Fixed sun
        scene.add(turningpoint);   // Fixed rotation point
        scene.add(turningpointi);
        scene.add(Suni);   
    



        turningpoint.position.x=300;
        Sun.position.x = 300;
        earth.position.x = 190;
        moon.position.x = 200;
        turningpointi.position.x=-400;
        Suni.position.x = -400;
        earthi.position.x = -200;
        mooni.position.x = -150;
        // Camera position
        camera.position.z=500;

        // Adding a spot light since we are working with lambert material.
        var spotLight = new THREE.SpotLight(0xffffff);
        spotLight.position.set(200, 400, 300);
        scene.add(spotLight);
        // Adding a render function
        function render(time)
        
        {
          turningpoint.rotation.y=Math.PI/30000*time;
          turningpoint.rotation.y=Math.PI/6000*time+Math.PI/30000*time;
          turningpointi.rotation.y=Math.PI/30000*time;
          turningpointi.rotation.y=Math.PI/6000*time+Math.PI/30000*time;
          renderer.render(scene,camera);
        }
          renderer.setAnimationLoop(render);
          //renderer.setClearColor (new THREE.Color( 0x00fffff), 0.5 );


         // const texture = new THREE.TextureLoader().load("file:///D:/playg/threejsdev/galaxy.jpg");
         // texture.wrapS = THREE.RepeatWrapping;
          //texture.wrapT = THREE.RepeatWrapping;


         let myKeyboardHandler = function ( keyEvent) {
         alert("key"+keyEvent.keyCode+"has been pressed.");}
         window.onekeydown=myKeyboardHandler;



     </script>
    </body>
</html>
