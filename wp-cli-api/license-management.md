# License Management

The theme provides a WP-CLI interface for managing theme license activation directly from the command line. This is useful for automated deployments, CI/CD pipelines, or managing licenses on staging/production environments without accessing the WordPress admin.

### Namespace

All commands are available under the `kalium license` namespace.

***

### Commands

#### Activate License

Activates the theme license using a license key.

```bash
wp kalium license activate <license-key>
```

**Arguments**

| Argument        | Description                               |
| --------------- | ----------------------------------------- |
| `<license-key>` | **Required.** The license key to activate |

**Example**

```bash
wp kalium license activate 'sk_abc123def456ghi789'
```

> **Important:** Always wrap the license key in single quotes to prevent shell escaping issues.

**Behavior**

* Validates that a license key is provided
* Checks if a license is already activated (will error if so)
* Activates the license via the Freemius SDK
* Returns success or error message

**Error Cases**

| Error                           | Description                                                         |
| ------------------------------- | ------------------------------------------------------------------- |
| `License key is required.`      | No license key was provided                                         |
| `License is already activated.` | A license is already active on this installation                    |
| `{API Error}`                   | License activation failed (invalid key, exceeded activations, etc.) |

***

#### Deactivate License

Deactivates the currently active theme license.

```bash
wp kalium license deactivate
```

**Example**

```bash
wp kalium license deactivate
```

**Behavior**

* Checks if there is an active license to deactivate
* Deactivates the license via the Freemius SDK
* Returns success or error message

**Error Cases**

| Error                                       | Description                    |
| ------------------------------------------- | ------------------------------ |
| `There is no active license to deactivate.` | No license is currently active |
| `{API Error}`                               | License deactivation failed    |

***

### Typical Workflow

#### New Installation

```bash
# Activate license on a fresh installation
wp kalium license activate 'sk_abc123def456ghi789'
```

#### Migration Between Environments

```bash
# Deactivate license on old server
wp kalium license deactivate

# Activate license on new server
wp kalium license activate 'sk_abc123def456ghi789'
```

#### CI/CD Pipeline

```bash
# Activate license during deployment (using environment variable)
wp kalium license activate "$KALIUM_LICENSE_KEY"
```

***

### Notes

* Always wrap the license key in single quotes (`'license-key'`) to prevent shell escaping issues
* Only one license can be active at a time per installation
* Deactivate your license before migrating to a new domain to free up the activation slot
* License activation requires an internet connection to communicate with the licensing server
* The license key is stored securely in the WordPress database
