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
---------------------------------------------
# TYPOGRAPHY
scss / typography
--typp-utils.scss - utility functions for fetching font specific data from config and genereting font css
--- # TYPOGRAPHY CONFIG - via mat-typography-config() fn