# Integration-Projects
Contains X++ and .NET(C#) for integration with FnO

Custom Services:
1. D365FOCustomServiceSample.zip - The zip file contains a C# console application, C# objects that contain purchase order header\line and service response data, and X++ objects to     create the PO using the PO Data Entities. 
    
        a. The D365FO model used for the X++ project is named CPRCustomServiceSample. The D365FO_XPP_CustomServiceObjects Export Package.axpp file is in the zip file.
        b. The D365FO_Common_Controller.cs file contains the placeholder entries you will need to enter for you Azure App Client Id and secret. Along with the D2365FO URLs and                 Azure AD tenant:

            //global settings for D365FO and Azure App Id info
   	        private static string aadClientAppId = "xxxxxxxx-de0c-415d-a1d6-b4ea7f66a8e6";
            private static string aadClientAppSecret = "xxxxxvitXHJ93oLQEiK0tR1b3mAKUW6sLC1mUlVieS8=";
            private static string aadTenant = https://login.windows.net/microsoft.com;
            private static string baseURL = https://xxxxxxxfinopsdeveec2c152fa9c727ddevaos.cloudax.dynamics.com;
            private static string ApiUrl = https://xxxxxxxfinopsdeveec2c152fa9c727ddevaos.cloudax.dynamics.com/api/services;
    c. The D365FO_CSharp_Objects_Sample project requires Nuget packages Microsoft.Identity.Client and Newtonsoft.Json. 	
    d. The XPP D365FO_CustomService_XPP_Objects project contains the X++ code to create the PO with lines and populates the response object back for the console app to iterate             through.  In the D365FP_CustomService_AP class, there are two service operations that create the purchase order. The response object contains an array of PO Line data. 

