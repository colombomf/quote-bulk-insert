# Quotes Management System

This is a script for managing quotes. It reads quotes from a JSON file, adds them to a MongoDB database, and sends them to an API.

## Prerequisites

-   Python 3.x
-   MongoDB
-   dotenv package (`pip install python-dotenv`)
-   pymongo package (`pip install pymongo`)
-   requests package (`pip install requests`)

## Installation

1.  Clone this repository or download the script.
2.  Install the required packages using the commands mentioned in the prerequisites section.

## Configuration

1.  Create a `.env` file in the project directory.
2.  Set the following environment variables in the `.env` file:
    -   `mongodb_url`: The URL for connecting to your MongoDB database.
    -   `DB_NAME`: The name of the database in MongoDB.
    -   `COLLECTION_NAME`: The name of the collection in MongoDB.
    -   `API_URL`: The URL of the API where you want to send the quotes.

## Usage

1.  Create a JSON file (`quotes.json`) containing the quotes you want to add. The file should have the following structure:

jsonCopy code

`{
  "quotes":[
     {
        "text":"Your quote.",
        "author":"Your author",
        "videoUrl":"https://xyz.com"
     },
     {
        "text":"Your quote.",
        "author":"Your author",
        "videoUrl":"https://xyz.com",
        "imgUrl":"https://xyz.com"
     },
     {
        "text":"Your quote.",
        "author":"Your author",
        "imgUrl":"https://xyz.com"
     }
  ]
}` 

2.  Run the script by executing the command: `python script.py`.
3.  The script will read the quotes from the JSON file, add them to the MongoDB database, and send them to the specified API.
4.  If a quote already exists in the database, it will be skipped and not added again.
5.  The script will print the status of each operation (adding to the database and sending to the API).

## Contributing

Contributions are welcome! If you find any issues or want to add new features, please create a pull request or submit an issue.

## License

This project is licensed under the [MIT License](https://chat.openai.com/LICENSE).