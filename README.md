# hound.nvim

A plugin that can query and display [hound](https://github.com/hound-search/hound) code search results with highlighting. This is a port of [jfo/hound.vim](https://github.com/jfo/hound.vim) in Lua.

## Install

### [packer](https://github.com/wbthomason/packer.nvim)

```lua
-- Lua
use {
  "davegallant/hound.nvim",
  requires = "nvim-lua/plenary.nvim",
  config = function()
    require("hound").setup {
      -- your config or leave blank for defaults
    }
  end
}
```

## ⚙️ Configuration

```lua
{
  hound_base_url = "http://localhost", -- base url for the hound api
  hound_port = 6080, -- the port hound is running on
  hound_url_pattern = "https://github.com/{repo}/blob/{revision}/{path}", -- the format of the url displayed for file matches
  display_file_match_urls = false, -- whether or not urls should be displayed alongside file matches
  search_results_buffer = "newtab", -- how to open the search results (vsplit, split, newtab)
}

```

## Usage

The `:Hound` command that takes a query (string) and displays the search results in a new buffer.
