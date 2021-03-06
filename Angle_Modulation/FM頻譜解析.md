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
> **$\beta$很小** </br>

$S(t)=A_c\cos[2\pi f_c t+\beta \sin (2\pi f_m t)]=A_c\cos(2\pi f_c t)\cos[\beta \sin (2\pi f_m t)]-A_c \sin(2\pi f_c t)\sin[\beta \sin (2\pi f_m t)]$ </br>
若$\beta$很小: $\cos[\beta \sin (2\pi f_m t)]\simeq 1$, $\sin[\beta \sin (2\pi f_m t)]\simeq \beta \sin (2\pi f_m t)$ </br>
$\rightarrow S(t)\simeq A_c \cos (2\pi f_c t)-\beta A_c \sin (2\pi f_c t)\sin (2\pi f_m t)$ </br>
與DSBSC做比較： $S(t)=A_c m(t)\cos (2\pi f_c t)$ </br>
發現S(t)的第一項為載波訊號，第二項則類似DSBSC的調變訊號，可以用以下Block Diagram來產生NBFM調變訊號 </br>
![NBFM_modulator](https://github.com/ChenBlue/Communication-System-Note/blob/master/Angle_Modulation/Material/NBFM_mod.JPG) </br>
</br>
**缺點**: </br>
理想上，FM要有不變的envelope，但是對於NBFM來說，他有多餘的AM訊號[$\beta A_c \sin (2\pi f_c t)\sin (2\pi f_m t)$]，因此$\theta _i (t)$將有"Harmonic distortion"

## 寬帶FM調變(WBFM)
> **$\beta$很大** </br>

$S(t)=A_c\cos[2\pi f_c t+\beta \sin (2\pi f_m t)]=Re[A_c exp(j2\pi f_c t)exp(j\beta \sin (2\pi f_m t)]=Re[\tilde{S}(t)exp(j2\pi f_c t)]$ </br>
$\tilde{S}(t)$為S(t)之複包跡(Complex envelope) </br>
$\tilde{S}(t)=A_c exp[j\beta \sin (2\pi f_m t)]=\sum^{\infty} \_{n=-\infty} C_n exp(j2\pi nf_m t)$, 週期$T_m=\frac{1}{f_m}$ </br>
其中，$C_n=\int ^{\frac{1}{2f_m}}_{\frac{-1}{2f_m}}A_c exp[j\beta sin(2\pi f_m t)]exp(-j2\pi nf_m t)dt$ </br>
令$x=2\pi f_m t \rightarrow C_n=\frac{A_c}{2\pi}\int ^{\pi}\_{-\pi}exp[j(\beta sinx-nx)]dx=A_c J_n(\beta)$ </br>
Bessel function $J_n(\beta)=\frac{1}{2\pi}\int ^{\pi}\_{-\pi}exp[j(\beta sinx-nx)]dx$ </br>
</br>
$S(t)=A_c Re[\sum _{n=-\infty}^{\infty} J_n(\beta)e^{j2\pi (f_c+nf_m)t}]=A_c \sum _{n=-\infty}^{\infty} J_n(\beta)\cos[2\pi (f_c+nf_m)t]$ </br>
Fourier Transform $\rightarrow S(f)=\frac{A_c}{2}\sum _{n=-\infty}^{\infty}J_n(\beta)[\delta (f-f_c-nf_m)+\delta (f+f_c+nf_m)]$ </br>

> [Bessel function](https://zh.wikipedia.org/wiki/%E8%B4%9D%E5%A1%9E%E5%B0%94%E5%87%BD%E6%95%B0) </br>
> 1. $J_n(\beta)=(-1)^n J_{-n}(\beta)$ </br>
> 2. $\sum ^{\infty}_{n=-\infty}J_n ^2(\beta)=1$ </br>
> 3. For $\beta \ll 1$, $J_0(\beta)\simeq 1$, $J_1(\beta)\simeq \frac{\beta}{2}$, $J_n(\beta)\simeq 0$ for $n\geq 2$ </br>

##### NBFM
**$\beta<<1$**
$S(f)\sim \frac{A_c}{2} [\delta (f-f_c)+\delta(f+f_c)]+\frac {\beta A_c}{4}[\delta (f-f_c-f_m)+\delta (f+f_c+f_m)]-\frac {\beta A_c}{4}[\delta (f-f_c+f_m)+\delta (f+f_c-f_m)]$ </br>
![NBFM_spectrum](https://github.com/ChenBlue/Communication-System-Note/blob/master/Angle_Modulation/Material/NBFM_spectrum.PNG) </br>
\\\TODO
http://www.edaboard.com/thread236069.html
