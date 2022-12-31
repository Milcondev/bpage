# Bpage 

## Example
simple example for bpage

```js
const { bpage } = require('bpage.js');
const bpage = new bpage();

client.on('messageCreate', async (message) => {
    const page = [
        'This is page 1',
        'This is page 2',
        'This is page 3',
        'This is page 4',
    ]
    if (message.content === '!ping') {
        const embed = page.map((x) => new EmbedBuilder().setDescription(x));
        
       // options is optional
       bpage.setTime(40000);
       bpage.setStyle("secondary");
       await bpage.bpage(message, embed, options);
    }
});
```
## Customization
you can provide options to bpage

```js
const options = {
    style: ButtonStyle.Primary,
    timeout: 60000,
    emojis: {
        first: '⏮',
        back: '◀',
        next: '▶',
        last: '⏭',
        stop: '⏹',
    }
}
```

