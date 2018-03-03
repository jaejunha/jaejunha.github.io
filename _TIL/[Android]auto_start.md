---
layout: post 
tag: Android
title: Auto start
date: 2018.03.03
---

## Auto start  
To start you application **when system is booted**, you must use **broadcast**  
So, firt you need to make your broadcast class  
```
public class BootReceiver extends BroadcastReceiver{
	@Override
	public void onReceive(Context context, Intent intent) {
		if(intent.getAction().equals("android.intent.action.BOOT_COMPLETED"))
			Intent newIntent = new Intent(context,StartActivity.class);
			newIntent.addFlags(Intent.Flag_ACTIVITY_NEW_TASK);
			context.startActivity(newIntent));
		}
	}
}
```
To catch booting event, you must check **whether event is boot event or not**. So, I check the event using "if" statement. Next, to start initial activity, **make new intent**. Following above codes, StartActivity is my initial activity. Finally, **by using "startActivity" method**, you can call your initial activity.  

However, work is not finished. You must register **permission and broadcast information at AndroidManifest.xml**  
- Permission  
```
<uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED" />
```
- Receiver  
```
<receiver
	android:name=".util.receiver.BootReceiver"
	android:enabled="true"
	android:exported="false">
	<intent-filter >
		<action android:name="android.intent.action.BOOT_COMPLETED"/>
	</intent-filter>
</receiver>
```
To catch boot event, you must **register action related to boot event at intent-filter**  