# HomeAssistant.nvim

Simple plugin to provide some interaction with Home Assistant, currently supports:

1. Rendering templates

## Installation

Using [packer.nvim](https://github.com/wbthomason/packer.nvim), require [plenary.nvim](https://github.com/nvim-lua/plenary.nvim) for its curl wrapper.

```lua
  use({
    "muniter/homeassistant.nvim",
    requires = {
      "nvim-lua/plenary.nvim",
    },
  })
```

## Setup

Requires configuration before being able to use the defined command.

```lua
require("homeassistant").setup({ 
  url = "http://homeassistant.loc:8123",
  token = "my_long_lived_access_token"
})
```

## Usage

To render a template, run the command `HARender` and a floating window with the rendered template will pop up. **Make sure the setup function has been run before using the command**.
