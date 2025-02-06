function searchMap() {
    let city = document.getElementById("cityInput").value.trim().toLowerCase();
    let mapContainer = document.getElementById("mapContainer");

    if (city === "") {
        mapContainer.innerHTML = "<p>Please enter a city name.</p>";
        return;
    }

    let cityMaps = {
        "new york": "https://upload.wikimedia.org/wikipedia/commons/8/8a/NYC_subway-4D.svg",
        "london": "https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/London_Underground.svg/800px-London_Underground.svg.png",
        "paris": "https://upload.wikimedia.org/wikipedia/commons/2/2b/Paris_Metro_Map.svg",
        "tokyo": "https://upload.wikimedia.org/wikipedia/commons/2/2a/Tokyo_Subway_map_2013.svg",
        "toronto": "https://upload.wikimedia.org/wikipedia/commons/thumb/4/41/Toronto_subway_map.svg/800px-Toronto_subway_map.svg.png"
    };

    if (cityMaps[city]) {
        mapContainer.innerHTML = `<img src="${cityMaps[city]}" alt="${city} Transit Map">`;
    } else {
        mapContainer.innerHTML = "<p>Sorry, transit map not available for this city.</p>";
    }
}
