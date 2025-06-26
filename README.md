# Aigeon AI Google News Search

## Project Description

Aigeon AI Google News Search is a Python-based server application designed to interface with the SerpApi to perform comprehensive searches on Google News. The application leverages the FastMCP framework to provide a structured and efficient way to query Google News, offering a variety of parameters to customize search results according to user needs.

## Features Overview

- **Flexible Query Parameters**: Allows users to define search queries using a variety of parameters such as country, language, topic, publication, and more.
- **Sorting and Caching Options**: Supports sorting results by relevance or date and provides options to use cached results or force fresh searches.
- **Asynchronous Search Capability**: Offers the ability to perform searches asynchronously, enabling users to submit queries and retrieve results at a later time.
- **Enterprise Features**: Includes advanced options like ZeroTrace mode for enhanced privacy and data management.

## Main Features and Functionality

1. **Search Customization**: 
   - Users can specify search queries (`q`) similar to a regular Google News search.
   - Country (`gl`) and language (`hl`) parameters allow localization of search results.
   - Topic, publication, section, and story tokens provide targeted search capabilities for specific news categories or sources.

2. **Search Management**:
   - The `so` parameter allows sorting of search results by relevance or date.
   - The `no_cache` parameter controls whether to use cached results or fetch new data.
   - The `async` parameter enables asynchronous search submission, useful for handling large or complex queries.

3. **Enterprise-Level Privacy**:
   - The `zero_trace` parameter, available for enterprise users, ensures that search parameters and metadata are not stored, enhancing privacy and security.

## Main Function Description

### `search_google_news`

This function serves as the core utility for performing Google News searches through the SerpApi. It accepts a variety of parameters to tailor the search experience:

- **Parameters**:
  - `q`: Defines the search query.
  - `gl`: Specifies the country code for localization.
  - `hl`: Specifies the language code for localization.
  - `topic_token`: Targets specific news topics.
  - `publication_token`: Filters results by specific publishers.
  - `section_token`: Accesses subsections within a topic.
  - `story_token`: Provides full coverage of specific stories.
  - `so`: Determines sorting method (by relevance or date).
  - `no_cache`: Controls caching behavior.
  - `async`: Enables asynchronous search processing.
  - `zero_trace`: Activates enhanced privacy mode.

- **Functionality**:
  - Constructs a payload with the specified parameters, omitting any that are `None`.
  - Sends a GET request to the SerpApi endpoint with the constructed payload.
  - Processes the response and returns the JSON data for further use.

This function is designed to provide a robust and flexible interface for accessing Google News data, catering to a wide range of search needs and preferences.