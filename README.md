# Syntax Definitions in Configuration Files

## 1.Equal Sign (=)

- **Definition**: Assigns a value to a variable or attribute.
- **Use Case**: Setting configuration values, defining resource attributes.
- **Example**: `location = "East US"`

## 2.Curly Braces ({})

- **Definition**: Defines blocks for resource configurations, variables, outputs, etc.
- **Use Case**: Organizing configuration into logical blocks.
- **Example**:

```hcl
resource "azurerm_virtual_machine" "pulse_vm" {
  name                  = "Pulse-vm"
  location              = "East US"
  resource_group_name   = "Pulse-rg01"
}

## 3.Double Quotes (" ")

- **Definition**: Defines string literals.
- **Use Case**: Specifying string values.
- **Example**: `name = "Pulse-vm"`
## 4.Square Brackets ([])

- **Definition**: Defines lists of values or indices for resource attributes.
- **Use Case**: Specifying lists of values, referencing resources in expressions.
- **Example**:

```hcl
subnet_ids = [
  azurerm_subnet.subnet1.id,
  azurerm_subnet.subnet2.id
]
