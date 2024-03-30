# Syntax Definitions in Configuration Files

## 1. Equal Sign (=)

- **Definition**: Assigns a value to a variable or attribute.
- **Use Case**: Setting configuration values, defining resource attributes.
- **Example**: `location = "East US"`

## 2. Curly Braces ({})

- **Definition**: Defines blocks for resource configurations, variables, outputs, etc.
- **Use Case**: Organizing configuration into logical blocks.
- **Example**:
  ```
resource "azurerm_virtual_machine" "Pulse_vm" {
  name                  = "Pulse-vm"
  location              = "East US"
  resource_group_name   = "Pulse-rg01"
}
