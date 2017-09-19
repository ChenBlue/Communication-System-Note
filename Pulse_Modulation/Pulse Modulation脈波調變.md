# 基本觀念
與連續波調變不同的是，首先要經過取樣程序，將連續訊號轉換成離散型訊號。
![Pulse mod diagram](https://github.com/ChenBlue/Communication-System-Note/blob/master/Pulse_Modulation/Resource/Pulse_Mod_block.JPG)

# 脈波調變的分類
### 類比脈波調變(Analog Pulse Modulation)
週期性的脈波烈被拿來當載波，為連續性的變化。</br>
1. PAM: Pulse Amplitude Modulation
2. PWM: Pulse Width Modulation
3. PPM: Pulse Position Modulation </br>
![PAM&PWM&PPM](https://github.com/ChenBlue/Communication-System-Note/blob/master/Pulse_Modulation/Resource/PAM_PWM_PCM.jpg)

### 數位脈波調變(Digital Pulse Modulation)
訊號在時間及振幅都是以離散的形式表示，以一段Code脈波之數位形式傳輸。
##### 基頻帶脈波調變 (Baseband Transmission)
1. PCM: Pulse Coded Modulation
2. DM: Delta Modulation
3. DPCM: Differential PCM
4. ADPCM: Adaptive DPCM
##### 旁頻帶脈波調變
ASK, PSK, FSK, MSK
