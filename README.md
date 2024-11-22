<img src="icon.png"/>

# Old Reddit Redirect Chrome Extension

An extension for Chrome that redirects the user to the old version of Reddit.

## Features

- Redirects all `www.reddit.com` URLs to `old.reddit.com`
- Redirects Reddit gallery URLs to old Reddit comments
- Allows specific Reddit paths without redirection
- Removes `Accept` header for specific Reddit image domains

## Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/zuedev/old-reddit-redirect-chrome-extension.git
   cd old-reddit-redirect-chrome-extension
   ```

2. Open Chrome and navigate to `chrome://extensions/`.

3. Enable "Developer mode" by toggling the switch in the top right corner.

4. Click on "Load unpacked" and select the cloned repository folder.

## Permissions Justification

### declarativeNetRequestWithHostAccess

The `declarativeNetRequestWithHostAccess` permission is required to enable our extension to intercept and modify network requests. This is essential for redirecting users from the new version of Reddit to the old version. By using this permission, we ensure that the redirection happens seamlessly and efficiently without compromising user privacy or security.

### host_permissions

The `host_permissions` permission is necessary to specify the domains that our extension will interact with. In this case, we need access to `https://www.reddit.com/*` to detect when a user is navigating to the new version of Reddit and to redirect them to the old version. This permission is scoped to only the Reddit domain to minimize the extension's access to other web resources, ensuring that it operates within the least privilege principle.
