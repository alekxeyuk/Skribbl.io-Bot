# Skribbl.io-Bot

<p align="center"><a href="https://github.com/alekxeyuk/Skribbl.io-Bot"><img src="https://raw.githubusercontent.com/alekxeyuk/Skribbl.io-Bot/master/resources/logo.png"></a></p>

My try at creating fully automated game bot.

## Features
* Asynchronous, event based code style
* Line optimization for faster drawing
* Supports two different dither algos
* Easy image size control
* Automatic googling, and image picking
* Search filters (image size, colors, etc...)
* Chat bot
* And many more ...

## Contributing
We are welcome any contributing: bug fixes, improvements, code refactoring and other stuffs.

## Dependencies
- `Python 3.4` or higher
- `Asyncio`
- `websockets` [websockets](https://github.com/aaugustin/websockets)
- `aiohttp` [aiohttp](https://github.com/aio-libs/aiohttp/)
- `socketio` [python-socketio](https://github.com/miguelgrinberg/python-socketio)
- `requests` [requests](https://github.com/kennethreitz/requests)
- `hitherdither` [hitherdither](https://github.com/hbldh/hitherdither)
- `pillow` [pillow](https://github.com/python-pillow/Pillow)
- `google-images-download` [google-images-download](https://github.com/hardikvasa/google-images-download)
- `numpy` for `hitherdither`

## Install
Clone repository, then make sure that you have Dependencies installed in your system, then:

```bash
python draw_bot.py 'port' - not necessary default's to 5002 
```

You can always change settings:

```python
# App settings
SETTINGS = {'port': '5002', 'join': '', 'language': 'English', 'x': 3, 'y': 4, 'shuffle': True}
# Connect user settings
await sio.emit('userData' , {"name": "­", "code":"", "avatar": [-1, -1, -1, -1], "join": SETTINGS['join'], "language": SETTINGS['language'], "createPrivate": False})
# Google search settings
arguments = {"keywords": word, "limit":10, "print_urls":False, 'no_download':True, 'safe_search':True, 'exact_size':'200,200', 'type': 'clipart', 'format': 'jpg'}
```

You should remember that the game does not allow more than 6 concurrent connections to 1 port
so that means that the max amount of bots that you can run on 1 machine is 12.

Also because of how socketio work, if you want your bot to auto-reconnect you can run it via loop.bat and loop 5001.bat

## Screenshots
- Using large draw size and no optimization
![Example](resources/EXAMPLE.png)
![Example2](resources/EXAMPLE2.png)
- Using line optimization and yliluoma's 1 ordered dithering
![Example3](resources/EXAMPLE3.png)
- Using line optimization and cluster dot dithering
![Example4](resources/EXAMPLE4.png)

## Warning!
`This code is published for educational purposes ONLY, I have no responsibility for how this code will be used, all responsibility lies on YOU. Please just don't be a FREAK. gl hf`

## License
[MIT](https://github.com/alekxeyuk/Skribbl.io-Bot/blob/master/LICENSE)
