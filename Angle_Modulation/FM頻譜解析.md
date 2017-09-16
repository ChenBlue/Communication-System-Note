# 單頻(Single tone)FM調變頻譜
**調變信號**：$S(t)=A_ccos[\theta _i (t)]=A_c cos[2\pi f_c t+\phi (t)]$ </br>
**訊息**: $m(t)=A_m \cos(2\pi f_m t)$ </br>
$f_i (t)=f_c +k_f A_m \cos(2\pi f_m t)=f_c + \Delta f\cos(2\pi f_m t)$, $\Delta f=k_f A_m=|f_i (t)-f_c|\_{max}$ 為Frquency Deviation頻率偏差 </br>
$\theta _i (t)=2\pi \int ^t _0 f_i(\tau) d\tau =2\pi \int ^t _0 (f_c+\Delta f\cos(2\pi f_m \tau) d\tau=2\pi f_c t+\phi (t)$ </br>
$\phi (t)=2\pi k_f \int_0 ^t m(\tau )d\tau =2\pi k_f \int_0 ^t A_m \cos(2\pi f_m \tau) d\tau =2\pi k_f A_m \frac{1}{2\pi f_m }\sin (2\pi f_m t)=\frac{k_f A_m}{f_m }\sin (2\pi f_m t)=\beta \sin (2\pi f_m t)$
> $\beta=\frac{k_f A_m}{f_m }=\frac{\Delta f}{f_m }$: Modulation index 調變指數 </br>
> 若$\beta\ll 1\rightarrow \Delta f<<f_m$,稱為窄帶FM(Narrowband FM) </br>
> 若$\Delta f\approx f_m or \Delta f>f_m$, 稱為寬帶FM(Wideband FM) </br>

## 窄帶FM調變(NBFM)
$S(t)=A_c\cos[2\pi f_c t+\beta \sin (2\pi f_m t)]=A_c\cos(2\pi f_c t)\cos[\beta \sin (2\pi f_m t)]-A_c \sin(2\pi f_c t)\sin[\beta \sin (2\pi f_m t)]$ </br>
若$\beta$很小: $\cos[\beta \sin (2\pi f_m t)]\simeq 1$, $\sin[\beta \sin (2\pi f_m t)]\simeq \beta \sin (2\pi f_m t)$ </br>
$\rightarrow S(t)\simeq A_c \cos (2\pi f_c t)-\beta A_c \sin (2\pi f_c t)\sin (2\pi f_m t)$ </br>
與DSBSC做比較： $S(t)=A_c m(t)\cos (2\pi f_c t)$ </br>
發現S(t)的第一項為載波訊號，第二項則類似DSBSC的調變訊號，可以用以下Block Diagram來產生NBFM調變訊號 </br>
![NBFM_modulator](https://github.com/ChenBlue/Communication-System-Note/blob/master/Angle_Modulation/Material/NBFM_mod.JPG) </br>
</br>
**缺點**: </br>
理想上，FM要有不變的envelope，但是對於NBFM來說，他有多餘的AM訊號($\beta A_c \sin (2\pi f_c t)\sin (2\pi f_m t)$，因此$\theta _i (t)$將有"Harmonic distortion"

## 寬帶FM調變(WBFM)
\\\TODO
http://www.edaboard.com/thread236069.html
