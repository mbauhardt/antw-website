---
layout: documentation
title: JUnit Profiler Formatter
---
{% include JB/setup %}

### JUnit Formatter
It is also recommended but optional to enable the antw junit formatter in your ant project when you use  *antw*. 
The class *antw.junit.JUnitProfilerFormatter* extends the *JUnitFormatter* and profile your code and print some profiling messages about your code.

#### antw.junit.JUnitProfilerFormatter
Goto the [downloads](/downloads) page and download the *antw-junit-0.6.1-fat.jar* and *antw-profiler-0.6.1-fat.jar* add this jar files to your classpath.
To enable the profiler you need to add the profiler and the formatter jar to your *test target* in your build.xml and configure the classes you want to profile in file *antw-transform.properties*.


	<target name="test" depends="jar, unit-jar">
	    <mkdir dir="build/reports" />
	    <junit haltonfailure="true" fork="yes" forkmode="once">
	        <jvmarg value="-javaagent:lib/provided/antw-profiler-0.6.1-fat.jar"/>
	        <sysproperty key="antw-transform.properties" value="${basedir}/${root.dir}/antw-transform.properties"/>
	        <formatter classname="antw.junit.JUnitProfilerFormatter" usefile="false"/>
	            <classpath>
	                <path refid="compile.classpath" />
	                <path refid="artifact.classpath" />
	            </classpath>
	            <batchtest fork="yes" todir="build/reports">
	                <fileset dir="src/test/java">
	                    <include name="**/*Test.java" />
	                </fileset>
	            </batchtest>
	    </junit>
        </target>

You also have to add and configure the file *antw-transform.properties*, when you want to profile your code. Define packages you want to include/exclude.
Per default all classes are included. When you want to exclude a package, use the property *antw.transform.excludes*. When you have classes or packages within the exclude folder you want to profile, you can use the include property *antw.transform.includes* for that.

    antw.transform.includes=foo/bar
    antw.transform.excludes=foo

The above example excludes the package *foo* from the profiling. Except the package *bar* within *foo*. This package is explicit includeded in the profiling.
 

The [tree logger](/documentation/logger/tree.html), [junit profiler logger](/documentation/logger/junit-profiler.html), [message logger](/documentation/logger/message.html) and [apache ant default logger](/documentation/logger/ant-default.html) will filter and log the profiling messages.