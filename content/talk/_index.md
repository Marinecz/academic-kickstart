---
title: Recent & Upcoming Talks

# View.
#   1 = List
#   2 = Compact
#   3 = Card
view: 2

# Optional header image (relative to `static/img/` folder).
header:
  caption: ""
  image: ""
  
  
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
  
---
