# mygallry
Gallery of pictures an a web site
File HTML:
<!-- <-------HTML--------->  
 <!DOCTYPE html>  
 <html lang="en">  
 <head>  
  <title>Galeria de Imagenes</title>  
  <meta charset="utf-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1">  
  <link rel="stylesheet" href="migaleria.css">  
 </head>  
 <body>  
 <section class="gallery">  
      <div class="container">  
           <div class="row">  
                <div class="gallery-filter">  
                     <span class="filter-item active" data-filter="all">All</span>  
                     <span class="filter-item" data-filter="shoe">Shoe</span>  
                     <span class="filter-item" data-filter="headphone">Headphone</span>  
                     <span class="filter-item" data-filter="camera">Camera</span>  
                </div>  
           </div>  
           <div class="row">  
                <!-- gallery item start -->  
                <div class="gallery-item shoe">  
                     <div class="gallery-item-inner">  
                          <img src="https://i.postimg.cc/7PJ4yYHh/revolt-164-6w-VEHf-I-unsplash.jpg" alt="shoe">  
                     </div>  
                </div>  
                <!-- gallery item end -->               <!-- gallery item start -->  

                    <div class="gallery-item headphone">  
                         <div class="gallery-item-inner">  
                              <img src="https://i.postimg.cc/zf7MT4q9/istockphoto-1289318271-170667a.jpg" alt="headphone">  
                         </div>  
                    </div>  
                    <!-- gallery item end -->  
                    <!-- gallery item start -->  
                    <div class="gallery-item camera">  
                         <div class="gallery-item-inner">  
                              <img src="https://i.postimg.cc/vZ7QQdMP/nordwood-themes-F3-Dde-9thd8-unsplash.jpg" alt="camera">  
                         </div>  
                    </div>  
                    <!-- gallery item end -->  
                    <!-- gallery item start -->  
                    <div class="gallery-item headphone">  
                         <div class="gallery-item-inner">  
                              <img src="https://i.postimg.cc/3xTY15HR/c-d-x-PDX-a-82obo-unsplash.jpg" alt="headphone">  
                         </div>  
                    </div>  
                    <!-- gallery item end -->  
                    <!-- gallery item start -->  
                    <div class="gallery-item camera">  
                         <div class="gallery-item-inner">  
                              <img src="https://i.postimg.cc/PrYL89TD/patrick-dozk-Vh-Dyvh-Q-unsplash.jpg" alt="camera">  
                         </div>  
                    </div>  
                    <!-- gallery item end -->  
                    <!-- gallery item start -->  
                    <div class="gallery-item headphone">  
                         <div class="gallery-item-inner">  
     <img src="https://i.postimg.cc/PqYyN2Nr/ervo-rocks-Zam8-Tv-Eg-N5o-unsplash.jpg" alt="headphone3">  
                         </div>  
                    </div>  
                    <!-- gallery item end -->  
               </div>  
          </div>  
     </section>  
     <script src="migaleria.js"></script>  
     </body>  
     </html>  
     
     File CSS:
     /*--------------CSS----------------*/  
     body{  
          line-height: 1.5;  
          font-family: 'noto-serif', serif;  
     }  
	 
	 *{  
          margin:0;  
          box-sizing: border-box;  
     }  
     .container{  
          max-width: 1180px;  
          margin:auto;  
     }  
     .row{  
          display: flex;  
          flex-wrap: wrap;  
     }  
     img{  
          max-width: 100%;  
          vertical-align: middle;  
     }  
     /*.gallery*/  
     .gallery{  
          width: 100%;  
          display: block;  
          min-height: 100vh;  
          background-color: #000000;  
          padding: 70px 0;  
     }  
     .gallery .gallery-filter{  
          padding: 0 15px;  
          width: 100%;  
          text-align: center;  
          margin-bottom: 24px;   
     }  
	 .gallery .gallery-filter .filter-item{  
          color: orange;  
          font-size: 28px;  
          text-transform: uppercase;  
          display: inline-block;  
          margin:0 30px; 
          cursor: pointer;  
          border-bottom: 2px solid transparent;  
          line-height: 2.2;  
          transition: all 0.3s ease;  
     }  
     .gallery .gallery-filter .filter-item.active{  
          colour: #ff9800;  
          border-colour: #ff9800;  
     }  
     .gallery .gallery-item{  
          width: calc(100% / 3);  
          padding: 12px;  
     }  
      .gallery .gallery-item-inner img{  
          width: 100%;  
     }  
     .gallery .gallery-item.show{  
          animation: fadeIn 0.5s ease; 
     }  
     @keyframes fadeIn{  
          0%{  
               opacity: 0;  
          }  
          100%{               
               opacity: 1;  
          }  
     }  
    .gallery .gallery-item.hide{  
          display: none;  
     }  
     /*responsive*/  
     @media(max-width: 991px){  
          .gallery .gallery-item{  
               width: 50%;  
          }  
     }  
     @media(max-width: 767px){  
       .gallery .gallery-item{  
               width: 100%;  
          }       
          .gallery .gallery-filter .filter-item{  
               margin-bottom: 30px;  /*.revisar*/ 
          }  
     }  
     
     File JS:
     // Javascript   
     const filter container = document.querySelector(".gallery-filter"),  
      galleryItems = document.querySelectorAll(".gallery-item");  
      filter container.addEventListener("click", (event) =>{  
       if(event.target.classList.contains("filter-item")){  
             // deactivate existing active 'filter-item'  
             filter container.querySelector(".active").classList.remove("active");  
             // activate new 'filter-item'  
             event.target.classList.add("active");  
             const filter value = event. target.getAttribute("data-filter");  
             galleryItems.forEach((item) =>{  
         if(item.classList.contains(filterValue) || filter value === 'all'){  
              item.classList.remove("hide");  
               item.classList.add("show");  
         }  
         else{  
              item.classList.remove("show");  
              item.classList.add("hide");  
         }  
             });  
       }  
      });  
