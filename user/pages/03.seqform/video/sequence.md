---
title: Safety Video
sequence:
    banner: true
    content: below
contentEdit:
    nopreview: true
form:
    name: video
    fields:
        - name: tool
          type: text
          default: hammer
    buttons:
        - type: submit
          value: Watched Video
        - type: submit
          value: 'Did Not Watch'
          task: sequence_reset
    process:
        - next_page: true
---
![](timelapse.mp4?resize=85%,600)
