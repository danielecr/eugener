# eugener - at the End Use GENErify and simple template management

## command line interface

A primer definition:

>$ eugener set templates_source https://gogs.target.to.it/repo.git

>$ eugener set templates_localfolder ~/.eugener

>$ eugener get templates_version

>$ eugener get templates

>$ eugener get template_spec TMPLNAME

>$ eugener gen TMPLNAME

>$ eugener check TMPLNAME

templates
```
{source: "https://gogs.target.to.it/repo.git"}
templates:
 [
    { name: TMPLNAME
        checklist: [
        { name, type: fileNotExists, value: 'file/path/name' },
        { name, type: fileExists, value: 'file/path'},
        { name, type: folderExists, value: 'path/folder' }
        ],
        replaceList: [
        {name: "name", fallback: "currentFolderName"},
        {name: "author", fallback: "value", value: "dc@xwave.de"},
        ],
        source_folder: "subfolder_name_of_tilde_dot_eugener_one_level"
    }
 ]
}
```
