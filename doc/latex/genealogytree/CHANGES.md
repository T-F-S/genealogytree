# Changelog
All notable changes to this project will be documented in this file.

The format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to
[Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
### Changed
### Deprecated
### Removed
### Fixed
### Security



## [2.1.0] - 2021-09-20

### Added
- Portuguese translation provided by Natan de Almeida Laverde
- Value `portuguese` for option `language`

### Changed
- Readme moved and adapted from README to README.md
- Changelog moved from documentation `genealogytree.pdf` to CHANGES.md and adapted to
  [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
- From now on version numbers adhere to
  [Semantic Versioning](http://semver.org/spec/v2.0.0.html)

### Fixed
- `options for subtree` had no effect in v2.01 (issue #39)



## [2.01] - 2020-07-28

### Added
- New *LaTeXÜ macros added corresponding to existing macros:
    - `\getree_set_options_for_subtree:nn`
    - `\getree_set_options_for_family:nn`
    - `\getree_set_options_for_node:nn`
- Some hints for events with unknown dates added
  to the documentation (issue #36)

### Changed
- Implementation changed to avoid problems with spurious blanks 
  and resulting errors for
    - Option `tcb/if image defined`
    - Option `date range before`
    - Option `date range after`
    - Option `place text`
    - Option `options for subtree`
    - Option `options for family`
    - Option `options for node`
    - Option `ignore subtree`
    - Option `ignore node`
    - `\gtrsetoptionsforsubtree`
    - `\gtrsetoptionsforfamily`
    - `\gtrsetoptionsfornode`
    - `\gtrignoresubtree`
    - `\gtrignorenode`
    - `\gtrloadlanguage`
    - `\gtrSymbolsSetCreateSelected`



## [2.00] - 2020-06-19

### Added
- New options for influencing the autolayout algorithm to avoid
  overlapping edges for childless families (issue #34):
    - Option `insert for childless families`
    - Option `insert phantom for childless families`
    - Option `insert for childless families level limit`
- New algorithm for automatic ancestor completion. This autofill is
  controlled by the new options
    - Option `autofill parents unspecific`
    - Option `autofill parents unspecific*`
    - Option `autofill parents male female`
    - Option `autofill parents male female*`
    - Option `autofill parents female male`
    - Option `autofill parents female male*`
    - Option `autofill parents none`
    - Option `complemented`
    - Option `complemented phantom`
- New option `ignore parent childs` to remove all
  siblings in an ancestor tree.
- New data base keys for holding relation information:
    - Option `database/relation`
    - Option `database/ancestor`
    - Option `database/descendant`
    - Option `database/sibling`
    - Option `database/unrelated`
- New data base key for holding age information and accompanying
  options and macros:
    - Option `database/age`
    - Option `age code`
    - `\gtrPrintAge`
    - `\gtrifagedefined`
    - `\gtrDBage`
- Conversion with MuPDF added and externalization rewritten for MuPDF.
- New auxiliary tools for graph (picture) sizing
    - `\gtrautosizebox`
    - `\gtrautosizebox*`
    - Environment `autosizetikzpicture`
    - Environment `autosizetikzpicture*`
- Graph example file `example.neumann.graph`
- New library `fanchart` to draw fan chart diagrams
  with a plethora of macros and options (issue #31):
    - `\gtrfanchart`
    - `\gtrfanchartinput`
    - Option `fanchart radii`
    - Option `fanchart inner offset`
    - Option `fanchart outer offset`
    - Option `fanchart minor angle`
    - Option `fanchart major angle`
    - Option `fanchart angles`
    - Option `fanchart open full`
    - Option `fanchart open up`
    - Option `fanchart open down`
    - Option `fanchart open left`
    - Option `fanchart open right`
    - Option `fanchart open for`
    - Option `fanchart reset bounds`
    - Option `fanchart bounds border`
    - Option `fanchart landscape from level`
    - Option `fanchart text portrait`
    - Option `fanchart text landscape`
    - Option `fanchart boundary color`
    - Option `fanchart boundary width`
    - Option `fanchart root style`
    - Option `fanchart root malefemale`
    - Option `fanchart segment style`
    - Option `fanchart segment malefemale`
    - Option `fanchart segment relation`
    - Option `fanchart segment wave`
    - Option `fanchart segment colorwheel`
    - Option `fanchart segment radial`
    - Option `fanchart marker style`
    - Option `fanchart marker malefemale`
    - Option `fanchart marker relation`
    - Option `fanchart marker wave`
    - Option `fanchart marker colorwheel`
    - Option `fanchart marker radial`
    - Option `tikz/gtr set color wave`
    - Option `tikz/gtr set color colorwheel`
    - Option `tikz/gtr set color series`
    - Option `fanchart complemented segment style`
    - Option `fanchart complemented marker style`
    - Option `fanchart segment style for levels`
    - Option `fanchart marker style for levels`
    - Option `fanchart segment style for ids`
    - Option `fanchart marker style for ids`
    - Option `fanchart male style`
    - Option `fanchart female style`
    - Option `fanchart neuter style`
    - Option `fanchart ancestor style`
    - Option `fanchart descendant style`
    - Option `fanchart sibling style`
    - Option `fanchart unrelated style`
- Option `fanchart template` with
    - Template `malefemale sober`
    - Template `malefemale relation`
    - Template `colorwheel sober`
    - Template `colorwheel serious`
    - Template `colorwheel malefemale`
    - Template `colorwheel rich`
    - Template `colorwheel opulent`
    - Template `wave sober`
    - Template `wave serious`
    - Template `wave malefemale`
    - Template `wave rich`
    - Template `wave opulent`
    - Template `radial sober`
    - Template `radial serious`
    - Template `radial malefemale`
    - Template `radial rich`
    - Template `radial opulent`
- Advanced customization by
    - `\gtrcomplemented`
    - Option `fanchart-segment-definition`
    - Option `fanchart-marker-definition`
    - Option `fanchart-segment-code`
    - Option `fanchart-root-code`
    - `\l_getree_fanchart_minor_angle_tl`
    - `\l_getree_fanchart_major_angle_tl`
    - `\l_getree_fanchart_angle_a_tl`
    - `\l_getree_fanchart_angle_b_tl`
    - `\l_getree_fanchart_radius_a_tl`
    - `\l_getree_fanchart_radius_b_tl`
    - `\l_getree_fanchart_offset_a_tl`
    - `\l_getree_fanchart_offset_b_tl`
    - `\l_getree_fanchart_line_width_tl`
    - `\l_getree_fanchart_level_tl`
    - `\l_getree_fanchart_ratio_tl`
    - `\l_getree_fanchart_id_tl`
    - `\c_getree_fanchart_maximum_rings_tl`
    - `\getree_fanchart_if_complemented_node_p:`
    - `\getree_fanchart_if_complemented_node:TF`
    - `\getree_fanchart_set_segment_style:n`
    - `\getree_fanchart_set_marker_style:n`
    - `\getree_fanchart_set_color_wave:n`
    - `\getree_fanchart_set_color_colorwheel:n`
    - `\getree_fanchart_draw_path:n`
    - `\getree_fanchart_draw_path:nnn`
    - `\getree_fanchart_draw_root_style:n`
    - `\getree_fanchart_draw_segment_standard:`

### Changed
- Implementation of `\genealogytree` slightly changed.

### Fixed
- Template `database sideways` et.al. raised errors when used in combination with
  `family database` (issue #31).



## [1.32] - 2019-04-08

### Added
- Internal database print command documented `\gtrPrintDatabase` (issue #24)

### Changed
- `tcolorbox` needs to be version 4.20 (2019/03/02) or newer.

### Fixed
- The templates library used some internal color names of `tcolorbox`. 
  They are adapted now to the new official names (issue #30).



## [1.31] - 2018-04-17

### Added
- Option `database/imageopt`
- Option `database/viewport`
- `\gtrDBimageopt`
- `\gtrincludeDBimage`
- TikZ-Option `fill overzoom DBimage`

### Changed
- `tcolorbox` needs to be version 4.13 (2018/03/22) or newer.



## [1.30] - 2017-12-08

### Added
- Spanish translation `language=spanish` provided by Francisco G. Pérez Sánchez
- Swedish translation `language=swedish` provided by Per Starbäck
- New values `date format`: `d/m yyyy`, `yyyy d/m`
- Warnings for missing language strings added to \url{genealogytree-languages.pdf}
- Option `edges shift`
- Option `edges up`
- Option `edges down`
- Option `edges up by`
- Option `edges down by`
- Option `reset edge level shift`
- Option `switch edge level shift`
- Option `nullify edge level shift`



## [1.21] - 2017-09-15

### Added
- Italian translation `language=italian` provided by Andrea Vaccari 
- Template `database pole reduced`
- Template `database poleportrait`
- Template `database poleportrait reduced`
- Template `database portrait reduced`
- Template `database traditional reduced`
- Template `database sideways reduced`
- Template `database sidewaysportait`
- Template `database sidewaysportait reduced`

### Changed
- `\gtrsymFloruit` symbol rotated by 36 degrees for an enhanced
  optical differentiation from `\gtrsymBorn`.



## [1.20] - 2017-07-18

### Added
- Dutch translation `language=dutch` provided by Dirk Bosmans
- New event `floruit` with symbol `\gtrsymFloruit` proposed by Mikkel Eide Eriksen
  Accompanying keys are
  `database/floruit`, `database/floruit+`, `database/floruit-`, `symlang/Floruit`, `event prefix/floruit`.
  The standard options for `database format` were extended for floruit.
  The standard options for `database format` were extended for floruit.



## [1.10] - 2017-01-29

### Added
- Danish translation `language=danish` provided by Mikkel Eide Eriksen
- French translation `language=french` provided by Denis Bitouzé
- Separate document `genealogytree-languages` added to give a short survey
  of language settings.
- New values for `date format`:
    `typical`, `dd mon.yyyy`, `d mon.yyyy`, `dd/mm yyyy`, `yyyymmdd`
- Option `database/profession`
- Option `profession code`
- Option `info separators`
- `\gtrDBprofession`
- `\gtrPrintProfession`
- `\gtrifprofessiondefined`
- Environment `gtrinfolist`
- ``

### Changed
- Option settings for `database format`
   updated to process `database/comment` and `database/profession`.
- Implementation for level sensitive variables changed to
  support extension packages.
- Implementation for `\gtruselibrary` changed to support
  third party extension packages.



## [1.01] - 2016-07-29

### Added
- Option `tikz`
- Option `genealogytree extra edges scope`
- Tutorial *Multi-Ancestors*

### Changed
- Family options like `pivot shift` are now applicable
  for `options for family` and `gtrsetoptionsforfamily`.



## [1.00] - 2015-09-21

### Added
- Template `database relationship`

### Changed
- Library loading made compatible with expl3.



## [0.91 beta] - 2015-06-22

### Added
- Option `id prefix`
- Option `id suffix`
- Template `database sideways`
- Tutorial *Externalization*
- Tutorial *Conversion*
- Option `date format` complemented with many more formats.

### Changed
- Settings for `date range full` and `date range separator` changed.

### Fixed
- `phantom` and `phantom*` switch off more settings of `tcolorbox`.



## [0.90 beta] - 2015-05-22

### Added
- First functional beta release.
- Full genealogy tree customization, tree positioning, input insertion and deletion,
  edge customization.
- Database processing.
- Genealogy symbols.
- Internationalization.
- Templates library.
- Tutorials.



## [0.10 alpha] - 2015-01-12

### Added
- Initial public release (alpha version).
- Grammar and Debugger as preview release.



## [0.00] - 2013-2014

### Added
- Pre publication development.



[v2.1.0] https://github.com/T-F-S/genealogytree/compare/v2.01...2.1.0
[v2.01] https://github.com/T-F-S/genealogytree/compare/v2.00...v2.01

