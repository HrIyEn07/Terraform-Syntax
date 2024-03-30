Equal Sign (=):

Definition: Assigns a value to a variable or attribute.
Use Case: Setting configuration values, defining resource attributes.
Example: location = "East US"
Curly Braces ({}):

Definition: Defines blocks for resource configurations, variables, outputs, etc.
Use Case: Organizing configuration into logical blocks.
Example:
hcl
Copy code
resource "azurerm_virtual_machine" "example" {
  name                  = "example-vm"
  location              = "East US"
  resource_group_name   = "example-resources"
}
Double Quotes (""):

Definition: Defines string literals.
Use Case: Specifying string values.
Example: name = "example-vm"
Square Brackets ([]):

Definition: Defines lists of values or indices for resource attributes.
Use Case: Specifying lists of values, referencing resources in expressions.
Example:
hcl
Copy code
subnet_ids = [
  azurerm_subnet.subnet1.id,
  azurerm_subnet.subnet2.id
]
Forward Slash (/):

Definition: Used in resource names and URLs.
Use Case: Defining resource names, constructing URLs.
Example: name = "example-vnet"
Period (.):

Definition: Accesses attributes or sub-resources.
Use Case: Accessing properties of resources or variables.
Example: location = azurerm_resource_group.example.location
Plus Sign (+):

Definition: Used in expressions for addition.
Use Case: Performing arithmetic operations.
Example: size = var.base_count + var.additional_count
Minus Sign (-):

Definition: Used in expressions for subtraction or negation.
Use Case: Subtracting values, negating expressions.
Example: count = var.enable_feature ? 1 : 0
Asterisk (*):

Definition: Used in expressions for multiplication.
Use Case: Performing multiplication operations.
Example: size = var.count * 10
Colon (:):

Definition: Separates keys and values in maps or block configurations.
Use Case: Defining key-value pairs, specifying block attributes.
Example:
hcl
Copy code
tags = {
  environment : "production"
  app         : "web"
}
Question Mark (?):

Definition: Used in conditional expressions.
Use Case: Implementing conditional logic.
Example: var.enable_feature ? "enabled" : "disabled"
Exclamation Mark (!):

Definition: Used for negation in some expressions.
Use Case: Negating expressions, applying logical NOT.
Example: count = var.enable_feature ? 1 : 0
Semicolon (;):

Definition: Used to separate statements or multiple resource configurations.
Use Case: Separating multiple statements or configurations.
Example: depends_on = [azurerm_resource_group.example]
Underscore (_):

Definition: Typically used in variable names or resource identifiers.
Use Case: Naming variables, resources, or identifiers.
Example: name = "example_${var.environment}"
Hash (#):

Definition: Used for comments in Terraform code.
Use Case: Adding comments for documentation or clarity.
Example: # This is a comment
At Sign (@):

Definition: Used in provider-specific configurations.
Use Case: Specifying provider-specific settings or configurations.
Example: provider "azurerm" { features {} }
Percent Sign (%):

Definition: Used in expressions for modulus.
Use Case: Calculating the remainder of a division operation.
Example: count = length(azurerm_subnet.example) % 2
Backslash ():

Definition: Typically used as an escape character in string literals.
Use Case: Escaping special characters in strings.
Example: file_path = "C:\\Users\\username\\file.txt"
Vertical Bar (|):

Definition: Used in some expressions and configurations.
Use Case: Specifying logical OR in expressions.
Example: value = var.enable_feature || false
Ampersand (&):

Definition: Used in some expressions and configurations.
Use Case: Specifying logical AND in expressions.
Example: value = var.enable_feature && true
Left Parenthesis (():

Definition: Begins a group in an expression or function call.
Use Case: Grouping expressions to control order of operations.
Example: count = length(azurerm_subnet.example)
Right Parenthesis ()):

Definition: Ends a group in an expression or function call.
Use Case: Ending a grouped expression.
Example: count = (length(azurerm_subnet.example) + 1)
Left Square Bracket ([):

Definition: Begins an index or defines a list.
Use Case: Specifying indices or defining lists.
Example: ids = [azurerm_virtual_machine.example.id]
Right Square Bracket (]):

Definition: Ends an index or defines a list.
Use Case: Ending an index or list definition.
Example: ids = [azurerm_virtual_machine.example.id]
Left Curly Brace ({):

Definition: Begins a block in a map or configuration.
Use Case: Defining blocks in configurations.
Example: tags = { environment = "production" }
Right Curly Brace (}):

Definition: Ends a block in a map or configuration.
Use Case: Ending a block in configurations.
Example: tags = { environment = "production" }
Single Quote ('):

Definition: Defines string literals, similar to double quotes.
Use Case: Specifying string values.
Example: name = 'example-vm'
Greater Than Sign (>):

Definition: Used in some expressions for comparison.
Use Case: Performing comparison operations.
Example: result = var.value > 10
Less Than Sign (<):

Definition: Used in some expressions for comparison.
Use Case: Performing comparison operations.
Example: result = var.value < 10
Double Greater Than (>>):

Definition: Used in some expressions for shifting bits to the right.
Use Case: Performing bit-shifting operations.
Example: shifted_value = var.value >> 2
Double Less Than (<<):

Definition: Used in some expressions for shifting bits to the left.
Use Case: Performing bit-shifting operations.
Example: shifted_value = var.value << 2
Vertical Ellipsis (...):

Definition: Represents an ellipsis or omission of content.
Use Case: Indicating continuation or omission in code examples.
Example: ...
Tilde (~):

Definition: Used in some expressions for bitwise negation.
Use Case: Performing bitwise negation operations.
Example: result = ~var.value
Caret (^):

Definition: Used in some expressions for bitwise XOR.
Use Case: Performing bitwise XOR operations.
Example: result = var.value ^ 0xFF
Pipe (|):

Definition: Used in some expressions for bitwise OR.
Use Case: Performing bitwise OR operations.
Example: result = var.value | 0xFF
Ampersat (@):

Definition: Represents an "at" symbol, used in some configurations.
Use Case: Specifying email addresses, usernames, or identifiers.
Example: email = "user@example.com"
Dollar Sign ($):

Definition: Represents a dollar sign, used in some configurations or expressions.
Use Case: Specifying currency values, variable names.
Example: price = $100
Plus Equal (+=):

Definition: Used in expressions for addition assignment.
Use Case: Adding a value to an existing variable.
Example: total += var.additional_cost
Minus Equal (-=):

Definition: Used in expressions for subtraction assignment.
Use Case: Subtracting a value from an existing variable.
Example: total -= var.discount
Asterisk Equal (*=):

Definition: Used in expressions for multiplication assignment.
Use Case: Multiplying an existing variable by a value.
Example: total *= var.quantity
Slash Equal (/=):

Definition: Used in expressions for division assignment.
Use Case: Dividing an existing variable by a value.
Example: total /= var.units
Percent Equal (%=):

Definition: Used in expressions for modulus assignment.
Use Case: Taking the modulus of an existing variable.
Example: remainder %= var.divisor
Ampersand Equal (&=):

Definition: Used in expressions for bitwise AND assignment.
Use Case: Performing bitwise AND on an existing variable.
Example: flags &= var.mask
Pipe Equal (|=):

Definition: Used in expressions for bitwise OR assignment.
Use Case: Performing bitwise OR on an existing variable.
Example: flags |= var.value
Caret Equal (^=):

Definition: Used in expressions for bitwise XOR assignment.
Use Case: Performing bitwise XOR on an existing variable.
Example: flags ^= var.key
Greater Than Equal (>=):

Definition: Used in expressions for greater than or equal comparison.
Use Case: Comparing values to determine if one is greater than or equal to another.
Example: result = var.value >= 10
Less Than Equal (<=):

Definition: Used in expressions for less than or equal comparison.
Use Case: Comparing values to determine if one is less than or equal to another.
Example: result = var.value <= 10
Double Ampersand (&&):

Definition: Used in expressions for logical AND.
Use Case: Combining conditions to evaluate logical AND.
Example: enabled = var.flag1 && var.flag2
Double Pipe (||):

Definition: Used in expressions for logical OR.
Use Case: Combining conditions to evaluate logical OR.
Example: enabled = var.flag1 || var.flag2
Double Colon (::):

Definition: Represents a double colon symbol, used in some configurations or expressions.
Use Case: Specifying namespace or scope in some contexts.
Example: ::1
