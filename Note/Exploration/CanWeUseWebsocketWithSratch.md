Code to connect to your game in python
``` py
from scratchapi import Scratch

# Connect to your Scratch project
scratch = Scratch('YourUsername', 'YourPassword', 'YourProjectId')

# Define a function to handle WebSocket messages
def handle_message(message):
    print(f"Received message: {message}")

# Connect to the WebSocket server and set the callback function
scratch.socket.on_message = handle_message
scratch.socket.connect()

# Keep the script running to maintain the WebSocket connection
while True:
    pass

```
