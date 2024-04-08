
# Rapport

The name of the app was changed to "Lore Archive" to make it more fitting
considering the contents of the internal webpage, even though it is far
from an actual archive. 

The first actual change that was made in the project
was to enable internet access, because the external webpage will not be
able to function without it.

I then replaced the existing "TextView" in activity_main.xml 
with a "WebView" and created a new object instance. Used "loadUrl"
to load an external webpage, in this case www.his.se, but to get access
to all its features, the app requires javascript so it became the logical
next step to proceed with the assignment.

One of the final steps was to create a html-file so the internal webpage
could load it. I filled the content of the html-file with something that
fit the name of the app, using very simple html code. Then I properly
listed the directory in the method for showing the internal webpage. At
this stage, the app is very simple but it works as intended.


In this code snippet, the last few lines of code shows how I did to enable
JavaScript in the app. It also insures that the WebView is working as
intended.
```
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toolbar toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);

        myWebView = findViewById(R.id.my_webview);
        WebSettings webSettings = myWebView.getSettings();
        webSettings.setJavaScriptEnabled(true);
        myWebView.setWebViewClient(new WebViewClient());

    }
```

![img.png](img.png) ![img_1.png](img_1.png)

