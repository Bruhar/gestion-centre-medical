# Gestion Centre Médical
```markdown
This project is a Drupal 11-based web application for managing a medical center. It includes features for handling doctor profiles, patient appointments, and internal content management. The site is built using Composer and DDEV for modern PHP and Drupal development workflows.
```

## Project Structure

├── .ddev/                 # DDEV configuration for local environment <br>
├── vendor/                # Composer dependencies (not committed) <br>
├── web/                   # Drupal web root <br>
│   ├── core/              # Drupal core (managed by Composer) <br>
│   ├── modules/           # Modules (contrib/custom) <br>
│   ├── themes/            # Themes (contrib/custom) <br>
│   ├── sites/             # Site-specific configuration and files <br>
├── composer.json          # Project dependencies and scripts <br>
├── composer.lock          # Locked versions of dependencies <br>
├── README.md              # Project documentation <br>

## Requirements
````
- PHP 8.1 or higher
- Composer 2.x
- DDEV (Docker-based development environment)
- Git
````
## Setup Instructions

1. **Clone the project:**

```bash
   git clone https://github.com/Bruhar/gestion-centre-medical.git gestion-centre-medical
   cd gestion-centre-medical
````

2. **Start DDEV:**

   ```bash
   ddev start
   ```

3. **Install dependencies:**

   ```bash
   ddev composer install
   ```

4. **Install Drupal (web installer or Drush):**

   ```bash
   ddev drush site:install
   ```

5. **Access the site:**

   ```
   http://gestion-centre-medical.ddev.site
   ```

## Features

* Custom Content Type: `Médecin` (Name, Speciality, Phone, Email)
* Webform for patient appointment booking
* Clean URLs with Pathauto
* Admin-friendly interface with Admin Toolbar
* Configurable permissions and user roles

## Development Workflow

* All custom code should be placed in:

  * `web/modules/custom/`
  * `web/themes/custom/`
* Use Drush or the Drupal UI for configuration
* Configuration can be exported with:

  ```bash
  ddev drush config-export
  ```
* Commit only configuration and custom code (not vendor or files)

## Useful Commands

* Start environment: `ddev start`
* Clear cache: `ddev drush cr`
* Export config: `ddev drush cex`
* Import config: `ddev drush cim`
* Login as admin: `ddev drush uli`

## Git Best Practices

* Do not commit `/vendor/` or `/web/core/`
* Track `composer.json`, `composer.lock`, and config exports
* Use feature branches for new development

## License

This project is open source and publicly available. It uses [Drupal](https://www.drupal.org/about/licensing) (GPL-2.0-or-later) as its core framework. Contributed modules and themes follow their respective open source licenses. All custom code in this repository is licensed under the GNU General Public License v2.0 or later unless otherwise stated.
