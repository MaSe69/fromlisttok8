---
layout: page_public
title: From Lists to K8s
meta: Overview Meta
permalink: /plot_tables/
---

# Plot Tables

This part is all about visualizing data in tables.
Visualization is pretty much the first thing you usually do when receiving new data.

## Step 1: Plot a Column

Based on the csv-file created earlier, we want to plot that data. For simplicity, we start with only one column. 

**Coding**
>
    df.plot.bar(
        y=para["Y-Axis"],
        use_index=True,
        title=para["Title"],
        figsize=para["FigSize"],
        legend=myLegend,
        rot=0,
    )
    plt.show()

A new window pops up that contains the plot.

A simple bar plot based on the previous data in a table.

## Step 2: Save the Plot as an Image

Often, you want to re-use the image in your presentation like a Powerpoint slide. You can certainly make a screenshot of the pop-up window and embed that screenshot.

**Coding**
>
    plt.savefig(plotFullPath, dpi=300)


Another reason to save the picture is to stop having to close the pop-up window after each iteration. You can limit the duration of the existence of this pop-up window.
Here is some coding indicating how to either save the image to your file system suppressing the pop-up or to have the pop-up, but make the pop-up go away after a few seconds.

**Coding**
>
    ### When a filename for the plot is specified then save the plot
    try:
        _ = plt.show(block=False)
        if para["PlotFileName"]:
            plotFullPath = para["Stem"] + para["PlotPath"] + para["PlotFileName"]
            plt.savefig(plotFullPath, dpi=300)
    except:
        plt.show(block=False)
        time.sleep(para["Sleep"])

Literature suggests that the “png”-format is suitable for this kind of images. It suffices to specify the extenaion of your filename as “.png”.

## Step 3: More Data in the Plot

We need to specify the columns that shall be displayed. As we want to display all columns, just get the list of all columns.

**Coding**
>
header = list(df.columns.values)

Plot showing all columns previously created

## Step 4: Make it more Excel Like

As many people are used to graphs as shown in Excel, it is worth to tune the plots into this direction. The same data when used in Excel can easily be visualized as shown below.

Excel visualization of the sample data.

Pandas visualization using Matplotlib. Not quite but close enough to Excel.