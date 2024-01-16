# Snake Tutorial

## Chapter Zero - Zoom

Zoom: https://github.com/nineteendo/ti-84-plus-programs/tree/master/zoom

## Chapter One - Auto Movement

```ti-basic
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
    Text(8F,6G,"     // 3 spaces
    remainder(G+1,16−>G
    D+1
    If Ans>15
        15-D
    Ans−>D
    Y+1−>Y
End
```

## Chapter Two - Manual Movement

```ti-basic
ClrDraw
DelVar B4−>C
8−>D
C−>F
D−>G
DelVar Y {0−>L₁
Repeat 0
    Text(8C,6D,"O
    getKey-21
    If Ans=13
        6
    If Y>ᴇ2 or Ans=84
        DelVar YPause
    If 3≤Ans and Ans≤6 and 2≠abs(B-Ans
        DelVar YAns−>B
    While 3<dim(L₁
        L₁(3−>E
        If E
            Text(8F,6G,"     // 3 spaces
        remainder(F+8+(E-5)(E≥4),8−>F
        remainder(G+1 6-(E=3)+(E=5),16−>G
        3−>dim(L₁
    End
    C+(B-5)(B≥4
    If Ans>7 or Ans<0
        7-C
    Ans−>C
    D+(B=5)-(B=3
    If Ans>15 or Ans<0
        15-D
    Ans−>D
    Y+1−>Y
    augment({B},L₁→L₁
End
```

## Chapter Three - Eating Fruit

```ti-basic
ClrDraw
DelVar ADelVar B4−>C
8−>D
C−>F
D−>G
C−>H
D−>I
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
            Text(8F,6G,"     // 3 spaces
        remainder(F+8+(E-5)(E≥4),8−>F
        remainder(G+16-(E=3)+(E=5),16−>G
        A−>dim(L₁
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
A
```

## Chapter Four - Variations
### Variation One - CLASSIC

```ti-basic
ClrDraw
DelVar ADelVar B4−>C
8−>D
C−>F
D−>G
C−>H
D−>I
0−>K  // change `0` to `1` for normal mode
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
            Text(8F,6G,"     // 3 spaces
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
```

### Variation Two - Better Food

```ti-basic
ClrDraw
1-7−>Α  // Change `7` for different growth
DelVar B4−>C
8−>D
C−>F
D−>G
C−>H
D−>I
0−>K  // change `0` to `1` for normal mode
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
        A+7−>A  // Change `7` for different growth
    End
    While A<dim(L₁
        L₁(A−>E
        If E
            Text(8F,6G,"     // 3 spaces
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
```

### Variation Three - Longest Snake

```ti-basic
ClrDraw
9-7−>A  // Change `9` for different length, `7` for different growth
DelVar B4−>C
8−>D
C−>F
D−>G
C−>H
D−>I
0−>K  // change `0` to `1` for normal mode
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
        A+7−>A  // Change `7` for different growth
    End
    While A<dim(L₁
        L₁(A−>E
        If E
            Text(8F,6G,"     // 3 spaces
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
```

### Variation Four - TI-82 Edition

```ti-basic
ClrDraw
9-7−>A  // Change `9` for different length, `7` for different growth
DelVar B4−>C
11−>D
C−>F
D−>G
C−>H
D−>I
0−>K  // change `0` to `1` for normal mode
DelVar Y{0−>L₁
Repeat Bpxl-Test(86C+1,64D
    Text(6C,4D,"O
    getKey-21
    If Ans=13
        6
    If Y>ᴇ2 or Ans=84
        DelVar YPause 
    If 3≤Ans and Ans≤6 and 2≠abs(B-Ans
        DelVar YAns−>B
    While C=H and D=I
        While pxl-Test(6H+3,4I
            randInt(0,9−>H
            randInt(0,22−>I
        End
        Text(6H,4I,"+
        A+7−>A  // Change `7` for different growth
    End
    While A<dim(L₁
        L₁(A−>E
        If E
            Text(6F,4G,"SPACE SPACE SPACE
        remainder(F+10+(E-5)(E≥4),10−>F
        remainder(G+23-(E=3)+(E=5),23−>G
        A−>dim(L₁
    End
    C+(B-5)(B≥4
    If Ans>9 or Ans<0
        abs(K9-C
    Ans−>C
    D-(B=3)+(B=5
    If Ans>22 or Ans<0
        abs(K22-D
    Ans−>D
    Y+1->Y
    augment({B},L₁→L₁
End
A
```

### Variation Five - TI-84 Edition

```ti-basic
ClrDraw
9-7−>A  // Change `9` for different length, `7` for different growth
DelVar B4−>C
8−>D
C−>F
D−>G
C−>H
D−>I
0−>K  // change `0` to `1` for normal mode
DelVar Y{0−>L₁
Repeat Bpxl-Test(8C+1,6D
    Text(-1,8C,6D,"O
    getKey-21
    If Ans=13
        6
    If Y>ᴇ2 or Ans=84
        DelVar YPause 
    If 3≤Ans and Ans≤6 and 2≠abs(B-Ans
        DelVar YAns−>B
    While C=H and D=I
        While pxl-Test(8H+2,6I
            randInt(0,7−>H
            randInt(0,15−>I
        End
        Text(-1,8H,6I,"+*
        A+7−>A  // Change `7` for different growth
    End
    While A<dim(L₁
        L₁(A−>E
        If E
            Text(8F,6G,"   // 1 space
        remainder(F+8+(E-5)(E≥4),8−>F
        remainder(G+16-(E=3)+(E=5),16−>G
        A−>dim(L₁
    End
    C+(B-5)(B≥4
    If Ans>7 or Ans<0 
        abs(7K-C
    Ans−>C
    D-(B=3)+(B=5
    If Ans>15 or Ans<0
        abs(15-D
    Ans−>D
    Y+1->Y
    augment({B},L₁→L₁
End
A
```