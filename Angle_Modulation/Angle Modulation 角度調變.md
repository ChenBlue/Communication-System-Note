# 角度調變 (Angle Modulation)
一種以載波瞬時頻率的變化來表示資訊的調變方式。 </br>
調變信號：$S(t)=A_ccos[\theta _i (t)]=A_c cos[2\pi f_c t+\phi (t)]$ </br>
1. 瞬時相位: $\theta _i (t)=2\pi f_c t+\phi (t)$ </br>
2. 平均頻率(從t到$t+\Delta t$): $f_{\Delta t}(t)=\frac{\theta _i (t+\Delta t)-\theta _i (t)}{2\pi \Delta t}$ </br>
3. 瞬時頻率: $f_i (t)=\lim_{\Delta t \shortrightarrow 0} f_{\Delta t}(t)=\frac{1}{2\pi}\frac{d\theta _i (t)}{dt}$ </br>

## 相位與頻率調變
|   |$\theta _i (t)$ | $f_i (t)$|
|----|--------------|----------|
|未調變訊號|$2\pi f_c t$|$f_i (t)$|
