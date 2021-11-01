---
title: Use macros
---
The following macros contain the configuration parameters for certain page elements. These macros inject specific content or functionality automatically.

## orgName

Inserts the org name title.

Example:

```html
<title>{{orgName}} - {{errorSummary}}</title>
```

## errorSummary

Inserts the error title text.

Example:

```html
<h2 class="o-form-title">{{errorSummary}}</h2>
```

## bgImageUrl

Inserts a URL to the background image configured for your application. You can change this image using the **Sign-in Configuration** option accessed by selecting **Settings**, and then **Appearance** from the Admin Console, but this changes the background image in all instances where the macro is used, including your custom sign-in page.

If you want to just change the background image for your custom error pages, include the URL to the image instead of the macro:

Example:

```html
<div class="login-bg-image" style="background-image: url('https://example.com//YourBackgroundImage.png')"></div>
```

## orgLogo

Inserts the logo image that has been configured for your application. You can change this logo using the **Organization Logo** option accessed by selecting **Settings**, and then **Appearance** from the Admin Console, but this changes the org logo in all instances where the macro is used, including your custom sign-in page.

If you want to just change the logo image for your custom error pages, include the URL to the image instead of the macro:

Example:
```html
<img alt="{{orgName}}" src="https://example.com//SomeOtherImage.png" class="org-logo">
```

## errorSummary and errorDescription

Inserts a title and detailed description of the error.

Example:

```html
<h2 class="o-form-title">{{errorSummary}}</h2>
<p class="o-form-explain">What happened? {{{errorDescription}}}</p>
```

## back

Inserts the text `Go to Homepage`. The button takes the user back to the sign-in page when clicked.

Example:

```html
 <a href="/" class="button">{{back}}</a>
```

## technicalDetails

Inserts additional error codes, if there are any. See [Okta Error Codes](/docs/reference/error-codes/#okta-error-codes-listed-by-error-code) for more information.

Example:

```html
<p class="technical-details">Additional Error Details: {{technicalDetails}}</p>
```

> **Note:** Macros only available with Branding

## buttonText

Inserts the button text based on the page context. The button takes the user back to the `buttonHref` when clicked. `{{back}}` is also supported for the same purpose.

## buttonHref

Inserts the href for the button.

Example:

```html
 <a href="{{buttonHref}}" class="button">{{buttonText}}</a>
```

## themedStylesUrl

Inserts the href for the themed style sheet.

Example:

```html
 <link href="{{themedStylesUrl}}" rel="stylesheet" type="text/css">
```

## faviconUrl

Inserts the href for the favicon.

Example:

```html
 <link rel="shortcut icon" href="{{faviconUrl}}" type="image/x-icon"/>
```

<NextSectionLink/>
