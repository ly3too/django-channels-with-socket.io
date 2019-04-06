# Django channels with socket.io demo

Django channels' ProtocolTypeRouter accept any asgi application, socketio can be setup as a asgi app.
This makes it possible to use socketio with django channels

## setup
cannot use `manage.py runserver` to serve it

you need to create asgi.py and setup asgi app entry point.

then you go: `daphne django_channel.asgi:application`

## configure socket.io client to use websocket as transport layer protocol
because I only route websocket to consumers, socketio client must use websocket to 
communicate with the server, other http traffic is routed the traditional way


the chat socketio demo was taken from [here](https://github.com/miguelgrinberg/python-socketio)