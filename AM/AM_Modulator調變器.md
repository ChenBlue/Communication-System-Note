# AM調變 (Amplitude Modulation)
發射信號為 $S(t)=A_c [1+k_a m(t)]cos(2\pi f_c t)$

## AM調變器 (Modulator)
1. 平方律調變器(Square Law Modulator) </br>
![square_modulator](https://github.com/ChenBlue/Communication-System-Note/blob/master/AM/square_modulator.jpg) </br>
$V_2 (t)=a_1 V_1 (t)+a_2 V_1 ^2 (t)$ </br>
$V_1 (t)=Acos(2\pi f_c t)+m(t)$ </br>
→ $V_2 (t)=a_1 [m(t)+Acos(2\pi f_c t)]+a_2 [m(t)+Acos(2\pi f_c t)]^2 =a_1 m(t)+a_2 m^2 (t)+a_1 A[1+\frac{2a_2 }{a_1 }m(t)]cos(2\pi f_c t)+a_2 A^2 cos^2 (2\pi f_c t)$
