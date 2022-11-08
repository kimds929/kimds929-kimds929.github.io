---
layout: single
title: "DataAnalysis Basic Intro"
categories: python_basic
tag: [python, basic]
toc: true
---



<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>DataAnalysis_Basic00_Intro(Ipynb)</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; margin: 0; }
td.linenos pre { color: #000000; background-color: #f0f0f0; padding-left: 5px; padding-right: 5px; }
span.linenos { color: #000000; background-color: #f0f0f0; padding-left: 5px; padding-right: 5px; }
td.linenos pre.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>



<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/*
 * Phosphor
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
/*!

Copyright 2015-present Palantir Technologies, Inc. All rights reserved.
Licensed under the Apache License, Version 2.0.

*/
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  text-transform:none;
  line-height:1.28581;
  letter-spacing:0;
  font-size:14px;
  font-weight:400;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-top:0;
  margin-bottom:10px; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  line-height:40px;
  font-size:36px; }

h2.bp3-heading, .bp3-running-text h2{
  line-height:32px;
  font-size:28px; }

h3.bp3-heading, .bp3-running-text h3{
  line-height:25px;
  font-size:22px; }

h4.bp3-heading, .bp3-running-text h4{
  line-height:21px;
  font-size:18px; }

h5.bp3-heading, .bp3-running-text h5{
  line-height:19px;
  font-size:16px; }

h6.bp3-heading, .bp3-running-text h6{
  line-height:16px;
  font-size:14px; }
.bp3-ui-text{
  text-transform:none;
  line-height:1.28581;
  letter-spacing:0;
  font-size:14px;
  font-weight:400; }

.bp3-monospace-text{
  text-transform:none;
  font-family:monospace; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  line-height:1.5;
  font-size:14px; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    margin:20px 0;
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15); }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  text-decoration:none;
  color:#106ba3; }
  a:hover{
    cursor:pointer;
    text-decoration:underline;
    color:#106ba3; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  text-transform:none;
  font-family:monospace;
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  background:rgba(255, 255, 255, 0.7);
  padding:2px 5px;
  color:#5c7080;
  font-size:smaller; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  text-transform:none;
  font-family:monospace;
  display:block;
  margin:10px 0;
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  background:rgba(255, 255, 255, 0.7);
  padding:13px 15px 12px;
  line-height:1.4;
  color:#182026;
  font-size:13px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none;
    padding:0;
    color:inherit;
    font-size:inherit; }

.bp3-running-text kbd, .bp3-key{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  min-width:24px;
  height:24px;
  padding:3px 6px;
  vertical-align:middle;
  line-height:24px;
  color:#5c7080;
  font-family:inherit;
  font-size:12px; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    background:#394b59;
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  margin:0 0 10px;
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  margin:0;
  padding:0;
  list-style:none; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    margin-top:0;
    margin-right:20px;
    font-size:40px; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  margin:0;
  cursor:default;
  height:30px;
  padding:0;
  list-style:none; }
  .bp3-breadcrumbs > li{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center; }
    .bp3-breadcrumbs > li::after{
      display:block;
      margin:0 5px;
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 0 0-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 0 0 1.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      width:16px;
      height:16px;
      content:""; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    vertical-align:baseline;
    font-size:inherit;
    font-weight:inherit; }

.bp3-breadcrumbs-collapsed{
  margin-right:2px;
  border:none;
  border-radius:3px;
  background:#ced9e0;
  cursor:pointer;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    display:block;
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    width:16px;
    height:16px;
    content:""; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    text-decoration:none;
    color:#182026; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  padding:5px 10px;
  vertical-align:middle;
  text-align:left;
  font-size:14px;
  min-width:30px;
  min-height:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
      background-clip:padding-box;
      background-color:#ebf1f5; }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#d8e1e8;
      background-image:none; }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      outline:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#106ba3; }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#0e5a8a;
      background-image:none; }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#0d8050; }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#0a6640;
      background-image:none; }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#bf7326; }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#a66321;
      background-image:none; }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#c23030; }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#a82a2a;
      background-image:none; }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-width:40px;
    min-height:40px;
    padding:5px 15px;
    font-size:16px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-width:24px;
    min-height:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      position:absolute;
      margin:0; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-image:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none; }
    .bp3-button.bp3-minimal:hover{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(167, 182, 194, 0.3);
      text-decoration:none;
      color:#182026; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(115, 134, 148, 0.3);
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        cursor:not-allowed;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-top-left-radius:0;
    border-bottom-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:-1px;
    border-top-right-radius:0;
    border-bottom-right-radius:0; }
  .bp3-button-group.bp3-minimal .bp3-button{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(167, 182, 194, 0.3);
      text-decoration:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(115, 134, 148, 0.3);
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        cursor:not-allowed;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      width:unset;
      height:100%; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  line-height:1.5;
  font-size:14px;
  position:relative;
  border-radius:3px;
  background-color:rgba(138, 155, 168, 0.15);
  width:100%;
  padding:10px 12px 9px; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      position:absolute;
      top:10px;
      left:10px;
      color:#5c7080; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      position:absolute;
      top:10px;
      left:10px;
      color:#5c7080; }
  .bp3-callout .bp3-heading{
    margin-top:0;
    margin-bottom:5px;
    line-height:20px; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  background-color:#ffffff;
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
    background-color:#30404d; }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  opacity:0.9;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  margin:5px;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  border-bottom:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:100%;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }

.bp3-dialog{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background:#ebf1f5;
  width:500px;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background:#293742;
    color:#f5f8fa; }

.bp3-dialog-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  background:#ffffff;
  min-height:40px;
  padding-right:5px;
  padding-left:20px; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px;
    color:#5c7080; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    margin:0;
    line-height:inherit; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
    background:#30404d; }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  margin:20px;
  line-height:18px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-drawer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    top:0;
    right:0;
    left:0;
    height:50%; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-bottom{
    right:0;
    bottom:0;
    left:0;
    height:50%; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-left{
    top:0;
    bottom:0;
    left:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-right{
    top:0;
    right:0;
    bottom:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    top:0;
    right:0;
    bottom:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    right:0;
    bottom:0;
    left:0;
    height:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background:#30404d;
    color:#f5f8fa; }

.bp3-drawer-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:relative;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  min-height:40px;
  padding:5px;
  padding-left:20px; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px;
    color:#5c7080; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    margin:0;
    line-height:inherit; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  overflow:auto;
  line-height:18px; }

.bp3-drawer-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  position:relative;
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  padding:10px 20px; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  display:inline-block;
  position:relative;
  cursor:text;
  max-width:100%;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    position:absolute;
    top:-3px;
    right:-3px;
    bottom:-3px;
    left:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
    background-color:#ffffff; }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background-color:rgba(16, 22, 26, 0.3); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  display:inherit;
  position:relative;
  min-width:inherit;
  max-width:inherit;
  vertical-align:top;
  text-transform:inherit;
  letter-spacing:inherit;
  color:inherit;
  font:inherit;
  resize:none; }

.bp3-editable-text-input{
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none;
  width:100%;
  padding:0;
  white-space:pre-wrap; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    position:absolute;
    left:0;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    z-index:2;
    border-radius:inherit; }
    .bp3-control-group .bp3-input:focus{
      z-index:14;
      border-radius:3px; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    z-index:4;
    border-radius:inherit; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group:not(.bp3-vertical) > *{
    margin-right:-1px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *{
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    margin-right:0;
    border-radius:0 3px 3px 0; }
  .bp3-control-group > :only-child{
    margin-right:0;
    border-radius:3px; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      margin-top:0;
      border-radius:3px 3px 0 0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  display:block;
  position:relative;
  margin-bottom:10px;
  cursor:pointer;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#106ba3; }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#0e5a8a; }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(19, 124, 189, 0.5); }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#106ba3; }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#0e5a8a; }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(14, 90, 138, 0.5); }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    position:absolute;
    top:0;
    left:0;
    opacity:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    display:inline-block;
    position:relative;
    margin-top:-3px;
    margin-right:10px;
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    cursor:pointer;
    width:1em;
    height:1em;
    vertical-align:middle;
    font-size:16px;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none; }
    .bp3-control .bp3-control-indicator::before{
      display:block;
      width:1em;
      height:1em;
      content:""; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#d8e1e8; }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-top:1px;
    margin-left:10px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#106ba3; }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#0e5a8a; }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(19, 124, 189, 0.5); }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#106ba3; }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(14, 90, 138, 0.5); }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 0 0-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0 0 12 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    width:auto;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      position:absolute;
      left:0;
      margin:2px;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      background:#ffffff;
      width:calc(1em - 4px);
      height:calc(1em - 4px);
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background:#394b59; }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    text-align:center;
    font-size:0.7em; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    visibility:hidden;
    margin-right:1.2em;
    margin-left:0.5em;
    line-height:0; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    visibility:visible;
    margin-right:0.5em;
    margin-left:1.2em;
    line-height:1em; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    visibility:visible;
    line-height:1em; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    visibility:hidden;
    line-height:0; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0)); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background:#202b33; }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  display:inline-block;
  position:relative;
  cursor:pointer;
  height:30px; }
  .bp3-file-input input{
    opacity:0;
    margin:0;
    min-width:200px; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(206, 217, 224, 0.5);
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6);
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        outline:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        cursor:not-allowed;
        color:rgba(92, 112, 128, 0.6); }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:rgba(57, 75, 89, 0.5);
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          -webkit-box-shadow:none;
                  box-shadow:none;
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  outline:none;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  height:30px;
  padding:0 10px;
  vertical-align:middle;
  line-height:30px;
  color:#182026;
  font-size:14px;
  font-weight:400;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  position:absolute;
  top:0;
  right:0;
  left:0;
  padding-right:80px;
  color:rgba(92, 112, 128, 0.6);
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6);
    resize:none; }
  .bp3-file-upload-input::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    color:#182026;
    min-width:24px;
    min-height:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    position:absolute;
    top:0;
    right:0;
    margin:3px;
    border-radius:3px;
    width:70px;
    text-align:center;
    line-height:24px;
    content:"Browse"; }
    .bp3-file-upload-input::after:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
      background-clip:padding-box;
      background-color:#ebf1f5; }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#d8e1e8;
      background-image:none; }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      outline:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-file-upload-input:active::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-large .bp3-file-upload-input{
    height:40px;
    line-height:40px;
    font-size:16px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-width:30px;
      min-height:30px;
      margin:5px;
      width:85px;
      line-height:30px; }
  .bp3-dark .bp3-file-upload-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
        background-color:#30404d; }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
        background-color:#202b33;
        background-image:none; }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-file-upload-input:active::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }

.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    margin-top:5px;
    color:#5c7080;
    font-size:12px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      margin:0 10px 0 0;
      line-height:40px; }
    .bp3-form-group.bp3-inline label.bp3-label{
      margin:0 10px 0 0;
      line-height:30px; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-width:24px;
    min-height:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-icon{
    z-index:1;
    color:#5c7080; }
    .bp3-input-group > .bp3-icon:empty{
      line-height:1;
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-width:30px;
    min-height:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    height:40px;
    line-height:40px;
    font-size:16px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-width:20px;
    min-height:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-width:20px;
    min-height:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    height:24px;
    padding-right:8px;
    padding-left:8px;
    line-height:24px;
    font-size:12px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  outline:none;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  height:30px;
  padding:0 10px;
  vertical-align:middle;
  line-height:30px;
  color:#182026;
  font-size:14px;
  font-weight:400;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none; }
  .bp3-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6);
    resize:none; }
  .bp3-input.bp3-large{
    height:40px;
    line-height:40px;
    font-size:16px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    height:24px;
    padding-right:8px;
    padding-left:8px;
    line-height:24px;
    font-size:12px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-top:0;
  margin-bottom:15px; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    width:100%;
    vertical-align:top;
    font-weight:400; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  width:30px;
  min-height:0;
  padding:0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  padding:5px 10px;
  vertical-align:middle;
  text-align:left;
  font-size:14px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  color:#182026;
  border-radius:3px;
  width:100%;
  height:30px;
  padding:0 25px 0 10px;
  -moz-appearance:none;
  -webkit-appearance:none; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    outline:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(167, 182, 194, 0.3);
    text-decoration:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(115, 134, 148, 0.3);
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  height:40px;
  padding-right:35px;
  font-size:16px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#30404d; }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#202b33;
    background-image:none; }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  -webkit-box-shadow:none;
          box-shadow:none;
  background-color:rgba(206, 217, 224, 0.5);
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  position:absolute;
  top:7px;
  right:7px;
  color:#5c7080;
  pointer-events:none; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  position:relative;
  vertical-align:middle;
  letter-spacing:normal; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    top:12px;
    right:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  line-height:1;
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    vertical-align:top;
    text-align:left; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-top:6px;
  padding-bottom:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(92, 112, 128, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
    -webkit-box-shadow:none;
            box-shadow:none; }

.bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(92, 112, 128, 0.3);
  cursor:pointer; }

.bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  top:40px;
  padding-bottom:0; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-right:0;
  margin-left:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  line-height:1;
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  line-height:1;
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  line-height:1;
  font-family:"Icons20";
  font-size:inherit;
  font-weight:400;
  font-style:normal; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  margin:0;
  border-radius:3px;
  background:#ffffff;
  min-width:180px;
  padding:5px;
  list-style:none;
  text-align:left;
  color:#182026; }

.bp3-menu-divider{
  display:block;
  margin:5px;
  border-top:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  padding:5px 7px;
  text-decoration:none;
  line-height:20px;
  color:inherit;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    margin-top:2px;
    color:#5c7080; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    outline:none !important;
    background-color:inherit !important;
    cursor:not-allowed !important;
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    padding:9px 7px;
    line-height:22px;
    font-size:16px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-top:1px;
      margin-right:10px; }

button.bp3-menu-item{
  border:none;
  background:none;
  width:100%;
  text-align:left; }
.bp3-menu-header{
  display:block;
  margin:5px;
  border-top:1px solid rgba(16, 22, 26, 0.15);
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    margin:0;
    padding:10px 7px 0 1px;
    line-height:17px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    padding-top:15px;
    padding-bottom:5px;
    font-size:18px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item.bp3-intent-primary{
  color:#48aff0; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
    color:#48aff0; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
    background-color:#137cbd; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
    background-color:#106ba3; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-success{
  color:#3dcc91; }
  .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
    color:#3dcc91; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
    background-color:#0f9960; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:active{
    background-color:#0d8050; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-warning{
  color:#ffb366; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
    color:#ffb366; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
    background-color:#d9822b; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
    background-color:#bf7326; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-danger{
  color:#ff7373; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
    color:#ff7373; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
    background-color:#db3737; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
    background-color:#c23030; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item::before,
.bp3-dark .bp3-menu-item > .bp3-icon{
  color:#a7b6c2; }

.bp3-dark .bp3-menu-item .bp3-menu-item-label{
  color:#a7b6c2; }

.bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
  background-color:rgba(138, 155, 168, 0.3); }

.bp3-dark .bp3-menu-item.bp3-disabled{
  color:rgba(167, 182, 194, 0.6) !important; }
  .bp3-dark .bp3-menu-item.bp3-disabled::before,
  .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
  .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
    color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  position:relative;
  z-index:10;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  width:100%;
  height:50px;
  padding:0 15px; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    position:fixed;
    top:0;
    right:0;
    left:0; }

.bp3-navbar-heading{
  margin-right:15px;
  font-size:16px; }

.bp3-navbar-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  margin:0 10px;
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:100%;
  height:100%;
  text-align:center; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  position:static;
  top:0;
  right:0;
  bottom:0;
  left:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    position:fixed;
    overflow:hidden; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    position:fixed;
    overflow:auto; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  position:fixed;
  top:0;
  right:0;
  bottom:0;
  left:0;
  opacity:1;
  z-index:20;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  position:relative;
  overflow:hidden; }

.bp3-panel-stack-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  z-index:1;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  height:30px; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1;
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  position:absolute;
  top:0;
  right:0;
  bottom:0;
  left:0;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  background-color:#ffffff;
  overflow-y:auto; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  display:inline-block;
  z-index:20;
  border-radius:3px; }
  .bp3-popover .bp3-popover-arrow{
    position:absolute;
    width:30px;
    height:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      margin:5px;
      width:20px;
      height:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-top:-17px;
    margin-bottom:17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-right:17px;
    margin-left:-17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover .bp3-popover-content{
    position:relative;
    border-radius:3px; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
        -webkit-transition-delay:0;
                transition-delay:0; }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
        -webkit-transition-delay:0;
                transition-delay:0; }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg);
  border-radius:2px;
  content:""; }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  position:absolute;
  top:0;
  right:0;
  left:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  display:block;
  position:relative;
  border-radius:40px;
  background:rgba(92, 112, 128, 0.2);
  width:100%;
  height:8px;
  overflow:hidden; }
  .bp3-progress-bar .bp3-progress-meter{
    position:absolute;
    border-radius:40px;
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    width:100%;
    height:100%;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    border-color:rgba(206, 217, 224, 0.2);
    background:rgba(206, 217, 224, 0.2); }
  to{
    border-color:rgba(92, 112, 128, 0.2);
    background:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    border-color:rgba(206, 217, 224, 0.2);
    background:rgba(206, 217, 224, 0.2); }
  to{
    border-color:rgba(92, 112, 128, 0.2);
    background:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  cursor:default;
  color:transparent !important;
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  width:100%;
  min-width:150px;
  height:40px;
  position:relative;
  outline:none;
  cursor:default;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    opacity:0.5;
    cursor:not-allowed; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  top:5px;
  right:0;
  left:0;
  height:6px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  color:#182026;
  position:absolute;
  top:0;
  left:0;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  width:16px;
  height:16px; }
  .bp3-slider-handle:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    outline:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5;
    z-index:2;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab; }
  .bp3-slider-handle.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:#bfccd6;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none;
    background:#5c7080; }
  .bp3-slider-handle .bp3-slider-label{
    margin-left:8px;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    background:#394b59;
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      background:#e1e8ed;
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-top-right-radius:0;
    border-bottom-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    margin-left:8px;
    border-top-left-radius:0;
    border-bottom-left-radius:0; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  position:absolute;
  padding:2px 5px;
  vertical-align:top;
  line-height:1;
  font-size:12px; }

.bp3-slider.bp3-vertical{
  width:40px;
  min-width:40px;
  height:150px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:0;
    bottom:0;
    left:5px;
    width:6px;
    height:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-top:-8px;
      margin-left:0; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      margin-left:0;
      width:16px;
      height:8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-top-left-radius:0;
      border-bottom-right-radius:3px; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      margin-bottom:8px;
      border-top-left-radius:3px;
      border-bottom-left-radius:0;
      border-bottom-right-radius:0; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round; }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      width:100%;
      padding:0 10px; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(19, 124, 189, 0.2); }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      top:0;
      right:0;
      bottom:0;
      left:0;
      border-radius:3px;
      background-color:rgba(19, 124, 189, 0.2);
      height:auto; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  position:relative;
  margin:0;
  border:none;
  padding:0;
  list-style:none; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  position:relative;
  cursor:pointer;
  max-width:100%;
  vertical-align:top;
  line-height:30px;
  color:#182026;
  font-size:14px; }
  .bp3-tab a{
    display:block;
    text-decoration:none;
    color:inherit; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    background-color:transparent !important; }
  .bp3-tab[aria-disabled="true"]{
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    line-height:40px;
    font-size:16px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  position:absolute;
  top:0;
  left:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
  pointer-events:none; }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    position:absolute;
    right:0;
    bottom:0;
    left:0;
    background-color:#106ba3;
    height:3px; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:relative;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  background-color:#5c7080;
  min-width:20px;
  max-width:100%;
  min-height:20px;
  padding:2px 6px;
  line-height:16px;
  color:#f5f8fa;
  font-size:12px; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-right:8px;
    padding-left:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    min-width:30px;
    min-height:30px;
    padding:0 10px;
    line-height:20px;
    font-size:14px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-right:12px;
      padding-left:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  opacity:0.5;
  margin-top:-2px;
  margin-right:-6px !important;
  margin-bottom:-2px;
  border:none;
  background:none;
  cursor:pointer;
  padding:2px;
  padding-left:0;
  color:inherit; }
  .bp3-tag-remove:hover{
    opacity:0.8;
    background:none;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:5px;
    padding-left:0; }
    .bp3-large .bp3-tag-remove:empty::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  min-height:30px;
  padding-right:0;
  padding-left:5px;
  line-height:inherit; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    margin-top:7px;
    margin-right:7px;
    margin-left:2px;
    color:#5c7080; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    margin-top:5px;
    margin-right:7px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:80px;
    line-height:20px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-width:24px;
    min-height:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-top:10px;
      margin-left:5px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-width:30px;
      min-height:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
    background-color:#ffffff; }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background-color:rgba(16, 22, 26, 0.3); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  position:relative !important;
  margin:20px 0 0;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  min-width:300px;
  max-width:500px;
  pointer-events:all; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:50ms;
            transition-delay:50ms; }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    margin:12px;
    margin-right:0;
    color:#5c7080; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
    background-color:#394b59; }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:fixed;
  right:0;
  left:0;
  z-index:40;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0;
    bottom:auto; }
  .bp3-toast-container.bp3-toast-container-bottom{
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto;
    bottom:0; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    position:absolute;
    width:22px;
    height:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      margin:4px;
      width:14px;
      height:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-top:-11px;
    margin-bottom:11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-right:11px;
    margin-left:-11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  margin:0;
  padding-left:0;
  list-style:none; }

.bp3-tree-root{
  position:relative;
  background-color:transparent;
  cursor:default;
  padding-left:0; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  width:100%;
  height:30px;
  padding-right:5px; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  cursor:pointer;
  padding:7px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  position:relative;
  margin-right:7px; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
/*!

Copyright 2017-present Palantir Technologies, Inc. All rights reserved.
Licensed under the Apache License, Version 2.0.

*/
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  top:20vh;
  left:calc(50% - 250px);
  z-index:21;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  width:500px; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-omnibar .bp3-input{
    border-radius:0;
    background-color:transparent; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    background-color:transparent;
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background-color:#30404d; }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDhoLTIuODFjLS40NS0uNzgtMS4wNy0xLjQ1LTEuODItMS45NkwxNyA0LjQxIDE1LjU5IDNsLTIuMTcgMi4xN0MxMi45NiA1LjA2IDEyLjQ5IDUgMTIgNWMtLjQ5IDAtLjk2LjA2LTEuNDEuMTdMOC40MSAzIDcgNC40MWwxLjYyIDEuNjNDNy44OCA2LjU1IDcuMjYgNy4yMiA2LjgxIDhINHYyaDIuMDljLS4wNS4zMy0uMDkuNjYtLjA5IDF2MUg0djJoMnYxYzAgLjM0LjA0LjY3LjA5IDFINHYyaDIuODFjMS4wNCAxLjc5IDIuOTcgMyA1LjE5IDNzNC4xNS0xLjIxIDUuMTktM0gyMHYtMmgtMi4wOWMuMDUtLjMzLjA5LS42Ni4wOS0xdi0xaDJ2LTJoLTJ2LTFjMC0uMzQtLjA0LS42Ny0uMDktMUgyMFY4em0tNiA4aC00di0yaDR2MnptMC00aC00di0yaDR2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTYuMTdMNC44MyAxMmwtMS40MiAxLjQxTDkgMTkgMjEgN2wtMS40MS0xLjQxeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pg0KPHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4Ig0KCSB2aWV3Qm94PSIwIDAgNTAuOTc4IDUwLjk3OCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgNTAuOTc4IDUwLjk3ODsiIHhtbDpzcGFjZT0icHJlc2VydmUiPg0KPGc+DQoJPGc+DQoJCTxnPg0KCQkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik00My41Miw3LjQ1OEMzOC43MTEsMi42NDgsMzIuMzA3LDAsMjUuNDg5LDBDMTguNjcsMCwxMi4yNjYsMi42NDgsNy40NTgsNy40NTgNCgkJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDANCgkJCQljNi44MTYsMCwxMy4yMjEtMi42NDgsMTguMDI5LTcuNDU4YzQuODA5LTQuODA5LDcuNDU3LTExLjIxMiw3LjQ1Ny0xOC4wM0M1MC45NzcsMTguNjcsNDguMzI4LDEyLjI2Niw0My41Miw3LjQ1OHoNCgkJCQkgTTQyLjEwNiw0Mi4xMDVjLTQuNDMyLDQuNDMxLTEwLjMzMiw2Ljg3Mi0xNi42MTUsNi44NzJoLTAuMDAyYy02LjI4NS0wLjAwMS0xMi4xODctMi40NDEtMTYuNjE3LTYuODcyDQoJCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzINCgkJCQljNC40MzEsNC40MzEsNi44NzEsMTAuMzMyLDYuODcxLDE2LjYxN0M0OC45NzcsMzEuNzcyLDQ2LjUzNiwzNy42NzUsNDIuMTA2LDQyLjEwNXoiLz4NCgkJPC9nPg0KCQk8Zz4NCgkJCTxwYXRoIHN0eWxlPSJmaWxsOiMwMTAwMDI7IiBkPSJNMjMuNTc4LDMyLjIxOGMtMC4wMjMtMS43MzQsMC4xNDMtMy4wNTksMC40OTYtMy45NzJjMC4zNTMtMC45MTMsMS4xMS0xLjk5NywyLjI3Mi0zLjI1Mw0KCQkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUNCgkJCQljMC0xLjA5Ni0wLjI2LTIuMDg4LTAuNzc5LTIuOTc5Yy0wLjU2NS0wLjg3OS0xLjUwMS0xLjMzNi0yLjgwNi0xLjM2OWMtMS44MDIsMC4wNTctMi45ODUsMC42NjctMy41NSwxLjgzMg0KCQkJCWMtMC4zMDEsMC41MzUtMC41MDMsMS4xNDEtMC42MDcsMS44MTRjLTAuMTM5LDAuNzA3LTAuMjA3LDEuNDMyLTAuMjA3LDIuMTc0aC0yLjkzN2MtMC4wOTEtMi4yMDgsMC40MDctNC4xMTQsMS40OTMtNS43MTkNCgkJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQ0KCQkJCWMwLDEuMTQyLTAuMTM3LDIuMTExLTAuNDEsMi45MTFjLTAuMzA5LDAuODQ1LTAuNzMxLDEuNTkzLTEuMjY4LDIuMjQzYy0wLjQ5MiwwLjY1LTEuMDY4LDEuMzE4LTEuNzMsMi4wMDINCgkJCQljLTAuNjUsMC42OTctMS4zMTMsMS40NzktMS45ODcsMi4zNDZjLTAuMjM5LDAuMzc3LTAuNDI5LDAuNzc3LTAuNTY1LDEuMTk5Yy0wLjE2LDAuOTU5LTAuMjE3LDEuOTUxLTAuMTcxLDIuOTc5DQoJCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+DQoJCTwvZz4NCgk8L2c+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8L3N2Zz4NCg==);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}
.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}
.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}
.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}
.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}
.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}
.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}
.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}
.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}
.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}
.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}
.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}
.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}
.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}
.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}
.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}
.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}
.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}
.jp-FileIcon {
  background-image: var(--jp-icon-file);
}
.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}
.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}
.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}
.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}
.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}
.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}
.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}
.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}
.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}
.jp-ListIcon {
  background-image: var(--jp-icon-list);
}
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}
.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}
.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}
.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}
.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}
.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}
.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}
.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}
.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}
.jp-RunIcon {
  background-image: var(--jp-icon-run);
}
.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}
.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}
.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}
.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}
.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

:root {
  --jp-icon-search-white: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
}

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}
/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}
/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}
/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}
.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}
.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}
.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}
.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}
.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}
.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}
.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}
.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}
/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}
.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}
.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}
.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}
.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}
.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}
.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}
/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) svg {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}
select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.lm-CommandPalette-wrapper::after {
  content: ' ';
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  height: 30px;
  width: 10px;
  padding: 0px 10px;
  background-image: var(--jp-icon-search-white);
  background-size: 20px;
  background-repeat: no-repeat;
  background-position: center;
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color3);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item.lm-mod-active {
  background: var(--jp-layout-color3);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  background: var(--jp-layout-color4);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.4;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty:after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0px 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0px;
  left: 0px;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px;
  padding-bottom: 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

.jp-Dialog-header {
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;

  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;

  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #aa00ff;

  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;

  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;

  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;

  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;

  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;

  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;

  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;

  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;

  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;

  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ffff00;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;

  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;

  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;

  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;

  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;

  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eeeeee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;

  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0px 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 1;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 30px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -30px; margin-right: -30px;
  padding-bottom: 30px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 30px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -30px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*
  Name:       material
  Author:     Mattia Astorino (http://github.com/equinusocio)
  Website:    https://material-theme.site/
*/

.cm-s-material.CodeMirror {
  background-color: #263238;
  color: #EEFFFF;
}

.cm-s-material .CodeMirror-gutters {
  background: #263238;
  color: #546E7A;
  border: none;
}

.cm-s-material .CodeMirror-guttermarker,
.cm-s-material .CodeMirror-guttermarker-subtle,
.cm-s-material .CodeMirror-linenumber {
  color: #546E7A;
}

.cm-s-material .CodeMirror-cursor {
  border-left: 1px solid #FFCC00;
}

.cm-s-material div.CodeMirror-selected {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material.CodeMirror-focused div.CodeMirror-selected {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-line::selection,
.cm-s-material .CodeMirror-line>span::selection,
.cm-s-material .CodeMirror-line>span>span::selection {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-line::-moz-selection,
.cm-s-material .CodeMirror-line>span::-moz-selection,
.cm-s-material .CodeMirror-line>span>span::-moz-selection {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-activeline-background {
  background: rgba(0, 0, 0, 0.5);
}

.cm-s-material .cm-keyword {
  color: #C792EA;
}

.cm-s-material .cm-operator {
  color: #89DDFF;
}

.cm-s-material .cm-variable-2 {
  color: #EEFFFF;
}

.cm-s-material .cm-variable-3,
.cm-s-material .cm-type {
  color: #f07178;
}

.cm-s-material .cm-builtin {
  color: #FFCB6B;
}

.cm-s-material .cm-atom {
  color: #F78C6C;
}

.cm-s-material .cm-number {
  color: #FF5370;
}

.cm-s-material .cm-def {
  color: #82AAFF;
}

.cm-s-material .cm-string {
  color: #C3E88D;
}

.cm-s-material .cm-string-2 {
  color: #f07178;
}

.cm-s-material .cm-comment {
  color: #546E7A;
}

.cm-s-material .cm-variable {
  color: #f07178;
}

.cm-s-material .cm-tag {
  color: #FF5370;
}

.cm-s-material .cm-meta {
  color: #FFCB6B;
}

.cm-s-material .cm-attribute {
  color: #C792EA;
}

.cm-s-material .cm-property {
  color: #C792EA;
}

.cm-s-material .cm-qualifier {
  color: #DECB6B;
}

.cm-s-material .cm-variable-3,
.cm-s-material .cm-type {
  color: #DECB6B;
}


.cm-s-material .cm-error {
  color: rgba(255, 255, 255, 1.0);
  background-color: #FF5370;
}

.cm-s-material .CodeMirror-matchingbracket {
  text-decoration: underline;
  color: white !important;
}
/**
 * "
 *  Using Zenburn color palette from the Emacs Zenburn Theme
 *  https://github.com/bbatsov/zenburn-emacs/blob/master/zenburn-theme.el
 *
 *  Also using parts of https://github.com/xavi/coderay-lighttable-theme
 * "
 * From: https://github.com/wisenomad/zenburn-lighttable-theme/blob/master/zenburn.css
 */

.cm-s-zenburn .CodeMirror-gutters { background: #3f3f3f !important; }
.cm-s-zenburn .CodeMirror-foldgutter-open, .CodeMirror-foldgutter-folded { color: #999; }
.cm-s-zenburn .CodeMirror-cursor { border-left: 1px solid white; }
.cm-s-zenburn { background-color: #3f3f3f; color: #dcdccc; }
.cm-s-zenburn span.cm-builtin { color: #dcdccc; font-weight: bold; }
.cm-s-zenburn span.cm-comment { color: #7f9f7f; }
.cm-s-zenburn span.cm-keyword { color: #f0dfaf; font-weight: bold; }
.cm-s-zenburn span.cm-atom { color: #bfebbf; }
.cm-s-zenburn span.cm-def { color: #dcdccc; }
.cm-s-zenburn span.cm-variable { color: #dfaf8f; }
.cm-s-zenburn span.cm-variable-2 { color: #dcdccc; }
.cm-s-zenburn span.cm-string { color: #cc9393; }
.cm-s-zenburn span.cm-string-2 { color: #cc9393; }
.cm-s-zenburn span.cm-number { color: #dcdccc; }
.cm-s-zenburn span.cm-tag { color: #93e0e3; }
.cm-s-zenburn span.cm-property { color: #dfaf8f; }
.cm-s-zenburn span.cm-attribute { color: #dfaf8f; }
.cm-s-zenburn span.cm-qualifier { color: #7cb8bb; }
.cm-s-zenburn span.cm-meta { color: #f0dfaf; }
.cm-s-zenburn span.cm-header { color: #f0efd0; }
.cm-s-zenburn span.cm-operator { color: #f0efd0; }
.cm-s-zenburn span.CodeMirror-matchingbracket { box-sizing: border-box; background: transparent; border-bottom: 1px solid; }
.cm-s-zenburn span.CodeMirror-nonmatchingbracket { border-bottom: 1px solid; background: none; }
.cm-s-zenburn .CodeMirror-activeline { background: #000000; }
.cm-s-zenburn .CodeMirror-activeline-background { background: #000000; }
.cm-s-zenburn div.CodeMirror-selected { background: #545454; }
.cm-s-zenburn .CodeMirror-focused div.CodeMirror-selected { background: #4f4f4f; }

.cm-s-abcdef.CodeMirror { background: #0f0f0f; color: #defdef; }
.cm-s-abcdef div.CodeMirror-selected { background: #515151; }
.cm-s-abcdef .CodeMirror-line::selection, .cm-s-abcdef .CodeMirror-line > span::selection, .cm-s-abcdef .CodeMirror-line > span > span::selection { background: rgba(56, 56, 56, 0.99); }
.cm-s-abcdef .CodeMirror-line::-moz-selection, .cm-s-abcdef .CodeMirror-line > span::-moz-selection, .cm-s-abcdef .CodeMirror-line > span > span::-moz-selection { background: rgba(56, 56, 56, 0.99); }
.cm-s-abcdef .CodeMirror-gutters { background: #555; border-right: 2px solid #314151; }
.cm-s-abcdef .CodeMirror-guttermarker { color: #222; }
.cm-s-abcdef .CodeMirror-guttermarker-subtle { color: azure; }
.cm-s-abcdef .CodeMirror-linenumber { color: #FFFFFF; }
.cm-s-abcdef .CodeMirror-cursor { border-left: 1px solid #00FF00; }

.cm-s-abcdef span.cm-keyword { color: darkgoldenrod; font-weight: bold; }
.cm-s-abcdef span.cm-atom { color: #77F; }
.cm-s-abcdef span.cm-number { color: violet; }
.cm-s-abcdef span.cm-def { color: #fffabc; }
.cm-s-abcdef span.cm-variable { color: #abcdef; }
.cm-s-abcdef span.cm-variable-2 { color: #cacbcc; }
.cm-s-abcdef span.cm-variable-3, .cm-s-abcdef span.cm-type { color: #def; }
.cm-s-abcdef span.cm-property { color: #fedcba; }
.cm-s-abcdef span.cm-operator { color: #ff0; }
.cm-s-abcdef span.cm-comment { color: #7a7b7c; font-style: italic;}
.cm-s-abcdef span.cm-string { color: #2b4; }
.cm-s-abcdef span.cm-meta { color: #C9F; }
.cm-s-abcdef span.cm-qualifier { color: #FFF700; }
.cm-s-abcdef span.cm-builtin { color: #30aabc; }
.cm-s-abcdef span.cm-bracket { color: #8a8a8a; }
.cm-s-abcdef span.cm-tag { color: #FFDD44; }
.cm-s-abcdef span.cm-attribute { color: #DDFF00; }
.cm-s-abcdef span.cm-error { color: #FF0000; }
.cm-s-abcdef span.cm-header { color: aquamarine; font-weight: bold; }
.cm-s-abcdef span.cm-link { color: blueviolet; }

.cm-s-abcdef .CodeMirror-activeline-background { background: #314151; }

/*

    Name:       Base16 Default Light
    Author:     Chris Kempson (http://chriskempson.com)

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-base16-light.CodeMirror { background: #f5f5f5; color: #202020; }
.cm-s-base16-light div.CodeMirror-selected { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-line::selection, .cm-s-base16-light .CodeMirror-line > span::selection, .cm-s-base16-light .CodeMirror-line > span > span::selection { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-line::-moz-selection, .cm-s-base16-light .CodeMirror-line > span::-moz-selection, .cm-s-base16-light .CodeMirror-line > span > span::-moz-selection { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-gutters { background: #f5f5f5; border-right: 0px; }
.cm-s-base16-light .CodeMirror-guttermarker { color: #ac4142; }
.cm-s-base16-light .CodeMirror-guttermarker-subtle { color: #b0b0b0; }
.cm-s-base16-light .CodeMirror-linenumber { color: #b0b0b0; }
.cm-s-base16-light .CodeMirror-cursor { border-left: 1px solid #505050; }

.cm-s-base16-light span.cm-comment { color: #8f5536; }
.cm-s-base16-light span.cm-atom { color: #aa759f; }
.cm-s-base16-light span.cm-number { color: #aa759f; }

.cm-s-base16-light span.cm-property, .cm-s-base16-light span.cm-attribute { color: #90a959; }
.cm-s-base16-light span.cm-keyword { color: #ac4142; }
.cm-s-base16-light span.cm-string { color: #f4bf75; }

.cm-s-base16-light span.cm-variable { color: #90a959; }
.cm-s-base16-light span.cm-variable-2 { color: #6a9fb5; }
.cm-s-base16-light span.cm-def { color: #d28445; }
.cm-s-base16-light span.cm-bracket { color: #202020; }
.cm-s-base16-light span.cm-tag { color: #ac4142; }
.cm-s-base16-light span.cm-link { color: #aa759f; }
.cm-s-base16-light span.cm-error { background: #ac4142; color: #505050; }

.cm-s-base16-light .CodeMirror-activeline-background { background: #DDDCDC; }
.cm-s-base16-light .CodeMirror-matchingbracket { color: #f5f5f5 !important; background-color: #6A9FB5 !important}

/*

    Name:       Base16 Default Dark
    Author:     Chris Kempson (http://chriskempson.com)

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-base16-dark.CodeMirror { background: #151515; color: #e0e0e0; }
.cm-s-base16-dark div.CodeMirror-selected { background: #303030; }
.cm-s-base16-dark .CodeMirror-line::selection, .cm-s-base16-dark .CodeMirror-line > span::selection, .cm-s-base16-dark .CodeMirror-line > span > span::selection { background: rgba(48, 48, 48, .99); }
.cm-s-base16-dark .CodeMirror-line::-moz-selection, .cm-s-base16-dark .CodeMirror-line > span::-moz-selection, .cm-s-base16-dark .CodeMirror-line > span > span::-moz-selection { background: rgba(48, 48, 48, .99); }
.cm-s-base16-dark .CodeMirror-gutters { background: #151515; border-right: 0px; }
.cm-s-base16-dark .CodeMirror-guttermarker { color: #ac4142; }
.cm-s-base16-dark .CodeMirror-guttermarker-subtle { color: #505050; }
.cm-s-base16-dark .CodeMirror-linenumber { color: #505050; }
.cm-s-base16-dark .CodeMirror-cursor { border-left: 1px solid #b0b0b0; }

.cm-s-base16-dark span.cm-comment { color: #8f5536; }
.cm-s-base16-dark span.cm-atom { color: #aa759f; }
.cm-s-base16-dark span.cm-number { color: #aa759f; }

.cm-s-base16-dark span.cm-property, .cm-s-base16-dark span.cm-attribute { color: #90a959; }
.cm-s-base16-dark span.cm-keyword { color: #ac4142; }
.cm-s-base16-dark span.cm-string { color: #f4bf75; }

.cm-s-base16-dark span.cm-variable { color: #90a959; }
.cm-s-base16-dark span.cm-variable-2 { color: #6a9fb5; }
.cm-s-base16-dark span.cm-def { color: #d28445; }
.cm-s-base16-dark span.cm-bracket { color: #e0e0e0; }
.cm-s-base16-dark span.cm-tag { color: #ac4142; }
.cm-s-base16-dark span.cm-link { color: #aa759f; }
.cm-s-base16-dark span.cm-error { background: #ac4142; color: #b0b0b0; }

.cm-s-base16-dark .CodeMirror-activeline-background { background: #202020; }
.cm-s-base16-dark .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*

    Name:       dracula
    Author:     Michael Kaminsky (http://github.com/mkaminsky11)

    Original dracula color scheme by Zeno Rocha (https://github.com/zenorocha/dracula-theme)

*/


.cm-s-dracula.CodeMirror, .cm-s-dracula .CodeMirror-gutters {
  background-color: #282a36 !important;
  color: #f8f8f2 !important;
  border: none;
}
.cm-s-dracula .CodeMirror-gutters { color: #282a36; }
.cm-s-dracula .CodeMirror-cursor { border-left: solid thin #f8f8f0; }
.cm-s-dracula .CodeMirror-linenumber { color: #6D8A88; }
.cm-s-dracula .CodeMirror-selected { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula .CodeMirror-line::selection, .cm-s-dracula .CodeMirror-line > span::selection, .cm-s-dracula .CodeMirror-line > span > span::selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula .CodeMirror-line::-moz-selection, .cm-s-dracula .CodeMirror-line > span::-moz-selection, .cm-s-dracula .CodeMirror-line > span > span::-moz-selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula span.cm-comment { color: #6272a4; }
.cm-s-dracula span.cm-string, .cm-s-dracula span.cm-string-2 { color: #f1fa8c; }
.cm-s-dracula span.cm-number { color: #bd93f9; }
.cm-s-dracula span.cm-variable { color: #50fa7b; }
.cm-s-dracula span.cm-variable-2 { color: white; }
.cm-s-dracula span.cm-def { color: #50fa7b; }
.cm-s-dracula span.cm-operator { color: #ff79c6; }
.cm-s-dracula span.cm-keyword { color: #ff79c6; }
.cm-s-dracula span.cm-atom { color: #bd93f9; }
.cm-s-dracula span.cm-meta { color: #f8f8f2; }
.cm-s-dracula span.cm-tag { color: #ff79c6; }
.cm-s-dracula span.cm-attribute { color: #50fa7b; }
.cm-s-dracula span.cm-qualifier { color: #50fa7b; }
.cm-s-dracula span.cm-property { color: #66d9ef; }
.cm-s-dracula span.cm-builtin { color: #50fa7b; }
.cm-s-dracula span.cm-variable-3, .cm-s-dracula span.cm-type { color: #ffb86c; }

.cm-s-dracula .CodeMirror-activeline-background { background: rgba(255,255,255,0.1); }
.cm-s-dracula .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*

    Name:       Hopscotch
    Author:     Jan T. Sott

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-hopscotch.CodeMirror {background: #322931; color: #d5d3d5;}
.cm-s-hopscotch div.CodeMirror-selected {background: #433b42 !important;}
.cm-s-hopscotch .CodeMirror-gutters {background: #322931; border-right: 0px;}
.cm-s-hopscotch .CodeMirror-linenumber {color: #797379;}
.cm-s-hopscotch .CodeMirror-cursor {border-left: 1px solid #989498 !important;}

.cm-s-hopscotch span.cm-comment {color: #b33508;}
.cm-s-hopscotch span.cm-atom {color: #c85e7c;}
.cm-s-hopscotch span.cm-number {color: #c85e7c;}

.cm-s-hopscotch span.cm-property, .cm-s-hopscotch span.cm-attribute {color: #8fc13e;}
.cm-s-hopscotch span.cm-keyword {color: #dd464c;}
.cm-s-hopscotch span.cm-string {color: #fdcc59;}

.cm-s-hopscotch span.cm-variable {color: #8fc13e;}
.cm-s-hopscotch span.cm-variable-2 {color: #1290bf;}
.cm-s-hopscotch span.cm-def {color: #fd8b19;}
.cm-s-hopscotch span.cm-error {background: #dd464c; color: #989498;}
.cm-s-hopscotch span.cm-bracket {color: #d5d3d5;}
.cm-s-hopscotch span.cm-tag {color: #dd464c;}
.cm-s-hopscotch span.cm-link {color: #c85e7c;}

.cm-s-hopscotch .CodeMirror-matchingbracket { text-decoration: underline; color: white !important;}
.cm-s-hopscotch .CodeMirror-activeline-background { background: #302020; }

/****************************************************************/
/*   Based on mbonaci's Brackets mbo theme                      */
/*   https://github.com/mbonaci/global/blob/master/Mbo.tmTheme  */
/*   Create your own: http://tmtheme-editor.herokuapp.com       */
/****************************************************************/

.cm-s-mbo.CodeMirror { background: #2c2c2c; color: #ffffec; }
.cm-s-mbo div.CodeMirror-selected { background: #716C62; }
.cm-s-mbo .CodeMirror-line::selection, .cm-s-mbo .CodeMirror-line > span::selection, .cm-s-mbo .CodeMirror-line > span > span::selection { background: rgba(113, 108, 98, .99); }
.cm-s-mbo .CodeMirror-line::-moz-selection, .cm-s-mbo .CodeMirror-line > span::-moz-selection, .cm-s-mbo .CodeMirror-line > span > span::-moz-selection { background: rgba(113, 108, 98, .99); }
.cm-s-mbo .CodeMirror-gutters { background: #4e4e4e; border-right: 0px; }
.cm-s-mbo .CodeMirror-guttermarker { color: white; }
.cm-s-mbo .CodeMirror-guttermarker-subtle { color: grey; }
.cm-s-mbo .CodeMirror-linenumber { color: #dadada; }
.cm-s-mbo .CodeMirror-cursor { border-left: 1px solid #ffffec; }

.cm-s-mbo span.cm-comment { color: #95958a; }
.cm-s-mbo span.cm-atom { color: #00a8c6; }
.cm-s-mbo span.cm-number { color: #00a8c6; }

.cm-s-mbo span.cm-property, .cm-s-mbo span.cm-attribute { color: #9ddfe9; }
.cm-s-mbo span.cm-keyword { color: #ffb928; }
.cm-s-mbo span.cm-string { color: #ffcf6c; }
.cm-s-mbo span.cm-string.cm-property { color: #ffffec; }

.cm-s-mbo span.cm-variable { color: #ffffec; }
.cm-s-mbo span.cm-variable-2 { color: #00a8c6; }
.cm-s-mbo span.cm-def { color: #ffffec; }
.cm-s-mbo span.cm-bracket { color: #fffffc; font-weight: bold; }
.cm-s-mbo span.cm-tag { color: #9ddfe9; }
.cm-s-mbo span.cm-link { color: #f54b07; }
.cm-s-mbo span.cm-error { border-bottom: #636363; color: #ffffec; }
.cm-s-mbo span.cm-qualifier { color: #ffffec; }

.cm-s-mbo .CodeMirror-activeline-background { background: #494b41; }
.cm-s-mbo .CodeMirror-matchingbracket { color: #ffb928 !important; }
.cm-s-mbo .CodeMirror-matchingtag { background: rgba(255, 255, 255, .37); }

/*
  MDN-LIKE Theme - Mozilla
  Ported to CodeMirror by Peter Kroon <plakroon@gmail.com>
  Report bugs/issues here: https://github.com/codemirror/CodeMirror/issues
  GitHub: @peterkroon

  The mdn-like theme is inspired on the displayed code examples at: https://developer.mozilla.org/en-US/docs/Web/CSS/animation

*/
.cm-s-mdn-like.CodeMirror { color: #999; background-color: #fff; }
.cm-s-mdn-like div.CodeMirror-selected { background: #cfc; }
.cm-s-mdn-like .CodeMirror-line::selection, .cm-s-mdn-like .CodeMirror-line > span::selection, .cm-s-mdn-like .CodeMirror-line > span > span::selection { background: #cfc; }
.cm-s-mdn-like .CodeMirror-line::-moz-selection, .cm-s-mdn-like .CodeMirror-line > span::-moz-selection, .cm-s-mdn-like .CodeMirror-line > span > span::-moz-selection { background: #cfc; }

.cm-s-mdn-like .CodeMirror-gutters { background: #f8f8f8; border-left: 6px solid rgba(0,83,159,0.65); color: #333; }
.cm-s-mdn-like .CodeMirror-linenumber { color: #aaa; padding-left: 8px; }
.cm-s-mdn-like .CodeMirror-cursor { border-left: 2px solid #222; }

.cm-s-mdn-like .cm-keyword { color: #6262FF; }
.cm-s-mdn-like .cm-atom { color: #F90; }
.cm-s-mdn-like .cm-number { color:  #ca7841; }
.cm-s-mdn-like .cm-def { color: #8DA6CE; }
.cm-s-mdn-like span.cm-variable-2, .cm-s-mdn-like span.cm-tag { color: #690; }
.cm-s-mdn-like span.cm-variable-3, .cm-s-mdn-like span.cm-def, .cm-s-mdn-like span.cm-type { color: #07a; }

.cm-s-mdn-like .cm-variable { color: #07a; }
.cm-s-mdn-like .cm-property { color: #905; }
.cm-s-mdn-like .cm-qualifier { color: #690; }

.cm-s-mdn-like .cm-operator { color: #cda869; }
.cm-s-mdn-like .cm-comment { color:#777; font-weight:normal; }
.cm-s-mdn-like .cm-string { color:#07a; font-style:italic; }
.cm-s-mdn-like .cm-string-2 { color:#bd6b18; } /*?*/
.cm-s-mdn-like .cm-meta { color: #000; } /*?*/
.cm-s-mdn-like .cm-builtin { color: #9B7536; } /*?*/
.cm-s-mdn-like .cm-tag { color: #997643; }
.cm-s-mdn-like .cm-attribute { color: #d6bb6d; } /*?*/
.cm-s-mdn-like .cm-header { color: #FF6400; }
.cm-s-mdn-like .cm-hr { color: #AEAEAE; }
.cm-s-mdn-like .cm-link { color:#ad9361; font-style:italic; text-decoration:none; }
.cm-s-mdn-like .cm-error { border-bottom: 1px solid red; }

div.cm-s-mdn-like .CodeMirror-activeline-background { background: #efefff; }
div.cm-s-mdn-like span.CodeMirror-matchingbracket { outline:1px solid grey; color: inherit; }

.cm-s-mdn-like.CodeMirror { background-image: url(data:image/png;base64,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); }

/*

    Name:       seti
    Author:     Michael Kaminsky (http://github.com/mkaminsky11)

    Original seti color scheme by Jesse Weed (https://github.com/jesseweed/seti-syntax)

*/


.cm-s-seti.CodeMirror {
  background-color: #151718 !important;
  color: #CFD2D1 !important;
  border: none;
}
.cm-s-seti .CodeMirror-gutters {
  color: #404b53;
  background-color: #0E1112;
  border: none;
}
.cm-s-seti .CodeMirror-cursor { border-left: solid thin #f8f8f0; }
.cm-s-seti .CodeMirror-linenumber { color: #6D8A88; }
.cm-s-seti.CodeMirror-focused div.CodeMirror-selected { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti .CodeMirror-line::selection, .cm-s-seti .CodeMirror-line > span::selection, .cm-s-seti .CodeMirror-line > span > span::selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti .CodeMirror-line::-moz-selection, .cm-s-seti .CodeMirror-line > span::-moz-selection, .cm-s-seti .CodeMirror-line > span > span::-moz-selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti span.cm-comment { color: #41535b; }
.cm-s-seti span.cm-string, .cm-s-seti span.cm-string-2 { color: #55b5db; }
.cm-s-seti span.cm-number { color: #cd3f45; }
.cm-s-seti span.cm-variable { color: #55b5db; }
.cm-s-seti span.cm-variable-2 { color: #a074c4; }
.cm-s-seti span.cm-def { color: #55b5db; }
.cm-s-seti span.cm-keyword { color: #ff79c6; }
.cm-s-seti span.cm-operator { color: #9fca56; }
.cm-s-seti span.cm-keyword { color: #e6cd69; }
.cm-s-seti span.cm-atom { color: #cd3f45; }
.cm-s-seti span.cm-meta { color: #55b5db; }
.cm-s-seti span.cm-tag { color: #55b5db; }
.cm-s-seti span.cm-attribute { color: #9fca56; }
.cm-s-seti span.cm-qualifier { color: #9fca56; }
.cm-s-seti span.cm-property { color: #a074c4; }
.cm-s-seti span.cm-variable-3, .cm-s-seti span.cm-type { color: #9fca56; }
.cm-s-seti span.cm-builtin { color: #9fca56; }
.cm-s-seti .CodeMirror-activeline-background { background: #101213; }
.cm-s-seti .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*
Solarized theme for code-mirror
http://ethanschoonover.com/solarized
*/

/*
Solarized color palette
http://ethanschoonover.com/solarized/img/solarized-palette.png
*/

.solarized.base03 { color: #002b36; }
.solarized.base02 { color: #073642; }
.solarized.base01 { color: #586e75; }
.solarized.base00 { color: #657b83; }
.solarized.base0 { color: #839496; }
.solarized.base1 { color: #93a1a1; }
.solarized.base2 { color: #eee8d5; }
.solarized.base3  { color: #fdf6e3; }
.solarized.solar-yellow  { color: #b58900; }
.solarized.solar-orange  { color: #cb4b16; }
.solarized.solar-red { color: #dc322f; }
.solarized.solar-magenta { color: #d33682; }
.solarized.solar-violet  { color: #6c71c4; }
.solarized.solar-blue { color: #268bd2; }
.solarized.solar-cyan { color: #2aa198; }
.solarized.solar-green { color: #859900; }

/* Color scheme for code-mirror */

.cm-s-solarized {
  line-height: 1.45em;
  color-profile: sRGB;
  rendering-intent: auto;
}
.cm-s-solarized.cm-s-dark {
  color: #839496;
  background-color: #002b36;
  text-shadow: #002b36 0 1px;
}
.cm-s-solarized.cm-s-light {
  background-color: #fdf6e3;
  color: #657b83;
  text-shadow: #eee8d5 0 1px;
}

.cm-s-solarized .CodeMirror-widget {
  text-shadow: none;
}

.cm-s-solarized .cm-header { color: #586e75; }
.cm-s-solarized .cm-quote { color: #93a1a1; }

.cm-s-solarized .cm-keyword { color: #cb4b16; }
.cm-s-solarized .cm-atom { color: #d33682; }
.cm-s-solarized .cm-number { color: #d33682; }
.cm-s-solarized .cm-def { color: #2aa198; }

.cm-s-solarized .cm-variable { color: #839496; }
.cm-s-solarized .cm-variable-2 { color: #b58900; }
.cm-s-solarized .cm-variable-3, .cm-s-solarized .cm-type { color: #6c71c4; }

.cm-s-solarized .cm-property { color: #2aa198; }
.cm-s-solarized .cm-operator { color: #6c71c4; }

.cm-s-solarized .cm-comment { color: #586e75; font-style:italic; }

.cm-s-solarized .cm-string { color: #859900; }
.cm-s-solarized .cm-string-2 { color: #b58900; }

.cm-s-solarized .cm-meta { color: #859900; }
.cm-s-solarized .cm-qualifier { color: #b58900; }
.cm-s-solarized .cm-builtin { color: #d33682; }
.cm-s-solarized .cm-bracket { color: #cb4b16; }
.cm-s-solarized .CodeMirror-matchingbracket { color: #859900; }
.cm-s-solarized .CodeMirror-nonmatchingbracket { color: #dc322f; }
.cm-s-solarized .cm-tag { color: #93a1a1; }
.cm-s-solarized .cm-attribute { color: #2aa198; }
.cm-s-solarized .cm-hr {
  color: transparent;
  border-top: 1px solid #586e75;
  display: block;
}
.cm-s-solarized .cm-link { color: #93a1a1; cursor: pointer; }
.cm-s-solarized .cm-special { color: #6c71c4; }
.cm-s-solarized .cm-em {
  color: #999;
  text-decoration: underline;
  text-decoration-style: dotted;
}
.cm-s-solarized .cm-error,
.cm-s-solarized .cm-invalidchar {
  color: #586e75;
  border-bottom: 1px dotted #dc322f;
}

.cm-s-solarized.cm-s-dark div.CodeMirror-selected { background: #073642; }
.cm-s-solarized.cm-s-dark.CodeMirror ::selection { background: rgba(7, 54, 66, 0.99); }
.cm-s-solarized.cm-s-dark .CodeMirror-line::-moz-selection, .cm-s-dark .CodeMirror-line > span::-moz-selection, .cm-s-dark .CodeMirror-line > span > span::-moz-selection { background: rgba(7, 54, 66, 0.99); }

.cm-s-solarized.cm-s-light div.CodeMirror-selected { background: #eee8d5; }
.cm-s-solarized.cm-s-light .CodeMirror-line::selection, .cm-s-light .CodeMirror-line > span::selection, .cm-s-light .CodeMirror-line > span > span::selection { background: #eee8d5; }
.cm-s-solarized.cm-s-light .CodeMirror-line::-moz-selection, .cm-s-ligh .CodeMirror-line > span::-moz-selection, .cm-s-ligh .CodeMirror-line > span > span::-moz-selection { background: #eee8d5; }

/* Editor styling */



/* Little shadow on the view-port of the buffer view */
.cm-s-solarized.CodeMirror {
  -moz-box-shadow: inset 7px 0 12px -6px #000;
  -webkit-box-shadow: inset 7px 0 12px -6px #000;
  box-shadow: inset 7px 0 12px -6px #000;
}

/* Remove gutter border */
.cm-s-solarized .CodeMirror-gutters {
  border-right: 0;
}

/* Gutter colors and line number styling based of color scheme (dark / light) */

/* Dark */
.cm-s-solarized.cm-s-dark .CodeMirror-gutters {
  background-color: #073642;
}

.cm-s-solarized.cm-s-dark .CodeMirror-linenumber {
  color: #586e75;
  text-shadow: #021014 0 -1px;
}

/* Light */
.cm-s-solarized.cm-s-light .CodeMirror-gutters {
  background-color: #eee8d5;
}

.cm-s-solarized.cm-s-light .CodeMirror-linenumber {
  color: #839496;
}

/* Common */
.cm-s-solarized .CodeMirror-linenumber {
  padding: 0 5px;
}
.cm-s-solarized .CodeMirror-guttermarker-subtle { color: #586e75; }
.cm-s-solarized.cm-s-dark .CodeMirror-guttermarker { color: #ddd; }
.cm-s-solarized.cm-s-light .CodeMirror-guttermarker { color: #cb4b16; }

.cm-s-solarized .CodeMirror-gutter .CodeMirror-gutter-text {
  color: #586e75;
}

/* Cursor */
.cm-s-solarized .CodeMirror-cursor { border-left: 1px solid #819090; }

/* Fat cursor */
.cm-s-solarized.cm-s-light.cm-fat-cursor .CodeMirror-cursor { background: #77ee77; }
.cm-s-solarized.cm-s-light .cm-animate-fat-cursor { background-color: #77ee77; }
.cm-s-solarized.cm-s-dark.cm-fat-cursor .CodeMirror-cursor { background: #586e75; }
.cm-s-solarized.cm-s-dark .cm-animate-fat-cursor { background-color: #586e75; }

/* Active line */
.cm-s-solarized.cm-s-dark .CodeMirror-activeline-background {
  background: rgba(255, 255, 255, 0.06);
}
.cm-s-solarized.cm-s-light .CodeMirror-activeline-background {
  background: rgba(0, 0, 0, 0.06);
}

.cm-s-the-matrix.CodeMirror { background: #000000; color: #00FF00; }
.cm-s-the-matrix div.CodeMirror-selected { background: #2D2D2D; }
.cm-s-the-matrix .CodeMirror-line::selection, .cm-s-the-matrix .CodeMirror-line > span::selection, .cm-s-the-matrix .CodeMirror-line > span > span::selection { background: rgba(45, 45, 45, 0.99); }
.cm-s-the-matrix .CodeMirror-line::-moz-selection, .cm-s-the-matrix .CodeMirror-line > span::-moz-selection, .cm-s-the-matrix .CodeMirror-line > span > span::-moz-selection { background: rgba(45, 45, 45, 0.99); }
.cm-s-the-matrix .CodeMirror-gutters { background: #060; border-right: 2px solid #00FF00; }
.cm-s-the-matrix .CodeMirror-guttermarker { color: #0f0; }
.cm-s-the-matrix .CodeMirror-guttermarker-subtle { color: white; }
.cm-s-the-matrix .CodeMirror-linenumber { color: #FFFFFF; }
.cm-s-the-matrix .CodeMirror-cursor { border-left: 1px solid #00FF00; }

.cm-s-the-matrix span.cm-keyword { color: #008803; font-weight: bold; }
.cm-s-the-matrix span.cm-atom { color: #3FF; }
.cm-s-the-matrix span.cm-number { color: #FFB94F; }
.cm-s-the-matrix span.cm-def { color: #99C; }
.cm-s-the-matrix span.cm-variable { color: #F6C; }
.cm-s-the-matrix span.cm-variable-2 { color: #C6F; }
.cm-s-the-matrix span.cm-variable-3, .cm-s-the-matrix span.cm-type { color: #96F; }
.cm-s-the-matrix span.cm-property { color: #62FFA0; }
.cm-s-the-matrix span.cm-operator { color: #999; }
.cm-s-the-matrix span.cm-comment { color: #CCCCCC; }
.cm-s-the-matrix span.cm-string { color: #39C; }
.cm-s-the-matrix span.cm-meta { color: #C9F; }
.cm-s-the-matrix span.cm-qualifier { color: #FFF700; }
.cm-s-the-matrix span.cm-builtin { color: #30a; }
.cm-s-the-matrix span.cm-bracket { color: #cc7; }
.cm-s-the-matrix span.cm-tag { color: #FFBD40; }
.cm-s-the-matrix span.cm-attribute { color: #FFF700; }
.cm-s-the-matrix span.cm-error { color: #FF0000; }

.cm-s-the-matrix .CodeMirror-activeline-background { background: #040; }

/*
Copyright (C) 2011 by MarkLogic Corporation
Author: Mike Brevoort <mike@brevoort.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
*/
.cm-s-xq-light span.cm-keyword { line-height: 1em; font-weight: bold; color: #5A5CAD; }
.cm-s-xq-light span.cm-atom { color: #6C8CD5; }
.cm-s-xq-light span.cm-number { color: #164; }
.cm-s-xq-light span.cm-def { text-decoration:underline; }
.cm-s-xq-light span.cm-variable { color: black; }
.cm-s-xq-light span.cm-variable-2 { color:black; }
.cm-s-xq-light span.cm-variable-3, .cm-s-xq-light span.cm-type { color: black; }
.cm-s-xq-light span.cm-property {}
.cm-s-xq-light span.cm-operator {}
.cm-s-xq-light span.cm-comment { color: #0080FF; font-style: italic; }
.cm-s-xq-light span.cm-string { color: red; }
.cm-s-xq-light span.cm-meta { color: yellow; }
.cm-s-xq-light span.cm-qualifier { color: grey; }
.cm-s-xq-light span.cm-builtin { color: #7EA656; }
.cm-s-xq-light span.cm-bracket { color: #cc7; }
.cm-s-xq-light span.cm-tag { color: #3F7F7F; }
.cm-s-xq-light span.cm-attribute { color: #7F007F; }
.cm-s-xq-light span.cm-error { color: #f00; }

.cm-s-xq-light .CodeMirror-activeline-background { background: #e8f2ff; }
.cm-s-xq-light .CodeMirror-matchingbracket { outline:1px solid grey;color:black !important;background:yellow; }

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor-static {
  margin: var(--jp-code-padding);
}

.jp-CodeMirrorEditor,
.jp-CodeMirrorEditor-static {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0px;
  padding: 0px;
  line-height: normal;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}
.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}
.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}
.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0em;
}

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}
.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}
.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}
.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}
.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}
.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}
.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}
.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}
.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: 0.8em;
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 4px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: space-evenly;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 1;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 100%;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item.jp-mod-selected {
  color: white;
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: limegreen;
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

.jp-FileDialog.jp-mod-conflict input {
  color: red;
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0px;
  padding: 0px;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

.jp-OutputArea-executeResult.jp-RenderedText {
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;
  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0px;
  bottom: 0px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: flex;
  flex-direction: row;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0px;
  background: var(--jp-cell-editor-background);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: 2px;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: flex;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0px;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label {
  line-height: 1.4;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

</style>

    <style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;

  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-700);
  --jp-brand-color1: var(--md-blue-500);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-700);
  --jp-accent-color1: var(--md-green-500);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-700);
  --jp-warn-color1: var(--md-orange-500);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-700);
  --jp-error-color1: var(--md-red-500);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-700);
  --jp-success-color1: var(--md-green-500);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-700);
  --jp-info-color1: var(--md-cyan-500);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;

  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;

  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);

  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: 'Source Code Pro', monospace;
  --jp-cell-prompt-letter-spacing: 0px;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);
  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;
  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: #05a;
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #aa22ff;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #aa22ff;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 180px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);
}
</style>

<style type="text/css">
a.anchor-link {
   display: none;
}
.highlight  {
    margin: 0.4em;
}

/* Input area styling */
.jp-InputArea {
    overflow: hidden;
}

.jp-InputArea-editor {
    overflow: hidden;
}

@media print {
  body {
    margin: 0;
  }
}
</style>



<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-MML-AM_CHTML-full,Safe"> </script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: { 
                    automatic: true 
                    }
                },
                "HTML-CSS": {
                    linebreaks: { 
                    automatic: true 
                    }
                }
            });
        
            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">

<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h1 id="&#12304;-DataAnalysis-Basic-&#12305;">&#12304; DataAnalysis Basic &#12305;<a class="anchor-link" href="#&#12304;-DataAnalysis-Basic-&#12305;">&#182;</a></h1>
</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Pandas-(DataFrame-Library)">Pandas (DataFrame Library)<a class="anchor-link" href="#Pandas-(DataFrame-Library)">&#182;</a></h2>
</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Pandas Libarary 실행</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[1]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Data Load (데이터불러오기)</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 데이터 파일 또는 URL-File에서 불러오기</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s2">&quot;https://raw.githubusercontent.com/kimds929/kimds929.github.io/master/_data/test_df.csv&quot;</span><span class="p">)</span>
<span class="n">df</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[2]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>10</td>
      <td>2</td>
      <td>a</td>
      <td>10</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>13</td>
      <td>4</td>
      <td>a</td>
      <td>8</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>2</td>
      <td>b</td>
      <td>12</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[3]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 데이터 클립보드에서 불러오기</span>
<span class="n">df = pd.read_clipboard()</span>
<span class="n">df</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[3]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>10</td>
      <td>2</td>
      <td>a</td>
      <td>10</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>13</td>
      <td>4</td>
      <td>a</td>
      <td>8</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>2</td>
      <td>b</td>
      <td>12</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 직접입력 Data로부터 만들기</span>
<span class="n">test_dict</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;y&#39;</span><span class="p">:</span> <span class="p">[</span><span class="mi">10</span><span class="p">,</span> <span class="mi">13</span><span class="p">,</span> <span class="mi">20</span><span class="p">,</span> <span class="mi">7</span><span class="p">,</span> <span class="mi">15</span><span class="p">],</span>
            <span class="s1">&#39;x1&#39;</span><span class="p">:</span> <span class="p">[</span><span class="mi">2</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">4</span><span class="p">],</span>
            <span class="s1">&#39;x2&#39;</span><span class="p">:</span> <span class="p">[</span><span class="s1">&#39;a&#39;</span><span class="p">,</span> <span class="s1">&#39;a&#39;</span><span class="p">,</span> <span class="s1">&#39;b&#39;</span><span class="p">,</span> <span class="s1">&#39;b&#39;</span><span class="p">,</span> <span class="s1">&#39;b&#39;</span><span class="p">],</span>
            <span class="s1">&#39;x3&#39;</span><span class="p">:</span> <span class="p">[</span><span class="mi">10</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">12</span><span class="p">,</span> <span class="mi">7</span><span class="p">],</span>
            <span class="s1">&#39;x4&#39;</span><span class="p">:</span> <span class="p">[</span><span class="s1">&#39;g1&#39;</span><span class="p">,</span> <span class="s1">&#39;g2&#39;</span><span class="p">,</span> <span class="s1">&#39;g1&#39;</span><span class="p">,</span> <span class="s1">&#39;g2&#39;</span><span class="p">,</span> <span class="s1">&#39;g3&#39;</span><span class="p">]}</span>

<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">test_dict</span><span class="p">)</span>
<span class="n">df</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[4]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>10</td>
      <td>2</td>
      <td>a</td>
      <td>10</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>13</td>
      <td>4</td>
      <td>a</td>
      <td>8</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>2</td>
      <td>b</td>
      <td>12</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[5]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 데이터 클립보드로 내보내기</span>
<span class="n">df</span><span class="o">.</span><span class="n">to_clipboard</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Display &amp; Indexing (데이터 확인 &amp; 인덱싱)</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[6]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span>      <span class="c1"># 데이터보기</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[6]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>10</td>
      <td>2</td>
      <td>a</td>
      <td>10</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>13</td>
      <td>4</td>
      <td>a</td>
      <td>8</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>2</td>
      <td>b</td>
      <td>12</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[7]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">sample</span><span class="p">(</span><span class="mi">3</span><span class="p">)</span>      <span class="c1"># 데이터보기 (3개만보기)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[7]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>2</td>
      <td>b</td>
      <td>12</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[8]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 1개 Colum 선택하기 (select, indexing)</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span>                <span class="c1"># 1개만 선택 (Series)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[8]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>0    2
1    4
2    5
3    2
4    4
Name: x1, dtype: int64</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[9]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 2개이상 Colum 선택하기 (select, indexing)</span>
<span class="n">df</span><span class="p">[[</span><span class="s1">&#39;x1&#39;</span><span class="p">,</span> <span class="s1">&#39;x2&#39;</span><span class="p">]]</span>        <span class="c1"># 2개이상 선택 (DataFrame)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[9]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>x1</th>
      <th>x2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>a</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>a</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5</td>
      <td>b</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>b</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>b</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[10]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 1개이상 Colum을 DataFrame형태로 선택하기 (select, indexing)</span>
<span class="n">df</span><span class="p">[[</span><span class="s1">&#39;x1&#39;</span><span class="p">]]</span>        <span class="c1"># 1개를 DataFrame 형태로 선택 (DataFrame)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[10]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>x1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><strong>※ (참고) 기능어 역할</strong> <br>
&nbsp; * □.□ : 앞의 대상에 어떤 함수를 사용하거나, 변수를 불러올때 사용 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   pd.read_csv(...) → pandas Library에서  read_csv 함수를 사용 <br>
    <br>
&nbsp; * □() : 함수( input → 함수 → output) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   pd.read_csv(...) → pandas Library에서  read_csv함수를 사용하는데 ...이라는 경로에서 불러올 예정 <br>
    <br>
&nbsp; * □[] : 대상에 접근, Item추출 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   df['x1'] → df라는 데이터프레임에서 'x1' column에 접근하여 데이터를 추출 <br>
<br>
<br>
<br>
<br></p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Filtering (필터링)</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[11]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;equal&#39; filtering</span>
<span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x2&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;a&#39;</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[11]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>10</td>
      <td>2</td>
      <td>a</td>
      <td>10</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>13</td>
      <td>4</td>
      <td>a</td>
      <td>8</td>
      <td>g2</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[12]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;not equal&#39; filtering</span>
<span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x2&#39;</span><span class="p">]</span> <span class="o">!=</span> <span class="s1">&#39;a&#39;</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[12]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>2</td>
      <td>b</td>
      <td>12</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[13]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;inequality&#39; filtering</span>
<span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;y&#39;</span><span class="p">]</span> <span class="o">&gt;</span> <span class="mi">10</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[13]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>13</td>
      <td>4</td>
      <td>a</td>
      <td>8</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[14]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># filtering → select &#39;x2&#39;</span>
<span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x2&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;a&#39;</span><span class="p">][</span><span class="s1">&#39;x2&#39;</span><span class="p">]</span>       <span class="c1"># 필터링 후 특정 column선택</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[14]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>0    a
1    a
Name: x2, dtype: object</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Operation (연산)</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[15]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;x1&#39; column select</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[15]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>0    2
1    4
2    5
3    2
4    4
Name: x1, dtype: int64</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[16]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 갯수</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[16]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>5</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[17]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 합계</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[17]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>17</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[18]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 평균</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[18]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>3.4</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[19]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 편차</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">std</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[19]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>1.3416407864998738</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[20]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 합계함수로 평균값 구하기</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">agg</span><span class="p">(</span><span class="s1">&#39;mean&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[20]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>3.4</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[21]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 합계함수로 여러개의 통계값(갯수, 평균, 편차) 한꺼번에 구하기</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">agg</span><span class="p">([</span><span class="s1">&#39;count&#39;</span><span class="p">,</span> <span class="s1">&#39;mean&#39;</span><span class="p">,</span> <span class="s1">&#39;std&#39;</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[21]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>count    5.000000
mean     3.400000
std      1.341641
Name: x1, dtype: float64</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ groupby (Pivot)</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[22]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;x2&#39;로 grouping 후 전체 Column에 대한 합계</span>
<span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="s1">&#39;x2&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[22]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x3</th>
    </tr>
    <tr>
      <th>x2</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>23</td>
      <td>6</td>
      <td>18</td>
    </tr>
    <tr>
      <th>b</th>
      <td>42</td>
      <td>11</td>
      <td>24</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[23]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;x2&#39;로 grouping 후 &#39;x1&#39;column에 대한 합계</span>
<span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="s1">&#39;x2&#39;</span><span class="p">)[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[23]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>x2
a     6
b    11
Name: x1, dtype: int64</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[24]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;x2, x4&#39; 로 grouping 후 &#39;x1&#39;column에 대한 합계</span>
<span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;x2&#39;</span><span class="p">,</span><span class="s1">&#39;x4&#39;</span><span class="p">])[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[24]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>x2  x4
a   g1    2
    g2    4
b   g1    5
    g2    2
    g3    4
Name: x1, dtype: int64</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[25]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;x2, x4&#39; 로 grouping 후 &#39;x1&#39;column에 대한 통계값(갯수, 평균, 편차)</span>
<span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;x2&#39;</span><span class="p">,</span><span class="s1">&#39;x4&#39;</span><span class="p">])[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">agg</span><span class="p">([</span><span class="s1">&#39;count&#39;</span><span class="p">,</span><span class="s1">&#39;mean&#39;</span><span class="p">,</span><span class="s1">&#39;std&#39;</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[25]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
    </tr>
    <tr>
      <th>x2</th>
      <th>x4</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="2" valign="top">a</th>
      <th>g1</th>
      <td>1</td>
      <td>2</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>g2</th>
      <td>1</td>
      <td>4</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">b</th>
      <th>g1</th>
      <td>1</td>
      <td>5</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>g2</th>
      <td>1</td>
      <td>2</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>g3</th>
      <td>1</td>
      <td>4</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><br>
<br>
<br>
<br>
<br></p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Matplotlib.pyplot-&amp;-Seaborn-(Graph-Library)">Matplotlib.pyplot &amp; Seaborn (Graph Library)<a class="anchor-link" href="#Matplotlib.pyplot-&amp;-Seaborn-(Graph-Library)">&#182;</a></h2>
</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ matplotlib, seaborn Libarary 실행</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[26]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[27]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># data 확인</span>
<span class="n">df</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[27]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>10</td>
      <td>2</td>
      <td>a</td>
      <td>10</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>13</td>
      <td>4</td>
      <td>a</td>
      <td>8</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>2</td>
      <td>b</td>
      <td>12</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Draw Graph</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[28]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># histogram</span>
<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">])</span>      <span class="c1"># histogram</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[28]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>(array([2., 0., 0., 0., 0., 0., 2., 0., 0., 1.]),
 array([2. , 2.3, 2.6, 2.9, 3.2, 3.5, 3.8, 4.1, 4.4, 4.7, 5. ]),
 &lt;BarContainer object of 10 artists&gt;)</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[29]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># scatter-plot</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">y</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;y&#39;</span><span class="p">])</span>      <span class="c1"># scatter plot</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[29]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;matplotlib.collections.PathCollection at 0xa7f01c0&gt;</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXAAAAD4CAYAAAD1jb0+AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjMuMSwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/d3fzzAAAACXBIWXMAAAsTAAALEwEAmpwYAAAPvUlEQVR4nO3dfWxk1XnH8e9Tr6sMJKkTrXlZQ7pRRaw2kLKpS2loGwJJvW1RWKEmAol21aKuiqI2oNRpNpFA+YsojtKkrdRoVVYQldLQYhwUhRpEX0ikQOTFEEOJ20gldG2UNd0YEmWaLsvTPzxLvYO98+KxPWf2+5Esz5x7Zu5z9mh/vj733nFkJpKk8vzEVhcgSWqPAS5JhTLAJalQBrgkFcoAl6RCbdvMnW3fvj137ty5mbuUpOIdOnTohcwcrG/f1ADfuXMn09PTm7lLSSpeRHx3tXaXUCSpUAa4JBXKAJekQhngklQoA1ySCtXwKpSIOB/4InAO8ApwIDM/HxFvBr4E7ASeBT6Ymd/fuFIlqTyTM/OMT82xsFRlx0CFsdFh9uwa6sh7N3ME/jLwkcz8WeBS4EMR8XPAx4CHM/MC4OHac0lSzeTMPPsnZplfqpLA/FKV/ROzTM7Md+T9GwZ4Zj6fmY/XHv8AeAYYAq4G7qx1uxPY05GKJKlHjE/NUT12/KS26rHjjE/NdeT9W1oDj4idwC7gMeDszHwelkMeOGuN1+yLiOmImF5cXFxnuZJUjoWlakvtrWo6wCPi9cC9wE2Z+VKzr8vMA5k5kpkjg4OvuRNUknrWjoFKS+2tairAI6Kf5fC+KzMnas3fi4hza9vPBY50pCJJ6hFjo8NU+vtOaqv09zE2OtyR928Y4BERwO3AM5n52RWb7gf21h7vBb7ckYokqUfs2TXEbddcxNBAhQCGBircds1FHbsKJRr9TcyI+BXga8Asy5cRAnyc5XXwe4C3AM8BH8jMo6d6r5GRkfTDrCSpNRFxKDNH6tsbXgeemV8HYo3NV663MElSe7wTU5IKZYBLUqEMcEkqlAEuSYUywCWpUAa4JBXKAJekQhngklQoA1ySCmWAS1KhDHBJKpQBLkmFMsAlqVAGuCQVygCXpEIZ4JJUKANckgplgEtSoQxwSSqUAS5JhTLAJalQDQM8Ig5GxJGIeGpF28UR8WhEPBER0xFxycaWKUmq18wR+B3A7rq2TwOfzMyLgVtqzyVJm6hhgGfmI8DR+mbgjbXHPwUsdLguSVID29p83U3AVER8huUfAu/qWEWSpKa0exLzRuDmzDwfuBm4fa2OEbGvtk4+vbi42ObuJEn12g3wvcBE7fHfA2uexMzMA5k5kpkjg4ODbe5OklSv3QBfAN5de3wF8B+dKUeS1KyGa+ARcTdwObA9Ig4DtwJ/AHw+IrYB/wPs28giJUmv1TDAM/O6NTb9QodrkSS1wDsxJalQBrgkFcoAl6RCGeCSVCgDXJIKZYBLUqEMcEkqlAEuSYUywCWpUAa4JBXKAJekQhngklQoA1ySCmWAS1KhDHBJKpQBLkmFMsAlqVAGuCQVygCXpEIZ4JJUKANckgplgEtSoRoGeEQcjIgjEfFUXfsfRcRcRDwdEZ/euBIlSatp5gj8DmD3yoaIeA9wNfCOzHw78JnOlyZJOpWGAZ6ZjwBH65pvBD6VmT+u9TmyAbVJkk6h3TXwtwG/GhGPRcS/RsQvrtUxIvZFxHRETC8uLra5O0lSvXYDfBvwJuBSYAy4JyJitY6ZeSAzRzJzZHBwsM3dSZLqtRvgh4GJXPZN4BVge+fKkiQ10m6ATwJXAETE24CfBF7oUE2SpCZsa9QhIu4GLge2R8Rh4FbgIHCwdmnh/wJ7MzM3slBJ0skaBnhmXrfGpus7XIskqQXeiSlJhTLAJalQBrgkFcoAl6RCGeCSVCgDXJIK1fAyQkllmJyZZ3xqjoWlKjsGKoyNDrNn19BWl6UNZIBLPWByZp79E7NUjx0HYH6pyv6JWQBDvIe5hCL1gPGpuVfD+4TqseOMT81tUUXaDAa41AMWlqottas3GOBSD9gxUGmpXb3BAJd6wNjoMJX+vpPaKv19jI0Ob1FF2gyexJR6wIkTlV6FcnoxwKUesWfXkIF9mnEJRZIKZYBLUqEMcEkqlAEuSYUywCWpUAa4JBXKAJekQjUM8Ig4GBFHIuKpVbb9SURkRGzfmPIkSWtp5gj8DmB3fWNEnA+8D3iuwzVJkprQMMAz8xHg6Cqb/gz4KJCdLkqS1Fhba+AR8X5gPjOfbKLvvoiYjojpxcXFdnYnSVpFywEeEWcAnwBuaaZ/Zh7IzJHMHBkcHGx1d5KkNbRzBP4zwFuBJyPiWeA84PGIOKeThUmSTq3lTyPMzFngrBPPayE+kpkvdLAuSVIDzVxGeDfwDWA4Ig5HxA0bX5YkqZGGR+CZeV2D7Ts7Vo0kqWneiSlJhTLAJalQBrgkFcoAl6RCGeCSVCgDXJIKZYBLUqFavhNTUneanJlnfGqOhaUqOwYqjI0Os2fX0FaXpQ1kgEs9YHJmnv0Ts1SPHQdgfqnK/olZAEO8h7mEIvWA8am5V8P7hOqx44xPzW1RRdoMBrjUAxaWqi21qzcY4FIP2DFQaaldvcEAl3rA2Ogwlf6+k9oq/X2MjQ5vUUXaDJ7ElHrAiROVXoVyejHApR6xZ9eQgX2acQlFkgplgEtSoQxwSSqUAS5JhTLAJalQBrgkFcoAl6RCNQzwiDgYEUci4qkVbeMR8e2I+FZE3BcRAxtapSTpNZo5Ar8D2F3X9hBwYWa+A/h3YH+H65IkNdAwwDPzEeBoXduDmfly7emjwHkbUJsk6RQ6sQb++8ADa22MiH0RMR0R04uLix3YnSQJ1hngEfEJ4GXgrrX6ZOaBzBzJzJHBwcH17E6StELbH2YVEXuBq4ArMzM7V5IkqRltBXhE7Ab+FHh3Zv6osyVJkprRzGWEdwPfAIYj4nBE3AD8JfAG4KGIeCIivrDBdUqS6jQ8As/M61Zpvn0DapEktcA7MSWpUAa4JBXKAJekQhngklQoA1ySCmWAS1KhDHBJKpQBLkmFMsAlqVAGuCQVygCXpEIZ4JJUKANckgplgEtSoQxwSSqUAS5JhTLAJalQBrgkFcoAl6RCGeCSVCgDXJIK1fCv0kfEQeAq4EhmXlhrezPwJWAn8Czwwcz8/kYUODkzz/jUHAtLVXYMVBgbHWbPrqGN2JUkFaWZI/A7gN11bR8DHs7MC4CHa887bnJmnv0Ts8wvVUlgfqnK/olZJmfmN2J3klSUhgGemY8AR+uarwburD2+E9jT2bKWjU/NUT12/KS26rHjjE/NbcTuJKko7a6Bn52ZzwPUvp+1VseI2BcR0xExvbi42NJOFpaqLbVL0ulkw09iZuaBzBzJzJHBwcGWXrtjoNJSuySdTtoN8O9FxLkAte9HOlfS/xsbHabS33dSW6W/j7HR4Y3YnSQVpd0Avx/YW3u8F/hyZ8o52Z5dQ9x2zUUMDVQIYGigwm3XXORVKJJEc5cR3g1cDmyPiMPArcCngHsi4gbgOeADG1Xgnl1DBrYkraJhgGfmdWtsurLDtUiSWuCdmJJUKANckgplgEtSoQxwSSqUAS5JhTLAJalQBrgkFcoAl6RCGeCSVCgDXJIKZYBLUqEMcEkqlAEuSYUywCWpUAa4JBXKAJekQhngklQoA1ySCmWAS1KhDHBJKpQBLkmFMsAlqVDrCvCIuDkino6IpyLi7oh4XacKkySdWtsBHhFDwB8DI5l5IdAHXNupwiRJp7beJZRtQCUitgFnAAvrL0mS1Iy2Azwz54HPAM8BzwMvZuaD9f0iYl9ETEfE9OLiYvuVSpJOsp4llDcBVwNvBXYAZ0bE9fX9MvNAZo5k5sjg4GD7lUqSTrKeJZT3Av+ZmYuZeQyYAN7VmbIkSY2sJ8CfAy6NiDMiIoArgWc6U5YkqZH1rIE/BvwD8DgwW3uvAx2qS5LUwLb1vDgzbwVu7VAtkqQWeCemJBXKAJekQhngklQoA1ySCmWAS1KhDHBJKtS6LiPcDJMz84xPzbGwVGXHQIWx0WH27Bra6rIkact1dYBPzsyzf2KW6rHjAMwvVdk/MQtgiEs67XX1Esr41Nyr4X1C9dhxxqfmtqgiSeoeXR3gC0vVltol6XTS1QG+Y6DSUrsknU66OsDHRoep9Ped1Fbp72NsdHiLKpKk7tHVJzFPnKj0KhRJeq2uDnBYDnEDW5Jeq6uXUCRJazPAJalQBrgkFcoAl6RCGeCSVKjIzM3bWcQi8N02X74deKGD5Wwlx9J9emUc4Fi61XrG8tOZOVjfuKkBvh4RMZ2ZI1tdRyc4lu7TK+MAx9KtNmIsLqFIUqEMcEkqVEkBfmCrC+ggx9J9emUc4Fi6VcfHUswauCTpZCUdgUuSVjDAJalQXRXgEXF+RPxzRDwTEU9HxIdX6RMR8ecR8Z2I+FZEvHMram2kybFcHhEvRsQTta9btqLWU4mI10XENyPiydo4PrlKn1LmpJmxdP2crBQRfRExExFfWWVbEfMCDcdRzJxExLMRMVurc3qV7R2dk277ONmXgY9k5uMR8QbgUEQ8lJn/tqLPbwAX1L5+Cfir2vdu08xYAL6WmVdtQX3N+jFwRWb+MCL6ga9HxAOZ+eiKPqXMSTNjge6fk5U+DDwDvHGVbaXMC5x6HFDWnLwnM9e6Yaejc9JVR+CZ+XxmPl57/AOWJ7T+w8CvBr6Yyx4FBiLi3E0utaEmx9L1av/OP6w97a991Z/5LmVOmhlLMSLiPOC3gL9eo0sR89LEOHpJR+ekqwJ8pYjYCewCHqvbNAT814rnh+nyYDzFWAB+ufYr/QMR8fbNraw5tV9vnwCOAA9lZrFz0sRYoIA5qfkc8FHglTW2lzIvn+PU44By5iSBByPiUETsW2V7R+ekKwM8Il4P3AvclJkv1W9e5SVdexTVYCyPs/wZBz8P/AUwucnlNSUzj2fmxcB5wCURcWFdl2LmpImxFDEnEXEVcCQzD52q2yptXTUvTY6jiDmpuSwz38nyUsmHIuLX6rZ3dE66LsBra5P3Andl5sQqXQ4D5694fh6wsBm1tarRWDLzpRO/0mfmV4H+iNi+yWU2LTOXgH8BdtdtKmZOTlhrLAXNyWXA+yPiWeDvgCsi4m/q+pQwLw3HUdCckJkLte9HgPuAS+q6dHROuirAIyKA24FnMvOza3S7H/jd2tncS4EXM/P5TSuySc2MJSLOqfUjIi5heT7+e/OqbCwiBiNioPa4ArwX+HZdt1LmpOFYSpgTgMzcn5nnZeZO4FrgnzLz+rpuXT8vzYyjlDmJiDNrFywQEWcCvw48Vdeto3PSbVehXAb8DjBbW6cE+DjwFoDM/ALwVeA3ge8APwJ+b/PLbEozY/lt4MaIeBmoAtdm990aey5wZ0T0sfwf557M/EpE/CEUNyfNjKWEOVlTofPyGoXOydnAfbWfNduAv83Mf9zIOfFWekkqVFctoUiSmmeAS1KhDHBJKpQBLkmFMsAlqVAGuCQVygCXpEL9H11jBgAOnU8VAAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[30]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># line-plot</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;y&#39;</span><span class="p">])</span>      <span class="c1"># Line Plot</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[30]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[&lt;matplotlib.lines.Line2D at 0xa82bf40&gt;]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[31]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># boxplot (seaborn)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">,</span> <span class="n">x</span><span class="o">=</span><span class="s1">&#39;x2&#39;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s1">&#39;x1&#39;</span><span class="p">)</span>    <span class="c1"># boxplot (seaborn)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[31]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;AxesSubplot:xlabel=&#39;x2&#39;, ylabel=&#39;x1&#39;&gt;</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[32]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># boxplot (pyplot)</span>
<span class="n">box1</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x2&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;a&#39;</span><span class="p">][</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span>
<span class="n">box2</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x2&#39;</span><span class="p">]</span> <span class="o">!=</span> <span class="s1">&#39;a&#39;</span><span class="p">][</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">boxplot</span><span class="p">([</span><span class="n">box1</span><span class="p">,</span> <span class="n">box2</span><span class="p">],</span> <span class="n">labels</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;Class_1&#39;</span><span class="p">,</span> <span class="s1">&#39;Class_2&#39;</span><span class="p">])</span>        <span class="c1"># boxplot (pyplot)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[32]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>{&#39;whiskers&#39;: [&lt;matplotlib.lines.Line2D at 0xa8c8160&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8c8310&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8c8d30&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8c8ee0&gt;],
 &#39;caps&#39;: [&lt;matplotlib.lines.Line2D at 0xa8c84c0&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8c8670&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8d60b8&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8d6268&gt;],
 &#39;boxes&#39;: [&lt;matplotlib.lines.Line2D at 0xa8b8f70&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8c8b80&gt;],
 &#39;medians&#39;: [&lt;matplotlib.lines.Line2D at 0xa8c8820&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8d6418&gt;],
 &#39;fliers&#39;: [&lt;matplotlib.lines.Line2D at 0xa8c89d0&gt;,
  &lt;matplotlib.lines.Line2D at 0xa8d65c8&gt;],
 &#39;means&#39;: []}</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Draw Option</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[33]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">bins</span><span class="o">=</span><span class="mi">30</span><span class="p">)</span>      <span class="c1"># 막대 갯수</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[33]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>(array([2., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
        0., 0., 0., 2., 0., 0., 0., 0., 0., 0., 0., 0., 1.]),
 array([2. , 2.1, 2.2, 2.3, 2.4, 2.5, 2.6, 2.7, 2.8, 2.9, 3. , 3.1, 3.2,
        3.3, 3.4, 3.5, 3.6, 3.7, 3.8, 3.9, 4. , 4.1, 4.2, 4.3, 4.4, 4.5,
        4.6, 4.7, 4.8, 4.9, 5. ]),
 &lt;BarContainer object of 30 artists&gt;)</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXoAAAD4CAYAAADiry33AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjMuMSwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/d3fzzAAAACXBIWXMAAAsTAAALEwEAmpwYAAAR70lEQVR4nO3df6jd913H8efLNEGt1eFy1438WPpH/rCTpSuXdKPi2uFKuh+Gwf5ImBsMR9hoYYoo0T861H+Ugci2biHMUIe2Regyg6a/wGmno5qb2rXNuo5LVuklhWSttqsblsy3f5xv9Hh67j3fJOcm93z6fMDhnu/nx/d8Pv3Q1/3eb77f70lVIUlq109c7gFIklaXQS9JjTPoJalxBr0kNc6gl6TGXXG5BzDOxo0ba9u2bZd7GJI0M44fP/79qpobV7cmg37btm0sLCxc7mFI0sxI8m/L1XnqRpIaZ9BLUuMMeklqnEEvSY0z6CWpcQa9JDVuYtAn2ZLk60meTnIiyafHtEmSzyVZTPJEkuuH6nYleaar2z/tCUiSVtbniP4s8FtV9QvAO4Hbklw70uZWYHv32gd8CSDJOuDOrv5aYO+YvpKkVTQx6Kvq+ap6rHv/A+BpYNNIs93AV2rgUeANSd4C7AQWq+pkVb0K3Nu1lSRdIud1Z2ySbcA7gH8eqdoEPDe0vdSVjSu/YZl972Pw1wBbt249n2H9P9v2/22vds/+0fsv+DOkFvj/yutH73+MTfIzwH3Ab1TVy6PVY7rUCuWvLaw6WFXzVTU/Nzf2cQ2SpAvQ64g+yXoGIf+XVfXVMU2WgC1D25uBU8CGZcolSZdIn6tuAvwZ8HRV/ckyzY4AH+uuvnkn8FJVPQ8cA7YnuSbJBmBP11aSdIn0OaK/Efgo8GSSx7uy3wO2AlTVAeAo8D5gEfgh8PGu7myS24EHgXXAoao6Mc0JSJJWNjHoq+ofGX+ufbhNAbctU3eUwS8CSdJl4J2xktQ4g16SGmfQS1LjDHpJapxBL0mNM+glqXEGvSQ1zqCXpMYZ9JLUOINekhpn0EtS4wx6SWqcQS9JjTPoJalxBr0kNc6gl6TGTfzikSSHgA8Ap6vqF8fU/zbwkaH9/QIwV1UvJnkW+AHwY+BsVc1Pa+CSpH76HNHfBexarrKqPltV11XVdcDvAv9QVS8ONbm5qzfkJekymBj0VfUI8OKkdp29wD0XNSJJ0lRN7Rx9kp9mcOR/31BxAQ8lOZ5k37Q+S5LU38Rz9Ofhg8A/jZy2ubGqTiV5E/Bwku90fyG8RveLYB/A1q1bpzgsSXp9m+ZVN3sYOW1TVae6n6eBw8DO5TpX1cGqmq+q+bm5uSkOS5Je36YS9El+Dng38NdDZVcmuerce+AW4KlpfJ4kqb8+l1feA9wEbEyyBHwGWA9QVQe6Zh8CHqqq/xzqejVwOMm5z7m7qh6Y3tAlSX1MDPqq2tujzV0MLsMcLjsJ7LjQgUmSpsM7YyWpcQa9JDXOoJekxhn0ktQ4g16SGmfQS1LjDHpJapxBL0mNM+glqXEGvSQ1zqCXpMYZ9JLUOINekhpn0EtS4wx6SWqcQS9JjTPoJalxE4M+yaEkp5OM/b7XJDcleSnJ493rjqG6XUmeSbKYZP80By5J6qfPEf1dwK4Jbb5RVdd1rz8ASLIOuBO4FbgW2Jvk2osZrCTp/E0M+qp6BHjxAva9E1isqpNV9SpwL7D7AvYjSboI0zpH/64k30pyf5K3dWWbgOeG2ix1ZWMl2ZdkIcnCmTNnpjQsSdI0gv4x4K1VtQP4PPC1rjxj2tZyO6mqg1U1X1Xzc3NzUxiWJAmmEPRV9XJVvdK9PwqsT7KRwRH8lqGmm4FTF/t5kqTzc9FBn+TNSdK939nt8wXgGLA9yTVJNgB7gCMX+3mSpPNzxaQGSe4BbgI2JlkCPgOsB6iqA8CHgU8lOQv8CNhTVQWcTXI78CCwDjhUVSdWZRaSpGVNDPqq2juh/gvAF5apOwocvbChSZKmwTtjJalxBr0kNc6gl6TGGfSS1DiDXpIaZ9BLUuMMeklqnEEvSY0z6CWpcQa9JDXOoJekxhn0ktQ4g16SGmfQS1LjDHpJapxBL0mNM+glqXETgz7JoSSnkzy1TP1HkjzRvb6ZZMdQ3bNJnkzyeJKFaQ5cktRPnyP6u4BdK9R/D3h3Vb0d+EPg4Ej9zVV1XVXNX9gQJUkXo893xj6SZNsK9d8c2nwU2DyFcUmSpmTa5+h/Hbh/aLuAh5IcT7JvpY5J9iVZSLJw5syZKQ9Lkl6/Jh7R95XkZgZB/0tDxTdW1akkbwIeTvKdqnpkXP+qOkh32md+fr6mNS5Jer2byhF9krcDXwZ2V9UL58qr6lT38zRwGNg5jc+TJPV30UGfZCvwVeCjVfXdofIrk1x17j1wCzD2yh1J0uqZeOomyT3ATcDGJEvAZ4D1AFV1ALgDeCPwxSQAZ7srbK4GDndlVwB3V9UDqzAHSdIK+lx1s3dC/SeAT4wpPwnseG0PSdKl5J2xktQ4g16SGmfQS1LjDHpJapxBL0mNM+glqXEGvSQ1zqCXpMYZ9JLUOINekhpn0EtS4wx6SWqcQS9JjTPoJalxBr0kNc6gl6TGGfSS1LiJQZ/kUJLTScZ+32sGPpdkMckTSa4fqtuV5Jmubv80By5J6qfPEf1dwK4V6m8FtnevfcCXAJKsA+7s6q8F9ia59mIGK0k6fxODvqoeAV5coclu4Cs18CjwhiRvAXYCi1V1sqpeBe7t2kqSLqGJXw7ewybguaHtpa5sXPkNy+0kyT4GfxGwdevWKQxLktaGbfv/tle7Z//o/avy+dP4x9iMKasVyseqqoNVNV9V83Nzc1MYliQJpnNEvwRsGdreDJwCNixTLkm6hKZxRH8E+Fh39c07gZeq6nngGLA9yTVJNgB7uraSpEto4hF9knuAm4CNSZaAzwDrAarqAHAUeB+wCPwQ+HhXdzbJ7cCDwDrgUFWdWIU5SJJWMDHoq2rvhPoCblum7iiDXwSSpMvEO2MlqXEGvSQ1zqCXpMYZ9JLUOINekhpn0EtS4wx6SWqcQS9JjTPoJalxBr0kNc6gl6TGGfSS1DiDXpIaZ9BLUuMMeklqnEEvSY0z6CWpcb2CPsmuJM8kWUyyf0z9byd5vHs9leTHSX6+q3s2yZNd3cK0JyBJWlmf74xdB9wJvBdYAo4lOVJV3z7Xpqo+C3y2a/9B4Der6sWh3dxcVd+f6sglSb30OaLfCSxW1cmqehW4F9i9Qvu9wD3TGJwk6eL1CfpNwHND20td2Wsk+WlgF3DfUHEBDyU5nmTfch+SZF+ShSQLZ86c6TEsSVIffYI+Y8pqmbYfBP5p5LTNjVV1PXArcFuSXx7XsaoOVtV8Vc3Pzc31GJYkqY8+Qb8EbBna3gycWqbtHkZO21TVqe7naeAwg1NBkqRLpE/QHwO2J7kmyQYGYX5ktFGSnwPeDfz1UNmVSa469x64BXhqGgOXJPUz8aqbqjqb5HbgQWAdcKiqTiT5ZFd/oGv6IeChqvrPoe5XA4eTnPusu6vqgWlOQJK0solBD1BVR4GjI2UHRrbvAu4aKTsJ7LioEUqSLop3xkpS4wx6SWqcQS9JjTPoJalxBr0kNc6gl6TGGfSS1DiDXpIaZ9BLUuMMeklqnEEvSY0z6CWpcQa9JDXOoJekxhn0ktQ4g16SGmfQS1LjegV9kl1JnkmymGT/mPqbkryU5PHudUffvpKk1TXxqwSTrAPuBN4LLAHHkhypqm+PNP1GVX3gAvtKklZJnyP6ncBiVZ2sqleBe4HdPfd/MX0lSVPQJ+g3Ac8NbS91ZaPeleRbSe5P8rbz7EuSfUkWkiycOXOmx7AkSX30CfqMKauR7ceAt1bVDuDzwNfOo++gsOpgVc1X1fzc3FyPYUmS+ugT9EvAlqHtzcCp4QZV9XJVvdK9PwqsT7KxT19J0urqE/THgO1JrkmyAdgDHBlukOTNSdK939nt94U+fSVJq2viVTdVdTbJ7cCDwDrgUFWdSPLJrv4A8GHgU0nOAj8C9lRVAWP7rtJcJEljTAx6+N/TMUdHyg4Mvf8C8IW+fSVJl453xkpS4wx6SWqcQS9JjTPoJalxBr0kNc6gl6TGGfSS1DiDXpIaZ9BLUuMMeklqnEEvSY0z6CWpcQa9JDXOoJekxhn0ktQ4g16SGmfQS1LjegV9kl1JnkmymGT/mPqPJHmie30zyY6humeTPJnk8SQL0xy8JGmyiV8lmGQdcCfwXmAJOJbkSFV9e6jZ94B3V9W/J7kVOAjcMFR/c1V9f4rjliT11OeIfiewWFUnq+pV4F5g93CDqvpmVf17t/kosHm6w5QkXag+Qb8JeG5oe6krW86vA/cPbRfwUJLjSfYt1ynJviQLSRbOnDnTY1iSpD4mnroBMqasxjZMbmYQ9L80VHxjVZ1K8ibg4STfqapHXrPDqoMMTvkwPz8/dv+SpPPX54h+CdgytL0ZODXaKMnbgS8Du6vqhXPlVXWq+3kaOMzgVJAk6RLpE/THgO1JrkmyAdgDHBlukGQr8FXgo1X13aHyK5Ncde49cAvw1LQGL0mabOKpm6o6m+R24EFgHXCoqk4k+WRXfwC4A3gj8MUkAGerah64GjjclV0B3F1VD6zKTCRJY/U5R09VHQWOjpQdGHr/CeATY/qdBHaMlkuSLh3vjJWkxhn0ktQ4g16SGmfQS1LjDHpJapxBL0mNM+glqXEGvSQ1zqCXpMYZ9JLUOINekhpn0EtS4wx6SWqcQS9JjTPoJalxBr0kNc6gl6TG9Qr6JLuSPJNkMcn+MfVJ8rmu/okk1/ftK0laXRODPsk64E7gVuBaYG+Sa0ea3Qps7177gC+dR19J0irqc0S/E1isqpNV9SpwL7B7pM1u4Cs18CjwhiRv6dlXkrSK+nw5+CbguaHtJeCGHm029ewLQJJ9DP4aAHglyTM9xjbORuD7kxrljy9w75dWr7nMgFbmAa/DuczA/yvNrEn++KLm8tblKvoEfcaUVc82ffoOCqsOAgd7jGdFSRaqav5i97MWtDKXVuYBzmUtamUesHpz6RP0S8CWoe3NwKmebTb06CtJWkV9ztEfA7YnuSbJBmAPcGSkzRHgY93VN+8EXqqq53v2lSStoolH9FV1NsntwIPAOuBQVZ1I8smu/gBwFHgfsAj8EPj4Sn1XZSb/56JP/6whrcyllXmAc1mLWpkHrNJcUjX2lLkkqRHeGStJjTPoJalxMxn0SbYk+XqSp5OcSPLpMW2WfSzDWtFzHjcleSnJ493rjssx1kmS/GSSf0nyrW4uvz+mzZpfE+g9l5lYFxjcoZ7kX5P8zZi6mViTcybMZZbW5NkkT3bjXBhTP9V16XN55Vp0FvitqnosyVXA8SQPV9W3h9oMP5bhBgaPZRh7s9Zl1GceAN+oqg9chvGdj/8C3lNVryRZD/xjkvu7O6XPmYU1gX5zgdlYF4BPA08DPzumblbW5JyV5gKzsyYAN1fVcjdHTXVdZvKIvqqer6rHuvc/YLDwm0aaLfdYhjWj5zxmQvff+ZVuc333Gv2X/jW/JtB7LjMhyWbg/cCXl2kyE2sCvebSkqmuy0wG/bAk24B3AP88UrXcYxnWpBXmAfCu7jTC/UnedmlH1l/3Z/XjwGng4aqa2TXpMReYjXX5U+B3gP9epn5m1oTJc4HZWBMYHDg8lOR4Bo9/GTXVdZnpoE/yM8B9wG9U1cuj1WO6rMmjsgnzeAx4a1XtAD4PfO0SD6+3qvpxVV3H4A7onUl+caTJzKxJj7ms+XVJ8gHgdFUdX6nZmLI1tyY957Lm12TIjVV1PYNTNLcl+eWR+qmuy8wGfXfu9D7gL6vqq2Oa9Hl0w2U3aR5V9fK50whVdRRYn2TjJR7meamq/wD+Htg1UjUTazJsubnMyLrcCPxqkmcZPDn2PUn+YqTNrKzJxLnMyJoAUFWnup+ngcMMnvQ7bKrrMpNBnyTAnwFPV9WfLNNsuccyrBl95pHkzV07kuxksGYvXLpR9pNkLskbuvc/BfwK8J2RZmt+TaDfXGZhXarqd6tqc1VtY/D4kb+rql8baTYTa9JnLrOwJgBJruwuviDJlcAtwFMjzaa6LrN61c2NwEeBJ7vzqAC/B2yFlR/LsMb0mceHgU8lOQv8CNhTa/N25rcAf57Bl838BPBXVfU36fGojDWoz1xmZV1eY0bXZKwZXZOrgcPd76QrgLur6oHVXBcfgSBJjZvJUzeSpP4MeklqnEEvSY0z6CWpcQa9JDXOoJekxhn0ktS4/wHO1GRKapmy/gAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[34]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;skyblue&#39;</span><span class="p">)</span>      <span class="c1"># 채우기색</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[34]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>(array([2., 0., 0., 0., 0., 0., 2., 0., 0., 1.]),
 array([2. , 2.3, 2.6, 2.9, 3.2, 3.5, 3.8, 4.1, 4.4, 4.7, 5. ]),
 &lt;BarContainer object of 10 artists&gt;)</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[35]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;skyblue&#39;</span><span class="p">,</span> <span class="n">edgecolor</span><span class="o">=</span><span class="s1">&#39;grey&#39;</span><span class="p">)</span>      <span class="c1"># 외곽선</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[35]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>(array([2., 0., 0., 0., 0., 0., 2., 0., 0., 1.]),
 array([2. , 2.3, 2.6, 2.9, 3.2, 3.5, 3.8, 4.1, 4.4, 4.7, 5. ]),
 &lt;BarContainer object of 10 artists&gt;)</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[36]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;skyblue&#39;</span><span class="p">,</span> <span class="n">edgecolor</span><span class="o">=</span><span class="s1">&#39;grey&#39;</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>      <span class="c1"># 투명도</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[36]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>(array([2., 0., 0., 0., 0., 0., 2., 0., 0., 1.]),
 array([2. , 2.3, 2.6, 2.9, 3.2, 3.5, 3.8, 4.1, 4.4, 4.7, 5. ]),
 &lt;BarContainer object of 10 artists&gt;)</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[37]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">y</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;y&#39;</span><span class="p">],</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;orange&#39;</span><span class="p">)</span>      <span class="c1"># 채우기색</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[37]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;matplotlib.collections.PathCollection at 0xaa38c70&gt;</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[38]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">y</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;y&#39;</span><span class="p">],</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="n">edgecolor</span><span class="o">=</span><span class="s1">&#39;blue&#39;</span><span class="p">)</span>      <span class="c1"># 외곽선</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[38]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;matplotlib.collections.PathCollection at 0xa7d84c0&gt;</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[39]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">y</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;y&#39;</span><span class="p">],</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="n">edgecolor</span><span class="o">=</span><span class="s1">&#39;blue&#39;</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>      <span class="c1"># 투명도</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[39]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;matplotlib.collections.PathCollection at 0xaa1f598&gt;</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[40]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Histogram with Normal Distribution Curve</span>
<span class="kn">from</span> <span class="nn">scipy</span> <span class="kn">import</span> <span class="n">stats</span>
<span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">fit</span><span class="o">=</span><span class="n">stats</span><span class="o">.</span><span class="n">norm</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr">
<pre>C:\Users\Admin\Anaconda3\lib\site-packages\seaborn\distributions.py:2551: FutureWarning: `distplot` is a deprecated function and will be removed in a future version. Please adapt your code to use either `displot` (a figure-level function with similar flexibility) or `histplot` (an axes-level function for histograms).
  warnings.warn(msg, FutureWarning)
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[40]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;AxesSubplot:xlabel=&#39;x1&#39;&gt;</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Graph Draw Full Code</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[41]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 다중줄수행 및 기타 옵션 </span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>                    <span class="c1"># Canvas 그리기</span>
<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">])</span>            <span class="c1"># Histogram</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">3</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;red&#39;</span><span class="p">,</span> <span class="n">ls</span><span class="o">=</span><span class="s1">&#39;dashed&#39;</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">)</span>      <span class="c1"># Vertical Line</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>                      <span class="c1"># plot 그리기의 종료(plt.show(), plot.close())</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[42]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Figure의 변수 저장 (plt.show)</span>
<span class="n">f</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axhline</span><span class="p">(</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="n">ls</span><span class="o">=</span><span class="s1">&#39;dashed&#39;</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">)</span>      <span class="c1"># Horizontal Line</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[43]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">f</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[43]:</div>




<div class="jp-RenderedImage jp-OutputArea-output jp-OutputArea-executeResult">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[44]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Figure의 변수 저장 (plt.close)</span>
<span class="n">f</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axhline</span><span class="p">(</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="n">ls</span><span class="o">=</span><span class="s1">&#39;dashed&#39;</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">)</span>      <span class="c1"># Horizontal Line</span>
<span class="n">plt</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[45]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">f</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[45]:</div>




<div class="jp-RenderedImage jp-OutputArea-output jp-OutputArea-executeResult">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><br>
<br>
<br>
<br>
<br></p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Scipy-(Statistics)">Scipy (Statistics)<a class="anchor-link" href="#Scipy-(Statistics)">&#182;</a></h2>
</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ Scipy Libarary 실행 """
from scipy import stats</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[46]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[46]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x2</th>
      <th>x3</th>
      <th>x4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>10</td>
      <td>2</td>
      <td>a</td>
      <td>10</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>13</td>
      <td>4</td>
      <td>a</td>
      <td>8</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>5</td>
      <td>b</td>
      <td>5</td>
      <td>g1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>2</td>
      <td>b</td>
      <td>12</td>
      <td>g2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>15</td>
      <td>4</td>
      <td>b</td>
      <td>7</td>
      <td>g3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ t-test <br>
&nbsp;$nbsp; '두집단의 평균이 같은지?'를 비교하는 모수적 통계방법</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[47]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">agg</span><span class="p">([</span><span class="s1">&#39;mean&#39;</span><span class="p">,</span> <span class="s1">&#39;std&#39;</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[47]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>y</th>
      <th>x1</th>
      <th>x3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>mean</th>
      <td>13.000000</td>
      <td>3.400000</td>
      <td>8.400000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>4.949747</td>
      <td>1.341641</td>
      <td>2.701851</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ 1 Sample t</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[48]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 1-sample t</span>
<span class="n">stats</span><span class="o">.</span><span class="n">ttest_1samp</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="mi">4</span><span class="p">)</span>   <span class="c1"># x1 Column의 평균이 4와 같은가?</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[48]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>Ttest_1sampResult(statistic=-1.0, pvalue=0.373900966300059)</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[49]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 1-sample t</span>
<span class="n">stats</span><span class="o">.</span><span class="n">ttest_1samp</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="mi">6</span><span class="p">)</span>   <span class="c1"># x1 Column의 평균이 6와 같은가?</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[49]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>Ttest_1sampResult(statistic=-4.333333333333333, pvalue=0.012317352470240385)</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[50]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># # visualization (histogram)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x1&#39;</span><span class="p">],</span> <span class="n">bins</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">fit</span><span class="o">=</span><span class="n">stats</span><span class="o">.</span><span class="n">norm</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">hist</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">4</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">,</span> <span class="n">ls</span><span class="o">=</span><span class="s1">&#39;dashed&#39;</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;4&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">6</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">,</span> <span class="n">ls</span><span class="o">=</span><span class="s1">&#39;dashed&#39;</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;brown&#39;</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;6&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr">
<pre>C:\Users\Admin\Anaconda3\lib\site-packages\seaborn\distributions.py:2551: FutureWarning: `distplot` is a deprecated function and will be removed in a future version. Please adapt your code to use either `displot` (a figure-level function with similar flexibility) or `histplot` (an axes-level function for histograms).
  warnings.warn(msg, FutureWarning)
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>○ 2 Sample t</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[51]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># gruop나누기</span>
<span class="n">t1_data</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x2&#39;</span><span class="p">]</span><span class="o">==</span><span class="s1">&#39;a&#39;</span><span class="p">][</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span>
<span class="n">t2_data</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;x2&#39;</span><span class="p">]</span><span class="o">==</span><span class="s1">&#39;b&#39;</span><span class="p">][</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[52]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">t1_data</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[52]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>0    2
1    4
Name: x1, dtype: int64</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[53]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">t2_data</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[53]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>2    5
3    2
4    4
Name: x1, dtype: int64</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[54]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="s1">&#39;x2&#39;</span><span class="p">)[</span><span class="s1">&#39;x1&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">agg</span><span class="p">([</span><span class="s1">&#39;mean&#39;</span><span class="p">,</span><span class="s1">&#39;std&#39;</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[54]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>mean</th>
      <th>std</th>
    </tr>
    <tr>
      <th>x2</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>3.000000</td>
      <td>1.414214</td>
    </tr>
    <tr>
      <th>b</th>
      <td>3.666667</td>
      <td>1.527525</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[55]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 2-sample t</span>
<span class="n">ttest_ind</span> <span class="o">=</span> <span class="n">stats</span><span class="o">.</span><span class="n">ttest_ind</span><span class="p">(</span><span class="n">t1_data</span><span class="p">,</span> <span class="n">t2_data</span><span class="p">,</span> <span class="n">equal_var</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>      <span class="c1"># 두개 그룹의 평균이 같은가?</span>
<span class="n">ttest_ind</span> <span class="c1"># 결과 : (t_value, p-value)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[55]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>Ttest_indResult(statistic=-0.4999999999999999, pvalue=0.6588098059554004)</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[56]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># visualization (Histogram)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">t1_data</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">fit</span><span class="o">=</span><span class="n">stats</span><span class="o">.</span><span class="n">norm</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">hist</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">fit_kws</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;color&#39;</span><span class="p">:</span><span class="s1">&#39;steelblue&#39;</span><span class="p">})</span>
<span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">t2_data</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">fit</span><span class="o">=</span><span class="n">stats</span><span class="o">.</span><span class="n">norm</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">hist</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">fit_kws</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;color&#39;</span><span class="p">:</span><span class="s1">&#39;orange&#39;</span><span class="p">})</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="n">t1_data</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">,</span> <span class="n">ls</span><span class="o">=</span><span class="s1">&#39;dashed&#39;</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;steelblue&#39;</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;t1&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="n">t2_data</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">,</span> <span class="n">ls</span><span class="o">=</span><span class="s1">&#39;dashed&#39;</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;t2&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr">
<pre>C:\Users\Admin\Anaconda3\lib\site-packages\seaborn\distributions.py:2551: FutureWarning: `distplot` is a deprecated function and will be removed in a future version. Please adapt your code to use either `displot` (a figure-level function with similar flexibility) or `histplot` (an axes-level function for histograms).
  warnings.warn(msg, FutureWarning)
C:\Users\Admin\Anaconda3\lib\site-packages\seaborn\distributions.py:2551: FutureWarning: `distplot` is a deprecated function and will be removed in a future version. Please adapt your code to use either `displot` (a figure-level function with similar flexibility) or `histplot` (an axes-level function for histograms).
  warnings.warn(msg, FutureWarning)
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[57]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># visualization (boxplot)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">boxplot</span><span class="p">([</span><span class="n">t1_data</span><span class="p">,</span> <span class="n">t2_data</span><span class="p">],</span> <span class="n">showmeans</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">meanprops</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;marker&#39;</span><span class="p">:</span><span class="s1">&#39;o&#39;</span><span class="p">,</span> <span class="s1">&#39;markerfacecolor&#39;</span><span class="p">:</span><span class="s1">&#39;red&#39;</span><span class="p">,</span> <span class="s1">&#39;markeredgecolor&#39;</span><span class="p">:</span><span class="s1">&#39;none&#39;</span><span class="p">})</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">([</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">],</span> <span class="p">[</span><span class="s1">&#39;t1&#39;</span><span class="p">,</span> <span class="s1">&#39;t2&#39;</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[58]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># visualization (vertical boxplot)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">boxplot</span><span class="p">([</span><span class="n">t1_data</span><span class="p">,</span> <span class="n">t2_data</span><span class="p">],</span> <span class="n">vert</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">showmeans</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">meanprops</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;marker&#39;</span><span class="p">:</span><span class="s1">&#39;o&#39;</span><span class="p">,</span> <span class="s1">&#39;markerfacecolor&#39;</span><span class="p">:</span><span class="s1">&#39;red&#39;</span><span class="p">,</span> <span class="s1">&#39;markeredgecolor&#39;</span><span class="p">:</span><span class="s1">&#39;none&#39;</span><span class="p">})</span>
<span class="n">plt</span><span class="o">.</span><span class="n">yticks</span><span class="p">([</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">],</span> <span class="p">[</span><span class="s1">&#39;t1&#39;</span><span class="p">,</span> <span class="s1">&#39;t2&#39;</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAW4AAAD4CAYAAADM6gxlAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjMuMSwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/d3fzzAAAACXBIWXMAAAsTAAALEwEAmpwYAAALPklEQVR4nO3cb4il51nH8d+1TVolzXZnTdDYdF0ogmDA7LLESkBsEYlJWVkQLMXWihg0vqggSBUxCfRFoSCioBL0hfUPotSVJdlsLdqiFmPJbmKbGqEVWgwpxGYnTUolUOf2xZng7Di7cyYz58919vOBYXae8+zMdeee+eac55zZGmMEgD4OLXoAAPZGuAGaEW6AZoQboBnhBmjmhll/gVtuuWUcP3581l8GYKVcvHjxa2OMW3e6bebhPn78eJ588slZfxmAlVJVX7nabS6VADQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzQj3ADNCDdAM8IN0IxwAzRzw6IHoJ+jR49mfX190WOwzXjwcOrhlxc9xr6tra3l8uXLix5jqQk3e7a+vp4xxqLHYLuH3rIS+1JVix5h6blUAtCMcAM0s/Th9rAJ6GpW/bpmuKvqSFU9sPnnO6vqn6vqC1X1uar6qZlMBF1sbCTnzycf/vDk/cbGoifiOrHbk5NHkjyQ5PeSfDPJ+8cYX6yq705ysao+McZ4abYjwhLa2EjOnEnOnfu/Y6dPJ2fPJoeW/oEsze32HfaRJG+vqqeT/PwY44tJMsZ4PskLSW6d7XiwpC5cuDLayeTjCxcWMw/Xld3ucX8oyR1jjDu3Hqyqu5K8Mcl/7PSXqur+JPcnybFjx/Y9pOvcLJ1Ll3Y+/tRTyb33zneWFeRn/tr2/DruqrotyZ8k+Zkxxo4X9cYYjyR5JElOnTq17xeWrsJrU1eJH6okJ0/ufPzEifnOsaJW5Wd+IU9O7jDE4SSPJfmNMcYTM5kIOrjnnsk17a1On54chxnb7R73K0luTpKqemOSs0k+Nsb4q1kPBkvt0KHJE5EXLkwuj5w4MYm2JyaZg2uGe4zxYlV9pqqeSXJTktuTfEdVfWDzlA+MMZ6e7YiwpA4dmlzPdk2bOdv1GvcY473zGOQaX3+RXx7gdZtVvzyuA2hGuAGa8c+68rp4SeDyGQ8eXol9WVtbW/QIS0+42TPPOyyv8dCiJ2AeXCoBaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZoRboBmhBugGeEGaEa4AZq5YdEDXC+OHj2a9fX1RY9xIMaDh1MPv7zoMQ7E2tpaLl++vOgxYE+Ee07W19czxlj0GAfjobeszFqqatEjwJ65VALQjHADNLP04fZQFqbjZ+X6cc1wV9WRqnpgy8cXquqlqnp09qOxdDY2kvPnk394dfJ+Y2PRE8F1abd73EeSPLDl448med/MpmF5bWwkZ84k992XfOrVyfszZ8QbFmC3cH8kydur6umq+ugY4++SvDKHuVg2Fy4k585deezcuclxYK52ezngh5LcMca4cy+ftKruT3J/khw7duz1TXbl59v352CfLl3a+fhTTyX33jvfWQ6Y7y+6mcnruMcYjyR5JElOnTq17xf8rsJrhtvH4eTJnY+fODHfOWZgFb6/khX4HmNqS/+qEpbEPfckp09feez06clxYK52C/crSW6exyAsuUOHkrNnk8ceS975psn7s2cnx4G5uualkjHGi1X1map6JsnjSd6R5PuSvLmqnkvyc2OMT8xhTpbBoUOT69mffVP769rQ2a7XuMcY753HIABMZ+kf567KE0cwa35Wrh9LH24AriTcAM3497jnaFVeZzsePLwya1lbW1v0CLBnwj0nq3b9cTy06Ang+uVSCUAzwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM0IN0Azwg3QjHADNCPcAM3UGGO2X6Dqv5J8ZR+f4pYkXzugcRZpVdaRWMuyWpW1rMo6kv2t5XvGGLfudMPMw71fVfXkGOPUoufYr1VZR2Ity2pV1rIq60hmtxaXSgCaEW6AZjqE+5FFD3BAVmUdibUsq1VZy6qsI5nRWpb+GjcAV+pwjxuALYQboJmFh7uq3lZVn6qqZ6vqC1X1wR3Oqar6nar6UlV9rqpOLmLW3Uy5lh+pqq9X1dObb7+5iFl3U1XfVlWfrap/3VzLwzuc02VfpllLi31Jkqp6Q1U9VVWP7nBbiz15zS5r6bQnX66qz2/O+eQOtx/ovtywn798QL6V5FfGGJeq6uYkF6vqk2OMf9tyzo8n+d7Ntx9M8vub75fNNGtJkn8cY7x7AfPtxatJ3jXG+EZV3Zjkn6rq8THGE1vO6bIv06wl6bEvSfLBJM8mObzDbV325DXXWkvSZ0+S5J1jjKv9ss2B7svC73GPMb46xri0+edXMtnEt2477SeSfGxMPJHkSFXdNudRdzXlWlrY/G/9jc0Pb9x82/5Mdpd9mWYtLVTV7UnuS/KHVzmlxZ4kU61llRzoviw83FtV1fEkJ5L8y7ab3prkP7d8/FyWPIjXWEuS/NDmw/bHq+r75zvZ9DYfxj6d5IUknxxjtN2XKdaS9NiX307yq0k2rnJ7mz3J7mtJeuxJMrkj8LdVdbGq7t/h9gPdl6UJd1W9OcnHk/zyGOPl7Tfv8FeW9h7TLmu5lMm/QfADSX43yd/MebypjTH+Z4xxZ5Lbk9xVVXdsO6XNvkyxlqXfl6p6d5IXxhgXr3XaDseWbk+mXMvS78kWd48xTmZySeSXquqHt91+oPuyFOHevO748SR/Nsb46x1OeS7J27Z8fHuS5+cx217ttpYxxsuvPWwfY5xPcmNV3TLnMfdkjPFSkk8nuWfbTW325TVXW0uTfbk7yemq+nKSv0jyrqr6023ndNmTXdfSZE+SJGOM5zffv5DkbJK7tp1yoPuy8HBXVSX5oyTPjjF+6yqnnUvy/s1nZt+R5OtjjK/ObcgpTbOWqvquzfNSVXdlsgcvzm/K6VTVrVV1ZPPP357kR5P8+7bTuuzLrmvpsC9jjF8bY9w+xjie5D1J/n6M8dPbTmuxJ9OspcOeJElV3bT5YoRU1U1JfizJM9tOO9B9WYZXldyd5H1JPr95DTJJfj3JsSQZY/xBkvNJ7k3ypSTfTPKz8x9zKtOs5SeT/GJVfSvJfyd5z1jOX1+9LckfV9UbMvmB+csxxqNV9QtJu32ZZi1d9uX/abonO2q6J9+Z5Ozm/2NuSPLnY4wLs9wXv/IO0MzCL5UAsDfCDdCMcAM0I9wAzQg3QDPCDdCMcAM0878rwEKcyfR0JAAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>

</div>

</div>
</body>







</html>
