Above-ground module dividing the model area into cells. In each cell, the tree with the largest crown height receives all available sunlight.  
The class requires input variables that define the boundaries of the model domain.

Attributes:
    type (string): "AsymmetricZOI"
    domain (nesting tag): coordinates to define the tree interaction grid
    x_1 (domain-nested int): x-coordinate of left border of grid    
    y_1 (domain-nested int): y-coordinate of bottom border of grid
    x_2 (domain-nested int): x-coordinate of right border of grid
    y_2 (domain-nested int): y-coordinate of top border of grid
    x_resolution (domain-nested int): x-resolution of grid
    y_resolution (domain-nested int): y-resolution of grid

The coordinates with the indices **1** define the numerically lower values, the indices **2** the numericall higher values of the boundaries. Spatial discretization of the model domain with the number of grid nodes in the respective spatial direction is defined by `x_resolution` and `y_resolution`.  

Example:

```xml
<belowground>
    <type> AsymmetricZOI  </type>
    <domain>
        <x_1>0</x_1>
        <y_1> 0 </y_1>
        <x_2> 185 </x_2>
        <y_2> 10 </y_2>
        <x_resolution> 720 </x_resolution>
        <y_resolution> 38 </y_resolution>
    </domain>
</belowground>
```