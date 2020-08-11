# Url shortener service

An Express app that generates, saves and returns a short url when a long url is entered. When the short url is used, the app searches the database and redirects the request to the long url if it is found in the database.

## Example usage:

-   POST request to http://baseUrl.com/api/shorten with a body of {longUrl: url}

## Example output:

```json
{
    "_id": "5f32062a9184fa25d3dff9f6",
    "longUrl": "https://www.amazon.com/gp/product/B01M1GLSSF?pf_rd_r=AN7CTHK93AZHG89SABXG&pf_rd_p=edaba0ee-c2fe-4124-9f5d-b31d6b1bfbee",
    "shortUrl": "http://baseUrl.com/RBDlnk3ec",
    "urlCode": "RBDlnk3ec",
    "date": "Mon Aug 10 2020 21:44:58 GMT-0500 (Central Daylight Time)"
}
```

Visiting http://baseUrl.com/urlCode will redirect to the longUrl if it is found in the database

## Getting Started

```node
npm install
```

```node
npm start
```

A config folder should be created with a default.json file that contains a mongoDB connection string, and a baseUrl value.

Once the server has started, navigate to localhost:5000.

## Built With

-   [Express](https://github.com/expressjs/express) - Server
-   [Moment](https://github.com/moment/moment) - Parsing Dates
-   [mongoose](https://github.com/Automattic/mongoose) - Database ORM
-   [shortid](https://github.com/dylang/shortid) - shortCode generation
-   [valid-url](https://github.com/ogt/valid-url) - validate urls

## Authors

-   **John Irle** - [JohnIrle](https://github.com/JohnIrle)
