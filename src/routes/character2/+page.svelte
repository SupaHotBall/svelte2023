<script>
  let videoIndex = 0;

  function scrollRight() {
    videoIndex++;
    if (videoIndex >= 2) { // Adjust this based on the number of videos
      videoIndex = 2;
    }
  }

  function scrollLeft() {
    videoIndex--;
    if (videoIndex < 0) {
      videoIndex = 0;
    }
  }

  function getVideoUrl(index) {
    const videoUrls = [
      "https://www.youtube.com/embed/SWRUnpHU7yw?si=iDvFC-NWi_sP7IHr",
      "https://www.youtube.com/embed/MohkTXPEsc8?si=TNERoCYUgteP-3NC",
      "https://www.youtube.com/embed/R1cfvvj1vr0?si=c3PoFV6BvyiNkxfW",
      "https://www.youtube.com/embed/uCkrWgvovY8?si=9cEwjnxDxnitdFKQ"
    ];

    if (index >= 0 && index < videoUrls.length) {
      return videoUrls[index];
    } else {
      return ""; // Return an empty URL for invalid indices
    }
  }
</script>



<div class="Ryomen-page-background">
  <div class="Name">
    <h1>Ryomen</h1>
    <h1>Sukuna</h1>
  </div>

  <div class="Video-container">
    <button class="left-button">
      <i class="fa-solid fa-circle-arrow-left fa-xl" />
    </button>
  </div>
</div>
