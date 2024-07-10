<br />

** For building the surf 5 code please refer to [getting_started.md](getting_started.md) for examples usage.**

<br />

# Surf5-Wizbeacon
WizBeacon provides audio cues to help visually impaired swimmers to time their flip turns and stay oriented in the pool using sound signals. 

#Pico I2S Code
```
import time
import board
import audiobusio
import audiocore

# Audio output object
audio = audiobusio.I2SOut(board.D24, board.D25, board.A3)

# Define sound to play
sound = '3_meters'

# Open sound wave file
wave_file = open('sounds/' + sound + '.wav', 'rb')
wave = audiocore.WaveFile(wave_file)

# Main loop
while True:
    # Play selected sound
    print("Playing:", sound)
    audio.play(wave)

    # Delay
    time.sleep(5)
```
<br />

![alt text]https://github.com/Aj31331/Surf5-WizBeacon/blob/main/Picocircuit.png







<br />


