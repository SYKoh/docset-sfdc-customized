# Shawn's Customized SFDashC

When I attempted to use the original project [SFDashC](https://github.com/ViViDboarder/docset-sfdc) in August 2023, I encountered difficulties in generating the correct Salesforce Apex Dash docset. Determined to address the issue despite my lack of experience with Golang, I conducted some research into the original project. Fortunately, I was able to 'fix' the code and successfully generate the desired docset.

Here is an overview of what I accomplished and my insights into the original project. It's important to note that there might be some misconceptions, and this repository is intended solely for reference purposes.

- Adjusted the sub URL settings in certain files from `apexcode` to `apexref` (possibly due to changes in the URL path of the Apex reference guide documentation web sites).
- Commented out specific code lines in the Makefile to ensure that only the Apex Reference docset would be generated (as I only required that particular documentation).

Now, when you execute the `make` command, the Apex Reference Guide Dash docset is generated accurately and exclusively.

- In the `supportedtypes.go` file, it defined the strings for matching URLs, thereby controlling the content that should be generated.


---
# Origin Repository README: 

SFDashC
=======

SFDashC is a go application for downloading and constructing Dash docsets from the Salesforce online documentation

Everything is wrapped with a Makefile and can be completely built by executing:

    make

That's it!

It will generate 3 docsets: Salesforce Apex, Salesforce Visualforce, and Salesforce Lightning

To Do
-----

 - [ ] Now that new `ForceCascadeType` is available, some of the entries in `./SFDashC/supportedtypes.go` can be simplified
