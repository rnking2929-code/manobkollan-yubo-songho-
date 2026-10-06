মানবকল্যাণ যুব সংঘ — Supabase Connected Build

এই ZIP-এ Supabase URL ও Publishable key config.js-এ বসানো আছে।

GitHub-এ আপলোড:
1) repository খুলুন
2) Add file → Upload files
3) এই ZIP-এর ভেতরের ফাইলগুলো repository root-এ আপলোড করুন; ZIP নিজে আপলোড করবেন না
4) config.js, finance.html, admin.html, index.html সহ প্রয়োজনীয় ফাইল Replace/Commit করুন
5) GitHub Pages deployment শেষ হলে Visit site চাপুন

Finance:
- finance.html public transactions পড়বে
- admin.html Supabase Auth দিয়ে login করে transaction যোগ করবে

নিরাপত্তা:
- Database password, service-role/secret key কখনো frontend-এ দেবেন না
- Publishable/anon key frontend-এ থাকা স্বাভাবিক
- Public donor phone/OTP/PIN প্রকাশ করবেন না
- Production-এ write policy নির্দিষ্ট admin user/role-এ সীমাবদ্ধ করা উচিত
