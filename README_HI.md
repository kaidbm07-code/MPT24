# MPT24 PWA + APK (मोबाइल से)

## अभी क्या तैयार है
- मोबाइल-फ्रेंडली MPT24 PWA prototype
- Solo, Duo, Squad demo match cards
- सभी मैच ₹0 / FREE दिखते हैं; कोई payment flow नहीं
- Demo join form (जानकारी केवल उसी फोन के browser localStorage में रहती है)
- Web app manifest और offline service worker

## Chrome से PWA install
1. `pwa` फ़ोल्डर की सभी फाइलें HTTPS hosting पर डालें (उदाहरण: GitHub Pages)।
2. GitHub account बनाकर नया public repository `mpt24` बनाएं।
3. ZIP extract करें; `pwa` फ़ोल्डर के अंदर की सामग्री repository के root में upload करें।
4. Repository → Settings → Pages → Deploy from branch → `main` / `/root` → Save.
5. GitHub Pages URL खुलने के बाद Android Chrome में खोलें → ⋮ → Install app या Add to Home screen.

## APK बनाना (कंप्यूटर के बिना)
1. पहले PWA को HTTPS URL पर publish करें।
2. Android Chrome से `https://www.pwabuilder.com/` खोलें और अपना GitHub Pages URL डालें।
3. Start → Package for stores → Android चुनें; उपलब्ध विकल्पों के अनुसार package generate करें।
4. Android package (आमतौर पर TWA) डाउनलोड करके signature/key setup पूरा करें। APK/AAB output उपलब्धता और signing निर्देश PWABuilder में दिखेंगे।
5. निजी फोन पर sideload APK install किया जा सकता है। Google Play पर publish करने के लिए Play Console और AAB/signing की अलग जरूरतें हो सकती हैं।

## जरूरी सीमा
यह अभी frontend demo है, live tournament service नहीं। Join form का data server/admin को नहीं जाता; सिर्फ उसी डिवाइस में रहता है। असली player login, central database, admin dashboard, room ID/password release, results और anti-cheat प्रक्रिया जोड़ने से पहले Firebase/Supabase जैसे backend और सुरक्षित admin access की जरूरत होगी। वास्तविक मैच/समय/slots admin द्वारा तय होने तक demo schedule को confirmed न मानें।

सभी टूर्नामेंट FREE हैं: Entry fee ₹0. इस prototype में payment gateway नहीं है।
