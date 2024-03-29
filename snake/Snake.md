# Snake Tutorial

## Chapter Zero - Zoom

Zoom: https://github.com/nineteendo/ti-84-plus-programs/tree/master/zoom

## Chapter One - Auto Movement

```ti-basic
ClrDraw
4->C
8->D
C->F
D->G
DelVar Y
Repeat 0
    Text(8C,6D,"O
    If Y>ᴇ2
        DelVar YPause
    Text(8F,6G,"     // 3 spaces
    remainder(G+1,16->G
    D+1
    If Ans>15
        15-D
    Ans->D
    Y+1->Y
End
```

## Chapter Two - Manual Movement

```diff
 ClrDraw
-4->C
+DelVar B4->C
 8->D
 C->F
 D->G
-DelVar Y
+DelVar Y{0->L₁
 Repeat 0
     Text(8C,6D,"O
+    getKey-21
+    If Ans=13
+        6
-    If Y>ᴇ2
+    If Y>ᴇ2 or Ans=84
         DelVar YPause
+    If Ans≥3 and Ans≤6 and 2≠abs(B-Ans
+        DelVar YAns->B
+    While 3<dim(L₁
+        L₁(3->E
+        If E
             Text(8F,6G,"     // 3 spaces
+        remainder(F+8+(E-5)(E≥4),8->F
-        remainder(G+1,16->G
+        remainder(G+16-(E=3)+(E=5),16->G
+        3->dim(L₁
+    End
+    C+(B-5)(B≥4
+    If Ans>7 or Ans<0
+        7-C
+    Ans->C
-    D+1
-    If Ans>15
+    D-(B=3)+(B=5
+    If Ans>15 or Ans<0
         15-D
     Ans->D
     Y+1->Y
+    augment({B},L₁→L₁
 End
```

## Chapter Three - Eating Fruit

```diff
 ClrDraw
-DelVar B4->C
+DelVar ADelVar B4->C
 8->D
 C->F
 D->G
+C->H
+D->I
 DelVar Y{0->L₁
-Repeat 0
+Repeat Bpxl-Test(8C+1,6D
     Text(8C,6D,"O
     getKey-21
     If Ans=13
         6
     If Y>ᴇ2 or Ans=84
         DelVar YPause 
     If Ans≥3 and Ans≤6 and 2≠abs(B-Ans
         DelVar YAns->B
+    While C=H and D=I
+        While pxl-Test(8H+3,6I
+            randInt(0,7->H
+            randInt(0,15->I
+        End
+        Text(8H,6I,"+
+        A+1->A
+    End
-    While 3<dim(L₁
-        L₁(3->E
+    While A<dim(L₁
+        L₁(A->E
         If E
             Text(8F,6G,"     // 3 spaces
         remainder(F+8+(E-5)(E≥4),8->F
         remainder(G+1 6-(E=3)+(E=5),16->G
-        3->dim(L₁
+        A->dim(L₁
     End
     C+(B-5)(B≥4
     If Ans>7 or Ans<0
         7-C
     Ans->C
     D-(B=3)+(B=5
     If Ans>15 or Ans<0
         15-D
     Ans->D
     Y+1->Y
     augment({B},L₁→L₁
 End
+A
```

## Chapter Four - Variations

### Variation One - CLASSIC

```diff
 ClrDraw
 DelVar ADelVar B4->C
 8->D
 C->F
 D->G
 C->H
 D->I
+0->K  // change `0` to `1` for normal mode
 DelVar Y{0->L₁
 Repeat Bpxl-Test(8C+1,6D
     Text(8C,6D,"O
     getKey-21
     If Ans=13
         6
     If Y>ᴇ2 or Ans=84
         DelVar YPause 
     If Ans≥3 and Ans≤6 and 2≠abs(B-Ans
         DelVar YAns->B
     While C=H and D=I
         While pxl-Test(8H+3,6I
             randInt(0,7->H
             randInt(0,15->I
         End
         Text(8H,6I,"+
         A+1->A
     End
     While A<dim(L₁
         L₁(A->E
         If E
             Text(8F,6G,"     // 3 spaces
         remainder(F+8+(E-5)(E≥4),8->F
         remainder(G+16-(E=3)+(E=5),16->G
         A->dim(L₁
     End
     C+(B-5)(B≥4
     If Ans>7 or Ans<0
-        7-C
+        abs(7K-C
     Ans->C
     D-(B=3)+(B=5
     If Ans>15 or Ans<0
-        15-D
+        abs(15K-D
     Ans->D
     Y+1->Y
     augment({B},L₁→L₁
 End
 A
```

### Variation Two - Better Food

```diff
 ClrDraw
-DelVar ADelVar B4->C
+1-7->Α  // Change `7` for different growth
+DelVar B4->C
 8->D
 C->F
 D->G
 C->H
 D->I
 0->K  // change `0` to `1` for normal mode
 DelVar Y{0->L₁
 Repeat Bpxl-Test(8C+1,6D
     Text(8C,6D,"O
     getKey-21
     If Ans=13
         6
     If Y>ᴇ2 or Ans=84
         DelVar YPause 
     If Ans≥3 and Ans≤6 and 2≠abs(B-Ans
         DelVar YAns->B
     While C=H and D=I
         While pxl-Test(8H+3,6I
             randInt(0,7->H
             randInt(0,15->I
         End
         Text(8H,6I,"+
-        A+1->A
+        A+7->A  // Change `7` for different growth
     End
     While A<dim(L₁
         L₁(A->E
         If E
             Text(8F,6G,"     // 3 spaces
         remainder(F+8+(E-5)(E≥4),8->F
         remainder(G+16-(E=3)+(E=5),16->G
         A->dim(L₁
     End
     C+(B-5)(B≥4
     If Ans>7 or Ans<0
         abs(7K-C
     Ans->C
     D-(B=3)+(B=5
     If Ans>15 or Ans<0
         abs(15K-D
     Ans->D
     Y+1->Y
     augment({B},L₁→L₁
 End
 A
```

### Variation Three - Longest Snake

```diff
-1-7->Α  // Change `7` for different growth
+9-7->A  // Change `9` for different length, `7` for different growth
 DelVar B4->C
 8->D
 C->F
 D->G
 C->H
 D->I
 0->K  // change `0` to `1` for normal mode
 DelVar Y{0->L₁
 Repeat Bpxl-Test(8C+1,6D
     Text(8C,6D,"O
     getKey-21
     If Ans=13
         6
     If Y>ᴇ2 or Ans=84
         DelVar YPause 
     If Ans≥3 and Ans≤6 and 2≠abs(B-Ans
         DelVar YAns->B
     While C=H and D=I
         While pxl-Test(8H+3,6I
             randInt(0,7->H
             randInt(0,15->I
         End
         Text(8H,6I,"+
         A+7->A  // Change `7` for different growth
     End
     While A<dim(L₁
         L₁(A->E
         If E
             Text(8F,6G,"     // 3 spaces
         remainder(F+8+(E-5)(E≥4),8->F
         remainder(G+16-(E=3)+(E=5),16->G
         A->dim(L₁
     End
     C+(B-5)(B≥4
     If Ans>7 or Ans<0
         abs(7K-C
     Ans->C
     D-(B=3)+(B=5
     If Ans>15 or Ans<0
         abs(15K-D
     Ans->D
     Y+1->Y
     augment({B},L₁→L₁
 End
 A
```

### Variation Four (A) - TI-82 Edition

```diff
 ClrDraw
 9-7->A  // Change `9` for different length, `7` for different growth
 DelVar B4->C
-8->D
+11->D
 C->F
 D->G
 C->H
 D->I
 0->K  // change `0` to `1` for normal mode
 DelVar Y{0->L₁
-Repeat Bpxl-Test(8C+1,6D
-    Text(8C,6D,"O
+Repeat Bpxl-Test(6C+1,4D
+    Text(6C,4D,"O
     getKey-21
     If Ans=13
         6
     If Y>ᴇ2 or Ans=84
         DelVar YPause 
     If Ans≥3 and Ans≤6 and 2≠abs(B-Ans
         DelVar YAns->B
     While C=H and D=I
-        While pxl-Test(8H+3,6I
-            randInt(0,7->H
-            randInt(0,15->I
+        While pxl-Test(6H+3,4I
+            randInt(0,9->H
+            randInt(0,22->I
         End
-        Text(8H,6I,"+
+        Text(6H,4I,"+
         A+7->A  // Change `7` for different growth
     End
     While A<dim(L₁
         L₁(A->E
         If E
-            Text(8F,6G,"     // 3 spaces
-        remainder(F+8+(E-5)(E≥4),8->F
-        remainder(G+16-(E=3)+(E=5),16->G
+            Text(6F,4G,"     // 3 spaces
+        remainder(F+10+(E-5)(E≥4),10->F
+        remainder(G+23-(E=3)+(E=5),23->G
         A->dim(L₁
     End
     C+(B-5)(B≥4
-    If Ans>7 or Ans<0
-        abs(7K-C
+    If Ans>9 or Ans<0
+        abs(9K-C
     Ans->C
     D-(B=3)+(B=5
-    If Ans>15 or Ans<0
-        abs(15K-D
+    If Ans>22 or Ans<0
+        abs(22K-D
     Ans->D
     Y+1->Y
     augment({B},L₁→L₁
 End
 A
```

### Variation Four (B) - TI-84 Edition

```diff
 ClrDraw
 9-7->A  // Change `9` for different length, `7` for different growth
 DelVar B4->C
 8->D
 C->F
 D->G
 C->H
 D->I
 0->K  // change `0` to `1` for normal mode
 DelVar Y{0->L₁
 Repeat Bpxl-Test(8C+1,6D
-    Text(8C,6D,"O
+    Text(-1,8C,6D,"O
     getKey-21
     If Ans=13
         6
     If Y>ᴇ2 or Ans=84
         DelVar YPause 
     If Ans≥3 and Ans≤6 and 2≠abs(B-Ans
         DelVar YAns->B
     While C=H and D=I
-        While pxl-Test(8H+3,6I
+        While pxl-Test(8H+2,6I
             randInt(0,7->H
             randInt(0,15->I
         End
-        Text(8H,6I,"+
+        Text(-1,8H,6I,"*
         A+7->A  // Change `7` for different growth
     End
     While A<dim(L₁
         L₁(A->E
         If E
-            Text(8F,6G,"     // 3 spaces
+            Text(-1,8F,6G,"   // 1 space
         remainder(F+8+(E-5)(E≥4),8->F
         remainder(G+16-(E=3)+(E=5),16->G
         A->dim(L₁
     End
     C+(B-5)(B≥4
     If Ans>7 or Ans<0
         abs(7K-C
     Ans->C
     D-(B=3)+(B=5
     If Ans>15 or Ans<0
         abs(15K-D
     Ans->D
     Y+1->Y
     augment({B},L₁→L₁
 End
 A
```