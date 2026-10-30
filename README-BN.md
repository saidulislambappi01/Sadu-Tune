# SADU TUNE — Android starter project

এই ZIP-এ SADU TUNE-এর একটি Android APK-buildable starter project আছে। এটি এখনো পূর্ণাঙ্গ YouTube Music বিকল্প নয়।

## এখন যা কাজ করে
- Android launcher app: SADU TUNE
- Dark / red music-style interface
- YouTube-এ গান ও ভিডিও সার্চ (অফিসিয়াল YouTube ফলাফল খোলে)
- Home, Downloads, Liked Songs ও Cloud Sync UI

## এখনো সেটআপ/ডেভেলপমেন্ট দরকার
- Google Sign-In ও Cloud Sync: Firebase project এবং `google-services.json`/OAuth configuration লাগবে।
- YouTube-এর in-app playback ও background playback: YouTube-এর অনুমোদিত API/SDK ও তাদের নীতিমালা মেনে আলাদা integration লাগবে। সাধারণ YouTube search link background audio দেয় না।
- Offline download: কেবল অধিকারপ্রাপ্ত/ডাউনলোড-অনুমোদিত অডিও সোর্সের জন্য বাস্তব download manager যোগ করতে হবে। YouTube content অনুমতি ছাড়া ডাউনলোড করা হবে না।
- বর্তমান ZIP-এ APK বাইনারি নেই; GitHub Actions দিয়ে APK build করার workflow আছে।

## মোবাইল থেকে APK বানানোর পথ
1. ZIP-টি GitHub-এ নতুন repository-তে upload করুন।
2. Repository-র Actions tab খুলুন।
3. `Build SADU TUNE APK` workflow নির্বাচন করে `Run workflow` চাপুন।
4. Build শেষ হলে Artifacts থেকে `SADU-TUNE-debug-apk` download করে extract করুন।
5. `app-debug.apk` Android ফোনে install করুন (প্রয়োজনে “Install unknown apps” অনুমতি দিন)।

এটি debug APK; Play Store release-এর জন্য আলাদা signing ও production configuration লাগবে।
