# /admin/config

## Installation
1. Import this module in your Hugo `config.toml`.
    ```toml
    [module]
        [[module.imports]]
            path = "github.com/basa-casa/hugo-admin"
    ```
    `config.yml`
    ```yaml
    module:
      imports:
        - path: github.com/basa-casa/hugo-admin
    ```
    `config.json`
    ```json
    {
        "module": {
            "imports": [
                {
                    "path": "github.com/basa-casa/hugo-admin"
                },
            ]
        }
    }
    ```
2. Vendor the module files for easier copying/overriding
    ```
    hugo mod vendor
    ```
3. Copy `/exampleSite/content/admin/_index.md` into your project
    ```
    cp _vendor/github.com/basa-casa/hugo-admin/exampleSite/content/admin/_index.md exampleSite/content/admin/_index.md
    ```
4. Modify the `cascade.config` object to reflect your project. This controls the static cms backend and other settings common to each sub-cms. 
5. Copy `/exampleSite/content/admin/content/index.md` into your project
    ```
    cp _vendor/github.com/basa-casa/hugo-admin/exampleSite/content/admin/content/index.md exampleSite/content/admin/content/index.md
    ```
6. Repeat Step 5 as needed, for other Admin CMS files you want to control. 

## Usage
### Getting Started
1. Run `hugo server`
    
2. Open [http://localhost:1313](http://localhost:1313)

Your site now has a mostly-blank **index page** at `/`, **CMS instances** at `/admin`, `/admin/collections`, `/admin/fields`, `/admin/content`, `/admin/configuration`, `/admin/data`, `/admin/help`, and **help pages** at 
`/admin/help/admin/*` for each CMS.
### /admin

Manages the name, collections, and menu placement of each `/admin/{{cms}}/index.md`

### /admin/content

Controls the collections available to content editors. You need to recreate this cms in /admin or by copying `/exampleSite/content/admin/content/index.md` from the module into your project and edit the list of collections.

### /admin/collections

Create and manage collections as individual `.yml` files in `/data/scms/collections` for import to any CMS. 

### /admin/fields
Has collections enabled for creating 16 different types of fields as individual `.yml` files in `/data/scms/fields` for import to any collection or parent field. 

### /admin/configuration
Manage the Hugo configuration, with collections available for creating an individual config.(toml,yaml,json) files
Hugo config.modules?
Hugo Environments

### /admin/help

Edits the markdown body for each admin (_)index.md file, creating help pages at (/admin/help/admin)(http://localhost:1313/admin/help/admin/content) and the like.

