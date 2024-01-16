# Jump Twice tutorial

## Zoom

Zoom: https://github.com/nineteendo/ti-84-plus-programs/tree/master/zoom

## Creating a moving pixel

```ti-basic
ClrDraw
61→A
1→B
While B≠94
    A→C
    B→D
    B+1→B
    Pxl-Off(C,D
    Pxl-On(A,B
End
```

## Loading a level

```ti-basic
ClrDraw
Vertical 0
For(θ,0,11
    Line(9θ,θ,9θ+5+3,θ
End
Repeat B=94
    61→A
    1→B
    While B≠94
        A→C
        B→D
        B+1→B
        Pxl-Off(C,D
        Pxl-On(A,B
    End
End
```

## Controlling the pixel

```ti-basic
ClrDraw
Vertical 0
For(θ,0,11
    Line(9θ,θ,9θ+5+3,θ
End
Repeat B=94
    61→A
    1→B
    1→E
    DelVar F
    1→I
    While B≠94
        A→C
        B→D
        For(θ,0,5
            getKey
            If Ans=105
            Then
                If pxl-Test(A+1,B)A,B-E
                    DelVar I
                If pxl-Test(A,B-E)not(pxl-Test(A+1,B
                    –E→E
                If I<2
                Then
                    I+1→I
                    1→F
                End
            End
        End
        (F<4)(F+not(not(F→F
        B-Enot(pxl-Test(A,B-E→B
        A+not(F or pxl-Test(A+1,B))-(F and not(pxl-Test(A-1,B→A
        Pxl-Off(C,D
        Pxl-On(A,B
    End
End
```

## Finishing the game

```ti-basic
ClrDraw
Text(–1,5,30,"Jump*2
Text(–1,31,27,"[Enter]
Text(57,19,"2019 Nineteendo  // 1 space before Nineteendo
1→H
94→X
Pause 
For(G,0,4
    ClrDraw
    Vertical 0
    1
    If G=3
    Then
        For(θ,0,7
            Line(10θ,20,10θ,30
        End
    End
    If G=2
    Then
        For(X,1,93
            Line(X,0,X,Ans
            Ans+randInt(2(Ans<57),–(Ans>9
        End
    End
    If G<2
    Then
        For(θ,0,11
            Line(9θ,θ,9θ+5+3not(G),θ
        End
    End
    Repeat B=X
        61→A
        If G=3
            36→A
        1→B
        –1→E
        DelVar F1→I
        Text(0,2,G,"-",H
        While B≠X and A<62
            A→C
            B→D
            For(θ,0,5
                getKey
                If Ans=105
                Then
                    If pxl-Test(A+1,B)A,B-E
                        DelVar I
                    If pxl-Test(A,B-E)not(pxl-Test(A+1,B
                        –E→E
                    If I<2
                    Then
                        I+1→I
                        1→F
                    End
                End
            End
            (F<4)(F+not(not(F→F
            B-Enot(pxl-Test(A,B-E→B
            A+not(F or pxl-Test(A+1,B))-(F and not(pxl-Test(A-1,B→A
            Pxl-Off(C,D
            Pxl-On(A,B
        End
        H+(B≠X→H
    End
End
"
```