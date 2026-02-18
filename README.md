# cloudinary-react-simple-demo
## Cloudinary Setup

### Step 1: Create Cloudinary Account

1. Sign up at [cloudinary.com](https://cloudinary.com/)
2. Free tier includes **25 GB storage** and **25 GB bandwidth per month**
3. Complete email verification

### Step 2: Get Cloud Name

1. Log in to Cloudinary dashboard
2. Note your **Cloud Name** (visible on the dashboard homepage)
   - Format: `dxxxxxxxxx`

### Step 3: Create Unsigned Upload Preset

1. In Cloudinary dashboard, go to **Settings** → **Upload**
2. Scroll to **Upload Presets** section
3. Click **Add upload preset**
4. Fill in:
   - **Preset Name:** `react-demo` (or any name)
   - **Signing Mode:** Select **Unsigned**
   - **Allowed formats:** Leave as default or specify (e.g., jpg, png, gif)
5. Click **Save**
6. Copy the preset name

### Step 4: Get Your Credentials

You now have:
- **Cloud Name:** e.g., `dxjlref2c`
- **Upload Preset:** e.g., `react-demo`

### Step 5: 

npm install
```

### Step 6: Create Environment File

Create `.env` in project root (inside the cloudinary-demo folder):

```env
VITE_CLOUDINARY_CLOUD_NAME=your-cloud-name
VITE_CLOUDINARY_UPLOAD_PRESET=your-upload-preset
```

Replace with your actual credentials from Step 4.

### Step 6: Run the App

```powershell
npm run dev
```

Opens at `http://localhost:5173/`

---

## Usage

1. Click the upload box
2. Select an image file
3. Image uploads to Cloudinary instantly
4. Image URL and thumbnail displayed
5. "Remove" button deletes from display (but image stays on Cloudinary)

---

## Key Features

- **No backend** – Uploads directly to Cloudinary
- **Unsigned upload** – No API key needed in frontend
- **Instant display** – Shows uploaded images immediately
- **Responsive grid** – Images display in auto-fit columns

---

## File Structure

```
cloudinary-demo/
├── .env
├── package.json
├── vite.config.js
├── index.html
├── src/
│   ├── App.jsx       (main upload component)
│   ├── App.css
│   └── main.jsx
```

---

## Next Steps

- Add drag-and-drop support for file upload
- Display image metadata (size, dimensions)
- Add delete functionality with Cloudinary API (requires backend)
- Add image transformations (resize, filters, effects)
- Store URLs in a database (requires backend)
- Add multiple file upload

---

## Troubleshooting

**Q: Upload fails with "Unsigned preset required"**
- Ensure upload preset has **Signing Mode: Unsigned**

**Q: Images not displaying**
- Check `VITE_CLOUDINARY_CLOUD_NAME` spelling in `.env`
- Verify preset name matches exactly

**Q: "Cloudinary is not configured" error**
- Ensure `.env` exists and has correct keys
- Run `npm run dev` again after creating `.env`

