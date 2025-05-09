# Ex.08 Design of Interactive Image Gallery
# Date:
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Interactive Photo Gallery</title>
      <style>
        body {
          font-family: Arial, sans-serif;
          background: #121212;
          color: #fff;
          margin: 0;
          padding: 20px;
        }
        h1 {
          text-align: center;
        }
        .gallery {
          display: grid;
          grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
          gap: 15px;
          padding: 20px;
        }
        .gallery-item {
          text-align: center;
        }
        .gallery img {
          width: 100%;
          border-radius: 10px;
          cursor: pointer;
          transition: transform 0.3s ease;
        }
        .gallery img:hover {
          transform: scale(1.05);
        }
        .caption {
          margin-top: 8px;
          font-size: 0.9em;
          color: #ccc;
        }
      </style>
    </head>
    <body>
      <h1>Interactive Photo Gallery</h1>
      <div class="gallery" id="gallery"></div>
    
      <script>
        const images = [
          { src: 'https://picsum.photos/400/300?random=1', caption: 'Serene mountain view' },
          { src: 'https://picsum.photos/400/300?random=2', caption: 'Urban cityscape at dusk' },
          { src: 'https://picsum.photos/400/300?random=3', caption: 'Misty forest trail' },
          { src: 'https://picsum.photos/400/300?random=4', caption: 'Sunset over the ocean' },
          { src: 'https://picsum.photos/400/300?random=5', caption: 'Snowy mountain peak' },
          { src: 'https://picsum.photos/400/300?random=6', caption: 'Golden field of wheat' }
        ];
    
        const gallery = document.getElementById('gallery');
    
        images.forEach(({ src, caption }) => {
          const container = document.createElement('div');
          container.className = 'gallery-item';
    
          const link = document.createElement('a');
          link.href = src;
          link.target = '_blank';
    
          const img = document.createElement('img');
          img.src = src;
          img.alt = caption;
    
          const captionEl = document.createElement('div');
          captionEl.className = 'caption';
          captionEl.textContent = caption;
    
          link.appendChild(img);
          container.appendChild(link);
          container.appendChild(captionEl);
          gallery.appendChild(container);
        });
      </script>
    </body>
    </html>

# OUTPUT:
![image](https://github.com/user-attachments/assets/12409739-3c3e-465f-b06c-7ac09784fc49)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
