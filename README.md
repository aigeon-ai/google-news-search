```markdown
# Aigeon AI Google News Search

Aigeon AI Google News Search is a Python-based server application designed to interact with the Google News API via SerpApi. It provides a comprehensive interface for querying Google News, allowing users to specify various parameters to tailor their news search results according to specific needs such as language, country, topic, and more.

## Features Overview

- **Flexible Querying**: Allows users to perform detailed searches on Google News using a variety of parameters.
- **International Support**: Supports multiple languages and countries for localized news results.
- **Topic and Publication Specific Searches**: Enables searches based on specific topics or publications.
- **Sorting and Caching Options**: Offers sorting by relevance or date and includes caching options to optimize search performance.
- **Enterprise Features**: Includes advanced features like ZeroTrace mode for enhanced privacy.

## Main Features and Functionality

The application is built using the `FastMCP` framework, which facilitates the creation of microservices. The main feature of this application is the `search_google_news` function, which interacts with the SerpApi to fetch news results based on user-defined parameters.

### Key Functionalities:

- **Query Parameter (`q`)**: Allows users to specify the search query, similar to a regular Google News search.
- **Geolocation (`gl`)**: Defines the country for the search using a two-letter country code.
- **Language (`hl`)**: Specifies the language for the search using a two-letter language code.
- **Topic Token**: Searches for news within a specific topic.
- **Publication Token**: Filters news results from a specific publisher.
- **Section Token**: Accesses sub-sections of a specific topic.
- **Story Token**: Retrieves full coverage of a specific story.
- **Sorting Option (`so`)**: Sorts results by relevance or date.
- **Caching (`no_cache`)**: Controls whether to use cached results or fetch new data.
- **Asynchronous Search (`async`)**: Allows for asynchronous search submission to SerpApi.
- **ZeroTrace Mode**: An enterprise feature that enhances privacy by not storing search parameters or metadata.

## API Endpoints or Main Functions Description

### `search_google_news`

This is the primary function of the application, designed to perform a search on Google News using the SerpApi. It constructs a request payload based on the provided parameters and sends a GET request to the SerpApi endpoint. The function returns the JSON response containing the search results.

#### Parameters:

- **q**: The search query string.
- **gl**: Country code for geolocation.
- **hl**: Language code for the search.
- **topic_token**: Token for specific news topics.
- **publication_token**: Token for specific news publications.
- **section_token**: Token for sub-sections of topics.
- **story_token**: Token for full story coverage.
- **so**: Sorting method (0 for relevance, 1 for date).
- **no_cache**: Boolean to force fetching new results.
- **async**: Boolean for asynchronous search submission.
- **zero_trace**: Boolean for enabling ZeroTrace mode.

## Configuration Parameters Explanation

- **`SERP_API_KEY`**: This environment variable must be set with your SerpApi key to authenticate requests.
- **`serp_url`**: The endpoint URL for the SerpApi, set to `https://serpapi.com/search`.

The application is designed to be run as a standalone server using the `FastMCP` framework, which listens for incoming requests and processes them using the defined `search_google_news` function.

To start the server, execute the script, and it will begin listening for requests via the standard input/output transport method.
```
