## Usage/Examples

```javascript
import { Safe, Delay, Loop, Log } from 'uTIL'
import { Host, Client } from 'uNET'

Safe(() => {

	const uHost = new Host(1020)
	uHost.on('message', Log)
	Loop(() => uHost.emit('Hello from the Server'), 250)

	const uclient = new Client(1020)
	uClient.on('message', Log)
	Loop(() => uClient.emit('Hello from the Client'), 250)

})
```
