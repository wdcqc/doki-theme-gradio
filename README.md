## doki-theme-gradio

Use cute anime theme in your Gradio app!

Themes ported from https://github.com/doki-theme/doki-theme-jupyter

If you like this, please check out the [Doki Themes](https://doki-theme.unthrottled.io/)! Cute anime theme for every programming tool.

### Usage

1. Put the `templates` folder as well as `doki_settings.json`, `gradio_doki.py` in your Gradio project
2. Add the requirements in `requirements.txt`
3. Import the theme and add to your app with

- Interface API

```python
# Import the doki theme
from gradio_doki import theme, theme_settings

# Your demo interface
demo = gr.Interface(...)

# Add the theme to your interface
with demo:
    theme()
    theme_settings()

demo.launch()
```

- Blocks API

```python
# Import the doki theme
from gradio_doki import theme, theme_settings

# Add the theme to your interface
with gr.Blocks() as demo:
    # Your components in the demo
    text = gr.Textbox(lines=2, interactive=True)
    
    # ...

    # Add the theme to your interface
    theme()
    theme_settings()

demo.launch()
```

### Notes

1. `theme_settings()` adds a block of settings that lets the user choose the theme. If you think this block is redundant in your app, you can leave it out and force the users to use the theme of your personal favorite character.

2. For apps where the codebase is complex and not in a single folder, support a parameter `files_dir` to `theme_settings()` which should point to a `files` folder from your main path which can be accessed in front-end by `http://<server>/file=files/`

### Preview

TODO

Enjoy!