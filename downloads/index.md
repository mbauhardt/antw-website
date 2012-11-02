---
layout: page
title: Downloads
group: main_navigation
icon: icon-download icon-black
permalink: /
weight: 4
---
{% include JB/setup %}

Antw does'nt provide an artifact you can download. You have only to execute the following command line

    curl -L https://raw.github.com/mbauhardt/antw/latest/src/main/scripts/antw-checkout.sh | sh

*You does'nt need administration privileges.*
See [Documentation](/documentation) how to [use](/documentation/usage/antw.html) and [install](/documentation/get-remove/installation.html) the application.


---

But you can also use antw jar files without to install antw.
When you want to use antw without to install the application read the [documentation](/documentation/usage/apache-ant.html) how to do this and download the following files

<table class="table">
	<thead>
		<tr>
			<th>#Version</th>
			<th>Jar File</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>0.6.1</td>
			<td><a href="https://github.com/downloads/mbauhardt/antw/antw-logger-0.6.1-fat.jar">antw-logger-0.6.1-fat.jar</a></td>
			<td>logger classes</td>
		</tr>
	</tbody>
</table>


It is also recommended to enable the *antw junit formatter's*. Read the documentation how to enable the [antw junit standard formatter](/documentation/junit-formatter/junit-standard-formatter.html) 
and the [antw profiler formatter](/documentation/junit-formatter/junit-profiler-formatter.html). Here are the files you have to use.

<table class="table">
	<thead>
		<tr>
			<th>#Version</th>
			<th>Jar File</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>0.6.1</td>
			<td><a href="https://github.com/downloads/mbauhardt/antw/antw-junit-0.6.1-fat.jar">antw-junit-0.6.1-fat.jar</a></td>
			<td>junit formatter classes</td>
		</tr>
		<tr>
			<td>0.6.1</td>
			<td><a href="https://github.com/downloads/mbauhardt/antw/antw-profiler-0.6.1-fat.jar">antw-profiler-0.6.1-fat.jar</a></td>
			<td>profler classes which profiles your code</td>
		</tr>
	</tbody>
</table>
