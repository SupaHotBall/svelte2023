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
      "https://www.youtube.com/embed/SQc2jhbGT2k?si=1DGQq0olblMVibZ3",
      "https://www.youtube.com/embed/fueqERLu-Fk?si=Apns2jVo_RotE1GL&start=4",
      "https://www.youtube.com/embed/ia6sRyT6ArE?si=fWr3a2GfZIYFC6nb&start=4",
      "https://www.youtube.com/embed/pzIbP2AUXy8?si=SyqzzAsuVhhSISg2&start=4"
    ];

    if (index >= 0 && index < videoUrls.length) {
      return videoUrls[index];
    } else {
      return ""; // Return an empty URL for invalid indices
    }
  }
</script>

<div class="Kento-page-background">
    <div class="Name">
    <h1>Kento</h1>
    <h1>Nanami</h1>
  </div>

  <div class="Video-container">
    <button class="left-button">
        <i class="fa-solid fa-circle-arrow-left fa-xl"></i>
    </button>
  </div>
</div>
