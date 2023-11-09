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
      "https://www.youtube.com/embed/sy1Kdw1V0r0?si=r1rXZ0-II6G9EOvU",
      "https://www.youtube.com/embed/UeOTYQwlUtA?si=ckft7GhTAi5IqG7v",
      "https://www.youtube.com/embed/2V_O7lH3NRQ?si=8wTra3DCm97Il_YG",
      "https://www.youtube.com/embed/SCAiB_AKu9U?si=e81cuSkyOAEdNOKB"
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
    <span>K</span>
    <span>E</span>
    <span>N</span>
    <span>T</span>
    <span>O</span>
    <span>N</span>
    <span>A</span>
    <span>N</span>
    <span>A</span>
    <span>M</span>
    <span>I</span>
  </div>

  <div class="Video-container">
    <button class="left-button">
        <i class="fa-solid fa-circle-arrow-left fa-xl"></i>
    </button>
  </div>
</div>
