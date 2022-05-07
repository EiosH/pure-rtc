# pure-rtc

开箱即用的 webRTC 库, 封装 RTCSessionDescription、RTCIceCandidate 等

### 使用方法

```js
const peer = new Peer();

peer.on("signal", (signal: Signal) => {
  // send signal
});

const receiveSignal = (data: any) => {
  peer.signal(data);
};

peer.send("hello");

// or manual

const peer = new Peer({ isManual: true });

peer.on("signal", (signal: Signal) => {
  // send signal
});

const receiveSignal = (data: any) => {
  peer.signal(data);
};

peer.start();
peer.send("hello");
```
