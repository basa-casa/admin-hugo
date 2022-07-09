---
title: "Admin"
type: netlifycms
menu:
  admin:
    weight: 10
collections:
  - collection_type: import
    import: collection admin-pages
cascade:
- outputs:
    - HTML
    - netlifycms_config
  config:
    local_backend: true
    backend:
      branch: main
      name: github
    media_folder: assets/img
    public_folder: img
    site_url: ../../
    display_url: /
    logo_url: /img/nc-admin.png
    collections: 
      - import: collection hugo-content-default
--- 
