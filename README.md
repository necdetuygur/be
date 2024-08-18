```sh
docker stop be-db-1
docker stop be-node-1
docker stop be-admin-1

docker rm be-db-1
docker rm be-node-1
docker rm be-admin-1

docker compose up -d
```

```js
let headersList = {
  "Content-Type": "application/json",
};

let bodyContent = JSON.stringify({
  title: "Test",
  description: "Test",
});

let response = await fetch("http://localhost:3000/todos", {
  method: "POST",
  body: bodyContent,
  headers: headersList,
});

let data = await response.text();
console.log(data);
```
