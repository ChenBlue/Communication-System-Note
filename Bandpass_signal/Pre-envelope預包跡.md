# 帶通訊號 Bandpass signal
利用較高頻的載波訊號來傳遞我們想傳的訊息，將此訊號畫出頻譜，會發現頻譜會落在兩側，因此我們將其稱為帶通訊號(Bandpass signal)。詳情可以參照以下網址
http://www.ni.com/white-paper/3013/zht/  

# Pre-envelope 預包跡 & Complex-envelope 複包跡
而當我們在處理一個帶通訊號時，我們可以將帶通訊號簡化成一個低頻的訊號來看，這樣子計算上會較簡單，此簡化後的低頻訊號即為複包跡也是我們想傳遞的訊息。  
  
若g(t)為以f<sub>c</sub>為中心頻率的帶通訊號。  

預包跡Pre-envelope:$g\_{+}(t)=g(t)+j\hat{g}(t)=\widetilde{g(t)}e\^{j2\pi f\_{0}t}=[g\_{I}(t)+jg\_{Q}(t)]e\^{j2\pi f\_{0}t}=[A(t)e\^{j\phi t}]e\^{j2\pi f\_{0}t}$
	

> 註： $\hat{g}(t)$ 是g(t)的Hilbert Transform，詳情請參閱https://zh.wikipedia.org/wiki/%E5%B8%8C%E7%88%BE%E4%BC%AF%E7%89%B9%E8%BD%89%E6%8F%9B  
  
預包跡經傅立葉轉換後得到的頻譜為：  
  
$G\_{+}(f)=G(f)+j[-jsgn(f)G(f)]=[1+sgn(f)]G(f)=2G(f)$, if f>0  
> 口訣：正頻率乘2倍

# Spectrum of pre-envelope & complex envelope
帶通訊號g(t) → G(f)  
![alt text](https://github.com/ChenBlue/Communication-System-Note/blob/master/Bandpass_signal/G(f).png)



