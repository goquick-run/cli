# 🧩 `quick addc` Command

The `addc` command is used to add a new controller to an existing Quick project.

## Usage

```bash
quick addc [controller-name] [flags]
```

## Flags

- `-h, --help`: Help for addc

## Examples

### Add a user controller

```bash
quick addc user
```

### Add a product controller

```bash
quick addc product
```

## What it Does

When you run the `addc` command, Quick CLI will:

1. Check if you're in a valid Quick project
2. Create a new controller file in the appropriate directory
3. Add necessary imports and boilerplate code
4. Register the controller routes (if applicable)

## Controller Structure

A typical controller generated by the `addc` command looks like this:

```go
package controllers

import (
	"net/http"
)

// UserController handles user-related requests
type UserController struct {
}

// NewUserController creates a new UserController
func NewUserController() *UserController {
	return &UserController{}
}

// GetAll handles GET requests to retrieve all users
func (c *UserController) GetAll(w http.ResponseWriter, r *http.Request) {
	// Implementation goes here
}

// GetByID handles GET requests to retrieve a user by ID
func (c *UserController) GetByID(w http.ResponseWriter, r *http.Request) {
	// Implementation goes here
}

// Create handles POST requests to create a new user
func (c *UserController) Create(w http.ResponseWriter, r *http.Request) {
	// Implementation goes here
}

// Update handles PUT requests to update a user
func (c *UserController) Update(w http.ResponseWriter, r *http.Request) {
	// Implementation goes here
}

// Delete handles DELETE requests to delete a user
func (c *UserController) Delete(w http.ResponseWriter, r *http.Request) {
	// Implementation goes here
}
```

## Next Steps

After adding a controller, you should:

1. Implement the controller methods
2. Add any necessary models
3. Register the controller routes (if not done automatically)
4. Test your endpoints

For more information, see the [Quick CLI Documentation](../README.md).
