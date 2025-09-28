# VIM emulator for Godot 4 (version 4.4.1)

## What is this?
This is a Godot 4 plugin to emulates VIM-like editor behavior witin Godot editor itself (i.e. after installed and enabled, one could edit (kind of) like in VIM.

## How to install?
1. Clone or download the source of the repo, and copy the `addons` folder to the root of your project.
2. Go to `Project` -> `Project Settings` -> `Plugins` tab and check the check box of the plugin named `godot-vim`

## What's new?
- Changed version schema to godot_major_version.godot_minir_version.vim_plugin_version, so that it is easier to find the correct version of plugin for specific version of Godot editors
- Created a new branch `4.2` for Godot Editors 4.0 to 4.2
- Fixed selection issues due to CodeEdit.select() behavior change


## VIM features supprted
#### Mode

    - Normal mode
    - Insert mode
    - Visual mode
    - Visual line mode

#### Motions

    h, l, j, k, +, -
    ^, 0, $, |
    H, L, M,
    c-f, c-b, c-d, c-u,
    G, gg
    w, W, e, E, b, ge
    %, f, F, t, T, ;
    *, #, /, n, N
    aw, a(, a{, a[, a", a'
    iw, i(, i{, i[, i", i'
    {, }

#### Operator

    c, C,
    d, D, x, X,
    y, Y,
    u, U, ~

#### Actions

    p,
    u, c-r,
    c-o, c-i,
    za, zM, zR,
    q, @, .,
    >, <
    m, '

## FAQ
1. How to override default Godot shortcuts with `godot-vim`'s ones

    Note that all non-ascii character mappings that are already mapped in the default Godot editor have to be unmapped from the Editor settings (Editor >> Editor Settings >> Shorcuts) before being usable with `godot-vim`.
    
    This currently goes for:
    
    - `Ctrl+R`
    - `Ctrl+U`
    - `Ctrl+D`
    
    See the full list of non-ascii shortucts that may already be mapped by Godot and thus wouldn't work in `godot-vim` before releasing them in Godot settings: https://github.com/wenqiangwang/godot-vim/blob/main/addons/godot-vim/godot-vim.gd#L138

2. I found a problem, what should I do?

   - You could debug by yourself, changing the value of `DEBUGGING` variable to 1 to see logs
   - Or report the issue by providing a) the content of original text editing, b) the cursor position and c) key sequence that repros the issue
