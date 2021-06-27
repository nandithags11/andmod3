# andmod3
Android module 3

Android common controls 
> Button
>
> Text field
>
> Checkbox
>
> Radio button
>
> Toggle button
>
> Spinner
>
> Picker

Text Controls

---

<EditText
android:id="@+id/phone"
android:layout_height="match_parent"
android:layout_width="match_parent"
androi:hint="@string/phone_hint"
android:inputType="phone"/>

password => android:inputType="textPassword"
auto spell => android:inputType="textAutoCorrect"
multi line => android:inputType="textMultiLine"
Number
datetime


Button

<Button
android:layout_width=”wrap_content”
android:layout_height=”wrap_content”
android:onClick="sendMessage"
android:text=”@string/button_text” />


=== << HEAD

The send message is handle by
Public void send Message(View view){
// Do something
}

===

Button button = (Button) findViewByID(R.id.button_send)
button.setOnClickListner(newView.onClickListner()
{
Public voif onClick(View v){
//  Do something
}})

======== << ELSE


If the button uses an image instead

<ImageButton
android:layout_width=”wrap_content”
android:layout_height=”wrap_content”
android:src=”@drawable/button_icon” /> //src drawable-> button icon

CheckBox

Just a check box
User should create diffrent event listener for every items

<CheckBox
android:id=”@+id/checkbox_cheese”
android:layout_width=”wrap_content”
android:layout_height=”wrap_content”
android:text=”@string/cheese”
android:onClick=”onCheckboxClicked” />

Radio button 
Only one can be selelcted
Grouping multple elemens ensure only one can be selected



<?xml version="1.0" encoding="utf-8"?> //XML version
<RadioGroup
xmlns:android="http://schemas.android.com/apk/res/android" //Link
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:orientation="vertical">
 
 <RadioButton android:id="@+id/radio_pirates"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="@string/pirates"
 android:onClick="onRadioButtonClicked"/>
 
 <RadioButton android:id="@+id/radio_navy"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="@string/navy"
 android:onClick="onRadioButtonClicked"/>
</RadioGroup>

##### Image View

<LinearLayout
 xmlns:android="http://schemas.android.com/apk/res/android"
 android:layout_width="match_parent"
 android:layout_height="match_parent">
 
<ImageView
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:src="@drawable/my_image"
 android:contentDescription="@string/my_image_description" />
 </LinearLayout>

Date and Time Controls
Allows user to pick date and time
Hour minute AM/PM date as in month day and year
TimePIckerDialog anf datePickerDialog

Map

Provided by Google API and Mapfragment class

setMapType()
 
- Normal Map
- Hybrid Map
- Satelite Map
- Terrain Map

Inbuilt UI / UX Controls 
Compass Map Toolbar, My location, Level Picker, Map gestures

Adapters
Adapters are the bridge between UI component and data source that helps fill data in UI component. It holds data and sends data to views

- ArrayAdapter
- CursorAdapter
- SimpleAdapter
- SimpleCursorAdapter

#### List View
Displays vertically scrollable collection of views, each view is positioned immediately below the previous view in the list.


<ListView
    android:id="@+id/list_view"
    android:layout_width="match_parent"
    android:layout_height="match_parent"/>


##### GridView

2D Scrolling Grid


<?xml version="1.0" encoding=utf-8""?>
<GridView 
xmlns:android="https://schema.android.com/aps/res/android"
    android:id="@+id/gridview"
    android:layout_height="fill_parent"
    android:layout_width="fill_parent"
    android:columWidth="90px"
    android:columHeight="90px"
    android:horizondalSpacing="10px"
    android:verticalSpacing="10px"
    android:streachMode="columnWidth"
    android:gravity="center
/>


#### Spinner Control

Spinners

To select a value form a set, Dropdown menu


<Spinner
    android:id="@+id/planets_spinner"
    android:layout_width="fill_parent"
    android:layout_height="wrap_content"/>

AdapterView.OntemSelectedListner interface and corresponding onItemSelected()



#### Gallery control
Select images

<Gallery
    android:id="@+id/gallery1"
    android:layout_width="fill_parent"
    android:layout_height="wrap_content"/>

    - Center locked horizondal sccroling list


## Android styles
- Collection of attributes that specify the appearence for a view.
- font color, size, background color etc
- in res/values/styles.xml

Declaring Style

<?xml version="1.0" encoding="utf-8"?>
<resources>
<style name="GreenText">
    <item name="android:textColor">#000FFF</item>
    <item nmae="android:textSize">12pt</item>
    <item name="android:typeface">monospace</item>
</style>
</resources>

Using Styles

<TextView
    android:id="@+id/text_id"
    android:layout_width="fill_parent"
    android:layout_height="wrap_content"
    style="@style/GreenText"
    android:text="Hello"/>
     

    #### App theme

    Theme is something that applies for the  whole application, not in just a view, It can even effect non-view elements, such as the status bar and window background.

    To set a theme for all application. Include
    
    <application android:theme="@style/CustomTheme">
    ```
    in AndroidManifest.xml

    - To set theme for just a activity <activity> tag needs to be edited
