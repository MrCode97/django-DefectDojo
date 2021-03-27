---
title: "Features"
date: 2021-02-02T20:46:28+01:00
draft: false
weight: 03
---


Below are the main sections within DefectDojo. Each is designed to allow
for ease of use and simple organization of Products and their Tests. The
[models](../models) page will help you understand the
terminology we use below, so we recommend taking a look at that first.

## Products

The following attributes describe a Product:

Name

:   A short name for the product, used for easy identification. This
    field can hold up to 300 characters.

Description

:   Used to fully describe the product. This field can hold up to 2000
    characters.

Product Manager

:   Provides the ability to store who manages the product lifecycle.
    Useful for contacting team members. This field can hold up to 200
    characters.

Technical Contact

:   Provides the ability to store who should be contacted in case of
    technical questions and/or difficulties. This field can hold up to
    200 characters.

Manager

:   Provides the ability to store who manages the technical resources
    for the product. This field can hold up to 200 characters.

Date Created

:   Stores when the Product was first added to DefectDojo.

Date Updated

:   Stores when the Product was updated.

Business Criticality

:   Criticality of the product.

Platform

:   Type of product: web, API, mobile etc.

Lifecycle

:   Stage of product development

Product Type

:   Used to group products together.

Authorized Users

:   List of users who are allowed to view and interact with the product.

Products are listed on the `/product` page and can be filtered by their
attributes as well as sorted by their name and product type.

![Product Listing Page](../../images/product_3.png)

Visual representation of a product:

![View Product Page](../../images/product_1.png)

Product with metrics:

![View Product Page With Metrics Displayed](../../images/product_2.png)

## Engagements

The following attributes describe an Engagement:

Name

:   Helps distinguish one Engagement from another on the same product.
    This field can hold up to 300 characters.

Target Start Date

:   The projected start date for this engagement.

Target End Date

:   The projected end date for this engagement.

Lead

:   The DefectDojo user who is considered the lead for this group of
    tests.

Product

:   The Product being tested as part of this group of tests.

Active

:   Denotes if the Engagement is currently active or not.

Test Strategy

:   The URL of the testing strategy defined for this Engagement.

Threat Model

:   The document generated by a threat modeling session discussing the
    risks associated with this product at this moment in time.

Hash Code

:   A hash over a configurable set of fields that is used for findings
    deduplication.

Payload

:   Payload used to attack the service / application and trigger the bug
    / problem.

Status

:   Describes the current state of the Engagement. Values include In
    Progress, On Hold and Completed.

Engagements are listed in the `/engagement` page and can be filtered by
their attributes as well as sorted by the product or product type.

![Engagement Listing Page](../../images/eng_2.png)

Visual representation of an engagement:

![View Engagement Page](../../images/eng_1.png)

## Endpoints

Endpoints represent testable systems defined by IP address or Fully
Qualified Domain Name.

The following attributes describe an Endpoint:

Protocol

:   The communication protocol such as \'http\', \'https\', \'ftp\',
    etc.

Host

:   The host name or IP address, you can also include the port number.
    For example \'127.0.0.1\', \'127.0.0.1:8080\', \'localhost\',
    \'yourdomain.com\'.

Path

:   The location of the resource, it should start with a \'/\'. For
    example \"/endpoint/420/edit\"

Query

:   The query string, the question mark should be omitted. \"For example
    \'group=4&team=8\'

Fragment

:   The fragment identifier which follows the hash mark. The hash mark
    should be omitted. For example \'section-13\', \'paragraph-2\'.

Product

:   The Product that this endpoint should be associated with.

Endpoints are listed in the `/endpoints` page and can be filtered by
their attributes as well as sorted by the product or host.

![Endpoint Listing Page](../../images/end_1.png)

Visual representation of an endpoint:

![View Endpoint Page](../../images/end_2.png)

Visual representation of an endpoint with metrics displayed:

![View Endpoint Page with metrics](../../images/end_3.png)

## Findings

Findings represent a flaw within the product being tested. The following
attributes help define a Finding:

Title

:   A short description of the flaw (Up to 511 characters).

Description

:   Longer more descriptive information about the flaw.

Date

:   The date the flaw was discovered.

CVE

:   The Common Vulnerabilities and Exposures (CVE) associated with this
    flaw.

CVSSV3

:   Common Vulnerability Scoring System version 3 (CVSSv3) score
    associated with this flaw.

CWE

:   The CWE number associated with this flaw.

URL

:   External reference that provides more information about this flaw.

Severity

:   The severity level of this flaw (Critical, High, Medium, Low,
    Informational)

Numerical Severity

:   The numerical representation of the severity (S0, S1, S2, S3, S4)

Mitigation

:   Text describing how to best fix the flaw.

Impact

:   Text describing the impact this flaw has on systems, products,
    enterprise, etc.

Steps to Reproduce

:   Text describing the steps that must be followed in order to
    reproduce the flaw / bug.

Severity Justification

:   Text describing why a certain severity was associated with this
    flaw.

Endpoints

:   The hosts within the product that are susceptible to this flaw.

Endpoint Status

:   The status of the endpoint associated with this flaw (Vulnerable,
    Mitigated, \...).

References

:   The external documentation available for this flaw.

Thread ID

:   Thread ID

Hash Code

:   A hash over a configurable set of fields that is used for findings
    deduplication.

Test

:   The test that is associated with this flaw.

Is Template

:   Denotes if this finding is a template and can be reused.

Active

:   Denotes if this flaw is active or not.

Verified

:   Denotes if this flaw has been manually verified by the tester.

False Positive

:   Denotes if this flaw has been deemed a false positive by the tester.

Duplicate

:   Denotes if this flaw is a duplicate of other flaws reported.

Duplicate Finding

:   Link to the original finding if this finding is a duplicate.

Out Of Scope

:   Denotes if this flaw falls outside the scope of the test and/or
    engagement.

Under Review

:   Denotes is this flaw is currently being reviewed.

Mitigated

:   Denotes if this flaw has been fixed, by storing the date it was
    fixed.

Is Mitigated

:   Denotes if this flaw has been fixed.

Mitigated By

:   Documents who has deemed this flaw as fixed.

Reporter

:   Documents who reported the flaw.

Reviewers

:   Document who reviewed the flaw.

Last Reviewed

:   Provides the date the flaw was last \"touched\" by a tester.

Last Reviewed By

:   Provides the person who last reviewed the flaw.

Component Name

:   Name of the affected component (library name, part of a system,
    \...).

Component Version

:   Version of the affected component.

Found By

:   The name of the scanner that identified the flaw.

SonarQube Issue

:   The SonarQube issue associated with this finding.

Unique ID from tool

:   Vulnerability technical id from the source tool. Allows to track
    unique vulnerabilities.

Defect Review Requested By

:   Document who requested a defect review for this flaw.

Under Defect Review

:   Denotes if this finding is under defect review.

Review Requested By

:   Document who requested a review for this finding.

Static Finding

:   Flaw has been detected from a Static Application Security Testing
    tool (SAST).

Dynamic Finding

:   Flaw has been detected from a Dynamic Application Security Testing
    tool (DAST).

Jira Creation

:   The date a Jira issue was created from this finding.

Jira Change

:   The date the linked Jira issue was last modified.

SLA Days Remaining

:   The number of day remaining to stay within the SLA.

Finding Meta

:   Custom metadata (K/V) that can be set on top of findings.

Tags

:   Add custom tags on top of findings (helpful for searching).

Created

:   The date the finding was created inside DefectDojo.

Param

:   Parameter used to trigger the issue (DAST).

Payload

:   Payload used to attack the service / application and trigger the bug
    / problem.

Age

:   The number of days since the finding was created.

Scanner confidence

:   Confidence level of vulnerability which is supplied by the scanner.

Number of Occurrences

:   Number of occurrences in the source tool when several
    vulnerabilities were found and aggregated by the scanner.

Source File

:   Name of the source code file in which the flaw is located.

Source File Path

:   Filepath of the source code file in which the flaw is located.

Notes

:   Stores information pertinent to the flaw or the mitigation.
    Initially there isn\'t a way to categorize notes added for Findings.
    Admin can introduce a new attribute to notes as \'note-type\' which
    can categorize notes. To enable note-types go to System Settings,
    select Note Types and add new note-types to Dojo.

    Note-type

    :   A note-type has 4 attributes.

        -   Name
        -   Description
        -   is\_active - This has to be true to assign the note-type to
            a note.
        -   is\_single - If true, only one note of that note-type can
            exist for a Finding.
        -   is\_mandatory - If true, a Finding has to have at least one
            note from the note-type in order to close it.

    If note-types are enabled, User has to first select the note-type
    from the \"Note Type\" drop down and then add the contents of the
    note.

Images

:   Image(s) / Screenshot(s) related to the flaw.

### SAST specific

For SAST, when source (start of the attack vector) and sink (end of the
attack vector) information are available.

Line

:   Source line number of the attack vector.

Line Number

:   Deprecated will be removed, use line.

File Path

:   Identified file(s) containing the flaw.

SAST Source Object

:   Source object (variable, function\...) of the attack vector.

SAST Sink Object

:   Sink object (variable, function\...) of the attack vector.

SAST Source line

:   Source line number of the attack vector,

SAST Source File Path

:   Source file path of the attack vector.

### Images {#finding_pics}

Images

:   Finding images can now be uploaded to help with documentation and
    proof of vulnerability.

If you are upgrading from an older version of DefectDojo, you will have
to complete the following and make sure [MEDIA\_ROOT]{.title-ref} and
[MEDIA\_URL]{.title-ref} are properly configured:

Add imagekit to INSTALLED\_APPS:

    INSTALLED_APPS = (
        'django.contrib.auth',
        'django.contrib.contenttypes',
        'django.contrib.sessions',
        'django.contrib.sites',
        'django.contrib.messages',
        'django.contrib.staticfiles',
        'polymorphic',  # provides admin templates
        'overextends',
        'django.contrib.admin',
        'django.contrib.humanize',
        'gunicorn',
        'tastypie',
        'djangobower',
        'auditlog',
        'dojo',
        'tastypie_swagger',
        'watson',
        'tagging',
        'custom_field',
        'imagekit',
    )

Add [r\'\^media/\']{.title-ref} to \`LOGIN\_EXEMPT\_URLS\`:

    LOGIN_EXEMPT_URLS = (
        r'^static/',
        r'^api/v1/',
        r'^ajax/v1/',
        r'^reports/cover$',
        r'^finding/image/(?P<token>[^/]+)$'
    )

Then run the following commands (make sure your virtual environment is
activated):

    pip install django-imagekit
    pip install pillow --upgrade
    ./manage.py makemigrations dojo
    ./manage.py makemigrations
    ./manage.py migrate

New installations will already have finding images configured.

Findings are listed on the `/finding/open`, `/finding/closed`,
`/finding/accepted` and `/finding/all` pages. They can be filtered by
their attributes as well as sorted by their Name, Date, Reviewed Date,
Severity and Product.

![Finding Listing Page](../../images/find_1.png)

| 

![Finding Listing Page](../../images/find_2.png)

| 

![Finding Listing Page](../../images/find_3.png)

| 

Visual representation of a Finding:

![Finding View](../../images/find_4.png)

![Finding View](../../images/find_5.png)

![Finding View](../../images/find_6.png)

### Deduplication / Similar findings

Automatically Flag Duplicate Findings

:   \'De-duplication\' is a feature that when enabled will compare
    findings to automatically identify duplicates. To enable
    de-duplication go to System Settings and check Deduplicate findings.
    Dojo deduplicates findings by comparing endpoints, CWE fields, and
    titles. If two findings share a URL and have the same CWE or title,
    Dojo marks the less recent finding as a duplicate. When
    deduplication is enabled, a list of deduplicated findings is added
    to the engagement view. The following image illustrates the option
    deduplication on engagement and deduplication on product level:

    ![Deduplication on product and engagement level](../../images/deduplication.png)

Similar Findings Visualization:

![Similar findings list](../../images/similar_finding_1.png)

![Similar findings list with a duplicate](../../images/similar_finding_2.png)

Similar Findings

:   While viewing a finding, similar findings within the same product
    are listed along with buttons to mark one finding a duplicate of the
    other. Clicking the \"Use as original\" button on a similar finding
    will mark that finding as the original while marking the viewed
    finding as a duplicate. Clicking the \"Mark as duplicate\" button on
    a similar finding will mark that finding as a duplicate of the
    viewed finding. If a similar finding is already marked as a
    duplicate, then a \"Reset duplicate status\" button is shown instead
    which will remove the duplicate status on that finding along with
    marking it active again.

Metrics
-------

DefectDojo provides a number of metrics visualization in order to help
with reporting, awareness and to be able to quickly communicate a
products/product type\'s security stance.

The following metric views are provided:

Product Type Metrics

:   This view provides graphs displaying Open Bug Count by Month,
    Accepted Bug Count by Month, Open Bug Count by Week, Accepted Bug
    Count by Week as well as tabular data on Top 10 Products by bug
    severity, Detail Breakdown of all reported findings, Opened
    Findings, Accepted Findings, Closed Findings, Trending Open Bug
    Count, Trending Accepted Bug Count, and Age of Issues.

    ![Product Type Metrics](../../images/met_1.png)

Product Type Counts

:   This view provides tabular data of Total Current Security Bug Count,
    Total Security Bugs Opened In Period, Total Security Bugs Closed In
    Period, Trending Total Bug Count By Month, Top 10 By Bug Severity,
    and Open Findings. This view works great for communication with
    stakeholders as it is a snapshot in time of the product.

    ![Product Type Counts](../../images/met_2.png)

Simple Metrics

:   Provides tabular data for all Product Types. The data displayed in
    this view is the total number of S0, S1, S2, S3, S4, Opened This
    Month, and Closed This Month.

    ![Simple Metrics](../../images/met_3.png)

Engineer Metrics

:   Provides graphs displaying information about a tester\'s activity.

    ![Simple Metrics](../../images/met_4.png)

Metrics Dashboard

:   Provides a full screen, auto scroll view with many metrics in graph
    format. This view is great for large displays or \"Dashboards.\"

    ![Metrics Dashboard](../../images/met_5.png)

Users
-----

DefectDojo users inherit from
[django.contrib.auth.models.User](https://docs.djangoproject.com/en/1.8/topics/auth/default/#user-objects).

A username, first name, last name, and email address can be associated
with each. Additionally the following describe the type of use they are:

Active

:   Designates whether this user should be treated as active. Unselect
    this instead of deleting accounts.

Staff status

:   Designates whether the user can log into this site.

Superuser status

:   Designates that this user has all permissions without explicitly
    assigning them.

Calendar
--------

The calendar view provides a look at all the engagements occurring
during the month displayed. Each entry is a direct link to the
Engagement view page.

Notifications
-------------

![Notification settings](../../images/notifications_1.png)

DefectDojo can inform you of different events in a variety of ways. You
can be notified about things like an upcoming engagement, when someone
mentions you in a comment, a scheduled report has finished generating,
and more.

The following notification methods currently exist: - Email - Slack -
Microsoft Teams - Alerts within DefectDojo

You can set these notifications on a global scope (if you have
administrator rights) or on a personal scope. For instance, an
administrator might want notifications of all upcoming engagements sent
to a certain Slack channel, whereas an individual user wants email
notifications to be sent to the user\'s specified email address when a
report has finished generating.

Microsoft Teams does not provide an easy way to send messages to a personal
channel. Therefore, DefectDojo can only send system scope notifications
to Microsoft Teams.

In order to identify and notify you about things like upcoming
engagements, DefectDojo runs scheduled tasks for this purpose. These
tasks are scheduled and run using Celery beat, so this needs to run for
those notifications to work. Instructions on how to run Celery beat are
available in the [Reports](#reports) section.

Benchmarks
----------

![OWASP ASVS Benchmarks](../../images/owasp_asvs.png)

DefectDojo utilizes the OWASP ASVS Benchmarks to benchmark a product to
ensure the product meets your application technical security controls.
Benchmarks can be defined per the organizations policy for secure
development and multiple benchmarks can be applied to a product.

Benchmarks are available from the Product view. To view the configured
benchmarks select the dropdown menu from the right hand drop down menu.
You will find the selection near the bottom of the menu entitled:
\'OWASP ASVS v.3.1\'.

![OWASP ASVS Benchmarks Menu](../../images/owasp_asvs_menu.png)

In the Benchmarks view for each product, the default level is ASVS Level
1. On the top right hand side the drop down can be changed to the
desired ASVS level (Level 1, Level 2 or Level 3). The publish checkbox
will display the ASVS score on the product page and in the future this
will be applied to reporting.

![OWASP ASVS Score](../../images/owasp_asvs_score.png)

On the left hand side the ASVS score is displayed with the desired
score, the % of benchmarks passed to achieve the score and the total
enabled benchmarks for that AVSV level.

Additional benchmarks can be added/updated in the Django admin site. In
a future release this will be brought out to the UI.

Reports
-------

![Report Listing](../../images/report_1.png)

Reports can be generated for:

1.  Product types
2.  Products
3.  Engagements
4.  Tests
5.  List of Findings
6.  Endpoints
7.  Custom reports

![Report Generation](../../images/report_2.png)

Filtering is available on all report generation views to aid in focusing the report for the appropriate need.

Custom reports, generated with the Report Builder, allow you to select specific components to be added to the report. These include:

1.  Cover Page
2.  Table of Contents
3.  WYSIWYG Content
4.  Findings 
5.  Vulnerable Endpoints
6.  Page Breaks

DefectDojo's reports can be generated in HTML and AsciiDoc.

Issue Consolidation
-------------------

DefectDojo allows users to automatically consolidate issues from
multiple scanners to remove duplicates.

To enable this feature, hover over the configuration tab on the left
menu and click on system settings. In system settings, click
\'Deduplicate findings\'. Click \'Submit\' at the bottom of the page.

When deduplication is enabled, Dojo will compare CWE, title, and
endpoint details for all findings in a given product. If an issue is
added with either the CWE or title being the same while the endpoint is
also the same, Dojo marks the old issue as a duplicate.

False Positive Removal
----------------------

DefectDojo allows users to tune out false positives by enabling False
Positive History. This will track what engineers have labeled as false
positive for a specific product and for a specific scanner. While
enabled, when a tool reports the same issue that has been flagged as a
false positive previously, it will automatically mark the finding as a
false positive, helping to tune overly verbose security tools.

Deduplication
-------------

Deduplication is a process that allows DefectDojo to find out that a
finding has already been imported.

Upon saving a finding, defectDojo will look at the other findings in the
product or the engagement (depending on the configuration) to find
duplicates

When a duplicate is found:

-   The newly imported finding takes status: inactive, duplicate
-   An \"Original\" link is displayed after the finding status, leading
    to the original finding

There are two ways to use the deduplication:

-   

    Deduplicate vulnerabilities in the same build/release. The vulnerabilities may be found by the same scanner (same scanner deduplication) or by different scanners (cross-scanner deduplication).

    :   -   this helps analysis and assessment of the technical debt,
            especially if using many different scanners; although
            detecting duplicates across scanners is not trivial as it
            requires a certain standardization.

-   

    Track unique vulnerabilities across builds/releases so that defectDojo knows when it finds a vulnerability whether it has seen it before.

    :   -   this allows you keep information attached to a given finding
            in a unique place: all further duplicate findings will point
            to the original one.

### Deduplication Configuration

#### Global configuration

The deduplication can be activated in \"System Settings\" by ticking
\"Deduplicate findings\".

An option to delete duplicates can be found in the same menu, and the
maximum number of duplicates to keep for the same finding can be
configured.

#### Engagement configuration

When creating an engagement or later by editing the engagement, the
\"Deduplication within engagement only\" checkbox can be ticked.

-   If activated: Findings are only deduplicated within the same
    engagement. Findings present in different engagements cannot be
    duplicates
-   Else: Findings are deduplicated across the whole product

Note that deduplication can never occur across different products.

### Deduplication algorithms

The behavior of the deduplication can be configured for each parser in
settings.dist.py (or settings.py after install) by configuring the
[DEDUPLICATION\_ALGORITHM\_PER\_PARSER]{.title-ref} variable.

The available algorithms are:

-   

    [DEDUPE\_ALGO\_UNIQUE\_ID\_FROM\_TOOL]{.title-ref}

    :   -   the deduplication occurs based on
            finding.unique\_id\_from\_tool which is a unique technical
            id existing in the source tool. Few scanners populate this
            field currently. If you want to use this algorithm, you may
            need to update the scanner code beforehand
        -   

            Advantages:

            :   -   If your source tool has a reliable means of tracking
                    a unique vulnerability across scans, this
                    configuration will allow defectDojo to use this
                    ability

        -   

            Drawbacks:

            :   -   Using this algorithm will not allow cross-scanner
                    deduplication as other tools will have a different
                    technical id.
                -   When the tool evolves, it may change the way the
                    unique id is generated. In that case you won\'t be
                    able to recognise that findings found in previous
                    scans are actually the same as the new findings.

-   

    [DEDUPE\_ALGO\_HASH\_CODE]{.title-ref}

    :   -   the deduplication occurs based on finding.hash\_code. The
            hash\_code itself is configurable for each scanner in
            parameter [HASHCODE\_FIELDS\_PER\_SCANNER]{.title-ref}

-   

    [DEDUPE\_ALGO\_UNIQUE\_ID\_FROM\_TOOL\_OR\_HASH\_CODE]{.title-ref}

    :   -   a finding is a duplicate with another if they have the same
            unique\_id\_from\_tool OR the same hash\_code
        -   

            Allows to use both

            :   -   a technical deduplication (based on
                    unique\_id\_from\_tool) for a reliable same-parser
                    deduplication
                -   and a functional one (based on hash\_code configured
                    on CWE+severity+file\_path for example) for
                    cross-parser deduplication

-   

    [DEDUPE\_ALGO\_LEGACY]{.title-ref}

    :   -   This is algorithm that was in place before the configuration
            per parser was made possible, and also the default one for
            backward compatibility reasons.
        -   

            Legacy algorithm basically deduplicates based on:

            :   -   For static scanner: \[\'title\', \'cwe\', \'line\',
                    \'file\_path\', \'description\'\]
                -   For dynamic scanner: \[\'title\', \'cwe\', \'line\',
                    \'file\_path\', \'description\', \'endpoints\'\]

        -   Note that there are some subtleties that may give unexpected
            results. Switch
            [dojo.specific-loggers.deduplication]{.title-ref} to debug
            in settings.py to get more info in case of trouble.

### Hash\_code computation configuration

The hash\_code computation can be configured for each parser using the
parameter [HASHCODE\_FIELDS\_PER\_SCANNER]{.title-ref} in
settings.dist.py.

The parameter [HASHCODE\_ALLOWED\_FIELDS]{.title-ref} list the fields
from finding table that were tested and are known to be working when
used as a hash\_code. Don\'t hesitate to enrich this list when required
(the code is generic and allows adding new fields by configuration only)

Note that [endpoints]{.title-ref} isn\'t a field from finding table but
rather a meta value that will trigger a computation based on all the
endpoints.

Whe populating [HASHCODE\_FIELDS\_PER\_SCANNER]{.title-ref}, please
respect the order of declaration of the fields: use the same order as in
[HASHCODE\_ALLOWED\_FIELDS]{.title-ref} : that will allow cross-scanner
deduplication to function because the hash\_code is computed as a
sha-256 of concatenated values of the configured fields.

Tips:

-   It\'s advised to use fields that are standardized for a reliable
    deduplication, especially if aiming at cross-scanner deduplication.
    For example [title]{.title-ref} and [description]{.title-ref} tend
    to change when the tools evolve and don\'t allow cross-scanner
    deduplication
-   

    Good candidates are

    :   -   cwe or cve
        -   Adding the severity will make sure the deduplication won\'t
            be to aggressive (there are several families of XSS and sql
            injection for example, with various severities but the same
            cwe).
        -   Adding the file\_path or endpoints is advised too.

-   The parameter [HASHCODE\_ALLOWS\_NULL\_CWE]{.title-ref} will allow
    switching to legacy algorithm when a null cwe is found for a given
    finding: this is to avoid getting many duplicates when the tool
    fails to give a cwe while we are expecting it.

### Debugging deduplication

There is a specific logger that can be activated in order to have
details about the deduplication process : switch
[dojo.specific-loggers.deduplication]{.title-ref} to debug in
settings.py.

### Deduplication - APIv2 parameters

-   [skip\_duplicates]{.title-ref} : if true, duplicates are not
    inserted at all
-   [close\_old\_findings]{.title-ref} : if true, findings that are not
    duplicates and that were in the previous scan of the same type
    (example ZAP) for the same product (or engagement in case of
    \"Deduplication on engagement\") and that are not present in the new
    scan are closed (Inactive, Verified, Mitigated)

Service Level Agreement (SLA)
-----------------------------

DefectDojo allows you to maintain your security SLA and automatically
remind teams whenever a SLA is about to get breached, or breaches.

Simply indicate in the `System Settings` for each severity, how many
days teams have to remediate a finding.

![SLA configuration screen](../../images/sla_global_settings.png)

### SLA notification configuration

There are 5 variables in the settings.py file that you can configure, to
act on the global behavior. By default, any findings across the instance
that are in `Active, Verified` state will be considered for
notifications.

``` {.sourceCode .bash}
SLA_NOTIFY_ACTIVE = False
SLA_NOTIFY_ACTIVE_VERIFIED_ONLY = True
SLA_NOTIFY_WITH_JIRA_ONLY = False
SLA_NOTIFY_PRE_BREACH = 3
SLA_NOTIFY_POST_BREACH = 7
```

Setting both `SLA_NOTIFY_ACTIVE` and `SLA_NOTIFY_ACTIVE_VERIFIED_ONLY`
to `False` will effectively disable SLA notifications.

You can choose to only consider findings that have a JIRA issue linked
to them. If so, please set `SLA_NOTIFY_WITH_JIRA_ONLY` to `True`.

The `SLA_NOTIFY_PRE_BREACH` is expressed in days. Whenever a finding\'s
\"SLA countdown\" (time to remediate) drops to this number, a
notification would be sent everyday, as scheduled by the crontab in
`settings.py`, until the day it breaches.

The `SLA_NOTIFY_POST_BREACH` lets you define in days how long you want
to be kept notified about findings that have breached the SLA. Passed
that number, notifications will cease.

{{% notice warning %}}
Be mindful of performance if you choose to have SLA notifications on
non-verified findings, especially if you import a lot of findings
through CI in \'active\' state.
{{% /notice %}}


### What notification channels for SLA notifications?

The same as usual. You will notice that an extra [SLA
breach]{.title-ref} option is now present on the `Notification` page and
also in the `Product` view.

![SLA notification checkbox](../../images/sla_notification_product_checkboxes.png)

### SLA notification with JIRA

You can choose to also send SLA notification as JIRA comments, if your
product is configured with JIRA. You can enable it at the JIRA
configuration level or at the Product level.

The Product level JIRA notification configuration takes precendence over
the global JIRA notification configuration.

### When is the SLA notification job run?

The default setup will trigger the SLA notification code at 7:30am on a
daily basis, as defined in the `settings.py` file. You can of course
modify this schedule to your context.

``` {.sourceCode .python}
'compute-sla-age-and-notify': {
    'task': 'dojo.tasks.async_sla_compute_and_notify',
    'schedule': crontab(hour=7, minute=30),
}
```

{{% notice note %}}
The celery containers are the ones concerned with this configuration. If
you suspect things are not working as expected, make sure they have the
latest version of your settings.py file.
{{% /notice %}}


You can of course change this default by modifying that stanza.

### Launching from the CLI

You can also invoke the SLA notification function from the CLI. For
example, if run from docker-compose:

``` {.sourceCode .bash}
$ docker-compose exec uwsgi /bin/bash -c 'python manage.py sla_notifications'
```