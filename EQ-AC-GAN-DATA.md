```python
import numpy as np
import ipywidgets as widgets
from IPython.display import display

# Create a sample NumPy array
array = np.random.randint(0, 100, size=(5, 5))

def display_element(row, col):
    """
    Function to display the element at the specified row and column.
    """
    element = array[row, col]
    print(f"Element at row {row} and column {col}: {element}")

# Create interactive widgets
row_slider = widgets.IntSlider(value=0, min=0, max=array.shape[0]-1, description='Row:')
col_slider = widgets.IntSlider(value=0, min=0, max=array.shape[1]-1, description='Column:')
button = widgets.Button(description='Display Element')

# Define callback function for button click
def on_button_click(button):
    """
    Callback function to display the element when the button is clicked.
    """
    row = row_slider.value
    col = col_slider.value
    display_element(row, col)

button.on_click(on_button_click)

# Display the widgets
display(widgets.VBox([row_slider, col_slider, button]))
```


    VBox(children=(IntSlider(value=0, description='Row:', max=4), IntSlider(value=0, description='Column:', max=4)…


    Element at row 1 and column 0: 94
    Element at row 0 and column 0: 98



```python

```
