---
layout: blankpage
title: Photos
# description: Lorem ipsum dolor est
image: assets/photos/cork%20in%20waves.jpg
nav-menu: true
---
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
         #title {
            text-align: center;
            margin-top: 30px;
        }
        body {
            margin: 0;
            padding: 0;
            font-family: _font(family); /* Use the font variable */
        }
        #photos {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .photo {
            margin: 10px;
            cursor: pointer;
            position: relative;
            transition: transform 0.3s ease;
        }
        .photo img {
            width: 300px; /* Set fixed width */
            height: auto; /* Automatically adjust height to maintain aspect ratio */
            object-fit: cover;
            border-radius: 5px;
            transition: filter 0.3s ease; /* Add transition for blur effect */
        }
        .photo .description {
            display: none;
            position: absolute;
            top: 50%; /* Position on top of thumbnail */
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 1;
            /* background-color: rgba(0, 0, 0, 0.7); */
            color: #fff;
            padding: 10px;
            border-radius: 5px;
            font-size: 20px; /* Increase font size */
            text-align: center;
        }
        .photo:hover img {
            filter: blur(3px); /* Apply blur effect on hover */
        }
        .photo:hover .description {
            display: block; /* Show description on hover */
        }
        .photo.expanded img {
            filter: none; /* Remove blur effect when expanded */
            width: auto;
            height: auto;
            max-width: 80vw;
            max-height: 80vh;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 1000;
            cursor: zoom-out;
        }   
        .photo.expanded .description {
            display: block;
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translate(-50%, 85%);
            z-index: 1001;
            color: #fff;
            padding: 10px;
            border-radius: 5px;
            font-size: 30px; /* Increase font size */
            text-align: center;
        }
        #overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.87); /* Semi-transparent black overlay */
            backdrop-filter: blur(8px); /* Apply blur effect to the overlay */
            pointer-events: none; /* Allow click events to pass through the overlay */
            z-index: -1; /* Initially behind other elements */
            display: none; /* Initially hidden */
        }
        @media (max-width: 768px) {
            #overlay {
                background-color: rgba(0, 0, 0, 1); /* Completely opaque background on mobile */
                backdrop-filter: none; /* Remove blur effect on mobile */
            }
        }
        .photo.expanded {
            z-index: 1000; /* Ensure the expanded photo is on top of the overlay */
        }
    </style>
</head>
<body>
    <div id="overlay"></div> <!-- Overlay element -->
    <div id="title">
        <p>All shot on 35mm film. Refresh to shuffle!</p>
    </div>
    <div id="photos">
        {% for photo in site.static_files %}
            {% if photo.path contains '/assets/compressed/' %}
                <div class="photo" onclick="toggleExpand(this)">
                    <img src="{{ photo.path | remove_first: '/' }}" alt="{{ photo.name }}">
                    <div class="description">{{ photo.name | split: '.' | first }}</div>
                </div>
            {% endif %}
        {% endfor %}
    </div>
    <script>
        // Function to shuffle an array
        function shuffleArray(array) {
            for (let i = array.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [array[i], array[j]] = [array[j], array[i]];
            }
            return array;
        }

        // Array to store photo paths
        let photoPaths = [];

        // Function to populate photoPaths and shuffle it
        function preparePhotos() {
            {% for photo in site.static_files %}
                {% if photo.path contains '/assets/compressed/' %}
                    photoPaths.push("{{ photo.path | remove_first: '/' }}");
                {% endif %}
            {% endfor %}
            photoPaths = shuffleArray(photoPaths);
        }

        // Function to generate photo elements and append them to the photos container
        function generatePhotos() {
            const photosContainer = document.getElementById('photos');
            photosContainer.innerHTML = ''; // Clear existing content
            photoPaths.forEach(path => {
                const photoName = path.split('/').pop().split('.')[0]; // Extract photo name from path
                const photoElement = `
                    <div class="photo" onclick="toggleExpand(this)">
                        <img src="${path}" alt="${photoName}">
                        <div class="description">${photoName}</div>
                    </div>`;
                photosContainer.innerHTML += photoElement;
            });
        }

         // Function to toggle photo expansion
        function toggleExpand(element) {
            const photosContainer = document.getElementById('photos');
            const overlay = document.getElementById('overlay');

            element.classList.toggle('expanded');

            // Toggle visibility and z-index of the overlay
            overlay.style.display = element.classList.contains('expanded') ? 'block' : 'none';
            overlay.style.zIndex = element.classList.contains('expanded') ? '999' : '-1';

            // Add event listener to overlay to handle clicks
            overlay.style.pointerEvents = element.classList.contains('expanded') ? 'auto' : 'none';

            // Add event listener to document to handle clicks
            if (element.classList.contains('expanded')) {
                document.addEventListener('click', minimizeExpandedImage);
            } else {
                document.removeEventListener('click', minimizeExpandedImage);
            }
        }

        // Function to minimize expanded image if click occurs outside the expanded image
        function minimizeExpandedImage(event) {
            const expandedImage = document.querySelector('.photo.expanded');
            if (expandedImage && !expandedImage.contains(event.target)) {
                toggleExpand(expandedImage);
            }
        }

        // Call functions to prepare and generate photos when the page loads
        window.onload = function() {
            preparePhotos();
            generatePhotos();
        };
    </script>
</body>