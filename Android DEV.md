* Package name should be unique
### Android Menifest 
Decides how the application will look.
### Drawable 
pictures wagiyra yehi save krenge.
### Layout
it Consist of frontend files and menifest contains backend files of app

frontend uses - xml

View - is a simple building block in UI
![[Pasted image 20241023131100.png]]
View Types 
![[Pasted image 20241023131137.png]]
# Layout
It hold all the views basically it is the parent of all the views
![[Pasted image 20241023133643.png]]
Types of layout

![[Pasted image 20241023133714.png]]

# View and View GRoup

![[Pasted image 20241023134146.png]]
Layout ke andr layout
 

ViewGroup bs layout ka ni hota bhot sare components ka viewGroup ho skta hai

# View vs ViewGroup
![[Pasted image 20241023143224.png]]
# Creating first Layout

![[Pasted image 20241023144122.png]]
# **1. dp (Density-independent Pixels):**

- Purpose: dp is a unit of measurement that is density-independent. It is recommended to specify dimensions in layouts to ensure consistent visual size across different screen densities.
- Calculation: 1 dp is equivalent to one physical pixel on a medium-density screen (160 dpi). The actual size of a dp is adjusted based on the screen’s density.

<TextView  
    android:layout_width="100dp"  
    android:layout_height="50dp"  
    android:text="Hello, World!"  
/>

In this above example, the width and height of the TextView are set to 100dp and 50dp, respectively.

# 2. sp (Scale-independent Pixels):

- Purpose: sp is similar to dp, but it is specifically used for defining text size. It takes into account the user’s preferred text size setting in the device’s system settings.
- Calculation: 1 sp is the same as 1 dp, but it also considers the user’s font size preference.

<TextView  
    android:layout_width="wrap_content"  
    android:layout_height="wrap_content"  
    android:text="Hello, World!"  
    android:textSize="16sp"  
/>

# 3. px (Pixels):

- Purpose: px is the most basic unit and represents a single pixel on the screen. It is not recommended to specify dimensions in layouts due to its lack of density independence.

<ImageView  
    android:layout_width="200px"  
    android:layout_height="100px"  
    android:src="@drawable/my_image"  
/>

In this example, the width and height of the ImageView are set to 200px and 100px, respectively.

# 4. dip (Density-independent Pixels):

- Purpose: dip is an older term for dp, and the two can be used interchangeably. Both represent density-independent pixels.

Here, the padding is set to 10dip, which means 10 density-independent pixels.

In summary, dp and sp are commonly used for dimensions in layouts and text sizes, respectively, due to their density independence. It is generally recommended to use dp for dimensions and sp for text sizes to ensure a consistent and user-friendly experience across different devices with varying screen densities and user preferences.

# Mastering the art of layout

Padding-left == paddingStart kyuki mmanlo language english hai to english left se start hoti hai aur padding start lagyege to left se margin milega mgr agr urdu hoti to wo right se start hoti to padding start me rigth me padding milta.

### Gravity 
Gravity is to define the position of  a view like top bottom center etc
![[Pasted image 20241023152012.png]]
Hamesha view ke andr wali cheez pe gravity apply hogi 

note - agr ek se jyada gravity ke options use krne hai to attributes me jake krenge
![[Pasted image 20241023152358.png]]
ya fir code me aise
![[Pasted image 20241023152411.png]]
## Edit Text
![[Pasted image 20241024004623.png]]
EditText means user can write something here minEms mtlb minimum itne character and maxEms vice versa
![[Pasted image 20241024004743.png]]
Name and password are EditText signIn is textView

## Image view Important attributes 

agr icon ki color change krne hai to hm tint attribute ka use krte hai
![[Pasted image 20241027125251.png]]
## Relative Layout 
relative layout relativity ke base pe kaam krta hai mtlb ki agr kisi textview ko kahi place krna hai to hm batayenge ki is imageview ke left right bottom top me yaha chle jao

In Android, the `RelativeLayout` is a ViewGroup that allows you to position its child views in relation to each other or to the parent container. It’s especially useful for creating complex layouts where elements need to be aligned with or positioned around other views.

*hmko yaha id dena compulsary hai taki hm bata sake is is id ke element ke uopr chale jao*

![[Pasted image 20241027130257.png]]
first view is id of the textview
Relative layout me jo upr rhega wohi UI me niche rhega

![[Pasted image 20241027130824.png]]
here we can see ki one is under two
![[Pasted image 20241027130856.png]]
but here in code it is above two and this is happening due to re;ative layout

![[Pasted image 20241027130948.png]]
just changed the layout form relative to linear and see the diffrence in the output
![[Pasted image 20241027131024.png]]
## Relative Layout important attributes
rigthof, left of,bellow of, kr ke use krte hai

# Linear Layouts

ye ek predefined direction deta hai jo ki horizontal ya verticle hoti hai
- yaha hmko sbse phle orientation define krni hoti hai
#### Weight in linear Layout
**Layout Weight** in Android is the priority level of space that a child view occupies in a linear layout.
**![[Pasted image 20241027142207.png]]
![[Pasted image 20241027142254.png]]
![[Pasted image 20241027142306.png]]
![[Pasted image 20241027142321.png]]
- For Button **“@+id/b”** and **“@+id/b2”**, the `layout_weight` is set to **1**. Therefore, both buttons occupy equal space in the layout.
- For **“@+id/b3”**, the `layout_weight` is set to **2**. _Button3_ will occupy the most space in the layout since it has a higher `layout_weight` as compared to _Button1_ and _Button2_.
![[Pasted image 20241027142351.png]]
### Weigthsum
Weightsum hm layout ke attributes me hi define kr denge ye ye batyega ki kitne element ko same length milegi


![[Pasted image 20241027142551.png]]
yaha hmne 5 define kra hai to 5 elements ko same length milegi
![[Pasted image 20241027142650.png]]
yaha dekho 6 button hai to 5 ke same size hai 6th ka different hai agr Weightsum ko 6 kr de to 6wo bararabr ho jayenge
![[Pasted image 20241027142819.png]]
![[Pasted image 20241027142828.png]]
*Note - height = wrapcontant === height=0dp*

## Constraint layout
This layout is faster than other layouts in loading time.
## Make your own button and view
![[Pasted image 20241031000148.png]]
- Go to drawable
- select drawable resource file 
- name it and change from selector to shape
code it in the new drawble file
ex for button -
![[Pasted image 20241031002923.png]]
to usi this just go to activity and for apply this as background
![[Pasted image 20241031003010.png]]
like this
![[Pasted image 20241031003024.png]]
if the normal button doesnt work just change the attribute to this
![[Pasted image 20241031003055.png]]
It will work as same as button
- angle bhi de skte hai magr wo 90 se divide hona chahiye.
- agr hm custom component wale fine me changing krenge t0 direct activity me bhi changing ho jayegi

## TO make custom cardView
![[Pasted image 20241031005423.png]]
this call , chat , comment, duo are cards

Cardview ek view group hai jo ki views ko contains krta hai aur ye predefined hota hai studio me

##### Important elements of card view
- cardElevation is an attribute jo define krta hai ki card apne backgroud se kitna utha hoga 
- ![[Pasted image 20241031010932.png]]
- ![[Pasted image 20241031010942.png]]
-- Card View is created on heirarcy constraint layout>cardview>constraint layout> other elemets

![[Pasted image 20241031011701.png]]
aise

# Kotlin
	JAVA and kotlin are interoperable kotlin bhi JVM ka use kr ke interprate hoti hai

![[Pasted image 20241031014202.png]]
Dekho kotlin java ke andr hai
## Variables in Kotlin
val and var
![[Pasted image 20241031014440.png]]
to use a value we have to use template littrels like in JS 

var can be reassigned but val can not be reassigned
![[Pasted image 20241031015819.png]]
yaha tk thik hai mtlb aise data type define na bhi kre to chalega  jaise ki JS me hota hai
![[Pasted image 20241031015920.png]]
lekin aise aise kiye to ni hoga jbki JS me possible hai 

![[Pasted image 20241031020008.png]]
define kr diye to shi chalega
![[Pasted image 20241031020141.png]]

Note - Ek lateinit kr ke bhi type hota hai jaise ki var val ko turant initialize krna pdta hai agr hm chah rhe ki baad me kre to lateinit ka use kr skte hai 
![[Pasted image 20241104000456.png]]

# Data types
![[Pasted image 20241031020346.png]]
## Integer data type 
dekho hm app bna rhe hai to app ka size bhi bhut matter krta hai to uske liye hme shi data types use krne hinge
![[Pasted image 20241031155936.png]]
By default agr hmne data type ni batya kisi number ka to wo by default int leta hai
## Floating data type
![[Pasted image 20241031160329.png]]
by Default Double![[Pasted image 20241031160501.png]]
dekho float le hi ni rha wo isko explicitly batyenge ki bhai tum float ho 
![[Pasted image 20241031160541.png]]
F ya f lga ke 

# Operators
![[Pasted image 20241031161221.png]]
![[Pasted image 20241031161240.png]]
![[Pasted image 20241031161252.png]]

# Conditional Statement
![[Pasted image 20241031161506.png]]
![[Pasted image 20241031161538.png]]

## When (same as switch case)
Important arrow operator use krna hoga
![[Pasted image 20241031161644.png]]
ab yaha pe dekho sbke liye ek ek condition to use ni kr skte to iske liye hm range function ka use krte hi jaise is age<60 etc

### Range operator

range..operator
![[Pasted image 20241031162434.png]]
rangeTo()
![[Pasted image 20241031162503.png]]
downTo()
![[Pasted image 20241031162536.png]]
ulta hota hai rang ka descending order me hota hai

## Why no null pointer error in kotlin
Kotlin null ko support hi ni krta hme kisi bhi variable to initialize krna bhut jaruri hai
ex
![[Pasted image 20241031163109.png]]
aur hm null se init bhi ni kr skte
![[Pasted image 20241031163144.png]]
agr hmko null se init hi krna hai to dataType declaration ke baad "?"
ka use krenge
![[Pasted image 20241031163234.png]]
Known as safe call

Note - ? known as elvis operator in kotlin
![[Pasted image 20241031163434.png]]
AGR  is se deal krna hai to wahi elvis operator ka use krenge
![[Pasted image 20241031163506.png]]
## Functions in kotlin
with parameter
![[Pasted image 20241031231719.png]]
Function with return values
![[Pasted image 20241031231801.png]]
`fun myFun(x:Int):Int{ this last is return type
}`

# OOPS
![[Pasted image 20241031232758.png]]
![[Pasted image 20241031232813.png]]
# Encapsulation
![[Pasted image 20241031233226.png]]
Access modefiers in kotlin
![[Pasted image 20241031234246.png]]
- encapsulation is achieved through access modifiers such as `private`, `protected`, `internal` and public.

# Constructor in kotlin
1. Default constructor (primary constructor)- ye khud se call ho jata hai isko call ni krte jaise ye ![[Pasted image 20241101113535.png]]yaaha carr ko car() aise ni likkha hai 
2. Paramatrize constructor (secondary constructor )
agr parameter pass krna ho to 
![[Pasted image 20241101113630.png]]
yaha dekho parameter pass kiya hai to round braket ka use kr rhe hai 
-- Ye krna ek achi practice ni hai iske liye hm construstor ka use krte hei

```kotlin
class cal{
    var a :Int? =null
    var b:Int?=null
   constructor(){}; // Primary constructor ye tb call hoga jb hmko nomral object banan hoga jaise var a1=cal();
    constructor(y : Int =5 , z:Int=8){
        this.a = y
        this.b=z
        
    }//Secondary constructor agar value deke pass krenge t0 ye wala call hoga 
    fun add(){
        println(a!!+b!!) // ye to null value handle krne ke liye hai
    }
}
fun main(){
    var op = cal()
    op.add()
    
}
```
We can make many constructors like this
#### Important
![[Pasted image 20241101122440.png]]
agr upr hi CH1() aise define kr diya to tum niche constructor ko define ni kr skte
# Inheritance 
Are ye wahi hai jo ki parent class ki properties le leta hai
Syntax
![[Pasted image 20241101134310.png]]
java me hm simply
![[Pasted image 20241101134359.png]]
ye krte the but yaaha hmko
- Extends ki jgh : lgana hoga 
- aur parent class ho open krna hoga joki java me ni krna hota tha

```kotlin
open class Father{
    var car = " BMW"
    
    
}
class Son : Father(){
    
    fun carName(){
        print(car)
    }
    
}
fun main(){
    var obj = Son();
    obj.carName()
    // yaha dekho father ki car son use kr pa rha hai 
}
```
Types of Inheritance
- Single level Inheritance
![[Pasted image 20241101135753.png]]

- MultiLevel Inhertance
![[Pasted image 20241101140150.png]]

- Hierarchy Inheritance - ek father ke do bachee
![[Pasted image 20241101140531.png]]
dono papa ki hi gadi use kr rhe
- Hybrid inheritance - ye dono ka mixup hota hai heirarchy aur multiple dono
- multiple inheritance(does not support by kotlin and java)

# Poly-Morphism 
The word polymorphism means having many forms. In simple words, we can define polymorphism as the ability of a message to be displayed in more than one form.

1. Compile-time Polymorphism
Function overLoading parameters change kr ke 
![[Pasted image 20241101155415.png]]

2. Runtime Polymorphism
![[Pasted image 20241101155629.png]]
yaha override function ka use krte hai
important - jis bhi function ko over ride krna hai usko open krna hoga

# Abstraction 
- Agar class abstract hai to minimum uska ek function abstract hona chahiye
- agr koi function abstract hai to class bhi abstract honi chahiye
- ![[Pasted image 20241101160144.png]]
- Abstract class ka object ni bana skte
- jb object bana ni skte to uske function ya memebers ko use krne ke liye child class unko inherit krwate hai 
![[Pasted image 20241101160757.png]]
- agr kisi bhi function ki body hai to usko abstract ni kr skte 
```kotlin
abstract function car(){} xxxxxxxx Aisa ni kr skte
abstract function car() ✅✅✅✅✅✅ aise krna hogaq without body
```
- agar function abstract hai to wo age jake inherit hoga ye default nature hai to oepn lagao na lagao jyada anatar ni hai

# Data classes(Java ❌ Kotlin ✅)

![[Pasted image 20241101161430.png]]
agr hm kisi bhi class ko data class define kr dete hia to kotlin already smjh jata hai ki ye bs data ke kaam ayegi aur wo kuch function apne taraf se hi provide kr deti hia 
- equals()
- hashCode()
- toString()
- copy()
ye function java me khud se define krne pdte the 
important 
- - The primary constructor needs to have at least one parameter.
- All primary constructor parameters need to be marked as _val_ or _var_.
- Data classes cannot be abstract, open, sealed or inner.
- Data classes may only implement interfaces.
# Sealed and Enum class in Kotlin
In programming, sometimes there arises a need for a type to have only certain values. To accomplish this, the concept of enumeration was introduced. Enumeration is a named list of constants. In Kotlin, like many other programming languages, an ****enum**** has its own specialized type, indicating that something has a number of possible values. Unlike [Java enums](https://www.geeksforgeeks.org/enum-in-java/), Kotlin enums are ****classes****.
![[Pasted image 20241101162456.png]]
![[Pasted image 20241101162515.png]]

# Android Activity Life Cycle 

![[Pasted image 20241101164112.png]]
there are 7 methods in  Activity life cycle

# Intent 
agr ek activity se dure  activity me jana hai to intent ka use krte hai 
![[Pasted image 20241101232929.png]]
Types of intent 
1. Implicit Intent - jo dusre app pe redirect kre
2. Explicit intent - same app me activity change

![[Pasted image 20241101235142.png]]
ek activity se dure me jane ka code kisi button ko click kr ke
# ImplicitIntent (dusre app me jana)
![[Pasted image 20241102103803.png]]
Backend
![[Pasted image 20241102104155.png]]
# WebView
![[Pasted image 20241102112253.png]]
Web view use krne ke liye ek important kaam hota hai user ko internet ki permision deni hoti hai menifest se
![[Pasted image 20241102112337.png]]
YE WALI
activity file
![[Pasted image 20241102112406.png]]
# Passing data form one screen to other
Dekho kuch bhi idhar se udhar pass krne ke liye hmko key ki jruruat lgti hai jo ki global ki mtlb har activity me access ho jaye to iske liye hmko global ki bnanani pdegi

java me to static keyword use kr ke bna dete the global mgr kotlin me static ni hota 

![[Pasted image 20241103114418.png]]
Companion Object in Kotlin 
- note -Static ki jgh Companion object ka use krte hai kotlin me

# To pass data from ONE Activity
![[Pasted image 20241103134652.png]]

mainly data pass krne ke lie hm putExtra ka use krte hai 
![[Pasted image 20241103134749.png]]
isko ek key dete hai jo ki unique hoti hai aur jo data pass krna hai wo dete hai is case me hmne order list diya hai jo editText se extract kiya hai 
jaise react e.value kr ke get krte the na yaha bhi kuch aise hi krte hai
![[Pasted image 20241103134915.png]]
yaha ek variable bnaya hai et1(editText ki id).text kr ke extract lr liya hai aur put extra me pass kr diya hai

# TO get the passed data in other activity
![[Pasted image 20241103135331.png]]
waha ek text view bnaya hai aur ek variable leke 
"intent.getStringExtra(Jis bhi activity se aa rha ho uska naam.key)"
aise leke access kr de
![[Pasted image 20241103135509.png]]
Aise odersOfCoustmer me value li aur fir 
![[Pasted image 20241103135558.png]]
jo text view tha usme daal diya .text property hoti hai change kr ne ki

That's It

# Setting data in fire base
Step 1. Fire base pe account bnaye 
Step 2. Android studio ko link kre Fire base se
![[Pasted image 20241104125356.png]]
yaha se link krenge connect kr ke 
step 3 . ![[Pasted image 20241104125425.png]]
fir fire base me jake real time database me jake rules ko true kr denge 
Step 4 . User ka sara data le lenge TextInput se
![[Pasted image 20241104125536.png]]
jaise yaha liya hai
Step 5. Ek class bnaynge jisme hm sara data store krenge 
![[Pasted image 20241104125619.png]]
Bs class bna ke chod denge aur jo value enter karani hai usko as a parameter pass kr denge
Step 6. Ek lateinit variable define krenge jiska data type hoga DatabaseRefrence
![[Pasted image 20241104125816.png]]
Step 7.![[Pasted image 20241104125838.png]]
yehi code hai bs itna sa fire base me data send krne ke liye 

Explanation of the code 
```
This code snippet is part of an Android application using Firebase Realtime Database to store user information. Here's a step-by-step explanation:

1. **FirebaseDatabase.getInstance().getReference("Users")**:
    
    - This retrieves a reference to the Firebase Realtime Database and points to the "Users" node. This is where user data will be stored.
2. **database.child(name)**:
    
    - This creates a child node under "Users" with the key `name`. The `name` is typically a unique identifier for the user, like a username or user ID.
3. **.setValue(user)**:
    
    - This sets the value of the newly created child node to `user`. `user` is an object containing the user details (like name, email, etc.).
4. **addOnSuccessListener { ... }**:
    
    - This is a callback that runs when the data is successfully written to the database.
    - Inside the callback:
        - A toast message is shown saying "User Registered".
5. **addOnFailureListener { ... }**:
    
    - This is a callback that runs if there is an error while writing the data to the database.
    - Inside the callback:
        - A toast message is shown saying "Failed".

### In short:

- **On success**: The user is registered, and a success message is displayed.
- **On failure**: An error message is displayed.
```

Complete code 
```Kotlin
package com.example.signupusingfirebase  
  
import User  
import android.os.Bundle  
import android.widget.Toast  
import androidx.activity.enableEdgeToEdge  
import androidx.appcompat.app.AppCompatActivity  
import androidx.appcompat.widget.AppCompatButton  
import androidx.appcompat.widget.AppCompatEditText  
import androidx.core.view.ViewCompat  
import androidx.core.view.WindowInsetsCompat  
import com.google.firebase.database.DatabaseReference  
import com.google.firebase.database.FirebaseDatabase  
  
class MainActivity : AppCompatActivity() {  
  
    lateinit var database : DatabaseReference  
    override fun onCreate(savedInstanceState: Bundle?) {  
        super.onCreate(savedInstanceState)  
        enableEdgeToEdge()  
        setContentView(R.layout.activity_main)  
  
        val btnSignUp = findViewById<AppCompatButton>(R.id.btnSignUp)  
        val etName=findViewById<AppCompatEditText>(R.id.etName)  
        val etEmail=findViewById<AppCompatEditText>(R.id.etMail)  
        val etUserName=findViewById<AppCompatEditText>(R.id.etUserName)  
        val etPassword=findViewById<AppCompatEditText>(R.id.etPassword)  
        btnSignUp.setOnClickListener{  
            val name = etName.text.toString()  
            val email = etEmail.text.toString()  
            val userName = etUserName.text.toString()  
            val password = etPassword.text.toString()  
            val user = User(name, email, userName, password)  
            etName.text?.clear()  
            etEmail.text?.clear()  
            etPassword.text?.clear()  
            etUserName.text?.clear()  
            database= FirebaseDatabase.getInstance().getReference("Users")  
            database.child(name).setValue(user).addOnSuccessListener {  
                Toast.makeText(this,"User Registered", Toast.LENGTH_SHORT).show()  
            }.addOnFailureListener {  
                Toast.makeText(this, "Failed", Toast.LENGTH_SHORT).show()  
            }  
  
        }  
    }  
}
```
![[Pasted image 20241104130254.png]] Image Format

Data in FireBase
![[Pasted image 20241104130736.png]]


# Reading Data And Using Data From FireBase Data base
### Read Data
![[Pasted image 20241104205731.png]]
same jaise waha set kra yha get krenge
![[Pasted image 20241104205806.png]]
![[Pasted image 20241104205819.png]]
data ko read kiya hai match kiya
# Use data ke liye 
![[Pasted image 20241104210002.png]]
Yaha se data base se value nikal li
fir jha use krna tha waha bhej diya
![[Pasted image 20241104210036.png]]
# View Binding
Find view by id baar baar likhna pdta hai isi ko overcome krne ke liye view binding ka use krte hai
![[Pasted image 20241104210718.png]]

### Steps to use
Step 1 - Gradle build me add krna
![[Pasted image 20241104232828.png]]
Step 2 - 
![[Pasted image 20241104232800.png]]
# Dialogue Box
1-Alert Dialogue box
2-Date Picker Dialogue box 
3-Time Picker Dialogue box
4-Progress Dialogue box

## Alert dialogue box 

![[Pasted image 20241105112555.png]]
![[Pasted image 20241105112911.png]]

# Alert box Option type
![[Pasted image 20241105113157.png]]

 ![[Pasted image 20241105113251.png]]

# Alert Box Type 3 - MultiOption
![[Pasted image 20241105113403.png]]
![[Pasted image 20241105113425.png]]

# Coustomized Alert boxes
![[Pasted image 20241105162112.png]]
![[Pasted image 20241105190214.png]]
Step 1 custom xml crete kiya jaha alert box khud se bnaya
baki steps image me hai
![[Pasted image 20241105192338.png]]














# Projects 
1. Splash screen
Backend
![[Pasted image 20241101175153.png]]

![[Pasted image 20241101175326.png]]

2. Splash screen when loading
it is a dynamic splash screen mtlb ki agr background me kuch load ho rha to splash screen chl jaye
```kotlin

activity
<ImageView  
    android:id="@+id/imageView2"  
    android:layout_width="200dp"  
    android:layout_height="200dp"  
    android:layout_marginStart="16dp"  
    android:layout_marginTop="212dp"  
    android:layout_marginBottom="211dp"  
    app:layout_constraintBottom_toBottomOf="parent"  
    app:layout_constraintEnd_toEndOf="parent"  
    app:layout_constraintHorizontal_bias="0.456"  
    app:layout_constraintStart_toStartOf="parent"  
    app:layout_constraintTop_toTopOf="parent"  
    app:layout_constraintVertical_bias="0.203"  
    app:srcCompat="@drawable/img" />  
  
<TextView  
    android:id="@+id/textView2"  
    android:layout_width="wrap_content"  
    android:layout_height="wrap_content"  
    android:layout_marginTop="200dp"  
    android:layout_marginBottom="34dp"  
    android:padding="10dp"  
    android:text="Ye screen tb chlegi jb kuch load hoga"  
    android:textSize="25sp"  
    android:textStyle="bold"  
    app:layout_constraintBottom_toBottomOf="parent"  
    app:layout_constraintEnd_toEndOf="parent"  
    app:layout_constraintStart_toStartOf="parent"  
    app:layout_constraintTop_toBottomOf="@+id/imageView2" />
```

```kotlin
bACKEND
  
import android.content.Intent  
import android.os.AsyncTask  
import android.os.Bundle  
import androidx.activity.enableEdgeToEdge  
import androidx.appcompat.app.AppCompatActivity  
import androidx.core.view.ViewCompat  
import androidx.core.view.WindowInsetsCompat  
  
class SplashScreenLoading : AppCompatActivity() {  
    override fun onCreate(savedInstanceState: Bundle?) {  
        super.onCreate(savedInstanceState)  
        enableEdgeToEdge()  
        setContentView(R.layout.activity_splash_screen_loading)  
        tillLoading();  
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main)) { v, insets ->  
            val systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars())  
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom)  
            insets  
  
  
        }  
    }  
    private fun tillLoading() {  
        loadingOperation().execute();  
    }  
    private open inner class loadingOperation : AsyncTask<String?,Void?,String?>(){  
        override fun doInBackground(vararg params: String?): String? {  
            for(i in 0..6){  
                try{  
                    Thread.sleep(1000)  
                }  
                catch(e:Exception){  
                    Thread.interrupted()  
  
                }  
            }  
            return "Result"  
        }  
  
        override fun onPostExecute(result: String?) {  
            super.onPostExecute(result)  
            val intent = Intent(this@SplashScreenLoading,MainActivity::class.java);  
            startActivity(intent)  
        }  
  
    }  
  
}
```
![[Pasted image 20241101204704.png]]
 