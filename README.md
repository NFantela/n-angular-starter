===========================================
# !!!!!!!!!!!!!! SCSS SETUP !!!!!!!!!!!!!!
===========================================
# WORKFLOW
- create scss file in file folder e.g. demo badge
- it has 2 mixins {name}-theme($theme) and {name}-typography($typoConfig)
- import theme mixin in _master-theme.scss 
- import typography mixin in _typography.scss

<h3>Edit colors in theme/palette.scss</h3>
<h3>Edit typography in typography/typo-config.scss</h3>
===========================================
# Directive scss importing
- Components have their own scss files hovewer directives e.g.
demo badge directive must have their own .scss files inside their modules like _demo-badge.scss and are loaded in main theme file in the end.

<h3> Directive scss file mixin example </h3>
-- theme scss files contain 2 mixins 1 for element and 1 for its typography e.g.
@mixin demo-badge-theme($theme) // $theme is colors
@mixin demo-badge-typography($config) 
-- additionaly it may containt optional mixins that must be included in main 2 above

# Variables file style/variables.scss
-- includex breakpoints and animation curves, the colors come from theme
# Coloring elements
add special classes e.g. color-primary, color-secondary
========================================
==================
# 1 TYPOGRAPHY
--- typo_utils (functions) --> typo_config (creates config & starting css) --> _typography create-typography($config: null) 

=========================================
# 2 ACCESIBILITY a11y
=========================================
-- only hidden class for now
=========================================
# 3 THEME
- pallette.scss
---- contains palletes of colors - generator : http://mcg.mbitson.com/
---- also contains background / foreground maps for light / dark themes
- theming.scss

=========================================
# HELPERS 
 e.g. @function em() // converts to em values uses fixed font size as 2nd argument found in variables.scss
=========================================
# LAYOUT
-- we have container class defined and it is sufficient to use media-queries($break) mixin from _media-queries 
inside elements css e.g.
section {
    // using media queries inside css selectors
    @include media-queries(large){
        width: 33%;
        display:inline-block;
    }
}
=========================================

# END - _core.scss
-- imports above stuff
-- prebuilt-themes - this ones we can include in styles.scss 