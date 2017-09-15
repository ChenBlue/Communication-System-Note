# 角度調變 (Angle Modulation)
一種以載波瞬時頻率的變化來表示資訊的調變方式。 </br>
調變信號：$S(t)=A_ccos[\theta _i (t)]=A_c cos[2\pi f_c t+\phi (t)]$ </br>
1. 瞬時相位: $\theta _i (t)=2\pi f_c t+\phi (t)$ </br>
2. 平均頻率(從t到$t+\Delta t$): $f_{\Delta t}(t)=\frac{\theta _i (t+\Delta t)-\theta _i (t)}{2\pi \Delta t}$ </br>
3. 瞬時頻率: $f_i (t)=\lim_{\Delta t \rightarrow 0} f_{\Delta t}(t)=\frac{1}{2\pi}\frac{d\theta _i (t)}{dt}$ </br>

### 相位調變(Phase Modulation)與頻率調變(Frequency Modulation)
|   |$\theta _i (t)$ | $f_i (t)$|
|----|--------------|----------|
|未調變訊號|$2\pi f_c t$|$f_c$|
|PM調變|*$2\pi fc t+k_p m(t)$*|$f_c +\frac{k_p}{2\pi}\frac{dm(t)}{dt}$|
|FM調變|$2\pi fc t+2\pi k_f \int^t _0 m(\tau )d\tau$|*$f_c +k_f m(t)$*|
> $k_p$: 相位靈敏度; $k_f$:頻率靈敏度

#### FM與PM之關係
