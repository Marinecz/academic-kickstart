---
name: talks
    label: Talks
    label_singular: Talk
    folder: 'content/talk'
    path: '{{slug}}/index'
    create: true  # Allow users to create new documents in this collection
    fields:  # The fields each document in this collection have
      - {label: "Title", name: "title", widget: "string"}
      - {label: "Abstract", name: "abstract", widget: "text"}
      - {label: "Where", name: "location", widget: "text"}
      - {label: "From", name: "date", widget: "datetime"}
      - {label: "To", name: "date_end", widget: "datetime", default: ""}
      - {label: "All day event?", name: "all_day", widget: "boolean", default: false}
      - label: Links/Tickets
        name: links
        required: false
        widget: list
        fields:
          - {label: Link, name: url, widget: string}
          - {label: Link text, name: name, widget: string, required: false}
          - label: Icon pack
            name: icon_pack
            widget: select
            multiple: false
            required: false
            options:
              - {label: "None", value: ""}
              - {label: "Solid", value: "fas"}
              - {label: "Regular", value: "far"}
              - {label: "Brand", value: "fab"}
              - {label: "Academic", value: "ai"}
          - {label: "Icon (see https://sourcethemes.com/academic/docs/page-builder/#icons)", name: icon, widget: string, required: false}
      - {label: "Event", name: "event", widget: "string"}
      - {label: "Event link", name: "event_url", widget: "string"}
      - {label: "Publish this page on", name: "publishDate", widget: "datetime"}
      - {label: "Markdown slides (reference a deck in 'content/slides/')", name: "slides", widget: "string", required: false}
      - label: "Draft"
        name: "draft"
        widget: "boolean"
        default: false
      - label: "Featured"
        name: "featured"
        widget: "boolean"
        default: false
      - label: "Authors"
        name: "authors"
        required: false
        widget: "list"
      - label: "Tags"
        name: "tags"
        required: false
        widget: "list"
      - label: "Categories"
        name: "categories"
        required: false
        widget: "list"
      - label: "Projects (reference projects in 'content/project/')"
        name: "projects"
        required: false
        widget: "list"
      - label: "Featured Image"
        name: "image"
        required: false
        widget: object
        fields:
          - label: "Upload an image named `featured.jpg/png`"
            name: "filename"
            widget: "image"
            default: "featured"
            media_library:
              config:
                multiple: false
          - {label: Caption, name: caption, widget: string, required: false}
          - {label: Description for screen readers, name: alt_text, widget: string, required: false}
          - {label: "Where's the focal point in the image? Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.", name: focal_point, widget: string, required: false, default: "Smart"}
          - {label: Thumbnail Only?, name: preview_only, widget: boolean, default: false}
      - {label: "Details", name: "body", widget: "markdown", required: false}
      
---
