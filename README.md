# sspa.jquery
Simple Single Page Application with AJAX jQuery

## Usage
Add jQuery and sspa.js at the bottom of page

      <!-- jQuery Library (IMPORTANT)-->
      <script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js' crossorigin='anonymous'></script>
      <!-- SSPA JS (IMPORTANT)-->
      <script src="../dist/sspa.js"></script>
     </body>
    </html>
      
Create a div element with sspa__content class, for sspa__boot

    <div class="sspa__content">
    </div>
Create a div elemnt with sspa__boot class inside sspa__content element, this element will load content from a file u request

    <div class="sspa__content">
        <div class="sspa__boot"></div>
    </div>
    
Now create any element with the sspa__ob class, add the data-href attribute with the value of the path to the file you want to load.

    <a class="sspa__ob" href="#" data-href="load1.html">load it!</a>
It will look like this

    <!DOCTYPE html>
    <html>
      <body>
        <a class="sspa__ob" href="#" data-href="load1.html">load it!</a>
        <div class="sspa__content">
          <div class="sspa__boot"></div>
        </div>
        <!-- jQuery Library (IMPORTANT)-->
        <script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js' crossorigin='anonymous'></script>
        <!-- SSPA JS (IMPORTANT)-->
        <script src="../dist/sspa.js"></script>
      </body>
    </html>
    
## How it work
I use the load() function to load a page without refreshing

When you click on the object with data-href, the sspa__boot element will be deleted and re-create a new sspa__boot element.

After creating a new sspa_boot element, AJAX will load a page from the data-href path into the sspa__boot element, then the entire page will not need to be reloaded. 
