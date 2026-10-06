# মানবকল্যাণ যুব সংঘ — ডাইনামিক আয়-ব্যয় সিস্টেম

এই সংস্করণে **Supabase** ব্যবহার করা হয়েছে। ফলে অ্যাডমিন প্যানেল থেকে আয়/খরচ যোগ করলে public `finance.html`-এ হিসাব স্বয়ংক্রিয়ভাবে বদলাবে।

## ১) Supabase তৈরি
1. https://supabase.com এ একটি Project তৈরি করুন।
2. SQL Editor খুলে `supabase_schema.sql`-এর পুরো কোড রান করুন।
3. Authentication → Users থেকে সংগঠনের অনুমোদিত অ্যাডমিনের Email/Password user তৈরি করুন।
4. Project Settings → API থেকে Project URL এবং `anon public` key কপি করুন।
5. `config.js`-এ বসান:
   - `SUPABASE_URL`
   - `SUPABASE_ANON_KEY`
   - `BKASH_NUMBER`

## ২) ব্যবহার
- সাধারণ মানুষ: `finance.html`
- অনুমোদিত অ্যাডমিন: `admin.html`
- মূল সাইট: `index.html`

## গুরুত্বপূর্ণ নিরাপত্তা
- অ্যাডমিন ইমেইল/পাসওয়ার্ড কখনো HTML/JS ফাইলে লিখবেন না। Supabase Auth ব্যবহার করুন।
- দাতার ফোন নম্বর, বিকাশ SMS, PIN, OTP বা পূর্ণ ব্যক্তিগত তথ্য public করবেন না।
- নাম প্রকাশের আগে দাতার সম্মতি নেওয়া ভালো; চাইলে `Anonymous` ব্যবহার করুন।
- bKash নম্বর দেখানো এবং payment verification এক বিষয় নয়। স্বয়ংক্রিয় bKash payment verification করতে অনুমোদিত merchant/payment API দরকার।
