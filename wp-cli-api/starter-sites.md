# Starter Sites

The theme provides a WP-CLI interface for managing starter sites (demo content) directly from the command line. This is useful for automated deployments, CI/CD pipelines, or quick site setup without using the WordPress admin interface.

### Namespace

All commands are available under the `kalium starter-site` namespace.

***

### Commands

#### List Starter Sites

Lists all available starter sites.

```bash
wp kalium starter-site list [--builder=<builder>] [--installed]
```

**Options**

| Option                | Description                                                                  |
| --------------------- | ---------------------------------------------------------------------------- |
| `--builder=<builder>` | Filter starter sites by builder type (e.g., `gutenberg`, `elementor`, `wpb`) |
| `--installed`         | Show only installed starter sites                                            |

**Example Output**

```
+---+------------+-----------------+------------------------------+
| # | id         | name            | builders                     |
+---+------------+-----------------+------------------------------+
| 1 | agency     | Agency          | wpb                          |
| 2 | * bookstore| Bookstore       | gutenberg, wpb               |
| 3 | hotel      | Hotel           | gutenberg, elementor         |
+---+------------+-----------------+------------------------------+
```

> **Note:** Starter sites marked with `*` are currently installed.

***

#### Install a Starter Site

Performs a complete installation of a starter site including plugins and content.

```bash
wp kalium starter-site install <id> [--builder=<builder>] [--regenerate-thumbnails]
```

**Arguments**

| Argument | Description                                     |
| -------- | ----------------------------------------------- |
| `<id>`   | **Required.** ID of the starter site to install |

**Options**

| Option                    | Description                                    |
| ------------------------- | ---------------------------------------------- |
| `--builder=<builder>`     | Specify the builder type to use                |
| `--regenerate-thumbnails` | Regenerate image thumbnails after installation |

**Example**

```bash
# Install the Bookstore starter site with Gutenberg (default)
wp kalium starter-site install bookstore

# Install with Elementor builder and thumbnail regeneration
wp kalium starter-site install bookstore --builder=elementor --regenerate-thumbnails
```

***

#### Install Plugins Only

Installs and activates only the required plugins for a starter site without importing content.

```bash
wp kalium starter-site install-plugins <id> [--builder=<builder>]
```

**Arguments**

| Argument | Description                          |
| -------- | ------------------------------------ |
| `<id>`   | **Required.** ID of the starter site |

**Options**

| Option                | Description              |
| --------------------- | ------------------------ |
| `--builder=<builder>` | Specify the builder type |

**Example**

```bash
wp kalium starter-site install-plugins architecture --builder=gutenberg
```

***

#### Import Content Only

Imports the content of a starter site (assumes required plugins are already installed).

```bash
wp kalium starter-site import-content <id> [--builder=<builder>]
```

**Arguments**

| Argument | Description                          |
| -------- | ------------------------------------ |
| `<id>`   | **Required.** ID of the starter site |

**Options**

| Option                | Description              |
| --------------------- | ------------------------ |
| `--builder=<builder>` | Specify the builder type |

**Example**

```bash
wp kalium starter-site import-content architecture --builder=elementor
```

***

#### Uninstall a Starter Site

Removes an installed starter site and its imported content.

```bash
wp kalium starter-site uninstall <id>
```

**Arguments**

| Argument | Description                                       |
| -------- | ------------------------------------------------- |
| `<id>`   | **Required.** ID of the starter site to uninstall |

**Example**

```bash
wp kalium starter-site uninstall agency
```

***

#### Regenerate Thumbnails

Regenerates image thumbnails for a specific starter site's imported media.

```bash
wp kalium starter-site regenerate-thumbnails <id> [--builder=<builder>]
```

**Arguments**

| Argument | Description                          |
| -------- | ------------------------------------ |
| `<id>`   | **Required.** ID of the starter site |

**Options**

| Option                | Description              |
| --------------------- | ------------------------ |
| `--builder=<builder>` | Specify the builder type |

**Example**

```bash
wp kalium starter-site regenerate-thumbnails architecture --builder=gutenberg
```

***

### Typical Workflow

#### Quick Installation

```bash
# 1. List available starter sites
wp kalium starter-site list

# 2. Install a starter site with Gutenberg (default)
wp kalium starter-site install bookstore --regenerate-thumbnails
```

#### Step-by-Step Installation

```bash
# 1. Install required plugins first
wp kalium starter-site install-plugins bookstore --builder=wpb

# 2. Import content
wp kalium starter-site import-content bookstore --builder=wpb

# 3. Regenerate thumbnails (optional)
wp kalium starter-site regenerate-thumbnails bookstore --builder=wpb
```

#### Cleanup

```bash
# Uninstall a starter site
wp kalium starter-site uninstall bookstore
```

***

### Error Handling

The CLI will exit with an error in the following cases:

* Starter site ID not provided
* Starter site not found
* Plugin download URL cannot be determined
* Import process encounters errors
* Attempting to uninstall a starter site that is not installed

***

### Notes

* Gutenberg is the default and recommended builder for most starter sites
* The `--builder` option is important when a starter site supports multiple page builders
* Available builders: `gutenberg` (default), `elementor`, `wpb`
* Running `install` will spawn separate processes for plugin installation and content import
* Thumbnail regeneration only affects images imported by the specific starter site
* The Portfolio post type is temporarily activated during plugin installation
