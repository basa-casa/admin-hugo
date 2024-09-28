---
title: Admin
collections:
  - import: collection admin-hugo-pages
    collection_type: import
menu:
  admin:
    weight: 10
cascade:
    outputs:
      - HTML
      - scms_config
      - help
    config:
      local_backend: true
      backend:
        branch: main
        name: github
        repo: basa-casa/hugo-admin
      media_folder: assets/img
      public_folder: img
      site_url: ../../
      display_url: /
      logo_url: "/img/hugo-admin.png"
draft: false
type: scms
---
 


The `admin-pages` collection generates instances of StaticCMS (scms), at `/admin/{{slug}}` by providing a title and collection import definitions. 
```yaml
{{< readfile file="/data/scms/collections/admin-pages.yml" >}}
```

## Create collections 
[Admin Collections](/admin/collections) has collections for creating folder collections, files collections, and collection sets. 
```yaml
{{< readfile file="/content/admin/collections/index.md" >}}
```
You can also create collections while editing admin pages, but only field `types:` from `/data/scms/fields/scms-collection-fields_primitive.yml` will be available. 
```yaml
{{< readfile file="/data/scms/fields/scms-collection-fields_primitive.yml" >}}
```