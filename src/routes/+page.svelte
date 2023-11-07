<script>
  import { onMount } from 'svelte';

  let player;
  let showVideo;

  onMount(() => {
    // Load the YouTube iframe API when the component is mounted
    const script = document.createElement('script');
    script.src = 'https://www.youtube.com/iframe_api';
    document.body.appendChild(script);

    script.onload = () => {
      window.onYouTubeIframeAPIReady = () => {
        player = new YT.Player('player', {
          height: '315', // Adjust to your desired height
          width: '560',  // Adjust to your desired width
          videoId: 'PKHQuQF1S8k', // Replace with your video ID
          events: {
            'onReady': onPlayerReady,
          },
        });
      };
    };
    showVideo =true;
  });

  // Function to start playing the video when it's ready
  function onPlayerReady(event) {
    event.target.playVideo();
    showVideo = true;
  }

  // Function to close the video
  function closeVideo() {
    player.stopVideo();
    showVideo = false;
  }

  function handleEscapeKey(event){
    if (event.key === 'Escape' && showVideo) {
      event.preventDefault();
    }
  }

  function preventEscapeDefault(event) {
    if (event.key === 'Escape' && showVideo) {
      event.preventDefault();
    }
  }
  console.log(showVideo)
  // Add event listeners to the document
  onMount(() => {
    document.addEventListener('keydown', handleEscapeKey);
    document.addEventListener('keydown', preventEscapeDefault);
  });

</script>

<div class="HomePagebase-background">
  <div class="body-image"></div>
</div>

<div id="container">
  {#if showVideo}
    <div id="player"></div>
    <div class="close-button" on:click={closeVideo}>Close</div>
  {/if}
</div>
