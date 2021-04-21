
# Rapport

## Changing the layout
To change the layout I edited the already present layout in
```activity_main.xml```. I changed the declared layout from the
constraints layout to a linear layout by changing the line
```xml
<androidx.coordinatorlayout.widget.CoordinatorLayout xmlns:android="http://schemas.android.com/apk/res/android" 
```
to
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
```
We also need to define the orientation of the layout, in this assignment
i choose to use vertical orientation, meaning that new elements will
fill the layout top to bottom. This will result an
```activity_main.xml``` that looks like this:
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">
</LinearLayout>
```
## Adding widgets
### Rating bar
The first widget i added was a rating bar, which I placed at the top. I
then wanted to center this so the rating bar gets placed at the top but
not anchored to the left corner. To do this i used the margin attribute
to add empty space between the corner and the ratings bar. I then
decided to make the rating bar transparent which i used the alpha
attribute to achieve. The final widget declaration looks like this:
```xml
    <RatingBar
        android:id="@+id/ratingBar"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="100dp"
        android:layout_marginLeft="100dp"
        android:layout_weight="0"
        android:alpha="0.5"
        android:clickable="true"
        android:focusable="true" />
```
### Toggle button
The next widget i added was a toggle button. Since this is the next
element present in the linear layout this will be placed below the
rating bar. I also added a margin to the right to prevent the button
from filling the entire screen horizontally. Since the toggle button
element requires a string I also added a string resource to
```strings.xml``` to conform to best practices. The final widget
declaration looks like this:
```xml
    <ToggleButton
        android:id="@+id/toggleButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginEnd="200dp"
        android:layout_marginRight="200dp"
        android:layout_weight="0"
        android:text="@string/togglebutton" />
```
```xml
<resources>
    <string name="app_name">Widgets</string>
    <string name="togglebutton">Button</string>
</resources>
```
### Search view
The final widget i added as a search view, which simply consists of a
text field and some buttons, the standard search box used by android.
This was added at the end of the linear layout which placed it right
below the button. I want to add som empty space between the button and
the search view and used margins to do so. This was the only attribute i
used to customize the widget, besides the standard layout settings. The
final declaration looks like this:
```xml
    <SearchView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_marginTop="200dp"
        android:layout_weight="0">
    </SearchView>
```
