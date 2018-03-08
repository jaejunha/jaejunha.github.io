---
layout: post 
tag: Android
title: Lock screen
date: 2018.03.08
---

## Lock screen  
If you want to make lock screen started when screen is on, you need to implement several things: Broadcast Receiver, Service, and etc...   

First, to catch screen on event, you make **Broadcast Receiver class**  
```
public class LockReceiver extends BroadcastReceiver {
	@Override
	public void onReceive(Context context, Intent intent) {
		if(intent.getAction().equals("android.intent.action.SCREEN_OFF")) {
			Intent intent_lockIntent = new Intent(context, LockActivity.class);
			intent_lockIntent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
			context.startActivity(intent_lockIntent);
		}
	}
}
```
I think it is better to use SCREEN_OFF event rather than SCREEN_OFF event. That's because turning on activity before screen is displayed can cause a little overhead   
In addition, to remove duplicate activity, I use Intent.FLAG_ACTIVITY_CLEAR_TOP flag  
  
Second, you must modify **AndroidManifest.xml** file to catch SCREEN_OFF action
```
<receiver
	android:name=".util.receiver.LockReceiver"
	android:enabled="true"
	android:exported="false">
	<intent-filter >
		<action android:name="android.intent.action.SCREEN_OFF"/>
	</intent-filter>
</receiver>
```
  
If you want to use action: SCREEN_OFF, then you need to implement service for it  
```
public class LockService extends Service {
	private LockReceiver lockReceiver;

	@Nullable
	@Override
	public IBinder onBind(Intent intent) {
		return null;
	}

	@Override
	public void onCreate() {
		super.onCreate();
		lockReceiver = new LockReceiver();
		IntentFilter filter = new IntentFilter(Intent.ACTION_SCREEN_OFF);
		registerReceiver(lockReceiver, filter);
	}

	@Override
	public void onDestroy(){
		super.onDestroy();

		if(lockReceiver != null)
		unregisterReceiver(lockReceiver);
	}
}
```
Using **registerReceiver()** method, you can register not only **receiver class** but aslo **intent filter**   
If you finish all of step, then you can see the result   