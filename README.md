<!DOCTYPE html>
<html>
    <head>
           <title>Ingreso a la biblioteca</title> 
           <link rel="stylesheet" href="web.css">
    </head>
    <style>
        body{ background: #f7f1e3 }

h1,h3,#centrado{ text-align: center; } 

div{ margin-bottom: 18px; } 

.espaciado{ margin-right: 18px; } 

form{ margin-bottom: 310px; }

h2{ position: relative; text-align: center; bottom: 470px; font-size: 90px } 

p{ position: relative; bottom: 300px; }

</style>
    
    <form action="" id = "centrado"  method="get" name = "formulario">
    
        <h1>Registra tus datos</h1>

        <div>
        <label for="">Nombre</label>
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
    
        <input type="submit" id = "enviar" name = "enviar" value = "Registrarse">
    
      
        <h2 id = "registroCompleto"></h2>
    
      </form>

      <script>
      
            var mes = new Date();
            document.write(mes.getMonth()+1 + "/");
            
            var dia = new Date(); document.write(dia.getDate() + "/");
            
            var año = new Date(); document.write(año.getFullYear());
            
            var hora = new Date(); document.write(" " + hora.getHours())
            
            var minutos = new Date(); document.write(":" + minutos.getMinutes())
            
                var formulario = document.getElementsByName("formulario")[0],
                    el = formulario.elements,
                    boton = document.getElementsByName("enviar");
            
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
             var validarEscolaridad = function(e){
                 if(formulario.escol[1].checked == true && formulario.escol[2].checked == true || (formulario.escol[1].checked == true && formulario.escol[3].checked == true) || 
                 (formulario.escol[2].checked == true && formulario.escol[3].checked == true) || (formulario.escol[1].checked == true && formulario.escol[4].checked == true) || 
                 (formulario.escol[4].checked == true && formulario.escol[5].checked == true) || (formulario.escol[1].checked == true && formulario.escol[5].checked == true) || 
                 (formulario.escol[1].checked == true && formulario.esco[6].checked == true) || (formulario.escol[2].checked == true && formulario.escol[4].checked == true) || 
                 (formulario.escol[2].checked == true && formulario.escol[5].checked == true) || (formulario.escol[2].checked == true && formulario[6].escol.checked == true) || 
                 (formulario.escol[3].checked == true && formulario.escol[4].checked == true) || (formulario.escol[3].checked == true && formulario[5].escol.checked == true) || 
                 (formulario.escol[4].checked == true && formulario.escol[6].checked == true) || (formulario.escol[3].checked == true && formulario[6].escol.checked == true) || 
                 (formulario.escol[5].checked == true && formulario.escol[6].checked == true) || (formulario.escol[1].checked == false && formulario.escol[2].checked == false && 
                 formulario.escol[3].checked == false && formulario.escol[4].checked == false && formulario.escol[5].checked == false && formulario.escol[6].checked == false) || 
                 (formulario.escol[1].checked == true && formulario.escol[2].checked == true && formulario.escol[3].checked == true && formulario.escol[4].checked == true && 
                 formulario.escol[5].checked == true && formulario.escol[6].checked == true)){
                    alert("Ingresa una escolaridad válida por favor")
                 }
                 e.preventDefault();
             }

            
             var validar = function(e){
            
                validarNombre(e);
                validarEdad(e);
                validarEscolaridad();
               
            };
            
            formulario.addEventListener("submit", validar);
            }())
            </script>

      
      </html>
