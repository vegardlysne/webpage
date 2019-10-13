+++
# Slider widget.
widget = "slider"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true # Activate this widget? true/false
weight = 1 # Order that this section will appear.

# Slide interval.
# Use `false` to disable animation or enter a time in ms, e.g. `5000` (5s).
interval = 5000

# Slide height (optional).
# E.g. `500px` for 500 pixels or `calc(100vh - 70px)` for full screen.
height = ""

# Slides.
# Duplicate an `[[item]]` block to add more slides.

  # Overlay a color or image (optional).
  #   Deactivate an option by commenting out the line, prefixing it with `#`.
  # overlay_img = "headers/bubbles-wide.jpg"  # Image path relative to your `static/img/` folder.
  overlay_filter = 0.5  # Darken the image. Value in range 0-1.

  # Call to action button (optional).
  #   Activate the button by specifying a URL and button label below.
  #   Deactivate by commenting out parameters, prefixing lines with `#`.
  # cta_label = "Download my thesis"
  # cta_url = "/files/PhD_Thesis_Lysne_2019.pdf"
  # cta_icon_pack = "fas"
  # cta_icon = "graduation-cap"

[[item]]
  title = "FENS - European Nutrition Conference"
  content = "I'm attending [FENS](http://www.fens2019.org/) 15-18 October"
  align = "center"  # Choose `center`, `left`, or `right`.
  overlay_color = "rgb(29, 33, 39)"  # An HTML color value.
  cta_label = "Conference notes"
  cta_url = "/contributions/courses/FENS2019.html"
  cta_icon_pack = "fas"
  cta_icon = "graduation-cap"

+++
