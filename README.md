<!DOCTYPE html>
<head>
    <title>Ingreso a la biblioteca</title>
    
</head>
<style>
body{
    background: #f7f1e3
}

h1,h3,#centrado{
    text-align: center;
}
div{
    margin-bottom: 18px;
}
.espaciado{
    margin-right: 18px;
}
form{
    margin-bottom: 310px;
}
h2{
    position: relative;
    text-align: center;
    bottom: 470px;
    font-size: 90px
}
p{
    position: relative;
    bottom: 300px;
}
</style>
<body>

        

    <form action="" id = "centrado"  method="get" name = "formulario">

            <h2>¡Registrado!</h2>

        <h1>Registra tus datos</h1>
        <link rel="stylesheet" href="web.css">
     

        <div class="validar">
        <label for="" name = "nombre">Nombre</label>
        <input type="text" name = "nombre">
        </div>

        <div>
        <label for="" class="espaciado" name = "edad">Edad</label>
        <input type="number" name = "edad">
        </div>

        <div>
        <label for="" name = "sexo">Sexo</label>
        <select name="sexo">
            <option>Hombre</option>
            <option>Mujer</option>>
        </select>
        </div>


        <h3>Escolaridad</h3>
        <div>
            <input type="checkbox" name = "escol">
            <label for="" >Personas con discapacidad</label>
        </div>
        <div>
            <input type="checkbox" name = "escol">
            <label for="" >Preescolar</label>
        </div>

        <div>
        <input type="checkbox" name = "escol">
        <label for="" >Primaria</label>
        </div>

        <div>
        <input type="checkbox" name = "escol">
        <label for="" >Secundaria</label>
        </div>

        <div>
        <input type="checkbox" name = "escol">
        <label for="" >Preparatoria</label>
        </div>

         <div>
        <input type="checkbox" name = "escol">
        <label for="" >Licienciatura</label>
         </div>

        <div>
        <input type="checkbox" name = "escol">
        <label for="" >Posgrado</label>
        </div>

        <input type="submit" id = "enviar" name = "enviar">

      
        <h2 id = "registroCompleto"></h2>
  
      </form>
      <script src="web.js" language="javascript" type="text/javascript"></script>
      
      <script>
       var mes = new Date();
document.write(mes.getMonth()+1 + "/");

var dia = new Date();
document.write(dia.getDate() + "/");

var año = new Date();
document.write(año.getFullYear());

var hora = new Date();
document.write("    " + hora.getHours())

var minutos = new Date();
document.write(":" + minutos.getMinutes())




        var formulario = document.getElementsByName("formulario")[0],
            el = formulario.elements,
            boton = document.getElementById("enviar");

            var oneNumber = {

        "one"   : [formulario.escol[1].checked],
        "two"   : [formulario.escol[2].checked],
        "three" : [formulario.escol[3].checked],
        "for"   : [formulario.escol[4].checked],
        "five"  : [formulario.escol[5].checked],
        "six"   : [formulario.escol[6].checked]
        }

            var  twoNumbers = {
        //one
        "oneTwo"   : [formulario.escol[1].checked + formulario.escol[2].checked],
        "oneThree" : [formulario.escol[1].checked + formulario.escol[3].checked],
        "oneFor"   : [formulario.escol[1].checked + formulario.escol[4].checked],
        "oneFive"  : [formulario.escol[1].checked + formulario.escol[5].checked],
        "oneSix"   : [formulario.escol[1].checked + formulario.escol[6].checked],
        //two
        "twoThree" : [formulario.escol[2].checked + formulario.escol[3].checked],
        "twoFor"   : [formulario.escol[2].checked + formulario.escol[4].checked],
        "twoFive"  : [formulario.escol[2].checked + formulario.escol[5].checked],
        "twoSix"   : [formulario.escol[2].checked + formulario.escol[6].checked],
        //three
        "threeFor" : [formulario.escol[3].checked + formulario.escol[4].checked],
        "threeFive": [formulario.escol[3].checked + formulario.escol[5].checked],
        "threeSix" : [formulario.escol[3].checked + formulario.escol[6].checked],
        //for
        "forFive"  : [formulario.escol[4].checked + formulario.escol[5].checked],
        "forSix"   : [formulario.escol[4].checked + formulario.escol[6].checked],
        //five
        "fiveSix"  : [formulario.escol[5].checked + formulario.escol[6].checked]

        }

        var threeNumbers = {
                                        //one

            //oneTwo
            /*
            Esto ya lo tenemos cubierto con la propiedad "oneTwo"
            del objeto twoNumbers ya que si seleccionamos tan solo uno y dos
            tendremos el error.
            */
    
            //oneThree
            "oneThreeFor" : [formulario.escol[1].checked + formulario.escol[3].checked + formulario.escol[4].checked],
            "oneThreeFive": [formulario.escol[1].checked + formulario.escol[3].checked + formulario.escol[5].checked],
            "oneThreeSix" : [formulario.escol[1].checked + formulario.escol[3].checked + formulario.escol[6].checked],
            //oneFor
            "oneForFive"  : [formulario.escol[1].checked + formulario.escol[4].checked + formulario.escol[5].checked],
            "oneForSix"   : [formulario.escol[1].checked + formulario.escol[4].checked + formulario.escol[6].checked],
            //oneFive
            "oneFiveSix"  : [formulario.escol[1].checked + formulario.escol[5].checked + formulario.escol[6].checked],
                                            //two
            //twoThree
            /*
            Esto ya lo tenemos cubierto con la propiedad "twoThree"
            del objeto twoNumbers ya que si seleccionamos tan solo dos y tres
            tendremos el error.
            */
           
            //twoFor
            "twoForFive"  : [formulario.escol[2].checked + formulario.escol[4].checked + formulario.escol[5].checked],
            "twoForSix"   : [formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[6].checked],
            //twoFive    
            "twoFiveSix"  : [formulario.escol[2].checked + formulario.escol[5].checked + formulario.escol[6].checked],
                                            //three
            //threeFor
            "threeFiveSix": [formulario.escol[3].checked + formulario.escol[5].checked + formulario.escol[6].checked],
                                            //for
            //forFive
            "forFiveSix"  : [formulario.escol[4].checked + formulario.escol[5].checked + formulario.escol[6].checked]
        } 

        var forNumbers = {
            "oneTwoThreeFor" : [formulario.escol[1].checked + formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[4].checked],
            "oneTwoThreeFive": [formulario.escol[1].checked + formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[5].checked],
            "oneTwoThreeSix" : [formulario.escol[1].checked + formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[6].checked],
            "twoThreeForFive": [formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[4].checked + formulario.escol[5].checked],
            "twoThreeForSix" : [formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[4].checked + formulario.escol[6].checked],
            "threeForFiveSix": [formulario.escol[3].checked + formulario.escol[4].checked + formulario.escol[5].checked + formulario.escol[6].checked]
        }
        var fiveNumbers  = {
            "oneTwoThreeForFive" : [formulario.escol[1].checked + formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[4].checked + formulario.escol[5].checked],
            "oneTwoThreeForSix"  : [formulario.escol[1].checked + formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[4].checked + formulario.escol[6].checked],
            "oneTwoThreeFiveSix" : [formulario.escol[1].checked + formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[5].checked + formulario.escol[6].checked],
            "oneThreeForFiveSix" : [formulario.escol[1].checked + formulario.escol[3].checked + formulario.escol[4].checked + formulario.escol[5].checked + formulario.escol[6].checked]
        }
        var sixNumbers = {
            "oneTwoThreeForFiveSix" : [formulario.escol[1].checked + formulario.escol[2].checked + formulario.escol[3].checked + formulario.escol[4].checked + formulario.escol[5].checked + formulario.escol[6].checked]
        }

(function(){
   

     var enviado = document.getElementById("registroCompleto");

     var validarNombre = function(e){
        if(formulario.nombre.value == 0){
        alert("Ingresa tu nombre por favor")
        }
        e.preventDefault();
     };
     var validarEdad = function(e){
        if(formulario.edad.value <= 0){
            alert("Ingresa tu edad por favor")
        }
        e.preventDefault();
     }
     console.log(twoNumbers.twoThree);

     var validarEscolaridad = function(e){
         if(twoNumbers.oneTwo[0] === 1){}
         else if(twoNumbers.twoThree[0] === 1){}
         else if(twoNumbers.threeFor[0] === 1){} 
         else if(twoNumbers.forFive[0] === 1){}
         else if(twoNumbers.fiveSix[0] === 1){}
         else if(twoNumbers.oneThree[0] === 1){}
         else if(twoNumbers.oneFor[0] === 1){}
         else if(twoNumbers.oneFive[0] === 1 || twoNumbers.oneSix[0] === 1){}
         else if(twoNumbers.twoFor[0] === 1 || twoNumbers.twoFive[0] === 1 || twoNumbers.twoSix[0] === 1){}
         else if(twoNumbers.threeFive[0] === 1 || twoNumbers.threeSix[0] === 1){}
         else if(twoNumbers.forSix[0] === 1){}
         else if(oneNumber.one == false || oneNumber.two == false || oneNumber.three == false || oneNumber.for == false || oneNumber.five == false || oneNumber.six == false){
            alert("Selecciona sólo un nivel de estudios")
         }
         else{
            alert("Selecciona sólo un nivel de estudios")
         }
       
        e.preventDefault(); 
     }


    

     var ingreso = function(e){
        if (formulario.nombre.value > "0" && formulario.edad.value > 0){
            enviado.innerHTML = "¡Registrado!";
     } else {
     }
     }

     var validar = function(e){
        validarNombre(e);
        validarEdad(e);
        validarEscolaridad(e);
        ingreso(e);
    };

    formulario.addEventListener("submit", validar);
}())
      </script>

</body>
