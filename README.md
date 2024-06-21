<p align="center">
<p align="center">
  <a href="https://github.com/i-rin-eam">
    <img src="https://avatars.githubusercontent.com/u/154800878?s=400&u=5d18880cc28646190a19a971bfcdbc54644eab07&v=4" alt="Logo" width="100" height="100">
  </a> 
<h2 align='center'>Send Firebase Push Notifications to allDevices from Server using the new FCM HTTP v1 API</h12>
</p>

## Step 1: change to `firebase.php` code.
```php
$arrayToSend = array('topic' => 'allDevices','data' => $datamsg);
```
## Step 2: change to `java` code.
```java
     FirebaseMessaging.getInstance().subscribeToTopic("allDevices")
                .addOnCompleteListener(new OnCompleteListener<Void>() {
                    @Override
                    public void onComplete(@NonNull Task<Void> task) {
                        String msg = "Subscribed to topic";
                        if (!task.isSuccessful()) {
                            msg = "Subscription failed";
                        }
                        Log.d("token", msg);
                    }
                });
```
## Authors

**MD YEAMIN** - Android Software Developer <a href="https://www.youtube.com/@LearnWithYeamin">**(Learn With Yeamin)**</a> 

<h1 align="center">Thank You ❤️</h1>
