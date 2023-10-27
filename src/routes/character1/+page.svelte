<div class="Gojo-page-background">
  <div>
    <h1>Gojo</h1>
    <h1>Satoru</h1>
  </div>

  <div class="Video-container">
    <button class="left-button">
      <i class="fa-solid fa-circle-arrow-left fa-2xl"></i>
    </button>

    <div class="video-wrapper">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/SQc2jhbGT2k?si=1DGQq0olblMVibZ3"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>

    <div class="video-wrapper">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/fueqERLu-Fk?si=Apns2jVo_RotE1GL&amp;start=4"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>

    <div class="video-wrapper">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/ia6sRyT6ArE?si=fWr3a2GfZIYFC6nb&amp;start=4"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>

    <div class="video-wrapper">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/pzIbP2AUXy8?si=SyqzzAsuVhhSISg2&amp;start=4"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>

    <button class="right-button">
      <i class="fa-solid fa-circle-arrow-right fa-2xl"></i>
    </button>
  </div>
</div>
CSS:

css
Copy code
.Gojo-page-background {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.Video-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.video-wrapper {
  margin-bottom: 20px; /* Adjust as needed to create space between videos */
}
In this code, I've wrapped each iframe in a div with the class video-wrapper. The CSS styles ensure that the videos are centered at the bottom of the .Video-container. You can adjust the margin-bottom property as needed to control the spacing between the videos.




User
how to make the left button next to the first video and right button next to the last video
ChatGPT
To place the left button next to the first video and the right button next to the last video, you can modify your HTML structure and use CSS for positioning. Here's how you can do it:

HTML:

html
Copy code
<div class="Gojo-page-background">
  <div>
    <h1>Gojo</h1>
    <h1>Satoru</h1>
  </div>

  <div class="Video-container">
    <button class="left-button">
      <i class="fa-solid fa-circle-arrow-left fa-2xl"></i>
    </button>

    <div class="video-wrapper">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/SQc2jhbGT2k?si=1DGQq0olblMVibZ3"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>

    <div class="video-wrapper">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/fueqERLu-Fk?si=Apns2jVo_RotE1GL&amp;start=4"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>

    <div class="video-wrapper">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/ia6sRyT6ArE?si=fWr3a2GfZIYFC6nb&amp;start=4"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>

    <div class="video-wrapper">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/pzIbP2AUXy8?si=SyqzzAsuVhhSISg2&amp;start=4"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>

    <button class="right-button">
      <i class="fa-solid fa-circle-arrow-right fa-2xl"></i>
    </button>
  </div>
</div>
