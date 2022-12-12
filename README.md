[![JavaDoc](https://img.shields.io/badge/javadoc-reference-blue.svg)](https://htmlpreview.github.io/?https://github.com/dheerajrinku93/OpenDataSDKDocs/blob/main/javaDocs/index.html)
![Coverage Status](https://s3.amazonaws.com/assets.coveralls.io/badges/coveralls_85.svg)

# BankOfApiSDK
The Bank Of Api SDK is an Open Source project that provides Software Development Kit (SDK) to build project over NatWest Bank Of API.

- It aims to provide a complete framework over the APIs provided by NatWest which allows developers to create applications efficiently and quickly.
- It provides ready to use features for building an application.
- It is used to shorten the code length and provide the easiest way to develop applications, and it increases productivity and reduces the development time.
- It allows developers to build more optimize, readable applications.

# Quick links

| [Getting Started](README.md#Getting-Started) | [Home](https://github.com/dheerajrinku93/OpenDataSDKDocs/wiki) | [Samples](https://github.com/dheerajrinku93/OpenDataSDK-Samples) | [Feedback](https://forms.office.com/Pages/ResponsePage.aspx?id=Wq6idgCfa0-V7V0z13xNYZ7nnvAosjxDh7243hA8A6lUOUZSTDA4OTYyQlZXTU00UzNTQ1JFNDkzUS4u) |
| --- | --- | --- | --- |

# Why BankOfApiSDK?
Suppose we are building an application, where for some of the usecases we need to consume APIs from Natwest Bank Of API. But as a developer I want to get rid of writing all boiler-plate codes (such as connectivity, AuthN, AuthZ, data-transformation etc.) and focus on developing the business logic. BankOfApiSDK is here to help you on this:

- BankOfApiSDK provides simple interface which makes it easy to create applications over Natwest Bank of APIs.
- it helps in building the app components faster and easier way and thus  increases productivity and reduces the development time
- It makes life easier for developers to reduce boilerPlate code over Natwest Bank of API.
- It uses cache to store data for escape call Natwest Bank of API.
- It provides tracability to trace call on server.
- It provides wrapper for ATMs and Banches over Natwest Bank of API.

# Features
- Support for multiple languages (e.g. Java, .Net, NodeJs, Python etc.)
- Easy to use interface to interact with Open Banking APIs
- Eliminates boiler-plate code (such as connectivity, AuthN, AuthZ, data-transformation etc.)
- Provides Additional Filters to get specific set of data
- In-memory cache (avoids unnecessary repeted calls and reduces response time)

# Languages & Frameworks
| SDK   | Supported Platform & Framework |
|   --- |    ------     |
|   BankOfApiSDK-Java  | Windows, macOS, Linux  |
|   BankOfApiSDK-Net   |     |
|   BankOfApiSDK-Node  |     |
|   BankOfApiSDK-Python|     |

# BankOfApiSDK-Java
The BankOfApiSDK enables Java applications to integrate with the Natwest Bank Of API in a easy and efficient manner.
<!--
### Methods
- **Generic Methods**
    ```
    - getAllData()
    ```
- **ATM Interface**
    ```
    - getATMsByFilter() 
    - getATMsByLocation()
    - getATMsByAccessibility()
    - getATMsByPostCode()
    - getATMsByTownName()
    ```
- **Branch Interface**
    ```
    - getBranchesByFilter()
    - getBranchesByLocation()
    - getBranchesByAccessibility()
    - getBranchesByPostCode()
    - getBranchesByTownName()
    ```
- **Product Interface**
    ```
    - BCA
        - getBCAByFilter()
        - getBCAByFeeCategory()
        - getBCAByFeeType()
        - getBCAByMarketingState()
    - CCA
        - getCCAByFilter()
        - getCCAByFeeCategory()
        - getCCAByFeeType()
        - getCCAByMarketingState()
    - PCA
        - getPCAByFilter()
        - getPCAByFeeCategory()
        - getPCAByFeeType()
        - getPCAByMarketingState()
    - SME
        - getSMEByFilter()
        - getSMEByMarketingState()
    ```
- **Metrics Interface**
  ```
  - PCA
      - getMetricsPCAByFilter()
      - getMetricsPCAByMatterMethodType()
      - getMetricsPCAByMatterType()
  - BCA
      - getMetricsBCAByFilter()
      - getMetricsBCAByMatterMethodType()
      - getMetricsBCAByMatterType()
  ```
-->
### Code Setup
The SDK supports the following  Java environments.
- **Java versions :** 8 (or above) - All the code consumer require minimum of Java 8 and have been tested against the oracle JVM, although we see no reason why later version of java wouldn't work
- **IDE**
  - [IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=windows)
  - [Eclipse](https://www.eclipse.org/downloads/)

Current SDK Version: 1.0.0
You can find the changes for each version in the change log on Bank Of API portal.
You can get the SDK  directly from repository or through Maven or Gradle

##### As External Jar
- Download the SDK jar from repository directly
- Add as external library in your project

##### Maven
- Find the latest version in the Maven central repository
- Add the below code as a maven dependency in the pom.xml file
    ```
    <dependency>
        <groupId>com.natwest.bankofapi</groupId>
        <artifactId>bankofapi-sdk-java</artifactId>
        <version>1.0.0</version>
    </dependency>
    ```

##### Gradle
- Find the latest version in the Maven central repository
- Add the below code as a gradle dependency in the build.gradle file
    ```
    implementation group: 'com.natwest.bankofapi', name: 'bankofapi-sdk-java', version: '1.0.0'
    ```

### Getting Started

1. This SDK provides a _plug and play_ facility for the TPP developers.
2. Add opendatasdk.jar or add the maven dependency from maven central in pom.xml.
3. Use below code for connect SDK :
    ```
    OpenDataService openDataService = new OpenDataService();
    ATMService atmService = openDataService.getAtmService();
    ```
<!--   
# SDK example setup

 ### Preliminary Steps
  1. Create your application, where will you use this SDK.
  2. Download the SDK jar from repository directly and add in your application or add the maven dependency from maven central in pom.xml.
-->

 ### Code Example

1. To get All Atms data using below code:
   ```
    OpenDataService openDataService = new OpenDataService();
    ATMService atmService = openDataService.getAtmService();
    List<ATM> allAtms = atmService.getAllData();
    ```
      a. To get All Atms data based on Postcode filter using below code:
      ```
      OpenDataService openDataService = new OpenDataService();
      ATMService atmService = openDataService.getAtmService();
      List<ATM> allAtms = atmService.getATMsByPostCode("SW1A");
     ```
        
      b. To get All Atms data based on Town Name filter using below code:
      ```
      OpenDataService openDataService = new OpenDataService();
      ATMService atmService = openDataService.getAtmService();
      List<ATM> allAtms = atmService.getATMsByTownName("London");
     ```
2. To get All Branches data using below code:
   ```
    OpenDataService openDataService = new OpenDataService();
    ATMService atmService = openDataService.getAtmService();
    List<ATM> allAtms = atmService.getAllData();
    ```
   a. To get All Branches data based on Accessibility filter using below code:
      ```
      OpenDataService openDataService = new OpenDataService();
      BranchesService branchesService = openDataService.getBranchesService();
      List<Branches> allBranches = branchesService.getBranchesByAccessibility("InductionLoop");
     ```

   b. To get All Branches data based on Town Name filter using below code:
      ```
      OpenDataService openDataService = new OpenDataService();
      BranchesService branchesService = openDataService.getBranchesService();
      List<Branches> allBranches = branchesService.getBranchesByTownName("Aberaeron");
     ```

# Roadmap

You can follow the latest updates and plans for BankOfAPI SDK for Java in the [Roadmap](https://github.com/dheerajrinku93/OpenDataSDKDocs/wiki#roadmap) published on our Wiki.

### Contributing

For any questions, bugs or feature requests please open an issue. For anything else please send an email to {bankofapisdk.support@natwest.com}.

To submit a contribution:

- Goto BankOfApiSDK repo (https://github.com/bankofapi/openDataSDK)
- Create your feature branch (git checkout -b feature/openDataSDKBar)
- Read our contribution guidelines and Community Code of Conduct
- Commit your changes (git commit -am 'Add some openDataSDKBar')
- Push to the branch (git push origin feature/openDataSDKBar)
- Create a new Pull Request
