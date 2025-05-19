# ZR Audit Bundle Guide

## Installation
To install the ZR Audit Bundle, follow the steps below:

1. Ensure the below has been added to the `composer.json` **repositories** before the drupal repository:
   ```json
   {
      "type": "vcs",
      "url": "https://git.drupalcode.org/issue/schema-3465075"
   },
   ```
2. Ensure the below has been added to the `composer.json` **installer-paths**:
    ```sh
    "web/recipes/custom/{$name}": ["type:drupal-recipe"]
    ```
3. Run `composer require zr/zr-audit-bundle`
4. Run the following command (within the `/web` directory):

    ```sh
    ddev drush recipe recipes/custom/zr-audit-bundle
    ```

This command will execute the ZR Audit Bundle installation.

You should also get https://www.drupal.org/project/sensitive_data. To do this:
- `cd ~/.drush/commands`
- `git clone https://git.drupalcode.org/project/sensitive_data.git`
- `drush cc drush`

## Usage:

## Required:
This bundle installs the following:
- site_audit
- reroute_email
- hacked
- diff
- unused_modules
- coder
- security_review
- schema
- upgrade_status
- phpmd