﻿TransMock allows you to easily test your BizTalk integrations in an end-to-end manner. 
It does so by introducing a set of custom BizUnit test steps, which when executed from a test case, 
communicate with an integration through the TransMock adapter.

The following BizTalk Server versions are supported:
- 2010/2013/2013 R2/2016

NB: Please note that for each version update the btdfproj file has to be updated in the part where the reference to the TransMock.targets file is defined!
    Example: v1.3.3 reference is:      <Import Project="$(MSBuildProjectDirectory)\..\packages\TransMock.Framework.1.3.3\BTDF\TransMock.targets" />
	         v1.3.5 reference will be: <Import Project="$(MSBuildProjectDirectory)\..\packages\TransMock.Framework.1.3.5\BTDF\TransMock.targets" />

**** Release notes ****
Version 1.3.5:
- Fixed issue with wrong target .NET framework for the BizTalk 2016 version of BizUnit integration project
 
Version 1.3.3:
- Fixed an issue with the BTDF integration where wrong name of an internal BTDF variable was used

Version 1.3.2:
- Fixed an issue with wrong path to the TransMock tools path
- Fixed an issue with the BTDF deploy target not invoked from older BTDF versions (<v5.7)

Version 1.3:
- Added support for BizTalk Server 2016
- Implemented support for BizUnit 5.0
- Implemented Nuget package distribution