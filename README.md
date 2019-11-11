# eugener - at the End Use GENErify and simple template management

## command line interface

A primer definition:

>$ eugener set templates_source https://gogs.target.to.it/repo.git

~~>$ eugener set templates_localfolder ~/.eugener~~

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
 ],
 lastUpdate: a Date()
}
```


## todos (by steps)

1. set an example template-repo (github repo)
2. download repo in target folder (default)
3. ~~`eugener set templates_localfolder` has to do with something else, I do not know: OMIT~~
4. just use git clone for templates
