# lcperez
estudiante

// ESCENA GRAB
dejar escena =  documento . querySelector ( ` una escena ' );
 escena  const =  documento . querySelector ( ' una escena ' )
const  sky  =  documento . querySelector ( ' a-sky ' )
const  objectContainer  =  documento . querySelector ( ' # object-container ' )

// SET CONTENEDOR
let objectContainer =  documento . createElement ( ` una entidad ' );
objectContainer . setAttribute ( ` posición ` , ` 0 1,6 -2 ` );
objectContainer . setAttribute ( ` escala ` , ` 0.4 0.4 0.4 ` );
escena . appendChild (objectContainer);

// FUNCIÓN DE COLOR AL AZAR
función  getRandomColor () {
  let randomColor =  Math . floor ( Math . random () * ( 16777215 - 600000 + 1 ) + 600000 ). toString ( 16 );
  // let randomColor = Math.floor (Math.random () * 16777215) .toString (16);
  return randomColor;
}

// FUNCIÓN DE NÚMERO ALEATORIO
función  getRandomnumber () {
  let randomNumber =  Math . piso ( Math . random () * ( 30 - 10 + 1 ) + 10 );
  return randomNumber;
función  getRandomNumber ( x , y ) {
  volver  matemáticas . floor ( Math . random () * x + y)
}

// ESTABLECER CANTIDAD DE ELEMENTOS
let totalSteps =  getRandomnumber ();
let totalRotations =  getRandomnumber ();

// SET LUCES
let sceneSky =  documento . createElement ( ` a-cielo ` );
sceneSky . setAttribute ( ` del color ' , ` # $ { getRandomColor () } ' );
sceneSky . setAttribute ( ` animation__color ` , ` propiedad: color, dir: alternas; dur: 2000; aliviando: easeInOutSine; bucle: verdadera; a: # $ { getRandomColor () } ' );
escena . appendChild (sceneSky);
const  totalSteps  =  getRandomNumber ( 17 , 10 )
const  totalRotations  =  getRandomNumber ( 17 , 10 )

let ambientLight =  documento . createElement ( ` a-luz ` );
ambientLight . setAttribute ( ` Identificación del ` , ` theAmbientLight ` );
ambientLight . setAttribute ( ` escriba ` , ` ambiente ` );
ambientLight . setAttribute ( ` intensidad ` , ` 0.7 ' );
ambientLight . setAttribute ( ` del color ` , ` #FFFFFF ` );
escena . appendChild (ambientLight);

let light1 =  documento . createElement ( ` a-luz ` );
luz1 . setAttribute ( ` Identificación del ` , ` blueToRedLight ` );
luz1 . setAttribute ( ` del color ' , ` # 0000FF ' );
luz1 . setAttribute ( ` intensidad ` , ` 3 ' );
luz1 . setAttribute ( ` posición ` , ` -5,72 6,65 0,80 ` );
luz1 . setAttribute ( ` animation__color ` , ` propiedad: color, dir: alterna; dur: 2000; aliviando: easeInOutSine; bucle: true; a: # FF0000 ` );
luz1 . setAttribute ( ` alongpath ` , ` ruta: 10,10, -10 -20,10, -10 10,0, -10; cerrado: true; dur: 12000; ` );
escena . appendChild (light1);
función  getRandomColor () {
  const  letters  =  ' 0123456789abcdef '
  let randomColor =  ' '
  para ( sea i =  0 ; i <  6 ; i ++ ) {
    randomColor + = letras [ Math . piso ( Math . random () *  16 )]
  }
  return randomColor
}

let light2 =  documento . createElement ( ` a-luz ` );
luz2 . setAttribute ( ` Identificación del ` , ` blueToRedLight ` );
luz2 . setAttribute ( ` del color ' , ` # FF0000 ' );
luz2 . setAttribute ( ` intensidad ` , ` 5 ` );
luz2 . setAttribute ( ` posición ` , ` 8,60 6,65 0,80 ` );
luz2 . setAttribute ( ` animation__color ` , ` propiedad: color, dir: alterna; dur: 2000; aliviando: easeInOutSine; bucle: true; a: # 0000FF ` );
luz2 . setAttribute ( ` alongpath ` , ` ruta: -2, -2,5 2, -1,5 0, -1,5; cerrado: true; dur: 3000; ` );
escena . appendChild (light2);
cielo . setAttribute ( ' color ' , ` # $ { getRandomColor () } ` )
cielo . setAttribute ( ' animation__color ' , ` property: color; dir: alternate; dur: 2000; easing: easeInOutSine; loop: true; to: # $ { getRandomColor () } ` )

// GENERAR ELEMENTOS Y AGREGARLOS A CONTENEDORES DE ROTACIÓN
for ( let i = 1 ; i <= totalRotations; i ++ ) {
  let currentRotation =  360  / totalRotations * i;
  let rotateContainer =  document . createElement ( ` una entidad ' );
  rotateContainer . setAttribute ( ` rotación ` , ` 0 0 $ { currentRotation } ' );
función  getRandomShape () {
   formas  const = [ ' esfera ' , ' octaedro ' , ' icosaedro ' , ' toro ' , ' tetraedro ' ]
  devolver formas [ Math . piso ( Math . random () *  formas . longitud )]
}

  for ( let i = 1 ; i <= totalSteps; i ++ ) {
    let circleElementContainer =  documento . createElement ( ` una entidad ' );
    circleElementContainer . setAttribute ( ` clase ' , ` circleElementContainer $ { i } ' );
    let evenDistance = i / totalSteps;
    // let evenDistance = i * 1.5 / totalSteps * i; // guarda esto para una verdadera uniformidad para los elementos
    circleElementContainer . setAttribute ( ` posición ` , ` 0 $ { evenDistance } 0 ' );
    let randomColorForThis =  getRandomColor ();
    let circleElement =  documento . createElement ( ` una entidad ' );
    circleElement . setAttribute ( ` clase ' , ` circleElement $ { i } ' );
    deje que currentSize = i / totalSteps;
    circleElement . setAttribute ( ` escala ` , ` $ { currentSize }  $ { currentSize }  $ { currentSize } ' );
    circleElement . setAttribute ( ` material de ` , ` color: # $ { randomColorForThis } ; metalness: 0; rugosidad: 0; ' );
    circleElement . setAttribute ( ` geometría ` , ` primitivo: esfera; radius: 1,5; ` );
    circleElement . setAttribute ( ` animation__yoyo ` , ` propiedad: escala; dir: alternas; dur: $ { currentSize * 10000 } ; aliviando: easeInOutSine; bucle: verdadera; a: 0 0 0 ' );
    circleElementContainer . appendChild (circleElement);
    rotateContainer . appendChild (circleElementContainer);
función  generateElements () {
  for ( let i =  1 ; i <= totalRotations; i ++ ) {
    const  currentRotation  =  360  / totalRotations * i
    const  rotateContainer  =  documento . createElement ( ' una entidad ' )
    rotateContainer . setAttribute ( ' rotación ' , ` 0 0 $ { currentRotation } ` )
    for ( let j =  1 ; j <= totalSteps; j ++ ) {
      const  evenDistance  = j / totalSteps
      const  currentSize  = j / totalSteps
      const  circleElementContainer  =  documento . createElement ( ' una entidad ' )
      circleElementContainer . setAttribute ( ' class ' , ` circleElementContainer $ { j } ` )
      circleElementContainer . setAttribute ( ' posición ' , ` 0 $ { evenDistance } 0 ' )
      const  circleElement  =  documento . createElement ( ' una entidad ' )
      circleElement . setAttribute ( ' class ' , ` circleElement $ { j } ` )
      circleElement . setAttribute ( ' scale ' , ` $ { currentSize }  $ { currentSize }  $ { currentSize } ` )
      circleElement . setAttribute ( ' materiales ' , ` color: # $ { getRandomColor () } ; metalness: 0; rugosidad: 0 ' )
      circleElement . setAttribute ( ' geometría ' , ` primitivo: $ { getRandomShape () } ; radius: 1,5 ` )
      circleElement . setAttribute ( ' animation__yoyo ' , ` propiedad: escala; dir: alternas; dur: $ { currentSize *  10000 } ; aliviando: easeInOutSine; bucle: verdadera; a: 0 0 0 ' )
      circleElementContainer . appendChild (circleElement)
      rotateContainer . appendChild (circleElementContainer)
    }
    objectContainer . appendChild (rotateContainer)
  }
  objectContainer . appendChild (rotateContainer);
}
// OBTENER VALOR PARA LA ALEATORIZACIÓN DE RUTA
función  pathValue () {
  volver  matemáticas . piso ( Math . random () * ( 10 * 2 + 1 ) - 10 );
}
// OBTENER DURACIÓN ALEATORIZACIÓN PARA EL CAMINO
 duración de la función () {
  volver  matemáticas . piso ( Math . random () * ( 10 - 5 + 1 ) + 5 );
}

// Agarra a cualquier otro elemento de la esfera en el anillo y altera su camino
for ( let i = 0 ; i <= totalSteps; i ++ ) {
  let circleRing =  documento . getElementsByClassName ( ` circleElement $ { i } ` );

      let valueOne =  pathValue ()
      let valueTwo =  pathValue ()
      let randomDuration =  duración ()

    for ( let i = 0 ; i < circleRing . length ; i ++ ) {
      si (i % 2  ==  0 ) {
      anillo circular [i]. setAttribute ( ` alongpath ` , ` ruta: 0,0,0 $ { valueOne } , $ { valueTwo } , $ { valueOne }  $ { valueTwo } , $ { valueOne } , $ { valueTwo } ; cerrado: true; dur: $ { randomDuration } 000; loop: verdadero ` );
    } más {
      anillo circular [i]. setAttribute ( ` alongpath ` , ` ruta: 0,0,0 $ { valueTwo } , $ { valueOne } , $ { valueTwo }  $ { valueOne } , $ { valueTwo } , $ { valueOne } ; cerrado: true; dur: $ { randomDuration } 000; loop: verdadero ` );
función  alterEveryOtherPath () {
  for ( let i =  0 ; i <= totalSteps; i ++ ) {
    let circleRing =  documento . getElementsByClassName ( ` circleElement $ { i } ` )
    let valueOne =  getRandomNumber ( 21 , - 10 )
    let valueTwo =  getRandomNumber ( 21 , - 10 )
    let randomDuration =  getRandomNumber ( 6 , 5 )
    for ( let j =  0 ; j <  circleRing . length ; j ++ ) {
      if (j %  2  ==  0 ) {
        circleRing [j]. setAttribute ( ' alongpath ' , ` ruta: 0,0,0 $ { valueOne } , $ { valueTwo } , $ { valueOne }  $ { valueTwo } , $ { valueOne } , $ { valueTwo } ; cerrado: verdadero; dur: $ { randomDuration } 000; loop: verdadero ` )
      } más {
        circleRing [j]. setAttribute ( ' alongpath ' , ` ruta: 0,0,0 $ { valueTwo } , $ { valueOne } , $ { valueTwo }  $ { valueOne } , $ { valueTwo } , $ { valueOne } ; cerrado: verdadero; dur: $ { randomDuration } 000; loop: verdadero ` )
      }
    }
  }
}

// TODO: arregla getRandomColor para generar solo valores hexadecimales válidos
// TODO: SECA las funciones de aleatorización. Sintiendo que tengo demasiados
// TODO: encapsula la lógica para minimizar las variables globales 
generateElements ()
alterEveryOtherPath ()
    
