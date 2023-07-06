

## Documentation on Integrating OpenAPI:


**1.  Ensure that the endpoint you are going to use is available in Swagger:**

 - Open Swagger at [https://staging-cms.edu-go.com/](https://staging-cms.edu-go.com/).
  -   Make sure that the endpoint you intend to use is present in Swagger.

 **2.  Go to the frontend repository:**

 - Open a terminal or command prompt. 	
 - Navigate to the frontend
   repository directory.

**3. Run the command "npm run openapi" in the terminal:**

 -  Type the command "npm run openapi" in the terminal.
   -   This command will execute the OpenAPI code generation process.

**4. Open the api.ts file in the frontend repository:**

 - Locate the api.ts file in the frontend repository directory. 	
 - Open the file using a text editor or IDE.

**5.  Import the generated service module class in api.ts:**

 -  Add the following code at the top of the api.ts file:

    import { ActivityApi } from "api/openapi";`

   
   **6.  Add to the instance const instance = useAxios():**

 - Find the code section where the axios instance is initialized. 	Add
   the following line before the return statement:

    `const instance = useAxios();`

**7. Add the API definition to the instance:**
	

 -   Locate the return statement inside the function.
 -   Add the following line before the return statement: 		`AuthApi: new ActivityApi(undefined, undefined, instance),`

	
**8.Then make the connector file with react-query**

    const  apiScope:  AvailableAPIScopeStrings  =  "ActivityApi"  as  const; 
    //ActivityApi is the endpoint classname you wanna use you check it on api,ts
	const  endpointId:  AvailableEndpoint<typeof  apiScope> = "ActivityDelete"  as  const; 
	//ActivityDelete is the functional programming name you wanna use you check it on api,ts too

    type  ParamType  =  GetApiParam<typeof  apiScope,typeof  endpointId>["activityStoreRequestPermissionsInner"]; 
    //activityStoreRequestPermissionsInner is type of param that fp above use // you can check in api.ts asswell
    // the rest of the connector code you can look up on existing connector file on "src/api/core"

	

