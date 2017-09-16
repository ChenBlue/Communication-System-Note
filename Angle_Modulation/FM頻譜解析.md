# 單頻(Single tone)FM調變頻譜
**調變信號**：$S(t)=A_ccos[\theta _i (t)]=A_c cos[2\pi f_c t+\phi (t)]$ </br>
**訊息**: $m(t)=A_m \cos(2\pi f_m t)$ </br>
$f_i (t)=f_c +k_f A_m \cos(2\pi f_m t)=f_c + \Delta f\cos(2\pi f_m t)$, $\Delta f=k_f A_m=|f_i (t)-f_c|_max$ (Frquency Deviation頻率偏差) </br>
$\theta _i (t)=2\pi \int ^t _0 f_i(\tau) d\tau =2\pi \int ^t _0 (f_c+\Delta f\cos(2\pi f_m \tau) d\tau=2\pi f_c t+\phi (t)$ </br>
$\phi (t)=2\pi k_f \int_0 ^t m(\tau )d\tau =2\pi k_f \int_0 ^t A_m \cos(2\pi f_m \tau) d\tau =2\pi k_f A_m \frac{1}{2\pi f_m }\sin (2\pi f_m t)=\frac{k_f A_m}{f_m }\sin (2\pi f_m t)=\beta \sin (2\pi f_m t)$
> $\beta=\frac{k_f A_m}{f_m }=\frac{\Delta f}{f_m }$: Modulation index 調變指數 </br>
> 若$\beta<<1\rightarrow \Delta f<<f_m$,稱為窄帶FM(Narrowband FM) </br>
> 若$\Delta f\aprox f_m or \Delta f>f_m$, 稱為寬帶FM(Wideband FM) </br>

