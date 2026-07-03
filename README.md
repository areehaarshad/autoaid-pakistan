# AutoAid Pakistan — Clickable Prototype

24/7 roadside assistance app ka clickable HTML/CSS prototype. Sab screens aapas mein linked hain — GitHub Pages pe direct deploy karne ke liye ready.

## 🚀 Live Deploy (GitHub Pages)

1. GitHub pe naya **public** repo banayein (e.g. `autoaid-pakistan`).
2. Is folder ki saari files (`.html`, `.png`, `style.css`) repo ke root mein upload karein.
3. Repo → **Settings → Pages**:
   - Source: `Deploy from a branch`
   - Branch: `main` / folder: `/root`
   - **Save**
4. 1–2 min baad site live: `https://<username>.github.io/autoaid-pakistan/`

## 📱 Screen Flow

```
index.html (Splash)
   └─▶ login.html ──▶ dashboard.html
          └─▶ register.html ──▶ otp.html ──▶ dashboard.html

dashboard.html
   ├─▶ issue.html ──▶ location.html ──▶ searching.html ──▶ assigned.html
   │                                                            ├─▶ tracking.html ──▶ chat.html
   │                                                            └─▶                 tracking.html ──▶ payment.html ──▶ feedback.html ──▶ dashboard.html
   ├─▶ history.html
   ├─▶ garage.html
   ├─▶ sos.html ──▶ searching.html
   ├─▶ login.html (logout)
   └─▶ profile.html
          ├─▶ history.html
          ├─▶ wallet.html
          ├─▶ settings.html ──▶ about.html
          ├─▶ notifications.html
          └─▶ complaint.html
```

## 📂 File Structure

| File | Screen |
|---|---|
| `index.html` | Splash / Welcome |
| `login.html` | Sign In |
| `register.html` | Create Account |
| `otp.html` | OTP Verification |
| `dashboard.html` | Home / Service Menu |
| `issue.html` | Select Issue |
| `location.html` | Set Location (GPS) |
| `searching.html` | Finding Mechanic (radar) |
| `assigned.html` | Provider Assigned |
| `tracking.html` | Live GPS Tracking |
| `chat.html` | Chat with Mechanic |
| `payment.html` | Payment / Invoice |
| `feedback.html` | Rate Service |
| `complaint.html` | Register Complaint |
| `profile.html` | User Profile |
| `history.html` | Service History |
| `garage.html` | My Vehicles |
| `wallet.html` | Digital Wallet / Cards |
| `settings.html` | App Settings |
| `sos.html` | Emergency SOS |
| `about.html` | About & Terms |
| `notifications.html` | Notification Center |
| `style.css` | Shared stylesheet for all screens |
| `bg-road.png` | App logo |
| `scene-bg.png` | Background scene image |

## 🛠 Local Preview

Koi build step nahi chahiye — bas `index.html` ko kisi bhi browser mein khol lein, ya VS Code ke "Live Server" extension se open karein taake sab relative links (CSS/images) sahi load hon.

## ✏️ Notes

- Saare forms (login/register/OTP) demo ke liye hain — koi real backend/database connected nahi hai, submit karne par bas agli screen pe le jaate hain.
- `searching.html` 3.5 second baad khud `assigned.html` pe redirect ho jaati hai (radar scan complete hone ka simulation).
