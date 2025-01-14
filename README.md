# print("Hello Freddy!")
# print("Hello World")

import board
import digitalio
import time

led = digitalio.DigitalInOut(board.LED)
led.direction = digitalio.Direction.OUTPUT

amits_button_D = digitalio.DigitalInOut(board.BUTTON_D)
amits_button_D.direction = digitalio.Direction.Input
amits_button_D.pull = digitalio.Pull.DOWN
                                        
def main():
    print(dir(board))
    print('----------------')
    print(dir(digitalio))
    print('----------------')
    print(dir(led))
    print('----------------')
    print(dir(amits_button_D))
    print('----------------')
    print(dir(digitalio.Pull))
    while True:
       led.value = amits_button_D.value
        print(amits_button_D.value)
        time.sleep(.2)
                                        
                                        
                                        
main()
    


