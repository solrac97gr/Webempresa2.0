<p align="center"><a href="https://solrac97gr.github.io/web_empresa/" target="_blank" rel="noopener noreferrer">
<img src="https://solrac97gr.github.io/web_empresa/img/logo-masthead.png" alt="drawing" width="150"/></a></p>

<h2 align="center">Websigth | Closed</h2>

Web created for a small development agency that I did a while ago. It is no longer operational but I keep it with love.Interesting things I learned in this project was to connect a web form with a google form, to solve the problem of not having backend since it was hosted on github and at that time I did not know serverless.

<p align="center"><img src="https://i.imgur.com/yGG7saJ.png" width="400" /></p>

<p align="center"><img src="https://i.imgur.com/sbr8p0u.png" width="200" /><img src="https://i.imgur.com/3LvBmrH.png" width="200" /></p>

```
<form  action="https://docs.google.com/forms/d/e/1FAIpQLSf9e3A7lCqIWgWUEkxzQsDiJ9UE3f7lmGDojVBo5a3pf1ko-w/formResponse?" name="gform" id="gform" enctype="text/plain" TARGET="hidden_iframe" onsubmit="sendform()">
            <div class="row control-group">
              <div class="form-group col-12 floating-label-form-group controls">
                <label>Nombre</label>
                <input type="text" name="entry.1681272265" class="form-control" placeholder="Nombre" id="name" required="required" data-validation-required-message="Ingresa tu nombre.">
                <p class="help-block text-danger"></p>
              </div>
            </div>
            <div class="row control-group">
              <div class="form-group col-12 floating-label-form-group controls">
                <label>Email</label>
                <input type="email" name="entry.1539217499" class="form-control" placeholder="Email" id="email" required="required" data-validation-required-message="Ingresa un correo electronico">
                <p class="help-block text-danger"></p>
              </div>
            </div>
           <br>
            <div id="success"></div>
            <div class="row text-center" >
              <div class="form-group col-12">

                <button type="submit" id="BotonEnviar" value="submit"  style="margin: 15px;padding-top: 12px;padding-bottom: 12px" class="btn btn-outline-dark">Contáctenme</button>
                <a class="btn btn-outline-dark js-scroll-trigger text-center"  style="margin: 15px" onclick="gtag('event', 'evento', { 'event_category': 'categoria', 'event_action': 'accion', 'event_label': 'wapp', 'value': 'valor'});" target="_blank" href="https://api.whatsapp.com/send?phone=51939169253&text=Hola, me pueden dar información ">Escríbenos a whatsapp</a>
              </div>
              </div>
             </div>
          </form>
          <iframe name="hidden_iframe" id="hidden_iframe" style="display:none;" onload="if(submitted) {}"></iframe>
```
          

```javascript
var submitted=false;
$('#gform').on('submit', function(e) {
    $('#gform *').fadeOut(2000);
    $('#gform').prepend('Solicitud Enviada');
    $('#gform *').fadeIn(5000);
    fbq('track', 'CompleteRegistration');
  });
  $( '#BotonEnviar' ).click(function() {
    fbq('track', 'CompleteRegistration');
    console.log('funciona')
```
