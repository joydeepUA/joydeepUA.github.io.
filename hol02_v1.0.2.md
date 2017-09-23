![Snap2](hol02_images/media/image1.png){width="2.1416666666666666in" height="0.9625in"}
=======================================================================================

![apex-round-128.pdf](hol02_images/media/image2.jpeg){width="1.9430555555555555in" height="1.9430555555555555in"}
=================================================================================================================

**Oracle Application Express: Developing Database Web Applications**
====================================================================

**Hands-On-Labs Guide**
=======================


*Unit 2: Using SQL Workshop*
============================

This exercise includes two hands-on-labs.

**HOL 2-1: Loading the Tables and Data**: In this lab, you use SQL Workshop to create the underlying database objects and data required for you to build the Demo Projects application.

**HOL 2-2: Creating a Lookup Table**: In this lab, you create a tabled named HARDWARE and load data in to the table. Then, you create a lookup table.


*HOL 2-1: Loading the Tables and Data*
=======================

It is essential to have at least the tables defined in order for the Create Application wizard to generate pages in your application. In this hands-on-lab, you create the required database objects, and populate the tables with sample data.

1.  Use SQL Workshop to upload a script that creates the tables for the Demo Projects application. Perform the following steps:

<!-- -->

a)  Click **SQL Workshop** and select **SQL Scripts**.\
    ![1a](hol02_images/media/image3.png){width="6.174305555555556in" height="2.3631944444444444in"}

b)  Click **Upload**.

c)  Click **Choose File**, navigate to the working directory where you extracted apex-course-labs.zip.\
    Locate the **Project\_Basic\_Tables.sql** file, and double-click the file or click the file and then click **Open**.

d)  Click **Upload**.\
    ![1d](hol02_images/media/image4.png){width="6.0472222222222225in" height="3.877083333333333in"}

e)  Review the uploaded script to see what tables will be created.\
    In the SQL Scripts list, click the **Edit** icon (pencil), to the left of the script you just uploaded.\
    ![1e](hol02_images/media/image5.png){width="6.136805555555555in" height="1.3069444444444445in"}

f)  Click the **Run** icon to the right of the script you uploaded.\
    ![1f](hol02_images/media/image6.png){width="5.896527777777778in" height="5.009722222222222in"}\
    Click **Run Now**.

g)  Click the **View Results** icon for the script you just ran.\
    ![1g](hol02_images/media/image7.png){width="5.920138888888889in" height="0.9861111111111112in"}\
    ![1h](hol02_images/media/image8.png){width="5.971527777777778in" height="4.457638888888889in"}

<!-- -->

2.  Currently the tables you created do not have any data. A script has been provided that creates an Oracle database package which can be run at any time to insert or reset the data in the tables. Use SQL Workshop to upload a script that you can use to populate table data. Perform the following steps:

<!-- -->

a)  Click **SQL Scripts**. Click **Upload**.

b)  Click **Choose File**, where you extracted apex-course-labs.zip.

c)  Locate the **Project\_Data.sql** file, and double-click the file or click the file and then click **Open**.

d)  Click **Upload**.\
    ![2a](hol02_images/media/image9.png){width="6.254861111111111in" height="3.8916666666666666in"}

e)  Click the **Run** icon to the right of the script you uploaded (top row).\
    ![2b](hol02_images/media/image10.png){width="6.263888888888889in" height="1.2597222222222222in"}\
    Click **Run Now**.

f)  Click the View Results icon for the script you just ran (top row).\
    ![2c](hol02_images/media/image11.png){width="6.273611111111111in" height="1.2027777777777777in"}\
    ![2d](hol02_images/media/image12.png){width="6.141666666666667in" height="2.8493055555555555in"}

<!-- -->

3.  In step 1, you uploaded a package called DEMO\_PROJECTS\_DATA\_PKG. However, this package has not yet been run so the tables you created still do not have any data. The SQL Commands facility, within SQL Workshop, allows a developer to run any valid SQL commands. You will run a SQL command to execute the data package and populate the tables. Use SQL Commands to execute n Oracle Database package. Perform the following steps:

<!-- -->

a)  Click the Up arrow, before SQL Scripts.\
    ![3a](hol02_images/media/image13.png){width="6.028472222222222in" height="2.042361111111111in"}

b)  Click **SQL Commands**.\
    ![3b](hol02_images/media/image14.png){width="6.089583333333334in" height="1.73125in"}

c)  Enter the following code:

  
      begin demo\_projects\_data\_pkg.load\_sample\_data;
      
      end;
  

a)  Click **Run**.\
    ![3c](hol02_images/media/image15.png){width="6.131944444444445in" height="2.3208333333333333in"}

> The Results show: Statement Processed.

4.  Use the Object Browser within SQL Workshop to review all of the database objects, such as the tables and packages you created, available in the underlying Oracle database schema which is associated with the Application Express workspace you logged into. Perform the following steps:

<!-- -->

a)  At the top of the page, select **SQL Workshop** and then select **Object Browser**.\
    ![3d](hol02_images/media/image16.png){width="5.5375in" height="2.5520833333333335in"}

b)  In Object Browser, select the **DEMO\_PROJ\_TEAM\_MEMBERS** table, and then click on the **Data** tab.\
    ![4a](hol02_images/media/image17.png){width="6.372916666666667in" height="4.004861111111111in"}\
    **Note**: There are a number of other tables listed, outside of those you created using the script file above. The APEX\$ tables are created by Application Express to store internal data specific to your workspace. Tables such as DEMO\_CUSTOMERS were created when the Sample Database Application was installed. The Sample Database Application is installed by default when an Application Express Workspace is created.

c)  To review the package you created, select Packages and select DEMO\_PROJECTS\_DATA\_PKG. Click **Body** to review the primary PL/SQL rather than the specification.\
    ![4b1](hol02_images/media/image18.png){width="1.7597222222222222in" height="2.75in"}

> **Note**: This package includes complex PL/SQL code to insert images and replicate users entering in records. It is not important that you understand the PL/SQL code in this package, as you will not normally have to populate data in this matter. Generally, you would create the tables with no data and then use the application you build to insert the records.\
> ![4b2](hol02_images/media/image19.png){width="6.311111111111111in" height="4.707638888888889in"}


*HOL 2-2: Creating a Lookup Table*
=======================

In this hands-on-lab, you use the Data Workshop utility to create a table and populate the table with data. Once this table is created, you also create a lookup table.

1.  Click **SQL Workshop &gt; Utilities &gt; Data Workshop**.\
    ![5a](hol02_images/media/image20.png){width="5.51875in" height="2.6791666666666667in"}

2.  Click **Data Load &gt;Spreadsheet Data**.\
    ![5b](hol02_images/media/image21.png){width="2.0659722222222223in" height="2.2263888888888888in"}

3.  The Load Data Wizard appears.\
    Under Load To, select **New Table**, and under Load From, select **Upload file**.\
    Click **Next**.\
    ![5c](hol02_images/media/image22.png){width="5.579861111111111in" height="3.8020833333333335in"}

4.  Click **Choose File**, open the working directory where you extracted **apex-course-labs.zip**. Locate the **hardware.csv** file, and double-click the file or click the file and then click **Open**.\
    Ensure that First row contains column names is selected, accept the remaining defaults, and click **Next**.\
    ![5d](hol02_images/media/image23.png){width="5.9006944444444445in" height="3.783333333333333in"}

5.  Enter **Hardware** for Table Name, verify the table properties, and click **Next**.\
    ![5e](hol02_images/media/image24.png){width="5.98125in" height="3.8069444444444445in"}

6.  Accept the defaults on the Load Data - Primary Key page, and click **Load Data**.\
    ![5f](hol02_images/media/image25.png){width="5.561111111111111in" height="3.589583333333333in"}

7.  The new table is now created and is populated with the data.

> Click **Object Browser**.\
> ![5g](hol02_images/media/image26.png){width="6.061111111111111in" height="2.3020833333333335in"}

8.  In the Object Selection pane, click **Hardware**.\
    The Detail pane now shows details about Hardware table. For the Hardware table, review the column names and data types.\
    Click **Data**.\
    Now you see a report of the data contained in the Hardware table.\
    ![5h](hol02_images/media/image27.png){width="6.23125in" height="2.5569444444444445in"}

9.  You want to create a lookup table now. Perform the following steps:

<!-- -->

a)  Click **Table**. Click **Create Lookup Table**.\
    ![6a](hol02_images/media/image28.png){width="6.127083333333333in" height="3.236111111111111in"}

b)  Select **DEPARTMENT** for Column. Click **Next**.\
    ![6b](hol02_images/media/image29.png){width="6.0375in" height="3.8069444444444445in"}

c)  Accept the defaults on this page and click **Next**.\
    ![6c](hol02_images/media/image30.png){width="6.089583333333334in" height="3.297222222222222in"}

d)  Click **Create Lookup Table**.\
    ![6d](hol02_images/media/image31.png){width="6.065972222222222in" height="3.329861111111111in"}

e)  Review the table definition of **DEPARTMENT\_LOOKUP** table.\
    ![6e](hol02_images/media/image32.png){width="6.113194444444445in" height="3.1319444444444446in"}

f)  In the Object Selection pane, click **HARDWARE**.\
    Review the table details. Notice that the DEPARTMENT column has been extracted from the HARDWARE table and is now available in the DEPARTMENT\_LOOKUP table.\
    \
    ![6f](hol02_images/media/image33.png){width="6.023611111111111in" height="3.292361111111111in"}

![Snap3.jpeg](hol02_images/media/image34.png){width="6.5in" height="2.5542027559055116in"}\
