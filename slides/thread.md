+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Threads

```typescript
class Vol {
  constructor(public altitude: number) {}
}

async function voler(vol: Vol) {
  let result = await setTimeout(() => {
    console.log(`Voler a ${vol.altitude} pieds`);
  }, 1000);
}

let vol = new Vol(15000);
Promise.resolve(voler(vol));
vol.altitude = 0 💀
```