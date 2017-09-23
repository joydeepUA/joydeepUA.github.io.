![Snap2](hol04_images/media/image1.png){width="2.1395833333333334in" height="0.9590277777777778in"}
===================================================================================================

![apex-round-128.pdf](hol04_images/media/image2.jpeg){width="1.9423611111111112in" height="1.9423611111111112in"}
=================================================================================================================

**Oracle Application Express: Developing Database Web Applications**
====================================================================

**Hands-On-Labs Guide**
=======================

*Unit 4: Managing Pages in Page Designer*
=========================================

In this lab, you create a dashboard by adding a new component to the Home page of the Demo Projects application. You open the home page in page designer, navigate through and review the page designer panes, add a chart region and edit the chart attributes.

1.  In the lab **HOL 3-1**, you finished by running the application. Given that you ran the application from the Application Builder, there is a Developer Toolbar at the bottom of the screen. This toolbar allows developers to quickly navigate between runtime and various sections within the Application Builder.\
    Navigate to the **Home** page in the runtime application.

In the Developer Toolbar, click **Edit Page 1**.

> **Note**: If you are not on the Home page then the Developer Toolbar will show the current page number, and clicking on Edit Page xx will navigate to that page, instead of Page 1.\
> ![1a](hol04_images/media/image3.png){width="6.5in" height="4.7625in"}

2.  The Page Designer is displayed for Page 1. There are three main panes within Page Designer: Left Pane, Central Pane, and Right Pane.\
    You can change the size of each pane by selecting the dividers and sliding them left or right. Change the size of **Grid Layout** and **Gallery** by sliding the divider between them up and down.\
    ![1b](hol04_images/media/image4.png){width="6.352777777777778in" height="4.229166666666667in"}

3.  In the Page Designer, you can invoke help on any attribute by clicking Help icon (shown as a question mark) on the toolbar. Select a component and then select an attribute in the Property Editor to display help on that attribute.\
    ![1c](hol04_images/media/image5.png){width="6.336111111111111in" height="2.245833333333333in"}

4.  Add a bar chart using drag and drop. The chart shows projects with the number of tasks.

<!-- -->

a)  Click **Layout**.\
    ![1d1](hol04_images/media/image6.png){width="4.614583333333333in" height="1.2048611111111112in"}

b)  In the Gallery (directly below the Grid Layout), click **Regions**, and locate **Chart**.\
    ![1d2](hol04_images/media/image7.png){width="5.950694444444444in" height="6.180555555555555in"}

c)  Click and hold **Chart** and drag it to the **Content Body** region. It should appear as a darkened tile before you drop it into place.\
    ![1d3](hol04_images/media/image8.png){width="6.057638888888889in" height="5.081944444444445in"}

> **Note**: When you drag the region up, and hover over the small yellow section, below Content Body, the yellow section will expand. A darker yellow section, with a black box around it, will indicate where the region will be placed.

d)  Now you modify the properties for a region, such as the Title and Template Options. When you first create a region, it is created with default properties, such as a Title of **New**.

> Use the Property Editor to edit attributes for the currently selected component.
>
> In the **Property Editor**, under Identification, for Title - enter **Project Tasks**.
>
> **Note**: The region name in the Rendering tree (left pane) and the Grid Layout (central pane) are updated to reflect the new title, as soon as you navigate out of the Title attribute in the Property Editor.\
> ![1de](hol04_images/media/image9.png){width="6.5in" height="2.3361111111111112in"}

e)  In the Property Editor, under **Appearance**, locate **Template Options** and click **Use Template Defaults, Scroll - Default**.\
    ![1f](hol04_images/media/image10.png){width="3.4756944444444446in" height="5.475694444444445in"}

f)  For Body Height select **480px**.

> Click **OK**.\
> ![1g](hol04_images/media/image11.png){width="5.532638888888889in" height="5.639583333333333in"}

g)  For certain region types, such as Charts, there are also Attribute properties. The region properties determine how the region is displayed, whereas, the Attributes for a region (where available) are used to define the characteristics of the region, and how the contents of the region are displayed.

> Locate the Rendering tree. Under the **Project Tasks** region, click **Attributes**.\
> ![1e](hol04_images/media/image12.png){width="3.057638888888889in" height="5.508333333333334in"}

h)  In the Property Editor:

-   Chart: Type - select **Bar**

-   Appearance: Orientation - select **Horizontal**

-   Appearance: Stack - select **Yes**

<!-- -->

-   Layout: Height - enter **480\
    **![1i](hol04_images/media/image13.png){width="4.614583333333333in" height="5.139583333333333in"}

i)  Under Rendering &gt; Project Tasks region, navigate to **Axes** and select **y**.\
    In the property editor, enter **Tasks** for Title.

> ![1j](hol04_images/media/image14.png){width="6.13125in"
  height="2.3604166666666666in"}
</br>

j)  The DEMO\_PROJ\_TASKS table includes a column called IS\_COMPLETE\_YN. This column is populated by users to indicate that a task is complete. Next, enter chart series details for completed and incomplete tasks within a project.\
    In the Rendering tree, nested under the Project Tasks region, click Series **X New**.\
    ![1k](hol04_images/media/image15.png){width="2.827777777777778in" height="6.311805555555556in"}

k)  In the property editor, under Identification &gt; Name, enter **Tasks**.

l)  In the property editor, under Source, click the Code Editor icon.\
    ![1m](hol04_images/media/image16.png){width="4.418055555555555in" height="3.696527777777778in"}

m)  For SQL Query, copy and paste the following code and then click **OK**.

  
      select p.id
      
      , p.name as label
      
      , (select count('x') from demo\_proj\_tasks t
      
      where p.id = t.project\_id
      
      and nvl(t.is\_complete\_yn,'N') = 'Y'
      
      ) value
      
      , 'Completed Tasks' series
      
      , p.created
      
      from demo\_projects p
      
      UNION ALL
      
      select p.id
      
      , p.name as label
      
      , (select count('x') from demo\_proj\_tasks t
      
      where p.id = t.project\_id
      
      and nvl(t.is\_complete\_yn,'N') = 'N'
      
      ) value
      
      , 'Incomplete Tasks' series
      
      , p.created
      
      from demo\_projects p
      
      order by 5
  

> ![Snap1](hol04_images/media/image17.png){width="6.245833333333334in" height="3.7784722222222222in"}

n)  Under Column Mapping, select:

-   Series Name: **SERIES**

-   Label: **LABEL**

-   Value: **VALUE**

> Click **Save**. Then, click **Save and Run Page**.\
> ![Snap2](hol04_images/media/image18.png){width="5.081944444444445in" height="6.254166666666666in"}

o)  You might have to log in using Workspace username and password. The Demo Projects application home page now looks like:\
    ![1](hol04_images/media/image19.png){width="6.024305555555555in" height="3.0493055555555557in"}

![Snap3.jpeg](hol04_images/media/image20.gif){width="7.155555555555556in" height="2.8118055555555554in"}
---------
