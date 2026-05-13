# Google Analytics 4 Setup Instructions
## For: Gunnison Wildfire Mitigation Workshop Website

These instructions will walk you through creating a new GA4 property and adding the Measurement ID to the website.

---

### Step 1: Create a Google Analytics Account (or sign in)

1. Go to [analytics.google.com](https://analytics.google.com)
2. Sign in with a Google account (or create one if needed)
3. If this is your first time, click **Start measuring**

---

### Step 2: Create a New Property

1. In the left sidebar, click the **gear icon** (Admin) at the bottom
2. Under the **Property** column, click **Create Property**
3. Fill in the details:
   - **Property name**: `Gunnison Wildfire Mitigation Workshop`
   - **Reporting time zone**: `United States – Mountain Time`
   - **Currency**: `US Dollar`
4. Click **Next**, fill in your business details, then click **Create**

---

### Step 3: Set Up a Data Stream

1. After creating the property, you'll be prompted to set up a data stream — choose **Web**
2. Enter the website details:
   - **Website URL**: `https://gunnisonwildfiremitigation.org`
   - **Stream name**: `Gunnison Wildfire Mitigation`
3. Leave **Enhanced measurement** turned on
4. Click **Create stream**

---

### Step 4: Copy Your Measurement ID

1. After creating the stream, you'll see a **Measurement ID** at the top right of the stream details — it looks like `G-XXXXXXXXXX`
2. Copy that ID

---

### Step 5: Send the Measurement ID to Paul

Send Paul the Measurement ID (e.g. `G-XXXXXXXXXX`) so he can plug it into the website code. He'll replace the placeholder in two spots in `index.html`:

```html
<!-- Replace both instances of G-XXXXXXXXXX with your real ID -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

### Step 6: Verify It's Working

Once Paul has updated and deployed the site, you can verify data is flowing:

1. Go to [analytics.google.com](https://analytics.google.com) and open your property
2. In the left sidebar, click **Reports → Realtime**
3. Visit [gunnisonwildfiremitigation.org](https://gunnisonwildfiremitigation.org) in another tab
4. You should see yourself appear as an active user within a minute or two

---

### Notes

- It can take **24–48 hours** for full data to start populating in most reports
- The Realtime report works immediately once the ID is in place
- If you don't see data after a few days, double-check the Measurement ID was entered correctly
