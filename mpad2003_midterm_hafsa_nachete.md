**November 4th, 2024**<br>
**MPAD 2003 A Fall, Introductory Data Storytelling**<br>
**Hafsa Nachete**<br>
**Presented to Jean-Sébastien Marier**<br>


# Midterm Project: Exploratory Data Analysis (EDA)

## Foreword

I will examine a portion of the "2024 Service Requests" dataset from the city of Ottawa. My goal is to uncover a meaningful narrative / story that reflect the community's ingeactions with services. I look forward to sharing my process throughout this assignment.

## 1. Introduction

As mentioned in the foreword, I will be analyzing a dataset from the City of Ottawa that focuses on service requests made by residents in August 2024. These requests cover non-emergency issues such as road repairs, waste collection, and bylaw enforcment. The dataset provides detailed records of 311 service requests, including the type of service requested, the submission date, location, and status updates. The original dataset can be accessed on [Open Ottawa](https://open.ottawa.ca/documents/65fe42e2502d442b8a774fd3d954cac5/about), with a CSV version available on the [Github portal](https://raw.githubusercontent.com/jsmarier/course-datasets/refs/heads/main/ottawa-311-service-requests-august-2024.csv). 

This report consists of four main sections. First, getting data, I will explain how the dataset was imported into Google Sheets and provide initial observations about its structure and content. Second, in Understanding data, I will perform a VIMO analysis to evaluate the data's quality, followed by data cleaning and exploratory analysis to uncover patterns. Thrid, I will explore potential stories from the dataset. Finallly, in the conclusion, I will reflect on the challenges, insights, and key takeaways from ompleting the analysis. 

## 2. Getting Data

To obtain the necessary data, I began by importing the dataset into Google Sheets. The involved downloading the CSV file from the Github portal. In Google Sheets, I selected "file", then "Import", followed by "Upload" to add my CSV file. After the import, I adjusted the settings to set the delimiter to "Comma", ensuring the columns would displayed correctly. 

You can see a results of this process in the screenshot below and in the attached [Google Sheet](https://docs.google.com/spreadsheets/d/1BZ9UBwwG1Ge7Uvxf2ftSpjDnVnBD0zheKhyqrZ12peE/edit?usp=sharing) link: 

![GS1](GS1.png)<br>
*Figure 1: Screenshot of the import process in Google sheets* 

In general observations, the dataset includes 11 columns and 28,539 rows. The column headings provide information such as the status of the request, the type, a description, the opened and closed dates, the adress, latitude, lontitude, the ward, and the channel through which the request was made. At first glance, the data appears to be relatively clean, with no significant issues like missing headers or misplaced information in the wrong columns. 

In terms of specific observations, Column C represents the type of request made, categorized as nominal variables.The data shows 5 caegories:"Garbagde and Recycling", "Bylaw services", "Roads and Transportation", "Water and the Environment" and finally "Parking Control Enforcment". Garbadge and Recycling" seems to be the most in frequency levels, while "Parking Control Enforcment" has the lowest frequency of requests. 

For column D, which describes the service requests in more detail, the most frequent description is related to "Organics - SWC" (Source Waste Collection).

Regarding Column F (Opening Date) and Column G (Closing Date), a significant number of closing dates are marked as "\N," indicating missing data. However, among the completed requests, many were closed on August 28, 2024, while a high number of cases were opened on August 29, 2024, which is an interesting trend to note.

In Column G (Address of Request), the most common entry is "\N," indicating missing data for many records. However, the address "99 Cobourg St" appears 18 times, followed closely by "1000 Airport Parkway Priv" with 11 occurrences.

Looking at Column J (Ward), the highest number of service requests originated from Ward 12 (Rideau-Vanier) and Ward 14 (Somerset).

For Columns H and I (Latitude and Longitude), the majority of geolocated requests are associated with "Roads and Transportation" (4,214 occurrences), with a smaller number linked to "Recreation and Culture" (844 occurrences).

Lastly, in Column K (Channels), most requests were made through dispatch services (13,551 instances), followed by web submissions (12,717), and voice-ins (828). The least common channels were data-in (817) and walk-in requests (498).

### The Hypothesis
The question that comes to mind is wherther certain wards in Ottawa have a higher frequency of service requests than others. In praticular, does Ward 12 (Rideau-Vanier) consistently report more service requests compraed to other wards, and if so, what might be the reason for this?

## 3. Understanding Data

### 3.1. VIMO Analysis

I will focus on the three columns for my VIMO analysis: "Column J: Ward", "Column C: Type of requests" and "Column K: Channels".  For column J, We find a lot of values in this colum marked as "\N" which is missing data. Missing ward data could hinder the readers ability to determine the distribution of the service requests [(Statistics Canada, 2020)
](https://apastyle.apa.org/style-grammar-guidelines/citations). There also significantly more requests from Ward 12, which is an outlier because its exptremly large compared to other wards [(Statistics Canada, 2020)
](https://apastyle.apa.org/style-grammar-guidelines/citations). 

For column C, varifying the service requests is important and consistent. Upon looking at the colum stats, there should be no unique values present. The main titles should more or less repeat themselves consistantly. 

For column K, there's also an outlier, with high proportion of channels in dispatch. 


### 3.2. Cleaning Data

I implemented several cleaning methods on my data. First, I checked the cleanup suggestions in my sheets and identified an issue with whitespace in Column D. I made the necessary changes and trimmed all the extra whitespace as suggested.

Next, I froze Row C by navigating to the View menu, selecting the Freeze option, and choosing Column C.

Lastly, I used the CONCATENATE function in cell M1 to combine the contents of H10 and J10.



### 3.3. Exploratory Data Analysis (EDA)

Insert text here.

**This section should include a screen capture of your pivot table, like so:**

![](pivot-table-screen-capture.png)<br>
*Figure 2: This pivot table shows...*

**This section should also include a screen capture of your exploratory chart, like so:**

![](chart-screen-capture.png)<br>
*Figure 3: This exploratory chart shows...*

## 4. Potential Story

Insert text here.

## 5. Conclusion

Insert text here.

## 6. References

Include a list of your references here. Please follow [APA guidelines for references](https://apastyle.apa.org/style-grammar-guidelines/references). Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)

