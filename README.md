# vpc_with_cloudFormation

> Creating a Virtual Private Cloud (VPC) with AWS CloudFormation

## Overview

AWS CloudFormation is a way to deploy your infrastructure resources and applications on AWS in a reliable, repeatable manner using a called template.

Because the template used by CloudFormation acts as documentation to show exactly what is being deployed.

## Use case description

Create an Amazon Virtual Private Cloud (VPC) using AWS CloudFormation.

Update the VPC adding two new subnets.

## Infrastructure objectives

<ul>
<li>Deploy an AWS CloudFormation template that creates an Amazon VPC</li>
<li>Examine the components of the template</li>
<li>Update a CloudFormation stack</li>
<li>Examine a template with the AWS CloudFormation Designer</li>
<li>Delete a CloudFormation stack</li>
</ul>

## How to use

### Create Stack

<ol start="1">
<li><p>In the <strong>AWS Management Console</strong>, on the <strong>Services</strong> menu, click <strong>CloudFormation</strong>.</p></li>
<li><p>Click <strong>Create Stack</strong>.</p></li>
<li><p>Select <i class="far fa-dot-circle"></i> <strong>Upload a template to Amazon S3</strong>.</p></li>
<li><p>Click <strong>Choose File</strong> or <strong>Browse</strong> to select the <strong>vpc.yaml</strong> located on the <code>v1</code> directory, then click <strong>Next</strong>.</p></li>
<li><p>At the <strong>Specify Details</strong> page, do the following:</p>
<ul>
<li>
<strong>Stack name:</strong> <input readonly="" class="copyable-inline-input" size="3" type="text" value="Lab">
</li>
<li>Click <strong>Next</strong>
</li>
> <p>The <strong>Options</strong> page allows you to specify tags, permissions and advanced options. You will use the default values.</p>
</ul>
</li>
<li><p>Click <strong>Next</strong>.</p></li>
<li><p>Review the configuration on the <strong>Review</strong> page, then click <strong>Create</strong>.</p></li>
</ol>

### Examine the VPC

<ol start="1">
<li><p>On the <strong>Services</strong> menu, click <strong>VPC</strong>.</p></li>
<li><p>In <strong>Filter by VPC</strong> in the top-left corner, select <strong>Lab VPC</strong>.</p></li>
<li><p>In the left navigation pane, click <strong>Your VPCs</strong>.</p></li>
<li><p>Select <i class="far fa-check-square"></i> <strong>Lab VPC</strong>.</p></li>
<li>In the left navigation pane, click <strong>Internet Gateways</strong>.</li>
<li>In the left navigation pane, click <strong>Subnets</strong>.
</li>
<li><p>In the left navigation pane, click <strong>Route Tables</strong>.</p></li>
<li><p>Select the <strong>Public Route Table</strong>.</p></li>
<li><p>Click the <strong>Routes</strong> tab in the lower half of the window.</p></li>
<li>Click the <strong>Subnet Associations</strong> tab.</li>
<li><p>On the <strong>Services</strong> menu, click <strong>CloudFormation</strong>.</p></li>
<li><p>Select the <i class="far fa-check-square"></i> <strong>Lab</strong> stack.</p></li>
<li><p>Click the <strong>Outputs</strong> tab.</p></li>
</ol>

### Update Stack

<p>Once a CloudFormation stack has been deployed, it is recommended that any changes to the resources should be made through CloudFormation rather than by directly modifying the resources.</p>

<ol start="1">
<li><p>In the <strong>Actions</strong> menu, click <strong>Update Stack</strong>.</p></li>
<li><p>Select <i class="far fa-dot-circle"></i> <strong>Upload a template to Amazon S3</strong>.</p></li>
<li><p>Click <strong>Choose File</strong> or <strong>Browse</strong> to select the <strong>vpc.yaml</strong> template located on the <code>v2</code> directory.</p></li>
<li><p>Click <strong>Next</strong>.</p></li>
<li>Click <strong>Next</strong>.</li>
<li>Scroll to the bottom of the screen, then click <strong>Next</strong>.</li>
<p>It indicates that two new Subnets will be created. In addition, two <em>Route Table Associations</em> will be added, to associate these Subnets with their appropriate Route Tables.</p>

<li>Scroll to the bottom of the screen, then click <strong>Update</strong>.</li>
</ol>


### Delete Stack

<ol start="1">
<li><p>In CloudFormation select the <i class="far fa-check-square"></i> <strong>Lab</strong> stack.</p></li>
<li><p>In the <strong>Actions</strong> menu, select <strong>Delete Stack</strong>, then click <strong>Yes, Delete</strong>.</p></li>
<li><p>Click the <strong>Events</strong> tab to view details of the deletion.</p></li>
<p>Click Refresh until the stack is deleted.</p>
</ol>