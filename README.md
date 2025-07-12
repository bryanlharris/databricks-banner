# Databricks Environment Banner with Stylus

This project adds a colored banner to the top of Databricks web pages using the Stylus browser extension. It helps you visually distinguish between dev, staging, and production workspaces to prevent mistakes.

## Supported Browsers

- Microsoft Edge
- Google Chrome
- Firefox

## Step 1: Install Stylus

1. Go to [Stylus in Chrome Web Store](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne)
2. Click **Add to Edge** (or Chrome/Firefox)
3. Approve permissions

## Step 2: Create Styles

Repeat this process for each environment.

### A. Dev Environment

1. Click the Stylus icon in your browser toolbar
2. Select **Manage**
3. Click **Write new style**
4. Name it: `Databricks DEV`
5. Under **Applies to**, choose:
   - `URLs starting with`
   - `https://dev-YOURORG.cloud.databricks.com/` *(replace with your actual dev workspace hostname)*
6. Paste the following CSS:

```css
/* === HOME ENVIRONMENT (Green) === */
body::before {
    content: "HOME ENVIRONMENT";
    display: block;
    background: green;
    color: white;
    text-align: center;
    font-weight: bold;
    padding: 2px;
    height: 24px;
    line-height: 20px;
}
```

```css
/* === DEV ENVIRONMENT (Green) === */
body::before {
    content: "DEV ENVIRONMENT";
    display: block;
    background: green;
    color: white;
    text-align: center;
    font-weight: bold;
    padding: 2px;
    height: 24px;
    line-height: 20px;
}
```

```css
/* === STAGING ENVIRONMENT (Blue) === */
body::before {
    content: "STAGING ENVIRONMENT";
    display: block;
    background: blue;
    color: white;
    text-align: center;
    font-weight: bold;
    padding: 2px;
    height: 24px;
    line-height: 20px;
}
```

```css
/* === PRODUCTION ENVIRONMENT (Red) === */
body::before {
    content: "PRODUCTION ENVIRONMENT";
    display: block;
    background: red;
    color: white;
    text-align: center;
    font-weight: bold;
    padding: 2px;
    height: 24px;
    line-height: 20px;
}
```


