/*Необходимо из объекта, который лежит в константе post вывести значения, к которым приписан комментарий, в консоль.

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Homework</title>
</head>

<body>
    <script>
        "use strict";

        const post = {
            author: "John", // вывести этот текст
            postId: 23,
            comments: [
                {
                    userId: 10,
                    userName: "Alex",
                    text: "lorem ipsum",
                    rating: {
                        likes: 10,
                        dislikes: 2, // вывести это число
                    },
                },
                {
                    userId: 5, // вывести это число
                    userName: "Jane",
                    text: "lorem ipsum 2", // вывести этот текст
                    rating: {
                        likes: 3,
                        dislikes: 1,
                    },
                },
            ],
        };

        console.log(post.author);
        console.log(post.comments[0].rating.dislikes);
        console.log(post.comments[1].userId);
        console.log(post.comments[1].text);

    </script>
</body>

</html>



Дан массив products, необходимо цену каждого продукта уменьшить на 15% используя метод forEach.


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Homework</title>
</head>

<body>
    <script>
        "use strict";

        const products = [
            {
                id: 3,
                price: 200,
            },
            {
                id: 4,
                price: 900,
            },
            {
                id: 1,
                price: 1000,
            },
        ];

        products.forEach(product => product.price = product.price * 0.85);

</script>
</body>

</html>*/

1. Необходимо вывести в консоль массив продуктов в котором есть хоть одна
фотография используя метод filter. Исходные данные - массив products.
2. Необходимо отсортировать массив products используя метод sort по цене,
начиная с самой маленькой, заканчивая самой большой ценой, после чего вывести
отсортированный массив в консоль.

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Homework</title>
</head>

<body>
    <script>
        "use strict";

        const products = [
            {
                id: 3,
                price: 127,
                photos: [
                    "1.jpg",
                    "2.jpg",
                ],
            },
            {
                id: 5,
                price: 499,
                photos: [],
            },
            {
                id: 10,
                price: 26,
                photos: [
                    "3.jpg",
                ],
            },
            {
                id: 8,
                price: 78,
            },
        ];

        console.log(products.filter(product => 'photos' in product && 
          product.photos.length !== 0));
        console.log(products.sort((product1, product2) => 
          product1.price - product2.price));

    </script>
</body>

</html>
