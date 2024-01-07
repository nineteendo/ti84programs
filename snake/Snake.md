### Chapter Zero - Zoom
### Chapter One - Auto Movement
ClrDraw   
4−>C  
8−>D  
C−>F  
D−>G  
DelVar Y  
Repeat 0  
Text(8C,6D,"O  
If Y>ᴇ2  
DelVar YPause  
Text(8F,6G,”SPACE SPACE SPACE  
remainder(G+1,16−>G  
D+1  
If Ans>15  
15-D  
Ans−>D  
Y+1−>Y  
End
### Chapter Two - Manual Movement
ClrDraw  
**DelVar B**4−>C  
8−>D  
C−>F  
D−>G  
DelVar Y **{0−>L₁**  
Repeat 0  
Text(8C,6D,"O  
**getKey-21  
If Ans=13  
6**  
If Y>ᴇ2 **or Ans=84**  
DelVar YPause  
**If 3≤Ans and Ans≤6 and 2≠abs(B-Ans  
DelVar YAns−>B  
While 3<dim(L₁  
L₁(3−>E  
If E**  
Text(8F,6G,”SPACE SPACE SPACE  
**remainder(F+8+(E-5)(E≥4),8−>F**  
remainder(G+1 **6-(E=3)+(E=5)**,16−>G  
**3−>dim(L₁  
End  
C+(B-5)(B≥4  
If Ans>7 or Ans<0  
7-C  
Ans−>C**  
D+~~1~~ **(B=5)-(B=3**  
If Ans>15 **or Ans<0**  
15-D  
Ans−>D  
Y+1−>Y  
**augment({B},L₁→L₁**  
End
### Chapter Three - Eating Fruit
ClrDraw  
**DelVar A** DelVar B4−>C  
8−>D  
C−>F  
D−>G  
**C−>H  
D−>I**  
DelVar Y{0−>L₁  
Repeat ~~0~~ **Bpxl-Test(8C+1,6D**  
Text(8C,6D,"O  
getKey-21  
If Ans=13  
6  
If Y>ᴇ2 or Ans=84  
DelVar YPause   
If 3≤Ans and Ans≤6 and 2≠abs(B-Ans  
DelVar YAns−>B  
**While C=H and D=I  
While pxl-Test(8H+3,6I  
randInt(0,7−>H  
randInt(0,15−>I  
End  
Text(8H,6I,"+  
A+1−>A  
End**  
While ~~3~~ **A**<dim(L₁  
L₁(~~3~~ **A**−>E  
If E  
Text(8F,6G,”SPACE SPACE SPACE  
remainder(F+8+(E-5)(E≥4),8−>F  
remainder(G+16-(E=3)+(E=5),16−>G  
~~3~~ **A**−>dim(L₁  
End  
C+(B-5)(B≥4  
If Ans>7 or Ans<0  
7-C  
Ans−>C  
D-(B=3)+(B=5  
If Ans>15 or Ans<0  
15-D  
Ans−>D  
Y+1−>Y  
augment({B},L₁→L₁  
End  
**A**
### Chapter Four - Variations
#### Variation One - CLASSIC
ClrDraw  
DelVar ADelVar B4−>C  
8−>D  
C−>F  
D−>G  
C−>H  
D−>I  
**0−>K**  
DelVar Y{0−>L₁  
Repeat Bpxl-Test(8C+1,6D  
Text(8C,6D,"O  
getKey-21  
If Ans=13  
6  
If Y>ᴇ2 or Ans=84  
DelVar YPause   
If 3≤Ans and Ans≤6 and 2≠abs(B-Ans  
DelVar YAns−>B  
While C=H and D=I  
While pxl-Test(8H+3,6I  
randInt(0,7−>H  
randInt(0,15−>I  
End  
Text(8H,6I,"+  
A+1−>A  
End  
While A<dim(L₁  
L₁(A−>E  
If E  
Text(8F,6G,”SPACE SPACE SPACE  
remainder(F+8+(E-5)(E≥4),8−>F  
remainder(G+16-(E=3)+(E=5),16−>G  
A−>dim(L₁  
End  
C+(B-5)(B≥4  
If Ans>7 or Ans<0  
**abs(K**7-C  
Ans−>C  
D-(B=3)+(B=5  
If Ans>15 or Ans<0  
**abs(K**15-D  
Ans−>D  
Y+1->Y  
augment({B},L₁→L₁  
End  
A
#### Variation Two - Better Food
ClrDraw  
~~DelVar A~~ **_1-GROWTH_** **−>Α**  
DelVar B4−>C  
8−>D  
C−>F  
D−>G  
C−>H  
D−>I  
0−>K  
DelVar Y{0−>L₁  
Repeat Bpxl-Test(8C+1,6D  
Text(8C,6D,"O  
getKey-21  
If Ans=13  
6  
If Y>ᴇ2 or Ans=84  
DelVar YPause   
If 3≤Ans and Ans≤6 and 2≠abs(B-Ans  
DelVar YAns−>B  
While C=H and D=I  
While pxl-Test(8H+3,6I  
randInt(0,7−>H  
randInt(0,15−>I  
End  
Text(8H,6I,"+  
A+~~1~~ **_GROWTH_** −>A  
End  
While A<dim(L₁  
L₁(A−>E  
If E  
Text(8F,6G,”SPACE SPACE SPACE  
remainder(F+8+(E-5)(E≥4),8−>F  
remainder(G+16-(E=3)+(E=5),16−>G  
A−>dim(L₁  
End  
C+(B-5)(B≥4  
If Ans>7 or Ans<0  
abs(K7-C  
Ans−>C  
D-(B=3)+(B=5  
If Ans>15 or Ans<0  
abs(K15-D  
Ans−>D  
Y+1->Y  
augment({B},L₁→L₁  
End  
A
#### Variation Three - Longest Snake
ClrDraw  
**_LENGTH-GROWTH_** −>A  
DelVar B4−>C  
8−>D  
C−>F  
D−>G  
C−>H  
D−>I  
0−>K  
DelVar Y{0−>L₁  
Repeat Bpxl-Test(8C+1,6D  
Text(8C,6D,"O  
getKey-21  
If Ans=13  
6  
If Y>ᴇ2 or Ans=84  
DelVar YPause   
If 3≤Ans and Ans≤6 and 2≠abs(B-Ans  
DelVar YAns−>B  
While C=H and D=I  
While pxl-Test(8H+3,6I  
randInt(0,7−>H  
randInt(0,15−>I  
End  
Text(8H,6I,"+  
A+_GROWTH_ −>A  
End  
While A<dim(L₁  
L₁(A−>E  
If E  
Text(8F,6G,”SPACE SPACE SPACE  
remainder(F+8+(E-5)(E≥4),8−>F  
remainder(G+16-(E=3)+(E=5),16−>G  
A−>dim(L₁  
End  
C+(B-5)(B≥4  
If Ans>7 or Ans<0  
abs(K7-C  
Ans−>C  
D-(B=3)+(B=5  
If Ans>15 or Ans<0  
abs(K15-D  
Ans−>D  
Y+1->Y  
augment({B},L₁→L₁  
End  
A
#### Variation Four - TI-82 Edition
ClrDraw  
_LENGTH-GROWTH_ −>A  
DelVar B4−>C  
~~8~~ **11** −>D  
C−>F  
D−>G  
C−>H  
D−>I  
0−>K  
DelVar Y{0−>L₁  
Repeat Bpxl-Test(86C+1,64D  
Text(~~8~~ **6** C,~~6~~ **4** D,"O  
getKey-21  
If Ans=13  
6  
If Y>ᴇ2 or Ans=84  
DelVar YPause   
If 3≤Ans and Ans≤6 and 2≠abs(B-Ans  
DelVar YAns−>B  
While C=H and D=I  
While pxl-Test(~~8~~ **6** H+3,~~6~~ **4**I  
randInt(0,~~7~~ **9** −>H  
randInt(0,~~15~~ **22** −>I  
End  
Text(~~8~~ **6** H,~~6~~ **4**I,”+  
A+_GROWTH_ −>A  
End  
While A<dim(L₁  
L₁(A−>E  
If E  
Text(~~8~~ **6** F,~~6~~ **4**G,”     
remainder(F+~~8~~ **10**+(E-5)(E≥4),~~8~~ **10**−>F  
remainder(G+~~16~~ **23**-(E=3)+(E=5),~~16~~ **23**−>G  
A−>dim(L₁  
End  
C+(B-5)(B≥4  
If Ans>~~7~~ **9**  or Ans<0  
abs(K~~7~~ **9** -C  
Ans−>C  
D-(B=3)+(B=5  
If Ans>~~15~~ **22** or Ans<0  
abs(K~~15~~ **22** -D  
Ans−>D  
Y+1->Y  
augment({B},L₁→L₁  
End  
A  
#### Variation Five - TI-84 Edition
ClrDraw  
_LENGTH-GROWTH_ −>A  
DelVar B4−>C  
~~11~~ **8**−>D  
C−>F  
D−>G  
C−>H  
D−>I  
0−>K  
DelVar Y{0−>L₁  
Repeat Bpxl-Test(~~6~~ **8** C+1,~~4~~ **6** D  
Text(~~6~~ **-1,8** C,~~4~~ **6** D,"O  
getKey-21  
If Ans=13  
6  
If Y>ᴇ2 or Ans=84  
DelVar YPause   
If 3≤Ans and Ans≤6 and 2≠abs(B-Ans  
DelVar YAns−>B  
While C=H and D=I  
While pxl-Test(~~6~~ **8** H+~~3~~ **2**,~~4~~ **6** I  
randInt(0,~~9~~ **7**−>H  
randInt(0,~~22~~ **15**−>I  
End  
Text(~~6~~ **-1,8** H,~~4~~ **6** I,”+*  
A+_GROWTH_ −>A  
End  
While A<dim(L₁  
L₁(A−>E  
If E  
Text(~~6~~ **-1,8** F,~~4~~ **6** G,”SPACE ~~SPACE SPACE~~  
remainder(F+~~10~~**8**+(E-5)(E≥4),~~10~~**8**−>F  
remainder(G+~~23~~ **16**-(E=3)+(E=5),~~23~~ **16**−>G  
A−>dim(L₁  
End  
C+(B-5)(B≥4  
If Ans>~~9~~ **7** or Ans<0   
abs(~~9~~ **7** K-C  
Ans−>C  
D-(B=3)+(B=5  
If Ans>~~22~~ **15** or Ans<0  
abs(~~22~~ **15**-D  
Ans−>D  
Y+1->Y  
augment({B},L₁→L₁  
End  
A
