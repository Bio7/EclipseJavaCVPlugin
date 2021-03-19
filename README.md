# EclipseJavaCVPlugin

This plugin can be updated and extended with customized libraries. By default this library is shipped with Bio7 as a dependency. 
Use a minor version number if you want to update this library.

In Eclipse you can convert the selected plugin to a Maven Project: 

#### Context menu->Configure->Convert to Maven Project

Add your custom maven dependencies. You can then run this build with arguments to copy the dependencies to the plugin libraries location with:

#### Context menu->Run as->Maven build (with arguments below)

In the run configuration add the following command to copy the libraries (Textfield "Goals" - with output directory 'target\lib' as a library subfolder in the plugin location):

#### install dependency:copy-dependencies -DincludeScope=runtime -DoutputDirectory=target\lib

If necessary you can disable the Maven nature with: 

#### Context menu->Maven->Disable Maven nature
