<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Galeria BSCMC.PL</title>
<style>
  body {
    font-family: 'Segoe UI', Tahoma, sans-serif;
    background: #111;
    color: #fff;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0;
    padding: 20px;
  }

  h1 {
    margin-bottom: 30px;
    text-transform: uppercase;
    letter-spacing: 5px;
    color: #ff00ff;
  }

  .gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    max-width: 1000px;
  }

  .gallery img {
    width: 300px;
    height: auto;
    border-radius: 15px;
    box-shadow: 0 0 20px #ff00ff;
    transition: transform 0.3s, box-shadow 0.3s;
    cursor: pointer;
  }

  .gallery img:hover {
    transform: scale(1.05);
    box-shadow: 0 0 30px #00ffff;
  }

  /* Modal */
  .modal {
    display: none;
    position: fixed;
    z-index: 20;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.9);
    justify-content: center;
    align-items: center;
  }

  .modal img {
    max-width: 90%;
    max-height: 90%;
    border-radius: 15px;
  }

  .close-modal {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 40px;
    color: #fff;
    cursor: pointer;
  }
</style>
</head>
<body>

<h1>Galeria BSCMC.PL</h1>

<div class="gallery">
  <img src="https://i.postimg.cc/MTcG3W0c/amongus.png" alt="Among Us">
  <img src="https://postimg.cc/hf5BVd52" alt="Post Image 2">
  <img src="https://i.postimg.cc/vBbfxx5r/igrzyska.png" alt="Igrzyska">
</div>

<!-- Modal -->
<div class="modal" id="modal">
  <span class="close-modal" id="closeModal">&times;</span>
  <img id="modalImg" src="">
</div>

<script>
  const galleryImages = document.querySelectorAll('.gallery img');
  const modal = document.getElementById('modal');
  const modalImg = document.getElementById('modalImg');
  const closeModal = document.getElementById('closeModal');

  galleryImages.forEach(img => {
    img.addEventListener('click', () => {
      modal.style.display = 'flex';
      modalImg.src = img.src;
    });
  });

  closeModal.addEventListener('click', () => {
    modal.style.display = 'none';
    modalImg.src = '';
  });

  // Zamknięcie modala po kliknięciu poza obraz
  modal.addEventListener('click', (e) => {
    if(e.target === modal) {
      modal.style.display = 'none';
      modalImg.src = '';
    }
  });
</script>

</body>
</html>
