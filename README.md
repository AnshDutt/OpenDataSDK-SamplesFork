[![JavaDoc](https://img.shields.io/badge/javadoc-reference-blue.svg)](https://htmlpreview.github.io/?https://github.com/dheerajrinku93/OpenDataSDKDocs/blob/main/javaDocs/index.html)
![Coverage Status](https://s3.amazonaws.com/assets.coveralls.io/badges/coveralls_85.svg)

# BankOfApiSDK-Java

The BankOfApiSDK-Java enables Java applications to integrate with the Natwest Bank Of API in an easy and efficient
manner.

# Why BankOfApiSDK-Java?

The BankOfApiSDK-Java enables the Java developers to:

- Offer a comprehensive framework over the Natwest APIs that enables developers to produce apps quickly and effectively.
- Eliminate the boiler-plate codes (such as connectivity, security, AuthN & AuthZ etc) while connecting to Natwest Bank
  Of APIs
- Leverage additional filters (such as get ATM By Location, PostCode, TownName etc.)
- Leverage in-memory caching for improved response time
- Refresh & clear cache whenever needed

# Quick links

| [Getting Started](README.md#Getting-Started) |  [Samples](https://github.com/dheerajrinku93/OpenDataSDK-Samples) | [Feedback](https://forms.office.com/Pages/ResponsePage.aspx?id=Wq6idgCfa0-V7V0z13xNYZ7nnvAosjxDh7243hA8A6lUOUZSTDA4OTYyQlZXTU00UzNTQ1JFNDkzUS4u) |
| --- | --- | --- |

### Code Setup

The SDK supports the following Java environments.

- **JDK version :** 8 or above (Tested JDK 8 against Oracle JVM)
- **IDE**
    - [IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=windows)
    - [Eclipse](https://www.eclipse.org/downloads/)
- **SDK Version :** 1.0.0

The Bank of API portal provides a change log for tracking changes in each version.

##### Accessibility of the SDK

You can include the SDK in your project by either of below-mentioned ways:

###### As an External Jar

- Download the SDK jar from repository directly <<_repo link_>>*
- Add as an external library in your project

###### Maven

- Find the latest version in the Maven central repository **
- Add the below code snippet as a maven dependency in the pom.xml file
    ```
    <dependency>
        <groupId>com.natwest.bankofapi</groupId>
        <artifactId>bankofapi-sdk-java</artifactId>
        <version>1.0.0</version>
    </dependency>
    ```

###### Gradle

- Find the latest version in the Maven central repository **
- Add the below code snippet as a gradle dependency in the build.gradle file
    ```
    implementation group: 'com.natwest.bankofapi', name: 'bankofapi-sdk-java', version: '1.0.0'
    ```

### Getting Started

This SDK provides a _plug and play_ facility for the TPP developers. The developer can perform below steps to access the
Natwest Bank Of APIs through the SDK:

1. Add opendatasdk.jar as an external library or add it as maven or gradle dependency in pom.xml or build.gradle file
   respectively.
2. Use below code to access Natwest Bank Of APIs through SDK:
    ```
    OpenDataService openDataService = new OpenDataService();
    ATMService atmService = openDataService.getAtmService();
    ```

### Code Example

- **For ATMs**
    - _Get All ATMs data_:

       ```
        OpenDataService openDataService = new OpenDataService();
        ATMService atmService = openDataService.getAtmService();
        List<ATM> allAtms = atmService.getAllData();
        ```
    - _Get All ATMs data based on Postcode filter_:

        ```
          OpenDataService openDataService = new OpenDataService();
          ATMService atmService = openDataService.getAtmService();
          List<ATM> allAtms = atmService.getATMsByPostCode("SW1A");
        ```
    - _Get All ATMs data based on Town Name filter_:

        ```
          OpenDataService openDataService = new OpenDataService();
          ATMService atmService = openDataService.getAtmService();
          List<ATM> allAtms = atmService.getATMsByTownName("London");
        ```

- **For Branches**

    - _Get All Branches data_:

       ```
        OpenDataService openDataService = new OpenDataService();
        ATMService atmService = openDataService.getAtmService();
        List<ATM> allAtms = atmService.getAllData();
        ```
    - _Get All Branches data based on Accessibility filter_:
       ```
       OpenDataService openDataService = new OpenDataService();
       BranchesService branchesService = openDataService.getBranchesService();
       List<Branches> allBranches = branchesService.getBranchesByAccessibility("InductionLoop");
      ```

    - _Get All Branches data based on Town Name filter_:

       ```
       OpenDataService openDataService = new OpenDataService();
       BranchesService branchesService = openDataService.getBranchesService();
       List<Branches> allBranches = branchesService.getBranchesByTownName("Aberaeron");
      ```

- **For Products & Service Metrics**
  Similarly the developer can access the Products & Service Metrics APIs using corresponding methods & filters from the
  SDK.

### Roadmap

Find below the latest updates and plans for BankOfApiSDK-Java:

| Date | Release | Main features |
|   --- |    ------     | ----- |
|   Dec 2022   | 1.0.0   | ATMs, Branches, Products and Service Metrics |
|   Feb 2023  | 1.1.0    | AISP |
|   May 2023  | 1.2.0    | PISP |
|   July 2023  | 1.3.0    | Upcoming & bank discretionary APIs |

### Contributing

- For any question, bug or feature request(s) please open an issue.
- To submit a contribution:
    - Goto BankOfApiSDK repo (https://github.com/bankofapi/openDataSDK)
    - Create your feature branch (git checkout -b feature/openDataSDKBar)
    - Read our contribution guidelines and Community Code of Conduct
    - Commit your changes (git commit -am 'Add some openDataSDKBar')
    - Push to the branch (git push origin feature/openDataSDKBar)
    - Create a new Pull Request
- For any further query or clarification please send an email to **bankofapisdk.support@natwest.com**.

___________________________________________________________________________________________________________
_Note_ :-
- *_The repo link will be made available once the code is checked-in on Github public repository_.
- **_The SDK Maven/Gradle dependency will be available on Maven central repository as an artifact once it is published_.  
 
