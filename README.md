To use custom messages, place the `custom_msgs` package along with the other packages in your exercise and run `dts exercises build`.

To create a new message, simply define the message in a `.msg` file in `msg` directory and add the name of the `.msg` file as an argument to the `add_message_files` function of `CMakeLists.txt`. You'll need to build again.

To use your defined message in some other ROS node, you can do:
```python
from custom_msgs.msg import CustomMessage
msg = CustomMessage()
msg.x, msg.y = 1.0, 2.0
publish(msg)
```
