---
layout: page_public
title: From Lists to K8s
meta: Overview Meta
permalink: /plot_tables/
---

# Plot Tables

This part is all about visualizing data in tables.
Visualization is pretty much the first thing you usually do when receiving new data.

Pandas works with [matplotlib](https://matplotlib.org/).
Matplotlib offers an abundance of graphics.
We start here with the simple bar chart.

## Step 1: Plot a Month For Each Account as Bar Chart

Based on the csv-file created earlier, we want to plot that data.
For simplicity, we start with only one column.

At the heart of the function call for the graphics is the import of the matplotlib library for pyplot and the call of the "show"-function.
Prior to showing the graph, some configurations have to be made. At least the values for the x-axis and the y-axis have to be specified.
Using dataframes, the index can be used as x-axis.

**Coding**
>
    import matplotlib.pyplot as plt
>
    df.plot.bar(
    use_index=True,
    y=para["Y-Axis"],
    legend=False, 
    rot=0,
    )
    plt.show()

A new window pops up that contains the plot.

**Image**
{% include images/image.html imagePath = "../images/img_blog/Plot_10.png" imageCaption = "A bar graph created from the accounting scenario."%}

Some recommendations:

- The default legend overlays with the bars. Hence, the legend is omitted here.
- The x-axis labels would not be readable without rotating them to position '0'
- Previous plots should be closed, which can be done using plt.close("all") before calling the new graph.

As default, a pop-up is displayed. This pop-up remains until it is closed manually. After having clicked away many, many such pop-ups while refining the graphical output,
you might want to limit the duration of this pop-up.

**Coding**
>
    plt.show(block=False)
    time.sleep(para["ShowGraphTime"])
    plt.close()

## Step 2: Save the Plot as an Image

We want to save the image as a file, without the need to create a screenshot manually.
After having defined the full path to which the plot shall be saved, the command "savefig" fulfills this task.

**Coding**
>
    plotFullPath = para["Stem"] + para["PlotPath"] + para["PlotFileName"]
    plt.savefig(plotFullPath, dpi=300)

Literature suggests that the “png”-format is suitable for this kind of images. It suffices to specify the extension of your filename as “.png”.

## Step 3: More Data in the Plot

We need to specify the columns that shall be displayed. As we want to display all columns, just get the list of all columns.

**Coding**
>
    header = list(df.columns.values)
    para["Y-Axis"] = header
>
    df.plot.bar(
        use_index=True,
        y=para["Y-Axis"],
        legend=False, 
        rot=0,
        color=greenGradient,
    )    

As many people are used to graphs as shown in Excel, it is worth to tune the plots into this direction. The same data when used in Excel can easily be visualized as shown below.
Plot showing all columns previously created.

**Image**
{% include images/image.html imagePath = "../images/img_blog/All Columns.png" imageCaption = "Beautified visualization of all sample data."%}

Pandas visualization using Matplotlib. Not quite, but close enough to an Excel visualization for now.
