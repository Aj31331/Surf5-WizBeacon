<br />

** For building the surf 5 code please refer to [getting_started.md](getting_started.md) for examples usage.**

<br />

# Surf5-Wizbeacon
WizBeacon provides audio cues to help visually impaired swimmers to time their flip turns and stay oriented in the pool using sound signals. 

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/kBOCzjM_PrU/0.jpg)](https://www.youtube.com/watch?v=kBOCzjM_PrU)


#Pico I2S Code
```
import time
import board
import audiobusio
import audiocore

# Audio output object
audio = audiobusio.I2SOut(board.D24, board.D25, board.A3)

# Define sound to play
name = 'Flip Turn'

# Open sound wave file
playfunc = open('Path/' + name + '.wav', 'rb')
wave = audiocore.WaveFile(playfunc)

#Uncomment or Add based on the beacon position

# Define sound to play
#name = 'Five meter'

# Open sound wave file
#playfunc = open('Path/' + name + '.wav', 'rb')
#wave = audiocore.WaveFile(playfunc)

# Define sound to play
#name = 'ten meter'

# Open sound wave file
#playfunc = open('Path/' + name + '.wav', 'rb')
#wave = audiocore.WaveFile(playfunc)

# Define sound to play
#name = 'Fifteen meter'

# Open sound wave file
#playfunc = open('Path/' + name + '.wav', 'rb')
#wave = audiocore.WaveFile(playfunc)

# Define sound to play
#name = 'Twenty Meter'

# Open sound wave file
#playfunc = open('Path/' + name + '.wav', 'rb')
#wave = audiocore.WaveFile(playfunc)

# Define sound to play
#name = 'Twenty Five'

# Open sound wave file
#playfunc = open('Path/' + name + '.wav', 'rb')
#wave = audiocore.WaveFile(playfunc)


# Main loop
while True:
    # Play selected sound
    print("Playing:", sound)
    audio.play(wave)

    # Delay
    time.sleep(5)

```

![alt text](https://github.com/Aj31331/Surf5-WizBeacon/blob/main/2024-07-13-22-09-42-892.jpg)

```

![alt text](https://github.com/Aj31331/Surf5-WizBeacon/blob/main/Picocircuit.png?raw=true)


```




<br />


