# Create a Test Report<a name="report-create"></a>


|  | 
| --- |
| The test reporting feature is in preview release for CodeBuild and is subject to change\. | 

 To create a test report, you run a build project that is configured with one to five report groups in its buildspec file\. A test report is created during the run\. It contains the results of the test cases that are specified for the report groups\. A new test report is generated for each subsequent build that uses the same buildspec file\. 

**To create a test report**

1.  Create a build project\. For information, see [Create a Build Project in CodeBuild](create-project.md)\. 

1.  Configure the buildspec file of your project with test report informaton: 

   1. Add a `reports:` section and specify the name for your report group\. CodeBuild creates a report group for you using your project name and the name you specified in the format `project-name`\-`report-group-name-in-buildspec`\. If you already have a report group you want to use, specify its ARN\. \(If you use its name instead of its ARN, CodeBuild creates a new report group\.\) For more information, see [Reports Syntax in the Buildspec File](build-spec-ref.md#reports-buildspec-file)\. 

   1. Under the report group, specify the location of the files that store test results\. If you use more than one report group, specify test result file locations for each one\. A new test report is created each time your build project runs\. For more information, see [Specify Test Files](report-group-test-cases.md)\. 

   1. In the `commands` section of the `build` or `post_build` sequence, specify the commands that run the tests cases you specified for your report groups\. For more information, see [ Specify Test Commands ](report-group-test-case-commands.md)\. 

1.  Run a build of the build project\. For more information, see [Run a Build in CodeBuild](run-build.md)\. 

1.  When the build is complete, choose the new build run from **Build history** on your project page\. Choose **Reports** to view the test report\. For more information, see [ View Test Reports for a Build ](test-view-reports.md#test-view-project-reports)\.