# Sunrise Data

[![Build Status](https://travis-ci.org/commercetools/commercetools-sunrise-data.svg?branch=master)](https://travis-ci.org/commercetools/commercetools-sunrise-data)

## How to create a project with Sunrise Data

Before starting the import, make sure you have access to the [Merchant Center](https://mc.commercetools.com). You will also need to run the application in this repository. Check that you meet the [requirements](#requirements) and [clone](https://help.github.com/articles/cloning-a-repository/) this repository to your computer.

## Amplience Dynamic Media
[![Amplience Dynamic Content](media/header.png)](https://amplience.com/dynamic-content)

All media references in the default catalogue have been updated to point Amplience Media sets. This enables:
1. Headless approach to media
2. Request of media at any size, any fomat
3. SEO friendly naming for media
4. Easy integration with [Amplience Viewer Kit](https://github.com/amplience/viewer-kit)

### Dynamic Media Documentation
- [Overview](https://amplience.com/products-services/dynamic-media/)
- [API Reference](https://docs.amplience.net/dynamicmedia/dmapireference.html)
- [Dynamic Media Playground](http://playground.amplience.com/di/app/#/intro)

### Example URL
Example Media URL from data set for a product:

```
https://i8.amplience.net/s/willow/072571
```

Example Tranformation of media for a thumbnail:

```
https://i8.amplience.net/s/willow/072571?w=84&qlt=65&unsharp=0,1,1,7
```


### 1. Create your project

Open the [Merchant Center](https://mc.commercetools.com) and create an empty project (without sample data).

### 2. Prepare node environemnt for Import

Go to the root of this project, where the `package.json` is located and install all node dependencies:

```
npm install
```
      
### 3. Set your commercetools project credentials

1. In the root of the project create a file named `.env`
2. Set the `.env` file with your credentials:

    ```shell
      CTP_PROJECT_KEY = <your project key>
      CTP_CLIENT_ID = <your client ID>
      CTP_CLIENT_SECRET = <your client secret>
      CTP_API_URL = <your apiUrl> (i.e., api.commercetools.com)
      CTP_AUTH_URL = <your authUrl> (i.e., auth.commercetools.com)
    ```
    *Url variables expect only the host name, not a full URL!*

### 4. Usage

1. Clean all existing project data and import new:

    ```
        npm run start
    ```

2. Clean project data:

    ```
        npm run clean:data
    ```
    
3. Import project data:

    ```
        npm run import:data
    ```
    
4. Clean or import certain data *(e.g. categories, products, customers, etc.)* 

    ```
        npm run clean:categories
    ```
    
    or
    
    ```
        npm run import:products
    ```

### Requirements

- Install [Node.js](https://nodejs.org/en/download/)
