# log

## 2024-01-01

Installed it on a standalone server.
The thing I missed is bind the port externally.

``viktor@tbox:~$ ./livekit-server --dev --bind 0.0.0.0``

Make first user
``livekit-cli create-token --join --identity user1 --room test``

Make second user
``livekit-cli create-token --join --identity user2 --room test``

I git cloned livekit meet. Because the brower will not allow mixing https and ws
I followed https://github.com/livekit-examples/meet?tab=readme-ov-file#dev-setup

The connection url you then use is:  
``http://localhost:3000/custom?liveKitUrl=ws://192.168.1.150:7880&token=eyJhb...``

And it works!

## 2023-12-30

Downloaded livekit for windows. Unzip and run with `.\livekit-server.exe --dev`

.\livekit-server.exe --config .\config.yaml --node-ip 192.168.1.50

Tried running in devcontainer but nmaps marks is as closed.

Starting with python backend. - can skip this for now. livekit-cli can make it.

https://github.com/livekit/livekit-cli


Want to website to be as basic as possible

Trying to get https://meet.livekit.io/?tab=custom working. It tries to connect to `wss://192.168.1.50:7881` but fails.

Using https://metricat.dev/ as viewer.

