## 条件付き確率密度関数
確率変数\\(X\\)がとる微小事象を\\(dA=\\{\omega| x < X(\omega) < x + dx\\}\\),確率変数\\(Y\\)がとる微小事象を\\(dB=\\{\omega| y < Y(\omega) < y + dy\\}\\)とすると,
\\(P(dB)=f_Y(y)dy,P(dA \cap dB)=f_{X,Y}(x,y)dxdy\\)となるので,
\\[
	P(dA|dB) = \frac{P(dA \cap dB)}{P(dB)} = \frac{f _{X,Y}(x,y) dy dx}{f _{Y}(y) dy} = \frac{f _{X,Y}(x,y) dx}{f _{Y}(y)}
\\]
ここで,\\(P(dA|dB)=dP(A|B)\\)とした時,
\\[
	P(dA|dB) = dP(A|B) = \frac{f _{X,Y}(x,y) dx}{f _{Y}(y)}
\\]
\\[
	P(A|B) = \int dP(A|B) = \int _{\\{\omega|\omega \in A\\}} \frac{f _{X,Y}(x,y) }{f _{Y}(y)} dx
\\]
\\[
\frac{dP(A|B)}{dx} = \frac{f _{X,Y}(x,y)}{f _{Y}(y)}
\\]
\\(\frac{f _{X,Y}(x,y)}{f _{Y}(y)} = f _{X|Y}(x,y)\\)と書いて,\\(X\\)の条件付き確率密度関数とする.
\\[
P(\Omega|B) = \frac{P(\Omega \cap B)}{P(B)} = 1
\\]
と同様,
\\[
\int ^{\infty} _{-\infty} f _{X|Y}(x,y) dx = \int ^{\infty} _{-\infty} \frac{f _{X,Y}(x,y)}{f _{Y} (y)} dx = \frac{f _{Y} (y)}{f _{Y} (y)} = 1
\\]
