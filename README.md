# Tindrels Website

Official website for Tindrels - hosted on GitHub Pages at tindrels.com

## Structure

```
tindrels/
├── index.html              # Main landing page
├── css/
│   ├── style.css          # Main stylesheet
│   └── privacy.css        # Privacy policy page styles
├── privacy/
│   └── template.html      # Template for app privacy policies
└── README.md
```

## Adding Privacy Policies for Apps

To add a privacy policy for a new app:

1. Copy `privacy/template.html` to a new file (e.g., `privacy/yourapp.html`)
2. Replace all instances of `[App Name]` with your actual app name
3. Replace `[Date]` with the current date
4. Fill in the specific details about your app's data collection and usage
5. The URL will be: `https://tindrels.com/privacy/yourapp.html`

## Hosting on GitHub Pages

1. Create a repository named `tindrelsllc.github.io` (or use a custom domain setup)
2. Push this code to the main/master branch
3. Go to repository Settings → Pages
4. Set source to deploy from main/master branch
5. For custom domain (tindrels.com):
   - Add a `CNAME` file with content: `tindrels.com`
   - Configure DNS with your domain registrar:
     - Add CNAME record: `www` → `tindrelsllc.github.io`
     - Add A records for apex domain pointing to GitHub's IPs:
       - `185.199.108.153`
       - `185.199.109.153`
       - `185.199.110.153`
       - `185.199.111.153`

## Local Development

Simply open `index.html` in your browser, or use a local server:

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (if you have npx)
npx serve
```

Then visit `http://localhost:8000`

## Customization

- **Colors**: Edit CSS variables in `css/style.css` under `:root`
- **Content**: Update `index.html` for main page content
- **Apps**: Add app cards in the `.apps-grid` section of `index.html`
- **Contact**: Email links point to team@tindrels.com
