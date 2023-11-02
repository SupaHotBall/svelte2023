<script>
    let regularImageUrl = '';
  
    // Define the query parameters for the Unsplash API request
    const query = 'anime'; // You can adjust the query as needed
    const clientId = 'U3Yj9H-A7xjn37lRamx6_TA0X0hBrpmVhWEHASXf7yc'; // Replace with your actual API key
  
    // Construct the API request URL
    const apiUrl = `https://api.unsplash.com/search/photos?query=${query}`;
  
    // Fetch the data and update the regularImageUrl
    fetch(apiUrl, {
      method: 'GET',
      headers: {
        'Authorization': `Client-ID ${clientId}`
      }
    })
    .then(response => {
      if (response.ok) {
        return response.json();
      } else {
        throw new Error('API request failed');
      }
    })
    .then(data => {
      if (data && data.results && data.results.length > 0) {
        regularImageUrl = data.results[0].urls.regular;
      } else {
        console.error('No results found in the API response.');
      }
    })
    .catch(error => {
      console.error('Error fetching data:', error);
    });
  </script>



<div class="about-page">
    <h1>About Page</h1>
    <!-- Display the regular-sized image -->
    <img src={regularImageUrl} alt="Anime Background" />
    <p>Your about page content goes here...</p>
  </div>
  In this modified code, we initialize the regularImageUrl variable to an empty string and then update it with the URL of the regular-sized image from the API response. We use an <img> element to display the image on your About page.
  
  
  
  
  
  
