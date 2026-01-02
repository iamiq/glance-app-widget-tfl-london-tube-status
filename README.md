# London Transport Status (Glance widget)

## What this is
A https://github.com/glanceapp widget that shows live TfL status for all tube lines. 

It fetches official status data from the [TfL public Unified API](https://api.tfl.gov.uk) and renders:
- Line name
- Service status (Good Service, Minor Delays, etc.)
- Colour-coded indicator per line

## How it works
- Uses Glance’s `custom-api` widget.
- Calls TfL endpoints such as:
  - `/line/{line-id}/status`
  - `/line/mode/{mode}/status`

## Configuration
You control which lines appear via:

```yaml
options:
  lines:
    - northern
    - piccadilly
    - jubilee
```
If you want all lines to appear by default change the `lines` to 
```yaml
options:
  lines: []
