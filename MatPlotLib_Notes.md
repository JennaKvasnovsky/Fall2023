# MatPlotLib Notes

# Vocab
  1. Matplotlib: Python library for creating data visualizations, including plots, charts, and graphs.
  2. Figure: The entire window or page in which your plot or visualization is created.
  3. Axes: An individual plot within a figure. A figure can contain one or more axes.
  4. Plot: A graphical representation of data on the axes, such as a line plot, scatter plot, bar plot, etc.
  5. Axis: The X and Y (and sometimes Z) axes that define the coordinates for plotting data.
  6. Title: A descriptive label or title for the entire figure or for a specific plot.
  7. Labels: Text used to describe the axes, data points, or other elements in a plot.
  8. Legend: A key that explains the meaning of the different elements in a plot, particularly when multiple data series are shown.
  9. Tick: The marks on an axis that represent specific data values.
  10. Tick Labels: The labels associated with tick marks, indicating the data value they represent.
  11. Grid: Horizontal and vertical lines on the plot to aid in reading data values.
  12. Data Series: Sets of data points plotted together, often represented by lines, markers, or bars.
  13. Marker: A symbol used to denote specific data points on a plot, such as dots, crosses, or triangles.
  14. Line Style: The pattern used to draw lines connecting data points, such as solid lines, dashed lines, or dotted lines.
  15. Color Map (Colormap): A color scheme used to map data values to colors in visualizations, often used in heatmaps and contour plots.
  16. Subplot: A grid of smaller plots within a single figure, allowing multiple visualizations to be displayed together.
  17. Bar Chart: A type of plot that uses rectangular bars to represent data values.
  18. Scatter Plot: A plot that displays individual data points as markers, useful for visualizing the distribution of data.
  19. Line Plot: A plot that connects data points with lines, typically used to show trends or changes over time.
  20. Histogram: A plot that displays the distribution of data values in the form of bins or bars.
  21. Pie Chart: A circular chart divided into sectors to represent data proportions as slices of a whole.
  22. Box Plot (Box-and-Whisker Plot): A graphical representation of the distribution of a dataset, showing median, quartiles, and outliers.
  23. Error Bars: Lines or bars added to a plot to represent the uncertainty or variability in data points.
  24. Annotation: Additional text or shapes added to a plot to provide context or highlight specific data points.
  25. Axis Limits: The range of data values displayed on the axes, determined by xlim (X-axis) and ylim (Y-axis) settings.
  26. Figure Size: The dimensions of the figure window, specified as width and height.
  27. Subplot Arrangement: The layout of subplots within a figure, defined by rows and columns.
  28. Axis Scaling: The scale used for the axes, which can be linear, logarithmic, or other transformations.
  29. Matplotlib Styles: Predefined styles or themes that change the appearance of plots and figures.
  30. Backend: The rendering engine used by Matplotlib to display or save plots, such as Tkinter, Qt, or Agg.
  31. Interactive Mode: A mode that allows for real-time interaction with plots, useful in some GUI environments.

# Installation
pip install matplotlib

# Importing
import matplotlib.pyplot as plt

# Basic Line Plot
    # Sample data
    x = [1, 2, 3, 4, 5]
    y = [2, 4, 6, 8, 10]
  
    # Create a basic line plot
    plt.plot(x, y)

    # Add labels and a title
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.title('Simple Line Plot')

    # Show the plot
    plt.show()
    
# Scatter Plot
    # Sample data
    x = [1, 2, 3, 4, 5]
    y = [2, 4, 6, 8, 10]

    # Create a scatter plot
    plt.scatter(x, y)
  
    # Add labels and a title
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.title('Scatter Plot')

    # Show the plot
    plt.show()
    
# Bar Chart
    # Sample data
    categories = ['Category A', 'Category B', 'Category C']
    values = [10, 20, 15]

    # Create a bar chart
    plt.bar(categories, values)

    # Add labels and a title
    plt.xlabel('Categories')
    plt.ylabel('Values')
    plt.title('Bar Chart')

    # Show the plot
plt.show()

# Customizing Plots
    # Sample data
    x = [1, 2, 3, 4, 5]
    y = [2, 4, 6, 8, 10]

    # Create a line plot with customizations
    plt.plot(x, y, marker='o', linestyle='--', color='g', label='Data')
    
    # Add labels and a title
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.title('Customized Line Plot')

    # Add a legend
    plt.legend()

    # Show the plot
    plt.show()

# SubPlots
    # Sample data
    x = [1, 2, 3, 4, 5]
    y1 = [2, 4, 6, 8, 10]
    y2 = [1, 3, 5, 7, 9]

    # Create subplots
    plt.subplot(2, 1, 1)  # 2 rows, 1 column, first plot
    plt.plot(x, y1)
    plt.title('Subplot 1')

    plt.subplot(2, 1, 2)  # 2 rows, 1 column, second plot
    plt.plot(x, y2)
    plt.title('Subplot 2')

    plt.tight_layout()  # Adjust subplot spacing
    plt.show()
    
# Random GrayScale Image
    # Define the dimensions of the image
    width, height = 256, 256

    # Generate a random grayscale image
    random_image = np.random.randint(0, 256, (height, width), dtype=np.uint8)

    # Display the random grayscale image
    plt.imshow(random_image, cmap='gray')
    plt.axis('off')  # Turn off axis labels
    plt.show()

  # MatPlotLib Documentation
  https://matplotlib.org/stable/users/index.html
