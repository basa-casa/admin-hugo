---
title: Fields
collections:
  - import: collection scms-string-fields
    collection_type: import
  - import: collection scms-boolean-fields
    collection_type: import
  - import: collection scms-select-fields
    collection_type: import
  - import: collection scms-object-fields
    collection_type: import
  - import: collection scms-list-fields
    collection_type: import
  - import: collection scms-list-variable-types-fields
    collection_type: import
  - import: collection scms-number-fields
    collection_type: import
  - import: collection scms-datetime-fields
    collection_type: import
  - import: collection scms-color-fields
    collection_type: import
  - import: collection scms-text-fields
    collection_type: import
  - import: collection scms-image-fields
    collection_type: import
  - import: collection scms-file-fields
    collection_type: import
  - import: collection scms-markdown-fields
    collection_type: import
  - import: collection scms-relation-fields
    collection_type: import
  - import: collection scms-code-fields
    collection_type: import
  - import: collection scms-map-fields
    collection_type: import
  - collection_type: files
    name: Admin
    label: "Admin"
    description: "Control the files that control the collection forms active in this CMS. "
    files:
      - type: file
        name: content/admin/fields/index.md
        label: content/admin/fields/index.md
        file: content/admin/fields/index.md
        fields:
          - field_type: import
            import: collection admin-pages.fields
menu:
  admin:
    weight: 20
---
