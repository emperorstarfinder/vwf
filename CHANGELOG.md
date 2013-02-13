VIRTUAL WORLD FRAMEWORK CHANGE LOG
==================================

----------------------------------

Note: (*) indicates an API change.
0.6.2
----------------------------------------------------------------------------------------------------
- BUG: Fix bug that overrides the glge color with vwf color.
- NEW: Add a JSDoc configuration file and enable Markdown.
- CHG: ruby -i requires an extension in Ruby 1.9.
- CHG: Update module declarations and comment styles for JSDoc 3.
- CHG: Standardize on "var exports = { ... } ; return exports;" so that JSDoc will identify the module's exported elements automatically.
- CHG: Add @module declarations. JSDoc 3 has explicit support for RequireJS-style modules. Standardize on placing the module description above the define() statement.
- CHG: Remove @namespace declarations. @namespace was the JSDoc Toolkit work-around to describe modules.
- CHG: Remove @name, @function, and @field declarations. JSDoc 3 recognizes the element names and types correctly in most cases.
- CHG: Add @function declarations to api/kernel since the API is described here.
- CHG: Add explicit @name declarations to vwf.js since the kernel is not a RequireJS module yet and JSDoc 3 can't parse it automatically.
- CHG: Add @see declarations to link vwf.js implementations to the vwf/api/kernel specifications.
- CHG: Convert most "//"-style descriptions to "///" to add them to the JSDoc 3 documentation.
- NEW: Add version.js and logger.js to the documentation build.
- NEW: Switch to JSDoc 3.
- CHG: Remove --recursion. Search *.vwf.yaml instead of *.yaml for components and remove .js from --ext.
- NEW: Be more specific to avoid vacuuming up non-component YAML files.
- CHG: Move the /// and ## to /** ... */ conversions into external scripts, and convert all files at once 
- CHG: Remove the "/** namespace */ function module.name() ..." hack from the conversion in anticipation of switching to JSDoc 3.
- CHG: Invoke JSDoc as: sh "java", "-jar", ... instead of: sh "java -jar ..." to bypass the shell 
- NEW: Interpret description text as Markdown.
- NEW: Allow the JSDoc scanner to automatically recognize more module elements.
- BUG: Patch the /// to /** */ conversion script to declare define() function arguments as namespaces and assign a name:
- CHG: Add @lends directives to vwf/configuration.js and vwf/utility.js to identify the object to JSDoc that provides the namespace members.
- CHG: Remove now-unnecessary @name and @function directives.
- CHG: Move the vwf/utility.js xpath quoteName and unquoteName functions to allow JSDoc to recognize them.
- CHG: Tweak vwf/configuration.js and vwf/utility.js comments.
- CHG: Tweak vwf/api/kernel.js comments.
- NEW: vwf.js JSDoc comments Correct bad JSDoc name overrides in vwf.js.
- NEW: vwf.js JSDoc comments Set a namespace.
- NEW: vwf.js JSDoc comments Add jsdoc comments for inner methods.
- CHG: vwf.js JSDoc comments Switch utility name overrides from instance to static.
- NEW: Add ambient lights to Humvee applications.
- NEW: Adding Bootstrap Framework to VWF Client Library. Upgrading VWF Client Loader to integrate Bootstrap framework into VWF startup compatibility check.
- BUG: 2D Interface recipe Remove appendTo instructions
- BUG: 2D Interface recipe Add requirements for position:absolute and no index.css
- BUG: 2D Interface recipe Other minor typos
- NEW: Add touch sensitive version of the hmmwv application.
- CHG: Replace Materials recipe "coming soon" page w/ a real recipe
- BUG: multiuser.md Remove typos
- BUG: multiuser.md Add a link to bootstrap.css in the login screen html where bootstrap classes are referenced
- BUG: multiuser.md Add a note that jquery is loaded automatically for every VWF app
- BUG: multiuser.md Edit "What needs to be created" section to show a clearer grouping that is now reflected in the later sections
- BUG: multiuser.md Remove one reference to "his" in multiuser.md to be more gender neutral.
- NEW: multiuser.md Add pages for cookbook recipes and add them to table of contents
- BUG: Fix type in html.md, standardized title capitalization across cookbook recipes
- BUG: Fix a typo in html.md
- BUG: Make title capitalization consistent on cookbook recipes
- NEW: Add 2D Interface recipe and reorganize doc link heirarchy to add cookbook






0.6.1
----------------------------------------------------------------------------------------------------
- BUG: Remove extraneous width in DIV for documentation page formatting.
- NEW: Change how state is written to file to remove POST errors for long states.
- NEW: Add versioning mechanism (instance ID and timestamp) when saving file. Allow save from any directory.
- NEW: Allow state files to be saved from anywhere in the directory structure.
- NEW: Update to latest version of the requestAnimationFrame implementation. Move it into a separate file so all drivers will have access to it.
- NEW: Redirect window to saved file when loading from editor.
- CHG: Changed the screenshot to be of the radio in Firefox where the textures actually show up
- CHG: Moved the location of the image in simulation.md to make more sense
- CHG: Added polish to cookbook recipes
- NEW: Added a "Create a simulation" cookbook recipe - fixed a typo in the radio application in the process
- CHG: Fix permissions for build rakefile updates.
- CHG: Compensate for canvas padding and border in GLGE.Scene.makeRay().
- BUG: Fix pick errors caused by the event-to-canvas coordinate translation.
- CHG: Use the vwf.utility.coordinates functions, which determine the element's page location without regard to other elements and properly account for the element's margins, borders, padding and offset.
- CHG: Remove the window.slideOffset special case that the editor maintained.
- NEW: DOM element coordinate conversion utilities.
- NEW: Make xpath a separate utility submodule.
- BUG: Correct capitalization in color utility references.
- NEW: Allow loading of saved state file directly from URL or editor.
- CHG: Removed the "work in progress" label at the top of multiuser.md
- CHG: Completed the first draft of the multiuser cookbook recipe
- CHG: Anchor ignores to the referenced directory. Ignore Windows standalone ruby.
- BUG: Fix build error: undefined method `DEVKIT' for main:Object.
- BUG: Removed generated file from source code
- NEW: Add list of available saved state files to the user tab in the editor.
- NEW: Add ability to save vwf state to file in current directory, either by name or instance id.
- CHG: GIT Update: Ignore *.pyc.
- CHG: Change 7z to p7zip in install instructions.
- CHG: Improved the multi-user cookbook recipe -Added a file for node.vwf.yaml so that documentation will be generated for it -Fixed a typo in node3.vwf.yaml comments
- CHG: Add 7z to cygwin installation instructions.
- CHG: Update downloads link on virtualworldframework.com
- CHG: Update master/apprentice move dates to late January/February
- CHG: Altered text in draft "about" page
- NEW: Added the source file for the landing page draft
- NEW: Updated new landing page draft and multiuser.md
- NEW: Adding the first draft of the VWF landing page (this will go away once we have a real draft and only the source markdown will remain)
- CHG: Move run.bat download information to be more prominent in README
- NEW: Updated multiuser.html documentation
- NEW: Add downloads navigation element to website
- CHG: Remove static ids in bzflag, test/worldtransform and tile-puzzle
- NEW*: Remove kernel.kernel calls
- CHG: Fix static id in car.vwf.yaml
- CHG: Fix static id in google earth
- CHG: Fix static IDs in cesium, google earth, physics and xmas tree
- NEW*: Change vwf.find to this.kernel.find
- CHG: Fix static ids in scripting tutorial
- NEW*: Add legacy ID patch to only use legacy IDs for index.vwf, appscene-vwf, the camera, and any prototype from vwf.example.com, except for node.vwf
- CHG: Fix static ids used for locating the application root
- CHG: Fix static ids in sandtable, tutorials and documentation
- CHG: Remove obsolete commented-out blocks that were referencing static IDs.
- NEW: Added the beginning of the Multiuser recipe
- NEW: Git Update Add branch information to README
- NEW: Git Update Normalize files still containing CRLF line endings.
- NEW: Git Update To Automatically normalize line endings on checkout and commit.
- NEW: Add vwf/utility to the define array instead of requiring it at each use
- NEW: Add new encodeForAlphaNumeric function to the jquery encoder.
- CHG: Update editor to use new function for HTML element IDs, so jQuery can use the IDs as a selector
- CHG: Update setParams function to use text encoding
- BUG: Fix converting typed arrays to regular arrays for prototype properties
- NEW: Encode editor content to handle untrusted data from the kernel
- NEW: Add the jquery-encoder utility for handling text encoding for various contexts.
- NEW*: Added navmode options to API.
- NEW*: Added backgroundColor property
- BUG: Fixed mouse navigation jump on key press
- BUG: Don't assume that the requestAnimationFrame() callback parameter is always a timestamp.
- BUG: Make proxy/test folder non-empty so that git retains the directory.
- CHG: Update CHANGELOG with API notation and additional comments.
- CHG: Update CHANGELOG for new release and converted to markdown file format.
- BUG: Don't create glge objects for the component prototypes, and boundingBox fix
- BUG: Views should use this (old style drivers) or this.kernel (new style) for accessing vwf.
- BUG: fixed parse error, needs more testing, white space should not cause and issues
- NEW: Added utility color object, fix bug when setting a texture to the same value, added color support to the model/glge driver
- CHG: Added ambientColor to the tile-puzzle and the minesweeper
- NEW: Demo to show use of the point light
- BUG: material fix for the tanks
- BUG: Correct spelling of 'antenna' property
- BUG: Add newline at end of last line to fix YAML parse error.
- CHG: Require "bundle exec rake ..." to utilize bundle environment.
- CHG: Don't "bundle install" within the build.
- CHG: Favor "bundle exec thin start" instead of "bin/thin start".
- CHG: Remove path gymnastics working around the lack of the bundler environment. Find the support/build tools without modifying /usr/bin.
- CHG: Save the Windows RubyInstall and DevKit downloads for reuse in a cache that's shared between working directories (if provided).
- CHG: Download, configure, and build the standalone Windows build incrementally.
- CHG: Factor common parts out into support/build/utility.rake.
- CHG: Make run.bat executable to fix the permissions error.
- CHG: GLGE Ambient Light removed the hard coded setting of the ambient light
- BUG: Remove and ignore .bundle, per Bundler's recommendation.
- CHG: Update forum link to http://forum.virtualworldframework.com.
- NEW: Google Earth - Enable buildings, terrain, and trees layers.
- NEW: Normalize node descriptors for kernel.hashNode().
- NEW: Provide the method return value to model.callingMethod() and view.calledMethod().
- CHG: Rename earth's "camera" to avoid a name conflict with the default camera.
- NEW: Use a dedicated driver flag for Cesium.
- NEW: Workaround texture bug by not allowing the texture to be reassigned to the same value
- CHG: Fix static ids in bzflag
- BUG: Fix horizontal rule incorrectly interpreted as a header indicator.
- BUG: Fix shuffled array out of sync problem in minesweeper and tile puzzle.
- CHG: Fix the static ID reference in the scene type test.
- CHG: Remove functions obsoleted by XPath tests.
- CHG: Fix the static ID reference in the scene type test by using kernel.test() with the URI (the formal type name).
- NEW: Fix static ID references in type tests by testing against the URI (the formal type name).
- NEW: Match the node itself and not just its prototypes in an XPath type test.
- CHG: Adapt to the logger's infoc()-to-infox() API change.
- CHG: Fix static ID references in the *application*.vwf.html by locating and testing nodes with kernel.find() and kernel.test().
- CHG: Fix navscene.vwf#orbitObjectID static ID references.
- CHG: Search for the node using the property as a search pattern, and use its ID.
- CHG: Rename the property to "orbitObjectPattern".
- CHG: Fix activeCamera and camera.lookAt static ID references.
- CHG: Navigate from the scene node to find the lookAt object, and use its ID.
- CHG: activeCamera doesn't need to be initialized since it's already defined in scene.vwf.
- NEW: Fix static ID references after this.children.create( ... ).
- CHG: Update minesweeper and tile-puzzle to use new replicated random function
- NEW: Replicated random (except for test/replication).
- CHG: Simplify prototypes(), to be like ancestors().
- NEW: The Alea pseudorandom number generator.
- NEW: Expose the Alea generator state.
- BUG: Work with Ruby 1.9.2+, where "." is no longer in the default $LOAD_PATH.
- CHG: Use the "testing" configuration for tests. Move shared config settings to the defaults.
- CHG: Deferred kernel.createNode() calls were referencing an undefined parameter.
- BUG: Remove orphan isolateProperties definition. Tweak comment about loading "chrome" html.
- BUG: Humvee Fix starting state of camera buttons so it is synced with state of existing clients
- BUG: Minesweeper Start button state when joining an in progress game
- BUG: Humvee Sync camera buttons so switching views on one client switches the view for all clients
- BUG: Humvee Move transform for interiorCamera to initialize function to fix problem where it would start outside the humvee
- BUG: Humvee Make accelerator and brake pedals momentary
- BUG: Humvee Fix problems with linked objects
- BUG: Humvee Prevent control value changes while an object is animating
- BUG: Humvee Link steering wheel and front wheels
- BUG: Humvee Link hood and hood latches
- BUG: Humvee Remove turning on rear tires
- BUG: Humvee Fix temperature knob
- BUG: Humvee Adjust camera positions
- CHG: Added control behavior to interior objects and added the ability to switch between exterior and interior views
- NEW: Added a controlValueUpdated event to the control behavior




0.6.0
----------------------------------------------------------------------------------------------------
- BUG: Fix exception on pointerHover event for undefined.
- BUG: Do not allow a texture to be reassigned to the same value. 
- BUG: Set minesweeper Start button state when joining an in-progress game.
- BUG: Fix starting state of the camera buttons in humvee so it is synced with state of existing clients.
- NEW*: Add a controlValueUpdated event to the control behavior.
- NEW: Add interaction and camera buttons to the humvee application.
- CHG: Replace humvee application model. Model now includes interior of the vehicle and articulated parts.
- NEW: Create bzflag application based on the classic arcade game, including tank navigation and firing effects. 
- BUG: Rename earth's "camera" to avoid a name conflict with the default camera.
- NEW: Add placeholder for Google Earth configuration options.
- NEW*: Use a dedicated driver flag for Cesium.
- NEW: Integrate ADL's hwmvee application.
- NEW: Integrate AGI's Cesium application.
- CHG: Update editor tab names.
- BUG: Add a message to the Models tab if no models are found.
- BUG: Correct drill up capability for prototype children in the editor. 
- CHG: Reorganize the order of the editor structure to: children, properties, methods, events, behaviors, scripts.
- CHG*: Update navscene component to have separate rotationSpeed and translationSpeed properties.
- BUG: Remove mouse movement choppiness.
- BUG: Allow cameras to be created under any node.
- CHG: Update mouse wheel zoom to use the same formula as keyboard navigation.
- CHG*: Change the camera speed to default to 1.
- NEW: Create worldTransform test for a pointer follower.
- CHG: Move the worldTransform property getter from the glge driver to the node3 component.
- NEW*: Add a replicated random function.
- NEW*: Add origin information to pickInfo.
- NEW: Include components in the auto-generated documentation.
- NEW: Add Developer's Guide to documentation.
- CHG: Clarify installation instructions. Add instructions to build website.
- BUG: Correct catalog to display sessions for applications with a forward slash in their name.
- CHG: Honor levels in the logger.
- CHG*: Rename the logger's infoc(), warnc(), etc. to infox(), warnx(), etc.
- CHG: Switch to MiniTest for compatibility with Ruby 1.9.
- NEW: Show a hint in run.bat to prompt users to launch a browser.
- BUG: Fix build error with pygmentize.
- CHG: Remove undefined kernel and view function properties from vwf_view.
- CHG*: Swap the modelGenerator/viewGenerator and kernelGenerator parameters in model.load()/view.load() to allow drivers to omit the kernel generator argument.

0.5.2.1
----------------------------------------------------------------------------------------------------
- BUG: Correct URL links on the about page.

0.5.2
----------------------------------------------------------------------------------------------------
- NEW: Add VWF Forum for General and Technical Questions.
- CHG: Add prototype Properties/Methods/Events/Children/Scripts to the editor interface.
- NEW: Increase the width of the editor when editing scripts.
- NEW: Add ability to create new scripts via the editor interface.
- NEW: Allow setting of basic properties (rotaiton, translation, scale) before dragging and dropping from the Model tab.
- CHG: Always attach new camera to its parent.
- BUG: Remove purple tint from drag and drop models.

0.5.1
----------------------------------------------------------------------------------------------------
- BUG: ERB files not generating HTML files during build process.
- BUG: Demonstration Missing Textures Causing Black Boxes for Imagery.
- NEW: Sync the entire graph when saving and loading the application state.
- NEW: Save and load the application state as a delta from the initial state.
- NEW: Support a script text editor in the list editor.
- NEW: Search Engine Optimization for Virtual World Framework Website.
- NEW: Create a Wikipedia Page for Virtual World Framework.
- NEW: Add SVN Change List to GitHub. Should occur at end of each sprint.
- NEW: Implement and complete VWF website.
- NEW: Update FAQs with enhanced version.
- BUG: Catalog page is not regenerated during the build process if it has already been created.
- NEW: Make script area editable.
- NEW: Submit edited scripts.
- NEW: Drag and Drop Components from Library into Scene.
- NEW: Create UI for component library.
- NEW: Add components from public/models to library.
- NEW: Update FAQs with full list.
- BUG: Remove duplicate scripts from editor view.
- NEW: Add sample tutorial application to demonstrate script editability.
- BUG: If new child nodes are added when hierarchy tab is visible, they do not show up in editor until the tab is refreshed. 
- CHG: Using mousewheel to zoom in and out of most applications is too fast. After one turn, most content isn't viewable.
- BUG: Warnings in build process.
- CHG: The loading overlay looks bad until the images load.
- CHG: Border around scene updated.
- BUG: Navigation doesn't work in sandtable anymore.
- BUG: Keyboard navigation in sandtable is much slower than it used to be.
- BUG: The position doesn't sync correctly when a second client joins an earth application.
- CHG: Default view for the earth application is not interesting.
- BUG: Toolbar states don't sync correctly in sandtable
- BUG: Lines don't sync correctly in sandtable.
- BUG: The clear button in physics doesn't clear items in a second client that existed when it joined.
- BUG: Javascript error when second client joins Humvee app.
- BUG: Remove toolbar buttons from earth application.
- BUG: Mousewheel doesn't zoom at all in Firefox.
- BUG: Users tab is empty on anything down a directory(i.e. the tutorial/ and adl/ applications)
- BUG: Editor hierarchy comes up blank on occasion