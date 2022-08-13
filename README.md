# Angular Testing Cookbook

## Report Config for command line

<details>
  <summary>Details</summary>

### Mocha Report

1. Install dependency
```
npm i karma-mocha-reporter --save-dev
```
2. Add plugin to **karma.conf.js** `require('karma-mocha-reporter')`
3. Change Report `reporters: ['mocha']`,
4. Change `browsers: ['ChromeHeadless']`

</details>

## Faker JS Dependecy

<details>
  <summary>Details</summary>

```
npm i faker-js/faker --save-dev

npm install --save-dev @faker-js/faker
```
#### Ejemplo de uso
```
 const {commerce, datatype, image} = faker;
  return {
    id: datatype.uuid(),
    taxes: 2,
    category: {
      id: datatype.number(),
      name: commerce.department()
    },
    description: commerce.productDescription(),
    images: [image.imageUrl(), image.imageUrl()],
    price: parseInt(commerce.price()),
    title: commerce.productName()
  }; 
```

</details>
