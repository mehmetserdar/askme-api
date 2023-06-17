# askme-api

askme API is a user-friendly and efficient platform that serves as a repository for a wide range of interesting and informative askme. It offers a straightforward and intuitive interface that allows users to access factual information easily.

The core functionality of askme API revolves around storing and retrieving askme. Users can make HTTP requests to specific endpoints to interact with the API and retrieve askme based on their preferences or requirements. The API is designed to handle these requests swiftly and deliver the requested information in a structured format.
### Endpoint: [https://raw.githubusercontent.com/mehmetserdar/askme-api/main/askme.json]

## Fetch Random askme
Below is the JavaScript code that can be used to fetch a random askme from an API using the fetch function:

```javascript
function getRandomaskme() {
    fetch('https://raw.githubusercontent.com/mehmetserdar/askme-api/main/askme.json')
        .then(function(response) {
            return response.json();
        })
        .then(function(data) {
            var askme = data.askme;
            var randomIndex = Math.floor(Math.random() * askme.length);
            var askme = askme[randomIndex];

            var TextArea = document.getElementById('text-area');
            TextArea.value = askme;
        })
        .catch(function(error) {
            console.log('An error occurred while fetching the random askme:', error);
        });
}

document.getElementById('random-askme-button').addEventListener('click', function() {
    getRandomaskme();
});

```




## Contributing
Additional contributions are welcome. If you know of a positive askme that would be useful to add, please contribute to this open-source project.

