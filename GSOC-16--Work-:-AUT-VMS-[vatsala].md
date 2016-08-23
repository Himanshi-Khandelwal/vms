Wiki Page for description of GSOC work for Systers Volunteer Management System

***

## Links:

For submission purpose, systers automated testing repository has been used while all the actual changes have been made to the main VMS repository. Code has been merged to the automated testing repository only once it has been reviewed for VMS.

* Submissions to automated testing repository - [Code Samples Folder](https://github.com/systers/automated-testing/tree/develop/PortalVMSTests), [PR list](https://github.com/systers/automated-testing/pulls?utf8=%E2%9C%93&q=is%3Apr%20author%3Asmarshy), [authored commits](https://github.com/systers/automated-testing/commits/develop?author=smarshy)
* Weekly status reports and blogs - [Doku profile](http://systers.org/systers-dev/doku.php/vatsala_swaroop)
* Blog -[here](https://smarshypants.wordpress.com/)  


## Completed tasks:

| Tasks                                          | Related Issue/PR in VMS| Status|
|----------------------------------------------------------|:------------------:|:-------: |
| Added automated tests to vms and synced them as per latest code |  [PR-315](https://github.com/systers/vms/pull/315)| Merged| 
| Integrated VMS with Travis | [Issue-140](https://github.com/systers/vms/issues/140), [PR-332](https://github.com/systers/vms/pull/332), [PR-334](https://github.com/systers/vms/pull/334), [343](https://github.com/systers/vms/pull/343)| Merged|
| Reported new bugs in vms | [Issue-325](https://github.com/systers/vms/issues/325), [Issue-326](https://github.com/systers/vms/issues/326), [Issue-327](https://github.com/systers/vms/issues/327), [Issue-336](https://github.com/systers/vms/issues/336), [Issue-337](https://github.com/systers/vms/issues/337), [Issue-340](https://github.com/systers/vms/issues/340), [Issue-345](https://github.com/systers/vms/issues/345), [Issue-350](https://github.com/systers/vms/issues/350)| N/A|
| Increased test coverage via functional tests | [Issue-346](https://github.com/systers/vms/issues/346), [PR-347](https://github.com/systers/vms/pull/347), [PR-335](https://github.com/systers/vms/pull/335), [PR-357](https://github.com/systers/vms/pull/357)| Merged|
| Minor changes to configure coverage for vms | [PR-348](https://github.com/systers/vms/pull/348), [PR-353](https://github.com/systers/vms/pull/353)| Merged|
| Reduced time, duplication for unit tests | [Issue-344](https://github.com/systers/vms/issues/344), [Issue-369](https://github.com/systers/vms/issues/369), [PR-356](https://github.com/systers/vms/pull/356), [PR-339](https://github.com/systers/vms/pull/339)| Merged|
| Increased test coverage via unit tests | [Issue-346](https://github.com/systers/vms/issues/346), [PR-358](https://github.com/systers/vms/pull/358), [PR-360](https://github.com/systers/vms/pull/360)| Merged|
| Reduced time, duplication for selenium tests | [Issue-369](https://github.com/systers/vms/issues/369), [PR-370](https://github.com/systers/vms/pull/370) | Merged|
| Migrated entire test architecture to POM | [Issue-369](https://github.com/systers/vms/issues/369), [Issue-376](https://github.com/systers/vms/issues/376), [PR-375](https://github.com/systers/vms/pull/375) | Open|
| Added Database checks for CRUD operations | [PR-380](https://github.com/systers/vms/pull/380) | Open|
| Documentation | [PR-378](https://github.com/systers/vms/pull/378)| Merged|

## Results/ Summary
* Migrated entire selenium test architecture of around 115 tests to follow page object model design, thus increasing scalibility and ease of maintenance for the system

* Refactored existing 167 tests to increase re usability and observed following approximate reductions: 

| Test Type | Time| Duplication| Database objects|
|---------------|:-------:|:-------: |:-------: |
|Selenium|41%|30%|N/A|
|Unit|50%|50%|74%|

* Increased test coverage to 83% by fixing errors in initial 76 tests, adding 45 new selenium tests, extending 22 unit tests and adding database checks to 64 tests
* Setup Travis and local Browserstack integration for vms

Detailed documents recording reductions - [unit](https://docs.google.com/spreadsheets/d/1UZgyiU292uWTiriv9kMA2B8uFwF0hu5gX7EF_xV5jDk/edit?usp=sharing) and [selenium](https://docs.google.com/spreadsheets/d/1srHVtKDA8x74uqoL6tNMvN5apaZjuvAflMg84oPgHzA/edit?usp=sharing)

## Guide to Work Continuation:
* Local Browserstack integration has been setup for my fork of VMS using username and local access key for my account. For the main project, these need to be updated to use the Systers account. Also, the desired capabilities need to be updated as per requirements and the results of the tests need to be recorded. If these tests are to be run automatically, Browserstack needs to be integrated with travis.
* Coverage report needs to be inspected to find out which lines are being missed and then tests should be expanded to address relevant lines.

