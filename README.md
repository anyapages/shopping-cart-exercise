# Shopping Cart Exercise 🛒

A restocking functionality solution for a Shopping-Cart exercise.

## Tasks:

- Implement the restock feature when a user clicks the `Restock` button, a call is made to the Strapi back end specified in the input field.
- The result of this call should be updated on the list of products.

## Solution

I use `doFetch`(url) function on `restockProducts` value to make a call to the API and use `setItem` to update the existing items as shown below;
```javaScript
const restockProducts = (url) => {
    doFetch(url);
    let newItems = data.map((item) => {
      let { name, country, cost, instock } = item;
      return { name, country, cost, instock };
    });
    setItems([...items, ...newItems]);
  };
```

## Installation

- `npm install`
- Run on `http://localhost:1337/products`

## Usage

<img src = 'https://raw.githubusercontent.com/anyapages/shopping-cart-exercise/main/public/restock.png?token=ATDMTEBA5UWDUW5PQ3XNT7DBEIZHS' width="500" height="440"> 

<a href="http://cart01.s3-website-us-east-1.amazonaws.com/">Live Demo on AWS</a>

## Learn More

To learn React and Strapi, check out the [React documentation](https://reactjs.org/), [Strapi API](https://strapi.io/resource-center).

## License

[MIT](https://github.com/anyapages/shopping-cart-exercise/blob/main/LICENSE) 
