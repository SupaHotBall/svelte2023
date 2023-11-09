<script>
  let regularImageUrl = "";

  // Define the query parameters for the Unsplash API request
  const query = "anime";
  const clientId = "U3Yj9H-A7xjn37lRamx6_TA0X0hBrpmVhWEHASXf7yc"; // Replace with your actual API key

  // Construct the API request URL
  const apiUrl = `https://api.unsplash.com/search/photos?query=${query}`;

  // Fetch the data and update the regularImageUrl
  fetch(apiUrl, {
    method: "GET",
    headers: {
      Authorization: `Client-ID ${clientId}`,
    },
  })
    .then((response) => {
      if (response.ok) {
        return response.json();
      } else {
        throw new Error("API request failed");
      }
    })
    .then((data) => {
      if (data && data.results && data.results.length > 0) {
        regularImageUrl = data.results[0].urls.regular;
      } else {
        console.error("No results found in the API response.");
      }
    })
    .catch((error) => {
      console.error("Error fetching data:", error);
    });
</script>

<div class="about-page">
  <h1>About Page</h1>
  <!-- Display the regular-sized image -->
  <div class="About-Page-Background">
    <div class="fetch-background">
      <img src={regularImageUrl} alt="Anime Background" />
    </div>
  </div>
</div>
