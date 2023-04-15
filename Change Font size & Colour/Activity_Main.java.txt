package com.example.ex4;importandroid.graphics.Color;
//import android.support.v7.app.AppCompatActivity;import androidx.appcompat.app.AppCompatActivity;importandroid.os.Bundle;
import android.view.View;import android.widget.Button;importandroid.widget.TextView;
publicclassMainActivityextendsAppCompatActivity
{
intch=1;float font=30;@Override
protectedvoidonCreate(BundlesavedInstanceState)
{
super.onCreate(savedInstanceState);setContentView(R.layout.activity_main);
final TextView t= (TextView) findViewById(R.id.textView);Button b1= (Button) findViewById(R.id.button1);b1.setOnClickListener(newView.OnClickListener(){
@Override
public void onClick(View v) {t.setTextSize(font);
font = font + 5;if (font == 50)font =30;
}
});
Button b2= (Button) findViewById(R.id.button2);b2.setOnClickListener(newView.OnClickListener(){
@Override
public void onClick(View v) {switch(ch) {
case1:
t.setTextColor(Color.RED);break;
case2:
t.setTextColor(Color.GREEN);break;
case3:
t.setTextColor(Color.BLUE);break;
case4:
t.setTextColor(Color.CYAN);break;
case5:
t.setTextColor(Color.YELLOW);break;
case6:
t.setTextColor(Color.MAGENTA);break;
}
}
});
}
}
ch++;
if (ch == 7)ch=1;
 

