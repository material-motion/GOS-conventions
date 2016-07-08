# A convention for Objective-C libraries

The following convention defines a file system structure for a shared Objective-C library.

    LibraryName/
      .clang-format                 <- Libraries are expected to use clang-format.
      .jazzy.yaml                   <- Libraries should support the Jazzy documentation generator.
      .travis.yml                   <- Libraries should support Travis CI.
                                    
      CHANGELOG.md                  <- Release notes and history.
      README.md                     <- Essential installation and usage guide.
      LibraryName.podspec           <- The podspec for the library.
                                    
      docs/                         <- In-depth technical documentation.
        TechnicalDoc1.md            <- Docs are written in Markdown.
        assets/                     <- All documentation assets live here.
          image.png                 <- Pngs, movs, gifs, etc...
                                    
      examples/                     
        Example.swift               <- Examples can be Swift,
        Example.h                   <-                        or
        Example.m                   <-                           Objective-C.
        supplemental/               <- Non-educational code used by the examples.
          SomeView.swift            <- Supplemental code can be Swift
          SomeView.h                <-                                or
          SomeView.m                <-                                   Objective-C.
        apps/                       <- Example applications live in this sub-directory.
          ExampleApp/               <- Example application.
          AnotherApp/               <- Another example application.
        resources/                  <- Resources required by the examples.
                                    
      src/                          <- All library source lives here.
        MaterialMotionLibraryName.h <- Umbrella header.
        MDMObject.h                 <- Library source must be written in Objective-C.
        MDMObject.m                 
        private/                    <- Private APIs live in a sub-directory
          MDMPrivateAPI.h           
          MDMPrivateAPI.m           
        MaterialMotionLibraryName.bundle/ <- All assets required by the source.
                                    
      tests/                        
        interaction/                <- User interaction tests.
          SomeTest.swift            <- Tests can be Swift,
          AnotherTest.m             <-                     or Objective-C.
        unit/                       <- Unit tests.
          SomeTest.swift            <- Tests can be Swift,
          AnotherTest.m             <-                     or Objective-C.

## Creating a new MDM library

Use `mdm new repo <name>` to create a new Objective-C library.

- [Documentation for `mdm`](https://github.com/material-motion/material-motion-team/tree/develop/contributor_tools/mdm)
- [Documentation for `mdm new`](https://github.com/material-motion/material-motion-team/tree/develop/contributor_tools/new)

## License

Licensed under the Apache 2.0 license. See LICENSE for details.
