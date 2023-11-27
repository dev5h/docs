# Bottom Navbar

### What?

Wel it's all known

### Why?

So that users can navigate properly

### How?

**Steps:**

1. Add the following implementation in the `build.gradble` module file `implementation("com.google.android.material:material:1.10.0")`

2. RIght click on the res and `res -> New -> Android Resource Directory` select resource type menu and create one

3. Right click on that new dirctory and create a new resource file

4. Than add some icons in the drawable folder and add menu items as follow
   
   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <menu xmlns:android="http://schemas.android.com/apk/res/android">
       <item
           android:id="@+id/home"
           android:title="Home"
           android:icon="@drawable/ic_home"/>
       <item
           android:id="@+id/add"
           android:title="Add"
           android:icon="@drawable/ic_add"/>
       <item
           android:id="@+id/settings"
           android:title="Settings"
           android:icon="@drawable/ic_gear"/>
   </menu>
   ```

5. Than add a material bottom nav view in the mainactivity layout file 
   
   ```xml
    <com.google.android.material.bottomnavigation.BottomNavigationView
          android:id="@+id/bottomNavigationView"
          android:layout_width="match_parent"
          android:layout_height="90dp"
          app:layout_constraintBottom_toBottomOf="parent"
          app:layout_constraintEnd_toEndOf="parent"
          app:menu="@menu/bottom_nav" />
   ```

6. Constrain that layout and you're done! Output will look like this ![](/home/shazin/Code/projects/docs/Android/assets/ss2.png)
