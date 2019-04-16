# ConstraintLayout 
---
What is the ConstraintLayout?<br/>
ConstraintLayout allows you to create large and complex layouts with a flat view hierarchy (no nested view groups).
The aim of the ConstraintLayout is to help reduce the number of nested views, which will improve the performance of our layout files
The layout class also makes it easier for us to define layouts than when using a RelativeLayout as we can now anchor any side of a view with any side of another, rather than having to place a whole view to any side of another.

Note: The ConstraintLayout is also compatible right down to API level 9

**ConstraintLayout features several more attributes**
* layout_constraintTop_toTopOf
* layout_constraintTop_toBottomOf
* layout_constraintBottom_toTopOf
* layout_constraintBottom_toBottomOf
* layout_constraintLeft_toTopOf
* layout_constraintLeft_toBottomOf
* layout_constraintLeft_toLeftOf
* layout_constraintLeft_toRightOf
* layout_constraintRight_toTopOf
* layout_constraintRight_toBottomOf
* layout_constraintRight_toLeftOf
* layout_constraintRight_toRightOf

**Baseline Constraint Handle**<br/>
 app:layout_constraintBaseline_toBaselineOf

**Vertical Bias**<br/>

It's allows us to position a view along the vertical axis using a bias value
`app:layout_constraintVertical_bias="0.5"` <br/>

**Horizontal Bias**<br/>

It's allows us to position a view along the horizontal axis using a bias value
`app:layout_constraintHorizontal_bias="0.5"` <br/>

**ConstraintDimensionRatio**<br/>
We need to set atleast one constrained dimension to be 0dp
````
 <ImageView
        android:layout_width="match_parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintDimensionRatio="1:0.50"
        android:background="@drawable/splash"
        android:layout_height="0dp" />
````
**Note**: `app:layout_constraintDimensionRatio="W:H"` <br/>
In the above example image height ration is half of the width ratio irrespect of screen dimension,So here height is automatically changed based on width ratio and given height ratio value.For the above scnario need to set the top constraint <br/>
````
 <ImageView
        android:layout_width="0dp"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintDimensionRatio="1:1"
        android:background="@drawable/splash"
        android:layout_height="0dp" />
````
Above case set constraint of view and width,height is `o dp` and then dimension ratio is 1:1 here width of image view ration is equal to the height of imageview ratio. <br/>

````
  <Button
        android:layout_width="0dp"
        android:layout_height="0dp"
        app:layout_constraintTop_toBottomOf="@+id/splashImage"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintDimensionRatio="h,1:0.20"
        android:text="@string/mailbox"
        android:layout_marginRight="@dimen/_20sdp"
        android:layout_marginLeft="@dimen/_20sdp"
      />
      
  ````
 app:layout_constraintDimensionRatio="h,1:0.20"


