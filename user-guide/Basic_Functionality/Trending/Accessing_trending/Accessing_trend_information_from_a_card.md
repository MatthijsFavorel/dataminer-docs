---
uid: Accessing_trend_information_from_a_card
---

# Accessing trend information from a card

On the data side of element cards, service cards and (for aggregation) view cards, trended parameters are indicated with a trending icon.

On a DMA using a Cassandra database, these trending icons can be displayed differently depending on the predicted trend:

| Trend icon  | Description |
|-------------|-------------|
| ![Upward trend icon](~/user-guide/images/Trend_icon_increase.png) | The predicted trend value is increasing. Hover over the icon to view the rate of increase. |
| ![Downward trend icon](~/user-guide/images/trend_icon_decrease.png) | The predicted trend value is decreasing. Hover over the icon to view the rate of decrease. |
| ![Stable trend icon](~/user-guide/images/trend_icon_stable.png)   | The predicted trend remains stable. |
| ![Trend icon without prediction](~/user-guide/images/trend_icon_unknown.png) | The trend behavior cannot be predicted, either because there is insufficient data, or because there is too much uncertainty in the direction of the trend during the past hour. On a DMA that does not use a Cassandra database, only this icon is displayed. |

> [!NOTE]
>
> - Behavior is calculated for single-value parameters and table parameters. For [partial tables](xref:Table_parameters#partial-tables), behavior is only calculated for the rows of the first page.
> - In the first hour after starting the SLAnalytics process, DataMiner has insufficient data to determine parameter behavior. This means that behavior arrows will only appear at least an hour after the SLAnalytics process was started.
> - The behavior of the arrows can be configured in the file *SLAnalytics.config*. See [SLAnalytics.config](xref:SLAnalytics_config#slanalyticsconfig).
> - You can enable or disable trend prediction icons via *System Center* > *System settings* > *analytics config*. That page also allows you to configure the minimum window duration these icons are based on and the update interval for the icons.

> [!TIP]
> See also: [Working with trend predictions](xref:Working_with_trend_predictions)

To access more detailed trend information for a parameter:

1. On the element card data page containing this parameter, double-click the parameter, or click the trend icon next to it. Alternatively, you can also right-click the parameter and select *Open*.

   For more information on how to use the displayed trend graph, see [Working with trend graphs](xref:Manipulating_trend_graphs).

1. To return to the card, click *Up to Data Display*.
