# portfolio-2024
## beta version with web components

-custom Elements with ES Modules

-later: with svelte maybe

-ventana en beta,falta drag and drop

    -❌ i trying rendering img in list item
    
    -❌ routing with errors

    -❌ aplicar estado o algo de reactividad o un signal talves,o probarlo con otro framework
    -❌ loader needed
    -❌ wrap main inside index?, similar to react
    -❌ bug in new loading ,need identify background-image inside , and fix ui
- Ejemplo de callback
  <script>
    function verificarCargaDeImagenes(callback) {
      const images = document.querySelectorAll("img");
      let loadedImages = 0;

      images.forEach((img) => {
        if (img.complete) {
          loadedImages++;
        } else {
          img.addEventListener("load", () => {
            loadedImages++;
            if (loadedImages === images.length) {
              callback();
            }
          });
          img.addEventListener("error", () => {
            loadedImages++;
            if (loadedImages === images.length) {
              callback();
            }
          });
        }
      });

      if (loadedImages === images.length) {
        callback();
      }
    }

    verificarCargaDeImagenes(() => {
      document.getElementById("loading").style.display = "none";
      document.getElementById("content").style.display = "block";
    });
  </script>


    -✅ web component aplyed

    -✅ filosofiá aplicada aquí: si es repetitivo,se puede automatizar.
    
### beta version 0.002

. ✅ methodo beta para mapear links de un objeto realizado,falta documentarlo
