## Usage/Examples

```javascript
import { Host, Client } from 'uNet'
import { Safe, Delay, Loop, Log } from 'uTil'

Safe(() => {

	const uHost = new Host(1020)
	uHost.on('message', Log)
	Loop(() => uHost.emit('Hello from the Server'), 1000 / 60 /**60fps**/)

	const uclient = new Client(1020)
	uClient.on('message', Log)
	Loop(() => uClient.emit('Hello from the Client'), 1000 / 60 /**60fps**/)

})
```
