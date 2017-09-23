![Snap2](hol03_images/media/image1.png){width="2.1395833333333334in" height="0.9590277777777778in"}
===================================================================================================

![apex-round-128.pdf](hol03_images/media/image2.jpeg){width="1.9423611111111112in" height="1.9423611111111112in"}
=================================================================================================================

**Oracle Application Express: Developing Database Web Applications**
====================================================================

**Hands-On-Labs Guide**
=======================

*Unit 3: Creating a Database Application*
=========================================



This exercise includes three hands-on-labs.

**HOL 3-1 Creating a Database Application from Scratch**: In this hands-on-lab, you create a database Web application, Demo Projects. You will extend and improve this application later.

**HOL 3-2 Creating a Database Application from a Spreadsheet**: In this hands-on lab, you use a spreadsheet to create a database Web application, Budget App. You do not extend this application but will use in a later exercise.

**HOL 3-3 Creating a Websheet Application**: In this hands-on lab, you create a Websheet application for the Tech Sales Team daily reporting.


*HOL 3-1: Creating a Database Application from Scratch*
-----------------------------------------------------

In this lab, you create the initial application using the Create Application wizard to define multiple pages. Now that you have created the underlying tables, you are ready to create a desktop application. You will be adding reports and forms for the tables you created.

Generally, when developing an application you will not know all of the pages required at the beginning. Therefore, you will only generate a select number of pages initially, and then use the wizard to add additional pages as required. However, for this exercise you will generate most of the pages required for the application up front.

1.  Using the Create Application Wizard, create the Demo Projects application. Navigate to **App Builder** and then click **Create**.\
    ![1a](hol03_images/media/image3.png){width="5.909722222222222in" height="2.6638888888888888in"}

2.  Click **Desktop**.\
    ![1b](hol03_images/media/image4.png){width="5.844444444444444in" height="3.86875in"}

3.  For Name, enter **Demo Projects**. Accept the remaining defaults and click **Next**.\
    ![1c](hol03_images/media/image5.png){width="5.680555555555555in" height="3.5in"}

4.  Next, add Report and Form page types for the following tables:

    -   DEMO\_PROJ\_TEAM\_MEMBERS

    -   DEMO\_PROJECTS

    -   DEMO\_PROJ\_MILESTONES

    -   DEMO\_PROJ\_TASKS\
        \
        \
        Click **Add Page**.\
        ![1d](hol03_images/media/image6.png){width="5.877083333333333in" height="3.13125in"}

> For Page Type, select **Report and Form** and then enter/select the following:

-   Table Name: **DEMO\_PROJ\_TEAM\_MEMBERS**

-   Report Type: **Interactive Grid**

-   Form Page Mode: **Modal Dialog**

> Then, click **Add Page**.\
> ![1e](hol03_images/media/image7.png){width="5.942361111111111in" height="4.122916666666667in"}

5.  Add Report and Form page type for the DEMO\_PROJECTS table.

> Click **Add Page**. For Page Type, select **Report and Form** and then enter/select the following:

-   Table Name: **DEMO\_PROJECTS**

-   Report Type: **Interactive Grid**

-   Form Page Mode: **Modal Dialog**

> Then, click **Add Page**.

6.  Add Report and Form page type for the DEMO\_PROJ\_MILESTONES table.

> Click **Add Page**. For Page Type, select **Report and Form** and then enter/select the following:

-   Table Name: **DEMO\_PROJ\_MILESTONES**

-   Report Type: **Interactive Grid**

-   Form Page Mode: **Modal Dialog**

> Then, click **Add Page**.

7.  Add Report and Form page type for the DEMO\_PROJ\_TASKS table. The form page mode for DEMO\_TASKS should be generated as a normal page rather than a modal dialog.

> Click **Add Page**. For Page Type, select **Report and Form** and then enter/select the following:

-   Table Name: **DEMO\_PROJ\_TASKS**

-   Report Type: **Interactive Grid**

-   Form Page Mode: **Normal**

> Then, click **Add Page**.

8.  Verify that your screen matches the following image. You must create these pages in the order shown to ensure that they correspond with instructions later in this tutorial. If your screen does not look the same as the illustration below, use the X icon to the right of each page to delete problem pages and restart Step 2. Do not delete the Home page.\
    ![1f](hol03_images/media/image8.png){width="6.196527777777778in" height="6.0in"}

> Click **Create Application**. On the confirmation page, click **Create Application**.

9.  Click **Run Application**. Then, log in using your Workspace username and password.\
    ![1g](hol03_images/media/image9.png){width="6.147222222222222in" height="2.327777777777778in"}

10.  Your screen should look like the following:\
    ![1h](hol03_images/media/image10.png){width="6.204861111111111in" height="4.844444444444444in"}

*HOL 3-2: Creating a Database Application from a Spreadsheet*
-----------------------------------------------------------

In this lab, you use a spreadsheet to create a database application.

1.  Navigate to **App Builder** and click **Create**.\
    ![2a](hol03_images/media/image11.png){width="6.188194444444444in" height="2.7625in"}

2.  Select **From a Spreadsheet**.\
    ![2b](hol03_images/media/image12.png){width="6.122916666666667in" height="3.4180555555555556in"}

3.  Select **Upload file, comma separate (\*.csv) or tab delimited** for Import From, and click **Next**.\
    ![2c](hol03_images/media/image13.png){width="6.295138888888889in" height="3.303472222222222in"}

4.  Click **Choose File**. Navigate to your working directory and double-click **budget.csv**. Then, click **Next**.\
    ![2d](hol03_images/media/image14.png){width="6.204861111111111in" height="5.098611111111111in"}

5.  Enter **Project\_Budget** for Table Name. Verify the data types for each of the columns. Make sure that START\_DATE and END\_DATE columns have DATE Data Type. Click **Next**.\
    ![5e](hol03_images/media/image15.png){width="6.155555555555556in" height="6.090277777777778in"}

6.  For Application Options, accept the defaults (Report Type: Interactive Report) and click **Create Application**.\
    ![2f](hol03_images/media/image16.png){width="6.360416666666667in" height="3.4180555555555556in"}

7.  Click **Run Application**.\
    ![2g](hol03_images/media/image17.png){width="6.311805555555556in" height="5.459027777777778in"}

8.  Enter your Workspace Username and Password. Click **Log In**.\
    ![2h](hol03_images/media/image18.png){width="5.024305555555555in" height="4.7375in"}

9.  Review the Budget App application that you just created.\
    ![2i](hol03_images/media/image19.png){width="6.229166666666667in" height="3.6805555555555554in"}


*HOL 3-3: Creating a Websheet Application*
----------------------------------------

Tech Sales Team management want to track the daily status of the sales executives. You help them create a Websheet application. Once created, managers add pages for daily status and executives simply enter their daily status online by logging in to the Websheet application.

1.  Navigate to **App Builder** and click **Create**.\
    ![3a](hol03_images/media/image20.png){width="6.229166666666667in" height="2.4347222222222222in"}

2.  Click **Websheet**.\
    ![3b](hol03_images/media/image21.png){width="6.303472222222222in" height="2.9180555555555556in"}

3.  Enter **Team Status** for Name, deselect the **Include Getting Started Guide** checkbox and click **Create Websheet**.\
    ![3c](hol03_images/media/image22.png){width="6.2868055555555555in" height="3.1805555555555554in"}

4.  Click **Run Websheet**.\
    ![3d](hol03_images/media/image23.png){width="6.3277777777777775in" height="3.4180555555555556in"}

5.  Enter user Workspace Username and password. Click **Sign In**.\
    ![3e](hol03_images/media/image24.png){width="4.614583333333333in" height="4.491666666666666in"}

6.  You want to rename the Home Page. Click **Edit** and select **Edit Page**.\
    ![3f](hol03_images/media/image25.png){width="6.2131944444444445in" height="4.13125in"}

7.  Enter **Tech Sales Team Daily Report** for Name and click **Apply Changes**.\
    ![3g](hol03_images/media/image26.png){width="6.5in" height="3.795138888888889in"}

8.  You want to add a new section on the page. Under **Control Panel**, click **New Section**.\
    ![3h](hol03_images/media/image27.png){width="2.254166666666667in" height="2.9180555555555556in"}

9.  You want to add a text section so that you can enter some instructions. Select **Text** and click **Next**.\
    ![3i](hol03_images/media/image28.png){width="6.155555555555556in" height="2.795138888888889in"}

10. Select **Create single text section** for Method, enter **Daily Report** for Title. Under Content, click the **Expand Toolbar** button to expand the toolbar. Enter text and click **Create Section**.\
    ![3j](hol03_images/media/image29.png){width="6.147222222222222in" height="4.885416666666667in"}

11. You want to add a navigation section now. Under Control Panel, click **New Section**.\
    ![3k](hol03_images/media/image30.png){width="2.254166666666667in" height="2.877083333333333in"}

12. Select **Navigation** and click **Next**.\
    ![3l](hol03_images/media/image31.png){width="6.229166666666667in" height="2.672222222222222in"}

13. You want to include page navigation to enable navigation across daily status report pages. Select **Page Navigation** for Navigation Type and click **Next**.\
    ![3m](hol03_images/media/image32.png){width="6.2868055555555555in" height="2.0166666666666666in"}

14. Enter text for Title and click **Create Section**.\
    ![3n](hol03_images/media/image33.png){width="6.2868055555555555in" height="3.5166666666666666in"}

15. Now you see the navigation has been created. You can create status report for each day as a page.\
    ![3o](hol03_images/media/image34.png){width="6.5in" height="2.8604166666666666in"}For example, as you add daily status report pages, your home page will look like:\
    ![3s](hol03_images/media/image35.png){width="6.180555555555555in" height="4.745833333333334in"}

16. You can view your Websheet in Presentation mode. Click the Presentation button to the top right of the Websheet.\
    ![3t1](hol03_images/media/image36.png){width="6.221527777777778in" height="3.057638888888889in"}

17. You are now on the home page. To navigate to the next section, click the **&lt;** button.\
    ![3t2](hol03_images/media/image37.png){width="6.2375in" height="1.3118055555555554in"}

18. To return to the normal mode, click **X**.\
    ![3t3](hol03_images/media/image38.png){width="6.245833333333334in" height="1.7048611111111112in"}

> You can also expand this application further by adding different sections, data grids. To learn more about Websheets, navigate to **Packaged Apps &gt; All** and install **Sample Websheet AnyCo IT Department**.\
> To perform the next hands-on-lab, you need to switch to the App Builder window.
>
![Snap3.jpeg](hol03_images/media/image39.gif){width="6.7131944444444445in" height="2.6395833333333334in"}
-------------------------