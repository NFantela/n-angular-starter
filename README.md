===========================================
# !!!!!!!!!!!!!! SCSS SETUP !!!!!!!!!!!!!!
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
--- pallette 
=========================================

# END - _core.scss
-- imports above stuff