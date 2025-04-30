# PayPal Button Configuration Options

This document provides an overview of the various configuration options available for PayPal buttons.

## Button Style Options

### Layout
Controls the arrangement of funding icons on the button.

```javascript
style: {
  layout: 'vertical' // or 'horizontal'
}
```

- `vertical`: Show funding options in a vertical stack (recommended for mobile).
- `horizontal`: Show funding options side by side (default).

### Color
Controls the background color of the button.

```javascript
style: {
  color: 'gold' // default
}
```

Options:
- `gold` (default)
- `blue`
- `silver`
- `white`
- `black`

### Shape
Controls the border of the button.

```javascript
style: {
  shape: 'rect' // default
}
```

Options:
- `rect` (default): Rectangular button with sharp corners
- `pill`: Rectangular button with rounded corners

### Height
Controls the height of the button in pixels.

```javascript
style: {
  height: 40 // default is 40
}
```

### Label
Controls the text displayed on the button.

```javascript
style: {
  label: 'paypal' // default
}
```

Options:
- `paypal` (default): Shows "PayPal" text
- `checkout`: Shows "Checkout" text
- `buynow`: Shows "Buy Now" text
- `pay`: Shows "Pay with PayPal" text
- `installment`: Shows "Pay in Installments" text

### Tagline
Controls whether to show a tagline below the button.

```javascript
style: {
  tagline: false // default is true
}
```

## Full Example

```javascript
paypal.Buttons({
  style: {
    layout: 'vertical',
    color: 'blue',
    shape: 'pill',
    label: 'buynow',
    height: 50,
    tagline: false
  },
  createOrder: function(data, actions) {
    // ...
  },
  onApprove: function(data, actions) {
    // ...
  }
}).render('#paypal-button-container');
```

## Button Capabilities

### Disable funding sources
You can disable specific funding sources in the PayPal SDK script tag:

```html
<script src="https://www.paypal.com/sdk/js?client-id=YOUR_CLIENT_ID&disable-funding=credit,card"></script>
```

Options:
- `credit`: PayPal Credit
- `card`: Credit cards
- `venmo`: Venmo
- `sepa`: SEPA-Lastschrift
- And others depending on country

### Enable funding sources
You can explicitly enable specific funding sources:

```html
<script src="https://www.paypal.com/sdk/js?client-id=YOUR_CLIENT_ID&enable-funding=venmo,sepa"></script>
```

## References

- [PayPal Buttons Documentation](https://developer.paypal.com/docs/checkout/standard/customize/buttons-style-guide/)
- [PayPal JavaScript SDK Reference](https://developer.paypal.com/docs/checkout/reference/customize-sdk/) 