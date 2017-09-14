# 帶通訊號 Bandpass signal
利用較高頻的載波訊號來傳遞我們想傳的訊息，將此訊號畫出頻譜，會發現頻譜會落在兩側，因此我們將其稱為帶通訊號(Bandpass signal)。詳情可以參照以下網址
http://www.ni.com/white-paper/3013/zht/  </br>
## 載波訊號 Carrier signal
可以將載波訊號想像成一種交通工具，他可以承載我們想傳的訊息到遠方，而將原本的訊息加上載波訊號即為調變(Modulation)，接收端接收到調變訊號解調(Demodulation)後即可得到我們想傳遞的訊息。 </br>
載波訊號有不同的頻率，接收端只會選擇某些固定的頻率接收，這樣就可以接收到我們所要傳遞的訊息。打個比方，不一樣的頻率就好像不一樣的交通工具，而空氣中充滿了不同頻率的訊號，假設某個訊號搭載著火車(頻率1的載波)到遠方，而遠方的接收端已經設定好只會接收搭載著火車過來的訊號，而不會接收搭載著其他種類交通工具過來的訊號，因此接收端就可以從充滿不同訊號的空氣中接收到想要的訊號。 </br>

# Pre-envelope 預包跡 & Complex-envelope 複包跡
而當我們在處理一個帶通訊號時，我們可以將帶通訊號簡化成一個低頻的訊號來看，這樣子計算上會較簡單，此簡化後的低頻訊號即為複包跡也是我們想傳遞的訊息。  
  
若g(t)為以f<sub>c</sub>為中心頻率的帶通訊號。  

預包跡Pre-envelope: $g\_{+}(t)=g(t)+j\hat{g}(t)=\widetilde{g(t)}e\^{j2\pi f\_{0}t}=[g\_{I}(t)+jg\_{Q}(t)]e\^{j2\pi f\_{0}t}=[A(t)e\^{j\phi t}]e\^{j2\pi f\_{0}t}$
	

> 註： $\hat{g}(t)$ 是g(t)的Hilbert Transform，詳情請參閱https://zh.wikipedia.org/wiki/%E5%B8%8C%E7%88%BE%E4%BC%AF%E7%89%B9%E8%BD%89%E6%8F%9B  
  
預包跡經傅立葉轉換後得到的頻譜為：  
  
$G\_{+}(f)=G(f)+j[-jsgn(f)G(f)]=[1+sgn(f)]G(f)=2G(f)$, if f>0  
> 口訣：正頻率乘2倍
</br>

# Spectrum of pre-envelope & complex envelope
**帶通訊號g(t)** → G(f)  
![alt text](https://github.com/ChenBlue/Communication-System-Note/blob/master/Bandpass_signal/G(f).png)    
</br>
</br>
**預包跡Pre-envelope**: $g\_{+}(t)=g(t)+j\hat{g}(t)$ → $G\_{+}(f)$ </br>
![alt text](https://github.com/ChenBlue/Communication-System-Note/blob/master/Bandpass_signal/G%2B(f).png)    
</br> </br>
**複包跡Complex-envelope**: $\tilde{g}(t)=g\_{+}(t)e\^{-j2\pi f\_{0}t}=g\_{I}(t)+jg\_{Q}(t) → \tilde{G}(f)= G\_{+}(f+f\_{c})$ (預包跡回原點)</br>
![alt text](https://github.com/ChenBlue/Communication-System-Note/blob/master/Bandpass_signal/G~(f).png) </br>

	複包跡即為欲傳之訊號

**In phase component** of g(t): $g\_{I}(t)=Re[\tilde{g}(t)]=\frac{\tilde{g}(t)+\tilde{g}\^\* (t)}{2}$ </br>
$G\_{I}(f)=G(f-f\_{c})+G(f+f\_{c}),|f|<W$
</br> </br>
**Quadrature phase component** of g(t): $g\_{Q}(t)=Im[\tilde{g}(t)]=\frac{\tilde{g}(t)-\tilde{g}\^\* (t)}{2j}$ </br>
$\frac{1}{j}G\_{Q}(f)=G(f-f\_{c})-G(f+f\_{c}),|f|<W$
</br> </br>

# 帶通訊號等效表示法
1. $g(t)=Re[\tilde{g}(t)e\^{j2\pi f\_{0}t}]$
2. $g(t)=g\_I (t)cos(2\pi f_0 t)-g_Q (t)sin(2\pi f_0 t)$
3. $g(t)=A(t)cos(2\pi f_0 t+\phi (t))$, and 大小$A(t)=\sqrt{g_I ^2 (t)+g_Q ^2 (t)}$, 相位$\phi (t)=tan^-1 (\frac{g_Q (t)}{g_I (t)})$
