# ANDINDA
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="campusmap.csu.org.myapplication.MainActivity"
    android:id="@+id/integ">

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:inputType="textPersonName"
        android:ems="10"
        android:id="@+id/user"
        android:layout_marginTop="54dp"
        android:hint="Enter userName"
        android:layout_alignParentTop="true"
        android:layout_alignLeft="@+id/pass"
        android:layout_alignStart="@+id/pass" />

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:inputType="textPassword"
        android:ems="10"
        android:id="@+id/pass"
        android:layout_below="@+id/user"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="65dp"
        android:hint="Enter Password"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="login"
        android:id="@+id/login"
        android:layout_marginTop="46dp"
        android:onClick="login"
        android:layout_below="@+id/error"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textAppearance="?android:attr/textAppearanceLarge"
        android:id="@+id/error"
        android:layout_below="@+id/pass"
        android:layout_alignRight="@+id/login"
        android:layout_alignEnd="@+id/login"
        android:textAlignment="center"
        android:textColor="#f21313" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="create account"
        android:id="@+id/account"
     android:onClick="account"
        android:layout_alignTop="@+id/login"
        android:layout_alignParentRight="true"
        android:layout_alignParentEnd="true" />
</RelativeLayout>

package campusmap.csu.org.myapplication;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.text.Layout;
import android.view.View;
import android.view.ViewParent;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    TextView user,pass,error;

    Button click;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
         user=(TextView) findViewById(R.id.user);
        pass=(TextView) findViewById(R.id.pass);
        error=(TextView) findViewById(R.id.error);
        click=(Button)findViewById(R.id.login);


        click.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MainActivity.this, Main2Activity.class);
                startActivity(intent);
            }
        });


        }

    public void exit() {

    }

    public void account(View view) {
        Intent intent = new Intent(MainActivity.this, Main3Activity.class);
        startActivity(intent);
    }
}


<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="campusmap.csu.org.myapplication.Main2Activity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textAppearance="?android:attr/textAppearanceLarge"
        android:text="WELCOME"
        android:id="@+id/textView2"
        android:layout_centerVertical="true"
        android:layout_centerHorizontal="true" />
</RelativeLayout>

package campusmap.csu.org.myapplication;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;

public class Main2Activity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
    }

}


<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="campusmap.csu.org.myapplication.Main3Activity">

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/editText"
        android:layout_alignParentTop="true"
        android:layout_alignParentRight="true"
        android:layout_alignParentEnd="true"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true"
        android:text="REGISTER HERE"
        android:textAlignment="center" />

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/editText2"
        android:layout_below="@+id/editText"
        android:layout_marginTop="43dp"
        android:layout_alignRight="@+id/editText"
        android:layout_alignEnd="@+id/editText"
        android:hint="enter first name"
        android:textAlignment="center"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/editText3"
        android:layout_below="@+id/editText2"
        android:layout_alignLeft="@+id/editText2"
        android:layout_alignStart="@+id/editText2"
        android:layout_marginTop="58dp"
        android:layout_alignRight="@+id/editText2"
        android:layout_alignEnd="@+id/editText2"
        android:hint="enter last name"
        android:textAlignment="center" />

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/editText4"
        android:layout_marginTop="58dp"
        android:layout_below="@+id/editText3"
        android:layout_alignLeft="@+id/editText3"
        android:layout_alignStart="@+id/editText3"
        android:layout_alignRight="@+id/editText3"
        android:layout_alignEnd="@+id/editText3"
        android:hint="enter username"
        android:textAlignment="center" />

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/editText5"
        android:layout_marginTop="49dp"
        android:layout_below="@+id/editText4"
        android:layout_alignLeft="@+id/editText4"
        android:layout_alignStart="@+id/editText4"
        android:layout_alignRight="@+id/editText4"
        android:layout_alignEnd="@+id/editText4"
        android:inputType="textPassword"
        android:hint="enter password"
        android:textAlignment="center" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="submit"
        android:id="@+id/button"
        android:layout_alignParentBottom="true"
        android:layout_centerHorizontal="true"
        android:onClick="lo"/>
</RelativeLayout>

package campusmap.csu.org.myapplication;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;

public class Main3Activity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main3);
    }

    public void lo(View view) {
        Intent intent = new Intent(Main3Activity.this, Main2Activity.class);
        startActivity(intent);
    }
}
