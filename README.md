# ZR Audit Bundle Installation Guide

To install the ZR Audit Bundle, follow the steps below:

1. Ensure the below has been added to the `composer.json` **installer-paths**:
    ```sh
    "web/recipes/custom/{$name}": ["type:drupal-recipe"]
    ```
2. Run `composer require zr/zr-audit-bundle`
3. Run the following command (within the `/web` directory):

    ```sh
    ddev drush recipe recipes/custom/zr-audit-bundle
    ```

This command will execute the ZR Audit Bundle installation.