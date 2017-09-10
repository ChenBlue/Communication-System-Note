# 帶通訊號 Bandpass signal
利用較高頻的載波訊號來傳遞我們想傳的訊息，將此訊號畫出頻譜，會發現頻譜會落在兩側，因此我們將其稱為帶通訊號(Bandpass signal)。詳情可以參照以下網址
http://www.ni.com/white-paper/3013/zht/  

# Pre-envelope 預包跡
而當我們在處理一個帶通訊號時，我們可以將帶通訊號簡化成一個低頻的訊號來看，這樣子計算上會較簡單，此簡化後的低頻訊號即為預包跡也是我們想傳遞的訊息。  
  
若g(t)為以f<sub>c</sub>為中心頻率的帶通訊號。  

$$ evidence\_{i}=\sum\_{j}W\_{ij}x\_{j}+b\_{i} $$

$x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$ 
其預包跡 $g\_{+}(t)=g(t)+j\hat{g}(t)=\widetilde{g(t)}e\^{2\pi}=$  
${g\_{I}(t)+jg\_{Q}(t)]e\^{2\pi f\_{0}t}$
