---
title:  "Elliptic Curve"
date: 2023-06-16
tags: ["math"]
math: true
---

Một vài ghi chú của mình khi tìm hiểu về Elliptic Curve cũng như những thứ liên quan tới nó, và 1 vài thứ linh tinh khác.

# Định nghĩa

Là 1 đường cong đại số có dạng
$$y^2 = x^3 + ax + b$$
với $a, b$ là hằng số.
Ví dụ:
![](https://upload.wikimedia.org/wikipedia/commons/d/d0/ECClines-3.svg#center)

# Tính chất
![](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c1/ECClines.svg/1020px-ECClines.svg.png)

- Elliptic Curve là một nhóm Abel, với $O$ là phần tử trung hoà (hoặc có cái tên ngầu hơn là **point at infinity**):
    - $P + O = O + P = P$
    - $P + (−P) = O$
    - $(P + Q) + R = P + (Q + R)$
    - $P + Q = Q + P$
- Elliptic Curve bao gồm phép cộng và phép nhân (bản chất là nhiều lần phép cộng). Ví dụ: $P + P = 2P,\ 2P + P = 3P$
    - $P + Q$: kẻ 1 đường thẳng nối $P$ và $Q$, đường thẳng này sẽ cắt đường cong elliptic tại 1 điểm, lấy đối xứng điểm đó qua trục tung $Ox$, gọi là $R$, ta được kết quả của phép tính $P+Q$.
    - $P + P$: Lúc này thì $R = P + P = 2P$ (đường thẳng trở thành tiếp tuyến của $P$)
- Tổng của $3$ điểm thẳng hàng nằm trên đường cong bằng phần tử trung hoà $O$ (hình 1).
- Algebraic curve of genus one. (này liên quan tới Algebra mà mình chưa chơi món này nhiều @@).
- Elliptic Curve không phải là hình Ellipse.
![](https://prateekvjoshi.files.wordpress.com/2015/02/1-main1.png)

# Ứng dụng
## Elliptic Curve Crytography (ECC)
### Linh tinh
- **Trapdoor function**:
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8f/Trapdoor_permutation.svg/1200px-Trapdoor_permutation.svg.png)
- **Asymmetric cryptography(Public key cryptography)**: 
![](https://assets.cdn.prod.twilio.com/images/19DfiKodi3T25Xz7g9EDTyvF9di2SzvJ.width-1616.format-webp.webp)

- **Symmetric cryptography**: 
![](https://assets.cdn.prod.twilio.com/images/z9ws4Rp8VZHoHpnhlh9I3QhAqiIdQZg6aSOlCCu1e5S.format-webp.webp)

- **Diffie–Hellman key exchange**: 
![](https://assets.cdn.prod.twilio.com/images/XTdQOAm3k7Q0_kVHMJG-qDcqLFAgL9uR968MInDZZZW.format-webp.webp)

---
Elliptic Curve ứng dụng rất nhiều vô mảng cryptography. Cụ thể, nó là một thuật toán thuộc loại public key cryptography, nó ngon hơn thuật toán [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)), nhưng ít được sử dụng hơn. Ngoài ra thì Bitcoin cũng sử dụng [NIST curve `secp256k1`](https://en.bitcoin.it/wiki/Secp256k1) với Elliptic Curve là $y^2 = x^3 + 7$. À và cả [Proton Mail](https://proton.me/mail) nữa (Curve25519).

Bạn có thể đọc thêm [thesis này](https://bearworks.missouristate.edu/cgi/viewcontent.cgi?article=4697&context=theses) để biết thêm 1 số ứng dụng của Elliptic Curve vào cryptography (tại nhiều quá nên mình cũng ngộp).

## Fermat's Last Theorem
Elliptic Curve còn có thể dùng để chứng minh định lý Fermat lớn (định lý không thể chứng minh được trong gần 4 thế kỉ): Không tồn tại các nghiệm nguyên dương $a, b, c$ thoả mãn $a^n + b^n = c^n$ với $n$ là một số nguyên lớn hơn $2$.

Về cách chứng minh thì mời các bạn đọc cách chứng minh của [Andrew Wiles](https://en.wikipedia.org/wiki/Wiles%27s_proof_of_Fermat%27s_Last_Theorem)  ~~chứ mình đọc cũng không hiểu~~.

## Lenstra elliptic-curve factorization 
Là thuật toán phân tách thừa số nguyên tố nhanh thứ 3 theo [Wiki](https://en.wikipedia.org/wiki/Lenstra_elliptic-curve_factorization). 

Có thể còn nhiều ứng dụng nữa mà mình không biết...

# References
- [https://en.wikipedia.org/wiki/Elliptic_curve](https://en.wikipedia.org/wiki/Elliptic_curve)
- [https://www.twilio.com/blog/what-is-public-key-cryptography](https://www.twilio.com/blog/what-is-public-key-cryptography)
- [https://cryptohack.org/courses/elliptic/bg/](https://cryptohack.org/courses/elliptic/bg/)
- [https://cryptobook.nakov.com/asymmetric-key-ciphers/elliptic-curve-cryptography-ecc](https://cryptobook.nakov.com/asymmetric-key-ciphers/elliptic-curve-cryptography-ecc)
-  Understanding Cryptography: A Textbook for Students and Practitioners - Christof Paar, Jan Pelzl

Nếu bạn muốn ~~đau khổ~~ tìm hiểu sâu về Elliptic Curve thì cuốn The Arithmetic of Elliptic Curves - Joseph H. Silverman dành cho bạn.
