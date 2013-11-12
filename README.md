# Desktop Base

This project aims to be a simple boilerplate to create Java Desktop 
projects that's backed by Ant as build system and Ivy as dependency
manager.

## Based on

* Ant 1.9.2
* Ivy 2.3.0

## How it works

1. Fork this repo
2. Put Java code in `src`
3. Edit `build.xml`
    * Change the project name
    * Configure `mf.built_by`, `mf.created_by` and `mf.main_class` properties
    * Point `revision.file` to a file that will receive revision identifier
    * Write `!repository_revision` placeholder into that file.
        * During build the placeholder will be replaced with the most recent git tag.


### Dependency Management

1. Put your dependencies into `ivy.xml`.
	* You can use [mvnrepository](mvnrepository.com) to look for libs.
2. Run `ant resolve` to download deps into `libs` directory

### Building

1. Run `ant` to build
2. You can clean `bin` and `dist` by using `ant clean`

### Running 

1. A shortcut to `java -jar` is `ant run`


## Fork me

You are free to use this project as template for your Desktop and Applet programs. 

Fork this repo! Make it better! Pull requests are welcome :)