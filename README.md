# OpenAPIClient-php

# API Reference


For more information, please visit [https://nft.storage](https://nft.storage).

## Installation & Usage

### Requirements

PHP 7.2 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/nftstorage/php-client.git"
    }
  ],
  "require": {
    "nftstorage/php-client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure Bearer (JWT) authorization: bearerAuth
$config = NFTStorage\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new NFTStorage\Api\NFTStorageAPI(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->callList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NFTStorageAPI->callList: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://nft.storage/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*NFTStorageAPI* | [**callList**](docs/Api/NFTStorageAPI.md#calllist) | **GET** / | List all stored files
*NFTStorageAPI* | [**delete**](docs/Api/NFTStorageAPI.md#delete) | **DELETE** /{cid} | Stop storing the content with the passed CID
*NFTStorageAPI* | [**status**](docs/Api/NFTStorageAPI.md#status) | **GET** /{cid} | Get information for the stored file CID
*NFTStorageAPI* | [**store**](docs/Api/NFTStorageAPI.md#store) | **POST** /upload | Store a file

## Models

- [Deal](docs/Model/Deal.md)
- [DeleteResponse](docs/Model/DeleteResponse.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [ErrorResponseError](docs/Model/ErrorResponseError.md)
- [ForbiddenErrorResponse](docs/Model/ForbiddenErrorResponse.md)
- [ForbiddenErrorResponseError](docs/Model/ForbiddenErrorResponseError.md)
- [GetResponse](docs/Model/GetResponse.md)
- [Links](docs/Model/Links.md)
- [LinksFile](docs/Model/LinksFile.md)
- [ListResponse](docs/Model/ListResponse.md)
- [NFT](docs/Model/NFT.md)
- [NFTDeals](docs/Model/NFTDeals.md)
- [Pin](docs/Model/Pin.md)
- [PinStatus](docs/Model/PinStatus.md)
- [UnauthorizedErrorResponse](docs/Model/UnauthorizedErrorResponse.md)
- [UnauthorizedErrorResponseError](docs/Model/UnauthorizedErrorResponseError.md)
- [UploadResponse](docs/Model/UploadResponse.md)

## Authorization

### bearerAuth

- **Type**: Bearer authentication (JWT)

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
