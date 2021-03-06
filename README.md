# swagger-java-client

Clever API
- API version: 3.0.0
  - Build date: 2021-12-24T14:02:24.069Z

The Clever API


*Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)*


## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>io.swagger</groupId>
  <artifactId>swagger-java-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "io.swagger:swagger-java-client:1.0.0"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/swagger-java-client-1.0.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import io.swagger.client.*;
import io.swagger.client.auth.*;
import io.swagger.client.model.*;
import io.swagger.client.api.DataApi;

import java.io.File;
import java.util.*;

public class DataApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        
        // Configure OAuth2 access token for authorization: oauth
        OAuth oauth = (OAuth) defaultClient.getAuthentication("oauth");
        oauth.setAccessToken("YOUR ACCESS TOKEN");

        DataApi apiInstance = new DataApi();
        String id = "id_example"; // String | 
        Integer limit = 56; // Integer | 
        String startingAfter = "startingAfter_example"; // String | 
        String endingBefore = "endingBefore_example"; // String | 
        try {
            UsersResponse result = apiInstance.getContactsForUser(id, limit, startingAfter, endingBefore);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DataApi#getContactsForUser");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://api.clever.com/v3.0*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DataApi* | [**getContactsForUser**](docs/DataApi.md#getContactsForUser) | **GET** /users/{id}/mycontacts | 
*DataApi* | [**getCourse**](docs/DataApi.md#getCourse) | **GET** /courses/{id} | 
*DataApi* | [**getCourseForSection**](docs/DataApi.md#getCourseForSection) | **GET** /sections/{id}/course | 
*DataApi* | [**getCourses**](docs/DataApi.md#getCourses) | **GET** /courses | 
*DataApi* | [**getCoursesForResource**](docs/DataApi.md#getCoursesForResource) | **GET** /resources/{id}/courses | 
*DataApi* | [**getCoursesForSchool**](docs/DataApi.md#getCoursesForSchool) | **GET** /schools/{id}/courses | 
*DataApi* | [**getDistrict**](docs/DataApi.md#getDistrict) | **GET** /districts/{id} | 
*DataApi* | [**getDistrictForCourse**](docs/DataApi.md#getDistrictForCourse) | **GET** /courses/{id}/district | 
*DataApi* | [**getDistrictForSchool**](docs/DataApi.md#getDistrictForSchool) | **GET** /schools/{id}/district | 
*DataApi* | [**getDistrictForSection**](docs/DataApi.md#getDistrictForSection) | **GET** /sections/{id}/district | 
*DataApi* | [**getDistrictForTerm**](docs/DataApi.md#getDistrictForTerm) | **GET** /terms/{id}/district | 
*DataApi* | [**getDistrictForUser**](docs/DataApi.md#getDistrictForUser) | **GET** /users/{id}/district | 
*DataApi* | [**getDistricts**](docs/DataApi.md#getDistricts) | **GET** /districts | 
*DataApi* | [**getResource**](docs/DataApi.md#getResource) | **GET** /resources/{id} | 
*DataApi* | [**getResources**](docs/DataApi.md#getResources) | **GET** /resources | 
*DataApi* | [**getResourcesForCourse**](docs/DataApi.md#getResourcesForCourse) | **GET** /courses/{id}/resources | 
*DataApi* | [**getResourcesForSection**](docs/DataApi.md#getResourcesForSection) | **GET** /sections/{id}/resources | 
*DataApi* | [**getResourcesForUser**](docs/DataApi.md#getResourcesForUser) | **GET** /users/{id}/resources | 
*DataApi* | [**getSchool**](docs/DataApi.md#getSchool) | **GET** /schools/{id} | 
*DataApi* | [**getSchoolForSection**](docs/DataApi.md#getSchoolForSection) | **GET** /sections/{id}/school | 
*DataApi* | [**getSchools**](docs/DataApi.md#getSchools) | **GET** /schools | 
*DataApi* | [**getSchoolsForCourse**](docs/DataApi.md#getSchoolsForCourse) | **GET** /courses/{id}/schools | 
*DataApi* | [**getSchoolsForTerm**](docs/DataApi.md#getSchoolsForTerm) | **GET** /terms/{id}/schools | 
*DataApi* | [**getSchoolsForUser**](docs/DataApi.md#getSchoolsForUser) | **GET** /users/{id}/schools | 
*DataApi* | [**getSection**](docs/DataApi.md#getSection) | **GET** /sections/{id} | 
*DataApi* | [**getSections**](docs/DataApi.md#getSections) | **GET** /sections | 
*DataApi* | [**getSectionsForCourse**](docs/DataApi.md#getSectionsForCourse) | **GET** /courses/{id}/sections | 
*DataApi* | [**getSectionsForResource**](docs/DataApi.md#getSectionsForResource) | **GET** /resources/{id}/sections | 
*DataApi* | [**getSectionsForSchool**](docs/DataApi.md#getSectionsForSchool) | **GET** /schools/{id}/sections | 
*DataApi* | [**getSectionsForTerm**](docs/DataApi.md#getSectionsForTerm) | **GET** /terms/{id}/sections | 
*DataApi* | [**getSectionsForUser**](docs/DataApi.md#getSectionsForUser) | **GET** /users/{id}/sections | 
*DataApi* | [**getStudentsForUser**](docs/DataApi.md#getStudentsForUser) | **GET** /users/{id}/mystudents | 
*DataApi* | [**getTeachersForUser**](docs/DataApi.md#getTeachersForUser) | **GET** /users/{id}/myteachers | 
*DataApi* | [**getTerm**](docs/DataApi.md#getTerm) | **GET** /terms/{id} | 
*DataApi* | [**getTermForSection**](docs/DataApi.md#getTermForSection) | **GET** /sections/{id}/term | 
*DataApi* | [**getTerms**](docs/DataApi.md#getTerms) | **GET** /terms | 
*DataApi* | [**getTermsForSchool**](docs/DataApi.md#getTermsForSchool) | **GET** /schools/{id}/terms | 
*DataApi* | [**getUser**](docs/DataApi.md#getUser) | **GET** /users/{id} | 
*DataApi* | [**getUsers**](docs/DataApi.md#getUsers) | **GET** /users | 
*DataApi* | [**getUsersForResource**](docs/DataApi.md#getUsersForResource) | **GET** /resources/{id}/users | 
*DataApi* | [**getUsersForSchool**](docs/DataApi.md#getUsersForSchool) | **GET** /schools/{id}/users | 
*DataApi* | [**getUsersForSection**](docs/DataApi.md#getUsersForSection) | **GET** /sections/{id}/users | 
*EventsApi* | [**getEvent**](docs/EventsApi.md#getEvent) | **GET** /events/{id} | 
*EventsApi* | [**getEvents**](docs/EventsApi.md#getEvents) | **GET** /events | 


## Documentation for Models

 - [BadRequest](docs/BadRequest.md)
 - [Contact](docs/Contact.md)
 - [Course](docs/Course.md)
 - [CourseObject](docs/CourseObject.md)
 - [CourseResponse](docs/CourseResponse.md)
 - [CoursesCreated](docs/CoursesCreated.md)
 - [CoursesDeleted](docs/CoursesDeleted.md)
 - [CoursesResponse](docs/CoursesResponse.md)
 - [CoursesUpdated](docs/CoursesUpdated.md)
 - [Credentials](docs/Credentials.md)
 - [District](docs/District.md)
 - [DistrictAdmin](docs/DistrictAdmin.md)
 - [DistrictContact](docs/DistrictContact.md)
 - [DistrictObject](docs/DistrictObject.md)
 - [DistrictResponse](docs/DistrictResponse.md)
 - [DistrictsCreated](docs/DistrictsCreated.md)
 - [DistrictsDeleted](docs/DistrictsDeleted.md)
 - [DistrictsResponse](docs/DistrictsResponse.md)
 - [DistrictsUpdated](docs/DistrictsUpdated.md)
 - [Event](docs/Event.md)
 - [EventResponse](docs/EventResponse.md)
 - [EventsResponse](docs/EventsResponse.md)
 - [InternalError](docs/InternalError.md)
 - [Link](docs/Link.md)
 - [Location](docs/Location.md)
 - [Name](docs/Name.md)
 - [NotFound](docs/NotFound.md)
 - [Principal](docs/Principal.md)
 - [Resource](docs/Resource.md)
 - [ResourceObject](docs/ResourceObject.md)
 - [ResourceResponse](docs/ResourceResponse.md)
 - [ResourcesCreated](docs/ResourcesCreated.md)
 - [ResourcesDeleted](docs/ResourcesDeleted.md)
 - [ResourcesResponse](docs/ResourcesResponse.md)
 - [ResourcesUpdated](docs/ResourcesUpdated.md)
 - [Roles](docs/Roles.md)
 - [School](docs/School.md)
 - [SchoolEnrollment](docs/SchoolEnrollment.md)
 - [SchoolObject](docs/SchoolObject.md)
 - [SchoolResponse](docs/SchoolResponse.md)
 - [SchoolsCreated](docs/SchoolsCreated.md)
 - [SchoolsDeleted](docs/SchoolsDeleted.md)
 - [SchoolsResponse](docs/SchoolsResponse.md)
 - [SchoolsUpdated](docs/SchoolsUpdated.md)
 - [Section](docs/Section.md)
 - [SectionObject](docs/SectionObject.md)
 - [SectionResponse](docs/SectionResponse.md)
 - [SectionsCreated](docs/SectionsCreated.md)
 - [SectionsDeleted](docs/SectionsDeleted.md)
 - [SectionsResponse](docs/SectionsResponse.md)
 - [SectionsUpdated](docs/SectionsUpdated.md)
 - [Staff](docs/Staff.md)
 - [Student](docs/Student.md)
 - [StudentRelationship](docs/StudentRelationship.md)
 - [Teacher](docs/Teacher.md)
 - [Term](docs/Term.md)
 - [TermObject](docs/TermObject.md)
 - [TermResponse](docs/TermResponse.md)
 - [TermsCreated](docs/TermsCreated.md)
 - [TermsDeleted](docs/TermsDeleted.md)
 - [TermsResponse](docs/TermsResponse.md)
 - [TermsUpdated](docs/TermsUpdated.md)
 - [User](docs/User.md)
 - [UserObject](docs/UserObject.md)
 - [UserResponse](docs/UserResponse.md)
 - [UsersCreated](docs/UsersCreated.md)
 - [UsersDeleted](docs/UsersDeleted.md)
 - [UsersResponse](docs/UsersResponse.md)
 - [UsersUpdated](docs/UsersUpdated.md)


## Documentation for Authorization

Authentication schemes defined for the API:
### oauth

- **Type**: OAuth
- **Flow**: accessCode
- **Authorization URL**: https://clever.com/oauth/authorize
- **Scopes**: N/A


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



#   c l e v e r V 3  
 