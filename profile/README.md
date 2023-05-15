## 👋 Usage/Examples

```javascript
import { Host, Client } from 'unet'
import { Safe, Delay, Loop, Log } from 'utils'

Safe(() => {

	const myHost = new Host(1020)
	myHost.on('message', Log)
	Loop(() => myHost.emit('Hello from the Server'), 1000 / 60 /**60fps**/)

	const myClient = new Client(1020)
	myClient.on('message', Log)
	Loop(() => myClient.emit('Hello from the Client'), 1000 / 60 /**60fps**/)

})
```
