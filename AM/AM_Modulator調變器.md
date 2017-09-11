# AM調變 (Amplitude Modulation)
發射信號為 $S(t)=A_c [1+k_a m(t)]cos(2\pi f_c t)$

## AM調變器 (Modulator)
m(t)為我們所要傳遞的訊號，經過這些調變器後，將會可以得到AM訊號
### 平方律調變器(Square Law Modulator) </br>
![square_modulator](https://github.com/ChenBlue/Communication-System-Note/blob/master/AM/square_modulator.jpg) </br>
$V_2 (t)=a_1 V_1 (t)+a_2 V_1 ^2 (t)$ </br>
$V_1 (t)=Acos(2\pi f_c t)+m(t)$ </br>
→ $V_2 (t)=a_1 [m(t)+Acos(2\pi f_c t)]+a_2 [m(t)+Acos(2\pi f_c t)]^2 $ </br>
$=a_1 m(t)+a_2 m^2 (t)+a_1 A[1+\frac{2a_2 }{a_1 }m(t)]cos(2\pi f_c t)+a_2 A^2 cos^2 (2\pi f_c t)$　</br>
</br>
若$V_2 (t)$經過中心頻率為$f_c$之帶通濾波器，可得 </br>
$S(t)=a_1 A[1+\frac{2a_2 }{a_1 }m(t)]cos(2\pi f_c t)=A_c [1+k_a m(t)]cos(2\pi f_c t)$

### 交換式調變器 (Switching Modulator)
![swithcing_modulator](https://github.com/ChenBlue/Communication-System-Note/blob/master/AM/switching-modulator.png) </br>
$V_1 (t)=A_c cos(2\pi f_c t)+m(t) → V_2(t)~[Acos(2\pi f_c t)+m(t)]g\_{T_0} (t)$ </br>
$g\_{T_0} (t)$是週期週期性脈衝串(Periodic pulse train) </br>
![swithcing_modulator](https://github.com/ChenBlue/Communication-System-Note/blob/master/AM/periodic_pulse_train.jpg) </br>
先找出$g\_{T_0}(t)$的Fourier Series: $g\_{T_0}(t)=\sum_{i=-\infty}^{\infty} a_k exp(jk2\pi f_c t)$ </br>
$a_0=\frac{1}{T_0}  \int\_{\frac{-T_0}{4}}\^{\frac{T_0}{4}}1\ \mathrm{d}t=\frac{1}{2}$</br>
$a_k=\frac{1}{T_0}  \int\_{\frac{-T_0}{4}}\^{\frac{T_0}{4}}exp(-jk2\pi f_c t)\ \mathrm{d}t=\frac{sin(\frac{1}{2}k\pi )}{k\pi }$ → if k is even, $a_k=0$ </br>
$g\_{T_0}(t)=...+\frac{1}{\pi}exp(-j2\pi f_ct)+\frac{1}{2}+\frac{1}{\pi}exp(j2\pi f_c t)+...=\frac{1}{2}+\frac{2}{\pi}\sum_{n=1}^{\infty}\frac{-1^{n-1}}{2n-1}cos(2\pi f_c t(2n-1))$
