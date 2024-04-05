# Widget Configuration Parameters

## `WIDGET_BUTTON_TYPE`
Type: `string`  
Description: Defines the type of button to be displayed on the widget. Options include `inline`, `overlay`, or `floating`.  
Example: 
    
    "WIDGET_BUTTON_TYPE": "inline"


## `THEME_COLOR`
Type: `string`  
Description: Specifies the primary color of the widget theme, given in hexadecimal format.  
Example: 

    "THEME_COLOR": "#5C305F"


## `THEME_BORDER_RADIUS`
Type: `string`  
Description: Sets the border-radius of the widget elements, defined in pixels.  
Example: 
    
    "THEME_BORDER_RADIUS": "10px"

## `WIDGET_BORDER`
Type: `string`  
Description: Determines the border style of the widget, specified with CSS syntax.  
Example: 

    "WIDGET_BORDER": "1px solid #121212"

## `WIDGET_EDGES`
Type: `string`  
Description: Sets the edge size of the widget, defined in pixels.  
Example: 

    "WIDGET_EDGES": "8px"

## `USER_LOCALE`
Type: `string`  
Description: Configures the locale setting for the user interface, influencing language and formatting.  
Example: 

    USER_LOCALE": "nl-NL"


### `BRANDING_LOGO_URL`
Type: `string`  
Description: URL to the logo used for branding purposes within the widget.  
Example: 
    
    "BRANDING_LOGO_URL": "https://some-url.com"

## `ENABLE_EMAIL_PNR`
Type: `boolean`  
Description: Toggles the feature to allow users to input PNR via email.  
Example: 

    "ENABLE_EMAIL_PNR": true

## `SUPPORT_EMAIL`
Type: `string`  
Description: Email address for support inquiries.  
Example: 

    "SUPPORT_EMAIL": "support@automicle.com"

## `IOS_APP_LINK`
Type: `string`  
Description: URL to the iOS app on the Apple App Store.  
Example: 

    "IOS_APP_LINK": "https://apps.apple.com/us/app/acompanion/id6449096055/"

## `ANDROID_APP_LINK`
Type: `string`  
Description: URL to the Android app on the Google Play Store.  
Example: 

    "ANDROID_APP_LINK": "https://play.google.com/store/apps/details?id=com.automicle.app.companion"

## `JOURNEY_INSTRUCTIONS`
Type: `array`  
Description: A list of instructions for users to follow during their journey.  
Example:

    "JOURNEY_INSTRUCTIONS": [
    "Activate your ticket before the journey date.",
    "Familiarize yourself with the rules and regulations.",
    "Arrive early at the departure point.",
    "Keep your ticket accessible throughout the journey."
    ]"


## `APP_DOWNLOAD_INSTRUCTIONS`
Type: `array`  
Description: Instructions for downloading and using the companion mobile app.  
Example:

    "APP_DOWNLOAD_INSTRUCTIONS": [
    "Download the App: Tap on the provided image to download the companion app.",
    "Enter PNR and Confirm: Open the app, enter your PNR, and confirm your journey.",
    "Scan Ticket: Use the app to scan each ticket’s barcode or QR code for easy access and validation."
    ]


## `JOURNEY_ENABLED_DATES`
Type: `array`  
Description: Specific dates on which the journey feature is enabled.  
Example: 

    "JOURNEY_ENABLED_DATES": ["2023-09-02", "2023-10-07"]

## `JOURNEY_ENABLED_WEEKDAYS`
Type: `array`  
Description: Days of the week when the journey feature is available.  
Example: 

    "JOURNEY_ENABLED_WEEKDAYS": ["Sunday", "Monday", "Wednesday"]

## `JOURNEY_TICKET_REDIRECT_LINK`
Type: `string`  
Description: URL where users will be redirected afterr the purchase of journey tickets.  
Example: 

    "JOURNEY_TICKET_REDIRECT_LINK": "https://automicle.com"

## `USER_INPUT_FORM`
Type: `array`  
Description: Configuration for input forms presented to the user, including fields such as name, email, and university selection. This array comprises various objects, each representing a different type of input field, including text inputs, dropdowns, checkboxes, and custom alert cards.
- **Text Input**
  - `type`: "text"
  - `label`: Descriptive label for the input field.
  - `placeholder`: Placeholder text shown inside the input box.
  - `name`: Unique identifier for the field.
    ```
    {
    "type": "text",
    "label": "First Name",
    "placeholder": "Enter your first name",
    "name": "firstName"
    }
    ```
- **Email Input**
  - `type`: "email"
  - `label`: Descriptive label specifically for email addresses.
  - `placeholder`: Placeholder text for email input.
  - `name`: Unique name for the email field.

    ```
    {
    "type": "email",
    "label": "Email",
    "placeholder": "Enter your email",
    "name": "email"
    }
- **Dropdown**
  - `type`: "dropdown"
  - `label`: Label for the dropdown menu.
  - `placeholder`: Placeholder text displayed in the dropdown.
  - `name`: Identifier for the dropdown.
  - `options`: Array of option objects, each with an `id` and `name`.

    ```
    {
        "type": "dropdown",
        "label": "University",
        "placeholder": "Select",
        "name": "university",
        "options": [
            {
                "id": 1,
                "name": "Automicle"
            }
        ]
    }

- **Checkbox**
  - `type`: "checkbox"
  - `name`: Name for the checkbox field.
  - `checkboxText`: Text or HTML content displayed alongside the checkbox.

    ```
    {
        "type": "checkbox",
        "name": "termsNConditionCheck",
        "checkboxText": "<p>By using this service</p>"
    }

- **Alert Card**
  - `type`: "alertcard"
  - `alertCardType`: Specifies the type of alert (`alert`, `warn`, `info`).
  - `heading`: Optional heading for the card.
  - `body`: Main content body of the card.
  
    ```
    {
        "type": "alertcard",
        "alertCardType": "info",
        "heading": "Example Heading",
        "body": "Example body text."
    }

## `START_LOCATION` and `END_LOCATION`
Type: `array`  
Description: Lists of start and end locations for journeys, including details such as name, coordinates, image, and stop type.  
Example:

    "START_LOCATION": [
        {
        "name": "Amsterdam Airport Schiphol (AMS)",
        "lon": 4.7643411,
        "lat": 52.30951,
        "image": "custom-stop-image",
        "stopType": "RAIL"
        },
        ...
    ]