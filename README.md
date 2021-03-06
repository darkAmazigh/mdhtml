# mdhtml
Static material site generator from markdown files.
## Prerequisite
- Minimum JRE / JDK : 11
## Structure of generated files
<pre>generated_dir
├── css/
│ ├── style.css
├── js/
│   ├── init.js
│   └── chance.js
└── pages/
    ├── page_1.html
    ├── ...
    ├── page_n.html</pre>
## How to use it
### Commands
- `maven package` : to generate the jar
- `java -jar <jarWithDependencies>.jar <mode> <workDir>` : cf below section
### Mandatory parameters
|Parameter|Description|Type of value|
|-----------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
|**Mode**   |defines the startup mode of the generation utility     |**init** : Initialisation mode prepare required config before generation<br/>**gen** :  Generate the static site from config|
|**workDir**|defines the directory to process (which conains .md files|**text** : must be a valid not empty directory                                                                       |

### Optional parameters
Initialisation mode creates a configuration file named `config.yml` which contains some default option. These option can be overriden.
|Parameter|Description|Type|comment|
|---------|-----------|-------------|-------|
|**extension**|defines which file will be included while processing|**array**|only `.md` extension is actually handeled|
|**gitlabRepo**|defines the remote repository|**text**|a valid http / https url|
|**homePageMd**|defines the filename of markdown main page|**text**|
|**homePage**|defines the main html page filename|**text**|
|**outputDir**|defines the output directory name|**text**|
|**projectName**|defines the navbar project name on main html page|**text**|
|**subHeader**|defines subheader text in navigation slider|**text**|
|**tempDir**|defines temp directory|**text**|
|**navcolor**|defines nav menu color|**text**|color as css valid color value - Example `#1e88e`|
## References
This tool uses : 
- Materialize CSS framework check official site at [Materialize](https://materializecss.com/)
- Commonmark-java library for markdown conversion check official site at [Commonmark-java](https://github.com/atlassian/commonmark-java)
- Javascript library chance.js for vectorial image generation check official site at [Chance.js](https://chancejs.com/)
