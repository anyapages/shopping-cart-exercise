# Shopping Cart Exercise

A brief restock solution for a Shopping-Cart exercise.

## Tasks:

- Implement the restock feature when a user clicks the “Restock” button, a call is made to the Strapi back end specified in the input field.
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
Implemented to strapi API  `http://localhost:1337/products`

## Usage

<img src = 'example.png' width="500" height="440"> 

## License
[MIT](https://github.com/anyapages/shopping-cart-exercise/blob/main/LICENSE) 
