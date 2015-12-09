# easy-volley
This repository have a Java class to simplify the use of  Volley library. Only for POST and GET requests.

NEEDS TO HAVE THE VOLLEY LIBRARY IN THE ANDROID PROJECT.

## Usage
```java
Context context = getContext();
String url = "http://www.google.com.br";


/* GET Request */
HttpRequest.getInstance(context).get(url,
        new HttpRequest.OnSuccessListener() {
            @Override
            public void onSuccess(String obj) {
                Log.i("HTTP REQUEST", "Request Success.");
                /* do something here on Success */
            }
        },
        new HttpRequest.OnFailedListener() {
            @Override
            public void onFailed(String obj) {
                Log.i("HTTP REQUEST", "Request Failed.");
                /* do something here on Failed */
            }
        });
        
        
/* POST Request */
Map<String, String> map = new HashMap<>();
map.put("post_info_1", "data1");
map.put("post_info_2", "data2");

HttpRequest.getInstance(context).post(url, map,
        new HttpRequest.OnSuccessListener() {
            @Override
            public void onSuccess(String obj) {
                Log.i("HTTP REQUEST", "Request Success.");
                /* do something here on Success */
            }
        },
        new HttpRequest.OnFailedListener() {
            @Override
            public void onFailed(String obj) {
                Log.i("HTTP REQUEST", "Request Failed.");
                /* do something here on Failed */
            }
        });
```

So simple... ;)
