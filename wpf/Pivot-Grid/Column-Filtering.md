---
layout: post
title: Column Filtering in Pivot Grid | PivotGrid | Syncfusion
description: Support to extract a subset of records that meet certain criteria for column fields in PivotGrid control.
platform: wpf
control: Pivot grid
documentation: ug
---

# Column Filtering

The pivot grid allows you to restrict the display of records by using a mechanism called filter. A filter enables you to extract a subset of records that meet certain criteria.

Property

* **AllowFilter**: Specifies whether the pivot grid control allows you to set a filter on the calculation column.

Method

* **ApplySavedValueFilter**: When RowPivotsOnly is true, this method filters the values in computation columns using the information passed in the dictionary.

It is possible to do filtering operations for pivot calculation during runtime as well as during initial load.

To do so, define the pivot grid control in RowPivotsOnly mode. Add the respective pivot calculations and set the `AllowFilter` property to "true".

Create the dictionary using the `Dictionary` class and add the pivot items that are to be filtered. Invoke the `ApplySavedValueFilter()` method for applying the filters.

Refer to the following code sample.

{% highlight C# %}

    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
            pivotGrid.Loaded += pivotGrid_Loaded;
        }

      void pivotGrid1_Loaded(object sender, RoutedEventArgs e)
      {
        pivotGrid.PivotCalculations.Add(new PivotComputationInfo(){FieldName ="Cost", FieldHeader = "Cost", AllowFilter = true });
        Dictionary<string,HashSet<string>>  dictionary = new Dictionary<string,HashSet<string>>();
        dictionary.Add("Cost", new HashSet<string>(){"701","230"});
        pivotGrid.InternalGrid.ApplySavedValueFilter(dictionary);
      }
    }

{% endhighlight %}

![To filter the records using column filter popup](Features-in-RowPivotsOnly-images/Filtering Enable in RowPivotsOnly.png)