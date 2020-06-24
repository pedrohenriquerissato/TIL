# Filter Arrays With Arrays

One of the easiest ways to filter an array of objets by another array

```javascript
const post = {
	...
	categories: ['Movies', 'Food', 'Tech']
};

const filter = ['Tech', 'Movies'];

```

```javascript
 const handleFilterPosts = (posts) => {
    return posts.filter((post) =>
      post.categories.find((category) => filter.includes(category))
    );
  };
 ```

[source](https://codereview.stackexchange.com/questions/141943/filter-array-with-another-array)