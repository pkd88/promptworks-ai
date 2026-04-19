Oracle® AI Database 
SQL*Plus® User's Guide and Reference 
26ai 
G44104-02 
January 2026
Oracle AI Database SQL*Plus® User's Guide and Reference, 26ai 
G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
Primary Author: Gunjan Jain 
Contributors: Luan Nim, Andrei Souleimanian, Senthilprabhu Dhamotharan, Mahantesh Savanur 
This software and related documentation are provided under a license agreement containing restrictions on use and disclosure and are protected by intellectual property laws. Except as expressly permitted in your license agreement or allowed by law, you may not use, copy, reproduce, translate, broadcast, modify, license, transmit, distribute, exhibit, perform, publish, or display any part, in any form, or by any means. Reverse engineering, disassembly, or decompilation of this software, unless required by law for interoperability, is prohibited. 
The information contained herein is subject to change without notice and is not warranted to be error-free. If you find any errors, please report them to us in writing. 
If this is software, software documentation, data (as defined in the Federal Acquisition Regulation), or related documentation that is delivered to the U.S. Government or anyone licensing it on behalf of the U.S. Government, then the following notice is applicable: 
U.S. GOVERNMENT END USERS: Oracle programs (including any operating system, integrated software, any programs embedded, installed, or activated on delivered hardware, and modifications of such programs) and Oracle computer documentation or other Oracle data delivered to or accessed by U.S. Government end users are "commercial computer software," "commercial computer software documentation," or "limited rights data" pursuant to the applicable Federal Acquisition Regulation and agency-specific supplemental regulations. As such, the use, reproduction, duplication, release, display, disclosure, modification, preparation of derivative works, and/or adaptation of i) Oracle programs (including any operating system, integrated software, any programs embedded, installed, or activated on delivered hardware, and modifications of such programs), ii) Oracle computer documentation and/or iii) other Oracle data, is subject to the rights and limitations specified in the license contained in the applicable contract. The terms governing the U.S. Government's use of Oracle cloud services are defined by the applicable contract for such services. No other rights are granted to the U.S. Government. 
This software or hardware is developed for general use in a variety of information management applications. It is not developed or intended for use in any inherently dangerous applications, including applications that may create a risk of personal injury. If you use this software or hardware in dangerous applications, then you shall be responsible to take all appropriate fail-safe, backup, redundancy, and other measures to ensure its safe use. Oracle Corporation and its affiliates disclaim any liability for any damages caused by use of this software or hardware in dangerous applications. 
Oracle®, Java, MySQL, and NetSuite are registered trademarks of Oracle and/or its affiliates. Other names may be trademarks of their respective owners. 
Intel and Intel Inside are trademarks or registered trademarks of Intel Corporation. All SPARC trademarks are used under license and are trademarks or registered trademarks of SPARC International, Inc. AMD, Epyc, and the AMD logo are trademarks or registered trademarks of Advanced Micro Devices. UNIX is a registered trademark of The Open Group. 
This software or hardware and documentation may provide access to or information about content, products, and services from third parties. Oracle Corporation and its affiliates are not responsible for and expressly disclaim all warranties of any kind with respect to third-party content, products, and services unless otherwise set forth in an applicable agreement between you and Oracle. Oracle Corporation and its affiliates will not be responsible for any loss, costs, or damages incurred due to your access to or use of third-party content, products, or services, except as set forth in an applicable agreement between you and Oracle.
Contents 
Preface 
Audience i Related Documents i Conventions ii 
Changes in This Release for Oracle AI Database SQL*Plus User's Guide and Reference 
New Features i Deprecated Features ii 
Introduction to SQL*Plus 
SQL*Plus Resources i SQL*Plus Overview i Certification ii SQL*Plus Prerequisites iii Starting SQL*Plus Command-line iii Using SQL*Plus from Oracle Instant Client Package iv About Connecting to a Different Database v About Sample Schemas and SQL*Plus v Running your first Query vi About Exiting SQL*Plus vii 
Part I Introduction to SQL*Plus 
1 SQL*Plus User Interface 
1.1 About the Command-line Screen 1 1.2 Changing the Command-line Font and Font Size 1 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page i of xii
2 Configuring SQL*Plus 
2.1 SQL*Plus Environment Variables 1 2.1.1 SQLPATH Registry Entry 2 2.2 SQL*Plus Configuration 3 2.2.1 Site Profile 4 2.2.1.1 Default Site Profile Script 4 2.2.2 User Profile 4 2.2.2.1 Modifying Your LOGIN File 5 2.2.3 Storing and Restoring SQL*Plus System Variables 5 2.2.3.1 Restoring the System Variables 5 2.2.4 About Installing Command-line Help 6 2.2.4.1 Running the hlpbld.sql Script to Install Command-line Help 6 2.2.4.2 Running the helpdrop.sql Script to Remove Command-line Help 7 2.2.5 About Configuring Oracle Net Services 7 
3 Starting SQL*Plus 
3.1 Login Username and Password 1 3.1.1 Secure External Password Store 2 3.1.2 Expired Password 2 3.1.3 About Changing your Password 2 
3.2 About Connecting to a Database 2 3.2.1 Easy Connection String 3 3.2.2 Net Service Name 3 3.2.3 Full Connection Identifier 4 3.2.4 Connectionless Session with /NOLOG 4 
3.3 About Starting SQL*Plus 4 3.3.1 About Starting Command-line SQL*Plus 5 3.3.2 About Getting Command-line Help 6 
3.4 About Exiting SQL*Plus Command-line 6 3.5 SQL*Plus Program Syntax 6 3.5.1 Options 7 3.5.1.1 HELP Option 7 3.5.1.2 VERSION Option 7 3.5.1.3 COMPATIBILITY Option 7 3.5.1.4 LOGON Option 8 3.5.1.5 FAST Option 8 3.5.1.6 MARKUP Options 8 3.5.1.7 MARKUP Usage Notes 11 3.5.1.8 No Login Time Option 11 3.5.1.9 PING Option 12 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page ii of xii
3.5.1.10 RESTRICT Option 12 3.5.1.11 SILENT Option 12 3.5.2 Logon 13 3.5.3 Start 14 
Part II Using SQL*Plus 
4 SQL*Plus Basics 
4.1 About Entering and Executing Commands 1 4.1.1 The SQL Buffer 1 4.1.2 About Executing Commands 2 
4.2 About Listing a Table Definition 2 4.3 About Listing PL/SQL Definitions 3 4.4 Running SQL Commands 3 
4.4.1 About Understanding SQL Command Syntax 4 4.4.1.1 About Dividing a SQL Command into Separate Lines 4 4.4.1.2 About Ending a SQL Command 4 
4.5 About Running PL/SQL Blocks 5 4.5.1 About Creating Stored Procedures 6 4.6 Running SQL*Plus Commands 6 4.6.1 About Understanding SQL*Plus Command Syntax 7 4.6.1.1 About Continuing a Long SQL*Plus Command on Additional Lines 7 4.7 System Variables that Affect How Commands Run 8 4.8 About Stopping a Command while it is Running 8 4.9 About Running Operating System Commands 8 4.10 About Pausing the Display 9 4.11 About Saving Changes to the Database Automatically 9 
5 Using Scripts in SQL*Plus 
5.1 About Editing Scripts 1 5.1.1 Writing Scripts with a System Editor 1 5.2 About Editing Scripts in SQL*Plus Command-Line 2 5.2.1 Listing the Buffer Contents 3 5.2.2 Editing the Current Line 4 5.2.3 Appending Text to a Line 5 5.2.4 Adding a New Line 6 5.2.5 Deleting Lines 7 5.3 About Placing Comments in Scripts 7 5.3.1 Using the REMARK Command 7 5.3.2 Using /*...*/ 7 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page iii of xii
5.3.3 Using - - 8 5.3.4 Notes on Placing Comments 8 5.4 Running Scripts 10 5.4.1 Running a Script as You Start SQL*Plus 11 5.5 Nesting Scripts 11 5.6 About Exiting from a Script with a Return Code 11 
6 Using Substitution Variables 
6.1 Defining Substitution Variables 1 6.2 About Using Predefined Variables 2 6.3 Referencing Substitution Variables 2 
6.3.1 Where and How to Use Substitution Variables 2 6.3.2 Difference Between "&" and "&&" Prefixes 4 6.3.3 Storing a Query Column Value in a Substitution Variable 5 6.3.4 Restrictions 5 6.3.5 How Substitution Variables are Handled in SQL*Plus 6 6.3.6 Substitution Variable Commands 6 
6.3.6.1 Using "&" Prefixes With Title Variables 7 6.3.6.2 Variables and Text Spacing in Titles 8 6.3.7 Substitution Variable Namespace, Types, Formats and Limits 9 6.3.8 Assigning Substitution Variables to Bind Variables 11 6.3.9 Assigning Bind Variables to Substitution Variables 11 6.3.10 Substitution Variable Examples 12 6.3.10.1 Setting a Substitution Variable's Value 12 6.3.10.2 Using a Substitution Variable 13 6.3.10.3 Finding All Defined Substitution Variables 13 6.3.10.4 Inserting Data Containing "&" Without Being Prompted 13 6.3.10.5 Putting the Current Date in a Spool File Name 14 
6.3.10.6 Appending Alphanumeric Characters Immediately After a Substitution 
Variable 14 
6.3.10.7 Putting a Period After a Substitution Variable 15 
6.3.10.8 Using a Fixed Value Variable in a TTITLE, BTITLE, REPHEADER or 
REPFOOTER 15 
6.3.10.9 Using a Changing Value Variable in a TTITLE, BTITLE, REPHEADER or 
REPFOOTER 15 
6.3.10.10 Using the Value of a Bind Variable in a SQL*Plus Command Like 
SPOOL 15 
6.3.10.11 Passing Parameters to SQL*Plus Substitution Variables 16 6.3.10.12 Passing Operating System Variables to SQL*Plus 16 6.3.10.13 Passing a Value to a PL/SQL Procedure From the Command Line 17 6.3.10.14 Allowing Script Parameters to be Optional and Have a Default Value 17 6.3.10.15 Using a Variable for the SQL*Plus Return Status 18 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page iv of xii
6.3.10.16 Putting the Username and Database in the Prompt 19 6.4 System Variables Influencing Substitution Variables 19 6.4.1 System Variables in Titles and EXIT 20 6.5 Passing Parameters through the START Command 20 6.5.1 Script Parameters 22 6.6 About Communicating with the User 23 6.6.1 Receiving a Substitution Variable Value 23 6.6.2 Customizing Prompts for Substitution Variable 24 6.6.3 Sending a Message and Accepting Return as Input 25 6.6.4 Clearing the Screen 25 6.7 About Using Bind Variables 25 6.7.1 Creating Bind Variables 26 6.7.2 Referencing Bind Variables 26 6.7.3 Displaying Bind Variables 26 6.7.4 Executing an Input Bind 26 6.7.5 Limitation 27 6.8 Using REFCURSOR Bind Variables 28 6.9 Fetching Iterative Results from a SELECT inside a PL/SQL Block 31 
7 Formatting SQL*Plus Reports 
7.1 About Formatting Columns 1 7.1.1 About Changing Column Headings 1 7.1.1.1 Default Headings 1 7.1.1.2 Changing Default Headings 1 7.1.2 About Formatting NUMBER Columns 3 7.1.2.1 Default Display 3 7.1.2.2 Changing the Default Display 3 7.1.3 About Formatting Datatypes 4 7.1.3.1 Default Display 5 7.1.3.2 Changing the Default Display 5 7.1.4 Copying Column Display Attributes 7 7.1.5 Listing and Resetting Column Display Attributes 7 7.1.6 About Suppressing and Restoring Column Display Attributes 8 7.1.7 Printing a Line of Characters after Wrapped Column Values 8 7.2 About Clarifying Your Report with Spacing and Summary Lines 9 7.2.1 Suppressing Duplicate Values in Break Columns 10 7.2.2 Inserting Space when a Break Column's Value Changes 10 7.2.3 Inserting Space after Every Row 11 7.2.4 Using Multiple Spacing Techniques 11 7.2.5 Listing and Removing Break Definitions 12 7.2.6 Computing Summary Lines when a Break Column's Value Changes 12 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page v of xii
7.2.7 Computing Summary Lines at the End of the Report 15 7.2.8 Computing Multiple Summary Values and Lines 16 7.2.9 Listing and Removing COMPUTE Definitions 17 
7.3 About Defining Page and Report Titles and Dimensions 18 7.3.1 Setting the Top and Bottom Titles and Headers and Footers 18 7.3.1.1 Positioning Title Elements 19 7.3.1.2 Indenting a Title Element 20 7.3.1.3 Entering Long Titles 21 7.3.2 Displaying System-Maintained Values in Titles 21 7.3.3 Listing, Suppressing, and Restoring Page Title Definitions 22 7.3.4 Displaying Column Values in Titles 23 7.3.5 About Displaying the Current Date in Titles 24 7.3.6 Setting Page Dimensions 24 7.4 About Storing and Printing Query Results 26 7.4.1 Creating a Flat File 26 7.4.2 Sending Results to a File 26 7.4.3 Sending Results to a Printer 27 
8 Generating Reports from SQL*Plus 
8.1 About Creating Reports using Command-line SQL*Plus 1 8.1.1 Creating HTML Reports 1 8.1.1.1 HTML Entities 5 8.1.2 Creating CSV Reports 5 8.1.3 About Suppressing the Display of SQL*Plus Commands in Reports 5 
9 Tuning SQL*Plus 
9.1 About Tracing Statements 1 9.1.1 Controlling the Autotrace Report 1 9.1.2 Execution Plan 2 9.1.3 Statistics 2 
9.2 About Collecting Timing Statistics 5 9.3 Tracing Parallel and Distributed Queries 5 9.4 Execution Plan Output in Earlier Databases 7 9.5 About SQL*Plus Script Tuning 8 
9.5.1 COLUMN NOPRINT 8 9.5.2 SET APPINFO OFF 8 9.5.3 SET ARRAYSIZE 8 9.5.4 SET DEFINE OFF 9 9.5.5 SET FLUSH OFF 9 9.5.6 SET LINESIZE 9 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page vi of xii
9.5.7 SET LONGCHUNKSIZE 9 9.5.8 SET PAGESIZE 9 9.5.9 SET SERVEROUTPUT 9 9.5.10 SET SQLPROMPT 9 9.5.11 SET TAB 10 9.5.12 SET TERMOUT 10 9.5.13 SET TRIMOUT ON SET TRIMSPOOL ON 10 9.5.14 UNDEFINE 10 9.5.15 SET ROWPREFETCH 10 9.5.16 SET STATEMENTCACHE 10 9.5.17 SET LOBPREFETCH 11 9.5.18 Command Line -FAST Option 11 
10 SQL*Plus Security 
10.1 Disabling SQL*Plus, SQL, and PL/SQL Commands 1 10.2 About Creating and Controlling Roles 4 10.2.1 About Disabling SET ROLE 5 10.2.2 About Disabling User Roles 5 10.3 About Disabling Commands with SQLPLUS -RESTRICT 5 10.4 About Program Argument Security 6 
11 Database Administration with SQL*Plus 
11.1 Overview 1 11.2 Introduction to Database Startup and Shutdown 1 11.2.1 Database Startup 1 11.2.2 PDB Startup 2 11.2.3 Database Shutdown 2 11.2.4 PDB Shutdown 3 11.3 Redo Log Files 3 11.3.1 ARCHIVELOG Mode 3 11.4 Database Recovery 4 
12 SQL*Plus Globalization Support 
12.1 About Configuring Globalization Support in Command-line SQL*Plus 1 12.1.1 SQL*Plus Client 1 12.1.2 Oracle Database 1 
12.2 NLS_LANG Environment Variable 1 12.2.1 Viewing NLS_LANG Settings 2 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page vii of xii
12.3 Setting NLS_LANG 2 Part III SQL*Plus Reference 
13 SQL*Plus Command Reference 
13.1 SQL*Plus Command Summary 1 13.2 @ (at sign) 4 13.3 @@ (double at sign) 5 13.4 / (slash) 6 13.5 ACCEPT 7 13.6 APPEND 9 13.7 ARCHIVE LOG 9 13.8 ARGUMENT 11 13.9 ATTRIBUTE 14 13.10 BREAK 15 13.11 BTITLE 19 13.12 CHANGE 20 13.13 CLEAR 21 13.14 COLUMN 22 13.15 COMPUTE 31 13.16 CONFIG 35 13.17 CONNECT 37 13.18 COPY 39 13.19 DEFINE 39 
13.19.1 Predefined Variables 41 13.20 DESCRIBE 44 13.21 DEL 52 13.22 DISCONNECT 53 13.23 EDIT 54 13.24 EXECUTE 55 13.25 EXIT 56 13.26 GET 57 13.27 HELP 58 13.28 HISTORY 59 13.29 HOST 61 13.30 INPUT 62 13.31 LIST 63 13.32 OERR 65 13.33 PASSWORD 66 13.34 PAUSE 67 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page viii of xii
13.35 PING 67 13.36 PRINT 68 13.37 PROMPT 69 13.38 RECOVER 70 13.39 REMARK 76 13.40 REPFOOTER 77 13.41 REPHEADER 78 13.42 RUN 80 13.43 SAVE 81 13.44 SET 82 13.45 SET System Variable Summary 82 
13.45.1 SET APPINFO 86 13.45.2 SET ARRAYSIZE 87 13.45.3 SET AUTOCOMMIT 87 13.45.4 SET AUTOPRINT 88 13.45.5 SET AUTORECOVERY 88 13.45.6 SET AUTOTRACE 89 13.45.7 SET BLOCKTERMINATOR 89 13.45.8 SET CMDSEP 90 13.45.9 SET COLINVISIBLE 91 13.45.10 SET COLSEP 92 13.45.11 SET CONCAT 92 13.45.12 SET COPYCOMMIT 92 13.45.13 SET COPYTYPECHECK 93 13.45.14 SET DEFINE 93 13.45.15 SET DESCRIBE 93 13.45.16 SET ECHO 96 13.45.17 SET EDITFILE 96 13.45.18 SET EMBEDDED 97 13.45.19 SET ERRORDETAILS 97 13.45.20 SET ERRORLOGGING 98 13.45.21 SET ESCAPE 103 13.45.22 SET ESCCHAR 103 13.45.23 SET EXITCOMMIT 104 13.45.24 SET FEEDBACK 104 13.45.25 SET FLAGGER 106 13.45.26 SET FLUSH 106 13.45.27 SET HEADING 106 13.45.28 SET HEADSEP 107 13.45.29 SET HISTORY 107 13.45.30 SET INSTANCE 108 13.45.31 SET JSONPRINT 108 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page ix of xii
13.45.32 SET LINESIZE 109 13.45.33 SET LOBOFFSET 110 13.45.34 SET LOBPREFETCH 110 13.45.35 SET LOGSOURCE 111 13.45.36 SET LONG 111 13.45.37 SET LONGCHUNKSIZE 112 13.45.38 SET MARKUP 112 13.45.39 SET NEWPAGE 117 13.45.40 SET NULL 117 13.45.41 SET NUMFORMAT 117 13.45.42 SET NUMWIDTH 117 13.45.43 SET PAGESIZE 118 13.45.44 SET PAUSE 118 13.45.45 SET RECSEP 118 13.45.46 SET RECSEPCHAR 118 13.45.47 SET ROWLIMIT 119 13.45.48 SET ROWPREFETCH 120 13.45.49 SET SECUREDCOL 120 13.45.50 SET SERVEROUTPUT 121 13.45.51 SET SHIFTINOUT 123 13.45.52 SET SHOWMODE 124 13.45.53 SET SQLBLANKLINES 124 13.45.54 SET SQLCASE 125 13.45.55 SET SQLCONTINUE 125 13.45.56 SET SQLNUMBER 125 13.45.57 SET SQLPLUSCOMPATIBILITY 126 
13.45.57.1 SQL*Plus Compatibility Matrix 126 13.45.58 SET SQLPREFIX 127 13.45.59 SET SQLPROMPT 127 13.45.60 SET SQLTERMINATOR 128 13.45.61 SET STATEMENTCACHE 128 13.45.62 SET SUFFIX 129 13.45.63 SET TAB 129 13.45.64 SET TERMOUT 129 13.45.65 SET TIME 130 13.45.66 SET TIMING 130 13.45.67 SET TRIMOUT 130 13.45.68 SET TRIMSPOOL 131 13.45.69 SET UNDERLINE 131 13.45.70 SET VERIFY 131 13.45.71 SET WRAP 131 13.45.72 SET XMLOPTIMIZATIONCHECK 131 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page x of xii
13.45.73 SET XQUERY BASEURI 132 13.45.74 SET XQUERY ORDERING 132 13.45.75 SET XQUERY NODE 133 13.45.76 SET XQUERY CONTEXT 133 
13.46 SHOW 134 13.47 SHUTDOWN 140 13.48 SPOOL 142 13.49 START 143 13.50 STARTUP 144 13.51 STORE 149 13.52 TIMING 149 13.53 TTITLE 150 13.54 UNDEFINE 153 13.55 VARIABLE 153 13.56 WHENEVER OSERROR 161 13.57 WHENEVER SQLERROR 162 13.58 XQUERY 164 
Part IV SQL*Plus Appendixes 
A SQL*Plus Limits 
B SQL*Plus COPY Command 
B.1 COPY Command Syntax B-1 B.1.1 Terms B-1 B.1.2 Usage B-3 B.1.3 Examples B-3 
B.2 Copying Data from One Database to Another B-3 B.2.1 Understanding COPY Command Syntax B-4 B.2.2 About Controlling Treatment of the Destination Table B-5 B.2.3 About Interpreting the Messages that COPY Displays B-6 B.2.4 Specifying Another User's Table B-6 B.3 About Copying Data between Tables on One Database B-7 
C Obsolete SQL*Plus Commands 
C.1 SQL*Plus Obsolete Command Alternatives C-1 C.2 BTITLE (old form) C-2 C.3 COLUMN DEFAULT C-2 C.4 DOCUMENT C-2 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page xi of xii
C.5 NEWPAGE C-3 C.6 SET BUFFER C-3 C.7 SET COMPATIBILITY C-3 C.8 SET CLOSECURSOR C-4 C.9 SET DOCUMENT C-4 C.10 SET MAXDATA C-4 C.11 SET SCAN C-4 C.12 SET SPACE C-5 C.13 SET TRUNCATE C-5 C.14 TTITLE (old form) C-5 
D SQL*Plus Instant Client 
D.1 About Choosing the SQL*Plus Instant Client to Install D-1 D.1.1 Basic Instant Client D-1 D.1.2 Lightweight Instant Client D-1 
D.1.2.1 Lightweight SQL*Plus Instant Client Error with Unsupported Character Set D-2 D.2 List of Files Required for SQL*Plus Instant Client D-2 D.3 Installing SQL*Plus Instant Client by Downloading Installation Files from OTN D-3 D.4 Installing SQL*Plus Instant Client from the 21c Client Release Media D-4 D.5 Configuring SQL*Plus Instant Client D-4 D.6 About Connecting to a Database with SQL*Plus Instant Client D-6 D.7 AS SYSDBA or AS SYSOPER Connections with SQL*Plus Instant Client D-7 D.8 About Uninstalling Instant Client D-7 
D.8.1 Uninstalling SQL*Plus Instant Client D-8 D.8.2 Uninstalling the Complete Instant Client D-8 
Index 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page xii of xii
Preface 
The SQL*Plus (pronounced "sequel plus") User's Guide and Reference introduces SQL*Plus and its uses, and describes each SQL*Plus command. 
This preface contains these topics: 
• Audience 
• Related Documents 
• Conventions 
Audience 
The SQL*Plus User's Guide and Reference is intended for business and technical users and system administrators who perform the following tasks: 
• Develop and run batch scripts 
• Format, calculate on, store, print and create web output from query results 
• Examine table and object definitions 
• Perform database administration 
This document assumes a basic understanding of the SQL language. If you do not have familiarity with SQL, see the Oracle AI Database SQL Language Reference. If you plan to use PL/SQL with SQL*Plus, see the Oracle AI Database PL/SQL Language Reference. 
Related Documents 
For more information, see these Oracle resources: 
• Oracle AI Database PL/SQL Language Reference 
• Oracle AI Database SQL Language Reference 
• Oracle Call Interface Developer's Guide 
• Oracle AI Database Concepts 
• Oracle AI Database Administrator’s Guide 
• Oracle AI Database Backup and Recovery User’s Guide 
• Oracle AI Database Development Guide 
• Oracle XML DB Developer’s Guide 
• Oracle AI Database Globalization Support Guide 
• Oracle AI Database Heterogeneous Connectivity User's Guide 
• Oracle AI Database Upgrade Guide 
• Oracle AI Database Reference 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page i of ii
Preface 
• Oracle AI Database Performance Tuning Guide 
• Oracle AI Database Net Services Administrator's Guide 
• Pro*COBOL Developer's Guide 
• Pro*C/C++ Developer's Guide 
• Oracle Database installation and user's manuals for your operating system 
Many of the examples in this book use the sample schemas, which you need to download from the GitHub repository. See Oracle AI Database Sample Schemas for information on how these schemas were created and how you can use them yourself. 
Conventions 
The following text conventions are used in this document: 
Convention Meaning 
boldface Boldface type indicates graphical user interface elements associated with an action, or terms defined in text or the glossary. 
italic Italic type indicates book titles, emphasis, or placeholder variables for which you supply particular values. 
monospace Monospace type indicates commands within a paragraph, URLs, code in examples, text that appears on the screen, or text that you enter. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page ii of ii
Changes in This Release for Oracle AI Database SQL*Plus User's Guide and Reference 
This preface contains the changes in this book for Oracle AI Database 26ai. 
New Features 
This section lists new features introduced in SQL*Plus releases. 
SQL*Plus Release 26ai 
This section describes new features introduced in SQL*Plus in 26ai. 
• A new command, CONFIG, generates the config store JSON file from the tnsnames.ora file. CONFIG 
• A new command, ARGUMENT, customizes the input prompt and sets default values when parameters are not passed to the script. 
ARGUMENT 
• A new command, PING, pings the database or database network listener to check availability. 
PING 
• Display error details 
– A new command, OERR, allows users to see the detailed cause and action text for Oracle errors. 
OERR 
– A new command, SET ERRORDETAILS, displays the Oracle Error Help URL along with the cause and action details when any SQL, PL/SQL, or SQL*Plus statement fails 
during execution. 
SET ERRORDETAILS 
– The HELP command is enhanced to display error details, such as Cause, Action, and Parameters, for the provided error code. 
HELP 
• The DESCRIBE command is enhanced to display annotation information for columns that have associated annotations available. 
DESCRIBE 
• The SHOW CONNECTION command lists the Oracle Net Service Names present in the tnsnames.ora file and resolves the given net service name to the connection string. 
SHOW 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page i of ii
Changes in This Release for Oracle AI Database SQL*Plus User's Guide and Reference 
• Support for the SQL BOOLEAN data type 
– Added support for a new data type, BOOLEAN, in SQL statements. 
DESCRIBE 
– Enhanced the syntax of the COLUMN and the VARIABLE commands. 
COLUMN 
VARIABLE 
• Support for a new data type, VECTOR, in SQL*Plus. 
VARIABLE 
SQL*Plus Release 21c 
This section describes new features introduced in SQL*Plus in 21c. 
• The HISTORY command syntax has been enhanced. If N is omitted in the command, then RUN, EDIT or DELETE is executed on the most recent entry in the history list. 
• SET JSONPRINT is a new command that enables you to format JSON data. 
SQL*Plus Release 19c 
This section describes a new feature introduced in SQL*Plus in 19c. 
The Easy Connect syntax, used by applications to connect to Oracle Database, has been enhanced and is called Easy Connect Plus. 
Deprecated Features 
This section lists the deprecated features in Oracle AI Database release 26ai. 
Deprecation of FIPS Parameters 
Starting with Oracle AI Database 26ai, several parameters associated with FIPS_140 are deprecated. 
FIPS_140 in FIPS.ORA can be used to enable FIPS for all features starting with Oracle AI Database 26ai. The following FIPS parameters are deprecated: 
• SQLNET.ORA: FIPS_140 to enable FIPS for native network encryption 
• FIPS.ORA: SSLFIPS_140 to enable FIPS for TLS 
• Initialization parameter: DBFIPS_140 to enable FIPS for TDE and DBMS_CRYPTO 
Deprecation of Enterprise User Security (EUS) 
Enterprise User Security (EUS) is deprecated with Oracle AI Database 26ai. 
Oracle recommends that you migrate to using Centrally Managed Users (CMU). This feature enables you to directly connect with Microsoft Active Directory without an intervening directory service for enterprise user authentication and authorization to the database. If your Oracle Database is in the cloud, you can also choose to move to one of the newer integrations with a cloud identity provider. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page ii of ii
Introduction to SQL*Plus 
These instructions are to enable you to login and connect to a database after you have installed SQL*Plus. You can connect to the default database you created during installation, or to another existing Oracle database. 
• SQL*Plus Resources 
• SQL*Plus Overview 
• Certification 
• SQL*Plus Prerequisites 
• Starting SQL*Plus Command-line 
• About Starting SQL*Plus Instant Client 
• About Connecting to a Different Database 
• About Sample Schemas and SQL*Plus 
• Running your first Query 
• About Exiting SQL*Plus 
SQL*Plus Resources 
• Oracle Documentation Library at http://www.oracle.com/technetwork/. 
SQL*Plus Overview 
SQL*Plus is an interactive and batch query tool that is installed with every Oracle Database installation. It has a command-line user interface. 
There is also the SQL*Plus Instant Client which is a standalone command-line interface available on platforms that support the OCI Instant Client. SQL*Plus Instant Client connects to any available Oracle database, but does not require its own Oracle database installation. See the Oracle Call Interface Programmer's Guide for more information on the OCI Instant Client. 
SQL*Plus has its own commands and environment, and it provides access to the Oracle Database. It enables you to enter and execute SQL, PL/SQL, SQL*Plus and operating system commands to perform the following: 
• Format, perform calculations on, store, and print from query results 
• Examine table and object definitions 
• Develop and run batch scripts 
• Perform database administration 
You can use SQL*Plus to generate reports interactively, to generate reports as batch processes, and to output the results to text file, to screen, or to HTML file for browsing on the Internet. You can generate reports dynamically using the HTML output facility of SQL*Plus. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page i of vii
Introduction to SQL*Plus 
Who Can Use SQL*Plus 
The SQL*Plus, SQL, and PL/SQL command languages are powerful enough to serve the needs of users with some database experience, yet straightforward enough for new users who are just learning to work with the Oracle Database. 
The SQL*Plus language is easy to use. For example, to rename a column labeled 
LAST_NAME with the heading "Family Name", enter the command: 
COLUMN LAST_NAME HEADING 'Family Name' 
Similarly, to list column definitions for the EMPLOYEES table, enter the command: 
DESCRIBE EMPLOYEES 
How to Use the SQL*Plus Guide 
This guide provides information about SQL*Plus that applies to all operating systems. It also includes some Windows and UNIX specific information. Some aspects of SQL*Plus may differ on each operating system. Operating system specific details are covered in the Oracle Database Installation Guide provided for your system. Use these operating system specific guides with this SQL*Plus User's Guide and Reference. 
Throughout this guide, examples showing how to enter commands use a common command syntax and a common set of sample tables. The tables are described in "About Sample Schemas and SQL*Plus". 
SQL*Plus Command-line Architecture 
SQL*Plus command-line uses a two-tier model comprising: 
• Client (command-line user interface). 
• Database (Oracle Database). 
The two tiers may be on the same computer. 
SQL*Plus Client 
The command-line user interface is the character-based terminal implementation. 
Oracle Database 
Oracle Database Net components provide communication between the SQL*Plus Client and Oracle Database. 
Certification 
SQL*Plus is certified against the operating systems set out in the operating-system specific Oracle Database documentation. 
SQL*Plus is certified against all the supported versions of Oracle Database and Oracle Server. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page ii of vii
Introduction to SQL*Plus 
SQL*Plus Prerequisites 
SQL*Plus is a component of Oracle Database. SQL*Plus is installed by default when you install the Oracle Database. 
Some aspects of Oracle Database and SQL*Plus differ from one computer and operating system to another. These topics are discussed in the Oracle Database Installation Guide for each operating system that SQL*Plus supports. 
What is necessary before you can run SQL*Plus? 
• Install Oracle Database or Oracle Client. See the Oracle Database Installation Guide for your operating system available at http://www.oracle.com/technetwork/. 
• Obtain an Oracle Database login username and password during installation or from your Database Administrator. See Login Username and Password. 
• Ensure a sample database is installed and that you have a login username and password for it. See About Sample Schemas and SQL*Plus. 
• Create a default database during installation or obtain the connection identifier for the Oracle Database you want to connect to from your Database Administrator. See About Connecting to a Database. 
• Ensure the database you want to connect to is started. See the STARTUP command. SQL*Plus Date Format 
The default date format in SQL*Plus is determined by the database NLS_DATE_FORMAT parameter and may use a date format displaying two digit years. You can use the SQL TO_CHAR function, or the SQL*Plus COLUMN FORMAT command in your SELECT statements to control the way dates are displayed in your report. 
Starting SQL*Plus Command-line 
The SQL*Plus executable is usually installed in $ORACLE_HOME/bin, which is usually included in your operating system PATH environment variable. You may need to change directory to the $ORACLE_HOME/bin directory to start SQL*Plus. 
In the following examples, you are prompted to enter the database account password. 
An example using an Easy Connection identifier to connect to the HR schema in the MYDB database running on mymachine is: 
sqlplus hr@\"//mymachine.mydomain:port/MYDB\" 
An example using a Net Service Name is: 
sqlplus hr@MYDB 
Net Service Names can be stored in several places, including Oracle Names. See the Net Services Reference Guide for more information. 
If you want to use Net Service Names configured in a local Oracle Net tnsnames.ora file, then set the environment variable TNS_ADMIN to the directory containing the tnsnames.ora file. For example, on UNIX, if your tnsnames.ora file is in /home/user1 and it defines the Net Service Name MYDB2: 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page iii of vii
TNS_ADMIN=/home/user1 export TNS_ADMIN sqlplus hr@MYDB2 
Introduction to SQL*Plus 
This example assumes the ORACLE_HOME environment variable is set, and 
the $ORACLE_HOME/network/admin/tnsnames.ora or 
ORACLE_HOME\network\admin\tnsnames.ora file defines the Net Service Name MYDB3: sqlplus hr@MYDB3 
The TWO_TASK (on UNIX) or LOCAL (on Windows) environment variable can be set to a connection identifier. This removes the need to explicitly enter the connection identifier whenever a connection is made in SQL*Plus or SQL*Plus Instant Client. This UNIX example connects to the database known as MYDB4: 
TNS_ADMIN=/home/user1 
export TNS_ADMIN 
TWO_TASK=MYDB4 
export TWO_TASK 
sqlplus hr 
To start SQL*Plus and connect to the default database 
1. Open a UNIX or a Windows terminal and enter the SQL*Plus command: 
sqlplus 
2. When prompted, enter your Oracle Database username and password. If you do not know your Oracle Database username and password, ask your Database Administrator. 
3. Alternatively, enter the SQL*Plus command in the form: 
sqlplus username 
You are prompted to enter your password. 
4. SQL*Plus starts and connects to the default database. 
Now you can start entering and executing SQL, PL/SQL and SQL*Plus statements and commands at the SQL> prompt. 
Example 1 To start SQL*Plus and connect to a database other than the default Open a UNIX or a Windows terminal and enter the SQL*Plus command: 
sqlplus username@connect_identifier 
You are prompted to enter your password. 
Using SQL*Plus from Oracle Instant Client Package 
SQL*Plus can be installed from Oracle Instant Client packages. For information about using it, see Starting SQL*Plus Command-line. 
Because SQL*Plus Instant Client does not include a database, it is always 'remote' from any database server. To connect to a database you must specify the database using an Oracle Net connection identifier. 
If TNS_ADMIN is not set, then an operating system dependent set of directories is examined to find tnsnames.ora. This search path includes looking in the directory specified by the ORACLE_HOME environment variable for network/admin/tnsnames.ora. This is the only reason to set the ORACLE_HOME environment variable for SQL*Plus Instant Client. If 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page iv of vii
Introduction to SQL*Plus 
ORACLE_HOME is set when running Instant Client applications, it must be set to a directory that exists. 
About Connecting to a Different Database 
From an existing command-line session, enter a CONNECT command in the form: 
SQL> connect username@connect_identifier 
You are prompted to enter your password. 
About Sample Schemas and SQL*Plus 
Sample schemas are no longer included with the Oracle Database. Starting from Oracle Database 21c, you need to download sample schemas from the GitHub repository. Examples in this guide use the EMP_DETAILS_VIEW view of the Human Resources (HR) sample schema. This schema contains personnel records for a fictitious company. To view column details for the view, EMP_DETAILS_VIEW, enter 
DESCRIBE EMP_DETAILS_VIEW 
For more information about the sample schemas, see the Oracle Database Sample Schemas guide. 
Unlocking the Sample Tables 
The Human Resources (HR) Sample Schema is not installed as part of the default Oracle Database installation. Starting from Oracle Database 21c, you need to download the sample schemas from the GitHub repository. The HR account is locked by default. 
You must unlock the HR account before you can use the HR sample schema. To unlock the HR account, log in as the SYSTEM user and enter the following command, where 
your_password is the password you want to define for the user HR: 
ALTER USER HR IDENTIFIED BY your_password ACCOUNT UNLOCK; 
For further information about unlocking the HR account, see the Oracle Database Sample Schemas guide. The HR user is primarily to enable you to access the HR sample schema and is necessary to enable you to run the examples in this guide. 
Each table in the database is "owned" by a particular user. You may want to have your own  copies of the sample tables to use as you try the examples in this guide. To get your own copies of the HR tables, see your DBA or see the Oracle Database Sample Schemas guide, or you can create the HR tables with the script HR_MAIN.SQL which is located in the following directory on UNIX: 
$ORACLE_HOME/demo/schema/human_resources/hr_main.sql 
And on the following directory on Windows: 
ORACLE_HOME\DEMO\SCHEMA\HUMAN_RESOURCES\HR_MAIN.SQL 
To create the HR tables from command-line SQL*Plus, do the following: 
1. Ask your DBA for your Oracle Database account username and password. 
2. Login to SQL*Plus. 
3. On UNIX, enter the following command at the SQL*Plus prompt: 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page v of vii
Introduction to SQL*Plus 
SQL> @?/DEMO/SCHEMA/HUMAN_RESOURCES/HR_MAIN.SQL 
On Windows, enter the following command at the SQL*Plus prompt: 
SQL> @?\DEMO\SCHEMA\HUMAN_RESOURCES\HR_MAIN.SQL 
To remove the sample tables, perform the same steps but substitute HR_DROP.SQL for HR_MAIN.SQL. 
Running your first Query 
You can use the DESCRIBE command to describe a database object, EMP_DETAILS_VIEW, as shown in the following example: 
DESCRIBE EMP_DETAILS_VIEW 
The following output is displayed: 

You can rename the column headings and select data from the EMP_DETAILS_VIEW as shown in the following example: 
COLUMN FIRST_NAME HEADING "First Name" 
COLUMN LAST_NAME HEADING "Family Name" 
SELECT FIRST_NAME, LAST_NAME 
FROM EMP_DETAILS_VIEW 
WHERE LAST_NAME LIKE 'K%'; 
The following output is displayed: 

SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page vi of vii
About Exiting SQL*Plus 
You can use the EXIT command to exit SQL*Plus. 
SQL*Plus® User's Guide and Reference 
G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
Introduction to SQL*Plus 
January 22, 2026 
Page vii of vii
Part I 
Introduction to SQL*Plus 
Part 1 provides the information you need to get started with SQL*Plus. It describes the command-line user interface, provides configuration information and information you need to log in and run SQL*Plus. 
Part 1 contains the following chapters: 
• SQL*Plus User Interface 
• Configuring SQL*Plus 
• Starting SQL*Plus 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 1 of 1
1 
SQL*Plus User Interface 
This chapter describes the SQL*Plus command-line user interface. It contains the following topics: 
• About The Command-line Screen 
• Changing the Command-line Font and Font Size 
1.1 About the Command-line Screen 
The SQL*Plus command-line interface is standard on all operating systems. 
When SQL*Plus starts, it displays the date and time, the SQL*Plus version and copyright information before the SQL*Plus prompt appears. The default prompt for SQL*Plus command line is: 
SQL>  
1.2 Changing the Command-line Font and Font Size 
In Windows, from a Command Prompt, open the Command Prompt Properties dialog to set the font and font size used in the SQL*Plus command-line interface. 
To Change the Command-line Interface Font and Font Size 
1. Right click in the command-line interface title bar. 
2. Click Properties. The Window Preview box displays the current window's relative size on your monitor based on your font and font size selections. The Selected Font: box displays a sample of the current font. 
3. Click the Font tab. 
4. Select the font size to use from the Size box. Raster font sizes are shown as width by height in pixels. TrueType font sizes are shown as height in pixels. 
5. Select the font to use from the Font box. 
6. Select the Bold Fonts check box to use a bold version of the font. 
For more information about changing Command Prompt properties, see Windows Help or click Help in the Command Prompt Properties dialog. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 1 of 1
2 
Configuring SQL*Plus 
This chapter explains how to configure your SQL*Plus command-line environment. It has the following topics: 
• SQL*Plus Environment Variables 
• SQL*Plus Configuration 
2.1 SQL*Plus Environment Variables 
These environment variables specify the location or path of files used by SQL*Plus. For other environment variables that influence the behavior of SQL*Plus, see the Oracle Database Administrator's Reference. 
Table 2-1 Parameters or Environment Variables influencing SQL*Plus 
Parameter or Variable Description 
LD_LIBRARY_PATH Environment variable to specify the path used to search for libraries on UNIX and Linux. The environment variable may have a different 
name on some operating systems, such as DYLD_LIBRARY_PATH on 
Apple Mac OS, LIBPATH on IBM/AIX-5L, and SHLIB_PATH on HP 
UX. Not applicable to Windows operating systems. 
Example 
$ORACLE_HOME/lib  
LOCAL Windows environment variable to specify a connection string. Performs the same function as TWO_TASK on UNIX. 
NLS_LANG Environment variable to specify globalization behavior. 
Example 
american_america.utf8 
ORACLE_HOME Environment variable to specify where SQL*Plus is installed. It is also used by SQL*Plus to specify where message files are located. 
Examples: 
d:\oracle\10g 
/u01/app/oracle/product/v10g 
ORA_EDITION Environment variable to specify the database edition to use. If you specify the edition with the CONNECT or SQLPLUS command option, 
edition=value, it is used instead of ORA_EDITION. If no edition is 
specified in either the CONNECT or SQLPLUS command option, or in 
ORA_EDITION, SQL*Plus connects to the default edition. 
When ORA_EDITION is set, a subsequent STARTUP command in the 
session results in an ORA-38802 error. To correct this, you must unset 
ORA_EDITION, then reconnect and shutdown the database, then 
start the database again. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 1 of 7
Chapter 2 
SQL*Plus Environment Variables 
Table 2-1 (Cont.) Parameters or Environment Variables influencing SQL*Plus 
Parameter or Variable Description 
ORA_NLS10 Environment variable to specify the locations of the NLS data and the user boot file in SQL*Plus 10.2. The default location 
is $ORACLE_HOME/nls/data. In a system with both Oracle9i and 10g, 
or a system under version upgrade, you should set ORA_NLS10 for 
Oracle 10g and set ORA_NLS33 for 9i. The default NLS location in 9i 
was $ORACLE_HOME/common/nls/admin/data. 
ORACLE_PATH Environment variable to specify the location of SQL scripts. If SQL*Plus cannot find the file in ORACLE_PATH, or if ORACLE_PATH 
is not set, it searches for the file in the current working directory. 
Not applicable to Windows 
ORACLE_SID Environment variable to specify the database instance, optional 
PATH Environment variable to specify the path to search for executables, and DLLs in Windows. Typically includes ORACLE_HOME/bin 
SQLPATH Environment variable or Windows registry entry to specify the location of SQL scripts. SQL*Plus searches for SQL scripts, including login.sql, 
in the directories specified by SQLPATH. SQLPATH is a colon 
separated list of directories. There is no default value set in UNIX 
installations. 
In Windows, SQLPATH is defined in a registry entry during installation. 
For more information about the SQLPATH registry entry, see  
SQLPATH Registry Entry. 
TNS_ADMIN Environment variable to specify the location of the tnsnames.ora file. If not specified, $ORACLE_HOME/network/admin is used 
Example 
h:\network  
/var/opt/oracle 
TWO_TASK UNIX environment variable to specify a connection string. 
Connections that do not specify a database will connect to the 
database specified in TWO_TASK. 
Example 
TWO_TASK=MYDB 
export TWO_TASK 
sqlplus hr 
is the same as: 
sqlplus hr@MYDB 
2.1.1 SQLPATH Registry Entry 
The SQLPATH registry entry specifies the location of SQL scripts. SQL*Plus searches for SQL scripts in the current directory and then in the directories specified by the SQLPATH registry entry, and in the subdirectories of SQLPATH directories. 
The HKEY_LOCAL_MACHINE\SOFTWARE\ORACLE\HOME0 registry subkey (or the HOMEn directory for the associated ORACLE_HOME) contains the SQLPATH registry entry. SQLPATH is created with a default value of ORACLE_HOME\DBS. You can specify any directories on any drive as valid values for SQLPATH. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 2 of 7
Chapter 2 
SQL*Plus Configuration 
When setting the SQLPATH registry entry, you can concatenate directories with a semicolon (;). For example: 
c:\oracle\ora12\database;c:\oracle\ora12\dbs 
See the Registry Editor's help system for instructions on how to edit the SQLPATH registry entry. 2.2 SQL*Plus Configuration 
You can set up your SQL*Plus environment to use the same settings with each session. There are two operating system files to do this: 
• The Site Profile file, glogin.sql, for site wide settings. 
• Additionally, the User Profile, login.sql, sets user specific settings. 
The exact names of these files is system dependent. 
Note 
The Site Profile and User Profile files are run after a successful Oracle Database 
connection from a SQLPLUS or CONNECT command, or where /NOLOG is specified.The 
Site Profile and User Profile files are not run when you switch to another PDB using 
ALTER SESSION SET CONTAINER. 
Some privileged connections may generate errors if SET SERVEROUTPUT or SET APPINFO commands are put in the Site Profile or User Profile. 
The following tables show the profile scripts, and some commands and settings that affect the Command-line user interface. 
Table 2-2 Profile Scripts affecting SQL*Plus User Interface Settings 
This script ... is run in the Command-line... 
Site Profile (glogin.sql) 
Can contain any content that can 
be included in a SQL*Plus script, 
such as system variable settings or 
other global settings the DBA 
wants to implement. 
User Profile (login.sql) 
Can contain any content that can 
be included in a SQL*Plus script, 
but the settings are only applicable 
to the user's sessions. 
SQL*Plus® User's Guide and Reference 
G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
After successful Oracle Database connection from a SQLPLUS or CONNECT command. 
Where /NOLOG is specified. 
Immediately after the Site Profile. 
January 22, 2026 
Page 3 of 7
Chapter 2 
SQL*Plus Configuration 
Table 2-3 Commands in Profile scripts affecting SQL*Plus User Interface Settings 
In a profile script, this 
command ... 
SET SQLPLUSCOMPAT[IBILITY] 
{x.y[.z]} 
Also see the SQL*Plus 
Compatibility Matrix. 
SQLPLUS command  
COMPATIBILITY Option 
SQLPLUS command RESTRICT 
Option 
2.2.1 Site Profile 
affects the Command-line by ... 
Setting the SQL*Plus compatibility mode to obtain the behavior the DBA wants for this site. 
As for SET SQLPLUSCOMPATIBILITY but set with the SQLPLUS command COMPATIBILITY option. 
Starting SQL*Plus with the RESTRICT option set to 3 prevents the User Profile script from being read. 
A Site Profile script is created during installation. It is used by the database administrator to configure site-wide behavior for SQL*Plus Command-line connections. The Site Profile script installed during installation is an empty script. 
The Site Profile script is generally named glogin.sql. SQL*Plus executes this script whenever a user starts a SQL*Plus session and successfully establishes the Oracle Database connection. 
The Site Profile enables the DBA to set up site wide SQL*Plus environment defaults for all users of a particular SQL*Plus installation 
Users cannot directly access the Site Profile. 
2.2.1.1 Default Site Profile Script 
The Site Profile script is $ORACLE_HOME/sqlplus/admin/glogin.sql in UNIX, and 
ORACLE_HOME\sqlplus\admin\glogin.sql in Windows. If a Site Profile already exists at this location, it is overwritten when you install SQL*Plus. If SQL*Plus is removed, the Site Profile script is deleted. 
2.2.2 User Profile 
For SQL*Plus command-line connections, SQL*Plus also supports a User Profile script. The User Profile is executed after the Site Profile and is intended to allow users to specifically customize their session. The User Profile script is generally named login.sql. SQL*Plus searches for the directories you specify with the ORACLE_PATH environment variable. SQL*Plus searches this colon-separated list of directories and their subdirectories in the order they are listed. 
Note 
SQL*Plus will no longer search for login.sql in the current directory. 
You can add any SQL commands, PL/SQL blocks, or SQL*Plus commands to your user profile. When you start SQL*Plus, it automatically searches for your user profile and runs the commands it contains. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 4 of 7
Chapter 2 
SQL*Plus Configuration 
2.2.2.1 Modifying Your LOGIN File 
You can modify your LOGIN file just as you would any other script. The following sample User Profile script shows some modifications that you could include: 
-- login.sql 
-- SQL*Plus user login startup file. 
-- 
-- This script is automatically run after glogin.sql 
-- 
-- To change the SQL*Plus prompt to display the current user, 
-- connection identifier and current time. 
-- First set the database date format to show the time. 
ALTER SESSION SET nls_date_format = 'HH:MI:SS'; 
-- SET the SQLPROMPT to include the _USER, _CONNECT_IDENTIFIER 
-- and _DATE variables. 
SET SQLPROMPT "_USER'@'_CONNECT_IDENTIFIER _DATE> " 
-- To set the number of lines to display in a report page to 24. 
SET PAGESIZE 24 
-- To set the number of characters to display on each report line to 78. 
SET LINESIZE 78 
-- To set the number format used in a report to $99,999. 
SET NUMFORMAT $99,999 
See Also 
• SET command for more information on these and other SET command variables you may wish to set in your SQL*Plus LOGIN file. 
• About Using Predefined Variables for more information about predefined variables. 
2.2.3 Storing and Restoring SQL*Plus System Variables 
From the Command-line you can store the current SQL*Plus system variables in a script with the STORE command. If you alter any variables, this script can be run to restore the original values. This is useful if you want to reset system variables after running a report that alters them. You could also include the script in your User Profile script so that these system variables are set each time you start SQL*Plus. 
To store the current setting of all system variables, enter 
STORE SET file_name 
Enter a file name and file extension, or enter only the file name to use the default 
extension .SQL. You can use the SET SUF[FIX] {SQL | text} command to change the default file extension. 
2.2.3.1 Restoring the System Variables 
To restore the stored system variables, enter 
START file_name 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 5 of 7
Chapter 2 
SQL*Plus Configuration 
If the file has the default extension (as specified by the SET SUF[FIX] {SQL | text} command), you do not need to add the period and extension to the file name. 
You can also use the @ (at sign) or the @@ (double at sign) commands to run the script. Created file plusenv 
Now the value of any system variable can be changed: 
SHOW PAGESIZE 
PAGESIZE 24 
SET PAGESIZE 60 
SHOW PAGESIZE 
PAGESIZE 60 
The original values of system variables can then be restored from the script: 
START plusenv 
SHOW PAGESIZE 
PAGESIZE 24 
Example 2-1 Storing and Restoring SQL*Plus System Variables 
To store the current values of the SQL*Plus system variables in a new script "plusenv.sql": STORE SET plusenv 
2.2.4 About Installing Command-line Help 
Command-line help is usually installed during Oracle Database installation. If not, the database administrator can create the SQL*Plus command-line help tables and populate them with SQL*Plus help data by running a supplied SQL script from SQL*Plus. 
The database administrator can also remove the SQL*Plus command-line help tables by running a SQL script from SQL*Plus. 
Before you can install or remove SQL*Plus help, ensure that: 
• SQL*Plus is installed. 
• The ORACLE_HOME environment variable is set. 
• The SQL*Plus help script files exist: 
– HLPBLD.SQL - to drop and create new help tables. 
– HELPDROP.SQL - to drop existing help tables. 
– HELPUS.SQL - to populate the help tables with the help data. 
2.2.4.1 Running the hlpbld.sql Script to Install Command-line Help Run the provided SQL script, HLPBLD.SQL, to load command-line help. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 6 of 7
Chapter 2 
SQL*Plus Configuration 
1. Log in to SQL*Plus as the SYSTEM user with: 
SQLPLUS SYSTEM 
You are prompted to enter the password you have defined for the SYSTEM user. 
2. In UNIX run the SQL script, HLPBLD.SQL, from SQL*Plus with: 
@$ORACLE_HOME/sqlplus/admin/help/hlpbld.sql helpus.sql 
In Windows run the SQL script, HLPBLD.SQL, from SQL*Plus with: 
@%ORACLE_HOME%\SQLPLUS\ADMIN\HELP\HLPBLD.SQL HELPUS.SQL 
The HLPBLD.SQL script creates and loads the help tables. 
2.2.4.2 Running the helpdrop.sql Script to Remove Command-line Help Run the provided SQL script, HELPDROP.SQL, to remove the command-line help. 
1. Log in to SQL*Plus as the SYSTEM user with: 
SQLPLUS SYSTEM 
You are prompted to enter the password you have defined for the SYSTEM user. 
2. In UNIX run the SQL script, HELPDROP.SQL, from SQL*Plus with: 
@$ORACLE_HOME/sqlplus/admin/help/helpdrop.sql 
In Windows run the SQL script, HELPDROP.SQL, from SQL*Plus with: 
@%ORACLE_HOME\SQLPLUS\ADMIN\HELP\HELPDROP.SQL 
The HELPDROP.SQL script drops the help tables, and then disconnects. 
2.2.5 About Configuring Oracle Net Services 
If you plan to connect to a database other than the default, whether on the same computer or another computer, you need to ensure that Oracle Net is installed, and the database listener is configured and running. Oracle Net services are used by SQL*Plus. 
Oracle Net services and the database listener are installed by default during Oracle Database installation. For further information about installing and configuring Oracle Net, see the Oracle Database documentation at http://www.oracle.com/technology/documentation. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 7 of 7
3 
Starting SQL*Plus 
This chapter describes how to start, login, and connect to a database, how to get help, and how to exit SQL*Plus. 
Specific topics discussed are: 
• Login Username and Password 
• About Connecting to a Database 
• About Starting SQL*Plus 
• About Exiting SQL*Plus Command-line 
• SQLPLUS Program Syntax 
3.1 Login Username and Password 
When you start SQL*Plus, you need a username and password to login to an Oracle Database schema. Your username and password identify you as an authorized user of the Oracle Database schema. 
The database administrator (DBA) is responsible for creating your database account with the necessary privileges and giving you the username and password that enables you to access your account. 
Default logins are created and you are prompted for associated passwords during Oracle Database installation. Some of the default login usernames created are: 
• SYS 
• SYSTEM 
• HR 
Logins are created and displayed in messages during Oracle Database installation. 
For further information about the default logins, see Types of Oracle Database Users. 
Once you have logged in, you can connect under a different username using the CONNECT command. The username and password must be valid for the database. For example, to connect the username TODD to the default database using the password FOX, you could enter 
CONNECT TODD 
You are prompted to enter the password, FOX. 
In the command-line interface, if you omit the username and password, SQL*Plus prompts you for them. Because CONNECT first disconnects you from your current database, you will be left unconnected to any database if you use an invalid username and password in your CONNECT command. 
If you log on or connect as a user whose account has expired, you are prompted to change your password before you can connect. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 1 of 14
Chapter 3 
About Connecting to a Database 
If an account is locked, a message is displayed and connection as this user is not permitted until the account is unlocked by your DBA. 
You can use the DISCONNECT command to disconnect from a database without leaving SQL*Plus. 
3.1.1 Secure External Password Store 
As a command-line alternative for large-scale deployments where applications use password credentials to connect to databases, it is possible to store such credentials in a client-side Oracle wallet. An Oracle wallet is a secure software container that is used to store 
authentication and signing credentials. 
Storing database password credentials in a client-side Oracle wallet eliminates the need to embed usernames and passwords in application code, batch jobs, or scripts. This reduces the risk of exposing passwords in the clear in scripts and application code, and simplifies maintenance because you need not change your code each time usernames and passwords change. In addition, not having to change application code also makes it easier to enforce password management policies for these user accounts. 
When you configure a client to use the external password store, applications can use the following syntax to connect to databases that use password authentication: 
CONNECT /@database_alias 
Note that you need not specify database login credentials in this CONNECT statement. Instead your system looks for database login credentials in the client wallet. 
See Also 
Oracle Database Administrator's Guide for information about configuring your client to use secure external password store and for information about managing credentials in it. 
3.1.2 Expired Password 
In the command-line interface, if your password has expired, SQL*Plus prompts you to change it when you attempt to log in. You are logged in once you successfully change your password. 
3.1.3 About Changing your Password 
In the command-line interface, you can change your password with the PASSWORD 
command. See PASSWORD. 
3.2 About Connecting to a Database 
You must connect to an Oracle Database (instance) before you can query or modify data in that database. You can connect to the default database and to other databases accessible through your network. To connect to another database over a network, both databases must have Oracle Net configured, and have compatible network drivers. You must enter either a connection identifier or a net service name to connect to a database other than the default. 
The connection identifier or net service name is entered: 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 2 of 14
Chapter 3 
About Connecting to a Database 
• as an argument to the SQL*Plus Program Syntax when starting a command-line session. 
• as an argument to the CONNECT command from a current session. For detailed usage, see Accessing a Container in a CDB in the Oracle Database Administrator's Guide. 
3.2.1 Easy Connection String 
The easy or abbreviated connection identifier has the syntax: 
[//]host[:port][/service_name] 
Example 3-1 Start a command-line session to the sales database using an easy connection string 
sqlplus hr@\"sales-server:1521/sales.us.example.com\" 
Example 3-2 CONNECT to the sales database using an easy connection string When the password is omitted, the connect string needs to be quoted. 
connect hr@"sales-server:1521/sales.us.example.com" 
The easy connection string can be used wherever you can use a full connection identifier, or a net service name. The easy syntax is less complex, and no tnsnames.ora entry is required. 
3.2.2 Net Service Name 
Your DBA is responsible for creating the databases you use and defining net service names for them in the tnsnames.ora file. 
A net service name definition in the tnsnames.ora file has the syntax: 
net_service_name = 
 (DESCRIPTION = 
 (ADDRESS = (PROTOCOL = tcp)(HOST = host)(PORT = port)) 
 (CONNECT_DATA = 
 (SERVICE_NAME = service_name) 
 ) 
 )  
To use a net service name (alias), it must have an entry in the tnsnames.ora file on the machine running SQL*Plus. An entry in tnsnames.ora is not required if you use a connection identifier. 
Example 3-3 The tnsnames.ora entry for the sales database 
SALES1 = 
 (DESCRIPTION = 
 (ADDRESS=(PROTOCOL=tcp)(HOST=sales-server)(PORT=1521) ) 
 (CONNECT_DATA= 
 (SERVICE_NAME=sales.us.example.com)  
 )  
 ) 
Example 3-4 Start a command-line session to the sales database using the net service name 
SQLPLUS hr@SALES1 
See Configuration Parameters and Configuration and Administration of Oracle Net Services for more information about database connections and net service name definitions. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 3 of 14
Chapter 3 
About Starting SQL*Plus 
3.2.3 Full Connection Identifier 
Depending on your configuration, use the full connection identifier syntax like: 
(DESCRIPTION= 
(ADDRESS=(PROTOCOL=tcp)(HOST=host)(PORT=port) ) 
(CONNECT_DATA= 
(SERVICE_NAME=service_name) ) ) 
The SERVICE_NAME is the global database name entered during database creation. It combines a database name with a domain name. For example, the SERVICE_NAME 
sales.us.example.com has a database name of sales and a domain of us.example.com. 
An INSTANCE_NAME is the name you give to the database instance during creation. It defaults to the SID you entered during database creation. 
An Oracle System Identifier (SID) identifies a specific Oracle release 8.0 database instance. You can optionally use an INSTANCE_NAME in place of the SERVICE_NAME phrase. 
Use a SID in place of the SERVICE_NAME when connecting to an Oracle release 8.0 or earlier database. 
Example 3-5 Full connection identifier for SALES1 
SQLPLUS hr@\"(DESCRIPTION= 
(ADDRESS=(PROTOCOL=tcp)(HOST=sales-server)(PORT=1521) ) 
(CONNECT_DATA= 
(SERVICE_NAME=sales.us.example.com) ) )\" 
3.2.4 Connectionless Session with /NOLOG 
In the command-line interface, it is possible to start SQL*Plus without connecting to a database. This is useful for performing some database administration tasks, writing 
transportable scripts, or to use SQL*Plus editing commands to write or edit scripts. 
You use the /NOLOG argument to the SQLPLUS command to start a connectionless command-line session. After SQL*Plus has started you can connect to a database with the CONNECT command. 
Example 3-6 Start a connectionless SQL*Plus session with /NOLOG 
SQLPLUS /NOLOG  
3.3 About Starting SQL*Plus 
If you are connecting to a remote Oracle database, make sure your Oracle Net software is installed and working properly. For more information, see Testing and Troubleshooting Oracle Net Services. 
When you start a SQL*Plus command-line session, and after a CONNECT command in that session, the site profile, glogin.sql, and the user profile file, login.sql, are processed: 
• After SQL*Plus starts and connects, and prior to displaying the first prompt. 
• After SQL*Plus starts and connects, and prior to running a script specified on the command line. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 4 of 14
Chapter 3 
About Starting SQL*Plus 
• Prior to the first prompt when /NOLOG is specified on the command line and no connection is made. 
The site profile file, glogin.sql is processed first, then the user profile file, login.sql. 
3.3.1 About Starting Command-line SQL*Plus 
To begin using SQL*Plus, you must first understand how to start and stop SQL*Plus. 
1. Make sure that SQL*Plus has been installed on your computer. 
2. Log on to the operating system (if required). 
3. Enter the command, SQLPLUS, and press Return. 
Note 
Some operating systems expect you to enter commands in lowercase letters. If 
your system expects lowercase, enter the SQLPLUS command in lowercase. 
SQLPLUS 
SQL*Plus displays its version number, the current date, and copyright information, and prompts you for your username (the text displayed on your system may differ slightly): 
SQL*Plus: Release 23.26.1.0.0 - Production on Mon Jan 19 11:55:34 2026 
Version 23.26.1.0.0 
Copyright (c) 1982, 2025, Oracle. All rights reserved. 
4. Enter your username and press Return. SQL*Plus displays the prompt "Enter password:". 
5. Enter your password and press Return again. For your protection, your password does not appear on the screen. 
Note 
If your password contains the "@" character, then the password must be enclosed 
in double quotes, and the quotes must be escaped using backslash (\). 
The process of entering your username and password is called logging in. SQL*Plus 
displays the version of Oracle Database to which you connected and the versions of 
available tools such as PL/SQL, and the local time of the last time you logged on. 
SQL*Plus: Release 23.26.1.0.0 - Production on Wed Jan 21 12:19:11 2026 
Version 23.26.1.0.0 
Copyright (c) 1982, 2025, Oracle. All rights reserved. 
Last Successful login time: Wed Jan 21 2026 12:19:04 +00:00 
Connected to: 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 5 of 14
Chapter 3 
About Exiting SQL*Plus Command-line 
Oracle AI Database 26ai Enterprise Edition Release 23.26.1.0.0 - Production Version 23.26.1.0.0 
Next, SQL*Plus displays the SQL*Plus command prompt: 
SQL> 
The SQL*Plus command prompt indicates that SQL*Plus is ready to accept your 
commands. 
If SQL*Plus does not start, you should see a message to help you correct the problem. Example 3-7 Starting SQL*Plus 
This example shows you how to start SQL*Plus: 
3.3.2 About Getting Command-line Help 
To access command-line help for SQL*Plus commands, type HELP or ? followed by the command name at the SQL command prompt or in the iSQL*Plus Workspace Input area. See the HELP command for more information. For example: 
HELP ACCEPT 
To display a list of SQL*Plus commands, type HELP followed by either TOPICS or INDEX. HELP TOPICS displays a single column list of SQL*Plus commands. HELP INDEX displays a four column list of SQL*Plus commands which fits in a standard screen. For example: 
HELP INDEX 
3.4 About Exiting SQL*Plus Command-line 
If you cannot log in to SQL*Plus because your username or password is invalid or for some other reason, SQL*Plus returns an error status equivalent to an EXIT FAILURE command. See the EXIT command for further information. 
When you are done working with SQL*Plus and wish to return to the operating system, enter EXIT or QUIT at the SQL*Plus prompt, or enter the end of file character, Ctrl+D on UNIX or Ctrl+Z on Windows. 
SQL*Plus displays the version of Oracle Database from which you disconnected and the versions of tools available through SQL*Plus before you return to the operating system prompt. 
3.5 SQL*Plus Program Syntax 
You use the SQLPLUS command at the operating system prompt to start command-line SQL*Plus: 
SQLPLUS [ [Options] [Logon|/NOLOG] [Start] ] 
where: Options has the following syntax: 
 -H[ELP]|-V[ERSION] 
 |[[-C[OMPATIBILITY] {x.y[.z]] [–F[ast]] [-M[ARKUP] markup_option] [-L[OGON]]  
 [-NOLOGINTIME] [-P <connect identifier>] [-R[ESTRICT] {1|2|3}] [-S[ILENT]]] 
and markup_option consists of: 
• csv_option 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 6 of 14
Chapter 3 
SQL*Plus Program Syntax 
• html_option 
csv_option has the following syntax: 
CSV {ON|OFF} [DELIMI[TER] character] [QUOTE {ON|OFF}] 
html_option has the following syntax: 
HTML [ON|OFF] [HEAD text] [BODY text] [TABLE text] [ENTMAP {ON|OFF}] [SPOOL {ON|OFF}]  [PRE[FORMAT] {ON|OFF}] 
where Logon has the following syntax: 
 {username[/password][@connect_identifier]| / }  
 [AS {SYSASM|SYSBACKUP|SYSDBA|SYSDG|SYSOPER|SYSRAC|SYSKM}][edition=value] 
where Start has the following syntax: 
 @{url|file_name[.ext]} [arg ...] 
Warning 
Including your password in plain text is a security risk. You can avoid this risk by 
omitting the password, and entering it only when the system prompts for it. 
You have the option of entering logon. If you do not specify logon but do specify start, SQL*Plus assumes that the first line of the script contains a valid logon. If neither start nor logon are specified, SQL*Plus prompts for logon information. 
3.5.1 Options 
The following sections contain descriptions of SQLPLUS command options: 
3.5.1.1 HELP Option 
-H[ELP] 
Displays the usage and syntax for the SQLPLUS command, and then returns control to the operating system. 
3.5.1.2 VERSION Option 
-V[ERSION] 
Displays the current version and level number for SQL*Plus, and then returns control to the operating system. 
3.5.1.3 COMPATIBILITY Option 
-C[OMPATIBILITY] {x.y[.z] 
Sets the value of the SQLPLUSCOMPATIBILITY system variable to the SQL*Plus release specified by x.y[.z]. Where x is the version number, y is the release number, and z is the update number. For example, 9.0.1 or 10.2. For more information, see the SET 
SQLPLUSCOMPAT[IBILITY] {x.y[.z]}system variable. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 7 of 14
3.5.1.4 LOGON Option -L[OGON] 
Chapter 3 
SQL*Plus Program Syntax 
Specifies not to reprompt for username or password if the initial connection does not succeed. This can be useful in operating system scripts that must either succeed or fail and you don't want to be reprompted for connection details if the database server is not running. 
3.5.1.5 FAST Option 
–F[ast] 
The FAST option improves general performance. This command line option changes the values of the following default settings: 
• ARRAYSIZE = 100 
• LOBPREFETCH = 16384 
• PAGESIZE = 50000 
• ROWPREFETCH = 2 
• STATEMENTCACHE = 20 
3.5.1.6 MARKUP Options 
-M[ARKUP] 
You can use the MARKUP options to generate output in HTML or CSV (Character Separated Values) format, through a query or script. 
MARKUP currently supports HTML 4.0 transitional, and the CSV format. 
Use SQLPLUS -MARKUP to produce output in HTML or CSV format. 
Note 
Depending on your operating system, the complete markup_option clause for the 
SQL*Plus command may need to be contained in quotes. 
For HTML output, use SQLPLUS -MARKUP HTML ON or SQLPLUS -MARKUP HTML ON SPOOL ON to produce standalone web pages. SQL*Plus will generate complete HTML pages automatically encapsulated with <HTML> and <BODY> tags. The HTML tags in a spool file are closed when SPOOL OFF is executed or SQL*Plus exits. 
The -SILENT and -RESTRICT command-line options may be useful when used in conjunction with -MARKUP. 
You can use MARKUP HTML ON to produce HTML output in either the <PRE> tag or in an HTML table. Output to a table uses standard HTML <TABLE>, <TR> and <TD> tags to automatically encode the rows and columns resulting from a query. Output to an HTML table is the default behavior when the HTML option is set ON. You can generate output using HTML <PRE> tags by setting PREFORMAT ON. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 8 of 14
Chapter 3 
SQL*Plus Program Syntax 
For CSV output, use SQLPLUS -MARKUP CSV ON to produce output in CSV format. You can specify the delimiter character by using the DELIMITER option. You can also output text without quotes by using QUOTE OFF. 
Use the SHOW MARKUP command to view the status of MARKUP options. 
The SQLPLUS -MARKUP command has the same functionality as the SET MARKUP command. These options are described in this section. For other information on the SET MARKUP command, see the SET command. 
CSV {ON|OFF} 
CSV is a mandatory MARKUP argument which specifies that the type of output to be generated is CSV. The optional CSV arguments, ON and OFF, specify whether or not to generate CSV output. The default is OFF. You can turn CSV output ON and OFF as required during a session. 
HTML {ON|OFF} 
HTML is a mandatory MARKUP argument which specifies that the type of output to be generated is HTML. The optional HTML arguments, ON and OFF, specify whether or not to generate HTML output. The default is OFF. 
MARKUP HTML ON generates HTML output using the specified MARKUP options. You can turn HTML output ON and OFF as required during a session. 
HEAD text 
The HEAD text option enables you to specify content for the <HEAD> tag. By default, text includes a default in-line cascading style sheet and title. 
If text includes spaces, it must be enclosed in quotes. SQL*Plus does not test this free text entry for HTML validity. You must ensure that the text you enter is valid for the HTML <HEAD> tag. This gives you the flexibility to customize output for your browser or special needs. 
BODY text 
The BODY text option enables you to specify attributes for the <BODY> tag. By default, there are no attributes. If text includes spaces, it must be enclosed in quotes. SQL*Plus does not test this free text entry for HTML validity. You must ensure that the text you enter is valid for the HTML <BODY> tag. This gives you the flexibility to customize output for your browser or special needs. 
TABLE text 
The TABLE text option enables you to enter attributes for the <TABLE> tag. You can use TABLE text to set HTML <TABLE> tag attributes such as BORDER, CELLPADDING, CELLSPACING and WIDTH. By default, the <TABLE> WIDTH attribute is set to 90% and the BORDER attribute is set to 1. 
If text includes spaces, it must be enclosed in quotes. SQL*Plus does not test this free text entry for HTML validity. You must ensure that the text you enter is valid for the HTML <TABLE> tag. This gives you the flexibility to customize output for your browser or special needs. 
ENTMAP {ON|OFF} 
ENTMAP ON or OFF specifies whether or not SQL*Plus replaces special characters <, >, " and & with the HTML entities &lt;, &gt;, &quot; and &amp; respectively. ENTMAP is set ON by default. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 9 of 14
Chapter 3 
SQL*Plus Program Syntax 
You can turn ENTMAP ON and OFF as required during a session. For example, with ENTMAP OFF, SQL*Plus screen output is: 
SQL>PROMPT A > B 
A > B 
With ENTMAP ON, SQL*Plus screen output is: 
SQL&gt; PROMPT A > B 
A &gt; B 
As entities in the <HEAD> and <BODY> tags are not mapped, you must ensure that valid entities are used in the MARKUP HEAD and BODY options. 
If entities are not mapped, web browsers may treat data as invalid HTML and all subsequent output may display incorrectly. ENTMAP OFF enables users to write their own HTML tags to customize output. 
Note 
ENTMAP only takes effect when the HTML option is set ON. For more information about using entities in your output, see the COLUMN command. 
SPOOL {ON|OFF} 
SPOOL ON or OFF specifies whether or not SQL*Plus writes the HTML opening tags, <HTML> and <BODY>, and the closing tags, </BODY> and </HTML>, to the start and end of each file created by the SQL*Plus SPOOL filename command. The default is OFF. 
You can turn SPOOL ON and OFF as required during a session. 
Note 
It is important to distinguish between the SET MARKUP HTML SPOOL option, and the SQLPLUS SPOOL filename command. 
The SET MARKUP HTML SPOOL ON option enables the writing of the <HTML> tag to the spool file. The spool file is not created, and the header and footer tags enabled by the SET MARKUP HTML SPOOL ON option are not written to the spool file until you issue the SQLPLUS SPOOL filename command. See the SPOOL command for more information. 
SQL*Plus writes several HTML tags to the spool file when you issue the SPOOL filename command. 
When you issue any of the SQL*Plus commands: EXIT, SPOOL OFF or SPOOL filename, SQL*Plus appends the following end tags and closes the file: 
</BODY> 
</HTML> 
You can specify <HEAD> tag contents and <BODY> attributes using the HEAD and BODY options 
PRE[FORMAT] {ON|OFF} 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 10 of 14
Chapter 3 
SQL*Plus Program Syntax 
PREFORMAT ON or OFF specifies whether or not SQL*Plus writes output to the <PRE> tag or to an HTML table. The default is OFF, so output is written to a HTML table by default. You can turn PREFORMAT ON and OFF as required during a session. 
Note 
To produce report output using the HTML <PRE> tag, you must set PREFORMAT ON. For example: 
SQLPLUS -M "HTML ON PREFORMAT ON" 
or 
SET MARKUP HTML ON PREFORMAT ON 
3.5.1.7 MARKUP Usage Notes 
MARKUP HTML ON 
When MARKUP HTML ON PREFORMAT OFF is used, commands originally intended to format paper reports have different meaning for reports intended for web tables: 
• PAGESIZE is the number of rows in an HTML table, not the number of lines. Each row may contain multiple lines. The TTITLE, BTITLE and column headings are repeated every PAGESIZE rows. 
• LINESIZE may have an effect on data if wrapping is on, or for very long data. Depending on data size, output may be generated on separate lines, which a browser may interpret as a space character. 
• TTITLE and BTITLE content is output to three line positions: left, center and right, and the maximum line width is preset to 90% of the browser window. These elements may not align with the main output as expected due to the way they are handled for web output. Entity mapping in TTITLE and BTITLE is the same as the general ENTMAP setting 
specified in the MARKUP command. 
• If you use a title in your output, then SQL*Plus starts a new HTML table for output rows that appear after the title. Your browser may format column widths of each table differently, depending on the width of data in each column. 
• SET COLSEP, RECSEP and UNDERLINE only produce output in HTML reports when PREFORMAT is ON. 
MARKUP CSV ON 
When MARKUP CSV ON is used, output from a query will be displayed in CSV format. 
You can enable CSV markup while logging into a user session, by using the -M[ARKUP] CSV ON option at the SQL*Plus command line. For more information, see SQL*Plus Program Syntax. While logged in to a user session, you can enable CSV markup by using the SET MARKUP CSV ON command. 
You can specify the delimiter character by using the DELIMITER option. You can also output text without quotes by using QUOTE OFF. 
3.5.1.8 No Login Time Option 
-nologintime 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 11 of 14
Chapter 3 
SQL*Plus Program Syntax 
When non-SYS users log on, by default, the last login time is displayed in local time format. You can use the -nologintime option to disable this security feature. After you login, the last login information is displayed. 
The last login time is not shown when making a connection with the CONNECT command. 3.5.1.9 PING Option 
-P connect_identifer 
Pings the network listener associated with the provided connect identifier and displays a success or error message along with one of the following exit codes: 
• 0: when the ping is successful 
• 1: when the ping fails 
See the PING command for more information. 
3.5.1.10 RESTRICT Option 
-R[ESTRICT] {1|2|3} 
Lets you disable certain commands that interact with the operating system. This is similar to disabling the same commands in the Product User Profile (PUP) table. However, commands disabled with the -RESTRICT option are disabled even if there is no connection to a server, and remain disabled until SQL*Plus terminates. 
If no -RESTRICT option is active, than all commands can be used, unless disabled in the PUP table. 
If -RESTRICT 3 is used, then LOGIN.SQL is not read. GLOGIN.SQL is read but restricted commands used will fail. 
Table 3-1 Commands Disabled by Restriction Level 
Command Level 1 Level 2 Level 3 
EDIT disabled disabled disabled 
GET disabled 
HOST disabled disabled disabled 
SAVE disabled disabled 
SPOOL disabled disabled 
START, @, @@ disabled 
STORE disabled disabled 
3.5.1.11 SILENT Option 
-S[ILENT] 
Suppresses all SQL*Plus information and prompt messages, including the command prompt, the echoing of commands, and the banner normally displayed when you start SQL*Plus. If you omit username or password, SQL*Plus prompts for them, but the prompts are not visible! Use SILENT to invoke SQL*Plus within another program so that the use of SQL*Plus is invisible to the user. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 12 of 14
Chapter 3 
SQL*Plus Program Syntax 
SILENT is a useful mode for creating reports for the web using the SQLPLUS -MARKUP command inside a CGI script or operating system script. 
3.5.2 Logon 
username[/password] 
Represent the username and password with which you wish to start SQL*Plus and connect to Oracle Database. 
Warning 
Including your password in plain text is a security risk. You can avoid this risk by 
omitting the password, and entering it only when the system prompts for it. 
If you omit username and password, SQL*Plus prompts you for them. If you omit only password, SQL*Plus prompts for it. In silent mode, username and password prompts are not visible! Your username appears when you type it, but not your password. 
@connect_identifier 
Consists of an Oracle Net connect identifier. The exact syntax depends upon the Oracle Net configuration. For more information, refer to the Oracle Net manual or contact your DBA. 
edition=value 
The value for the Oracle Edition. An edition enables two or more versions of an object in a database. It provides a staging area where changed objects can be loaded into the database, compiled, and executed during uptime. This is particularly useful to reduce downtime associated with patching an application. edition=value overrides any edition value specified in the ORA_EDITION environment variable. For more detailed information, see Using Edition Based Redefinition. 
/ 
Represents a default logon using operating system authentication. You cannot enter a connect identifier if you use a default logon. In a default logon, SQL*Plus typically attempts to log you in using the username OPS$name, where name is your operating system username. Note that the prefix "OPS$" can be set to any other string of text. For example, you may wish to change the settings in your INIT.ORA parameters file to LOGONname or USERIDname. See Using Operating System Authentication for information about operating system authentication. 
AS {SYSASM |SYSBACKUP |SYSDBA |SYSDG |SYSOPER |SYSRAC |SYSKM} 
The AS clause enables privileged connections by users who have been granted SYSASM, SYSBACKUP, SYSDBA, SYSDG, SYSOPER, SYSRAC or SYSKM system privileges. 
/NOLOG 
Establishes no initial connection to Oracle Database. Before issuing any SQL commands, you must issue a CONNECT command to establish a valid logon. Use /NOLOG when you want to have a SQL*Plus script prompt for the username, password, or database specification. The first line of this script is not assumed to contain a logon. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 13 of 14
Chapter 3 
SQL*Plus Program Syntax 
3.5.3 Start 
@{url|file_name[.ext]} [arg ...] 
Specifies the name of a script and arguments to run. The script can be called from the local file system or from a web server. 
SQL*Plus passes the arguments to the script as if executing the file using the SQL*Plus START command. If no file suffix (file extension) is specified, the suffix defined by the SET SUFFIX command is used. The default suffix is .sql. 
See the START command for more information. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 14 of 14
Part II 
Using SQL*Plus 
Part II helps you learn how to use SQL*Plus, how to tune SQL*Plus for better performance, how to restrict access to tables and commands and provides overviews of database administration tools and globalization support. 
Part II contains the following chapters: 
• SQL*Plus Basics 
• Using Scripts in SQL*Plus 
• Using Substitution Variables 
• Formatting SQL*Plus Reports 
• Generating HTML Reports from SQL*Plus 
• Tuning SQL*Plus 
• SQL*Plus Security 
• Database Administration with SQL*Plus 
• SQL*Plus Globalization Support 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 1 of 1
4 
SQL*Plus Basics 
This chapter helps you learn the basics of using SQL*Plus. It has the following topics: • About Entering and Executing Commands 
• About Listing a Table Definition 
• About Listing PL/SQL Definitions 
• Running SQL Commands 
• About Running PL/SQL Blocks 
• Running SQL*Plus Commands 
• System Variables that Affect How Commands Run 
• About Stopping a Command while it is Running 
• About Running Operating System Commands 
• About Pausing the Display 
• About Saving Changes to the Database Automatically 
4.1 About Entering and Executing Commands 
Unless stated otherwise, descriptions of commands are applicable to all user interfaces. 
In the command-line, type commands at the SQL*Plus prompt and press Return to execute them. 
Usually, you separate the words in a command with a space or a tab. You can use additional spaces or tabs between words to make your commands more readable. 
Case sensitivity is operating system specific. For the sake of clarity, all table names, column names, and commands in this guide appear in capital letters. 
You can enter three kinds of commands: 
• SQL commands, for working with information in the database 
• PL/SQL blocks, also for working with information in the database 
• SQL*Plus commands, for formatting query results, setting options, and editing and storing SQL commands and PL/SQL blocks 
The manner in which you continue a command on additional lines, end a command, or execute a command differs depending on the type of command you wish to enter and run. Examples of how to run and execute these types of commands are found on the following pages. 
4.1.1 The SQL Buffer 
The SQL buffer stores the most recently entered SQL command or PL/SQL block (but not SQL*Plus commands). The command or block remains in the buffer until replaced by the next SQL command or PL/SQL block. You can view the buffer contents with the LIST command. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 1 of 10
Chapter 4 
About Listing a Table Definition 
You can execute the command or block in the SQL buffer using the RUN or /(slash) 
commands. RUN displays the command or block in the buffer before executing it. /(slash) executes the command or block in the buffer without displaying it first. For information about editing a command or block stored in the buffer see About Editing Scripts in SQL*Plus Command-Line. 
SQL*Plus does not store the following in the SQL buffer: 
• SQL*Plus commands 
• Trailing white space 
• Semicolon or slash characters you type to execute a command 
4.1.2 About Executing Commands 
In command-line SQL*Plus, you type a command and direct SQL*Plus to execute it by pressing the Return key. SQL*Plus processes the command and re-displays the command prompt when ready for another command. 
4.2 About Listing a Table Definition 
To see the definitions of each column in a given table or view, use the SQL*Plus DESCRIBE command. 
 Name Null? Type 
 ----------------------------------------- -------- ---------------- 
 EMPLOYEE_ID NOT NULL NUMBER(6) 
 JOB_ID NOT NULL VARCHAR2(10) 
 MANAGER_ID NUMBER(6) 
 DEPARTMENT_ID NUMBER(4) 
 LOCATION_ID NUMBER(4) 
 COUNTRY_ID CHAR(2) 
 FIRST_NAME VARCHAR2(20) 
 LAST_NAME NOT NULL VARCHAR2(25) 
 SALARY NUMBER(8,2) 
 COMMISSION_PCT NUMBER(2,2) 
 DEPARTMENT_NAME NOT NULL VARCHAR2(30) 
 JOB_TITLE NOT NULL VARCHAR2(35) 
 CITY NOT NULL VARCHAR2(30) 
 STATE_PROVINCE VARCHAR2(25) 
 COUNTRY_NAME VARCHAR2(40) 
 REGION_NAME VARCHAR2(25) 
Note 
DESCRIBE accesses information in the Oracle Database data dictionary. You can also use SQL SELECT commands to access this and other information in the database. 
See your Oracle Database SQL Language Reference for details. 
Example 4-1 Using the DESCRIBE Command 
To list the column definitions of the columns in the sample view EMP_DETAILS_VIEW, enter 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 2 of 10
Chapter 4 
About Listing PL/SQL Definitions 
DESCRIBE EMP_DETAILS_VIEW 
4.3 About Listing PL/SQL Definitions 
To see the definition of a function or procedure, use the SQL*Plus DESCRIBE command. Example 4-2 Using the DESCRIBE Command 
To create and list the definition of a function called AFUNC, enter 
create or replace function afunc (f1 varchar2, f2 number) return number as 
begin 
 if (length(f1) > f2) then 
 return 1; 
 else 
 return 0; 
 end if; 
end; 
/ 
FUNCTION created. 
DESCRIBE afunc 
FUNCTION afunc RETURNS NUMBER 
Argument Name Type In/Out Default? 
--------------- -------- -------- --------- 
F1 VARCHAR2 IN 
F2 NUMBER IN 
4.4 Running SQL Commands 
The SQL command language enables you to manipulate data in the database. See your  Oracle Database SQL Language Reference for information on individual SQL commands. 
1. At the command prompt, enter the first line of the command: 
SELECT EMPLOYEE_ID, LAST_NAME, JOB_ID, SALARY 
If you make a mistake, use Backspace to erase it and re-enter. When you are done, press Return to move to the next line. 
2. SQL*Plus displays a "2", the prompt for the second line. Enter the second line of the command: 
FROM EMP_DETAILS_VIEW WHERE SALARY > 12000; 
The semicolon (;) means that this is the end of the command. Press Return or click 
Execute. SQL*Plus processes the command and displays the results: 
EMPLOYEE_ID LAST_NAME JOB_ID SALARY 
----------- ------------------------- ---------- -------------- 
 100 King AD_PRES $24,000 
 101 Kochhar AD_VP $17,000 
 102 De Haan AD_VP $17,000 
 145 Russell SA_MAN $14,000 
 146 Partners SA_MAN $13,500 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 3 of 10
Chapter 4 
Running SQL Commands 
 201 Hartstein MK_MAN $13,000 
6 rows selected. 
After displaying the results and the number of rows retrieved, SQL*Plus command-line displays the command prompt again. If you made a mistake and therefore did not get the results shown, re-enter the command. 
The headings may be repeated in your output, depending on the setting of a system 
variable called PAGESIZE. Sometimes, the result from a query will not fit the available page width. You can use the system variable, LINESIZE, to set the width of the output in characters. See Setting Page Dimensions. Typically, LINESIZE is set to 80 in command line. Whether you see the message stating the number of records retrieved depends on the setting of the system variable, FEEDBACK. See System Variables that Affect How Commands Run for more information. 
Example 4-3 Entering a SQL Command 
In this example, you will enter and execute a SQL command to display the employee number, name, job, and salary of each employee in the EMP_DETAILS_VIEW view. 
4.4.1 About Understanding SQL Command Syntax 
Just as spoken language has syntax rules that govern the way we assemble words into sentences, SQL*Plus has syntax rules that govern how you assemble words into commands. You must follow these rules if you want SQL*Plus to accept and execute your commands. 
4.4.1.1 About Dividing a SQL Command into Separate Lines 
You can divide your SQL command into separate lines at any points you wish, as long as individual words are not split. Thus, you can enter the query you entered in Example 4-3 on three lines: 
SELECT EMPLOYEE_ID, LAST_NAME, JOB_ID 
FROM EMP_DETAILS_VIEW 
WHERE SALARY>12000; 
In this guide, you will find most SQL commands divided into clauses, one clause on each line. In Example 4-3, for instance, the SELECT and FROM clauses were placed on separate lines. Many people find this clearly visible structure helpful, but you may choose whatever line division makes commands most readable to you. 
4.4.1.2 About Ending a SQL Command 
You can end a SQL command in one of three ways: 
• with a semicolon (;) 
• with a slash (/) on a line by itself 
• with a blank line 
A semicolon (;) tells SQL*Plus that you want to run the command. Type the semicolon at the end of the last line of the command, as shown in Example 4-3, and press Return or click Execute. SQL*Plus processes the command and also stores the command in the SQL buffer. See The SQL Buffer for details. If you mistakenly press Return before typing the semicolon, SQL*Plus prompts you with a line number for the next line of your command. Type the semicolon and press Return again or click Execute to run the command. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 4 of 10
Chapter 4 
About Running PL/SQL Blocks 
A slash (/) on a line by itself also tells SQL*Plus that you wish to run the command. Press Return at the end of the last line of the command. SQL*Plus prompts you with another line number. Type a slash and press Return again or click Execute. SQL*Plus executes the command and stores it in the buffer. 
A blank line in a SQL statement or script tells SQL*Plus that you have finished entering the command, but do not want to run it yet. Press Return at the end of the last line of the 
command. SQL*Plus prompts you with another line number. 
Note 
You can change the way blank lines appear and behave in SQL statements using the SET SQLBLANKLINES command. For more information about changing blank line 
behavior, see the SET command. 
To execute commands this way, press Return again; SQL*Plus now prompts you with the SQL*Plus command prompt. SQL*Plus does not execute the command, but stores it in the SQL buffer. See The SQL Buffer for details. If you subsequently enter another SQL command, SQL*Plus overwrites the previous command in the buffer. 
4.5 About Running PL/SQL Blocks 
You can also use PL/SQL subprograms (called blocks) to manipulate data in the database. See your Oracle Database PL/SQL Language Reference for information on individual PL/SQL statements. 
SQL*Plus treats PL/SQL subprograms in the same manner as SQL commands, except that a semicolon (;) or a blank line does not terminate and execute a block. Terminate PL/SQL subprograms by entering a period (.) by itself on a new line. You can also terminate and execute a PL/SQL subprogram by entering a slash (/) by itself on a new line. 
You enter the mode for entering PL/SQL statements when: 
• You type DECLARE or BEGIN. After you enter PL/SQL mode in this way, type the remainder of your PL/SQL subprogram. 
• You type a SQL command (such as CREATE PROCEDURE) that creates a stored procedure. After you enter PL/SQL mode in this way, type the stored procedure you want to create. 
SQL*Plus stores the subprograms you enter in the SQL buffer. Execute the current 
subprogram with a RUN or slash (/) command. A semicolon (;) is treated as part of the PL/SQL subprogram and will not execute the command. 
SQL*Plus sends the complete PL/SQL subprogram to Oracle Database for processing (as it does SQL commands). See your Oracle Database PL/SQL Language Reference for more information. 
You might enter and execute a PL/SQL subprogram as follows: 
DECLARE 
 x NUMBER := 100; 
 BEGIN 
 FOR i IN 1..10 LOOP 
 IF MOD (i, 2) = 0 THEN --i is even 
 INSERT INTO temp VALUES (i, x, 'i is even'); 
 ELSE 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 5 of 10
Chapter 4 
Running SQL*Plus Commands 
 INSERT INTO temp VALUES (i, x, 'i is odd'); 
 END IF; 
 x := x + 100; 
 END LOOP; 
 END; 
 . 
/ 
4.5.1 About Creating Stored Procedures 
Stored procedures are PL/SQL functions, packages, or procedures. To create stored 
procedures, you use the following SQL CREATE commands: 
• CREATE FUNCTION 
• CREATE LIBRARY 
• CREATE PACKAGE 
• CREATE PACKAGE BODY 
• CREATE PROCEDURE 
• CREATE TRIGGER 
• CREATE TYPE 
Entering any of these commands places you in PL/SQL mode, where you can enter your PL/SQL subprogram. For more information, see About Running PL/SQL Blocks. When you are done typing your PL/SQL subprogram, enter a period (.) on a line by itself to terminate PL/SQL mode. To run the SQL command and create the stored procedure, you must enter RUN or slash (/). A semicolon (;) will not execute these CREATE commands. 
When you use CREATE to create a stored procedure, a message appears if there are  compilation errors. To view these errors, you use SHOW ERRORS. For example: 
SHOW ERRORS PROCEDURE ASSIGNVL 
See SHOW for more information. 
To execute a PL/SQL statement that references a stored procedure, you can use the SQL*Plus EXECUTE command. EXECUTE runs the PL/SQL statement that you enter immediately after the command. For example: 
EXECUTE EMPLOYEE_MANAGEMENT.NEW_EMP('BLAKE') 
See EXECUTE for more information. 
4.6 Running SQL*Plus Commands 
You can use SQL*Plus commands to manipulate SQL commands and PL/SQL blocks and to format and print query results. SQL*Plus treats SQL*Plus commands differently than SQL commands or PL/SQL blocks. 
To speed up command entry, you can abbreviate many SQL*Plus commands. For information on and abbreviations of all SQL*Plus commands, see SQL*Plus Command Reference. 
1. Enter this SQL*Plus command: 
COLUMN SALARY FORMAT $99,999 HEADING 'MONTHLY SALARY' 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 6 of 10
Chapter 4 
Running SQL*Plus Commands 
If you make a mistake, use Backspace to erase it and re-enter. When you have entered the line, press Return. SQL*Plus notes the new format and displays the SQL*Plus command prompt again, ready for a new command. 
2. Enter the following query and press Return to run it: 
SELECT EMPLOYEE_ID, LAST_NAME, JOB_ID, SALARY 
FROM EMP_DETAILS_VIEW WHERE SALARY > 12000; 
EMPLOYEE_ID LAST_NAME JOB_ID MONTHLY SALARY 
----------- ------------------------- ---------- -------------- 
 100 King AD_PRES $24,000 
 101 Kochhar AD_VP $17,000 
 102 De Haan AD_VP $17,000 
 145 Russell SA_MAN $14,000 
 146 Partners SA_MAN $13,500 
 201 Hartstein MK_MAN $13,000 
6 rows selected. 
Example 4-4 Entering a SQL*Plus Command 
This example shows how you might enter a SQL*Plus command to change the format used to display the column SALARY of the sample view, EMP_DETAILS_VIEW. 
The COLUMN command formatted the column SALARY with a dollar sign ($) and a comma (,) and gave it a new heading. 
4.6.1 About Understanding SQL*Plus Command Syntax 
SQL*Plus commands have a different syntax from SQL commands or PL/SQL blocks. 
You do not need to end a SQL*Plus command with a semicolon. When you finish entering the command, you can just press Return or click Execute. There is no need to end a SQL*Plus command with a semicolon. 
4.6.1.1 About Continuing a Long SQL*Plus Command on Additional Lines 
You can continue a long SQL*Plus command by typing a hyphen at the end of the line and pressing Return. If you wish, you can type a space before typing the hyphen. SQL*Plus displays a right angle-bracket (>) as a prompt for each additional line. 
For example: 
COLUMN SALARY FORMAT $99,999 - 
HEADING 'MONTHLY SALARY' 
Since SQL*Plus identifies the hyphen as a continuation character, entering a hyphen within a SQL statement is ignored by SQL*Plus. SQL*Plus does not identify the statement as a SQL statement until after the input processing has joined the lines together and removed the hyphen. For example, entering the following: 
SELECT 200 - 
100 FROM DUAL; 
returns the error: 
SELECT 200 100 FROM DUAL 
 * 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 7 of 10
Chapter 4 
System Variables that Affect How Commands Run 
ERROR at line 1: 
ORA-00923: FROM keyword not found where expected 
To ensure that the statement is interpreted correctly, reposition the hyphen from the end of the first line to the beginning of the second line. 
4.7 System Variables that Affect How Commands Run 
The SQL*Plus SET command controls many variables—called SET variables or system variables—which affect the way SQL*Plus runs your commands. System variables control a variety of conditions within SQL*Plus, including default column widths for your output, whether SQL*Plus displays the number of records selected by a command, and your page size.  
The examples in this guide are based on running SQL*Plus with the system variables at their default settings. Depending on the settings of your system variables, your output may appear slightly different than the output shown in the examples. (Your settings might differ from the default settings if you have a SQL*Plus LOGIN file on your computer.) 
See the SET command for more information on system variables and their default settings. See SQL*Plus Configuration and SQLPLUS Program Syntax for details on the SQL*Plus LOGIN file. 
To list the current setting of a system variable, enter SHOW followed by the variable name. See the SHOW command for information on other items you can list with SHOW. 
4.8 About Stopping a Command while it is Running 
Suppose you have displayed the first page of a 50 page report and decide you do not need to see the rest of it. Press Cancel, the system's interrupt character, which is usually CTRL+C. SQL*Plus stops the display. 
Note 
Pressing Cancel does not stop the printing of a file that you have sent to a printer with the OUT clause of the SQL*Plus SPOOL command. (You will learn about printing 
query results in Formatting SQL*Plus Reports.) You can stop the printing of a file 
through your operating system. For more information, see your operating system's 
installation and user's guide. 
4.9 About Running Operating System Commands 
You can execute an operating system command from the SQL*Plus command prompt. This is useful when you want to perform a task such as listing existing operating system files. 
To run an operating system command, enter the SQL*Plus command HOST followed by the operating system command. For example, this SQL*Plus command runs the command, DIRECTORY *.SQL: 
HOST DIRECTORY *.SQL 
When the command finishes running, the SQL*Plus command prompt appears again. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 8 of 10
Chapter 4 
About Pausing the Display 
Note 
Operating system commands entered from a SQL*Plus session using the HOST 
command do not affect the current SQL*Plus session. For example, setting an 
operating system environment variable does not affect the current SQL*Plus session, but may affect SQL*Plus sessions started subsequently. 
You can suppress access to the HOST command. For more information about 
suppressing the HOST command see SQL*Plus Security. 
4.10 About Pausing the Display 
You can use the PAUSE system variable to stop and examine the contents of the screen after each page during the display of a long report, or during the display of a table definition with many columns. 
You can use SET PAUSE to pause output after displaying each screen of a query or report. See SET PAU[SE] {ON | OFF | text} for more information. 
4.11 About Saving Changes to the Database Automatically 
You can specify changes you wish to make to the information stored in the database using the SQL Database Manipulation Language (DML) commands UPDATE, INSERT, and DELETE— which can be used independently or within a PL/SQL block. These changes are not made permanent until you enter a SQL COMMIT command or a SQL Database Control Language (DCL) or Database Definition Language (DDL) command (such as CREATE TABLE), or use the autocommit feature. The SQL*Plus autocommit feature causes pending changes to be committed after a specified number of successful SQL DML transactions. (A SQL DML transaction is either an UPDATE, INSERT, or DELETE command, or a PL/SQL block.) 
You control the autocommit feature with the SQL*Plus AUTOCOMMIT system variable. Regardless of the AUTOCOMMIT setting, changes are committed when you exit SQL*Plus successfully. 
See Also 
SET EXITC[OMMIT] {ON | OFF} 
COMMIT COMPLETE 
When the autocommit feature is turned on, you cannot roll back changes to the database. 
To commit changes to the database after a number of SQL DML commands, for example, 10, enter 
SET AUTOCOMMIT 10 
SQL*Plus counts SQL DML commands as they are executed and commits the changes after each 10th SQL DML command. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 9 of 10
Chapter 4 
About Saving Changes to the Database Automatically 
Note 
For this feature, a PL/SQL block is regarded as one transaction, regardless of the actual number of SQL commands contained within it. 
To turn the autocommit feature off again, enter the following command: 
SET AUTOCOMMIT OFF 
To confirm that AUTOCOMMIT is now set to OFF, enter the following SHOW command: SHOW AUTOCOMMIT 
AUTOCOMMIT OFF 
See SET AUTO[COMMIT]{ON | OFF | IMM[EDIATE] | n} for more information. Example 4-5 Turning Autocommit On 
To turn the autocommit feature on, enter 
SET AUTOCOMMIT ON 
Alternatively, you can enter the following to turn the autocommit feature on: SET AUTOCOMMIT IMMEDIATE 
Until you change the setting of AUTOCOMMIT, SQL*Plus automatically commits changes from each SQL DML command that specifies changes to the database. After each autocommit, SQL*Plus displays the following message: 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 10 of 10
5 
Using Scripts in SQL*Plus 
This chapter helps you learn to write and edit scripts containing SQL*Plus commands, SQL commands, and PL/SQL blocks. It covers the following topics: 
• About Editing Scripts 
• About Editing Scripts in SQL*Plus Command-Line 
• About Placing Comments in Scripts 
• Running Scripts 
• Nesting Scripts 
• About Exiting from a Script with a Return Code 
Read this chapter while sitting at your computer and try out the examples shown. Before beginning, make sure you have access to the sample schema described in SQL*Plus Overview. 
5.1 About Editing Scripts 
In SQL*Plus command-line, the use of an external editor in combination with the @, @@ or START commands is an effective method of creating and executing generic scripts. You can write scripts which contain SQL*Plus, SQL and PL/SQL commands, which you can retrieve and edit. This is especially useful for storing complex commands or frequently used reports. 
5.1.1 Writing Scripts with a System Editor 
Your operating system may have one or more text editors that you can use to write scripts. You can run your operating system's default text editor without leaving the SQL*Plus command-line by entering the EDIT command. 
You can use the SQL*Plus DEFINE command to define the variable, _EDITOR, to hold the name of your preferred text editor. For example, to define the editor used by EDIT to be vi, enter the following command: 
DEFINE _EDITOR = vi 
You can include an editor definition in your user or site profile so that it is always enabled when you start SQL*Plus. See SQL*Plus Configuration, and the DEFINE and EDIT commands for more information. 
To create a script with a text editor, enter EDIT followed by the name of the file to edit or create, for example: 
EDIT SALES 
EDIT adds the filename extension .SQL to the name unless you specify the file extension. When you save the script with the text editor, it is saved back into the same file. EDIT lets you create or modify scripts. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 1 of 11
Chapter 5 
About Editing Scripts in SQL*Plus Command-Line 
You must include a semicolon at the end of each SQL command and a slash (/) on a line by itself after each PL/SQL block in the file. You can include multiple SQL commands and PL/SQL blocks in a script. 
Example 5-1 Using a System Editor to Write a SQL Script 
Suppose you have composed a query to display a list of salespeople and their commissions. You plan to run it once a month to keep track of how well each employee is doing. 
To compose and save the query using your system editor, invoke your editor and create a file to hold your script: 
EDIT SALES 
Enter each of the following lines in your editor. Do not forget to include the semicolon at the end of the SQL statement: 
COLUMN LAST_NAME HEADING 'LAST NAME' 
COLUMN SALARY HEADING 'MONTHLY SALARY' FORMAT $99,999 
COLUMN COMMISSION_PCT HEADING 'COMMISSION %' FORMAT 90.90 
SELECT LAST_NAME, SALARY, COMMISSION_PCT 
FROM EMP_DETAILS_VIEW 
WHERE JOB_ID='SA_MAN'; 
The format model for the column COMMISSION_PCT tells SQL*Plus to display an initial zero for decimal values, and a zero instead of a blank when the value of COMMISSION_PCT is zero for a given row. Format models and the COLUMN command are described in more detail in the COLUMN command and in Format Models. 
Now use your editor's save command to store your query in a file called SALES.SQL. 5.2 About Editing Scripts in SQL*Plus Command-Line 
You can use a number of SQL*Plus commands to edit the SQL command or PL/SQL block currently stored in the buffer. 
Table 5-1 lists the SQL*Plus commands that allow you to examine or change the command in the buffer without re-entering the command. 
Table 5-1 SQL*Plus Editing Commands 
Command Abbreviation Purpose 
APPEND text A text adds text at the end of the current line 
CHANGE/old/new C/old/newchanges old to new in the current line 
CHANGE/text C/text deletes text from the current line 
CLEAR BUFFER CL BUFF deletes all lines 
DEL (none) deletes the current line 
DEL n(none) deletes line n 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 2 of 11
Table 5-1 (Cont.) SQL*Plus Editing Commands Command Abbreviation Purpose 
Chapter 5 
About Editing Scripts in SQL*Plus Command-Line 
DEL * (none) deletes the current line 
DEL n *(none) deletes line n through the current line 
DEL LAST (none) deletes the last line 
DEL m n(none) deletes a range of lines (m to n) 
DEL * n(none) deletes the current line through line n 
INPUT Iadds one or more lines 
INPUT text I text adds a line consisting of text 
LIST ; or L lists all lines in the SQL buffer 
LIST n L n or nlists line n 
LIST * L * lists the current line 
LIST n * L n *lists line n through the current line 
LIST LAST L LAST lists the last line 
LIST m n L m nlists a range of lines (m to n) 
LIST * n L * nlists the current line through line n 
These are useful if you want to correct or modify a command you have entered. 
5.2.1 Listing the Buffer Contents 
The SQL buffer contains the last SQL or PL/SQL command. Any editing command other than LIST and DEL affects only a single line in the buffer. This line is called the current line. It is marked with an asterisk when you list the current command or block. 
SELECT EMPLOYEE_ID, LAST_NAME, JOB_ID, SALARY 
 2 FROM EMP_DETAILS_VIEW 
 3* WHERE SALARY>12000 
Notice that the semicolon you entered at the end of the SELECT command is not listed. This semicolon is necessary to indicate the end of the command when you enter it, but it is not part of the SQL command and SQL*Plus does not store it in the SQL buffer. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 3 of 11
Example 5-2 Listing the Buffer Contents 
Chapter 5 
About Editing Scripts in SQL*Plus Command-Line 
Suppose you want to list the current command. Use the LIST command as shown. (If you have exited SQL*Plus or entered another SQL command or PL/SQL block since following the steps in Example 4-3, perform the steps in that example again before continuing.) 
LIST 
5.2.2 Editing the Current Line 
The SQL*Plus CHANGE command enables you to edit the current line. Various actions determine which line is the current line: 
• LIST a given line to make it the current line. 
• When you LIST or RUN the command in the buffer, the last line of the command becomes the current line. (Note, that using the slash (/) command to run the command in the buffer does not affect the current line.) 
• If you get an error, the error line automatically becomes the current line. 
SELECT EMPLOYEE_ID, LAST_NAME, JO_ID, SALARY 
 * 
ERROR at line 1: 
ORA-00904: invalid column name 
Examine the error message; it indicates an invalid column name in line 1 of the query. The asterisk shows the point of error—the mis-typed column JOB_ID. 
Instead of re-entering the entire command, you can correct the mistake by editing the command in the buffer. The line containing the error is now the current line. Use the CHANGE command to correct the mistake. This command has three parts, separated by slashes or any other non-alphanumeric character: 
• the word CHANGE or the letter C 
• the sequence of characters you want to change 
• the replacement sequence of characters 
The CHANGE command finds the first occurrence in the current line of the character sequence to be changed and changes it to the new sequence. You do not need to use the CHANGE command to re-enter an entire line. 
1* SELECT EMPLOYEE_ID, FIRST_NAME, JOB_ID, SALARY 
Now that you have corrected the error, you can use the RUN command to run the command again: 
RUN 
SQL*Plus correctly displays the query and its result: 
 1 SELECT EMPLOYEE_ID, LAST_NAME, JOB_ID, SALARY 
 2 FROM EMP_DETAILS_VIEW 
 3* WHERE JOB_ID='SA_MAN' 
EMPLOYEE_ID LAST_NAME JOB_ID MONTHLY SALARY 
----------- ------------------------- ---------- -------------- 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 4 of 11
Chapter 5 
About Editing Scripts in SQL*Plus Command-Line 
 145 Russell SA_MAN $14,000 
 146 Partners SA_MAN $13,500 
 147 Errazuriz SA_MAN $12,000 
 148 Cambrault SA_MAN $11,000 
 149 Zlotkey SA_MAN $10,500 
Note that the column SALARY retains the format you gave it in Example 4-4. (If you have left SQL*Plus and started again since performing Example 4-4 the column has reverted to its original format.) 
See CHANGE for information about the significance of case in a CHANGE command and on using wildcards to specify blocks of text in a CHANGE command. 
Example 5-3 Making an Error in Command Entry 
Suppose you try to select the JOB_ID column but mistakenly enter it as JO_ID. Enter the following command, purposely misspelling JOB_ID in the first line: 
SELECT EMPLOYEE_ID, LAST_NAME, JO_ID, SALARY 
FROM EMP_DETAILS_VIEW 
WHERE JOB_ID='SA_MAN'; 
You see this message on your screen: 
Example 5-4 Correcting the Error 
To change JO_ID to JOB_ID, change the line with the CHANGE command: 
CHANGE /JO_ID/JOB_ID 
The corrected line appears on your screen: 
5.2.3 Appending Text to a Line 
To add text to the end of a line in the buffer, use the APPEND command. 
1. Use the LIST command (or the line number) to list the line you want to change. 
2. Enter APPEND followed by the text you want to add. If the text you want to add begins with a blank, separate the word APPEND from the first character of the text by two blanks: one to separate APPEND from the text, and one to go into the buffer with the text. 
Example 5-5 Appending Text to a Line 
To append a space and the clause DESC to line 4 of the current query, first list line 4: LIST 4 
4* ORDER BY SALARY 
Next, enter the following command (be sure to type two spaces between APPEND and DESC): APPEND DESC 
4* ORDER BY SALARY DESC 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 5 of 11
Type RUN to verify the query: 
Chapter 5 
About Editing Scripts in SQL*Plus Command-Line 
 1 SELECT EMPLOYEE_ID, LAST_NAME, JOB_ID, SALARY 
 2 FROM EMP_DETAILS_VIEW 
 3 WHERE JOB_ID='SA_MAN' 
 4* ORDER BY SALARY DESC 
EMPLOYEE_ID LAST_NAME JOB_ID MONTHLY SALARY 
----------- ------------------------- ---------- -------------- 
 145 Russell SA_MAN $14,000 
 146 Partners SA_MAN $13,500 
 147 Errazuriz SA_MAN $12,000 
 148 Cambrault SA_MAN $11,000 
 149 Zlotkey SA_MAN $10,500 
5.2.4 Adding a New Line 
To insert a new line after the current line, use the INPUT command. 
To insert a line before line 1, enter a zero ("0") and follow the zero with text. SQL*Plus inserts the line at the beginning of the buffer and all lines are renumbered starting at 1. 
0 SELECT EMPLOYEE_ID 
4 
Enter the new line. Then press Return. 
4 ORDER BY SALARY 
SQL*Plus prompts you again for a new line: 
5 
Press Return again to indicate that you will not enter any more lines, and then use RUN to verify and re-run the query. 
 1 SELECT EMPLOYEE_ID, LAST_NAME, JOB_ID, SALARY 
 2 FROM EMP_DETAILS_VIEW 
 3 WHERE JOB_ID='SA_MAN' 
 4* ORDER BY SALARY 
EMPLOYEE_ID LAST_NAME JOB_ID MONTHLY SALARY 
----------- ------------------------- ---------- -------------- 
 149 Zlotkey SA_MAN $10,500 
 148 Cambrault SA_MAN $11,000 
 147 Errazuriz SA_MAN $12,000 
 146 Partners SA_MAN $13,500 
 145 Russell SA_MAN $14,000 
Example 5-6 Adding a Line 
Suppose you want to add a fourth line to the SQL command you modified in Example 5-4. Since line 3 is already the current line, enter INPUT and press Return. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 6 of 11
Chapter 5 
About Placing Comments in Scripts 
INPUT 
SQL*Plus prompts you for the new line: 
5.2.5 Deleting Lines 
Use the DEL command to delete lines in the buffer. Enter DEL specifying the line numbers you want to delete. 
Suppose you want to delete the current line to the last line inclusive. Use the DEL command as shown. 
DEL * LAST 
DEL makes the following line of the buffer (if any) the current line. 
See DEL for more information. 
5.3 About Placing Comments in Scripts 
You can enter comments in a script in three ways: 
• using the SQL*Plus REMARK command for single line comments. 
• using the SQL comment delimiters /*... */ for single or multi line comments. 
• using ANSI/ISO (American National Standards Institute/International Standards 
Organization) comments - - for single line comments. 
Comments entered at the command-line are not stored in the SQL buffer. 
5.3.1 Using the REMARK Command 
Use the REMARK command on a line by itself in a script, followed by comments on the same line. To continue the comments on additional lines, enter additional REMARK commands. Do not place a REMARK command between different lines of a single SQL command. 
REMARK Commission Report; 
REMARK to be run monthly.; 
COLUMN LAST_NAME HEADING 'LAST_NAME'; 
COLUMN SALARY HEADING 'MONTHLY SALARY' FORMAT $99,999; 
COLUMN COMMISSION_PCT HEADING 'COMMISSION %' FORMAT 90.90; 
REMARK Includes only salesmen; 
SELECT LAST_NAME, SALARY, COMMISSION_PCT 
FROM EMP_DETAILS_VIEW 
WHERE JOB_ID='SA_MAN'; 
5.3.2 Using /*...*/ 
Enter the SQL comment delimiters, /*...*/, on separate lines in your script, on the same line as a SQL command, or on a line in a PL/SQL block. 
You must enter a space after the slash-asterisk(/*) beginning a comment. 
The comments can span multiple lines, but cannot be nested within one another: 
/* Commission Report 
 to be run monthly. */ 
COLUMN LAST_NAME HEADING 'LAST_NAME'; 
COLUMN SALARY HEADING 'MONTHLY SALARY' FORMAT $99,999; 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 7 of 11
Chapter 5 
About Placing Comments in Scripts 
COLUMN COMMISSION_PCT HEADING 'COMMISSION %' FORMAT 90.90; 
REMARK Includes only salesmen; 
SELECT LAST_NAME, SALARY, COMMISSION_PCT 
FROM EMP_DETAILS_VIEW 
/* Include only salesmen.*/ 
WHERE JOB_ID='SA_MAN';  
5.3.3 Using - - 
You can use ANSI/ISO "- -" style comments within SQL statements, PL/SQL blocks, or SQL*Plus commands. Since there is no ending delimiter, the comment cannot span multiple lines. 
For PL/SQL and SQL, enter the comment after a command on a line, or on a line by itself: 
-- Commissions report to be run monthly 
DECLARE --block for reporting monthly sales 
For SQL*Plus commands, you can only include "- -" style comments if they are on a line by themselves. For example, these comments are legal: 
-- set maximum width for LONG to 777 
SET LONG 777 
This comment is invalid: 
SET LONG 777 -- set maximum width for LONG to 777 
If you enter the following SQL*Plus command, SQL*Plus interprets it as a comment and does not execute the command: 
-- SET LONG 777 
5.3.4 Notes on Placing Comments 
SQL*Plus does not have a SQL or PL/SQL command parser. It scans the first few keywords of each new statement to determine the command type, SQL, PL/SQL or SQL*Plus. Comments in some locations can prevent SQL*Plus from correctly identifying the command type, giving unexpected results. The following usage notes may help you to use SQL*Plus comments more effectively: 
1. Do not put comments within the first few keywords of a statement. For example: 
CREATE OR REPLACE 
 2 /* HELLO */ 
 3 PROCEDURE HELLO AS 
 4 BEGIN 
 5 DBMS_OUTPUT.PUT_LINE('HELLO'); 
 6 END; 
 7 / 
Warning: Procedure created with compilation errors. 
The location of the comment prevents SQL*Plus from recognizing the command as a command. SQL*Plus submits the PL/SQL block to the server when it sees the slash "/" at the beginning of the comment, which it interprets as the "/" statement terminator. Move the comment to avoid this error. For example: 
 CREATE OR REPLACE PROCEDURE 
 2 /* HELLO */ 
 3 HELLO AS 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 8 of 11
 4 BEGIN 
 5 DBMS_OUTPUT.PUT_LINE('HELLO');  6 END; 
 7 / 
Procedure created. 
Chapter 5 
About Placing Comments in Scripts 
2. Do not put comments after statement terminators (period, semicolon or slash). For example, if you enter: 
SELECT 'Y' FROM DUAL; -- TESTING 
You get the following error: 
SELECT 'Y' FROM DUAL; -- TESTING 
 * 
ERROR at line 1: 
ORA-00911: invalid character 
SQL*Plus expects no text after a statement terminator and is unable to process the command. 
3. Do not put statement termination characters at the end of a comment line or after comments in a SQL statement or a PL/SQL block. For example, if you enter: 
SELECT * 
-- COMMENT; 
You get the following error: 
-- COMMENT 
 * 
ERROR at line 2: 
ORA-00923: FROM keyword not found where expected 
The semicolon is interpreted as a statement terminator and SQL*Plus submits the partially formed SQL command to the server for processing, resulting in an error. 
4. Do not use ampersand characters '&' in comments in a SQL statement or PL/SQL block. For example, if you enter a script such as: 
SELECT REGION_NAME, CITY 
/* THIS & THAT */ 
FROM EMP_DETAILS_VIEW 
WHERE SALARY>12000; 
SQL*Plus interprets text after the ampersand character "&" as a substitution variable and prompts for the value of the variable, &that: 
Enter value for that:  
old 2: /* THIS & THAT */ 
new 2: /* THIS */ 
REGION_NAME CITY 
------------------------- ------------------------------ 
Americas Seattle 
Americas Seattle 
Americas Seattle 
Europe Oxford 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 9 of 11
Chapter 5 
Running Scripts 
Europe Oxford 
Americas Toronto 
6 rows selected. 
You can SET DEFINE OFF to prevent scanning for the substitution character. 
For more information on substitution and termination characters, see DEFINE, 
SQLTERMINATOR and SQLBLANKLINES in the SET command. 
5.4 Running Scripts 
The START command retrieves a script and runs the commands it contains. Use START to run a script containing SQL commands, PL/SQL blocks, and SQL*Plus commands. You can have many commands in the file. Follow the START command with the name of the file: 
START file_name 
SQL*Plus assumes the file has a .SQL extension by default. 
Note 
Starting from Oracle Database release 19c, version 19.3, executing a script that contains a $ (dollar) symbol results in an error on Windows because the $ symbol denotes an environment variable in Linux and Unix. 
For example: 
SQL>@C:\User\my$script.sql 
LAST NAME MONTHLY SALARY COMMISSION % 
------------------------- -------------- ------------ 
Russell $14,000 0.40 
Partners $13,500 0.30 
Errazuriz $12,000 0.30 
Cambrault $11,000 0.30 
Zlotkey $10,500 0.20 
You can also use the @ (at sign) command to run a script: 
@SALES 
The @ and @@ commands list and run the commands in the specified script in the same manner as START. SET ECHO affects the @ and @@ commands in the same way as it affects the START command. 
To see the commands as SQL*Plus "enters" them, you can SET ECHO ON. The ECHO system variable controls the listing of the commands in scripts run with the START, @ and @@ commands. Setting the ECHO variable OFF suppresses the listing. 
START, @ and @@ leave the last SQL command or PL/SQL block of the script in the buffer. Example 5-7 Running a Script 
To retrieve and run the command stored in SALES.SQL, enter 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 10 of 11
START SALES 
Chapter 5 
Nesting Scripts 
SQL*Plus runs the commands in the file SALES and displays the results of the commands on your screen, formatting the query results according to the SQL*Plus commands in the file: 
5.4.1 Running a Script as You Start SQL*Plus 
To run a script as you start SQL*Plus, use one of the following options: 
• Follow the SQLPLUS command with your username, a slash, a space, @, and the name of the file: 
SQLPLUS HR @SALES 
SQL*Plus starts, prompts for your password and runs the script. 
• Include your username as the first line of the file. Follow the SQLPLUS command with @ and the filename. SQL*Plus starts, prompts for your password and runs the file. 
5.5 Nesting Scripts 
To run a series of scripts in sequence, first create a script containing several START 
commands, each followed by the name of a script in the sequence. Then run the script containing the START commands. For example, you could include the following START commands in a script named SALESRPT: 
START Q1SALES 
START Q2SALES 
START Q3SALES 
START Q4SALES 
START YRENDSLS 
Note 
The @@ command may be useful in this example. See the @@ (double at sign) 
command for more information. 
5.6 About Exiting from a Script with a Return Code 
You can include an EXIT command in a script to return a value when the script finishes. See the EXIT command for more information. 
You can include a WHENEVER SQLERROR command in a script to automatically exit SQL*Plus with a return code should your script generate a SQL error. Similarly, you can include a WHENEVER OSERROR command to automatically exit should an operating system error occur. See the WHENEVER SQLERROR command, and the WHENEVER OSERROR command for more information. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 11 of 11
6 
Using Substitution Variables 
This chapter explains how SQL*Plus substitution variables work and where they can be used. It shows the relationship between the three types of variables (substitution, bind, and system) used in SQL*Plus. 
This topics covered are: 
• Defining Substitution Variables 
• About Using Predefined Variables 
• Referencing Substitution Variables 
• System Variables Influencing Substitution Variables 
• Passing Parameters through the START Command 
• About Communicating with the User 
• About Using Bind Variables 
• Using REFCURSOR Bind Variables 
• Fetching Iterative Results from a SELECT inside a PL/SQL Block 
6.1 Defining Substitution Variables 
You can define variables, called substitution variables, for repeated use in a single script by using the SQL*Plus DEFINE command. You can also define substitution variables to use in titles and to save your keystrokes (by defining a long string as the value for a variable with a short name). 
DEFINE L_NAME = "SMITH" (CHAR) 
Note 
In a SQL*Plus session, there is just one global namespace for substitution variables. 
To list all substitution variable definitions, enter DEFINE by itself. Note that any substitution variable you define explicitly through DEFINE takes only CHAR values (that is, the value you assign to the variable is always treated as a CHAR datatype). You can define a substitution variable of datatype NUMBER implicitly through the ACCEPT command. You will learn more about the ACCEPT command. 
To delete a substitution variable, use the SQL*Plus command UNDEFINE followed by the variable name. 
Example 6-1 Defining a Substitution Variable 
To define a substitution variable L_NAME and give it the value "SMITH", enter the following command: 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 1 of 32
DEFINE L_NAME = SMITH 
Chapter 6 
About Using Predefined Variables 
To confirm the variable definition, enter DEFINE followed by the variable name: 
DEFINE L_NAME 
6.2 About Using Predefined Variables 
There are nine variables containing SQL*Plus information that are defined during SQL*Plus installation. These variables can be redefined, referenced or removed the same as any other variable. They are always available from session to session unless you explicitly remove or redefine them. 
See Also 
Predefined Variables for a list of the predefined variables and examples of their use. 
6.3 Referencing Substitution Variables 
Suppose you want to write a query like the one in SALES to list the employees with various jobs, not just those whose job is SA_MAN. You could do that by editing a different value into the WHERE clause each time you run the command, but there is an easier way. 
By using a substitution variable in place of the text, SA_MAN, in the WHERE clause, you can get the same results you would get if you had written the values into the command itself. 
A substitution variable is preceded by one or two ampersands (&). When SQL*Plus encounters a substitution variable in a command, SQL*Plus executes the command as though it contained the value of the substitution variable, rather than the variable itself. 
For example, if the variable SORTCOL has the value JOB_ID and the variable MYTABLE has the value EMP_DETAILS_VIEW, SQL*Plus executes the commands 
SELECT &SORTCOL, SALARY 
FROM &MYTABLE 
WHERE SALARY>12000; 
as if they were 
SELECT JOB_ID, SALARY 
FROM EMP_DETAILS_VIEW 
WHERE SALARY>12000; 
6.3.1 Where and How to Use Substitution Variables 
You can use substitution variables anywhere in SQL and SQL*Plus commands, except as the first word entered. When SQL*Plus encounters an undefined substitution variable in a command, SQL*Plus prompts you for the value. 
You can enter any string at the prompt, even one containing blanks and punctuation. If the SQL command containing the reference should have quote marks around the variable and you do not include them there, the user must include the quotes when prompted. 
SQL*Plus reads your response from the keyboard or standard input. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 2 of 32
Chapter 6 
Referencing Substitution Variables 
After you enter a value at the prompt, SQL*Plus lists the line containing the substitution variable twice: once before substituting the value you enter and once after substitution. You can suppress this listing by setting the SET command variable VERIFY to OFF. 
Created file STATS 
Now run the script STATS: 
@STATS 
And respond to the prompts for values as shown: 
Enter value for group_col: JOB_ID 
old 1: SELECT &GROUP_COL, 
new 1: SELECT JOB_ID, 
Enter value for number_col: SALARY 
old 2: MAX(&NUMBER_COL) MAXIMUM 
new 2: MAX(SALARY) MAXIMUM 
Enter value for table: EMP_DETAILS_VIEW 
old 3: FROM &TABLE 
new 3: FROM EMP_DETAILS_VIEW 
Enter value for group_col: JOB_ID 
old 4: GROUP BY &GROUP_COL 
new 4: GROUP BY JOB_ID 
SQL*Plus displays the following output: 
JOB_ID MAXIMUM 
---------- ---------- 
AC_ACCOUNT 8300 
AC_MGR 12000 
AD_ASST 4400 
AD_PRES 24000 
AD_VP 17000 
FI_ACCOUNT 9000 
FI_MGR 12000 
HR_REP 6500 
IT_PROG 9000 
MK_MAN 13000 
MK_REP 6000 
JOB_ID MAXIMUM 
---------- ---------- 
PR_REP 10000 
PU_CLERK 3100 
PU_MAN 11000 
SA_MAN 14000 
SA_REP 11500 
SH_CLERK 4200 
ST_CLERK 3600 
ST_MAN 8200 
19 rows selected. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 3 of 32
Chapter 6 
Referencing Substitution Variables 
A more practical use of substitution variables is to prompt for a value before referencing the variable: 
SQL> accept myv char prompt 'Enter a last name: '  
SQL> select employee_id from employees where last_name = '&myv';  
If these two commands are stored in a SQL*Plus script, a different last name can be entered each time the script is run. 
If you wish to append characters immediately after a substitution variable, use a period to separate the variable from the character. For example: 
SELECT SALARY FROM EMP_DETAILS_VIEW WHERE EMPLOYEE_ID='&X.5'; 
Enter value for X: 20 
is interpreted as 
SELECT SALARY FROM EMP_DETAILS_VIEW WHERE EMPLOYEE_ID='205'; 
If you want to append a period immediately after a substitution variable name, then use two periods together. For example, if "myfile" is defined as "reports" then the command: 
SQL> spool &myfile..log 
is the same as: 
SQL> spool reports.log 
Text in ANSI "/* */" or "--" comments that looks like a substitution variable may be treated as one. For example: 
SQL> select department_id, location_id /* get dept & loc */ from departments; Enter value for loc: _ 
Here the text "& loc" in the comment is interpreted as a variable reference. SQL*Plus prompts you for a value for the variable "loc". 
Example 6-2 Using Substitution Variables 
Create a script named STATS, to be used to calculate a subgroup statistic (the maximum value) on a numeric column: 
SELECT &GROUP_COL, MAX(&NUMBER_COL) MAXIMUM 
FROM &TABLE 
GROUP BY &GROUP_COL 
. 
SAVE STATS 
6.3.2 Difference Between "&" and "&&" Prefixes 
Both single ampersand (&) and double ampersand (&&) can prefix a substitution variable name in a statement. SQL*Plus pre-processes the statement and substitutes the variable's value. The statement is then executed. If the variable was not previously defined then SQL*Plus prompts you for a value before doing the substitution. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 4 of 32
Chapter 6 
Referencing Substitution Variables 
If a single ampersand prefix is used with an undefined variable, the value you enter at the prompt is not stored. Immediately after the value is substituted in the statement the variable is discarded and remains undefined. If the variable is referenced twice, even in the same statement, then you are prompted twice. Different values can be entered at each prompt: 
SQL> prompt Querying table &mytable 
Enter value for mytable: employees 
Querying table employees 
SQL> select employee_id from &mytable where last_name = 'Jones'; 
Enter value for mytable: employees 
EMPLOYEE_ID 
----------- 
 195 
If a double ampersand reference causes SQL*Plus to prompt you for a value, then SQL*Plus defines the variable as that value (that is, the value is stored until you exit). Any subsequent reference to the variable (even in the same command) using either "&" or "&&" substitutes the newly defined value. SQL*Plus will not prompt you again: 
SQL> prompt Querying table &&mytable 
Enter value for mytable: employees 
Querying table employees 
SQL> select employee_id from &mytable where last_name = 'Jones'; 
EMPLOYEE_ID 
----------- 
 195 
6.3.3 Storing a Query Column Value in a Substitution Variable 
Data stored in the database can be put into substitution variables: 
SQL> column last_name new_value mynv 
SQL> select last_name from employees where employee_id = 100; 
The NEW_VALUE option in the COLUMN command implicitly creates a substitution variable called mynv. The variable is not physically created until a query references the column LAST_NAME. When the query finishes, the variable mynv holds the last retrieved value from the column LAST_NAME: 
SQL> define mynv 
DEFINE mynv = "King" (CHAR) 
6.3.4 Restrictions 
You cannot use substitution variables in the buffer editing commands, APPEND, CHANGE, DEL, and INPUT, nor in other commands where substitution would be meaningless. The buffer editing commands, APPEND, CHANGE, and INPUT, treat text beginning with "&" or "&&" literally, like any other text string. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 5 of 32
Chapter 6 
Referencing Substitution Variables 
6.3.5 How Substitution Variables are Handled in SQL*Plus 
Substitution variable references are pre-processed and substituted before the command is parsed and executed. For each statement, SQL*Plus will do the following: 
1. Loop for each "&" and "&&" variable reference: 
 If the variable already has a value defined (i.e. stored) 
 Replace the variable reference with the value 
 else 
 Prompt for a value 
 Replace the variable reference with the value 
 If the variable is prefixed with "&&" then 
 define (i.e. store) the variable for future use 
2. Execute the statement 
Step 1 happens inside the SQL*Plus client tool. SQL*Plus then sends the final statement to the database engine where step 2 occurs. 
It is not possible to repeatedly prompt in a PL/SQL loop. This example prompts once and the entered value is substituted in the script text. The resulting script is then sent to the database engine for execution. The same entered value is stored five times in the table: 
begin 
 for i in 1 .. 5 loop 
 insert into mytable values (&myv); 
 end loop; 
end; 
/ 
Substitution variables are not recursively expanded. If the value of a referenced variable contains an ampersand, then the ampersand is used literally and is not treated as a second variable prefix: 
SQL> set escape \ 
SQL> define myv = \&mytext 
SQL> prompt &myv 
&mytext 
You cannot use a substitution variable as the first token of a command. Each command name must be hard-coded text else an error is displayed. For example: 
SQL> &myv * from dual; 
SP2-0734: unknown command beginning "&myv * fro..." - rest of line ignored. 6.3.6 Substitution Variable Commands 
Substitution variables can be used to replace options and values in almost all SQL*Plus commands. Several of the commands have special significance for substitution variables. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 6 of 32
Chapter 6 
Referencing Substitution Variables 
Command Description 
ACCEPT Reads a line of input and stores it in a given substitution variable. 
COLUMN Specifies display attributes for a given column. 
DEFINE Specifies a user or predefined variable and assigns a CHAR value to it, or lists the value and variable 
type of a single variable or all variables. 
EDIT Invokes an operating system text editor on the contents of the specified file or on the contents of 
the buffer. 
EXIT Commits or rolls back all pending changes, logs out of Oracle Database, terminates SQL*Plus and 
returns control to the operating system. 
HOST Executes an operating system command without leaving SQL*Plus. 
TTITLE, BTITLE, REPHEADER, REPFOOTER TTITLE places and formats a specified title at the top of each report page. 
BTITLE places and formats a specified title at the 
bottom of each report page. 
REPHEADER places and formats a specified report 
header at the top of each report. 
REPFOOTER places and formats a specified report 
footer at the bottom of each report. 
UNDEFINE Deletes one or more substitution variables that you defined either explicitly (with the DEFINE 
command) or implicitly (with an argument to the 
START command). 
WHENEVER WHENEVER OSERROR performs the specified action (exits SQL*Plus by default) if an operating system 
error occurs (such as a file writing error). 
WHENEVER SQLERROR performs the specified action 
(exits SQL*Plus by default) if a SQL command or 
PL/SQL block generates an error. 
See SQL*Plus Command Summary for more information about these substitution variable commands. 
6.3.6.1 Using "&" Prefixes With Title Variables 
The title commands (TTITLE, BTITLE, REPHEADER and REPFOOTER) substitute variables differently to most other commands. (The exceptions are the EXIT and SET SQLPROMPT commands, which are similar to the title commands). 
The guidelines for variables in titles are: 
• If you want the same value for a variable to be printed on every page then use an "&" prefix and put the variable inside a quoted string: 
accept mycustomer char prompt 'Enter your company name: ' 
ttitle left 'Report generated for company &mycustomer' 
select last_name, job_id from employees order by job_id; 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 7 of 32
Chapter 6 
Referencing Substitution Variables 
• If you want each title to have data from the query that is unique to each report page then do not use an "&" prefix for the variable and do not put the variable inside quotes. 
column job_id new_value ji_nv noprint 
break on job_id skip page 
ttitle left 'Employees in job: ' ji_nv 
select last_name, job_id from employees order by job_id; 
SQL*Plus substitution variables are expanded before each command is executed. After this happens in a title command, the resulting string is stored as the title text. What makes variables in titles special is that they need to be re-substituted for each page of query results. This is so the current COLUMN NEW_VALUE and OLD_VALUE substitution variable values are displayed on each page, customizing each title for the results displayed on its page. If "&" is used inadvertently or incorrectly to prefix title variables, it is possible to get double 
substitution. This is dependent on the variable's value and is easily overlooked when you write scripts. 
Any non-quoted, non-keyword in a title is checked when the page is printed to see if it is a variable. If it is, its value is printed. If not, then the word is printed verbatim. This means that if you use "&myvar" in a title command, and the text substituted for it can itself be interpreted as another variable name then you get double variable substitution. For example, the script: 
define myvar = scottsvar 
ttitle left &myvar 
define scottsvar = Hello 
select * from dual; 
causes the text "left scottsvar" to be stored as the title. When the title is printed on each page of the query this string is re-evaluated. The word "scottsvar" in the title is itself treated as a variable reference and substituted. The query output is: 
Hello 
D 
- 
deX 
Using "&" in titles most commonly causes a problem with the numeric variable names of the SQL*Plus script parameters. If the value of an arbitrary "&"-prefixed title variable is the same as a script parameter variable name, then double substitution will occur. 
To display an "&" in a title, prefix it with the SET ESCAPE character. The ampersand (&) is stored as the title text and is not substituted when page titles are printed. 
6.3.6.2 Variables and Text Spacing in Titles 
Unquoted whitespace in titles is removed. Use whitespace instead of the SET CONCAT character to separate variables from text that should appear immediately adjacent. Use whitespace inside quotes to display a space. For example, the script: 
define myvar = 'ABC' 
ttitle left myvar myvar Text ' Other words' 
select ...; 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 8 of 32
gives a title of: 
ABCABCText Other words 
Chapter 6 
Referencing Substitution Variables 
6.3.7 Substitution Variable Namespace, Types, Formats and Limits 
Substitution Variable Namespace 
In a SQL*Plus session there is just one global name space for substitution variables. If you reconnect using CONNECT, or run subscripts using "@", all variables ever defined are available for use and may be overridden or undefined. 
When a child script finishes, all substitution variables it defined or changed are visible to the calling script. This is particularly noticeable when a subscript executed with "@" or START is given script parameters. The parameters "&1" etc. get redefined and the parent script sees the new values. 
To minimize problems, and for general readability, use symbolic variable names for command parameters. All other references should use the new variable name instead of "&1". For example: 
define myuser = '&1' 
@myscript.sql King 
select first_name from employees where last_name = '&myuser'; 
The call to myscript.sql changes the value of "&1" to "King". By saving the original value of "&1" in "myuser" and using "&myuser" instead of "&1" in the SELECT, the query executes correctly. 
Substitution Variable Types 
The substitution variable types stored by SQL*Plus are: 
• CHAR 
• NUMBER 
• BINARY_FLOAT 
• BINARY_DOUBLE 
The CHAR type is a generic text format similar to the database table VARCHAR2 column type. All variables created from the following are of type CHAR: 
• with DEFINE 
• from prompts for "&" variables 
• from script parameters 
This ensures that values entered are substituted verbatim with no conversion loss. 
Variables created by COLUMN NEW_VALUE or OLD_VALUE for the columns in Oracle number format will have the type NUMBER. These substitution variables are stored in Oracle's internal number representation as they are in the database. This allows display formats to be altered without any internal value loss. Substitution variables of BINARY_FLOAT and BINARY_DOUBLE types are similarly created for Oracle BINARY_FLOAT and 
BINARY_DOUBLE columns. These variables are stored in native machine representation. The CHAR type is used for NEW_VALUE and OLD_VALUE variables with all other column types. 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 9 of 32
Chapter 6 
Referencing Substitution Variables 
There is no explicit DATE type. The DATE keyword in the ACCEPT command is used solely to allow correct format validation against a date format. Substitution variables created by ACCEPT ... DATE, or by COLUMN NEW_VALUE on a date column, are stored as type CHAR. For example: 
SQL> accept mydvar date format 'DD-MON-YYYY' 
prompt 'Enter a date: ' 
Enter a date: 03-APR-2003 
SQL> define mydvar 
DEFINE MYDVAR = "03-APR-2003" (CHAR) 
If a variable already exists and is redefined, its old type is discarded and the new type used. 
The type of a substitution variable is generally transparent. Substitution variables are weakly typed. For example, a COLUMN NEW_VALUE variable takes on the particular type of the named column in each new query. It may also change type during a query. For example, the type of a substitution variable used on a NUMBER column changes from NUMBER to CHAR when a NULL value is fetched. It changes back to NUMBER when the next numeric value is fetched. 
No type comparison semantics are defined for any type since there is no direct comparison of variables. All variables are textually substituted before any SQL or PL/SQL statement that could do a comparison is executed. 
Substitution Variable Formats 
When a variable is substituted, or its value is shown by a DEFINE command, it is formatted as text before the command referencing the variable is finally executed. 
CHAR variables are substituted verbatim. 
NUMBER variables are formatted according to SET NUMWIDTH (by default) or SET NUMFORMAT (if you have explicitly set one): 
The display format of a number can be changed even after the variable is created. To show this, first create a NUMBER variable. You cannot use DEFINE to do this because it makes the type of all new variables CHAR. Instead use a COLUMN NEW_VALUE command which inherits the NUMBER type from a NUMBER column: 
SQL> column c2 new_val m 
SQL> select 1.1 c2 from dual C2; 
---------- 
1.1 
SQL> define m 
DEFINE M = 1.1 (NUMBER) 
Changing the format affects the display of the number but not the stored value: 
SQL> set numformat 99.990 
SQL> define m 
DEFINE M = 1.100 (NUMBER) 
Substitution Variable Limits 
The maximum number of substitution variables allowed is 2048. SQL*Plus gives an error an attempt is made to create more. The limit includes the predefined variables, however these can 
SQL*Plus® User's Guide and Reference G44104-02 
Copyright © 1996, 2026, Oracle and/or its affiliates. 
January 22, 2026 Page 10 of 32