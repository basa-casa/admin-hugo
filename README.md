# /admin/config

## Installation
1. Import this module in your Hugo `config.toml`.
    ```toml
    [module]
        [[module.imports]]
            path = "github.com/basa-casa/admin-hugo"
    ```
    `config.yml`
    ```yaml
    module:
      imports:
        - path: github.com/basa-casa/admin-hugo
    ```
    `config.json`
    ```json
    {
        "module": {
            "imports": [
                {
                    "path": "github.com/basa-casa/admin-hugo"
                },
            ]
        }
    }
    ```
2. Vendor the module files for easier copying/overriding
    ```
    hugo mod vendor
    ```
3. Copy `/exampleSite/content/admin/` from all three admin modules, into your project.

4. Modify the `cascade.config` object in `_index.md` to reflect your project. This controls the static cms backend and other settings common to each sub-cms. 
