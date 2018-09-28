---
title: Sequential Form
slug: seqform
cache_enable: false
sequence:
    banner: true
    content: above
form:
    name: collect-data:
    fields:
        - name: location
          type: text
          label: Location
        - name: mood
          type: text
          label: Mood
        - name: tool
          type: hidden
          label: Tool
    buttons:
        - type: submit
          value: 'Start Registration'
    process:
        - sequence:
            routes:
                - video
                - terms
            icons:
                - address-card
                - video-camera
                - thumbs-up
        - sql-insert:
            table: data
        - redirect: seqform/final
---
# User Registration Data
