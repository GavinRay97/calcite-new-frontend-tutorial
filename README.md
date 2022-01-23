<html lang="en" theme="idea"><head>
    <meta charset="UTF-8">
    <title>Calcite Frontend Guide</title>
    
    
    
    
    

    



<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no">






<!-- Google Tag Manager -->

<!-- End Google Tag Manager -->



    










<style>::-ms-clear{display:none}.monaco-editor .editor-widget input{color:inherit}.monaco-editor{position:relative;overflow:visible;-webkit-text-size-adjust:100%}.monaco-editor .overflow-guard{position:relative;overflow:hidden}.monaco-editor .view-overlays{position:absolute;top:0}.monaco-diff-editor .diffOverview{z-index:9}.monaco-diff-editor .diffOverview .diffViewport{z-index:10}.monaco-diff-editor.vs .diffOverview{background:rgba(0,0,0,.03)}.monaco-diff-editor.vs-dark .diffOverview{background:rgba(255,255,255,.01)}.monaco-scrollable-element.modified-in-monaco-diff-editor.vs .scrollbar{background:rgba(0,0,0,0)}.monaco-scrollable-element.modified-in-monaco-diff-editor.vs-dark .scrollbar{background:rgba(0,0,0,0)}.monaco-scrollable-element.modified-in-monaco-diff-editor.hc-black .scrollbar{background:0 0}.monaco-scrollable-element.modified-in-monaco-diff-editor .slider{z-index:10}.modified-in-monaco-diff-editor .slider.active{background:rgba(171,171,171,.4)}.modified-in-monaco-diff-editor.hc-black .slider.active{background:0 0}.monaco-diff-editor .delete-sign,.monaco-diff-editor .insert-sign,.monaco-editor .delete-sign,.monaco-editor .insert-sign{font-size:11px!important;opacity:.7!important;display:flex!important;align-items:center}.monaco-diff-editor.hc-black .delete-sign,.monaco-diff-editor.hc-black .insert-sign,.monaco-editor.hc-black .delete-sign,.monaco-editor.hc-black .insert-sign{opacity:1}.monaco-editor .inline-deleted-margin-view-zone{text-align:right}.monaco-editor .inline-added-margin-view-zone{text-align:right}.monaco-editor .view-zones .view-lines .view-line span{display:inline-block}.monaco-editor .margin-view-zones .lightbulb-glyph:hover{cursor:pointer}.monaco-editor .bracket-match{box-sizing:border-box}.monaco-editor.vs .dnd-target{border-right:2px dotted #000;color:#fff}.monaco-editor.vs-dark .dnd-target{border-right:2px dotted #aeafad;color:#51504f}.monaco-editor.hc-black .dnd-target{border-right:2px dotted #fff;color:#000}.monaco-editor.hc-black.mac.mouse-default .view-lines,.monaco-editor.mouse-default .view-lines,.monaco-editor.vs-dark.mac.mouse-default .view-lines{cursor:default}.monaco-editor.hc-black.mac.mouse-copy .view-lines,.monaco-editor.mouse-copy .view-lines,.monaco-editor.vs-dark.mac.mouse-copy .view-lines{cursor:copy}.monaco-editor .detected-link,.monaco-editor .detected-link-active{text-decoration:underline;text-underline-position:under}.monaco-editor .detected-link-active{cursor:pointer}.monaco-editor .tokens-inspect-widget{z-index:50;user-select:text;-webkit-user-select:text;-ms-user-select:text;padding:10px}.tokens-inspect-separator{height:1px;border:0}.monaco-editor .tokens-inspect-widget .tm-token{font-family:var(--monaco-monospace-font)}.monaco-editor .tokens-inspect-widget .tm-token-length{font-weight:400;font-size:60%;float:right}.monaco-editor .tokens-inspect-widget .tm-metadata-table{width:100%}.monaco-editor .tokens-inspect-widget .tm-metadata-value{font-family:var(--monaco-monospace-font);text-align:right}.monaco-editor .tokens-inspect-widget .tm-token-type{font-family:var(--monaco-monospace-font)}.monaco-editor .iPadShowKeyboard{width:58px;min-width:0;height:36px;min-height:0;margin:0;padding:0;position:absolute;resize:none;overflow:hidden;background:url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNTMiIGhlaWdodD0iMzYiIHZpZXdCb3g9IjAgMCA1MyAzNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwKSI+CjxwYXRoIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNNDguMDM2NCA0LjAxMDQySDQuMDA3NzlMNC4wMDc3OSAzMi4wMjg2SDQ4LjAzNjRWNC4wMTA0MlpNNC4wMDc3OSAwLjAwNzgxMjVDMS43OTcyMSAwLjAwNzgxMjUgMC4wMDUxODc5OSAxLjc5OTg0IDAuMDA1MTg3OTkgNC4wMTA0MlYzMi4wMjg2QzAuMDA1MTg3OTkgMzQuMjM5MiAxLjc5NzIxIDM2LjAzMTIgNC4wMDc3OSAzNi4wMzEySDQ4LjAzNjRDNTAuMjQ3IDM2LjAzMTIgNTIuMDM5IDM0LjIzOTIgNTIuMDM5IDMyLjAyODZWNC4wMTA0MkM1Mi4wMzkgMS43OTk4NCA1MC4yNDcgMC4wMDc4MTI1IDQ4LjAzNjQgMC4wMDc4MTI1SDQuMDA3NzlaTTguMDEwNDIgOC4wMTMwMkgxMi4wMTNWMTIuMDE1Nkg4LjAxMDQyVjguMDEzMDJaTTIwLjAxODIgOC4wMTMwMkgxNi4wMTU2VjEyLjAxNTZIMjAuMDE4MlY4LjAxMzAyWk0yNC4wMjA4IDguMDEzMDJIMjguMDIzNFYxMi4wMTU2SDI0LjAyMDhWOC4wMTMwMlpNMzYuMDI4NiA4LjAxMzAySDMyLjAyNlYxMi4wMTU2SDM2LjAyODZWOC4wMTMwMlpNNDAuMDMxMiA4LjAxMzAySDQ0LjAzMzlWMTIuMDE1Nkg0MC4wMzEyVjguMDEzMDJaTTE2LjAxNTYgMTYuMDE4Mkg4LjAxMDQyVjIwLjAyMDhIMTYuMDE1NlYxNi4wMTgyWk0yMC4wMTgyIDE2LjAxODJIMjQuMDIwOFYyMC4wMjA4SDIwLjAxODJWMTYuMDE4MlpNMzIuMDI2IDE2LjAxODJIMjguMDIzNFYyMC4wMjA4SDMyLjAyNlYxNi4wMTgyWk00NC4wMzM5IDE2LjAxODJWMjAuMDIwOEgzNi4wMjg2VjE2LjAxODJINDQuMDMzOVpNMTIuMDEzIDI0LjAyMzRIOC4wMTA0MlYyOC4wMjZIMTIuMDEzVjI0LjAyMzRaTTE2LjAxNTYgMjQuMDIzNEgzNi4wMjg2VjI4LjAyNkgxNi4wMTU2VjI0LjAyMzRaTTQ0LjAzMzkgMjQuMDIzNEg0MC4wMzEyVjI4LjAyNkg0NC4wMzM5VjI0LjAyMzRaIiBmaWxsPSIjNDI0MjQyIi8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDAiPgo8cmVjdCB3aWR0aD0iNTMiIGhlaWdodD0iMzYiIGZpbGw9IndoaXRlIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==) center center no-repeat;border:4px solid #f6f6f6;border-radius:4px}.monaco-editor.vs-dark .iPadShowKeyboard{background:url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNTMiIGhlaWdodD0iMzYiIHZpZXdCb3g9IjAgMCA1MyAzNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwKSI+CjxwYXRoIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNNDguMDM2NCA0LjAxMDQySDQuMDA3NzlMNC4wMDc3OSAzMi4wMjg2SDQ4LjAzNjRWNC4wMTA0MlpNNC4wMDc3OSAwLjAwNzgxMjVDMS43OTcyMSAwLjAwNzgxMjUgMC4wMDUxODc5OSAxLjc5OTg0IDAuMDA1MTg3OTkgNC4wMTA0MlYzMi4wMjg2QzAuMDA1MTg3OTkgMzQuMjM5MiAxLjc5NzIxIDM2LjAzMTIgNC4wMDc3OSAzNi4wMzEySDQ4LjAzNjRDNTAuMjQ3IDM2LjAzMTIgNTIuMDM5IDM0LjIzOTIgNTIuMDM5IDMyLjAyODZWNC4wMTA0MkM1Mi4wMzkgMS43OTk4NCA1MC4yNDcgMC4wMDc4MTI1IDQ4LjAzNjQgMC4wMDc4MTI1SDQuMDA3NzlaTTguMDEwNDIgOC4wMTMwMkgxMi4wMTNWMTIuMDE1Nkg4LjAxMDQyVjguMDEzMDJaTTIwLjAxODIgOC4wMTMwMkgxNi4wMTU2VjEyLjAxNTZIMjAuMDE4MlY4LjAxMzAyWk0yNC4wMjA4IDguMDEzMDJIMjguMDIzNFYxMi4wMTU2SDI0LjAyMDhWOC4wMTMwMlpNMzYuMDI4NiA4LjAxMzAySDMyLjAyNlYxMi4wMTU2SDM2LjAyODZWOC4wMTMwMlpNNDAuMDMxMiA4LjAxMzAySDQ0LjAzMzlWMTIuMDE1Nkg0MC4wMzEyVjguMDEzMDJaTTE2LjAxNTYgMTYuMDE4Mkg4LjAxMDQyVjIwLjAyMDhIMTYuMDE1NlYxNi4wMTgyWk0yMC4wMTgyIDE2LjAxODJIMjQuMDIwOFYyMC4wMjA4SDIwLjAxODJWMTYuMDE4MlpNMzIuMDI2IDE2LjAxODJIMjguMDIzNFYyMC4wMjA4SDMyLjAyNlYxNi4wMTgyWk00NC4wMzM5IDE2LjAxODJWMjAuMDIwOEgzNi4wMjg2VjE2LjAxODJINDQuMDMzOVpNMTIuMDEzIDI0LjAyMzRIOC4wMTA0MlYyOC4wMjZIMTIuMDEzVjI0LjAyMzRaTTE2LjAxNTYgMjQuMDIzNEgzNi4wMjg2VjI4LjAyNkgxNi4wMTU2VjI0LjAyMzRaTTQ0LjAzMzkgMjQuMDIzNEg0MC4wMzEyVjI4LjAyNkg0NC4wMzM5VjI0LjAyMzRaIiBmaWxsPSIjQzVDNUM1Ii8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDAiPgo8cmVjdCB3aWR0aD0iNTMiIGhlaWdodD0iMzYiIGZpbGw9IndoaXRlIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==) center center no-repeat;border:4px solid #252526}.monaco-aria-container{position:absolute;left:-999em}:root{--sash-size:4px}.monaco-sash{position:absolute;z-index:35;touch-action:none}.monaco-sash.disabled{pointer-events:none}.monaco-sash.mac.vertical{cursor:col-resize}.monaco-sash.vertical.minimum{cursor:e-resize}.monaco-sash.vertical.maximum{cursor:w-resize}.monaco-sash.mac.horizontal{cursor:row-resize}.monaco-sash.horizontal.minimum{cursor:s-resize}.monaco-sash.horizontal.maximum{cursor:n-resize}.monaco-sash.disabled{cursor:default!important;pointer-events:none!important}.monaco-sash.vertical{cursor:ew-resize;top:0;width:var(--sash-size);height:100%}.monaco-sash.horizontal{cursor:ns-resize;left:0;width:100%;height:var(--sash-size)}.monaco-sash:not(.disabled)>.orthogonal-drag-handle{content:" ";height:calc(var(--sash-size) * 2);width:calc(var(--sash-size) * 2);z-index:100;display:block;cursor:all-scroll;position:absolute}.monaco-sash.horizontal.orthogonal-edge-north:not(.disabled)>.orthogonal-drag-handle.start,.monaco-sash.horizontal.orthogonal-edge-south:not(.disabled)>.orthogonal-drag-handle.end{cursor:nwse-resize}.monaco-sash.horizontal.orthogonal-edge-north:not(.disabled)>.orthogonal-drag-handle.end,.monaco-sash.horizontal.orthogonal-edge-south:not(.disabled)>.orthogonal-drag-handle.start{cursor:nesw-resize}.monaco-sash.vertical>.orthogonal-drag-handle.start{left:calc(var(--sash-size) * -.5);top:calc(var(--sash-size) * -1)}.monaco-sash.vertical>.orthogonal-drag-handle.end{left:calc(var(--sash-size) * -.5);bottom:calc(var(--sash-size) * -1)}.monaco-sash.horizontal>.orthogonal-drag-handle.start{top:calc(var(--sash-size) * -.5);left:calc(var(--sash-size) * -1)}.monaco-sash.horizontal>.orthogonal-drag-handle.end{top:calc(var(--sash-size) * -.5);right:calc(var(--sash-size) * -1)}.monaco-sash:before{content:'';pointer-events:none;position:absolute;width:100%;height:100%;transition:background-color .1s ease-out;background:0 0}.monaco-sash.vertical:before{width:var(--sash-hover-size);left:calc(50% - (var(--sash-hover-size)/ 2))}.monaco-sash.horizontal:before{height:var(--sash-hover-size);top:calc(50% - (var(--sash-hover-size)/ 2))}.monaco-sash.debug{background:#0ff}.monaco-sash.debug.disabled{background:rgba(0,255,255,.2)}.monaco-sash.debug:not(.disabled)>.orthogonal-drag-handle{background:red}.monaco-diff-editor .diff-review-line-number{text-align:right;display:inline-block}.monaco-diff-editor .diff-review{position:absolute;user-select:none;-webkit-user-select:none;-ms-user-select:none}.monaco-diff-editor .diff-review-summary{padding-left:10px}.monaco-diff-editor .diff-review-shadow{position:absolute}.monaco-diff-editor .diff-review-row{white-space:pre}.monaco-diff-editor .diff-review-table{display:table;min-width:100%}.monaco-diff-editor .diff-review-row{display:table-row;width:100%}.monaco-diff-editor .diff-review-spacer{display:inline-block;width:10px;vertical-align:middle}.monaco-diff-editor .diff-review-spacer>.codicon{font-size:9px!important}.monaco-diff-editor .diff-review-actions{display:inline-block;position:absolute;right:10px;top:2px}.monaco-diff-editor .diff-review-actions .action-label{width:16px;height:16px;margin:2px 0}.monaco-mouse-cursor-text{cursor:text}.hc-black .mac .monaco-mouse-cursor-text,.hc-black.mac .monaco-mouse-cursor-text,.vs-dark .mac .monaco-mouse-cursor-text,.vs-dark.mac .monaco-mouse-cursor-text{cursor:-webkit-image-set(url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAQAAAC1+jfqAAAAL0lEQVQoz2NgCD3x//9/BhBYBWdhgFVAiVW4JBFKGIa4AqD0//9D3pt4I4tAdAMAHTQ/j5Zom30AAAAASUVORK5CYII=) 1x,url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAAz0lEQVRIx2NgYGBY/R8I/vx5eelX3n82IJ9FxGf6tksvf/8FiTMQAcAGQMDvSwu09abffY8QYSAScNk45G198eX//yev73/4///701eh//kZSARckrNBRvz//+8+6ZohwCzjGNjdgQxkAg7B9WADeBjIBqtJCbhRA0YNoIkBSNmaPEMoNmA0FkYNoFKhapJ6FGyAH3nauaSmPfwI0v/3OukVi0CIZ+F25KrtYcx/CTIy0e+rC7R1Z4KMICVTQQ14feVXIbR695u14+Ir4gwAAD49E54wc1kWAAAAAElFTkSuQmCC) 2x) 5 8,text}.monaco-editor .codelens-decoration{overflow:hidden;display:inline-block;text-overflow:ellipsis;white-space:nowrap;color:var(--vscode-editorCodeLens-foreground)}.monaco-editor .codelens-decoration>a,.monaco-editor .codelens-decoration>span{user-select:none;-webkit-user-select:none;-ms-user-select:none;white-space:nowrap;vertical-align:sub}.monaco-editor .codelens-decoration>a{text-decoration:none}.monaco-editor .codelens-decoration>a:hover{cursor:pointer;color:var(--vscoce-editorLink-activeForeground)!important}.monaco-editor .codelens-decoration>a:hover .codicon{color:var(--vscoce-editorLink-activeForeground)!important}.monaco-editor .codelens-decoration .codicon{vertical-align:middle;color:currentColor!important;color:var(--vscode-editorCodeLens-foreground)}.monaco-editor .codelens-decoration>a:hover .codicon::before{cursor:pointer}@keyframes fadein{0%{opacity:0;visibility:visible}100%{opacity:1}}.monaco-editor .codelens-decoration.fadein{animation:fadein .1s linear}.monaco-editor .monaco-editor-overlaymessage{padding-bottom:8px;z-index:10000}.monaco-editor .monaco-editor-overlaymessage.below{padding-bottom:0;padding-top:8px;z-index:10000}@keyframes fadeIn{from{opacity:0}to{opacity:1}}.monaco-editor .monaco-editor-overlaymessage.fadeIn{animation:fadeIn 150ms ease-out}@keyframes fadeOut{from{opacity:1}to{opacity:0}}.monaco-editor .monaco-editor-overlaymessage.fadeOut{animation:fadeOut .1s ease-out}.monaco-editor .monaco-editor-overlaymessage .message{padding:1px 4px;color:var(--vscode-inputValidation-infoForeground);background-color:var(--vscode-inputValidation-infoBackground);border:1px solid var(--vscode-inputValidation-infoBorder)}.monaco-editor.hc-black .monaco-editor-overlaymessage .message{border-width:2px}.monaco-editor .monaco-editor-overlaymessage .anchor{width:0!important;height:0!important;border-color:transparent;border-style:solid;z-index:1000;border-width:8px;position:absolute}.monaco-editor .monaco-editor-overlaymessage .anchor.top{border-bottom-color:var(--vscode-inputValidation-infoBorder)}.monaco-editor .monaco-editor-overlaymessage .anchor.below{border-top-color:var(--vscode-inputValidation-infoBorder)}.monaco-editor .monaco-editor-overlaymessage.below .anchor.below,.monaco-editor .monaco-editor-overlaymessage:not(.below) .anchor.top{display:none}.monaco-editor .monaco-editor-overlaymessage.below .anchor.top{display:inherit;top:-8px}.monaco-editor .peekview-widget .head{box-sizing:border-box;display:flex}.monaco-editor .peekview-widget .head .peekview-title{display:flex;align-items:center;font-size:13px;margin-left:20px;min-width:0}.monaco-editor .peekview-widget .head .peekview-title.clickable{cursor:pointer}.monaco-editor .peekview-widget .head .peekview-title .dirname:not(:empty){font-size:.9em;margin-left:.5em}.monaco-editor .peekview-widget .head .peekview-title .meta{white-space:nowrap}.monaco-editor .peekview-widget .head .peekview-title .dirname{white-space:nowrap}.monaco-editor .peekview-widget .head .peekview-title .filename{overflow:hidden;text-overflow:ellipsis;white-space:nowrap}.monaco-editor .peekview-widget .head .peekview-title .meta:not(:empty)::before{content:'-';padding:0 .3em}.monaco-editor .peekview-widget .head .peekview-actions{flex:1;text-align:right;padding-right:2px}.monaco-editor .peekview-widget .head .peekview-actions>.monaco-action-bar{display:inline-block}.monaco-editor .peekview-widget .head .peekview-actions>.monaco-action-bar,.monaco-editor .peekview-widget .head .peekview-actions>.monaco-action-bar>.actions-container{height:100%}.monaco-editor .peekview-widget>.body{border-top:1px solid;position:relative}.monaco-editor .peekview-widget .head .peekview-title .codicon{margin-right:4px}.monaco-editor .peekview-widget .monaco-list .monaco-list-row.focused .codicon{color:inherit!important}.monaco-editor .goto-definition-link{text-decoration:underline;cursor:pointer}.monaco-editor .parameter-hints-widget{z-index:10;display:flex;flex-direction:column;line-height:1.5em}.monaco-editor .parameter-hints-widget>.phwrapper{max-width:440px;display:flex;flex-direction:row}.monaco-editor .parameter-hints-widget.multiple{min-height:3.3em;padding:0}.monaco-editor .parameter-hints-widget.visible{transition:left .05s ease-in-out}.monaco-editor .parameter-hints-widget p,.monaco-editor .parameter-hints-widget ul{margin:8px 0}.monaco-editor .parameter-hints-widget .body,.monaco-editor .parameter-hints-widget .monaco-scrollable-element{display:flex;flex:1;flex-direction:column;min-height:100%}.monaco-editor .parameter-hints-widget .signature{padding:4px 5px}.monaco-editor .parameter-hints-widget .docs{padding:0 10px 0 5px;white-space:pre-wrap}.monaco-editor .parameter-hints-widget .docs.empty{display:none}.monaco-editor .parameter-hints-widget .docs .markdown-docs{white-space:initial}.monaco-editor .parameter-hints-widget .docs .markdown-docs code{font-family:var(--monaco-monospace-font)}.monaco-editor .parameter-hints-widget .docs .code{white-space:pre-wrap}.monaco-editor .parameter-hints-widget .docs code{border-radius:3px;padding:0 .4em}.monaco-editor .parameter-hints-widget .controls{display:none;flex-direction:column;align-items:center;min-width:22px;justify-content:flex-end}.monaco-editor .parameter-hints-widget.multiple .controls{display:flex;padding:0 2px}.monaco-editor .parameter-hints-widget.multiple .button{width:16px;height:16px;background-repeat:no-repeat;cursor:pointer}.monaco-editor .parameter-hints-widget .button.previous{bottom:24px}.monaco-editor .parameter-hints-widget .overloads{text-align:center;height:12px;line-height:12px;opacity:.5;font-family:var(--monaco-monospace-font)}.monaco-editor .parameter-hints-widget .signature .parameter.active{font-weight:700}.monaco-editor .parameter-hints-widget .documentation-parameter>.parameter{font-weight:700;margin-right:.5em}.monaco-editor .rename-box{z-index:100;color:inherit}.monaco-editor .rename-box.preview{padding:3px 3px 0 3px}.monaco-editor .rename-box .rename-input{padding:3px;width:calc(100% - 6px)}.monaco-editor .rename-box .rename-label{display:none;opacity:.8}.monaco-editor .rename-box.preview .rename-label{display:inherit}.monaco-editor .snippet-placeholder{min-width:2px;outline-style:solid;outline-width:1px;background-color:var(--vscode-editor-snippetTabstopHighlightBackground,transparent);outline-color:var(--vscode-editor-snippetTabstopHighlightBorder,transparent)}.monaco-editor .finish-snippet-placeholder{outline-style:solid;outline-width:1px;background-color:var(--vscode-editor-snippetFinalTabstopHighlightBackground,transparent);outline-color:var(--vscode-editor-snippetFinalTabstopHighlightBorder,transparent)}.monaco-editor .suggest-widget{width:430px;z-index:40;display:flex;flex-direction:column}.monaco-editor .suggest-widget.message{flex-direction:row;align-items:center}.monaco-editor .suggest-details,.monaco-editor .suggest-widget{flex:0 1 auto;width:100%;border-style:solid;border-width:1px;border-color:var(--vscode-editorSuggestWidget-border);background-color:var(--vscode-editorSuggestWidget-background)}.monaco-editor.hc-black .suggest-details,.monaco-editor.hc-black .suggest-widget{border-width:2px}.monaco-editor .suggest-widget .suggest-status-bar{box-sizing:border-box;display:none;flex-flow:row nowrap;justify-content:space-between;width:100%;font-size:80%;padding:0 4px 0 4px;border-top:1px solid var(--vscode-editorSuggestWidget-border);overflow:hidden}.monaco-editor .suggest-widget.with-status-bar .suggest-status-bar{display:flex}.monaco-editor .suggest-widget .suggest-status-bar .left{padding-right:8px}.monaco-editor .suggest-widget.with-status-bar .suggest-status-bar .action-label{color:var(--vscode-editorSuggestWidgetStatus-foreground)}.monaco-editor .suggest-widget.with-status-bar .suggest-status-bar .action-item:not(:last-of-type) .action-label{margin-right:0}.monaco-editor .suggest-widget.with-status-bar .suggest-status-bar .action-item:not(:last-of-type) .action-label::after{content:', ';margin-right:.3em}.monaco-editor .suggest-widget.with-status-bar .monaco-list .monaco-list-row.focused.string-label>.contents>.main>.right>.readMore,.monaco-editor .suggest-widget.with-status-bar .monaco-list .monaco-list-row>.contents>.main>.right>.readMore{display:none}.monaco-editor .suggest-widget.with-status-bar:not(.docs-side) .monaco-list .monaco-list-row:hover>.contents>.main>.right.can-expand-details>.details-label{width:100%}.monaco-editor .suggest-widget>.message{padding-left:22px}.monaco-editor .suggest-widget>.tree{height:100%;width:100%}.monaco-editor .suggest-widget .monaco-list{user-select:none;-webkit-user-select:none;-ms-user-select:none}.monaco-editor .suggest-widget .monaco-list .monaco-list-row{display:flex;-mox-box-sizing:border-box;box-sizing:border-box;padding-right:10px;background-repeat:no-repeat;background-position:2px 2px;white-space:nowrap;cursor:pointer;touch-action:none}.monaco-editor .suggest-widget .monaco-list .monaco-list-row.focused{color:var(--vscode-editorSuggestWidget-selectedForeground)}.monaco-editor .suggest-widget .monaco-list .monaco-list-row.focused .codicon{color:var(--vscode-editorSuggestWidget-selectedIconForeground)}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents{flex:1;height:100%;overflow:hidden;padding-left:2px}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main{display:flex;overflow:hidden;text-overflow:ellipsis;white-space:pre;justify-content:space-between}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.left,.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right{display:flex}.monaco-editor .suggest-widget:not(.frozen) .monaco-highlighted-label .highlight{font-weight:700}.monaco-editor .suggest-widget .monaco-list .monaco-list-row .monaco-highlighted-label .highlight{color:var(--vscode-editorSuggestWidget-highlightForeground)}.monaco-editor .suggest-widget .monaco-list .monaco-list-row.focused .monaco-highlighted-label .highlight{color:var(--vscode-editorSuggestWidget-focusHighlightForeground)}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.header>.codicon-close,.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right>.readMore::before{color:inherit;opacity:1;font-size:14px;cursor:pointer}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.header>.codicon-close{position:absolute;top:6px;right:2px}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.header>.codicon-close:hover,.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right>.readMore:hover{opacity:1}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right>.details-label{opacity:.7}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.left>.signature-label{overflow:hidden;text-overflow:ellipsis;opacity:.6}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.left>.qualifier-label{margin-left:12px;opacity:.4;font-size:85%;line-height:initial;text-overflow:ellipsis;overflow:hidden;align-self:center}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right>.details-label{font-size:85%;margin-left:1.1em;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right>.details-label>.monaco-tokenized-source{display:inline}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right>.details-label{display:none}.monaco-editor .suggest-widget:not(.shows-details) .monaco-list .monaco-list-row.focused>.contents>.main>.right>.details-label{display:inline}.monaco-editor .suggest-widget .monaco-list .monaco-list-row:not(.string-label)>.contents>.main>.right>.details-label,.monaco-editor .suggest-widget.docs-side .monaco-list .monaco-list-row.focused:not(.string-label)>.contents>.main>.right>.details-label{display:inline}.monaco-editor .suggest-widget:not(.docs-side) .monaco-list .monaco-list-row:hover>.contents>.main>.right.can-expand-details>.details-label{width:calc(100% - 26px)}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.left{flex-shrink:1;flex-grow:1;overflow:hidden}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.left>.monaco-icon-label{flex-shrink:0}.monaco-editor .suggest-widget .monaco-list .monaco-list-row:not(.string-label)>.contents>.main>.left>.monaco-icon-label{max-width:100%}.monaco-editor .suggest-widget .monaco-list .monaco-list-row.string-label>.contents>.main>.left>.monaco-icon-label{flex-shrink:1}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right{overflow:hidden;flex-shrink:4;max-width:70%}.monaco-editor .suggest-widget .monaco-list .monaco-list-row>.contents>.main>.right>.readMore{display:inline-block;position:absolute;right:10px;width:18px;height:18px;visibility:hidden}.monaco-editor .suggest-widget.docs-side .monaco-list .monaco-list-row>.contents>.main>.right>.readMore{display:none!important}.monaco-editor .suggest-widget .monaco-list .monaco-list-row.string-label>.contents>.main>.right>.readMore{display:none}.monaco-editor .suggest-widget .monaco-list .monaco-list-row.focused.string-label>.contents>.main>.right>.readMore{display:inline-block}.monaco-editor .suggest-widget .monaco-list .monaco-list-row:hover>.contents>.main>.right>.readMore{visibility:visible}.monaco-editor .suggest-widget .monaco-list .monaco-list-row .monaco-icon-label.deprecated{opacity:.66;text-decoration:unset}.monaco-editor .suggest-widget .monaco-list .monaco-list-row .monaco-icon-label.deprecated>.monaco-icon-label-container>.monaco-icon-name-container{text-decoration:line-through}.monaco-editor .suggest-widget .monaco-list .monaco-list-row .monaco-icon-label::before{height:100%}.monaco-editor .suggest-widget .monaco-list .monaco-list-row .icon{display:block;height:16px;width:16px;margin-left:2px;background-repeat:no-repeat;background-size:80%;background-position:center}.monaco-editor .suggest-widget .monaco-list .monaco-list-row .icon.hide{display:none}.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon{display:flex;align-items:center;margin-right:4px}.monaco-editor .suggest-widget.no-icons .monaco-list .monaco-list-row .icon,.monaco-editor .suggest-widget.no-icons .monaco-list .monaco-list-row .suggest-icon::before{display:none}.monaco-editor .suggest-widget .monaco-list .monaco-list-row .icon.customcolor .colorspan{margin:0 0 0 .3em;border:.1em solid #000;width:.7em;height:.7em;display:inline-block}.monaco-editor .suggest-details-container{z-index:41}.monaco-editor .suggest-details{display:flex;flex-direction:column;cursor:default;color:var(--vscode-editorSuggestWidget-foreground)}.monaco-editor .suggest-details.focused{border-color:var(--vscode-focusBorder)}.monaco-editor .suggest-details a{color:var(--vscode-textLink-foreground)}.monaco-editor .suggest-details a:hover{color:var(--vscode-textLink-activeForeground)}.monaco-editor .suggest-details code{background-color:var(--vscode-textCodeBlock-background)}.monaco-editor .suggest-details.no-docs{display:none}.monaco-editor .suggest-details>.monaco-scrollable-element{flex:1}.monaco-editor .suggest-details>.monaco-scrollable-element>.body{box-sizing:border-box;height:100%;width:100%}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.header>.type{flex:2;overflow:hidden;text-overflow:ellipsis;opacity:.7;white-space:pre;margin:0 24px 0 0;padding:4px 0 12px 5px}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.header>.type.auto-wrap{white-space:normal;word-break:break-all}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs{margin:0;padding:4px 5px;white-space:pre-wrap}.monaco-editor .suggest-details.no-type>.monaco-scrollable-element>.body>.docs{margin-right:24px}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs.markdown-docs{padding:0;white-space:initial;min-height:calc(1rem + 8px)}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs.markdown-docs>div,.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs.markdown-docs>span:not(:empty){padding:4px 5px}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs.markdown-docs>div>p:first-child{margin-top:0}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs.markdown-docs>div>p:last-child{margin-bottom:0}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs.markdown-docs .monaco-tokenized-source{white-space:pre}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs .code{white-space:pre-wrap;word-wrap:break-word}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>.docs.markdown-docs .codicon{vertical-align:sub}.monaco-editor .suggest-details>.monaco-scrollable-element>.body>p:empty{display:none}.monaco-editor .suggest-details code{border-radius:3px;padding:0 .4em}.monaco-editor .suggest-details ul{padding-left:20px}.monaco-editor .suggest-details ol{padding-left:20px}.monaco-editor .suggest-details p code{font-family:var(--monaco-monospace-font)}.quick-input-widget{font-size:13px}.quick-input-widget .monaco-highlighted-label .highlight{color:#0066bf}.vs .quick-input-widget .monaco-list-row.focused .monaco-highlighted-label .highlight{color:#9dddff}.vs-dark .quick-input-widget .monaco-highlighted-label .highlight{color:#0097fb}.hc-black .quick-input-widget .monaco-highlighted-label .highlight{color:#f38518}.monaco-keybinding>.monaco-keybinding-key{background-color:rgba(221,221,221,.4);border:solid 1px rgba(204,204,204,.4);border-bottom-color:rgba(187,187,187,.4);box-shadow:inset 0 -1px 0 rgba(187,187,187,.4);color:#555}.hc-black .monaco-keybinding>.monaco-keybinding-key{background-color:transparent;border:solid 1px #6fc3df;box-shadow:none;color:#fff}.vs-dark .monaco-keybinding>.monaco-keybinding-key{background-color:rgba(128,128,128,.17);border:solid 1px rgba(51,51,51,.6);border-bottom-color:rgba(68,68,68,.6);box-shadow:inset 0 -1px 0 rgba(68,68,68,.6);color:#ccc}.monaco-editor .inputarea{min-width:0;min-height:0;margin:0;padding:0;position:absolute;outline:0!important;resize:none;border:none;overflow:hidden;color:transparent;background-color:transparent}.monaco-editor .inputarea.ime-input{z-index:10}.monaco-editor .view-overlays .current-line{display:block;position:absolute;left:0;top:0;box-sizing:border-box}.monaco-editor .margin-view-overlays .current-line{display:block;position:absolute;left:0;top:0;box-sizing:border-box}.monaco-editor .margin-view-overlays .current-line.current-line-margin.current-line-margin-both{border-right:0}.monaco-editor .lines-content .cdr{position:absolute}.monaco-editor .glyph-margin{position:absolute;top:0}.monaco-editor .margin-view-overlays .cgmr{position:absolute;display:flex;align-items:center;justify-content:center}.monaco-editor .lines-content .core-guide{position:absolute;box-sizing:border-box}.monaco-editor .margin-view-overlays .line-numbers{font-variant-numeric:tabular-nums;position:absolute;text-align:right;display:inline-block;vertical-align:middle;box-sizing:border-box;cursor:default;height:100%}.monaco-editor .relative-current-line-number{text-align:left;display:inline-block;width:100%}.monaco-editor .margin-view-overlays .line-numbers.lh-odd{margin-top:1px}.mtkcontrol{color:#fff!important;background:#960000!important}.monaco-editor.no-user-select .lines-content,.monaco-editor.no-user-select .view-line,.monaco-editor.no-user-select .view-lines{user-select:none;-webkit-user-select:none;-ms-user-select:none}.monaco-editor .view-lines{white-space:nowrap}.monaco-editor .view-line{position:absolute;width:100%}.monaco-editor .mtkz{display:inline-block}.monaco-editor .lines-decorations{position:absolute;top:0;background:#fff}.monaco-editor .margin-view-overlays .cldr{position:absolute;height:100%}.monaco-editor .margin-view-overlays .cmdr{position:absolute;left:0;width:100%;height:100%}.monaco-editor .minimap.slider-mouseover .minimap-slider{opacity:0;transition:opacity .1s linear}.monaco-editor .minimap.slider-mouseover:hover .minimap-slider{opacity:1}.monaco-editor .minimap.slider-mouseover .minimap-slider.active{opacity:1}.monaco-editor .minimap-shadow-hidden{position:absolute;width:0}.monaco-editor .minimap-shadow-visible{position:absolute;left:-6px;width:6px}.monaco-editor.no-minimap-shadow .minimap-shadow-visible{position:absolute;left:-1px;width:1px}.monaco-editor .overlayWidgets{position:absolute;top:0;left:0}.monaco-editor .view-ruler{position:absolute;top:0}.monaco-editor .scroll-decoration{position:absolute;top:0;left:0;height:6px}.monaco-editor .lines-content .cslr{position:absolute}.monaco-editor .top-left-radius{border-top-left-radius:3px}.monaco-editor .bottom-left-radius{border-bottom-left-radius:3px}.monaco-editor .top-right-radius{border-top-right-radius:3px}.monaco-editor .bottom-right-radius{border-bottom-right-radius:3px}.monaco-editor.hc-black .top-left-radius{border-top-left-radius:0}.monaco-editor.hc-black .bottom-left-radius{border-bottom-left-radius:0}.monaco-editor.hc-black .top-right-radius{border-top-right-radius:0}.monaco-editor.hc-black .bottom-right-radius{border-bottom-right-radius:0}.monaco-editor .cursors-layer{position:absolute;top:0}.monaco-editor .cursors-layer>.cursor{position:absolute;overflow:hidden}.monaco-editor .cursors-layer.cursor-smooth-caret-animation>.cursor{transition:all 80ms}.monaco-editor .cursors-layer.cursor-block-outline-style>.cursor{box-sizing:border-box;background:0 0!important;border-style:solid;border-width:1px}.monaco-editor .cursors-layer.cursor-underline-style>.cursor{border-bottom-width:2px;border-bottom-style:solid;background:0 0!important;box-sizing:border-box}.monaco-editor .cursors-layer.cursor-underline-thin-style>.cursor{border-bottom-width:1px;border-bottom-style:solid;background:0 0!important;box-sizing:border-box}@keyframes monaco-cursor-smooth{0%,20%{opacity:1}100%,60%{opacity:0}}@keyframes monaco-cursor-phase{0%,20%{opacity:1}100%,90%{opacity:0}}@keyframes monaco-cursor-expand{0%,20%{transform:scaleY(1)}100%,80%{transform:scaleY(0)}}.cursor-smooth{animation:monaco-cursor-smooth .5s ease-in-out 0s 20 alternate}.cursor-phase{animation:monaco-cursor-phase .5s ease-in-out 0s 20 alternate}.cursor-expand>.cursor{animation:monaco-cursor-expand .5s ease-in-out 0s 20 alternate}.monaco-action-bar{white-space:nowrap;height:100%}.monaco-action-bar .actions-container{display:flex;margin:0 auto;padding:0;height:100%;width:100%;align-items:center}.monaco-action-bar.vertical .actions-container{display:inline-block}.monaco-action-bar .action-item{display:block;align-items:center;justify-content:center;cursor:pointer;position:relative}.monaco-action-bar .action-item.disabled{cursor:default}.monaco-action-bar .action-item .codicon,.monaco-action-bar .action-item .icon{display:block}.monaco-action-bar .action-item .codicon{display:flex;align-items:center;width:16px;height:16px}.monaco-action-bar .action-label{font-size:11px;padding:3px;border-radius:5px}.monaco-action-bar .action-item.disabled .action-label,.monaco-action-bar .action-item.disabled .action-label::before,.monaco-action-bar .action-item.disabled .action-label:hover{opacity:.4}.monaco-action-bar.vertical{text-align:left}.monaco-action-bar.vertical .action-item{display:block}.monaco-action-bar.vertical .action-label.separator{display:block;border-bottom:1px solid #bbb;padding-top:1px;margin-left:.8em;margin-right:.8em}.monaco-action-bar .action-item .action-label.separator{width:1px;height:16px;margin:5px 4px!important;cursor:default;min-width:1px;padding:0;background-color:#bbb}.secondary-actions .monaco-action-bar .action-label{margin-left:6px}.monaco-action-bar .action-item.select-container{overflow:hidden;flex:1;max-width:170px;min-width:60px;display:flex;align-items:center;justify-content:center;margin-right:10px}.monaco-action-bar .action-item.action-dropdown-item{display:flex}.monaco-action-bar .action-item.action-dropdown-item>.action-label{margin-right:1px}.monaco-scrollable-element>.scrollbar>.scra{cursor:pointer;font-size:11px!important}.monaco-scrollable-element>.visible{opacity:1;background:rgba(0,0,0,0);transition:opacity .1s linear}.monaco-scrollable-element>.invisible{opacity:0;pointer-events:none}.monaco-scrollable-element>.invisible.fade{transition:opacity .8s linear}.monaco-scrollable-element>.shadow{position:absolute;display:none}.monaco-scrollable-element>.shadow.top{display:block;top:0;left:3px;height:3px;width:100%}.monaco-scrollable-element>.shadow.left{display:block;top:3px;left:0;height:100%;width:3px}.monaco-scrollable-element>.shadow.top-left-corner{display:block;top:0;left:0;height:3px;width:3px}.monaco-editor .zone-widget .zone-widget-container.reference-zone-widget{border-top-width:1px;border-bottom-width:1px}.monaco-editor .reference-zone-widget .inline{display:inline-block;vertical-align:top}.monaco-editor .reference-zone-widget .messages{height:100%;width:100%;text-align:center;padding:3em 0}.monaco-editor .reference-zone-widget .ref-tree{line-height:23px;background-color:var(--vscode-peekViewResult-background);color:var(--vscode-peekViewResult-lineForeground)}.monaco-editor .reference-zone-widget .ref-tree .reference{text-overflow:ellipsis;overflow:hidden}.monaco-editor .reference-zone-widget .ref-tree .reference-file{display:inline-flex;width:100%;height:100%;color:var(--vscode-peekViewResult-fileForeground)}.monaco-editor .reference-zone-widget .ref-tree .monaco-list:focus .selected .reference-file{color:inherit!important}.monaco-editor .reference-zone-widget .ref-tree .monaco-list:focus .monaco-list-rows>.monaco-list-row.selected:not(.highlighted){background-color:var(--vscode-peekViewResult-selectionBackground);color:var(--vscode-peekViewResult-selectionForeground)!important}.monaco-editor .reference-zone-widget .ref-tree .reference-file .count{margin-right:12px;margin-left:auto}.monaco-editor .reference-zone-widget .ref-tree .referenceMatch .highlight{background-color:var(--vscode-peekViewResult-matchHighlightBackground)}.monaco-editor .reference-zone-widget .preview .reference-decoration{background-color:var(--vscode-peekViewEditor-matchHighlightBackground);border:2px solid var(--vscode-peekViewEditor-matchHighlightBorder);box-sizing:border-box}.monaco-editor .reference-zone-widget .preview .monaco-editor .inputarea.ime-input,.monaco-editor .reference-zone-widget .preview .monaco-editor .monaco-editor-background{background-color:var(--vscode-peekViewEditor-background)}.monaco-editor .reference-zone-widget .preview .monaco-editor .margin{background-color:var(--vscode-peekViewEditorGutter-background)}.monaco-editor.hc-black .reference-zone-widget .ref-tree .reference-file{font-weight:700}.monaco-editor.hc-black .reference-zone-widget .ref-tree .referenceMatch .highlight{border:1px dotted var(--vscode-contrastActiveBorder,transparent);box-sizing:border-box}.monaco-editor .zone-widget{position:absolute;z-index:10}.monaco-editor .zone-widget .zone-widget-container{border-top-style:solid;border-bottom-style:solid;border-top-width:0;border-bottom-width:0;position:relative}.monaco-action-bar .action-item.menu-entry .action-label.icon{width:16px;height:16px;background-repeat:no-repeat;background-position:50%;background-size:16px}.monaco-action-bar .action-item.menu-entry .action-label{background-image:var(--menu-entry-icon-light)}.hc-black .monaco-action-bar .action-item.menu-entry .action-label,.vs-dark .monaco-action-bar .action-item.menu-entry .action-label{background-image:var(--menu-entry-icon-dark)}.monaco-dropdown-with-default{display:flex!important;flex-direction:row;border-radius:5px}.monaco-dropdown-with-default>.action-container>.action-label{margin-right:0}.monaco-dropdown-with-default>.action-container.menu-entry>.action-label.icon{width:16px;height:16px;background-repeat:no-repeat;background-position:50%;background-size:16px}.monaco-dropdown-with-default>.action-container.menu-entry>.action-label{background-image:var(--menu-entry-icon-light)}.hc-black .monaco-dropdown-with-default>.action-container.menu-entry>.action-label,.vs-dark .monaco-dropdown-with-default>.action-container.menu-entry>.action-label{background-image:var(--menu-entry-icon-dark)}.monaco-dropdown-with-default>.dropdown-action-container>.monaco-dropdown>.dropdown-label .codicon[class*=codicon-]{font-size:12px;padding-left:0;padding-right:0;line-height:16px;margin-left:-3px}.monaco-dropdown-with-default>.dropdown-action-container>.monaco-dropdown>.dropdown-label>.action-label{display:block;background-size:16px;background-position:center center;background-repeat:no-repeat}.monaco-hover{cursor:default;position:absolute;overflow:hidden;z-index:50;user-select:text;-webkit-user-select:text;-ms-user-select:text;box-sizing:initial;animation:fadein .1s linear;line-height:1.5em}.monaco-hover.hidden{display:none}.monaco-hover .hover-contents:not(.html-hover-contents){padding:4px 8px}.monaco-hover .markdown-hover>.hover-contents:not(.code-hover-contents){max-width:500px;word-wrap:break-word}.monaco-hover .markdown-hover>.hover-contents:not(.code-hover-contents) hr{min-width:100%}.monaco-hover .code,.monaco-hover p,.monaco-hover ul{margin:8px 0}.monaco-hover code{font-family:var(--monaco-monospace-font)}.monaco-hover hr{box-sizing:border-box;border-left:0;border-right:0;margin-top:4px;margin-bottom:-4px;margin-left:-8px;margin-right:-8px;height:1px}.monaco-hover .code:first-child,.monaco-hover p:first-child,.monaco-hover ul:first-child{margin-top:0}.monaco-hover .code:last-child,.monaco-hover p:last-child,.monaco-hover ul:last-child{margin-bottom:0}.monaco-hover ul{padding-left:20px}.monaco-hover ol{padding-left:20px}.monaco-hover li>p{margin-bottom:0}.monaco-hover li>ul{margin-top:0}.monaco-hover code{border-radius:3px;padding:0 .4em}.monaco-hover .monaco-tokenized-source{white-space:pre-wrap}.monaco-hover .hover-row.status-bar{font-size:12px;line-height:22px}.monaco-hover .hover-row.status-bar .actions{display:flex;padding:0 8px}.monaco-hover .hover-row.status-bar .actions .action-container{margin-right:16px;cursor:pointer}.monaco-hover .hover-row.status-bar .actions .action-container .action .icon{padding-right:4px}.monaco-hover .markdown-hover .hover-contents .codicon{color:inherit;font-size:inherit;vertical-align:middle}.monaco-hover .hover-contents a.code-link,.monaco-hover .hover-contents a.code-link:hover{color:inherit}.monaco-hover .hover-contents a.code-link:before{content:'('}.monaco-hover .hover-contents a.code-link:after{content:')'}.monaco-hover .hover-contents a.code-link>span{text-decoration:underline;border-bottom:1px solid transparent;text-underline-position:under}.monaco-hover .markdown-hover .hover-contents:not(.code-hover-contents):not(.html-hover-contents) span{margin-bottom:4px;display:inline-block}.monaco-hover-content .action-container a{-webkit-user-select:none;user-select:none}.monaco-hover-content .action-container.disabled{pointer-events:none;opacity:.4;cursor:default}.monaco-editor .unicode-highlight{border:1px solid var(--vscode-editorUnicodeHighlight-border);box-sizing:border-box}@font-face{font-family:codicon;font-display:block;src:url(codicon.ttf) format("truetype")}.codicon[class*=codicon-]{font:normal normal normal 16px/1 codicon;display:inline-block;text-decoration:none;text-rendering:auto;text-align:center;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;user-select:none;-webkit-user-select:none;-ms-user-select:none}.codicon-wrench-subaction{opacity:.5}@keyframes codicon-spin{100%{transform:rotate(360deg)}}.codicon-gear.codicon-modifier-spin,.codicon-loading.codicon-modifier-spin,.codicon-notebook-state-executing.codicon-modifier-spin,.codicon-sync.codicon-modifier-spin{animation:codicon-spin 1.5s steps(30) infinite}.codicon-modifier-disabled{opacity:.4}.codicon-loading,.codicon-tree-item-loading::before{animation-duration:1s!important;animation-timing-function:cubic-bezier(.53,.21,.29,.67)!important}.monaco-list{position:relative;height:100%;width:100%;white-space:nowrap}.monaco-list.mouse-support{user-select:none;-webkit-user-select:none;-ms-user-select:none}.monaco-list>.monaco-scrollable-element{height:100%}.monaco-list-rows{position:relative;width:100%;height:100%}.monaco-list.horizontal-scrolling .monaco-list-rows{width:auto;min-width:100%}.monaco-list-row{position:absolute;box-sizing:border-box;overflow:hidden;width:100%}.monaco-list.mouse-support .monaco-list-row{cursor:pointer;touch-action:none}.monaco-list-row.scrolling{display:none!important}.monaco-list.element-focused,.monaco-list.selection-multiple,.monaco-list.selection-single{outline:0!important}.monaco-drag-image{display:inline-block;padding:1px 7px;border-radius:10px;font-size:12px;position:absolute;z-index:1000}.monaco-list-type-filter{display:flex;align-items:center;position:absolute;border-radius:2px;padding:0 3px;max-width:calc(100% - 10px);text-overflow:ellipsis;overflow:hidden;text-align:right;box-sizing:border-box;cursor:all-scroll;font-size:13px;line-height:18px;height:20px;z-index:1;top:4px}.monaco-list-type-filter.dragging{transition:top .2s,left .2s}.monaco-list-type-filter.ne{right:4px}.monaco-list-type-filter.nw{left:4px}.monaco-list-type-filter>.controls{display:flex;align-items:center;box-sizing:border-box;transition:width .2s;width:0}.monaco-list-type-filter.dragging>.controls,.monaco-list-type-filter:hover>.controls{width:36px}.monaco-list-type-filter>.controls>*{border:none;box-sizing:border-box;-webkit-appearance:none;-moz-appearance:none;background:0 0;width:16px;height:16px;flex-shrink:0;margin:0;padding:0;display:flex;align-items:center;justify-content:center;cursor:pointer}.monaco-list-type-filter>.controls>.filter{margin-left:4px}.monaco-list-type-filter-message{position:absolute;box-sizing:border-box;width:100%;height:100%;top:0;left:0;padding:40px 1em 1em 1em;text-align:center;white-space:normal;opacity:.7;pointer-events:none}.monaco-list-type-filter-message:empty{display:none}.monaco-list-type-filter{cursor:grab}.monaco-list-type-filter.dragging{cursor:grabbing}.context-view .monaco-menu{min-width:130px}.context-view{position:absolute;z-index:2500}.context-view.fixed{all:initial;font-family:inherit;font-size:13px;position:fixed;z-index:2500;color:inherit}.monaco-table{display:flex;flex-direction:column;position:relative;height:100%;width:100%;white-space:nowrap}.monaco-table>.monaco-split-view2{border-bottom:1px solid transparent}.monaco-table>.monaco-list{flex:1}.monaco-table-tr{display:flex;height:100%}.monaco-table-th{width:100%;height:100%;font-weight:700;overflow:hidden;text-overflow:ellipsis}.monaco-table-td,.monaco-table-th{box-sizing:border-box;flex-shrink:0;overflow:hidden;white-space:nowrap;text-overflow:ellipsis}.monaco-table>.monaco-split-view2 .monaco-sash.vertical::before{content:"";position:absolute;left:calc(var(--sash-size)/ 2);width:0;border-left:1px solid transparent}.monaco-table>.monaco-split-view2,.monaco-table>.monaco-split-view2 .monaco-sash.vertical::before{transition:border-color .2s ease-out}.monaco-editor .contentWidgets .codicon-light-bulb,.monaco-editor .contentWidgets .codicon-lightbulb-autofix{display:flex;align-items:center;justify-content:center}.monaco-editor .contentWidgets .codicon-light-bulb:hover,.monaco-editor .contentWidgets .codicon-lightbulb-autofix:hover{cursor:pointer}.monaco-split-view2{position:relative;width:100%;height:100%}.monaco-split-view2>.sash-container{position:absolute;width:100%;height:100%;pointer-events:none}.monaco-split-view2>.sash-container>.monaco-sash{pointer-events:initial}.monaco-split-view2>.monaco-scrollable-element{width:100%;height:100%}.monaco-split-view2>.monaco-scrollable-element>.split-view-container{width:100%;height:100%;white-space:nowrap;position:relative}.monaco-split-view2>.monaco-scrollable-element>.split-view-container>.split-view-view{white-space:initial;position:absolute}.monaco-split-view2>.monaco-scrollable-element>.split-view-container>.split-view-view:not(.visible){display:none}.monaco-split-view2.vertical>.monaco-scrollable-element>.split-view-container>.split-view-view{width:100%}.monaco-split-view2.horizontal>.monaco-scrollable-element>.split-view-container>.split-view-view{height:100%}.monaco-split-view2.separator-border>.monaco-scrollable-element>.split-view-container>.split-view-view:not(:first-child)::before{content:' ';position:absolute;top:0;left:0;z-index:5;pointer-events:none;background-color:var(--separator-border)}.monaco-split-view2.separator-border.horizontal>.monaco-scrollable-element>.split-view-container>.split-view-view:not(:first-child)::before{height:100%;width:1px}.monaco-split-view2.separator-border.vertical>.monaco-scrollable-element>.split-view-container>.split-view-view:not(:first-child)::before{height:1px;width:100%}.monaco-dropdown{height:100%;padding:0}.monaco-dropdown>.dropdown-label{cursor:pointer;height:100%;display:flex;align-items:center;justify-content:center}.monaco-dropdown>.dropdown-label>.action-label.disabled{cursor:default}.monaco-dropdown-with-primary{display:flex!important;flex-direction:row;border-radius:5px}.monaco-dropdown-with-primary>.action-container>.action-label{margin-right:0}.monaco-dropdown-with-primary>.dropdown-action-container>.monaco-dropdown>.dropdown-label .codicon[class*=codicon-]{font-size:12px;padding-left:0;padding-right:0;line-height:16px;margin-left:-3px}.monaco-dropdown-with-primary>.dropdown-action-container>.monaco-dropdown>.dropdown-label>.action-label{display:block;background-size:16px;background-position:center center;background-repeat:no-repeat}.monaco-resizable-element>.resizer{cursor:nwse-resize;width:30px;height:30px;position:absolute;right:-15px;bottom:-15px;z-index:20}.colorpicker-widget{height:190px;user-select:none;-webkit-user-select:none;-ms-user-select:none}.monaco-editor .colorpicker-hover:focus{outline:0}.colorpicker-color-decoration{border:solid .1em #000;box-sizing:border-box;margin:.1em .2em 0 .2em;width:.8em;height:.8em;line-height:.8em;display:inline-block}.hc-black .colorpicker-color-decoration,.vs-dark .colorpicker-color-decoration{border:solid .1em #eee}.colorpicker-header{display:flex;height:24px;position:relative;background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAQAAAAECAYAAACp8Z5+AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAZdEVYdFNvZnR3YXJlAHBhaW50Lm5ldCA0LjAuMTZEaa/1AAAAHUlEQVQYV2PYvXu3JAi7uLiAMaYAjAGTQBPYLQkAa/0Zef3qRswAAAAASUVORK5CYII=);background-size:9px 9px;image-rendering:pixelated}.colorpicker-header .picked-color{width:216px;display:flex;align-items:center;justify-content:center;line-height:24px;cursor:pointer;color:#fff;flex:1}.colorpicker-header .picked-color .codicon{color:inherit;font-size:14px;position:absolute;left:8px}.colorpicker-header .picked-color.light{color:#000}.colorpicker-header .original-color{width:74px;z-index:inherit;cursor:pointer}.colorpicker-body{display:flex;padding:8px;position:relative}.colorpicker-body .saturation-wrap{overflow:hidden;height:150px;position:relative;min-width:220px;flex:1}.colorpicker-body .saturation-box{height:150px;position:absolute}.colorpicker-body .saturation-selection{width:9px;height:9px;margin:-5px 0 0 -5px;border:1px solid #fff;border-radius:100%;box-shadow:0 0 2px rgba(0,0,0,.8);position:absolute}.colorpicker-body .strip{width:25px;height:150px}.colorpicker-body .hue-strip{position:relative;margin-left:8px;cursor:grab;background:linear-gradient(to bottom,red 0,#ff0 17%,#0f0 33%,#0ff 50%,#00f 67%,#f0f 83%,red 100%)}.colorpicker-body .opacity-strip{position:relative;margin-left:8px;cursor:grab;background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAQAAAAECAYAAACp8Z5+AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAZdEVYdFNvZnR3YXJlAHBhaW50Lm5ldCA0LjAuMTZEaa/1AAAAHUlEQVQYV2PYvXu3JAi7uLiAMaYAjAGTQBPYLQkAa/0Zef3qRswAAAAASUVORK5CYII=);background-size:9px 9px;image-rendering:pixelated}.colorpicker-body .strip.grabbing{cursor:grabbing}.colorpicker-body .slider{position:absolute;top:0;left:-2px;width:calc(100% + 4px);height:4px;box-sizing:border-box;border:1px solid rgba(255,255,255,.71);box-shadow:0 0 1px rgba(0,0,0,.85)}.colorpicker-body .strip .overlay{height:150px;pointer-events:none}.editor-banner{box-sizing:border-box;cursor:default;width:100%;font-size:12px;display:flex;overflow:visible;height:26px;background:var(--vscode-banner-background)}.editor-banner .icon-container{display:flex;flex-shrink:0;align-items:center;padding:0 6px 0 10px}.editor-banner .icon-container.custom-icon{background-repeat:no-repeat;background-position:center center;background-size:16px;width:16px;padding:0;margin:0 6px 0 10px}.editor-banner .message-container{display:flex;align-items:center;line-height:26px;text-overflow:ellipsis;white-space:nowrap;overflow:hidden}.editor-banner .message-container p{margin-block-start:0;margin-block-end:0}.editor-banner .message-actions-container{flex-grow:1;flex-shrink:0;line-height:26px;margin:0 4px}.editor-banner .message-actions-container a.monaco-button{width:inherit;margin:2px 8px;padding:0 12px}.editor-banner .message-actions-container a{padding:3px;margin-left:12px;text-decoration:underline}.editor-banner .action-container{padding:0 10px 0 6px}.editor-banner{background-color:var(--vscode-banner-background)}.editor-banner,.editor-banner .action-container .codicon,.editor-banner .message-actions-container .monaco-link{color:var(--vscode-banner-foreground)}.editor-banner .icon-container .codicon{color:var(--vscode-banner-iconForeground)}.monaco-icon-label{display:flex;overflow:hidden;text-overflow:ellipsis}.monaco-icon-label::before{background-size:16px;background-position:left center;background-repeat:no-repeat;padding-right:6px;width:16px;height:22px;line-height:inherit!important;display:inline-block;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;vertical-align:top;flex-shrink:0}.monaco-icon-label>.monaco-icon-label-container{min-width:0;overflow:hidden;text-overflow:ellipsis;flex:1}.monaco-icon-label>.monaco-icon-label-container>.monaco-icon-name-container>.label-name{color:inherit;white-space:pre}.monaco-icon-label>.monaco-icon-label-container>.monaco-icon-name-container>.label-name>.label-separator{margin:0 2px;opacity:.5}.monaco-icon-label>.monaco-icon-label-container>.monaco-icon-description-container>.label-description{opacity:.7;margin-left:.5em;font-size:.9em;white-space:pre}.monaco-icon-label.nowrap>.monaco-icon-label-container>.monaco-icon-description-container>.label-description{white-space:nowrap}.vs .monaco-icon-label>.monaco-icon-label-container>.monaco-icon-description-container>.label-description{opacity:.95}.monaco-icon-label.italic>.monaco-icon-label-container>.monaco-icon-description-container>.label-description,.monaco-icon-label.italic>.monaco-icon-label-container>.monaco-icon-name-container>.label-name{font-style:italic}.monaco-icon-label.deprecated{text-decoration:line-through;opacity:.66}.monaco-icon-label.italic::after{font-style:italic}.monaco-icon-label.strikethrough>.monaco-icon-label-container>.monaco-icon-description-container>.label-description,.monaco-icon-label.strikethrough>.monaco-icon-label-container>.monaco-icon-name-container>.label-name{text-decoration:line-through}.monaco-icon-label::after{opacity:.75;font-size:90%;font-weight:600;margin:auto 16px 0 5px;text-align:center}.monaco-list:focus .selected .monaco-icon-label,.monaco-list:focus .selected .monaco-icon-label::after{color:inherit!important}.monaco-list-row.focused.selected .label-description,.monaco-list-row.selected .label-description{opacity:.8}.monaco-editor{font-family:-apple-system,BlinkMacSystemFont,"Segoe WPC","Segoe UI",HelveticaNeue-Light,system-ui,Ubuntu,"Droid Sans",sans-serif;--monaco-monospace-font:"SF Mono",Monaco,Menlo,Consolas,"Ubuntu Mono","Liberation Mono","DejaVu Sans Mono","Courier New",monospace}.monaco-menu .monaco-action-bar.vertical .action-item .action-menu-item:focus .action-label{stroke-width:1.2px}.monaco-editor.hc-black .monaco-menu .monaco-action-bar.vertical .action-menu-item:focus .action-label,.monaco-editor.vs-dark .monaco-menu .monaco-action-bar.vertical .action-menu-item:focus .action-label{stroke-width:1.2px}.monaco-hover p{margin:0}.monaco-aria-container{position:absolute!important;top:0;height:1px;width:1px;margin:-1px;overflow:hidden;padding:0;clip:rect(1px,1px,1px,1px);clip-path:inset(50%)}.monaco-editor.hc-black{-ms-high-contrast-adjust:none}@media screen and (-ms-high-contrast:active){.monaco-editor.vs .view-overlays .current-line,.monaco-editor.vs-dark .view-overlays .current-line{border-color:windowtext!important;border-left:0;border-right:0}.monaco-editor.vs .cursor,.monaco-editor.vs-dark .cursor{background-color:windowtext!important}.monaco-editor.vs .dnd-target,.monaco-editor.vs-dark .dnd-target{border-color:windowtext!important}.monaco-editor.vs .selected-text,.monaco-editor.vs-dark .selected-text{background-color:highlight!important}.monaco-editor.vs .view-line,.monaco-editor.vs-dark .view-line{-ms-high-contrast-adjust:none}.monaco-editor.vs .view-line span,.monaco-editor.vs-dark .view-line span{color:windowtext!important}.monaco-editor.vs .view-line span.inline-selected-text,.monaco-editor.vs-dark .view-line span.inline-selected-text{color:highlighttext!important}.monaco-editor.vs .view-overlays,.monaco-editor.vs-dark .view-overlays{-ms-high-contrast-adjust:none}.monaco-editor.vs .reference-decoration,.monaco-editor.vs .selectionHighlight,.monaco-editor.vs .wordHighlight,.monaco-editor.vs .wordHighlightStrong,.monaco-editor.vs-dark .reference-decoration,.monaco-editor.vs-dark .selectionHighlight,.monaco-editor.vs-dark .wordHighlight,.monaco-editor.vs-dark .wordHighlightStrong{border:2px dotted highlight!important;background:0 0!important;box-sizing:border-box}.monaco-editor.vs .rangeHighlight,.monaco-editor.vs-dark .rangeHighlight{background:0 0!important;border:1px dotted activeborder!important;box-sizing:border-box}.monaco-editor.vs .bracket-match,.monaco-editor.vs-dark .bracket-match{border-color:windowtext!important;background:0 0!important}.monaco-editor.vs .currentFindMatch,.monaco-editor.vs .findMatch,.monaco-editor.vs-dark .currentFindMatch,.monaco-editor.vs-dark .findMatch{border:2px dotted activeborder!important;background:0 0!important;box-sizing:border-box}.monaco-editor.vs .find-widget,.monaco-editor.vs-dark .find-widget{border:1px solid windowtext}.monaco-editor.vs .monaco-list .monaco-list-row,.monaco-editor.vs-dark .monaco-list .monaco-list-row{-ms-high-contrast-adjust:none;color:windowtext!important}.monaco-editor.vs .monaco-list .monaco-list-row.focused,.monaco-editor.vs-dark .monaco-list .monaco-list-row.focused{color:highlighttext!important;background-color:highlight!important}.monaco-editor.vs .monaco-list .monaco-list-row:hover,.monaco-editor.vs-dark .monaco-list .monaco-list-row:hover{background:0 0!important;border:1px solid highlight;box-sizing:border-box}.monaco-editor.vs .monaco-scrollable-element>.scrollbar,.monaco-editor.vs-dark .monaco-scrollable-element>.scrollbar{-ms-high-contrast-adjust:none;background:background!important;border:1px solid windowtext;box-sizing:border-box}.monaco-editor.vs .monaco-scrollable-element>.scrollbar>.slider,.monaco-editor.vs-dark .monaco-scrollable-element>.scrollbar>.slider{background:windowtext!important}.monaco-editor.vs .monaco-scrollable-element>.scrollbar>.slider:hover,.monaco-editor.vs-dark .monaco-scrollable-element>.scrollbar>.slider:hover{background:highlight!important}.monaco-editor.vs .monaco-scrollable-element>.scrollbar>.slider.active,.monaco-editor.vs-dark .monaco-scrollable-element>.scrollbar>.slider.active{background:highlight!important}.monaco-editor.vs .decorationsOverviewRuler,.monaco-editor.vs-dark .decorationsOverviewRuler{opacity:0}.monaco-editor.vs .minimap,.monaco-editor.vs-dark .minimap{display:none}.monaco-editor.vs .squiggly-d-error,.monaco-editor.vs-dark .squiggly-d-error{background:0 0!important;border-bottom:4px double #e47777}.monaco-editor.vs .squiggly-c-warning,.monaco-editor.vs-dark .squiggly-c-warning{border-bottom:4px double #71b771}.monaco-editor.vs .squiggly-b-info,.monaco-editor.vs-dark .squiggly-b-info{border-bottom:4px double #71b771}.monaco-editor.vs .squiggly-a-hint,.monaco-editor.vs-dark .squiggly-a-hint{border-bottom:4px double #6c6c6c}.monaco-editor.vs .monaco-menu .monaco-action-bar.vertical .action-menu-item:focus .action-label,.monaco-editor.vs-dark .monaco-menu .monaco-action-bar.vertical .action-menu-item:focus .action-label{-ms-high-contrast-adjust:none;color:highlighttext!important;background-color:highlight!important}.monaco-editor.vs .monaco-menu .monaco-action-bar.vertical .action-menu-item:hover .action-label,.monaco-editor.vs-dark .monaco-menu .monaco-action-bar.vertical .action-menu-item:hover .action-label{-ms-high-contrast-adjust:none;background:0 0!important;border:1px solid highlight;box-sizing:border-box}.monaco-diff-editor.vs .diffOverviewRuler,.monaco-diff-editor.vs-dark .diffOverviewRuler{display:none}.monaco-editor.vs .line-delete,.monaco-editor.vs .line-insert,.monaco-editor.vs-dark .line-delete,.monaco-editor.vs-dark .line-insert{background:0 0!important;border:1px solid highlight!important;box-sizing:border-box}.monaco-editor.vs .char-delete,.monaco-editor.vs .char-insert,.monaco-editor.vs-dark .char-delete,.monaco-editor.vs-dark .char-insert{background:0 0!important}}.monaco-tl-row{display:flex;height:100%;align-items:center;position:relative}.monaco-tl-indent{height:100%;position:absolute;top:0;left:16px;pointer-events:none}.hide-arrows .monaco-tl-indent{left:12px}.monaco-tl-indent>.indent-guide{display:inline-block;box-sizing:border-box;height:100%;border-left:1px solid transparent}.monaco-tl-indent>.indent-guide{transition:border-color .1s linear}.monaco-tl-contents,.monaco-tl-twistie{height:100%}.monaco-tl-twistie{font-size:10px;text-align:right;padding-right:6px;flex-shrink:0;width:16px;display:flex!important;align-items:center;justify-content:center;transform:translateX(3px)}.monaco-tl-contents{flex:1;overflow:hidden}.monaco-tl-twistie::before{border-radius:20px}.monaco-tl-twistie.collapsed::before{transform:rotate(-90deg)}.monaco-tl-twistie.codicon-tree-item-loading::before{animation:codicon-spin 1.25s steps(30) infinite}.quick-input-widget{position:absolute;width:600px;z-index:2000;padding:0 1px 1px 1px;left:50%;margin-left:-300px}.quick-input-titlebar{display:flex;align-items:center}.quick-input-left-action-bar{display:flex;margin-left:4px;flex:1}.quick-input-title{padding:3px 0;text-align:center;text-overflow:ellipsis;overflow:hidden}.quick-input-right-action-bar{display:flex;margin-right:4px;flex:1}.quick-input-right-action-bar>.actions-container{justify-content:flex-end}.quick-input-titlebar .monaco-action-bar .action-label.codicon{background-position:center;background-repeat:no-repeat;padding:2px}.quick-input-description{margin:6px}.quick-input-header .quick-input-description{margin:4px 2px}.quick-input-header{display:flex;padding:6px 6px 0 6px;margin-bottom:-2px}.quick-input-widget.hidden-input .quick-input-header{padding:0;margin-bottom:0}.quick-input-and-message{display:flex;flex-direction:column;flex-grow:1;min-width:0;position:relative}.quick-input-check-all{align-self:center;margin:0}.quick-input-filter{flex-grow:1;display:flex;position:relative}.quick-input-box{flex-grow:1}.quick-input-widget.show-checkboxes .quick-input-box,.quick-input-widget.show-checkboxes .quick-input-message{margin-left:5px}.quick-input-visible-count{position:absolute;left:-10000px}.quick-input-count{align-self:center;position:absolute;right:4px;display:flex;align-items:center}.quick-input-count .monaco-count-badge{vertical-align:middle;padding:2px 4px;border-radius:2px;min-height:auto;line-height:normal}.quick-input-action{margin-left:6px}.quick-input-action .monaco-text-button{font-size:11px;padding:0 6px;display:flex;height:27.5px;align-items:center}.quick-input-message{margin-top:-1px;padding:5px 5px 2px 5px;overflow-wrap:break-word}.quick-input-message>.codicon{margin:0 .2em;vertical-align:text-bottom}.quick-input-progress.monaco-progress-container{position:relative}.quick-input-progress.monaco-progress-container,.quick-input-progress.monaco-progress-container .progress-bit{height:2px}.quick-input-list{line-height:22px;margin-top:6px}.quick-input-widget.hidden-input .quick-input-list{margin-top:0}.quick-input-list .monaco-list{overflow:hidden;max-height:calc(20 * 22px)}.quick-input-list .quick-input-list-entry{box-sizing:border-box;overflow:hidden;display:flex;height:100%;padding:0 6px}.quick-input-list .quick-input-list-entry.quick-input-list-separator-border{border-top-width:1px;border-top-style:solid}.quick-input-list .monaco-list-row[data-index="0"] .quick-input-list-entry.quick-input-list-separator-border{border-top-style:none}.quick-input-list .quick-input-list-label{overflow:hidden;display:flex;height:100%;flex:1}.quick-input-list .quick-input-list-checkbox{align-self:center;margin:0}.quick-input-list .quick-input-list-rows{overflow:hidden;text-overflow:ellipsis;display:flex;flex-direction:column;height:100%;flex:1;margin-left:5px}.quick-input-widget.show-checkboxes .quick-input-list .quick-input-list-rows{margin-left:10px}.quick-input-widget .quick-input-list .quick-input-list-checkbox{display:none}.quick-input-widget.show-checkboxes .quick-input-list .quick-input-list-checkbox{display:inline}.quick-input-list .quick-input-list-rows>.quick-input-list-row{display:flex;align-items:center}.quick-input-list .quick-input-list-rows>.quick-input-list-row .monaco-icon-label,.quick-input-list .quick-input-list-rows>.quick-input-list-row .monaco-icon-label .monaco-icon-label-container>.monaco-icon-name-container{flex:1}.quick-input-list .quick-input-list-rows>.quick-input-list-row .codicon[class*=codicon-]{vertical-align:text-bottom}.quick-input-list .quick-input-list-rows .monaco-highlighted-label span{opacity:1}.quick-input-list .quick-input-list-entry .quick-input-list-entry-keybinding{margin-right:8px}.quick-input-list .quick-input-list-label-meta{opacity:.7;line-height:normal;text-overflow:ellipsis;overflow:hidden}.quick-input-list .monaco-highlighted-label .highlight{font-weight:700}.quick-input-list .quick-input-list-entry .quick-input-list-separator{margin-right:8px}.quick-input-list .quick-input-list-entry-action-bar{display:flex;flex:0;overflow:visible}.quick-input-list .quick-input-list-entry-action-bar .action-label{display:none}.quick-input-list .quick-input-list-entry-action-bar .action-label.codicon{margin-right:4px;padding:0 2px 2px 2px}.quick-input-list .quick-input-list-entry-action-bar{margin-top:1px}.quick-input-list .quick-input-list-entry-action-bar{margin-right:4px}.quick-input-list .monaco-list-row.focused .quick-input-list-entry-action-bar .action-label,.quick-input-list .quick-input-list-entry .quick-input-list-entry-action-bar .action-label.always-visible,.quick-input-list .quick-input-list-entry:hover .quick-input-list-entry-action-bar .action-label{display:flex}.quick-input-list .monaco-list-row.focused .monaco-keybinding-key,.quick-input-list .monaco-list-row.focused .quick-input-list-entry .quick-input-list-separator{color:inherit}.quick-input-list .monaco-list-row.focused .monaco-keybinding-key{background:0 0}.monaco-count-badge{padding:3px 6px;border-radius:11px;font-size:11px;min-width:18px;min-height:18px;line-height:11px;font-weight:400;text-align:center;display:inline-block;box-sizing:border-box}.monaco-count-badge.long{padding:2px 3px;border-radius:2px;min-height:auto;line-height:normal}.monaco-editor .peekview-widget .head .peekview-title .severity-icon{display:inline-block;vertical-align:text-top;margin-right:4px}.monaco-editor .marker-widget{text-overflow:ellipsis;white-space:nowrap}.monaco-editor .marker-widget>.stale{opacity:.6;font-style:italic}.monaco-editor .marker-widget .title{display:inline-block;padding-right:5px}.monaco-editor .marker-widget .descriptioncontainer{position:absolute;white-space:pre;user-select:text;-webkit-user-select:text;-ms-user-select:text;padding:8px 12px 0 20px}.monaco-editor .marker-widget .descriptioncontainer .message{display:flex;flex-direction:column}.monaco-editor .marker-widget .descriptioncontainer .message .details{padding-left:6px}.monaco-editor .marker-widget .descriptioncontainer .message .source,.monaco-editor .marker-widget .descriptioncontainer .message span.code{opacity:.6}.monaco-editor .marker-widget .descriptioncontainer .message a.code-link{opacity:.6;color:inherit}.monaco-editor .marker-widget .descriptioncontainer .message a.code-link:before{content:'('}.monaco-editor .marker-widget .descriptioncontainer .message a.code-link:after{content:')'}.monaco-editor .marker-widget .descriptioncontainer .message a.code-link>span{text-decoration:underline;border-bottom:1px solid transparent;text-underline-position:under;color:var(--vscode-textLink-foreground)}.monaco-editor .marker-widget .descriptioncontainer .message a.code-link>span{color:var(--vscode-textLink-activeForeground)}.monaco-editor .marker-widget .descriptioncontainer .filename{cursor:pointer}.monaco-editor .suggest-preview-additional-widget{white-space:nowrap}.monaco-editor .suggest-preview-additional-widget .content-spacer{color:transparent;white-space:pre}.monaco-editor .suggest-preview-additional-widget .button{display:inline-block;cursor:pointer;text-decoration:underline;text-underline-position:under}.monaco-editor .ghost-text-hidden{opacity:0;font-size:0}.monaco-editor .ghost-text-decoration{font-style:italic}.monaco-editor .suggest-preview-text{font-style:italic}.monaco-text-button{box-sizing:border-box;display:flex;width:100%;padding:4px;text-align:center;cursor:pointer;justify-content:center;align-items:center}.monaco-text-button:focus{outline-offset:2px!important}.monaco-text-button:hover{text-decoration:none!important}.monaco-button.disabled,.monaco-button.disabled:focus{opacity:.4!important;cursor:default}.monaco-text-button>.codicon{margin:0 .2em;color:inherit!important}.monaco-button-dropdown{display:flex;cursor:pointer}.monaco-button-dropdown>.monaco-dropdown-button{margin-left:1px}.monaco-description-button{flex-direction:column}.monaco-description-button .monaco-button-label{font-weight:500}.monaco-description-button .monaco-button-description{font-style:italic}.monaco-progress-container{width:100%;height:5px;overflow:hidden}.monaco-progress-container .progress-bit{width:2%;height:5px;position:absolute;left:0;display:none}.monaco-progress-container.active .progress-bit{display:inherit}.monaco-progress-container.discrete .progress-bit{left:0;transition:width .1s linear}.monaco-progress-container.discrete.done .progress-bit{width:100%}.monaco-progress-container.infinite .progress-bit{animation-name:progress;animation-duration:4s;animation-iteration-count:infinite;animation-timing-function:linear;transform:translate3d(0,0,0)}@keyframes progress{from{transform:translateX(0) scaleX(1)}50%{transform:translateX(2500%) scaleX(3)}to{transform:translateX(4900%) scaleX(1)}}.monaco-inputbox{position:relative;display:block;padding:0;box-sizing:border-box;font-size:inherit}.monaco-inputbox.idle{border:1px solid transparent}.monaco-inputbox>.ibwrapper>.input,.monaco-inputbox>.ibwrapper>.mirror{padding:4px}.monaco-inputbox>.ibwrapper{position:relative;width:100%;height:100%}.monaco-inputbox>.ibwrapper>.input{display:inline-block;box-sizing:border-box;width:100%;height:100%;line-height:inherit;border:none;font-family:inherit;font-size:inherit;resize:none;color:inherit}.monaco-inputbox>.ibwrapper>input{text-overflow:ellipsis}.monaco-inputbox>.ibwrapper>textarea.input{display:block;-ms-overflow-style:none;scrollbar-width:none;outline:0}.monaco-inputbox>.ibwrapper>textarea.input::-webkit-scrollbar{display:none}.monaco-inputbox>.ibwrapper>textarea.input.empty{white-space:nowrap}.monaco-inputbox>.ibwrapper>.mirror{position:absolute;display:inline-block;width:100%;top:0;left:0;box-sizing:border-box;white-space:pre-wrap;visibility:hidden;word-wrap:break-word}.monaco-inputbox-container{text-align:right}.monaco-inputbox-container .monaco-inputbox-message{display:inline-block;overflow:hidden;text-align:left;width:100%;box-sizing:border-box;padding:.4em;font-size:12px;line-height:17px;margin-top:-1px;word-wrap:break-word}.monaco-inputbox .monaco-action-bar{position:absolute;right:2px;top:4px}.monaco-inputbox .monaco-action-bar .action-item{margin-left:2px}.monaco-inputbox .monaco-action-bar .action-item .codicon{background-repeat:no-repeat;width:16px;height:16px}.monaco-keybinding{display:flex;align-items:center;line-height:10px}.monaco-keybinding>.monaco-keybinding-key{display:inline-block;border-style:solid;border-width:1px;border-radius:3px;vertical-align:middle;font-size:11px;padding:3px 5px;margin:0 2px}.monaco-keybinding>.monaco-keybinding-key:first-child{margin-left:0}.monaco-keybinding>.monaco-keybinding-key:last-child{margin-right:0}.monaco-keybinding>.monaco-keybinding-key-separator{display:inline-block}.monaco-keybinding>.monaco-keybinding-key-chord-separator{width:6px}.monaco-remote-cursor{position:absolute;pointer-events:none;z-index:4000;width:2px}.monaco-remote-cursor:before{content:"";width:6px;height:5px;display:block;margin-left:-2px;margin-top:0;z-index:4000;background:inherit}.monaco-remote-cursor-tooltip{position:absolute;white-space:nowrap;color:#fff;text-shadow:0 0 1px #000;opacity:1;font-size:12px;padding:2px;font-family:sans-serif;z-index:4000;transition:opacity .5s ease-out;-webkit-transition:opacity .5s ease-out;-moz-transition:opacity .5s ease-out;-ms-transition:opacity .5s ease-out;-o-transition:opacity .5s ease-out}.monaco-remote-selection{position:absolute;pointer-events:auto;opacity:.3;background:#00f}</style><style type="text/css" media="screen" class="monaco-colors">.codicon-add:before { content: '\ea60'; }
.codicon-light-bulb:before { content: '\ea61'; }
.codicon-warning:before { content: '\ea6c'; }
.codicon-info:before { content: '\ea74'; }
.codicon-close:before { content: '\ea76'; }
.codicon-symbol-folder:before { content: '\ea83'; }
.codicon-symbol-event:before { content: '\ea86'; }
.codicon-error:before { content: '\ea87'; }
.codicon-symbol-variable:before { content: '\ea88'; }
.codicon-symbol-array:before { content: '\ea8a'; }
.codicon-symbol-module:before { content: '\ea8b'; }
.codicon-symbol-package:before { content: '\ea8b'; }
.codicon-symbol-namespace:before { content: '\ea8b'; }
.codicon-symbol-object:before { content: '\ea8b'; }
.codicon-symbol-method:before { content: '\ea8c'; }
.codicon-symbol-function:before { content: '\ea8c'; }
.codicon-symbol-constructor:before { content: '\ea8c'; }
.codicon-symbol-boolean:before { content: '\ea8f'; }
.codicon-symbol-null:before { content: '\ea8f'; }
.codicon-symbol-number:before { content: '\ea90'; }
.codicon-symbol-struct:before { content: '\ea91'; }
.codicon-symbol-type-parameter:before { content: '\ea92'; }
.codicon-symbol-key:before { content: '\ea93'; }
.codicon-symbol-text:before { content: '\ea93'; }
.codicon-symbol-reference:before { content: '\ea94'; }
.codicon-symbol-enum:before { content: '\ea95'; }
.codicon-symbol-value:before { content: '\ea95'; }
.codicon-symbol-unit:before { content: '\ea96'; }
.codicon-arrow-down:before { content: '\ea9a'; }
.codicon-arrow-left:before { content: '\ea9b'; }
.codicon-arrow-up:before { content: '\eaa1'; }
.codicon-case-sensitive:before { content: '\eab1'; }
.codicon-check:before { content: '\eab2'; }
.codicon-chevron-down:before { content: '\eab4'; }
.codicon-chevron-right:before { content: '\eab6'; }
.codicon-chevron-up:before { content: '\eab7'; }
.codicon-lightbulb-autofix:before { content: '\eb13'; }
.codicon-loading:before { content: '\eb19'; }
.codicon-preserve-case:before { content: '\eb2e'; }
.codicon-regex:before { content: '\eb38'; }
.codicon-remove:before { content: '\eb3b'; }
.codicon-replace-all:before { content: '\eb3c'; }
.codicon-replace:before { content: '\eb3d'; }
.codicon-split-horizontal:before { content: '\eb56'; }
.codicon-split-vertical:before { content: '\eb57'; }
.codicon-symbol-class:before { content: '\eb5b'; }
.codicon-symbol-color:before { content: '\eb5c'; }
.codicon-symbol-constant:before { content: '\eb5d'; }
.codicon-symbol-enum-member:before { content: '\eb5e'; }
.codicon-symbol-field:before { content: '\eb5f'; }
.codicon-symbol-file:before { content: '\eb60'; }
.codicon-symbol-interface:before { content: '\eb61'; }
.codicon-symbol-keyword:before { content: '\eb62'; }
.codicon-symbol-operator:before { content: '\eb64'; }
.codicon-symbol-property:before { content: '\eb65'; }
.codicon-symbol-snippet:before { content: '\eb66'; }
.codicon-triangle-down:before { content: '\eb6e'; }
.codicon-triangle-left:before { content: '\eb6f'; }
.codicon-triangle-right:before { content: '\eb70'; }
.codicon-triangle-up:before { content: '\eb71'; }
.codicon-whole-word:before { content: '\eb7e'; }
.codicon-list-filter:before { content: '\eb83'; }
.codicon-list-selection:before { content: '\eb85'; }
.codicon-selection:before { content: '\eb85'; }
.codicon-symbol-string:before { content: '\eb8d'; }
.codicon-tree-item-expanded:before { content: '\eab4'; }
.codicon-tree-filter-on-type-on:before { content: '\eb83'; }
.codicon-tree-filter-on-type-off:before { content: '\eb85'; }
.codicon-tree-filter-clear:before { content: '\ea76'; }
.codicon-tree-item-loading:before { content: '\eb19'; }
.codicon-menu-selection:before { content: '\eab2'; }
.codicon-menu-submenu:before { content: '\eab6'; }
.codicon-scrollbar-button-left:before { content: '\eb6f'; }
.codicon-scrollbar-button-right:before { content: '\eb70'; }
.codicon-scrollbar-button-up:before { content: '\eb71'; }
.codicon-scrollbar-button-down:before { content: '\eb6e'; }
.codicon-quick-input-back:before { content: '\ea9b'; }
.codicon-widget-close:before { content: '\ea76'; }
.codicon-diff-review-insert:before { content: '\ea60'; }
.codicon-diff-review-remove:before { content: '\eb3b'; }
.codicon-diff-review-close:before { content: '\ea76'; }
.codicon-diff-insert:before { content: '\ea60'; }
.codicon-diff-remove:before { content: '\eb3b'; }
.codicon-marker-navigation-next:before { content: '\ea9a'; }
.codicon-marker-navigation-previous:before { content: '\eaa1'; }
.codicon-suggest-more-info:before { content: '\eab6'; }
.codicon-extensions-warning-message:before { content: '\ea6c'; }
.codicon-parameter-hints-next:before { content: '\eab4'; }
.codicon-parameter-hints-previous:before { content: '\eab7'; }
.monaco-editor, .monaco-editor-background, .monaco-editor .inputarea.ime-input { background-color: #f9f9f9; }
.monaco-editor, .monaco-editor .inputarea.ime-input { color: #000000; }
.monaco-editor .margin { background-color: #f9f9f9; }
.monaco-editor .rangeHighlight { background-color: rgba(253, 255, 0, 0.2); }
.monaco-editor .symbolHighlight { background-color: rgba(234, 92, 0, 0.33); }
.monaco-editor .mtkw { color: rgba(51, 51, 51, 0.2) !important; }
.monaco-editor .mtkz { color: rgba(51, 51, 51, 0.2) !important; }
.monaco-editor .unexpected-closing-bracket { color: rgba(255, 18, 18, 0.8); }
.monaco-editor .bracket-highlighting-0 { color: #0431fa; }
.monaco-editor .bracket-highlighting-1 { color: #319331; }
.monaco-editor .bracket-highlighting-2 { color: #7b3814; }
.monaco-editor .bracket-highlighting-3 { color: #0431fa; }
.monaco-editor .bracket-highlighting-4 { color: #319331; }
.monaco-editor .bracket-highlighting-5 { color: #7b3814; }
.monaco-editor .bracket-highlighting-6 { color: #0431fa; }
.monaco-editor .bracket-highlighting-7 { color: #319331; }
.monaco-editor .bracket-highlighting-8 { color: #7b3814; }
.monaco-editor .bracket-highlighting-9 { color: #0431fa; }
.monaco-editor .bracket-highlighting-10 { color: #319331; }
.monaco-editor .bracket-highlighting-11 { color: #7b3814; }
.monaco-editor .bracket-highlighting-12 { color: #0431fa; }
.monaco-editor .bracket-highlighting-13 { color: #319331; }
.monaco-editor .bracket-highlighting-14 { color: #7b3814; }
.monaco-editor .bracket-highlighting-15 { color: #0431fa; }
.monaco-editor .bracket-highlighting-16 { color: #319331; }
.monaco-editor .bracket-highlighting-17 { color: #7b3814; }
.monaco-editor .bracket-highlighting-18 { color: #0431fa; }
.monaco-editor .bracket-highlighting-19 { color: #319331; }
.monaco-editor .bracket-highlighting-20 { color: #7b3814; }
.monaco-editor .bracket-highlighting-21 { color: #0431fa; }
.monaco-editor .bracket-highlighting-22 { color: #319331; }
.monaco-editor .bracket-highlighting-23 { color: #7b3814; }
.monaco-editor .bracket-highlighting-24 { color: #0431fa; }
.monaco-editor .bracket-highlighting-25 { color: #319331; }
.monaco-editor .bracket-highlighting-26 { color: #7b3814; }
.monaco-editor .bracket-highlighting-27 { color: #0431fa; }
.monaco-editor .bracket-highlighting-28 { color: #319331; }
.monaco-editor .bracket-highlighting-29 { color: #7b3814; }
.monaco-editor .line-numbers { color: #237893; }
.monaco-editor .line-numbers.active-line-number { color: #0b216f; }
.monaco-editor .view-overlays .current-line { background-color: #fcfaec; }
.monaco-editor .margin-view-overlays .current-line-margin { background-color: #fcfaec; border: none; }

			.monaco-scrollable-element > .shadow.top {
				box-shadow: #dddddd 0 6px 6px -6px inset;
			}

			.monaco-scrollable-element > .shadow.left {
				box-shadow: #dddddd 6px 0 6px -6px inset;
			}

			.monaco-scrollable-element > .shadow.top.left {
				box-shadow: #dddddd 6px 6px 6px -6px inset;
			}
		

			.monaco-scrollable-element > .scrollbar > .slider {
				background: rgba(100, 100, 100, 0.4);
			}
		

			.monaco-scrollable-element > .scrollbar > .slider:hover {
				background: rgba(100, 100, 100, 0.7);
			}
		

			.monaco-scrollable-element > .scrollbar > .slider.active {
				background: rgba(0, 0, 0, 0.6);
			}
		
.monaco-editor .lines-content .core-guide-indent { box-shadow: 1px 0 0 0 #d3d3d3 inset; }
.monaco-editor .lines-content .core-guide-indent-active { box-shadow: 1px 0 0 0 #939393 inset; }
.monaco-editor .bracket-indent-guide.lvl-0 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-1 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-2 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-3 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-4 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-5 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-6 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-7 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-8 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-9 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-10 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-11 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-12 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-13 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-14 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-15 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-16 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-17 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-18 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-19 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-20 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-21 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-22 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-23 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-24 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-25 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-26 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .bracket-indent-guide.lvl-27 { --guide-color: rgba(4, 49, 250, 0.3); --guide-color-active: #0431fa; }
.monaco-editor .bracket-indent-guide.lvl-28 { --guide-color: rgba(49, 147, 49, 0.3); --guide-color-active: #319331; }
.monaco-editor .bracket-indent-guide.lvl-29 { --guide-color: rgba(123, 56, 20, 0.3); --guide-color-active: #7b3814; }
.monaco-editor .vertical { box-shadow: 1px 0 0 0 var(--guide-color) inset; }
.monaco-editor .horizontal-top { border-top: 1px solid var(--guide-color); }
.monaco-editor .horizontal-bottom { border-bottom: 1px solid var(--guide-color); }
.monaco-editor .vertical.indent-active { box-shadow: 1px 0 0 0 var(--guide-color-active) inset; }
.monaco-editor .horizontal-top.indent-active { border-top: 1px solid var(--guide-color-active); }
.monaco-editor .horizontal-bottom.indent-active { border-bottom: 1px solid var(--guide-color-active); }
.monaco-editor .minimap-slider .minimap-slider-horizontal { background: rgba(100, 100, 100, 0.2); }
.monaco-editor .minimap-slider:hover .minimap-slider-horizontal { background: rgba(100, 100, 100, 0.35); }
.monaco-editor .minimap-slider.active .minimap-slider-horizontal { background: rgba(0, 0, 0, 0.3); }
.monaco-editor .minimap-shadow-visible { box-shadow: #dddddd -6px 0 6px -6px inset; }
.monaco-editor .view-ruler { box-shadow: 1px 0 0 0 #d3d3d3 inset; }
.monaco-editor .scroll-decoration { box-shadow: #dddddd 0 6px 6px -6px inset; }
.monaco-editor .focused .selected-text { background-color: #add6ff; }
.monaco-editor .selected-text { background-color: #e5ebf1; }
.monaco-editor .cursors-layer .cursor { background-color: #000000; border-color: #000000; color: #ffffff; }
.monaco-editor .squiggly-error { background: url("data:image/svg+xml,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%206%203'%20enable-background%3D'new%200%200%206%203'%20height%3D'3'%20width%3D'6'%3E%3Cg%20fill%3D'%23e51400'%3E%3Cpolygon%20points%3D'5.5%2C0%202.5%2C3%201.1%2C3%204.1%2C0'%2F%3E%3Cpolygon%20points%3D'4%2C0%206%2C2%206%2C0.6%205.4%2C0'%2F%3E%3Cpolygon%20points%3D'0%2C2%201%2C3%202.4%2C3%200%2C0.6'%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E") repeat-x bottom left; }
.monaco-editor .squiggly-warning { background: url("data:image/svg+xml,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%206%203'%20enable-background%3D'new%200%200%206%203'%20height%3D'3'%20width%3D'6'%3E%3Cg%20fill%3D'%23bf8803'%3E%3Cpolygon%20points%3D'5.5%2C0%202.5%2C3%201.1%2C3%204.1%2C0'%2F%3E%3Cpolygon%20points%3D'4%2C0%206%2C2%206%2C0.6%205.4%2C0'%2F%3E%3Cpolygon%20points%3D'0%2C2%201%2C3%202.4%2C3%200%2C0.6'%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E") repeat-x bottom left; }
.monaco-editor .squiggly-info { background: url("data:image/svg+xml,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%206%203'%20enable-background%3D'new%200%200%206%203'%20height%3D'3'%20width%3D'6'%3E%3Cg%20fill%3D'%231a85ff'%3E%3Cpolygon%20points%3D'5.5%2C0%202.5%2C3%201.1%2C3%204.1%2C0'%2F%3E%3Cpolygon%20points%3D'4%2C0%206%2C2%206%2C0.6%205.4%2C0'%2F%3E%3Cpolygon%20points%3D'0%2C2%201%2C3%202.4%2C3%200%2C0.6'%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E") repeat-x bottom left; }
.monaco-editor .squiggly-hint { background: url("data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20height%3D%223%22%20width%3D%2212%22%3E%3Cg%20fill%3D%22%236c6c6c%22%3E%3Ccircle%20cx%3D%221%22%20cy%3D%221%22%20r%3D%221%22%2F%3E%3Ccircle%20cx%3D%225%22%20cy%3D%221%22%20r%3D%221%22%2F%3E%3Ccircle%20cx%3D%229%22%20cy%3D%221%22%20r%3D%221%22%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E") no-repeat bottom left; }
.monaco-editor.showUnused .squiggly-inline-unnecessary { opacity: 0.467; }
.monaco-editor.showDeprecated .squiggly-inline-deprecated { text-decoration: line-through; text-decoration-color: #000000}
.monaco-diff-editor .diff-review-line-number { color: #237893; }
.monaco-diff-editor .diff-review-shadow { box-shadow: #dddddd 0 -6px 6px -6px inset; }
.monaco-editor .line-insert, .monaco-editor .char-insert { background-color: rgba(190, 230, 190, 0.5); }
.monaco-diff-editor .line-insert, .monaco-diff-editor .char-insert { background-color: rgba(190, 230, 190, 0.5); }
.monaco-editor .inline-added-margin-view-zone { background-color: rgba(190, 230, 190, 0.5); }
.monaco-editor .line-delete, .monaco-editor .char-delete { background-color: rgba(214, 214, 214, 0.5); }
.monaco-diff-editor .line-delete, .monaco-diff-editor .char-delete { background-color: rgba(214, 214, 214, 0.5); }
.monaco-editor .inline-deleted-margin-view-zone { background-color: rgba(214, 214, 214, 0.5); }
.monaco-diff-editor.side-by-side .editor.modified { box-shadow: -6px 0 5px -5px #dddddd; }

			.monaco-diff-editor .diffViewport {
				background: rgba(100, 100, 100, 0.4);
			}
		

			.monaco-diff-editor .diffViewport:hover {
				background: rgba(100, 100, 100, 0.7);
			}
		

			.monaco-diff-editor .diffViewport:active {
				background: rgba(0, 0, 0, 0.6);
			}
		

	.monaco-editor .diagonal-fill {
		background-image: linear-gradient(
			-45deg,
			rgba(34, 34, 34, 0.2) 12.5%,
			#0000 12.5%, #0000 50%,
			rgba(34, 34, 34, 0.2) 50%, rgba(34, 34, 34, 0.2) 62.5%,
			#0000 62.5%, #0000 100%
		);
		background-size: 8px 8px;
	}
	
.monaco-editor .bracket-match { background-color: rgba(0, 100, 0, 0.1); }
.monaco-editor .bracket-match { border: 1px solid #b9b9b9; }

		.monaco-editor .contentWidgets .codicon.codicon-light-bulb {
			color: #ddb100;
			background-color: rgba(249, 249, 249, 0.7);
		}

		.monaco-editor .contentWidgets .codicon.codicon-lightbulb-autofix {
			color: #007acc;
			background-color: rgba(249, 249, 249, 0.7);
		}
.monaco-editor .goto-definition-link { color: #0000ff !important; }

			.monaco-editor .zone-widget .codicon.codicon-error,
			.markers-panel .marker-icon.codicon.codicon-error,
			.text-search-provider-messages .providerMessage .codicon.codicon-error,
			.extensions-viewlet > .extensions .codicon.codicon-error {
				color: #e51400;
			}
		

			.monaco-editor .zone-widget .codicon.codicon-warning,
			.markers-panel .marker-icon.codicon.codicon-warning,
			.extensions-viewlet > .extensions .codicon.codicon-warning,
			.extension-editor .codicon.codicon-warning,
			.text-search-provider-messages .providerMessage .codicon.codicon-warning,
			.preferences-editor .codicon.codicon-warning {
				color: #bf8803;
			}
		

			.monaco-editor .zone-widget .codicon.codicon-info,
			.markers-panel .marker-icon.codicon.codicon-info,
			.extensions-viewlet > .extensions .codicon.codicon-info,
			.text-search-provider-messages .providerMessage .codicon.codicon-info,
			.extension-editor .codicon.codicon-info {
				color: #1a85ff;
			}
		
.monaco-hover .hover-contents a.code-link span { color: #006ab1; }
.monaco-hover .hover-contents a.code-link span:hover { color: #006ab1; }
.codicon.codicon-symbol-array { color: #616161; }
.codicon.codicon-symbol-boolean { color: #616161; }
.codicon.codicon-symbol-class { color: #d67e00; }
.codicon.codicon-symbol-method { color: #652d90; }
.codicon.codicon-symbol-color { color: #616161; }
.codicon.codicon-symbol-constant { color: #616161; }
.codicon.codicon-symbol-constructor { color: #652d90; }

			.codicon.codicon-symbol-value,.codicon.codicon-symbol-enum { color: #d67e00; }
.codicon.codicon-symbol-enum-member { color: #007acc; }
.codicon.codicon-symbol-event { color: #d67e00; }
.codicon.codicon-symbol-field { color: #007acc; }
.codicon.codicon-symbol-file { color: #616161; }
.codicon.codicon-symbol-folder { color: #616161; }
.codicon.codicon-symbol-function { color: #652d90; }
.codicon.codicon-symbol-interface { color: #007acc; }
.codicon.codicon-symbol-key { color: #616161; }
.codicon.codicon-symbol-keyword { color: #616161; }
.codicon.codicon-symbol-module { color: #616161; }
.codicon.codicon-symbol-namespace { color: #616161; }
.codicon.codicon-symbol-null { color: #616161; }
.codicon.codicon-symbol-number { color: #616161; }
.codicon.codicon-symbol-object { color: #616161; }
.codicon.codicon-symbol-operator { color: #616161; }
.codicon.codicon-symbol-package { color: #616161; }
.codicon.codicon-symbol-property { color: #616161; }
.codicon.codicon-symbol-reference { color: #616161; }
.codicon.codicon-symbol-snippet { color: #616161; }
.codicon.codicon-symbol-string { color: #616161; }
.codicon.codicon-symbol-struct { color: #616161; }
.codicon.codicon-symbol-text { color: #616161; }
.codicon.codicon-symbol-type-parameter { color: #616161; }
.codicon.codicon-symbol-unit { color: #616161; }
.codicon.codicon-symbol-variable { color: #007acc; }
.monaco-editor .ghost-text-decoration { color: rgba(0, 0, 0, 0.47) !important; }
.monaco-editor .ghost-text-decoration-preview { color: rgba(0, 0, 0, 0.47) !important; }
.monaco-editor .suggest-preview-text .ghost-text { color: rgba(0, 0, 0, 0.47) !important; }
.monaco-link { color: #006ab1; }
.monaco-link:hover { color: #006ab1; }
.monaco-editor .hoverHighlight { background-color: rgba(173, 214, 255, 0.15); }
.monaco-editor .monaco-hover { background-color: #f3f3f3; }
.monaco-editor .monaco-hover { border: 1px solid #c8c8c8; }
.monaco-editor .monaco-hover .hover-row:not(:first-child):not(:empty) { border-top: 1px solid rgba(200, 200, 200, 0.5); }
.monaco-editor .monaco-hover hr { border-top: 1px solid rgba(200, 200, 200, 0.5); }
.monaco-editor .monaco-hover hr { border-bottom: 0px solid rgba(200, 200, 200, 0.5); }
.monaco-editor .monaco-hover a { color: #006ab1; }
.monaco-editor .monaco-hover a:hover { color: #006ab1; }
.monaco-editor .monaco-hover { color: #616161; }
.monaco-editor .monaco-hover .hover-row .actions { background-color: #e7e7e7; }
.monaco-editor .monaco-hover code { background-color: rgba(220, 220, 220, 0.4); }
.monaco-editor.vs .valueSetReplacement { outline: solid 2px #b9b9b9; }
.monaco-editor .detected-link-active { color: #0000ff !important; }
.monaco-editor .parameter-hints-widget { border: 1px solid #c8c8c8; }
.monaco-editor .parameter-hints-widget.multiple .body { border-left: 1px solid rgba(200, 200, 200, 0.5); }
.monaco-editor .parameter-hints-widget .signature.has-docs { border-bottom: 1px solid rgba(200, 200, 200, 0.5); }
.monaco-editor .parameter-hints-widget { background-color: #f3f3f3; }
.monaco-editor .parameter-hints-widget a { color: #006ab1; }
.monaco-editor .parameter-hints-widget a:hover { color: #006ab1; }
.monaco-editor .parameter-hints-widget { color: #616161; }
.monaco-editor .parameter-hints-widget code { background-color: rgba(220, 220, 220, 0.4); }
.monaco-editor .parameter-hints-widget .parameter.active { color: #0066bf}
.monaco-editor .focused .selectionHighlight { background-color: rgba(173, 214, 255, 0.3); }
.monaco-editor .selectionHighlight { background-color: rgba(173, 214, 255, 0.15); }
.monaco-editor .wordHighlight { background-color: rgba(87, 87, 87, 0.25); }
.monaco-editor .wordHighlightStrong { background-color: rgba(14, 99, 156, 0.25); }
.monaco-editor .tokens-inspect-widget { border: 1px solid #c8c8c8; }
.monaco-editor .tokens-inspect-widget .tokens-inspect-separator { background-color: #c8c8c8; }
.monaco-editor .tokens-inspect-widget { background-color: #f3f3f3; }
.monaco-editor .tokens-inspect-widget { color: #616161; }
.monaco-editor { --vscode-foreground: #616161;
--vscode-errorForeground: #a1260d;
--vscode-icon-foreground: #424242;
--vscode-focusBorder: #0090f1;
--vscode-textLink-foreground: #006ab1;
--vscode-textLink-activeForeground: #006ab1;
--vscode-textCodeBlock-background: rgba(220, 220, 220, 0.4);
--vscode-widget-shadow: rgba(0, 0, 0, 0.16);
--vscode-input-background: #ffffff;
--vscode-input-foreground: #616161;
--vscode-inputOption-activeBorder: rgba(0, 122, 204, 0);
--vscode-inputOption-activeBackground: rgba(0, 144, 241, 0.2);
--vscode-inputOption-activeForeground: #000000;
--vscode-inputValidation-infoBackground: #d6ecf2;
--vscode-inputValidation-infoBorder: #007acc;
--vscode-inputValidation-warningBackground: #f6f5d2;
--vscode-inputValidation-warningBorder: #b89500;
--vscode-inputValidation-errorBackground: #f2dede;
--vscode-inputValidation-errorBorder: #be1100;
--vscode-dropdown-background: #ffffff;
--vscode-button-foreground: #ffffff;
--vscode-button-background: #007acc;
--vscode-button-hoverBackground: #0062a3;
--vscode-badge-background: #c4c4c4;
--vscode-badge-foreground: #333333;
--vscode-scrollbar-shadow: #dddddd;
--vscode-scrollbarSlider-background: rgba(100, 100, 100, 0.4);
--vscode-scrollbarSlider-hoverBackground: rgba(100, 100, 100, 0.7);
--vscode-scrollbarSlider-activeBackground: rgba(0, 0, 0, 0.6);
--vscode-progressBar-background: #0e70c0;
--vscode-editorError-foreground: #e51400;
--vscode-editorWarning-foreground: #bf8803;
--vscode-editorInfo-foreground: #1a85ff;
--vscode-editorHint-foreground: #6c6c6c;
--vscode-editor-background: #f9f9f9;
--vscode-editor-foreground: #000000;
--vscode-editorWidget-background: #f3f3f3;
--vscode-editorWidget-foreground: #616161;
--vscode-editorWidget-border: #c8c8c8;
--vscode-quickInput-background: #f3f3f3;
--vscode-quickInput-foreground: #616161;
--vscode-quickInputTitle-background: rgba(0, 0, 0, 0.06);
--vscode-pickerGroup-foreground: #0066bf;
--vscode-pickerGroup-border: #cccedb;
--vscode-keybindingLabel-background: rgba(221, 221, 221, 0.4);
--vscode-keybindingLabel-foreground: #555555;
--vscode-keybindingLabel-border: rgba(204, 204, 204, 0.4);
--vscode-keybindingLabel-bottomBorder: rgba(187, 187, 187, 0.4);
--vscode-editor-selectionBackground: #add6ff;
--vscode-editor-inactiveSelectionBackground: #e5ebf1;
--vscode-editor-selectionHighlightBackground: rgba(173, 214, 255, 0.3);
--vscode-editor-findMatchBackground: #a8ac94;
--vscode-editor-findMatchHighlightBackground: rgba(234, 92, 0, 0.33);
--vscode-editor-findRangeHighlightBackground: rgba(180, 180, 180, 0.3);
--vscode-editor-hoverHighlightBackground: rgba(173, 214, 255, 0.15);
--vscode-editorHoverWidget-background: #f3f3f3;
--vscode-editorHoverWidget-foreground: #616161;
--vscode-editorHoverWidget-border: #c8c8c8;
--vscode-editorHoverWidget-statusBarBackground: #e7e7e7;
--vscode-editorLink-activeForeground: #0000ff;
--vscode-editorInlayHint-foreground: rgba(51, 51, 51, 0.8);
--vscode-editorInlayHint-background: rgba(196, 196, 196, 0.3);
--vscode-editorInlayHint-typeForeground: rgba(51, 51, 51, 0.8);
--vscode-editorInlayHint-typeBackground: rgba(196, 196, 196, 0.3);
--vscode-editorInlayHint-parameterForeground: rgba(51, 51, 51, 0.8);
--vscode-editorInlayHint-parameterBackground: rgba(196, 196, 196, 0.3);
--vscode-editorLightBulb-foreground: #ddb100;
--vscode-editorLightBulbAutoFix-foreground: #007acc;
--vscode-diffEditor-insertedTextBackground: rgba(190, 230, 190, 0.5);
--vscode-diffEditor-removedTextBackground: rgba(214, 214, 214, 0.5);
--vscode-diffEditor-diagonalFill: rgba(34, 34, 34, 0.2);
--vscode-list-focusOutline: #0090f1;
--vscode-list-activeSelectionBackground: #0060c0;
--vscode-list-activeSelectionForeground: #ffffff;
--vscode-list-inactiveSelectionBackground: #e4e6f1;
--vscode-list-hoverBackground: #f0f0f0;
--vscode-list-dropBackground: #d6ebff;
--vscode-list-highlightForeground: #0066bf;
--vscode-listFilterWidget-background: #efc1ad;
--vscode-listFilterWidget-outline: rgba(0, 0, 0, 0);
--vscode-listFilterWidget-noMatchesOutline: #be1100;
--vscode-tree-indentGuidesStroke: #a9a9a9;
--vscode-tree-tableColumnsBorder: rgba(97, 97, 97, 0.13);
--vscode-tree-tableOddRowsBackground: rgba(97, 97, 97, 0.04);
--vscode-quickInputList-focusForeground: #ffffff;
--vscode-quickInputList-focusBackground: #0060c0;
--vscode-menu-foreground: #616161;
--vscode-menu-background: #ffffff;
--vscode-menu-selectionForeground: #ffffff;
--vscode-menu-selectionBackground: #0060c0;
--vscode-menu-separatorBackground: #888888;
--vscode-toolbar-hoverBackground: rgba(184, 184, 184, 0.31);
--vscode-editorOverviewRuler-findMatchForeground: rgba(209, 134, 22, 0.49);
--vscode-editorOverviewRuler-selectionHighlightForeground: rgba(0, 0, 128, 0);
--vscode-editorOverviewRuler-unicodeForeground: rgba(209, 134, 22, 0.49);
--vscode-minimap-findMatchHighlight: #d18616;
--vscode-minimap-selectionOccurrenceHighlight: #c9c9c9;
--vscode-minimap-selectionHighlight: #add6ff;
--vscode-minimap-errorHighlight: rgba(255, 18, 18, 0.7);
--vscode-minimap-warningHighlight: #bf8803;
--vscode-minimap-foregroundOpacity: #000000;
--vscode-minimap-unicodeHighlight: #d18616;
--vscode-minimapSlider-background: rgba(100, 100, 100, 0.2);
--vscode-minimapSlider-hoverBackground: rgba(100, 100, 100, 0.35);
--vscode-minimapSlider-activeBackground: rgba(0, 0, 0, 0.3);
--vscode-problemsErrorIcon-foreground: #e51400;
--vscode-problemsWarningIcon-foreground: #bf8803;
--vscode-problemsInfoIcon-foreground: #1a85ff;
--vscode-editor-lineHighlightBackground: #fcfaec;
--vscode-editor-lineHighlightBorder: #eeeeee;
--vscode-editor-rangeHighlightBackground: rgba(253, 255, 0, 0.2);
--vscode-editor-symbolHighlightBackground: rgba(234, 92, 0, 0.33);
--vscode-editorCursor-foreground: #000000;
--vscode-editorWhitespace-foreground: rgba(51, 51, 51, 0.2);
--vscode-editorIndentGuide-background: #d3d3d3;
--vscode-editorIndentGuide-activeBackground: #939393;
--vscode-editorLineNumber-foreground: #237893;
--vscode-editorActiveLineNumber-foreground: #0b216f;
--vscode-editorLineNumber-activeForeground: #0b216f;
--vscode-editorRuler-foreground: #d3d3d3;
--vscode-editorBracketMatch-background: rgba(0, 100, 0, 0.1);
--vscode-editorBracketMatch-border: #b9b9b9;
--vscode-editorOverviewRuler-border: rgba(127, 127, 127, 0.3);
--vscode-editorGutter-background: #f9f9f9;
--vscode-editorUnnecessaryCode-opacity: rgba(0, 0, 0, 0.47);
--vscode-editorGhostText-foreground: rgba(0, 0, 0, 0.47);
--vscode-editorOverviewRuler-rangeHighlightForeground: rgba(0, 122, 204, 0.6);
--vscode-editorOverviewRuler-errorForeground: rgba(255, 18, 18, 0.7);
--vscode-editorOverviewRuler-warningForeground: #bf8803;
--vscode-editorOverviewRuler-infoForeground: #1a85ff;
--vscode-editorBracketHighlight-foreground1: #0431fa;
--vscode-editorBracketHighlight-foreground2: #319331;
--vscode-editorBracketHighlight-foreground3: #7b3814;
--vscode-editorBracketHighlight-foreground4: rgba(0, 0, 0, 0);
--vscode-editorBracketHighlight-foreground5: rgba(0, 0, 0, 0);
--vscode-editorBracketHighlight-foreground6: rgba(0, 0, 0, 0);
--vscode-editorBracketHighlight-unexpectedBracket.foreground: rgba(255, 18, 18, 0.8);
--vscode-editorBracketPairGuide-background1: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-background2: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-background3: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-background4: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-background5: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-background6: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-activeBackground1: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-activeBackground2: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-activeBackground3: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-activeBackground4: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-activeBackground5: rgba(0, 0, 0, 0);
--vscode-editorBracketPairGuide-activeBackground6: rgba(0, 0, 0, 0);
--vscode-editorOverviewRuler-bracketMatchForeground: rgba(0, 0, 128, 0);
--vscode-peekViewTitle-background: rgba(26, 133, 255, 0.1);
--vscode-peekViewTitleLabel-foreground: #000000;
--vscode-peekViewTitleDescription-foreground: #616161;
--vscode-peekView-border: #1a85ff;
--vscode-peekViewResult-background: #f3f3f3;
--vscode-editorMarkerNavigationError-background: #e51400;
--vscode-editorMarkerNavigationError-headerBackground: rgba(229, 20, 0, 0.1);
--vscode-editorMarkerNavigationWarning-background: #bf8803;
--vscode-editorMarkerNavigationWarning-headerBackground: rgba(191, 136, 3, 0.1);
--vscode-editorMarkerNavigationInfo-background: #1a85ff;
--vscode-editorMarkerNavigationInfo-headerBackground: rgba(26, 133, 255, 0.1);
--vscode-editorMarkerNavigation-background: #f9f9f9;
--vscode-symbolIcon-arrayForeground: #616161;
--vscode-symbolIcon-booleanForeground: #616161;
--vscode-symbolIcon-classForeground: #d67e00;
--vscode-symbolIcon-colorForeground: #616161;
--vscode-symbolIcon-constantForeground: #616161;
--vscode-symbolIcon-constructorForeground: #652d90;
--vscode-symbolIcon-enumeratorForeground: #d67e00;
--vscode-symbolIcon-enumeratorMemberForeground: #007acc;
--vscode-symbolIcon-eventForeground: #d67e00;
--vscode-symbolIcon-fieldForeground: #007acc;
--vscode-symbolIcon-fileForeground: #616161;
--vscode-symbolIcon-folderForeground: #616161;
--vscode-symbolIcon-functionForeground: #652d90;
--vscode-symbolIcon-interfaceForeground: #007acc;
--vscode-symbolIcon-keyForeground: #616161;
--vscode-symbolIcon-keywordForeground: #616161;
--vscode-symbolIcon-methodForeground: #652d90;
--vscode-symbolIcon-moduleForeground: #616161;
--vscode-symbolIcon-namespaceForeground: #616161;
--vscode-symbolIcon-nullForeground: #616161;
--vscode-symbolIcon-numberForeground: #616161;
--vscode-symbolIcon-objectForeground: #616161;
--vscode-symbolIcon-operatorForeground: #616161;
--vscode-symbolIcon-packageForeground: #616161;
--vscode-symbolIcon-propertyForeground: #616161;
--vscode-symbolIcon-referenceForeground: #616161;
--vscode-symbolIcon-snippetForeground: #616161;
--vscode-symbolIcon-stringForeground: #616161;
--vscode-symbolIcon-structForeground: #616161;
--vscode-symbolIcon-textForeground: #616161;
--vscode-symbolIcon-typeParameterForeground: #616161;
--vscode-symbolIcon-unitForeground: #616161;
--vscode-symbolIcon-variableForeground: #007acc;
--vscode-editorSuggestWidget-selectedBackground: #d6ebff;
--vscode-editorHoverWidget-highlightForeground: #0066bf;
--vscode-editor-wordHighlightBackground: rgba(87, 87, 87, 0.25);
--vscode-editor-wordHighlightStrongBackground: rgba(14, 99, 156, 0.25);
--vscode-editorOverviewRuler-wordHighlightForeground: rgba(160, 160, 160, 0.8);
--vscode-editorOverviewRuler-wordHighlightStrongForeground: rgba(192, 160, 192, 0.8); }

.mtk_3_1 { color: #000000; }
.mtk_3_2 { color: #f9f9f9; }
.mtk_3_3 { color: #808080; }
.mtk_3_4 { color: #ff0000; }
.mtk_3_5 { color: #0451a5; }
.mtk_3_6 { color: #0000ff; }
.mtk_3_7 { color: #098658; }
.mtk_3_8 { color: #008000; }
.mtk_3_9 { color: #dd0000; }
.mtk_3_10 { color: #660e7a; }
.mtk_3_11 { color: #383838; }
.mtk_3_12 { color: #cd3131; }
.mtk_3_13 { color: #863b00; }
.mtk_3_14 { color: #000080; }
.mtk_3_15 { color: #af00db; }
.mtk_3_16 { color: #800000; }
.mtk_3_17 { color: #e00000; }
.mtk_3_18 { color: #3030c0; }
.mtk_3_19 { color: #666666; }
.mtk_3_20 { color: #778899; }
.mtk_3_21 { color: #c700c7; }
.mtk_3_22 { color: #a31515; }
.mtk_3_23 { color: #008080; }
.mtk_3_24 { color: #0000b2; }
.mtk_3_25 { color: #4f76ac; }
.mtk_3_26 { color: #001188; }
.mtk_3_27 { color: #4864aa; }
.mtki { font-style: italic; }
.mtkb { font-weight: bold; }
.mtku { text-decoration: underline; text-underline-position: under; }</style><style type="text/css">.MathJax_Hover_Frame {border-radius: .25em; -webkit-border-radius: .25em; -moz-border-radius: .25em; -khtml-border-radius: .25em; box-shadow: 0px 0px 15px #83A; -webkit-box-shadow: 0px 0px 15px #83A; -moz-box-shadow: 0px 0px 15px #83A; -khtml-box-shadow: 0px 0px 15px #83A; border: 1px solid #A6D ! important; display: inline-block; position: absolute}
.MathJax_Menu_Button .MathJax_Hover_Arrow {position: absolute; cursor: pointer; display: inline-block; border: 2px solid #AAA; border-radius: 4px; -webkit-border-radius: 4px; -moz-border-radius: 4px; -khtml-border-radius: 4px; font-family: 'Courier New',Courier; font-size: 9px; color: #F0F0F0}
.MathJax_Menu_Button .MathJax_Hover_Arrow span {display: block; background-color: #AAA; border: 1px solid; border-radius: 3px; line-height: 0; padding: 4px}
.MathJax_Hover_Arrow:hover {color: white!important; border: 2px solid #CCC!important}
.MathJax_Hover_Arrow:hover span {background-color: #CCC!important}
</style><style type="text/css">#MathJax_About {position: fixed; left: 50%; width: auto; text-align: center; border: 3px outset; padding: 1em 2em; background-color: #DDDDDD; color: black; cursor: default; font-family: message-box; font-size: 120%; font-style: normal; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; z-index: 201; border-radius: 15px; -webkit-border-radius: 15px; -moz-border-radius: 15px; -khtml-border-radius: 15px; box-shadow: 0px 10px 20px #808080; -webkit-box-shadow: 0px 10px 20px #808080; -moz-box-shadow: 0px 10px 20px #808080; -khtml-box-shadow: 0px 10px 20px #808080; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
#MathJax_About.MathJax_MousePost {outline: none}
.MathJax_Menu {position: absolute; background-color: white; color: black; width: auto; padding: 2px; border: 1px solid #CCCCCC; margin: 0; cursor: default; font: menu; text-align: left; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; z-index: 201; box-shadow: 0px 10px 20px #808080; -webkit-box-shadow: 0px 10px 20px #808080; -moz-box-shadow: 0px 10px 20px #808080; -khtml-box-shadow: 0px 10px 20px #808080; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
.MathJax_MenuItem {padding: 2px 2em; background: transparent}
.MathJax_MenuArrow {position: absolute; right: .5em; padding-top: .25em; color: #666666; font-size: .75em}
.MathJax_MenuActive .MathJax_MenuArrow {color: white}
.MathJax_MenuArrow.RTL {left: .5em; right: auto}
.MathJax_MenuCheck {position: absolute; left: .7em}
.MathJax_MenuCheck.RTL {right: .7em; left: auto}
.MathJax_MenuRadioCheck {position: absolute; left: 1em}
.MathJax_MenuRadioCheck.RTL {right: 1em; left: auto}
.MathJax_MenuLabel {padding: 2px 2em 4px 1.33em; font-style: italic}
.MathJax_MenuRule {border-top: 1px solid #CCCCCC; margin: 4px 1px 0px}
.MathJax_MenuDisabled {color: GrayText}
.MathJax_MenuActive {background-color: Highlight; color: HighlightText}
.MathJax_MenuDisabled:focus, .MathJax_MenuLabel:focus {background-color: #E8E8E8}
.MathJax_ContextMenu:focus {outline: none}
.MathJax_ContextMenu .MathJax_MenuItem:focus {outline: none}
#MathJax_AboutClose {top: .2em; right: .2em}
.MathJax_Menu .MathJax_MenuClose {top: -10px; left: -10px}
.MathJax_MenuClose {position: absolute; cursor: pointer; display: inline-block; border: 2px solid #AAA; border-radius: 18px; -webkit-border-radius: 18px; -moz-border-radius: 18px; -khtml-border-radius: 18px; font-family: 'Courier New',Courier; font-size: 24px; color: #F0F0F0}
.MathJax_MenuClose span {display: block; background-color: #AAA; border: 1.5px solid; border-radius: 18px; -webkit-border-radius: 18px; -moz-border-radius: 18px; -khtml-border-radius: 18px; line-height: 0; padding: 8px 0 6px}
.MathJax_MenuClose:hover {color: white!important; border: 2px solid #CCC!important}
.MathJax_MenuClose:hover span {background-color: #CCC!important}
.MathJax_MenuClose:hover:focus {outline: none}
</style><style type="text/css">.MathJax_Preview .MJXf-math {color: inherit!important}
</style><style type="text/css">.MJX_Assistive_MathML {position: absolute!important; top: 0; left: 0; clip: rect(1px, 1px, 1px, 1px); padding: 1px 0 0 0!important; border: 0!important; height: 1px!important; width: 1px!important; overflow: hidden!important; display: block!important; -webkit-touch-callout: none; -webkit-user-select: none; -khtml-user-select: none; -moz-user-select: none; -ms-user-select: none; user-select: none}
.MJX_Assistive_MathML.MJX_Assistive_MathML_Block {width: 100%!important}
</style><style type="text/css">#MathJax_Zoom {position: absolute; background-color: #F0F0F0; overflow: auto; display: block; z-index: 301; padding: .5em; border: 1px solid black; margin: 0; font-weight: normal; font-style: normal; text-align: left; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; -webkit-box-sizing: content-box; -moz-box-sizing: content-box; box-sizing: content-box; box-shadow: 5px 5px 15px #AAAAAA; -webkit-box-shadow: 5px 5px 15px #AAAAAA; -moz-box-shadow: 5px 5px 15px #AAAAAA; -khtml-box-shadow: 5px 5px 15px #AAAAAA; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
#MathJax_ZoomOverlay {position: absolute; left: 0; top: 0; z-index: 300; display: inline-block; width: 100%; height: 100%; border: 0; padding: 0; margin: 0; background-color: white; opacity: 0; filter: alpha(opacity=0)}
#MathJax_ZoomFrame {position: relative; display: inline-block; height: 0; width: 0}
#MathJax_ZoomEventTrap {position: absolute; left: 0; top: 0; z-index: 302; display: inline-block; border: 0; padding: 0; margin: 0; background-color: white; opacity: 0; filter: alpha(opacity=0)}
</style><style type="text/css">.MathJax_Preview {color: #888}
#MathJax_Message {position: fixed; left: 1em; bottom: 1.5em; background-color: #E6E6E6; border: 1px solid #959595; margin: 0px; padding: 2px 8px; z-index: 102; color: black; font-size: 80%; width: auto; white-space: nowrap}
#MathJax_MSIE_Frame {position: absolute; top: 0; left: 0; width: 0px; z-index: 101; border: 0px; margin: 0px; padding: 0px}
.MathJax_Error {color: #CC0000; font-style: italic}
</style><style type="text/css">.MJXp-script {font-size: .8em}
.MJXp-right {-webkit-transform-origin: right; -moz-transform-origin: right; -ms-transform-origin: right; -o-transform-origin: right; transform-origin: right}
.MJXp-bold {font-weight: bold}
.MJXp-italic {font-style: italic}
.MJXp-scr {font-family: MathJax_Script,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-frak {font-family: MathJax_Fraktur,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-sf {font-family: MathJax_SansSerif,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-cal {font-family: MathJax_Caligraphic,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-mono {font-family: MathJax_Typewriter,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-largeop {font-size: 150%}
.MJXp-largeop.MJXp-int {vertical-align: -.2em}
.MJXp-math {display: inline-block; line-height: 1.2; text-indent: 0; font-family: 'Times New Roman',Times,STIXGeneral,serif; white-space: nowrap; border-collapse: collapse}
.MJXp-display {display: block; text-align: center; margin: 1em 0}
.MJXp-math span {display: inline-block}
.MJXp-box {display: block!important; text-align: center}
.MJXp-box:after {content: " "}
.MJXp-rule {display: block!important; margin-top: .1em}
.MJXp-char {display: block!important}
.MJXp-mo {margin: 0 .15em}
.MJXp-mfrac {margin: 0 .125em; vertical-align: .25em}
.MJXp-denom {display: inline-table!important; width: 100%}
.MJXp-denom > * {display: table-row!important}
.MJXp-surd {vertical-align: top}
.MJXp-surd > * {display: block!important}
.MJXp-script-box > *  {display: table!important; height: 50%}
.MJXp-script-box > * > * {display: table-cell!important; vertical-align: top}
.MJXp-script-box > *:last-child > * {vertical-align: bottom}
.MJXp-script-box > * > * > * {display: block!important}
.MJXp-mphantom {visibility: hidden}
.MJXp-munderover, .MJXp-munder {display: inline-table!important}
.MJXp-over {display: inline-block!important; text-align: center}
.MJXp-over > * {display: block!important}
.MJXp-munderover > *, .MJXp-munder > * {display: table-row!important}
.MJXp-mtable {vertical-align: .25em; margin: 0 .125em}
.MJXp-mtable > * {display: inline-table!important; vertical-align: middle}
.MJXp-mtr {display: table-row!important}
.MJXp-mtd {display: table-cell!important; text-align: center; padding: .5em 0 0 .5em}
.MJXp-mtr > .MJXp-mtd:first-child {padding-left: 0}
.MJXp-mtr:first-child > .MJXp-mtd {padding-top: 0}
.MJXp-mlabeledtr {display: table-row!important}
.MJXp-mlabeledtr > .MJXp-mtd:first-child {padding-left: 0}
.MJXp-mlabeledtr:first-child > .MJXp-mtd {padding-top: 0}
.MJXp-merror {background-color: #FFFF88; color: #CC0000; border: 1px solid #CC0000; padding: 1px 3px; font-style: normal; font-size: 90%}
.MJXp-scale0 {-webkit-transform: scaleX(.0); -moz-transform: scaleX(.0); -ms-transform: scaleX(.0); -o-transform: scaleX(.0); transform: scaleX(.0)}
.MJXp-scale1 {-webkit-transform: scaleX(.1); -moz-transform: scaleX(.1); -ms-transform: scaleX(.1); -o-transform: scaleX(.1); transform: scaleX(.1)}
.MJXp-scale2 {-webkit-transform: scaleX(.2); -moz-transform: scaleX(.2); -ms-transform: scaleX(.2); -o-transform: scaleX(.2); transform: scaleX(.2)}
.MJXp-scale3 {-webkit-transform: scaleX(.3); -moz-transform: scaleX(.3); -ms-transform: scaleX(.3); -o-transform: scaleX(.3); transform: scaleX(.3)}
.MJXp-scale4 {-webkit-transform: scaleX(.4); -moz-transform: scaleX(.4); -ms-transform: scaleX(.4); -o-transform: scaleX(.4); transform: scaleX(.4)}
.MJXp-scale5 {-webkit-transform: scaleX(.5); -moz-transform: scaleX(.5); -ms-transform: scaleX(.5); -o-transform: scaleX(.5); transform: scaleX(.5)}
.MJXp-scale6 {-webkit-transform: scaleX(.6); -moz-transform: scaleX(.6); -ms-transform: scaleX(.6); -o-transform: scaleX(.6); transform: scaleX(.6)}
.MJXp-scale7 {-webkit-transform: scaleX(.7); -moz-transform: scaleX(.7); -ms-transform: scaleX(.7); -o-transform: scaleX(.7); transform: scaleX(.7)}
.MJXp-scale8 {-webkit-transform: scaleX(.8); -moz-transform: scaleX(.8); -ms-transform: scaleX(.8); -o-transform: scaleX(.8); transform: scaleX(.8)}
.MJXp-scale9 {-webkit-transform: scaleX(.9); -moz-transform: scaleX(.9); -ms-transform: scaleX(.9); -o-transform: scaleX(.9); transform: scaleX(.9)}
.MathJax_PHTML .noError {vertical-align: ; font-size: 90%; text-align: left; color: black; padding: 1px 3px; border: 1px solid}
</style></head>
<body data-route="PUBLISHING_PRINT" class="print-page page-print"><div id="MathJax_Message" style="display: none;"></div>

























<!-- Google Tag Manager (noscript) -->

<!-- End Google Tag Manager (noscript) -->
















    















<div><div class="notebook_content"><div><div class="notebook"><div class="datalore-sheet"><div class="datalore-sheet_title">Sheet</div><div><div class="block markdown-block"><div class="markdown-output"><h1 id="Calcite-New-Frontend-Guide">Calcite New Frontend Guide</h1>
<p>This notebook will demonstrate how you can build frontends for languages other than SQL for Apache Calcite.</p>
<p>There are many languages for querying data. SQL is the most common, but other languages include:</p>
<ul>
<li>Datalog</li>
<li>RDF/Graph Queries</li>
<li>GraphQL</li>
<li>Custom DSL's</li>
</ul>
<p>Calcite currently does not have any tutorial materials on how to integrate alternative frontends.</p>
<p>This guide demonstrates how to do so, via a guided walkthrough of writing a <code>GraphQL -&gt; Calcite RelNode</code> converter.</p>
<p>(If you are familiar with the Calcite <code>Sql2RelConverter</code> class -- what we will be writing is essentially a <code>Gql2RelConverter</code>)</p>
</div></div><div class="block markdown-block"><div class="markdown-output"><h1 id="Overview-and-Goal">Overview and Goal</h1>
<p>The aim of this notebook is to walk through the translation of a GraphQL query like this:</p>
<pre><code class="language-graphql">query {
    EMP(
        limit: 2,
        offset: 1,
        where: {
            _or: [
                { DEPTNO: { _eq: 20 } },
                { DEPTNO: { _eq: 30 } }
            ]
            _and: [
                { SAL: { _gte: 1500 } }
                {
                    _or: [
                        { JOB: { _eq: "SALESMAN" } },
                        { JOB: { _eq: "MANAGER" } }
                    ]
                }
            ]
        }
    ) {
        EMPNO
        ENAME
        JOB
        MGR
        SAL
        COMM
        DEPTNO
    }
}
</code></pre>
<p>Into a SQL query like:</p>
<pre><code class="language-sql">SELECT "EMPNO", "ENAME", "JOB", "MGR", "SAL", "COMM", "DEPTNO"
FROM "EMP"
WHERE "DEPTNO" IN (20, 30) AND "SAL" &gt;= 1500 AND "JOB" IN ('MANAGER', 'SALESMAN')
</code></pre>
<p>And finally, execute that SQL statement &amp; ensure the proper results are returned.</p>
<p>You will learn about the following Calcite classes/concepts:</p>
<ul>
<li>SqlParser</li>
<li>RexNode</li>
<li>RelNode</li>
<li>RelToSqlConverter</li>
<li>RelBuilder</li>
<li>tools.Frameworks</li>
<li>CalciteConnection</li>
<li>Schema/SchemaPlus</li>
</ul>
</div></div><div class="block markdown-block"><div class="markdown-output"><h1 id="Technical-Overview,-10,000ft-View">Technical Overview, 10,000ft View</h1>
<p>What we need to do in order to accomplish our goal is roughly:</p>
<ol>
<li>Parse a GraphQL <strong>query string</strong> into a GraphQL <strong>Document AST</strong></li>
<li>Convert the GraphQL <strong>Document AST</strong> into some representation of <strong>Relational Query semantics</strong></li>
<li>Generate a Calcite <strong>"Row Expression" (RexNode)</strong> from our representation of the <strong><code>WHERE</code> clause</strong></li>
<li>Create a Calcite <strong>"Relational Expression" (RelNode)</strong> from a combination of the <strong><code>WHERE</code> "RexNode" and <code>SELECT</code> "RexNode"</strong></li>
<li><strong>Execute</strong> the RelNode against the <strong>data source</strong> we are trying to query against</li>
</ol>
<p>As a picture, it looks something like this:</p>
<p><img alt="GQL query translation pipeline" src="https://i.imgur.com/yfIVAga.png"></p>
</div></div><div class="block markdown-block"><div class="markdown-output"><h1 id="Dependencies-&amp;-Utility-Functions-(Skip-this)">Dependencies &amp; Utility Functions (Skip this)</h1>
<p>The following code cells simply install required libraries and define a few helper/utility functions.
You can skip this.</p>
</div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_3">@file</span><span class="mtk_3_1">:DependsOn(</span><span class="mtk_3_8 mtkb">"org.apache.calcite:calcite-core:1.29.0"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_3">@file</span><span class="mtk_3_1">:DependsOn(</span><span class="mtk_3_8 mtkb">"org.apache.calcite:calcite-testkit:1.29.0"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_3">@file</span><span class="mtk_3_1">:DependsOn(</span><span class="mtk_3_8 mtkb">"com.graphql-java:graphql-java:17.3"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_3">@file</span><span class="mtk_3_1">:DependsOn(</span><span class="mtk_3_8 mtkb">"org.hsqldb:hsqldb:2.4.1"</span><span class="mtk_3_1">)</span></span><br></pre></div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;Any.prettyPrint():&nbsp;String&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">var</span><span class="mtk_3_1">&nbsp;indentLevel&nbsp;=&nbsp;</span><span class="mtk_3_6">0</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;indentWidth&nbsp;=&nbsp;</span><span class="mtk_3_6">4</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;padding()&nbsp;=&nbsp;</span><span class="mtk_3_8 mtkb">""</span><span class="mtk_3_1">.padStart(indentLevel&nbsp;*&nbsp;indentWidth)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;toString&nbsp;=&nbsp;toString()</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;stringBuilder&nbsp;=&nbsp;StringBuilder(toString.length)</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">var</span><span class="mtk_3_1">&nbsp;i&nbsp;=&nbsp;</span><span class="mtk_3_6">0</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">while</span><span class="mtk_3_1">&nbsp;(i&nbsp;&lt;&nbsp;toString.length)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">when</span><span class="mtk_3_1">&nbsp;(</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;char&nbsp;=&nbsp;toString[i])&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">'('</span><span class="mtk_3_1">,&nbsp;</span><span class="mtk_3_8 mtkb">'['</span><span class="mtk_3_1">,&nbsp;</span><span class="mtk_3_8 mtkb">'{'</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;indentLevel++</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;stringBuilder.appendLine(char).app</span><span class="mtk_3_1">end(padding())</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">')'</span><span class="mtk_3_1">,&nbsp;</span><span class="mtk_3_8 mtkb">']'</span><span class="mtk_3_1">,&nbsp;</span><span class="mtk_3_8 mtkb">'}'</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;indentLevel--</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;stringBuilder.appendLine().append(</span><span class="mtk_3_1">padding()).append(char)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">','</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;stringBuilder.appendLine(char).app</span><span class="mtk_3_1">end(padding())</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_3 mtki">//&nbsp;ignore&nbsp;space&nbsp;after&nbsp;comma&nbsp;as&nbsp;we&nbsp;have&nbsp;added&nbsp;a&nbsp;new</span><span class="mtk_3_3 mtki">line</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;nextChar&nbsp;=&nbsp;toString.getOrElse(i&nbsp;+&nbsp;</span><span class="mtk_3_6">1</span><span class="mtk_3_1">)&nbsp;{&nbsp;char&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">if</span><span class="mtk_3_1">&nbsp;(nextChar&nbsp;==&nbsp;</span><span class="mtk_3_8 mtkb">'&nbsp;'</span><span class="mtk_3_1">)&nbsp;i++</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">else</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;stringBuilder.append(char)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i++</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;stringBuilder.toString()</span></span><br><span><span class="mtk_3_1">}</span></span><br></pre></div></div><div class="block markdown-block"><div class="markdown-output"><h1 id="1.-Parse-a-GraphQL-query-string-into-a-GraphQL-Document-AST">1. Parse a GraphQL query string into a GraphQL Document AST</h1>
<p>Below is code that we're not too interested in from the Calcite side of things.</p>
<p>This is necessary for the rest of the tutorial, but here we just set the groundwork for parsing a GraphQL query from a <code>String</code> into it's AST form (called a "<code>Document</code>").</p>
</div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;graphql.language.Argument</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;graphql.language.OperationDefinition</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;graphql.language.Field</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;graphql.parser.Parser</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;sampleQuery&nbsp;=</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"""</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;query&nbsp;{</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;EMP(</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;limit:&nbsp;2,</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;offset:&nbsp;1,</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;where:&nbsp;{</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;_or:&nbsp;[</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;DEPTNO:&nbsp;{&nbsp;_eq:&nbsp;20&nbsp;}&nbsp;},</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;DEPTNO:&nbsp;{&nbsp;_eq:&nbsp;30&nbsp;}&nbsp;}</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;]</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;_and:&nbsp;[</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;SAL:&nbsp;{&nbsp;_gte:&nbsp;1500&nbsp;}&nbsp;}</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;_or:&nbsp;[</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;JOB:&nbsp;{&nbsp;_eq:&nbsp;"SALESMA</span><span class="mtk_3_8 mtkb">N"&nbsp;}&nbsp;},</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;JOB:&nbsp;{&nbsp;_eq:&nbsp;"MANAGER</span><span class="mtk_3_8 mtkb">"&nbsp;}&nbsp;}</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;]</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;]</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;)&nbsp;{</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;EMPNO</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ENAME</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;JOB</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;MGR</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SAL</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;COMM</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DEPTNO</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_8 mtkb">&nbsp;&nbsp;&nbsp;&nbsp;"""</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;getFirstQuery(queryString:&nbsp;String):&nbsp;Field?&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;document&nbsp;=&nbsp;Parser.parse(queryString)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;root&nbsp;=&nbsp;document.definitions.first()&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;OperationDefinition</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;queries&nbsp;=&nbsp;root.selectionSet.selections</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;queries.first()&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;Field</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;getWhereArgumentFromGraphQLQuery(queryString:&nbsp;Str</span><span class="mtk_3_1">ing):&nbsp;Argument?&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;firstQuery&nbsp;=&nbsp;getFirstQuery(queryString)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">if</span><span class="mtk_3_1">&nbsp;(firstQuery&nbsp;!=&nbsp;</span><span class="mtk_3_14 mtkb">null</span><span class="mtk_3_1">)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;firstQuery.arguments.firstOrNull&nbsp;{&nbsp;</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.name&nbsp;==&nbsp;</span><span class="mtk_3_8 mtkb">"where"</span><span class="mtk_3_1">&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">null</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;getQuerySelectedFieldNames(queryString:&nbsp;String):&nbsp;</span><span class="mtk_3_1">List&lt;String&gt;&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;firstQuery&nbsp;=&nbsp;getFirstQuery(queryString)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">if</span><span class="mtk_3_1">&nbsp;(firstQuery&nbsp;!=&nbsp;</span><span class="mtk_3_14 mtkb">null</span><span class="mtk_3_1">)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;firstQuery.selectionSet.selections.map&nbsp;{&nbsp;(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;Field).name&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;emptyList()</span></span><br><span><span class="mtk_3_1">}</span></span><br></pre></div></div><div class="block markdown-block"><div class="markdown-output"><h1 id="2.-Convert-the-GraphQL-Document-AST-into-some-representation-of-Relational-Query-semantics">2. Convert the GraphQL Document AST into some representation of Relational Query semantics</h1>
<p>Here, we will write some code that converts the unwieldy GQL Query Document AST into a representation that is easier for us to work with and closer to the relational expression semantics we are trying to express.</p>
<p>Our Expression kind hierarchy looks like this:</p>
<pre><code class="language-scala">type Expression =
    | BinaryExpression
    | UnaryExpression
    | Column (name)
    | Literal (value)

type BinaryExpression (left, right) =
    | AND
    | OR
    | NOT
    | EQ
    | NE
    | LT
    | LTE
    | GT
    | GTE
    | IN
    | NIN

type UnaryExpression (operand) =
    | NOT
    | IS_NULL
</code></pre>
<p>Once we have a representation in this form, we can traverse it and convert it to a Calcite Row Expression (RexNode) that has identical semantics.</p>
<p>A useful tip here is that the signature for Calcite's <code>RelBuilder.call()</code> is:</p>
<pre><code class="language-java">public RexNode call(SqlOperator operator, RexNode... operands) {}
public RexNode call(SqlOperator operator, Iterable&lt;? extends RexNode&gt; operands) {}
</code></pre>
<p>We can model our own Relational Expression types as entities that each have an attached <code>SqlOperator</code>.</p>
<p>For binary operations, Calcite has a type called <code>SqlBinaryOperator</code>.</p>
<p>Calcite doesn't have something that maps directly to "Unary" operations. It has <code>SqlPrefixOperation</code> and <code>SqlPostfixOperation</code> instead.</p>
<p>You can find the operators under <strong><code>org.apache.calcite.sql.fun.SqlStdOperatorTable</code></strong>.</p>
</div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.rex.RexNode</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.sql.SqlBinaryOperator</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.sql.SqlOperator</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.sql.`</span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">`.SqlStdOperatorTable</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">sealed</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">interface</span><span class="mtk_3_1">&nbsp;Expression&nbsp;{}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">sealed</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">interface</span><span class="mtk_3_1">&nbsp;BinaryOperation&nbsp;:&nbsp;Expression&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">sealed</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">interface</span><span class="mtk_3_1">&nbsp;UnaryOperation&nbsp;:&nbsp;Expression&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operand:&nbsp;Expression</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlOperator</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;AND(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.AND</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;OR(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.OR</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;EQ(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.EQUALS</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;NEQ(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.NOT_EQUALS</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;LT(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.LESS_THAN</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;LTE(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.LESS_THAN_OR_EQUAL</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;GT(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.GREATER_THAN</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;GTE(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.GREATER_THAN_OR_EQUAL</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;IN(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.IN</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;NIN(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left:&nbsp;Expression,&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right:&nbsp;Expression)&nbsp;:&nbsp;BinaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlBinaryOperator&nbsp;=&nbsp;SqlStdOperatorTabl</span><span class="mtk_3_1">e.NOT_IN</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;NOT(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operand:&nbsp;Expression)&nbsp;:&nbsp;UnaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlOperator&nbsp;=&nbsp;SqlStdOperatorTable.NOT</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">data</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;IS_NULL(</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operand:&nbsp;Expression)&nbsp;:&nbsp;UnaryOperation&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">override</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operation:&nbsp;SqlOperator&nbsp;=&nbsp;SqlStdOperatorTable.IS_N</span><span class="mtk_3_1">ULL</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_3">@JvmInline</span></span><br><span><span class="mtk_3_1">value&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;COLUMN(</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;name:&nbsp;String)&nbsp;:&nbsp;Expression</span></span><br><span><span></span></span><br><span><span class="mtk_3_3">@JvmInline</span></span><br><span><span class="mtk_3_1">value&nbsp;</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">&nbsp;LITERAL(</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;value:&nbsp;Any)&nbsp;:&nbsp;Expression</span></span><br></pre></div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;graphql.language.*</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;graphql.parser.Parser</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Unwrap&nbsp;a&nbsp;GraphQL&nbsp;"Value"&nbsp;node&nbsp;to&nbsp;it's&nbsp;Java&nbsp;repr</span><span class="mtk_3_3 mtki">esentation</span></span><br><span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;graphqlValueToJava(value:&nbsp;Value&lt;*&gt;):&nbsp;Any&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">when</span><span class="mtk_3_1">&nbsp;(value)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;IntValue&nbsp;-&gt;&nbsp;value.value</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;FloatValue&nbsp;-&gt;&nbsp;value.value</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;StringValue&nbsp;-&gt;&nbsp;value.value</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;BooleanValue&nbsp;-&gt;&nbsp;value.isValue</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;EnumValue&nbsp;-&gt;&nbsp;value.name</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;ArrayValue&nbsp;-&gt;&nbsp;value.values.map&nbsp;{&nbsp;graphqlValueToJa</span><span class="mtk_3_1">va(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">)&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">else</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;</span><span class="mtk_3_14 mtkb">throw</span><span class="mtk_3_1">&nbsp;IllegalArgumentException(</span><span class="mtk_3_8 mtkb">"Unsupported&nbsp;value&nbsp;type:&nbsp;${value.javaClass}"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">}</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Convert&nbsp;a&nbsp;GraphQL&nbsp;query&nbsp;"where:&nbsp;{}"&nbsp;argument&nbsp;to</span><span class="mtk_3_3 mtki">&nbsp;an&nbsp;"Expression"&nbsp;AST</span></span><br><span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;graphqlWhereArgumentToExpression(whereArg:&nbsp;Argume</span><span class="mtk_3_1">nt):&nbsp;Expression&nbsp;{</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_3 mtki">//&nbsp;Recursive&nbsp;function&nbsp;which&nbsp;walks&nbsp;the&nbsp;GraphQL&nbsp;Quer</span><span class="mtk_3_3 mtki">y&nbsp;Document&nbsp;AST</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_3 mtki">//&nbsp;for&nbsp;the&nbsp;"where"&nbsp;argument,&nbsp;and&nbsp;constructs&nbsp;an&nbsp;equ</span><span class="mtk_3_3 mtki">ivalent&nbsp;relational&nbsp;expression&nbsp;AST</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;go(objectValue:&nbsp;ObjectValue):&nbsp;Expression&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;expr&nbsp;=&nbsp;objectValue.objectFields.map&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">when</span><span class="mtk_3_1">&nbsp;(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.name)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_not"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;NOT(go(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.value&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;ObjectValue))</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_and"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.value&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;ArrayValue).values</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.map&nbsp;{&nbsp;go(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;ObjectValue)&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.reduceRight(::AND)&nbsp;</span><span class="mtk_3_3 mtki">//&nbsp;Combine&nbsp;with&nbsp;logical&nbsp;AND</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_or"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.value&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;ArrayValue).values</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.map&nbsp;{&nbsp;go(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;ObjectValue)&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.reduceRight(::OR)&nbsp;</span><span class="mtk_3_3 mtki">//&nbsp;Combine&nbsp;with&nbsp;logical&nbsp;OR</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">else</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;name&nbsp;=&nbsp;</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.name</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;node&nbsp;=&nbsp;(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.value&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;ObjectValue).objectFields.first()</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;value&nbsp;=&nbsp;graphqlValueToJava(node.value)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">when</span><span class="mtk_3_1">&nbsp;(node.name)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_eq"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;EQ(COLUMN(name),&nbsp;LITERAL(value))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_ne"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;NEQ(COLUMN(name),&nbsp;LITERAL(value))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_lt"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;LT(COLUMN(name),&nbsp;LITERAL(value))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_lte"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;LTE(COLUMN(name),&nbsp;LITERAL(value))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_gt"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;GT(COLUMN(name),&nbsp;LITERAL(value))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_gte"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;GTE(COLUMN(name),&nbsp;LITERAL(value))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_in"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;IN(COLUMN(name),&nbsp;LITERAL(value))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_nin"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;NIN(COLUMN(name),&nbsp;LITERAL(value))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_8 mtkb">"_is_null"</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;IS_NULL(COLUMN(name))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">else</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;</span><span class="mtk_3_14 mtkb">throw</span><span class="mtk_3_1">&nbsp;IllegalArgumentException(</span><span class="mtk_3_8 mtkb">"Unsupported&nbsp;operator:&nbsp;${node.name}"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_3 mtki">//&nbsp;Combine&nbsp;all&nbsp;top-level&nbsp;conditions&nbsp;with&nbsp;logical&nbsp;A</span><span class="mtk_3_3 mtki">ND</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;expr.reduceRight(::AND)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span></span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">return</span><span class="mtk_3_1">&nbsp;go(whereArg.value&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;ObjectValue)</span></span><br><span><span class="mtk_3_1">}</span></span><br></pre></div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;whereArg&nbsp;=&nbsp;getWhereArgumentFromGraphQLQuery(sampl</span><span class="mtk_3_1">eQuery)</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;testExpression&nbsp;=&nbsp;whereArg?.let&nbsp;{&nbsp;graphqlWhereArgu</span><span class="mtk_3_1">mentToExpression(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">)&nbsp;}</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">if</span><span class="mtk_3_1">&nbsp;(testExpression&nbsp;!=&nbsp;</span><span class="mtk_3_14 mtkb">null</span><span class="mtk_3_1">)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;println(testExpression.prettyPrint())</span></span><br><span><span class="mtk_3_1">}</span></span><br></pre></div><div class="block-output datalore-block-output "><div><div class="publishing-text-output"><span>AND(</span><br><span>    left=OR(</span><br><span>        left=EQ(</span><br><span>            left=COLUMN(</span><br><span>                name=DEPTNO</span><br><span>            ),</span><br><span>            right=LITERAL(</span><br><span>                value=20</span><br><span>            )</span><br><span>        ),</span><br><span>        right=EQ(</span><br><span>            left=COLUMN(</span><br><span>                name=DEPTNO</span><br><span>            ),</span><br><span>            right=LITERAL(</span><br><span>                value=30</span><br><span>            )</span><br><span>        )</span><br><span>    ),</span><br><span>    right=AND(</span><br><span>        left=GTE(</span><br><span>            left=COLUMN(</span><br><span>                name=SAL</span><br><span>            ),</span><br><span>            right=LITERAL(</span><br><span>                value=1500</span><br><span>            )</span><br><span>        ),</span><br><span>        right=OR(</span><br><span>            left=EQ(</span><br><span>                left=COLUMN(</span><br><span>                    name=JOB</span><br><span>                ),</span><br><span>                right=LITERAL(</span><br><span>                    value=SALESMAN</span><br><span>                )</span><br><span>            ),</span><br><span>            right=EQ(</span><br><span>                left=COLUMN(</span><br><span>                    name=JOB</span><br><span>                ),</span><br><span>                right=LITERAL(</span><br><span>                    value=MANAGER</span><br><span>                )</span><br><span>            )</span><br><span>        )</span><br><span>    )</span><br><span>)</span><br><br></div></div><div class="edge"></div></div></div><div class="block markdown-block"><div class="markdown-output"><h1 id="3.-Generate-a-Calcite-&quot;Row-Expression&quot;-(RexNode)-from-our-representation-of-the-`WHERE`-clause">3. Generate a Calcite "Row Expression" (RexNode) from our representation of the <code>WHERE</code> clause</h1>
<p>Here we convert our "Expression" interface to the equivalent Calcite <code>RexNode</code>.</p>
<p>This is straightforward to do, because we assigned each of our interface types a corresponding <code>SqlOperator</code>.</p>
<p>We can just switch on the type of the expression and form the proper signature for <code>RelBuilder.call()</code></p>
</div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.tools.RelBuilder</span></span><br><span><span></span></span><br><span><span class="mtk_3_14 mtkb">fun</span><span class="mtk_3_1">&nbsp;Expression.toRexNode(builder:&nbsp;RelBuilder):&nbsp;RexNod</span><span class="mtk_3_1">e&nbsp;=&nbsp;</span><span class="mtk_3_14 mtkb">when</span><span class="mtk_3_1">&nbsp;(</span><span class="mtk_3_14 mtkb">this</span><span class="mtk_3_1">)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;BinaryOperation&nbsp;-&gt;&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;left&nbsp;=&nbsp;left.toRexNode(builder)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;right&nbsp;=&nbsp;right.toRexNode(builder)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;builder.call(operation,&nbsp;left,&nbsp;right)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;UnaryOperation&nbsp;-&gt;&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;operand&nbsp;=&nbsp;operand.toRexNode(builder)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;builder.call(operation,&nbsp;operand)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;COLUMN&nbsp;-&gt;&nbsp;builder.</span><span class="mtk_3_14 mtkb">field</span><span class="mtk_3_1">(name)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">is</span><span class="mtk_3_1">&nbsp;LITERAL&nbsp;-&gt;&nbsp;builder.literal(value)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">else</span><span class="mtk_3_1">&nbsp;-&gt;&nbsp;</span><span class="mtk_3_14 mtkb">throw</span><span class="mtk_3_1">&nbsp;Exception(</span><span class="mtk_3_8 mtkb">"Impossible"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_1">}</span></span><br></pre></div></div><div class="block markdown-block"><div class="markdown-output"><h1 id="4.-Create-a-Calcite-&quot;Relational-Expression&quot;-(RelNode)-from-a-combination-of-the-`WHERE`-&quot;RexNode&quot;-and-`SELECT`-&quot;RexNode&quot;">4. Create a Calcite "Relational Expression" (RelNode) from a combination of the <code>WHERE</code> "RexNode" and <code>SELECT</code> "RexNode"</h1>
<p>Now, we need to perform the meat of the functionality.</p>
<p>In order to create a full Relational Expression in Calcite, we need an underlying datasource and schema for it to be written against. In the <code>org.apache.test</code> namespace there is a class called <code>CalciteAssert</code> that can wire up a sample database to Calcite for you.</p>
<p>It's important to know what <code>CalciteAssert</code> is doing here. What is going to happen behind the scenes is:</p>
<ul>
<li>Calcite will initialize a JDBC connection, called <code>CalciteConnection</code></li>
<li>A "root schema" of type <code>SchemaPlus</code> will be created. This is the value that will hold all datasources.
<ul>
<li>The "root schema" will become available under <code>CaliteConnection.getRootSchema()</code></li>
<li>NOTE: You can manually create an empty "root schema" using <code>Frameworks.createRootSchema()</code></li>
</ul>
</li>
<li>The test database + schema will be added to the "root schema"</li>
</ul>
<p>Then we will use the <code>Frameworks</code> tool, to create a config object which initializes things like the Planner and many other necessary bits.</p>
</div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.jdbc.CalciteConnection</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.sql.dialect.CalciteSqlDialect</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.sql.parser.SqlParser</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.test.CalciteAssert</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.tools.Frameworks</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.tools.RelBuilder</span></span><br><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.rel.rel2sql.RelToSqlConverter</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Start&nbsp;by&nbsp;using&nbsp;"calcite-testkit"&nbsp;CalciteAssert&nbsp;</span><span class="mtk_3_3 mtki">to&nbsp;create&nbsp;a&nbsp;test&nbsp;JDBC&nbsp;schema&nbsp;and&nbsp;Calcite&nbsp;root&nbsp;sche</span><span class="mtk_3_3 mtki">ma</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;calciteAssert&nbsp;=&nbsp;CalciteAssert.that().with(Calcite</span><span class="mtk_3_1">Assert.SchemaSpec.JDBC_SCOTT)</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;connection&nbsp;=&nbsp;calciteAssert.connect()&nbsp;</span><span class="mtk_3_14 mtkb">as</span><span class="mtk_3_1">&nbsp;CalciteConnection</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Use&nbsp;the&nbsp;Framework&nbsp;utility,&nbsp;passing&nbsp;it&nbsp;the&nbsp;"conn</span><span class="mtk_3_3 mtki">ection.rootSchema"&nbsp;as&nbsp;the&nbsp;default&nbsp;schema</span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Make&nbsp;sure&nbsp;to&nbsp;set&nbsp;SqlParser.withCaseSensitive(fa</span><span class="mtk_3_3 mtki">lse)&nbsp;or&nbsp;else&nbsp;statements&nbsp;won't&nbsp;parse&nbsp;correctly</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;config&nbsp;=&nbsp;Frameworks.newConfigBuilder()</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;.defaultSchema(connection.rootSchema)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;.parserConfig(SqlParser.config().withCaseSensi</span><span class="mtk_3_1">tive(</span><span class="mtk_3_14 mtkb">false</span><span class="mtk_3_1">))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;.build()</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Create&nbsp;a&nbsp;Calcite&nbsp;"RelBuilder"&nbsp;using&nbsp;the&nbsp;Framewo</span><span class="mtk_3_3 mtki">rkConfig</span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;This&nbsp;RelBuilder&nbsp;has&nbsp;the&nbsp;context&nbsp;of&nbsp;our&nbsp;JDBC&nbsp;sch</span><span class="mtk_3_3 mtki">ema&nbsp;in&nbsp;it</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;relBuilder&nbsp;=&nbsp;RelBuilder.create(config)</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Convert&nbsp;GraphQL&nbsp;query&nbsp;to&nbsp;our&nbsp;"Expression"&nbsp;AST</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;whereArg&nbsp;=&nbsp;requireNotNull(getWhereArgumentFromGra</span><span class="mtk_3_1">phQLQuery(sampleQuery))</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;expression&nbsp;=&nbsp;graphqlWhereArgumentToExpression(whe</span><span class="mtk_3_1">reArg)</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Scan&nbsp;the&nbsp;"JDBC_SCOTT.EMP"&nbsp;table</span></span><br><span><span class="mtk_3_3 mtki">//</span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;-&nbsp;Filter&nbsp;by&nbsp;converting&nbsp;our&nbsp;"Expression"&nbsp;AST&nbsp;to</span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;&nbsp;&nbsp;a&nbsp;"RexNode"&nbsp;via&nbsp;the&nbsp;"RelBuilder"&nbsp;we&nbsp;initializ</span><span class="mtk_3_3 mtki">ed</span></span><br><span><span class="mtk_3_3 mtki">//</span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;-&nbsp;Select&nbsp;columns&nbsp;by&nbsp;iterating&nbsp;the&nbsp;GraphQL&nbsp;query</span><span class="mtk_3_3 mtki">&nbsp;selected</span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;&nbsp;&nbsp;fields&nbsp;and&nbsp;converting&nbsp;to&nbsp;"RelBuilder.field()"</span></span><br><span><span class="mtk_3_3 mtki">//</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;relRoot&nbsp;=&nbsp;relBuilder.scan(</span><span class="mtk_3_8 mtkb">"JDBC_SCOTT"</span><span class="mtk_3_1">,&nbsp;</span><span class="mtk_3_8 mtkb">"EMP"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;.filter(expression.toRexNode(relBuilder))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;.project(</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;getQuerySelectedFieldNames(sampleQuery).ma</span><span class="mtk_3_1">p&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;relBuilder.</span><span class="mtk_3_14 mtkb">field</span><span class="mtk_3_1">(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;.build()</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Print&nbsp;out&nbsp;the&nbsp;query&nbsp;(logical)&nbsp;plan</span></span><br><span><span class="mtk_3_1">println(relRoot.explain())</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Convert&nbsp;the&nbsp;RelNode&nbsp;of&nbsp;the&nbsp;query&nbsp;to&nbsp;equivalent&nbsp;</span><span class="mtk_3_3 mtki">SQL&nbsp;expression</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;sqlNode&nbsp;=&nbsp;RelToSqlConverter(CalciteSqlDialect.DEF</span><span class="mtk_3_1">AULT).visitRoot(relRoot).asStatement()</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Print&nbsp;the&nbsp;equivalent&nbsp;SQL&nbsp;to&nbsp;check&nbsp;that&nbsp;our&nbsp;new&nbsp;</span><span class="mtk_3_3 mtki">frontend&nbsp;works&nbsp;as&nbsp;we&nbsp;expect</span></span><br><span><span class="mtk_3_1">println(</span><span class="mtk_3_8 mtkb">"RelToSqlConverter&nbsp;result:&nbsp;"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_1">println(sqlNode.toSqlString(CalciteSqlDialect.DEFA</span><span class="mtk_3_1">ULT))</span></span><br></pre></div><div class="block-output datalore-block-output "><div><div class="publishing-text-output"><span>LogicalProject(EMPNO=[$0], ENAME=[$1], JOB=[$2], MGR=[$3], SAL=[$5], COMM=[$6], DEPTNO=[$7])</span><br><span>  LogicalFilter(condition=[AND(SEARCH($7, Sarg[20, 30]), &gt;=($5, 1500), SEARCH($2, Sarg['MANAGER':CHAR(8), 'SALESMAN']:CHAR(8)))])</span><br><span>    JdbcTableScan(table=[[JDBC_SCOTT, EMP]])</span><br><br><span>RelToSqlConverter result: </span><br><span>SELECT "EMPNO", "ENAME", "JOB", "MGR", "SAL", "COMM", "DEPTNO"</span><br><span>FROM "SCOTT"."EMP"</span><br><span>WHERE "DEPTNO" IN (20, 30) AND "SAL" &gt;= 1500 AND "JOB" IN ('MANAGER', 'SALESMAN')</span><br><br></div></div><div class="edge"></div></div></div><div class="block markdown-block"><div class="markdown-output"><h1 id="5.-Execute-the-RelNode-against-the-data-source-we-are-trying-to-query-against">5. Execute the RelNode against the data source we are trying to query against</h1>
</div></div><div class="block datalore"><div class="block_input"><pre class="static-editor has-scroll idea"><span><span class="mtk_3_14 mtkb">import</span><span class="mtk_3_1">&nbsp;org.apache.calcite.tools.RelRunner</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;We&nbsp;use&nbsp;the&nbsp;"RelRunner"&nbsp;class&nbsp;to&nbsp;execute&nbsp;RelNode</span><span class="mtk_3_3 mtki">&nbsp;expressions</span></span><br><span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;runner:&nbsp;RelRunner&nbsp;=&nbsp;connection.unwrap(RelRunner::</span><span class="mtk_3_14 mtkb">class</span><span class="mtk_3_1">.java)</span></span><br><span><span></span></span><br><span><span class="mtk_3_3 mtki">//&nbsp;Execute&nbsp;our&nbsp;query&nbsp;RelNode&nbsp;and&nbsp;print&nbsp;the&nbsp;results</span></span><br><span><span class="mtk_3_1">runner.prepareStatement(relRoot).executeQuery().le</span><span class="mtk_3_1">t&nbsp;{&nbsp;</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;md&nbsp;=&nbsp;</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.metaData</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">val</span><span class="mtk_3_1">&nbsp;columns&nbsp;=&nbsp;md.columnCount</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">while</span><span class="mtk_3_1">&nbsp;(</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.next())&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">for</span><span class="mtk_3_1">&nbsp;(i&nbsp;</span><span class="mtk_3_14 mtkb">in</span><span class="mtk_3_1">&nbsp;</span><span class="mtk_3_6">1</span><span class="mtk_3_1">..columns)&nbsp;{</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="mtk_3_14 mtkb">if</span><span class="mtk_3_1">&nbsp;(i&nbsp;&gt;&nbsp;</span><span class="mtk_3_6">1</span><span class="mtk_3_1">)&nbsp;print(</span><span class="mtk_3_8 mtkb">",&nbsp;&nbsp;"</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.</span><span class="mtk_3_14 mtkb">out</span><span class="mtk_3_1">.print(md.getColumnName(i)&nbsp;+&nbsp;</span><span class="mtk_3_8 mtkb">"&nbsp;"</span><span class="mtk_3_1">&nbsp;+&nbsp;</span><span class="mtk_3_14 mtkb">it</span><span class="mtk_3_1">.getString(i))</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;println(</span><span class="mtk_3_8 mtkb">""</span><span class="mtk_3_1">)</span></span><br><span><span class="mtk_3_1">&nbsp;&nbsp;&nbsp;&nbsp;}</span></span><br><span><span class="mtk_3_1">&nbsp;}</span></span><br></pre></div><div class="block-output datalore-block-output "><div><div class="publishing-text-output"><span>EMPNO 7499,  ENAME ALLEN,  JOB SALESMAN,  MGR 7698,  SAL 1600.00,  COMM 300.00,  DEPTNO 30</span><br><span>EMPNO 7566,  ENAME JONES,  JOB MANAGER,  MGR 7839,  SAL 2975.00,  COMM null,  DEPTNO 20</span><br><span>EMPNO 7698,  ENAME BLAKE,  JOB MANAGER,  MGR 7839,  SAL 2850.00,  COMM null,  DEPTNO 30</span><br><span>EMPNO 7844,  ENAME TURNER,  JOB SALESMAN,  MGR 7698,  SAL 1500.00,  COMM 0.00,  DEPTNO 30</span><br><br></div></div><div class="edge"></div></div></div><div class="block datalore"></div></div></div></div></div></div></div><div class="icon-container"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-access">  <path d="M11 3a3 3 0 1 1-6 0 3 3 0 0 1 6 0zM11.234 7a2 2 0 0 1 1.985 1.752l.032.255A4.5 4.5 0 0 0 9.256 15H2l.781-6.248A2 2 0 0 1 4.766 7h6.468zM13 11h1v2h2v1h-2v2h-1v-2h-2v-1h2v-2z"></path></symbol><symbol viewBox="0 0 36 36" xmlns="http://www.w3.org/2000/svg" id="icon-add-blue"><path d="M18 36C27.9411 36 36 27.9411 36 18C36 8.05887 27.9411 0 18 0C8.05887 0 0 8.05887 0 18C0 27.9411 8.05887 36 18 36Z" fill="#008DC0"></path><path d="M26 10H10V26H26V10Z" fill="#008DC0"></path><path d="M19 12H17V17H12V19H17V24H19V19H24V17H19V12Z" fill="white"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-add-database"><path d="M13.724 6.251A6 6 0 0 0 12 6c-1.773 0-3.367.77-4.466 1.993C4.438 7.893 2 6.815 2 5.5v-1C2 3.12 4.686 2 8 2s6 1.12 6 2.5v1c0 .262-.097.514-.276.751zM6.828 8.957a5.961 5.961 0 0 0-.722 1.916C3.72 10.543 2 9.605 2 8.5v-1c0-.032.001-.064.004-.096 1.04.856 2.794 1.402 4.824 1.553zM6 11.872V12c0 .664.108 1.302.307 1.9C3.817 13.594 2 12.635 2 11.5v-1c0-.032.001-.064.004-.096.896.738 2.321 1.245 3.997 1.468zM11 11V8h2v3h3v2h-3v3h-2v-3H8v-2h3z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-add-folder">  <path d="M9 4h6v2H1V2h7l1 2zM1 7v7h8.027A4.5 4.5 0 0 1 15 9.256V7H1zM13 13v-2h1v2h2v1h-2v2h-1v-2h-2v-1h2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-add-meerkat-wb"><path clip-rule="evenodd" d="M2 15V5h5V0h7v9.027A4.5 4.5 0 0 0 9.256 15H2zm2.5-2.5v1l.5.5h1l.5-.5v-1h-2zm2.77-2.223C7.612 9.727 8 9.105 8 8.5a2.5 2.5 0 0 0-5 0c0 .605.387 1.227.73 1.777l.095.147.132.199c.257.384.543.811.543 1.044V12h2v-.333c0-.233.286-.66.543-1.044.081-.122.16-.24.226-.346z"></path><path d="M2 4l4-4v4H2zm9 9h2v-2h1v2h2v1h-2v2h-1v-2h-2v-1z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-add-sheet">  <path d="M9 2H7v5H2v2h5v5h2V9h5V7H9V2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-add-wb">  <path fill-rule="evenodd" clip-rule="evenodd" d="M2 5v10h7.256a4.493 4.493 0 0 1-.229-2H4v-2h5.758A4.496 4.496 0 0 1 14 9.027V0H7v5H2zm6-2h4v2H8V3zm4 6V7H4v2h8z"></path>  <path d="M6 0L2 4h4V0zM14 11h-1v2h-2v1h2v2h1v-2h2v-1h-2v-2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-add">  <path d="M9 2H7v5H2v2h5v5h2V9h5V7H9V2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-arrow"><path d="M5 14L6 15L13 8L6 1L5 2L11 8L5 14Z"></path></symbol><symbol viewBox="0 0 11 22" xmlns="http://www.w3.org/2000/svg" id="icon-attach">  <path d="M4.5 4.75C4.5 4.33579 4.1642 4 3.75 4C3.3358 4 3 4.33579 3 4.75H4.5ZM10.5 4.75C10.5 4.33579 10.1642 4 9.75 4C9.3358 4 9 4.33579 9 4.75H10.5ZM3 4.75V16.25H4.5V4.75H3ZM7.5 16.25V3.75H6V16.25H7.5ZM0 3.75V16.25H1.5V3.75H0ZM10.5 16.25V4.75H9V16.25H10.5ZM5.25 21.5C8.1495 21.5 10.5 19.1495 10.5 16.25H9C9 18.3211 7.3211 20 5.25 20V21.5ZM0 16.25C0 19.1495 2.3505 21.5 5.25 21.5V20C3.1789 20 1.5 18.3211 1.5 16.25H0ZM3.75 0C1.6789 0 0 1.67893 0 3.75H1.5C1.5 2.50736 2.5074 1.5 3.75 1.5V0ZM7.5 3.75C7.5 1.67893 5.8211 0 3.75 0V1.5C4.9926 1.5 6 2.50736 6 3.75H7.5ZM5.25 18.5C6.4926 18.5 7.5 17.4926 7.5 16.25H6C6 16.6642 5.6642 17 5.25 17V18.5ZM3 16.25C3 17.4926 4.0074 18.5 5.25 18.5V17C4.8358 17 4.5 16.6642 4.5 16.25H3Z"></path></symbol><symbol viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" id="icon-attention"> <g>  <g id="svg_1">   <g id="XMLID_47_">    <g id="svg_2">     <g id="svg_3">      <path d="m31.80952,0c17.7,0 32,14.3 32,32s-14.3,32 -32,32s-32,-14.3 -32,-32s14.3,-32 32,-32z" id="svg_4"></path>     </g>    </g>   </g>   <g stroke="null" id="svg_5">    <g stroke="null" id="svg_6">     <g stroke="null" id="svg_7">      <polygon fill="#FFFFFF" points="24.76654054224491,10.768653854727745 39.04298593103886,10.768653854727745 36.66357995569706,36.982568725943565 27.14594842493534,36.982568725943565 " id="svg_8"></polygon>     </g>    </g>    <g stroke="null" id="svg_9">     <g stroke="null" id="svg_10">      <circle fill="#FFFFFF" cx="31.904762" cy="47.468131" r="5.242783" id="svg_11"></circle>     </g>    </g>   </g>  </g> </g></symbol><symbol viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" id="icon-avatar-placeholder"><circle cx="12" cy="12" r="12" fill="#E5E5E5"></circle><path fill-rule="evenodd" clip-rule="evenodd" d="M12 12a4 4 0 1 0 0-8 4 4 0 0 0 0 8zm0 12c3.294 0 6.278-1.327 8.447-3.476l-.642-5.19C19.582 13.993 18.322 13 16.84 13h-1.522c-.95.632-2.091 1-3.318 1a5.973 5.973 0 0 1-3.318-1H7.16c-1.482 0-2.742.992-2.966 2.335l-.64 5.189A11.962 11.962 0 0 0 12 24z" fill="#B3B3B3"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-breadcrumb-sep">    <g fill="none" fill-rule="nonzero">        <path fill="#000" d="M6 11l1 1 4-4-4-4-1 1 3 3z"></path>    </g></symbol><symbol viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg" id="icon-calendar"> <g>  <rect id="svg_1" height="9.773228" width="34" y="3" x="3" stroke-width="0" stroke="#000"></rect>  <rect stroke="#000" id="svg_2" height="10" width="9.86502" y="15" x="3" stroke-width="0" opacity="0.7"></rect>  <rect id="svg_3" height="9.616856" width="10" y="15" x="14.927798" stroke-width="0" stroke="#000" opacity="0.7"></rect>  <rect id="svg_4" height="9.616856" width="10" y="27" x="3" stroke-width="0" stroke="#000" opacity="0.7"></rect>  <rect id="svg_5" height="9.616856" width="10" y="15" x="27" stroke-width="0" stroke="#000" opacity="0.7"></rect>  <rect id="svg_6" height="9.616856" width="10" y="27" x="15" stroke-width="0" stroke="#000" opacity="0.7"></rect>  <rect id="svg_7" height="9.616856" width="10" y="27" x="27" stroke-width="0" stroke="#000" opacity="0.7"></rect> </g></symbol><symbol viewBox="0 0 10 8" xmlns="http://www.w3.org/2000/svg" id="icon-caret">  <path id="path0_fill" d="M 1 0L 0 0L 4 4L 0 8L 1 8L 5 4L 1 0Z" transform="translate(7.000000, 4.000000) scale(-1, -1) rotate(90.000000) translate(-7.000000, -4.000000) translate(4.000000, -2.000000)"></path></symbol><symbol viewBox="0 0 8 6" xmlns="http://www.w3.org/2000/svg" id="icon-check-mark-light"><desc>Created using Figma</desc><g id="Canvas" transform="translate(-14208 -23681)"><g id="Vector 2"><use xlink:href="#path0_stroke" transform="translate(14209.1 23681.7)" fill="#FFFFFF"></use></g></g><defs><path id="path0_stroke" d="M 1.75 4.08333L 1.21967 4.61366L 1.75 5.14399L 2.28033 4.61366L 1.75 4.08333ZM -0.53033 2.86366L 1.21967 4.61366L 2.28033 3.553L 0.53033 1.803L -0.53033 2.86366ZM 2.28033 4.61366L 6.36366 0.53033L 5.303 -0.53033L 1.21967 3.553L 2.28033 4.61366Z"></path></defs></symbol><symbol viewBox="0 0 8 6" xmlns="http://www.w3.org/2000/svg" id="icon-check-mark"><desc>Created using Figma</desc><g id="Canvas" transform="translate(-14208 -23681)"><g id="Vector 2"><use xlink:href="#path0_stroke" transform="translate(14209.1 23681.7)"></use></g></g><defs><path id="path0_stroke" d="M 1.75 4.08333L 1.21967 4.61366L 1.75 5.14399L 2.28033 4.61366L 1.75 4.08333ZM -0.53033 2.86366L 1.21967 4.61366L 2.28033 3.553L 0.53033 1.803L -0.53033 2.86366ZM 2.28033 4.61366L 6.36366 0.53033L 5.303 -0.53033L 1.21967 3.553L 2.28033 4.61366Z"></path></defs></symbol><symbol viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg" id="icon-checkbox-checked-focused">  <g filter="url(#filter0_i)">    <path fill-rule="evenodd" clip-rule="evenodd" d="M1 2C1 1.44772 1.44772 1 2 1H12C12.5523 1 13 1.44772 13 2V12C13 12.5523 12.5523 13 12 13H2C1.44772 13 1 12.5523 1 12V2Z" fill="white"></path>  </g>  <path fill-rule="evenodd" clip-rule="evenodd" d="M1 2C1 1.44772 1.44772 1 2 1H12C12.5523 1 13 1.44772 13 2V12C13 12.5523 12.5523 13 12 13H2C1.44772 13 1 12.5523 1 12V2Z" stroke="#0068BE"></path>  <path d="M3 6L6 9L11 4" stroke="#008DC0" stroke-width="2"></path>  <defs>    <filter id="filter0_i" x="0.5" y="0.5" width="13" height="14" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">      <feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood>      <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend>      <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 255 0" result="hardAlpha"></feColorMatrix>      <feOffset dy="1"></feOffset>      <feGaussianBlur stdDeviation="1"></feGaussianBlur>      <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1"></feComposite>      <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"></feColorMatrix>      <feBlend mode="normal" in2="shape" result="effect1_innerShadow"></feBlend>    </filter>  </defs></symbol><symbol viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg" id="icon-checkbox-checked">  <g filter="url(#filter0_i)">    <path fill-rule="evenodd" clip-rule="evenodd" d="M1 2C1 1.44772 1.44772 1 2 1H12C12.5523 1 13 1.44772 13 2V12C13 12.5523 12.5523 13 12 13H2C1.44772 13 1 12.5523 1 12V2Z" fill="white"></path>  </g>  <path fill-rule="evenodd" clip-rule="evenodd" d="M1 2C1 1.44772 1.44772 1 2 1H12C12.5523 1 13 1.44772 13 2V12C13 12.5523 12.5523 13 12 13H2C1.44772 13 1 12.5523 1 12V2Z" stroke="#B3B3B3"></path>  <path d="M3 6L6 9L11 4" stroke="#008DC0" stroke-width="2"></path>  <defs>    <filter id="filter0_i" x="0.5" y="0.5" width="13" height="14" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">      <feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood>      <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend>      <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 255 0" result="hardAlpha"></feColorMatrix>      <feOffset dy="1"></feOffset>      <feGaussianBlur stdDeviation="1"></feGaussianBlur>      <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1"></feComposite>      <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"></feColorMatrix>      <feBlend mode="normal" in2="shape" result="effect1_innerShadow"></feBlend>    </filter>  </defs></symbol><symbol viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg" id="icon-checkbox-empty-focused">  <g filter="url(#filter0_i)">    <path fill-rule="evenodd" clip-rule="evenodd" d="M1 2C1 1.44772 1.44772 1 2 1H12C12.5523 1 13 1.44772 13 2V12C13 12.5523 12.5523 13 12 13H2C1.44772 13 1 12.5523 1 12V2Z" fill="white"></path>  </g>  <path fill-rule="evenodd" clip-rule="evenodd" d="M1 2C1 1.44772 1.44772 1 2 1H12C12.5523 1 13 1.44772 13 2V12C13 12.5523 12.5523 13 12 13H2C1.44772 13 1 12.5523 1 12V2Z" stroke="#0068BE"></path>  <defs>    <filter id="filter0_i" x="0.5" y="0.5" width="13" height="14" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">      <feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood>      <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend>      <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 255 0" result="hardAlpha"></feColorMatrix>      <feOffset dy="1"></feOffset>      <feGaussianBlur stdDeviation="1"></feGaussianBlur>      <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1"></feComposite>      <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"></feColorMatrix>      <feBlend mode="normal" in2="shape" result="effect1_innerShadow"></feBlend>    </filter>  </defs></symbol><symbol viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg" id="icon-checkbox-empty">  <g filter="url(#filter0_i)">    <path fill-rule="evenodd" clip-rule="evenodd" d="M1 2C1 1.44772 1.44772 1 2 1H12C12.5523 1 13 1.44772 13 2V12C13 12.5523 12.5523 13 12 13H2C1.44772 13 1 12.5523 1 12V2Z" fill="white"></path>  </g>  <path fill-rule="evenodd" clip-rule="evenodd" d="M1 2C1 1.44772 1.44772 1 2 1H12C12.5523 1 13 1.44772 13 2V12C13 12.5523 12.5523 13 12 13H2C1.44772 13 1 12.5523 1 12V2Z" stroke="#B3B3B3"></path>  <defs>    <filter id="filter0_i" x="0.5" y="0.5" width="13" height="14" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">      <feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood>      <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend>      <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 255 0" result="hardAlpha"></feColorMatrix>      <feOffset dy="1"></feOffset>      <feGaussianBlur stdDeviation="1"></feGaussianBlur>      <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1"></feComposite>      <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"></feColorMatrix>      <feBlend mode="normal" in2="shape" result="effect1_innerShadow"></feBlend>    </filter>  </defs></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-checkmark-green"><path d="M2 8l2-2 3 3 6-6 2 2-8 8-5-5z" fill="#369711"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-clone">  <path d="M4 1V0h12v14h-4V1H4zm0 1L0 6h4V2z"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M5 2v5H0v9h11V2H5zm1 2h3v2H6V4zm3 4H2v2h7V8zm-7 4h7v2H2v-2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-close">  <path d="M13 2l1 1-5 5 5 5-1 1-5-5-5 5-1-1 5-5-5-5 1-1 5 5 5-5z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-collaboration">  <path fill-rule="evenodd" clip-rule="evenodd" d="M12 6a3 3 0 10-2.959-2.5L4.987 5.752a3 3 0 100 4.496L9.04 12.5a3 3 0 10.972-1.748L5.96 8.5a3.02 3.02 0 000-1l4.054-2.252C10.543 5.716 11.238 6 12 6zM3 9a1 1 0 100-2 1 1 0 000 2zm10-6a1 1 0 11-2 0 1 1 0 012 0zm-1 11a1 1 0 100-2 1 1 0 000 2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-collapse-block"><path d="M8 10l3 3H5l3-3zm6-3v2H2V7h12zm-3-4L8 6 5 3h6z" fill="#000"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-collapse-expand"><path fill="#000" fill-rule="nonzero" d="M2 5L1 6l7 7 7-7-1-1-6 6z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-collapse">  <path d="M 4.5 7 v 5.5 h 7 v -5.5 l -3.5 -3.5 Z" stroke-width="1"></path>  <path d="M 6 9 h 4 Z" stroke-width="1"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-column"><path d="M10 1H6V14H10V1Z"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M1 2H5V14H1V2ZM2 7V5H4V7H2ZM2 13H4V11H2V13ZM4 8V10H2V8H4Z"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M11 2V14H15V2H11ZM14 13H12V11H14V13ZM14 10H12V8H14V10ZM14 7H12V5H14V7Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-comments">  <path d="M0 15V3a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H3l-3 3zm12-7a1 1 0 1 0 0-2 1 1 0 0 0 0 2zM8 8a1 1 0 1 0 0-2 1 1 0 0 0 0 2zM4 8a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-control-date"><path d="M5 1H3V5H5V1Z"></path><path d="M13 1H11V5H13V1Z"></path><path d="M1 3H2L2 14L14 14V3H15L15 15L1 15V3Z"></path><path d="M6 4L10 4V3L6 3V4Z"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M3 6H13V13H3V6ZM6 9V7H4V9H6ZM6 12V10H4V12H6ZM7 7H9V9H7V7ZM9 10H7V12H9V10ZM10 9V7H12V9H10ZM12 12V10H10V12H12Z" fill="black"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-control-dropdown"><path d="M14 2H1V1H15V15H1V14H14V2Z"></path><path d="M8 10L11 7H5L8 10Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-control-number"><path d="M2 14L15 14V15L1 15L1 1L15 1L15 2L2 2L2 14Z"></path><path d="M4.632 10.088V11H8.28V10.096H5.848L7.048 8.90399C7.45333 8.50932 7.74667 8.14399 7.928 7.80799C8.11467 7.47199 8.208 7.12532 8.208 6.76799C8.208 6.42665 8.13333 6.13065 7.984 5.87999C7.83467 5.62399 7.624 5.42665 7.352 5.28799C7.08 5.14932 6.76 5.07999 6.392 5.07999C6.008 5.07999 5.672 5.15465 5.384 5.30399C5.096 5.45332 4.872 5.66399 4.712 5.93599C4.55733 6.20265 4.47733 6.52265 4.472 6.89599H5.472C5.472 6.60799 5.552 6.38399 5.712 6.22399C5.872 6.05865 6.09333 5.97599 6.376 5.97599C6.632 5.97599 6.83467 6.05332 6.984 6.20799C7.13333 6.36265 7.208 6.57332 7.208 6.83999C7.208 7.06399 7.14667 7.28265 7.024 7.49599C6.90133 7.70399 6.712 7.93865 6.456 8.19999L4.632 10.088Z"></path><path d="M9.46887 10.12V11H13.2129V10.12H11.9889V5.15999H10.8049L9.46087 6.12799V7.18399L10.9889 6.04799V10.12H9.46887Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-control-plot">  <path d="M2 14L15 14V15L1 15L1 1L2 1V2L2 14Z"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M15.208 2.83747L9.99126 10.2961L7.59803 8.58486L5.03163 12.1593L3.40701 10.9929L7.13757 5.79696L9.51063 7.49374L13.5691 1.69118L15.208 2.83747Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-control-slider"><path fill-rule="evenodd" clip-rule="evenodd" d="M11 8C11 9.65685 9.65685 11 8 11C6.34315 11 5 9.65685 5 8C5 6.34315 6.34315 5 8 5C9.65685 5 11 6.34315 11 8ZM10 8C10 9.10457 9.10457 10 8 10C6.89543 10 6 9.10457 6 8C6 6.89543 6.89543 6 8 6C9.10457 6 10 6.89543 10 8Z"></path><path d="M12 8C12 8.3453 11.9562 8.68038 11.874 9H14C14.5523 9 15 8.55229 15 8C15 7.44772 14.5523 7 14 7H11.874C11.9562 7.31962 12 7.6547 12 8Z"></path><path d="M2 9H4.12602C4.04375 8.68038 4 8.3453 4 8C4 7.6547 4.04375 7.31962 4.12602 7H2C1.44772 7 1 7.44772 1 8C1 8.55229 1.44772 9 2 9Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-control-text"><path fill-rule="evenodd" clip-rule="evenodd" d="M2 14L13 14H14H15V15L1 15V1H15L15 2H14H13L2 2L2 14ZM5.75203 5.16L4.28003 11H5.30403L5.62403 9.584H7.17603L7.49603 11H8.52003L7.04003 5.16H5.75203ZM6.64003 7.2L6.99203 8.768H5.80803L6.16003 7.192C6.2187 6.936 6.26936 6.704 6.31203 6.496C6.3547 6.28267 6.38403 6.128 6.40003 6.032C6.41603 6.128 6.44536 6.28267 6.48803 6.496C6.5307 6.704 6.58136 6.93867 6.64003 7.2ZM9.4129 5.16V11H11.2929C11.8742 11 12.3329 10.8507 12.6689 10.552C13.0102 10.248 13.1809 9.84267 13.1809 9.336C13.1809 8.93067 13.0662 8.608 12.8369 8.368C12.6129 8.12267 12.3249 7.97867 11.9729 7.936C12.2876 7.88267 12.5436 7.744 12.7409 7.52C12.9436 7.296 13.0449 7.01067 13.0449 6.664C13.0449 6.2 12.8796 5.83467 12.5489 5.568C12.2182 5.296 11.7702 5.16 11.2049 5.16H9.4129ZM11.1889 7.568H10.3889V5.992H11.1889C11.4556 5.992 11.6636 6.064 11.8129 6.208C11.9676 6.34667 12.0449 6.536 12.0449 6.776C12.0449 7.02134 11.9676 7.216 11.8129 7.36C11.6582 7.49867 11.4502 7.568 11.1889 7.568ZM11.2289 10.168H10.3889V8.376H11.2289C11.5222 8.376 11.7516 8.46134 11.9169 8.632C12.0876 8.79734 12.1729 9.016 12.1729 9.288C12.1729 9.56 12.0876 9.776 11.9169 9.936C11.7516 10.0907 11.5222 10.168 11.2289 10.168Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-convert">  <path fill-rule="nonzero" d="M9 0h2v3H9a4 4 0 0 0-4 4h2l-3.5 4L0 7h2a7 7 0 0 1 7-7zM7 16H5v-3h2a4 4 0 0 0 4-4H9l3.5-4L16 9h-2a7 7 0 0 1-7 7z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-copy-clipboard"><path d="M10 2a1 1 0 00-1-1H2a1 1 0 00-1 1v9a1 1 0 001 1h2v-2H3V3h7V2z"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M5 5a1 1 0 011-1h7a1 1 0 011 1v9a1 1 0 01-1 1H6a1 1 0 01-1-1V5zm2 8V6h5v7H7z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-copy">  <path d="M6 5L13 5V14H6L6 5Z" fill="none" stroke="white" stroke-width="2"></path>  <path d="M9 1C9.55229 1 10 1.44772 10 2V3H3V10H4V12H2C1.44772 12 1 11.5523 1 11V2C1 1.44771 1.44772 1 2 1H9Z" fill="white"></path></symbol><symbol viewBox="0 0 14 15" xmlns="http://www.w3.org/2000/svg" id="icon-create">  <path d="M7 4L2 9L5 9L5 15L9 15L9 9L12 9L7 4ZM14 2L14 0L1.31134e-06 -1.22392e-06L1.1365e-06 2L14 2Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-database"><path d="M2 5.5v-1C2 3.12 4.686 2 8 2s6 1.12 6 2.5v1C14 6.88 11.314 8 8 8S2 6.88 2 5.5zm.004 1.904C3.24 8.422 5.483 9 8 9c2.517 0 4.76-.578 5.996-1.596.003.032.004.064.004.096v1c0 1.38-2.686 2.5-6 2.5S2 9.88 2 8.5v-1c0-.032.001-.064.004-.096zm0 3C3.24 11.422 5.483 12 8 12c2.517 0 4.76-.578 5.996-1.596.003.032.004.064.004.096v1c0 1.38-2.686 2.5-6 2.5s-6-1.12-6-2.5v-1c0-.032.001-.064.004-.096z"></path></symbol><symbol viewBox="0 0 36 36" xmlns="http://www.w3.org/2000/svg" id="icon-datalore-kernel-logo">  <path fill-rule="evenodd" clip-rule="evenodd" d="M18 33c6.075 0 11-.448 11-1s-4.925-1-11-1-11 .448-11 1 4.925 1 11 1z" fill="#9E9E9E" fill-opacity=".5" filter="url(#filter0_f)"></path>  <path d="M18.419 3l10.35 5.98c-3.01-1.609-7.436-1.557-10.93-.346-2.877.998-4.627 3.654-5.308 6.366a4.353 4.353 0 0 1-.26-1.413c-.043-4.158 1.235-7.742 6.023-10.517L18.42 3z" fill="#69BD48"></path>  <path d="M12.503 15l.017-.018.003-.002v-.003a4.32 4.32 0 0 1-.26-1.405c-.044-4.134 1.231-7.698 6.006-10.457L8 8.991v.023c.92 1.524 2.515 4.02 4.503 5.986z" fill="#ADD361"></path>  <path d="M18.35 27L8 21.02c3.01 1.609 7.437 1.557 10.93.346 2.878-.998 4.627-3.654 5.308-6.366.165.453.253.931.261 1.413.043 4.157-1.236 7.742-6.024 10.516L18.35 27z" fill="#6283C2"></path>  <path d="M24.267 15l-.018.018-.002.002v.003c.164.45.252.926.26 1.405.043 4.134-1.232 7.698-6.007 10.457l10.27-5.875v-.024c-.92-1.524-2.515-4.02-4.503-5.986z" fill="#6F57A4"></path>  <path d="M8 9c1.72 2.855 5.791 9.1 10.383 8.976h.012c2.123.058 4.146-1.258 5.874-2.967v.003c-.682 2.713-2.435 5.371-5.318 6.37-3.5 1.211-7.936 1.263-10.951-.346V9z" fill="#29B2E7"></path>  <path d="M28.77 21c-1.72-2.855-5.792-9.1-10.384-8.976h-.011c-2.124-.057-4.146 1.257-5.875 2.967v-.003c.682-2.713 2.435-5.371 5.319-6.37 3.499-1.211 7.935-1.263 10.95.346V21z" fill="#00A677"></path>  <defs>    <filter id="filter0_f" x="4.282" y="28.282" width="27.437" height="7.437" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">      <feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood>      <feBlend in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend>      <feGaussianBlur stdDeviation="1.359" result="effect1_foregroundBlur"></feGaussianBlur>    </filter>  </defs></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-datalore-kernel">  <path fill-rule="evenodd" clip-rule="evenodd" d="M8 2L13 5V11L8 14L3 11V5L8 2ZM8 9.5C9.10457 9.5 10.1046 9 11 8C10.1046 7 9.10457 6.5 8 6.5C6.89543 6.5 5.89543 7 5 8C5.89543 9 6.89543 9.5 8 9.5Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-delete">  <path fill-rule="evenodd" clip-rule="evenodd" d="M8 15A7 7 0 1 0 8 1a7 7 0 0 0 0 14zM4 5l1-1 3 3 3-3 1 1-3 3 3 3-1 1-3-3-3 3-1-1 3-3-3-3z"></path></symbol><symbol viewBox="0 0 80 16" xmlns="http://www.w3.org/2000/svg" id="icon-diff-view-modes">  <use xlink:href="#a" transform="translate(0 1)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(0 4)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(0 7)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(0 10)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(0 13)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(9 1)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(9 4)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(9 7)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(9 10)" fill="#FFF"></use>  <use xlink:href="#a" transform="translate(9 13)" fill="#FFF"></use>  <g>    <use xlink:href="#b" transform="translate(25 1)" fill="#5E5E5E"></use>    <use xlink:href="#b" transform="translate(25 4)" fill="#5E5E5E"></use>    <use xlink:href="#b" transform="translate(25 7)" fill="#5E5E5E"></use>    <use xlink:href="#b" transform="translate(25 10)" fill="#5E5E5E"></use>    <use xlink:href="#b" transform="translate(25 13)" fill="#5E5E5E"></use>  </g>  <g>    <use xlink:href="#a" transform="translate(40 1)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(40 4)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(40 7)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(40 10)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(40 13)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(49 1)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(49 4)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(49 7)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(49 10)" fill="#5E5E5E"></use>    <use xlink:href="#a" transform="translate(49 13)" fill="#5E5E5E"></use>    <g>      <use xlink:href="#b" transform="translate(65 1)" fill="#FFF"></use>      <use xlink:href="#b" transform="translate(65 4)" fill="#FFF"></use>      <use xlink:href="#b" transform="translate(65 7)" fill="#FFF"></use>      <use xlink:href="#b" transform="translate(65 10)" fill="#FFF"></use>      <use xlink:href="#b" transform="translate(65 13)" fill="#FFF"></use>    </g>  </g>  <defs>    <path id="a" d="M0 0h7v2H0V0z"></path>    <path id="b" d="M0 0h14v2H0V0z"></path>  </defs></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-document"><path d="M8.5 8H11v1.5H8.5V8zM5 12v-1.5h2.5V12H5zM5 9.5h2.5V8H5v1.5zM8.5 12v-1.5H11V12H8.5z"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M14 15H2V5h4V1h8v14zM4 13h8V7H4v6z"></path><path d="M5 4H2l3-3v3z"></path></symbol><symbol viewBox="0 0 26 26" xmlns="http://www.w3.org/2000/svg" id="icon-dots">    <!-- Generator: Sketch 41.2 (35397) - http://www.bohemiancoding.com/sketch -->    <g id="Assets" stroke-width="1" fill-rule="evenodd">        <circle id="Oval" cx="3" cy="13" r="3"></circle>        <circle id="Oval" cx="13" cy="13" r="3"></circle>        <circle id="Oval" cx="23" cy="13" r="3"></circle>    </g></symbol><symbol viewBox="0 0 8 12" xmlns="http://www.w3.org/2000/svg" id="icon-down"><path d="M4 12L-0.00039577 6.52202L2.5 6.52799L2.5 1.5988e-07L5.52828 0.00114544L5.5 6.5L7.9996 6.52799L4 12Z" fill="#010101"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-download">  <path d="M13 6l-5 5-5-5h3V0h4v6h3zm2 9v-2H1v2h14z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-edit">  <path fill-rule="evenodd" clip-rule="evenodd" d="M11.293 1.707L10 3 4 9l3 3 6-6 1.293-1.293a1 1 0 0 0 0-1.414l-1.586-1.586a1 1 0 0 0-1.414 0zM3 10l3 3-4 1 1-4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-embed">  <path d="M10 4l1-1 5 5-5 5-1-1 4-4-4-4zM6 4L2 8l4 4-1 1-5-5 5-5 1 1z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-envelope">  <g>    <path d="M8 7L0 3V2h16v1L8 7z"></path>    <path d="M0 5l8 4 8-4v9H0V5z"></path>  </g></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-expand">  <path d="M 4.5 4.5 h 7 v 7 h -7 Z" stroke-width="1"></path>  <path d="M 6 8 h 4 Z" stroke-width="1"></path>  <path d="M 8 6 v 4 Z" stroke-width="1"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-export">  <path fill-rule="evenodd" clip-rule="evenodd" d="M2 15V5h5V0h7v9.027A4.496 4.496 0 0 0 9.758 11H4v2h5.027a4.547 4.547 0 0 0 .23 2H2zM12 3H8v2h4V3zm0 4v2H4V7h8z"></path>  <path d="M2 4l4-4v4H2zM13.5 16L11 13h2v-3h1v3h2l-2.5 3z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-facebook-mask">  <path d="M9.193 16V8.702h2.358l.354-2.845H9.193V4.041c0-.823.22-1.384 1.357-1.384H12V.111A18.673 18.673 0 0 0 9.887 0c-2.09 0-3.522 1.326-3.522 3.76v2.097H4v2.845h2.365V16h2.828z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-fav">  <path fill-rule="evenodd" clip-rule="evenodd" d="M8 13l6 3V0H2v16l6-3zm-4 0l4-2 4 2V2H4v11z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-favourite-alt">  <path d="M11 2a4 4 0 0 1 3.711 5.495l.001-.001L14.5 8h-.035V8L14.5 8c-.616 1.184-2.783 3.184-6.5 6-3.597-2.725-5.743-4.686-6.436-5.883L1.5 8l.036.001L1.534 8 1.5 8l-.212-.506A4 4 0 0 1 8 3.355 3.983 3.983 0 0 1 11 2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-feedback"><path d="M10 12l-4 3v-3H4a3 3 0 0 1-3-3V4a3 3 0 0 1 3-3h8a3 3 0 0 1 3 3v5a3 3 0 0 1-3 3h-2zm-2-1a1 1 0 1 0 0-2 1 1 0 0 0 0 2zM7 3v1l.5 4h1L9 4V3H7z" fill-rule="evenodd"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-file-fetched">  <path d="M14 1H6v4H2v10h4.803A6 6 0 0114 6.341V1z"></path>  <path d="M2 4l3-3v3H2zM12.646 11.94l.647-.647a1.829 1.829 0 00-2.586-2.586l-.646.647-.707-.708L10 8a2.828 2.828 0 114 4l-.646.646-.708-.707zM11.94 12.646l-.647.647a1.829 1.829 0 01-2.586-2.586l.647-.646-.708-.707L8 10a2.828 2.828 0 104 4l.646-.646-.707-.708z"></path>  <path d="M12.354 9.646a.5.5 0 010 .708l-2 2a.5.5 0 01-.708-.708l2-2a.5.5 0 01.708 0z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-file">  <path d="M2 15h12V1H6v4H2v10z"></path>  <path d="M2 4h3V1L2 4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-flyout">        <path d="M4 6h8l-4 4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-fold-cell"><path fill-rule="evenodd" clip-rule="evenodd" d="M12 3H4v6l4 4 4-4V3z" fill="#fff"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M5 4h6v4.586l-3 3-3-3V4zm3 9l4-4V3H4v6l4 4zm2-6.5H6v1h4v-1z" fill="#C5C5C5"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-folder-alt">        <path d="M1 2h6l1 2h7v10H1V2zm1 1v10h12V5H7.382l-1-2H2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-folder">  <path d="M9 4h6v2H1V2h7l1 2zM1 7v7h14V7H1z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-good-connection"><path fill-rule="evenodd" clip-rule="evenodd" d="M0 10.5c0 1.21.859 2.218 2 2.45V13h11a3 3 0 00.864-5.874 1.5 1.5 0 00-1.96-2.003A4.001 4.001 0 004.12 5.02 3.5 3.5 0 001 8.5c-.607.456-1 1.182-1 2zM10 6l1 1-4 4-2.5-2.5 1-1L7 9l3-3z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-help"><path fill-rule="evenodd" clip-rule="evenodd" d="M8 0C3.58172 0 0 3.58172 0 8C0 12.4183 3.58172 16 8 16C12.4183 16 16 12.4183 16 8C16 3.58172 12.4183 0 8 0ZM6.82369 5.83311H5C5.03365 4.15747 6.20458 3 8.27052 3C10.1952 3 11.467 4.06999 11.467 5.6245C11.467 6.63392 10.9758 7.34051 10.0269 7.89906C9.1319 8.41723 8.88291 8.74697 8.88291 9.393V9.74966H7.0996L7.08614 9.37954C6.99865 8.30283 7.36878 7.69717 8.29744 7.15209C9.16555 6.63392 9.42799 6.3109 9.42799 5.68506C9.42799 5.05922 8.91655 4.61507 8.14939 4.61507C7.3755 4.61507 6.86406 5.09287 6.82369 5.83311ZM9.27995 11.856C9.27995 12.5626 8.81561 13 8.06191 13C7.30821 13 6.83715 12.5626 6.83715 11.856C6.83715 11.1427 7.30821 10.7052 8.06191 10.7052C8.81561 10.7052 9.27995 11.1427 9.27995 11.856Z"></path></symbol><symbol viewBox="0 0 10 10" xmlns="http://www.w3.org/2000/svg" id="icon-hide">  <path fill-rule="evenodd" d="M10 5C10 5 7.76125 8.125 5 8.125C2.23875 8.125 0 5 0 5C0 5 2.23875 1.875 5 1.875C7.76125 1.875 10 5 10 5ZM5 5.625C4.65482 5.625 4.375 5.34518 4.375 5C4.375 4.65482 4.65482 4.375 5 4.375C5.34518 4.375 5.625 4.65482 5.625 5C5.625 5.34518 5.34518 5.625 5 5.625ZM5 3.125C6.03553 3.125 6.875 3.96447 6.875 5C6.875 6.03553 6.03553 6.875 5 6.875C3.96447 6.875 3.125 6.03553 3.125 5C3.125 3.96447 3.96447 3.125 5 3.125Z"></path>  <rect x="7.8125" y="1.25" width="1.25" height="8.75" transform="rotate(45 7.8125 1.25)"></rect></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-home">  <path d="M8 0L0 8l1 1 7-7 7 7 1-1-8-8z"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M8 4l6 6v6h-2v-6H8v6H2v-6l6-6zm-1 6H4v3h3v-3z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-import">  <path fill-rule="evenodd" clip-rule="evenodd" d="M2 5v10h7.256a4.493 4.493 0 0 1-.229-2H4v-2h5.758A4.496 4.496 0 0 1 14 9.027V0H7v5H2zm6-2h4v2H8V3zm4 6V7H4v2h8z"></path>  <path d="M6 0L2 4h4V0zM16 13l-2.5-3-2.5 3h2v3h1v-3h2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-info">  <path fill-rule="evenodd" clip-rule="evenodd" d="M8 16C3.58172 16 0 12.4183 0 8C0 3.58172 3.58172 0 8 0C12.4183 0 16 3.58172 16 8C16 12.4183 12.4183 16 8 16ZM6.667 6.645L7.34 7.02L7.159 8.391C6.929 10.153 6.77 11.315 6.684 11.878C6.67792 11.9167 6.67425 11.9558 6.673 11.995C6.673 12.221 6.775 12.404 6.98 12.543C7.185 12.681 7.475 12.751 7.85 12.751C8.288 12.751 8.648 12.658 8.931 12.472C9.215 12.287 9.432 12.098 9.585 11.907L9.421 11.479C9.3192 11.5579 9.21118 11.6285 9.098 11.69C9.03152 11.7261 8.95759 11.7463 8.882 11.749C8.8186 11.7528 8.75759 11.7242 8.72 11.673C8.67879 11.6062 8.65956 11.5283 8.665 11.45C8.665 11.423 8.669 11.374 8.676 11.303L9.426 5.96L9.104 5.819L6.76 6.124L6.667 6.645ZM7.683 4.296C7.595 4.147 7.551 3.993 7.551 3.833H7.552C7.552 3.614 7.598 3.416 7.692 3.238C7.78358 3.0624 7.92385 2.91692 8.096 2.819C8.272 2.717 8.477 2.667 8.712 2.667C8.89432 2.66387 9.07417 2.70944 9.233 2.799C9.37852 2.87986 9.49998 2.99787 9.585 3.141C9.6655 3.27584 9.708 3.42996 9.708 3.587C9.708 3.942 9.607 4.232 9.406 4.457C9.205 4.681 8.903 4.794 8.501 4.794C8.332 4.794 8.176 4.748 8.032 4.656C7.887 4.564 7.771 4.444 7.683 4.296Z"></path></symbol><symbol viewBox="0 0 36 36" xmlns="http://www.w3.org/2000/svg" id="icon-ipython-kernel-logo">  <path fill-rule="evenodd" clip-rule="evenodd" d="M18 33c6.075 0 11-.448 11-1s-4.925-1-11-1-11 .448-11 1 4.925 1 11 1z" fill="#9E9E9E" fill-opacity=".5" filter="url(#filter0_f)"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M10.415 8.283v12.495h1.546v-4.485h2.61c2.463 0 4.078-1.585 4.078-4 0-2.425-1.598-4.01-4.043-4.01h-4.191zM7.967 20.778v-1.36h-2.55V9.642h2.55V8.283H1.331v1.36h2.55v9.775h-2.55v1.36h6.636zm6.255-11.136h-2.261v5.291h2.261c1.834 0 2.864-.944 2.864-2.64 0-1.707-1.03-2.65-2.864-2.65z" fill="#474747"></path>  <path d="M20.382 12.986h2.567v.805h-1.558v6.248h1.58v.805h-2.589v-7.858z" fill="#008DC0"></path>  <path d="M24.284 21.74l-.278-.003a2.568 2.568 0 0 1-.128-.005v-.836c.035.007.14.011.216.013h.05c.467 0 .725-.177.873-.623l.066-.213-1.716-4.775h1.113l1.17 3.784h.066l1.17-3.784h1.078l-1.707 4.85c-.414 1.194-.917 1.592-1.973 1.592z" fill="#474747"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M28.478 12.986v.805h1.559v6.248h-1.58v.805h2.588v-7.858h-2.567zm5.264 7.113a.904.904 0 0 0 0-1.805.904.904 0 0 0 0 1.805zm-.891-4.203c0 .497.401.904.89.904a.9.9 0 0 0 .891-.904c0-.498-.402-.9-.89-.9a.897.897 0 0 0-.891.9z" fill="#008DC0"></path>  <defs>    <filter id="filter0_f" x="4.282" y="28.282" width="27.437" height="7.437" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">      <feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood>      <feBlend in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend>      <feGaussianBlur stdDeviation="1.359" result="effect1_foregroundBlur"></feGaussianBlur>    </filter>  </defs></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-ipython-kernel">  <path fill-rule="evenodd" clip-rule="evenodd" d="M1.67188 5.16797V6.18359H2.83203V9.98438H1.67188V11H5.14453V9.98438H3.98438V6.18359H5.14453V5.16797H1.67188ZM7.60156 7.84766V6.13672H8.07422C8.45182 6.13672 8.7168 6.20052 8.86914 6.32812C9.02149 6.45573 9.09766 6.67708 9.09766 6.99219C9.09766 7.30729 9.02149 7.52865 8.86914 7.65625C8.7168 7.78385 8.45182 7.84766 8.07422 7.84766H7.60156ZM6.44922 5.16797H8.03125C8.83594 5.16797 9.41471 5.3112 9.76758 5.59766C10.1204 5.88412 10.2969 6.34896 10.2969 6.99219C10.2969 7.63542 10.1204 8.10026 9.76758 8.38672C9.41471 8.67318 8.83594 8.81641 8.03125 8.81641H7.60156V11H6.44922V5.16797ZM12.8574 12.373C13.0723 12.1842 13.2565 11.8841 13.4102 11.4727L15.2266 6.625H14.0234L13.0664 9.46484L12.0664 6.625H10.8633L12.5273 10.8789L12.4414 11.1133C12.3294 11.4023 12.2188 11.5866 12.1094 11.666C12 11.7454 11.8281 11.7852 11.5938 11.7852H11.1289V12.6562H12.0742C12.3815 12.6562 12.6426 12.5619 12.8574 12.373Z"></path></symbol><symbol viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" id="icon-jb">  <path d="M 0 0 L 0 24 L 24 24 L 24 0 Z M 1.949219 12.449219 L 3.449219 10.800781 C 4.050781 11.550781 4.648438 11.851562 5.398438 11.851562 C 6.300781 11.851562 6.898438 11.25 6.898438 10.050781 L 6.898438 3 L 9.300781 3 L 9.300781 10.050781 C 9.300781 11.398438 9 12.300781 8.25 12.898438 C 7.648438 13.648438 6.601562 14.101562 5.398438 14.101562 C 3.75 14.101562 2.699219 13.351562 1.949219 12.449219 Z M 13.5 21 L 3 21 L 3 19.5 L 13.5 19.5 Z M 16.949219 13.800781 L 11.699219 13.800781 L 11.699219 3 L 16.800781 3 C 18 3 19.050781 3.300781 19.648438 3.898438 C 20.101562 4.351562 20.398438 4.949219 20.398438 5.699219 C 20.398438 6.898438 19.800781 7.648438 18.898438 8.101562 C 20.25 8.699219 21 9.449219 21 10.800781 C 21 12.75 19.351562 13.800781 16.949219 13.800781 Z M 16.949219 13.800781 "></path>  <path d="M 18 6.148438 C 18 5.398438 17.398438 5.101562 16.5 5.101562 L 14.101562 5.101562 L 14.101562 7.351562 L 16.351562 7.351562 C 17.398438 7.351562 18 7.050781 18 6.148438 Z M 18 6.148438 "></path>  <path d="M 16.800781 9.449219 L 14.101562 9.449219 L 14.101562 11.851562 L 16.949219 11.851562 C 18 11.851562 18.601562 11.550781 18.601562 10.648438 C 18.601562 9.898438 18.148438 9.449219 16.800781 9.449219 Z M 16.800781 9.449219 "></path></symbol><symbol viewBox="0 0 72 70" xmlns="http://www.w3.org/2000/svg" id="icon-key">  <use xlink:href="#a" fill="#E4E4E4"></use>  <defs>    <path id="a" fill-rule="evenodd" d="M72 21c0 11.598-9.402 21-21 21-2.4 0-4.707-.402-6.855-1.145L43 42l-2 2.023v1.989L39 48h-9v5h-5v5h-5v5h-5v4l-3 3H4l-4-4v-7l31.145-31.145A20.97 20.97 0 0 1 30 21C30 9.402 39.402 0 51 0s21 9.402 21 21zm-16 2a7 7 0 1 0 0-14 7 7 0 0 0 0 14z"></path>  </defs></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-kotlin"><path fill-rule="evenodd" clip-rule="evenodd" d="M14 2L8 8l6 6H2V2h12zM7.414 3h4.172L3 11.586V7.414L7.414 3z"></path></symbol><symbol viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" id="icon-library-manager">  <path fill-rule="evenodd" clip-rule="evenodd" d="M0 5L10 0L20 5V15L10 20L0 14.882V5ZM19 6L10 10.5V19L19 14.5V6ZM11 5.5L6 8V13L4 12V7L9 4.5L11 5.5Z"></path></symbol><symbol viewBox="0 0 12 16" xmlns="http://www.w3.org/2000/svg" id="icon-lightbulb">  <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">    <path d="M3.75,13.25 L3.75,11 L8.25,11 L8.25,13.25 L7.5,14 L4.5,14 L3.75,13.25 Z" id="-g-Combined-Shape" fill="#848484"></path>    <path fill="#FDBA0D" d="M3.00213319,8.00320207 C2.52990996,7.37590898 2.25,6.59564273 2.25,5.75 C2.25,3.67893219 3.92893219,2 6,2 C8.07106781,2 9.75,3.67893219 9.75,5.75 C9.75,6.59564273 9.47009004,7.37590898 8.99786681,8.00320207 C8.49928894,8.75213471 8.25,9.50106736 8.25,10.25 L6,10.25 L3.75,10.25 C3.75,9.50106736 3.50071106,8.75213471 3.00213319,8.00320207 Z"></path>  </g></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-lines">  <path d="M15 1H1v2h14V1zm0 8H1v2h14V9zM1 13h14v2H1v-2zm14-8H1v2h14V5z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-link">  <path d="M10.586 1.415a2 2 0 0 1 2.829 0l1.17 1.17a2 2 0 0 1 0 2.83L12 8a1.414 1.414 0 0 1-2 0l3.647-3.646a.5.5 0 0 0 0-.708l-1.293-1.292a.5.5 0 0 0-.707 0L8 6a1.414 1.414 0 0 1 0-2l2.586-2.585z"></path>  <path d="M11 6l-1-1-5 5 1 1 5-5z"></path>  <path d="M6 8l-3.646 3.647a.5.5 0 0 0 0 .707l1.292 1.293a.5.5 0 0 0 .708 0L8 10a1.414 1.414 0 0 1 0 2l-2.585 2.586a2 2 0 0 1-2.83 0l-1.17-1.171a2 2 0 0 1 0-2.83L4 8a1.414 1.414 0 0 1 2 0z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-list">  <path d="M3 1v2H1V1h2zm0 8v2H1V9h2zm-2 4h2v2H1v-2zm2-8v2H1V5h2zm12-4v2H4V1h11zm0 8v2H4V9h11zM4 13h11v2H4v-2zm11-8v2H4V5h11z"></path></symbol><symbol viewBox="0 0 10 14" xmlns="http://www.w3.org/2000/svg" id="icon-lock">  <path d="M5 2C6.10457 2 7 2.89543 7 4V6H9V4C9 1.79086 7.20914 0 5 0C2.79086 0 1 1.79086 1 4V6H3V4C3 2.89543 3.89543 2 5 2ZM10 12V7H0V12C0 13.1046 0.89543 14 2 14H8C9.10457 14 10 13.1046 10 12Z"></path></symbol><symbol viewBox="0 0 30 38" xmlns="http://www.w3.org/2000/svg" id="icon-logo-kotlin-kernel"><g filter="url(#prefix__filter0_f)"><path fill-rule="evenodd" clip-rule="evenodd" d="M15 35c6.075 0 11-.448 11-1s-4.925-1-11-1-11 .448-11 1 4.925 1 11 1z" fill="#9E9E9E" fill-opacity=".5"></path></g><path d="M27.014 24H3V0h24.014L15.007 11.993 27.014 24z" fill="url(#prefix__paint0_linear)"></path><defs><linearGradient id="prefix__paint0_linear" x1="27.011" y1="-.004" x2="3.004" y2="24.004" gradientUnits="userSpaceOnUse"><stop offset=".003" stop-color="#E44857"></stop><stop offset=".469" stop-color="#C711E1"></stop><stop offset="1" stop-color="#7F52FF"></stop></linearGradient><filter id="prefix__filter0_f" x="1.282" y="30.282" width="27.437" height="7.437" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB"><feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood><feBlend in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend><feGaussianBlur stdDeviation="1.359" result="effect1_foregroundBlur"></feGaussianBlur></filter></defs></symbol><symbol viewBox="0 0 30 38" xmlns="http://www.w3.org/2000/svg" id="icon-logo-python-kernel"><g filter="url(#prefix__filter0_f)"><path fill-rule="evenodd" clip-rule="evenodd" d="M15 35c6.075 0 11-.448 11-1s-4.925-1-11-1-11 .448-11 1 4.925 1 11 1z" fill="#9E9E9E" fill-opacity=".5"></path></g><path d="M14.914 2C8.82 2 9.2 4.642 9.2 4.642l.007 2.737h5.814v.822H6.9S3 7.76 3 13.907c0 6.147 3.403 5.93 3.403 5.93h2.03v-2.853s-.109-3.403 3.35-3.403h5.766s3.24.052 3.24-3.131V5.186S21.28 2 14.913 2zm-3.206 1.84a1.045 1.045 0 110 2.093 1.045 1.045 0 110-2.092z" fill="url(#prefix__paint0_linear)"></path><path d="M15.086 25.875c6.093 0 5.713-2.642 5.713-2.642l-.007-2.737h-5.814v-.822H23.1S27 20.116 27 13.968c0-6.147-3.403-5.93-3.403-5.93h-2.03v2.854s.109 3.402-3.35 3.402h-5.766s-3.24-.052-3.24 3.132v5.264s-.492 3.185 5.875 3.185zm3.206-1.84a1.045 1.045 0 110-2.093 1.045 1.045 0 110 2.092z" fill="url(#prefix__paint1_linear)"></path><defs><linearGradient id="prefix__paint0_linear" x1="5.306" y1="4.087" x2="17.174" y2="15.994" gradientUnits="userSpaceOnUse"><stop stop-color="#387EB8"></stop><stop offset="1" stop-color="#366994"></stop></linearGradient><linearGradient id="prefix__paint1_linear" x1="12.607" y1="11.662" x2="25.352" y2="23.872" gradientUnits="userSpaceOnUse"><stop stop-color="#FFE052"></stop><stop offset="1" stop-color="#FFC331"></stop></linearGradient><filter id="prefix__filter0_f" x="1.282" y="30.282" width="27.437" height="7.437" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB"><feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood><feBlend in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend><feGaussianBlur stdDeviation="1.359" result="effect1_foregroundBlur"></feGaussianBlur></filter></defs></symbol><symbol viewBox="0 0 30 38" xmlns="http://www.w3.org/2000/svg" id="icon-logo-r-kernel"><g filter="url(#prefix__filter0_f)"><path fill-rule="evenodd" clip-rule="evenodd" d="M15 35c6.075 0 11-.448 11-1s-4.925-1-11-1-11 .448-11 1 4.925 1 11 1z" fill="#9E9E9E" fill-opacity=".5"></path></g><path fill-rule="evenodd" clip-rule="evenodd" d="M14.982 21.108c-6.6 0-11.952-3.583-11.952-8.004 0-4.42 5.351-8.005 11.952-8.005 6.6 0 11.952 3.584 11.952 8.005 0 4.42-5.351 8.004-11.952 8.004zm1.83-12.879c-5.018 0-9.085 2.45-9.085 5.472 0 3.022 4.067 5.472 9.084 5.472 5.017 0 8.72-1.675 8.72-5.472 0-3.796-3.703-5.472-8.72-5.472z" fill="url(#prefix__paint0_linear)"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M21.232 17.497s.724.219 1.144.431c.145.074.398.221.58.415.178.189.265.38.265.38l2.85 4.807-4.607.002-2.155-4.046s-.44-.758-.712-.978c-.227-.183-.323-.248-.547-.248h-1.095v5.27l-4.076.001V10.07h8.187s3.73.067 3.73 3.615-3.564 3.812-3.564 3.812zM19.46 12.99l-2.469-.002-.001 2.29 2.47-.002s1.143-.003 1.143-1.164c0-1.184-1.143-1.122-1.143-1.122z" fill="url(#prefix__paint1_linear)"></path><defs><linearGradient id="prefix__paint0_linear" x1="3.03" y1="5.099" x2="17.834" y2="27.203" gradientUnits="userSpaceOnUse"><stop stop-color="#CBCED0"></stop><stop offset="1" stop-color="#84838B"></stop></linearGradient><linearGradient id="prefix__paint1_linear" x1="12.879" y1="10.07" x2="26.338" y2="23.261" gradientUnits="userSpaceOnUse"><stop stop-color="#276DC3"></stop><stop offset="1" stop-color="#165CAA"></stop></linearGradient><filter id="prefix__filter0_f" x="1.282" y="30.282" width="27.437" height="7.437" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB"><feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood><feBlend in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend><feGaussianBlur stdDeviation="1.359" result="effect1_foregroundBlur"></feGaussianBlur></filter></defs></symbol><symbol viewBox="0 0 30 38" xmlns="http://www.w3.org/2000/svg" id="icon-logo-scala-kernel"><g filter="url(#prefix__filter0_f)"><path fill-rule="evenodd" clip-rule="evenodd" d="M15 35c6.075 0 11-.448 11-1s-4.925-1-11-1-11 .448-11 1 4.925 1 11 1z" fill="#9E9E9E" fill-opacity=".5"></path></g><path d="M8 16.765v1.845c0 .312 6.712.833 11.085 1.846 2.113-.49 3.68-1.094 3.68-1.846v-1.845c0-.751-1.567-1.356-3.68-1.846C14.712 15.933 8 16.454 8 16.765z" fill="url(#prefix__paint0_linear)"></path><path d="M8 9.382v1.846c0 .311 6.712.832 11.085 1.846 2.113-.49 3.68-1.094 3.68-1.846V9.382c0-.75-1.567-1.356-3.68-1.845C14.712 8.55 8 9.072 8 9.382z" fill="url(#prefix__paint1_linear)"></path><path d="M8 13.074v5.536c0-.461 14.765-1.384 14.765-3.69V9.381C22.765 11.69 8 12.612 8 13.074z" fill="url(#prefix__paint2_linear)"></path><path d="M8 5.691v5.537c0-.461 14.765-1.384 14.765-3.691V2C22.765 4.307 8 5.23 8 5.691z" fill="url(#prefix__paint3_linear)"></path><path d="M8 20.456v5.537c0-.462 14.765-1.384 14.765-3.691v-5.537C22.765 19.072 8 19.995 8 20.456z" fill="url(#prefix__paint4_linear)"></path><defs><linearGradient id="prefix__paint0_linear" x1="8" y1="17.688" x2="22.765" y2="17.688" gradientUnits="userSpaceOnUse"><stop stop-color="#4F4F4F"></stop><stop offset="1"></stop></linearGradient><linearGradient id="prefix__paint1_linear" x1="8" y1="10.305" x2="22.765" y2="10.305" gradientUnits="userSpaceOnUse"><stop stop-color="#4F4F4F"></stop><stop offset="1"></stop></linearGradient><linearGradient id="prefix__paint2_linear" x1="8" y1="13.996" x2="22.765" y2="13.996" gradientUnits="userSpaceOnUse"><stop stop-color="#C40000"></stop><stop offset="1" stop-color="red"></stop></linearGradient><linearGradient id="prefix__paint3_linear" x1="8" y1="6.614" x2="22.765" y2="6.614" gradientUnits="userSpaceOnUse"><stop stop-color="#C40000"></stop><stop offset="1" stop-color="red"></stop></linearGradient><linearGradient id="prefix__paint4_linear" x1="8" y1="21.379" x2="22.765" y2="21.379" gradientUnits="userSpaceOnUse"><stop stop-color="#C40000"></stop><stop offset="1" stop-color="red"></stop></linearGradient><filter id="prefix__filter0_f" x="1.282" y="30.282" width="27.437" height="7.437" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB"><feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood><feBlend in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend><feGaussianBlur stdDeviation="1.359" result="effect1_foregroundBlur"></feGaussianBlur></filter></defs></symbol><symbol viewBox="0 0 32 14" xmlns="http://www.w3.org/2000/svg" id="icon-long-arrow">  <path d="M24 13L25 14L32 7L25 -4.37114e-08L24 1L30 7L24 13Z"></path>  <path d="M0 6H30V8H0V6Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-loupe">  <path fill-rule="evenodd" clip-rule="evenodd" d="M11 5.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0zm-2 0a3.5 3.5 0 1 1-7 0 3.5 3.5 0 0 1 7 0z"></path>  <path d="M14 16l2-2-4-4h-2v2l4 4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-mail">  <path d="M0 2h16L8 8 0 2zm0 2l8 6 8-6v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-markdown"><path fill-rule="evenodd" clip-rule="evenodd" d="M1 2a1 1 0 00-1 1v10a1 1 0 001 1h14a1 1 0 001-1V3a1 1 0 00-1-1H1zm3 10H2V4h2l2 2 2-2h2v8H8V7L6 9 4 7v5zm10-8h-2v6h-1l2 2 2-2h-1V4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-navigator">  <path fill-rule="evenodd" clip-rule="evenodd" d="M14.0952 8C14.0952 11.7871 11.7871 14.0952 8 14.0952C4.2129 14.0952 1.90476 11.7871 1.90476 8C1.90476 4.2129 4.2129 1.90476 8 1.90476C11.7871 1.90476 14.0952 4.2129 14.0952 8ZM16 8C16 12.4183 12.4183 16 8 16C3.58172 16 0 12.4183 0 8C0 3.58172 3.58172 0 8 0C12.4183 0 16 3.58172 16 8ZM5.5 5.5L4 12L10.5 10.5L12 4L5.5 5.5ZM9 8C9 8.55228 8.55228 9 8 9C7.44772 9 7 8.55228 7 8C7 7.44772 7.44772 7 8 7C8.55228 7 9 7.44772 9 8Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-new-file">  <path d="M6 1h8v5.341A6 6 0 006.803 15H2V5h4V1z"></path>  <path d="M5 1L2 4h3V1zM13 11V8h-2v3H8v2h3v3h2v-3h3v-2h-3z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-new-folder">    <path d="M13 8v2.999L16 11v2h-3v3h-2v-3H8v-2h3V8h2zM8 2l1 2h6l.001 2.803a5.97 5.97 0 0 0-1-.461L14 5H8.382l-1-2H2v10h4.083c.058.345.145.68.259 1H1V2h7z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-new-zpl-notebook">    <path d="M13 8v2.999L16 11v2h-3v3h-2v-3H8v-2h3V8h2zm1-8v6.341A6 6 0 0 0 6 12H3.5a.5.5 0 1 0 0 1h2.583c.058.345.145.68.258 1H3a1 1 0 0 1-1-1V1a1 1 0 0 1 1-1h11zM6.08 1.477h-2.7v.72h1.626v.047L3.353 4.43V5H6.13v-.72H4.427v-.047L6.08 2.046v-.569zm2.329 0H6.866V5h.896V3.967h.593c.784 0 1.323-.49 1.323-1.24 0-.757-.512-1.25-1.27-1.25zm2.822 0h-.896V5h2.393v-.74H11.23V1.477zm-3.059.689c.379 0 .6.192.6.563 0 .367-.224.562-.605.562h-.405V2.166h.41z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-no-connection"><path d="M8 2c1.032 0 1.972.39 2.682 1.032L1.126 12.59A2.498 2.498 0 011 8.499 3.5 3.5 0 014.12 5.02 4.002 4.002 0 018 2zM5.707 13l-2.353 2.354-.708-.707 12-12 .708.707-1.95 1.949a1.498 1.498 0 01.46 1.823A3.001 3.001 0 0113 13H5.707z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-notification">  <path d="M4 5a4 4 0 0 1 8 0v3a2 2 0 0 0 2 2v2H2v-2a2 2 0 0 0 2-2V5zm4 9c-.74 0-1.387-.402-1.732-1h3.464c-.345.598-.992 1-1.732 1z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-open">  <path d="M14 4H8L7 2H0v12l2-8h12V4z"></path>  <path d="M1 14l2-7h13l-2 7H1z"></path></symbol><symbol viewBox="0 0 36 36" xmlns="http://www.w3.org/2000/svg" id="icon-preview"><path d="M18 36C27.9411 36 36 27.9411 36 18C36 8.05887 27.9411 0 18 0C8.05887 0 0 8.05887 0 18C0 27.9411 8.05887 36 18 36Z" fill="#008DC0"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M18 23C22.4182 23 26 18 26 18C26 18 22.4182 13 18 13C13.5818 13 10 18 10 18C10 18 13.5818 23 18 23ZM18 21C19.6567 21 21 19.6567 21 18C21 16.3433 19.6567 15 18 15C16.3433 15 15 16.3433 15 18C15 19.6567 16.3433 21 18 21Z" fill="white"></path><path d="M18 19C18.5523 19 19 18.5523 19 18C19 17.4477 18.5523 17 18 17C17.4477 17 17 17.4477 17 18C17 18.5523 17.4477 19 18 19Z" fill="white"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-print"><path d="M5 12h4v1H5v-1zM8 10H5v1h3v-1z"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M3 1v4H1a1 1 0 00-1 1v5a1 1 0 001 1h2v3h10v-3h2a1 1 0 001-1V6a1 1 0 00-1-1h-2V1H3zm1 7h8v6H4V8zm8-6H4v3h8V2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-private-folder-alt"><path d="M15 4H9L8 2H1v12h5.342a5.958 5.958 0 01-.259-1H2V3h5.382l1 2H14v1.342c.35.123.685.278 1.001.461z"></path><path clip-rule="evenodd" d="M15 11v5H9v-5a3 3 0 116 0zm-1 1v-1a2 2 0 10-4 0v1z" fill-rule="evenodd"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-private-folder">        <path fill-rule="nonzero" d="M15 3v2H1V1h7l1 2h6zM8.682 6A5.994 5.994 0 0 0 6 11c0 .701.12 1.374.341 2H1V6h7.682zM15 10v5H9v-5a3 3 0 0 1 6 0zm-1 1v-1a2 2 0 1 0-4 0v1h4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-public"><path d="M13 4.5a2.5 2.5 0 1 1-5 0 2.5 2.5 0 0 1 5 0zM7.94 8a2 2 0 0 0-1.977 1.698L5 16h11l-.963-6.302A2 2 0 0 0 13.06 8H7.94zM6 7a2 2 0 1 1-4 0 2 2 0 0 1 4 0zm-1.095 3h-2.29a2 2 0 0 0-1.979 1.707L0 16h3.988l.917-6z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-publish">  <path d="M15 1H9l2 2-5.5 5.5 2 2L13 5l2 2V1z"></path>  <path d="M14 9v6H1V2h6v2H3v9h9V9h2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-published-notebook"><path fill-rule="evenodd" clip-rule="evenodd" d="M3 1a1 1 0 00-1 1v12a1 1 0 001 1h11v-1H3.5a.5.5 0 010-1H14V1H3zm6 4a1 1 0 11-2 0 1 1 0 012 0zM5.525 7.849C5.607 7.361 6.065 7 6.604 7h2.792c.54 0 .997.36 1.079.849L11 10H5l.525-2.151z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-published-notebooks"><path fill-rule="evenodd" clip-rule="evenodd" d="M15 4H9L8 2H1v12h14V4zM9 7a1 1 0 11-2 0 1 1 0 012 0zM5.525 9.849C5.607 9.361 6.065 9 6.604 9h2.792c.54 0 .997.36 1.079.849L11 12H5l.525-2.151z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-python"><path fill-rule="evenodd" clip-rule="evenodd" d="M11 2.297c0-.384-.218-.74-.578-.873A7.013 7.013 0 008 1c-.862 0-1.681.151-2.422.424-.36.133-.578.489-.578.873V4h3v1H2.297c-.384 0-.74.218-.873.578A7.013 7.013 0 001 8c0 .862.151 1.681.424 2.422.133.36.489.578.873.578H4V9a1.5 1.5 0 011.5-1.5h5A.5.5 0 0011 7V2.297zM6.5 3a.5.5 0 100-1 .5.5 0 000 1z"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M12 5v2a1.5 1.5 0 01-1.5 1.5h-5A.5.5 0 005 9v4.703c0 .384.218.74.578.873.74.273 1.56.424 2.422.424.862 0 1.681-.151 2.422-.424.36-.133.578-.489.578-.873V12H8v-1h5.703c.384 0 .74-.218.873-.578.273-.74.424-1.56.424-2.422 0-.862-.151-1.681-.424-2.422-.133-.36-.489-.578-.873-.578H12zm-2.5 9a.5.5 0 100-1 .5.5 0 000 1z"></path></symbol><symbol viewBox="0 0 7 10" xmlns="http://www.w3.org/2000/svg" id="icon-question">  <path d="M 2.1751 8.29001L 4.00821 8.29001L 4.00821 10L 2.1751 10L 2.1751 8.29001ZM 0 3.33789C 0 2.8363 0.0729594 2.3803 0.218878 1.9699C 0.373917 1.55951 0.592795 1.20839 0.875513 0.916553C 1.16735 0.624715 1.51391 0.401277 1.91518 0.246238C 2.32558 0.0820794 2.78158 0 3.28317 0C 3.70269 0 4.09029 0.0638395 4.44596 0.191518C 4.81076 0.310077 5.1254 0.487916 5.38988 0.725034C 5.66347 0.953033 5.87779 1.24031 6.03283 1.58687C 6.18787 1.93342 6.26539 2.32558 6.26539 2.76334C 6.26539 3.08254 6.22891 3.36069 6.15595 3.59781C 6.09211 3.82581 6.00091 4.02645 5.88235 4.19973C 5.77291 4.36389 5.64523 4.51436 5.49932 4.65116C 5.3534 4.77884 5.20748 4.90652 5.06156 5.0342C 4.88828 5.18012 4.72868 5.32148 4.58276 5.45828C 4.43684 5.59508 4.30916 5.75011 4.19973 5.92339C 4.09029 6.08755 4.00365 6.28363 3.93981 6.51163C 3.88509 6.73963 3.85773 7.01778 3.85773 7.3461L 2.3803 7.3461C 2.3803 6.94482 2.39854 6.60739 2.43502 6.33379C 2.48062 6.05107 2.54902 5.80483 2.64022 5.59508C 2.73142 5.38532 2.84086 5.20292 2.96854 5.04788C 3.10533 4.88372 3.26493 4.72412 3.44733 4.56908C 3.59325 4.4414 3.73005 4.32284 3.85773 4.21341C 3.99453 4.10397 4.11309 3.98541 4.21341 3.85773C 4.32284 3.72093 4.40492 3.57045 4.45964 3.40629C 4.52348 3.24213 4.5554 3.04606 4.5554 2.81806C 4.5554 2.54446 4.50524 2.3119 4.40492 2.12038C 4.31372 1.91974 4.19973 1.76015 4.06293 1.64159C 3.92613 1.52303 3.78021 1.43639 3.62517 1.38167C 3.47013 1.32695 3.33333 1.29959 3.21477 1.29959C 2.64934 1.29959 2.22982 1.48655 1.95622 1.86047C 1.69175 2.22526 1.55951 2.71774 1.55951 3.33789L 0 3.33789Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-r"><path d="M16 6.358c0 .37-.056.733-.163 1.082a3.5 3.5 0 00-.848-1.401c-.431-2.035-2.741-2.944-5.764-2.944-3.359 0-6.081 1.64-6.081 3.663 0 1.309 1.14 2.458 2.856 3.106v1.683c-3.45-.595-6-2.693-6-5.19C0 3.4 3.582 1 8 1s8 2.399 8 5.358z"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M13.357 11.26c-.281-.142-.765-.288-.765-.288s2.385-.177 2.385-2.552S12.48 6 12.48 6H7v9.01h2.73l-.001-3.528h.732c.15 0 .215.044.367.166.181.148.477.655.477.655l1.442 2.708 3.084-.001-1.908-3.217s-.058-.129-.178-.256a1.478 1.478 0 00-.388-.277zM9.752 7.953l1.652.002s.766-.042.766.75c0 .778-.766.78-.766.78H9.751l.001-1.532z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-recent">  <path d="M6 3v2h2v1H5V3h1z"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M11 5.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0zm-2 0a3.5 3.5 0 1 1-7 0 3.5 3.5 0 0 1 7 0z"></path>  <path d="M14 16l2-2-4-4h-2v2l4 4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-refresh">  <path d="M8 6V4a4 4 0 1 0 3.579 2.21l1.789-.894A6 6 0 1 1 8 2V0l4 3-4 3z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-report-badged"><path class="icon" fill-rule="evenodd" clip-rule="evenodd" d="M2 2a1 1 0 011-1h11v6.416A4.983 4.983 0 0012 7c-.632 0-1.236.117-1.793.331A1.136 1.136 0 009.397 7H6.603c-.54 0-.997.36-1.079.849L5 10h2.416a5.022 5.022 0 00-.316 3H3.5a.5.5 0 000 1h3.916c.156.357.352.692.584 1H3a1 1 0 01-1-1V2zm6 4a1 1 0 100-2 1 1 0 000 2z"></path><circle class="badge" cx="12" cy="12" r="4"></circle></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-resize">  <path d="M9.30947 7.96987C9.38685 7.96987 9.4553 7.99963 9.51482 8.05915L12.4791 11.0234L13.7648 9.73772C13.8779 9.62463 14.0118 9.56808 14.1666 9.56808C14.3214 9.56808 14.4553 9.62463 14.5684 9.73772C14.6815 9.85082 14.738 9.98475 14.738 10.1395V14.1395C14.738 14.2943 14.6815 14.4282 14.5684 14.5413C14.4553 14.6544 14.3214 14.7109 14.1666 14.7109H10.1666C10.0118 14.7109 9.87792 14.6544 9.76482 14.5413C9.65173 14.4282 9.59518 14.2943 9.59518 14.1395C9.59518 13.9847 9.65173 13.8508 9.76482 13.7377L11.0505 12.452L8.08625 9.48772C8.02673 9.4282 7.99697 9.35975 7.99697 9.28237C7.99697 9.20498 8.02673 9.13653 8.08625 9.07701L9.10411 8.05915C9.16363 7.99963 9.23208 7.96987 9.30947 7.96987ZM1.59518 0.996651H5.59518C5.74994 0.996651 5.88387 1.0532 5.99697 1.16629C6.11006 1.27939 6.16661 1.41332 6.16661 1.56808C6.16661 1.72284 6.11006 1.85677 5.99697 1.96987L4.71125 3.25558L7.67554 6.21987C7.73506 6.27939 7.76482 6.34784 7.76482 6.42522C7.76482 6.5026 7.73506 6.57106 7.67554 6.63058L6.65768 7.64844C6.59816 7.70796 6.5297 7.73772 6.45232 7.73772C6.37494 7.73772 6.30649 7.70796 6.24697 7.64844L3.28268 4.68415L1.99697 5.96987C1.88387 6.08296 1.74994 6.13951 1.59518 6.13951C1.44042 6.13951 1.30649 6.08296 1.19339 5.96987C1.0803 5.85677 1.02375 5.72284 1.02375 5.56808V1.56808C1.02375 1.41332 1.0803 1.27939 1.19339 1.16629C1.30649 1.0532 1.44042 0.996651 1.59518 0.996651Z" fill="black"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-restore">  <path d="M15 3h-2v2H9V3H7l4-3 4 3zM2 16V4h2v12H2z"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M16 14V7H6v7a2 2 0 0 0 2 2h6a2 2 0 0 0 2-2zm-6-6H9v6h1V8zm2 0h1v6h-1V8z"></path>  <path d="M1 8H0v4h1V8z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-run-cell-minor"><path fill-rule="evenodd" clip-rule="evenodd" d="M14 8L2 1v14l12-7zm-3.97 0L4 4.482v7.036L10.03 8z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-run-cell"><path d="M4 3v10l8-5-8-5z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-run">    <path d="M2 1v14l12-7z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-scala"><path fill-rule="evenodd" clip-rule="evenodd" d="M2 3C14 1 14 .5 14 0v3c0 .5 0 1-12 3V3zm0 10c12-2 12-2.5 12-3v3c0 .5 0 1-12 3v-3zm12-8c0 .5 0 1-12 3v3c12-2 12-2.5 12-3V5z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-secret">  <path d="M10 5a2 2 0 1 0-4 0v2H4V5a4 4 0 1 1 8 0v2h-2V5z"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M13 8v5a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8h10zm-5 2a1 1 0 0 0-1 1v1a1 1 0 1 0 2 0v-1a1 1 0 0 0-1-1z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-settings"><path fill-rule="evenodd" clip-rule="evenodd" d="M7 1h2l.313 1.876c.031.19.171.344.354.409a4.974 4.974 0 01.489.202.533.533 0 00.54-.038l1.547-1.106 1.414 1.414-1.106 1.548a.533.533 0 00-.038.54 4.902 4.902 0 01.203.488.532.532 0 00.408.354L15 7v2l-1.876.313a.532.532 0 00-.409.354 4.92 4.92 0 01-.202.489.532.532 0 00.038.539l1.106 1.548-1.414 1.414-1.548-1.106a.532.532 0 00-.54-.038 4.924 4.924 0 01-.488.203.532.532 0 00-.354.408L9 15H7l-.313-1.876a.532.532 0 00-.354-.409 5.005 5.005 0 01-.489-.202.532.532 0 00-.54.038l-1.547 1.106-1.414-1.414 1.106-1.548a.532.532 0 00.038-.54 5.01 5.01 0 01-.202-.488.533.533 0 00-.41-.354L1 9V7l1.876-.313a.533.533 0 00.409-.354 4.954 4.954 0 01.202-.489.532.532 0 00-.038-.54L2.343 3.758l1.414-1.414L5.305 3.45a.532.532 0 00.54.038 4.965 4.965 0 01.488-.202.532.532 0 00.354-.41L7 1.001zm1 10a3 3 0 100-6 3 3 0 000 6z"></path></symbol><symbol viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg" id="icon-side-panel"> <g>  <rect stroke-width="1.5" x="34.701341" y="2.82949" width="7.904191" height="42.832112" id="svg_1"></rect>  <line fill="none" stroke-width="4" fill-opacity="null" x1="2.862275" y1="24" x2="27.892214" y2="24" id="svg_2" stroke="#464646"></line>  <path fill="none" stroke="#464646" stroke-width="6" fill-opacity="null" d="m22.603326,26.151676l3.14465,-4.02516l3.14466,4.02516l-6.28931,0z" id="svg_3" transform="rotate(89.84203338623047 25.74798011779785,24.13909530639648) "></path> </g></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-slash">  <path d="M7 13H6L9 3h1z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-sorting-arrow">  <path d="M8 2l4 5H9v6H7V7H4l4-5z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-squares">  <path d="M9 0h6v7H9V0zM1 9h6v7H1V9zm8 0h6v7H9V9zM1 0h6v7H1V0z"></path></symbol><symbol viewBox="0 0 38 35" xmlns="http://www.w3.org/2000/svg" id="icon-star">    <defs></defs>    <g id="Pages" stroke-width="1" fill-rule="evenodd" fill-opacity="0">        <g id="recent-&amp;-favorites" transform="translate(-58.000000, -738.000000)" stroke-width="2" stroke="#464646">            <g id="Group-3" transform="translate(60.000000, 741.000000)">                <polygon id="Star" points="17 24.75 7.00765071 29.8487804 8.91601961 19.0493902 0.832039223 11.4012196 12.0038254 9.8256098 17 0 21.9961746 9.8256098 33.1679608 11.4012196 25.0839804 19.0493902 26.9923493 29.8487804"></polygon>            </g>        </g>    </g></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-stop-computation-alt"><path d="M5 5h6v6H5V5z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-stop-computation">    <path d="M2 2h12v12H2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-table"><path fill-rule="evenodd" clip-rule="evenodd" d="M1 2V14H15V2H1ZM2 5V7H5.25V5H2ZM6.25 5V7H9.75V5H6.25ZM10.75 5V7H14V5H10.75ZM5.25 13H2V11H5.25V13ZM9.75 13H6.25V11H9.75V13ZM14 13H10.75V11H14V13ZM14 10V8H10.75V10H14ZM9.75 10V8H6.25V10H9.75ZM5.25 10V8H2V10H5.25Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-terminal"><path fill-rule="evenodd" clip-rule="evenodd" d="M15 1H1v14h14V1zM4 3L3 4l2 2-2 2 1 1 3-3-3-3zm4 4.5h4V9H8V7.5z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-to-back"><rect width="12" height="11" fill="#474747"></rect><path d="M13 7V5H16V16H4V12H6V14H14V7H13Z" fill="#474747"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-to-front">  <path d="M0 0H12V4H3V11H0V0Z" fill="#474747"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M16 5H4V16H16V5ZM14 7H6V14H14V7Z" fill="#474747"></path></symbol><symbol viewBox="0 0 18 20" xmlns="http://www.w3.org/2000/svg" id="icon-toc">  <rect width="13" height="2" rx="1"></rect>  <rect x="3" y="4" width="10" height="2" rx="1"></rect>  <rect x="3" y="8" width="10" height="2" rx="1"></rect>  <rect y="12" width="13" height="2" rx="1"></rect>  <rect x="15" width="2" height="2"></rect>  <rect x="15" y="4" width="2" height="2"></rect>  <rect x="15" y="8" width="2" height="2"></rect>  <rect x="3" y="16" width="10" height="2" rx="1"></rect>  <rect x="15" y="16" width="2" height="2"></rect>  <rect x="15" y="12" width="2" height="2"></rect></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-toggle-bold"><path d="M8.414 14c2.414 0 3.938-1.273 3.938-3.25 0-1.438-1.141-2.586-2.618-2.664v-.149a2.431 2.431 0 002.102-2.398c0-1.75-1.328-2.812-3.578-2.812H3V14h5.414zM5.867 4.75h1.625c.977 0 1.547.484 1.547 1.29 0 .796-.61 1.28-1.656 1.28H5.867V4.75zm0 7.227V9.062h1.719c1.187 0 1.851.516 1.851 1.438 0 .953-.648 1.477-1.835 1.477H5.867z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-toggle-code"><path d="M1 8.568V7.419L7 4v1.967l-3.802 1.98v.093L7 10.02V12L1 8.568zM9 10l3.802-1.96v-.093L9 5.967V4l6 3.406v1.148L9 12v-2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-toggle-heading"><path d="M6.21 4.469V14H4.196V4.469H.727V2.727h8.96v1.742H6.212zM12.882 8.043V14h-1.26V8.043H9.454V6.954h5.6v1.089h-2.172z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-toggle-italic"><path d="M3 14l.224-1.344h2.624l2.424-8.48H5.648l.224-1.344h7.008l-.224 1.344h-2.624l-2.424 8.48h2.624L10.008 14H3z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-toggle-list"><path d="M6 2h8v2H6V2zM2 3a1 1 0 112 0 1 1 0 01-2 0zM2 12.5h2v1H2v-1zM6 7h8v2H6V7zM6 12h8v2H6v-2zM1.971 10v-.605h.94v-2.34h-.045l-.71.93-.48-.375.835-1.1h1.15v2.885h.74V10h-2.43z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-toggle-math"><path d="M5.285 4.36H.242L.2 5.851h.356c.16-.887.406-1.02 1.41-1.051l.21-.004v4.285c0 .379-.085.473-.714.54V10h2.605v-.379c-.632-.066-.714-.16-.714-.539V4.797l.21.004c1.004.031 1.25.164 1.415 1.05h.351L5.285 4.36zM9.734 7.36H5.25v.378c.594.063.66.137.66.485v3.914c0 .347-.066.422-.66.484V13h4.66l.05-1.68h-.35c-.22 1.07-.446 1.172-1.5 1.207l-1.024.036v-2.231h.965c.277 0 .37.113.488.781h.336V9.121h-.336c-.133.676-.223.777-.488.777h-.965V7.797l.992.031c.895.027 1.14.184 1.344 1.024h.355l-.043-1.493zM10.008 9.621c.52-.055.66-.16 1.105-.785l1.114-1.578-1.282-1.899c-.3-.437-.457-.535-.898-.62v-.38h2.637v.38c-.621.081-.657.206-.325.699l.829 1.222.789-1.223c.324-.5.3-.617-.325-.699V4.36h1.977v.38c-.516.054-.668.156-1.086.757l-1.09 1.559L14.77 9c.296.438.464.535.898.621V10h-2.637v-.379c.621-.082.656-.207.324-.7l-.859-1.265-.832 1.266c-.328.5-.3.617.324.7V10h-1.98v-.379z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-toggle-strikethrough"><path d="M3.968 7h3c-.81-.3-1.155-.7-1.155-1.29 0-.96.859-1.585 2.156-1.585 1.234 0 2.11.625 2.25 1.617h1.93c-.094-1.937-1.805-3.297-4.172-3.297-2.524 0-4.196 1.36-4.196 3.407 0 .424.062.806.187 1.148zM15 8v1H1V8h14zM7.898 14.281c-2.585 0-4.296-1.297-4.398-3.344h1.969c.125 1.008 1.125 1.657 2.554 1.657 1.329 0 2.29-.68 2.29-1.625 0-.395-.146-.71-.462-.969h2.412c.044.223.065.463.065.719 0 2.195-1.695 3.562-4.43 3.562z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-transfer-left"><path fill-rule="evenodd" clip-rule="evenodd" d="M5 3L0 8l5 5v-3h6V6H5V3zm10-2h-2v14h2V1z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-trash-perm">  <path d="M6 1h4v1H6V1zM2 3h12v2H2V3z"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M3 6h10v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V6zm8 2l-1-1-2 2-2-2-1 1 2 2-2 2 1 1 2-2 2 2 1-1-2-2 2-2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-trash">  <path fill-rule="evenodd" clip-rule="evenodd" d="M6 1h4v1H6V1zM3 6h10v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V6zm3 1h1v6H6V7zm4 0H9v6h1V7zm4-4H2v2h12V3z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-twitter-mask">  <path d="M5.032 14.003c6.038 0 9.34-5.002 9.34-9.34a8.54 8.54 0 0 0-.01-.424A6.675 6.675 0 0 0 16 2.54a6.546 6.546 0 0 1-1.885.517 3.294 3.294 0 0 0 1.443-1.816 6.583 6.583 0 0 1-2.084.797A3.283 3.283 0 0 0 7.88 5.031 9.32 9.32 0 0 1 1.113 1.6 3.28 3.28 0 0 0 2.13 5.983a3.259 3.259 0 0 1-1.486-.41v.042a3.284 3.284 0 0 0 2.633 3.218c-.483.131-.99.15-1.482.056a3.286 3.286 0 0 0 3.066 2.28 6.585 6.585 0 0 1-4.077 1.405c-.265 0-.526-.015-.783-.045a9.292 9.292 0 0 0 5.032 1.474"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-unfold-cell"><path d="M4 4h8v8H4V4z" fill="#fff"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M5 5h6v6H5V5zm-1 7V4h8v8H4zm3.5-6h1v1.5H10v1H8.5V10h-1V8.5H6v-1h1.5V6z" fill="#C5C5C5"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-unpack"><path fill-rule="evenodd" clip-rule="evenodd" d="M12 4L8 0 4 4h2v3l2 1 2-1V4h2zM1 5.5L2 5l1 .5L2 6l6 3 6-3-1-.5 1-.5 1 .5v7L8 16l-7-3.5v-7zM2 7l5 2.5v5L2 12V7z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-unpublish">  <path fill-rule="evenodd" clip-rule="evenodd" d="M5 11h6L9 9l6-6-2-2-6 6-2-2v6zm9 4H1V2h6v2H3v9h9V9h2v6z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-unsorted"><path d="M5 7l3-4 3 4H5zM11 9l-3 4-3-4h6z"></path></symbol><symbol viewBox="0 0 10 12" xmlns="http://www.w3.org/2000/svg" id="icon-up"><path d="M4.9942 1.62808e-05L8.99987 5.47415L6.49947 5.47058L6.50575 11.9986L3.47746 12.0003L3.4995 5.50146L0.999867 5.47587L4.9942 1.62808e-05Z" fill="#010101"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-upload-file">  <path d="M6 1H14V6.34141C13.3744 6.12031 12.7013 6 12 6C8.68629 6 6 8.68629 6 12C6 13.0929 6.29218 14.1175 6.80269 15H2V5H6V1Z"></path>  <path d="M5 1L2 4H5V1Z"></path>  <path d="M12 8L9 11H11V14H13V11H15L12 8Z"></path>  <path d="M16 15V16H8V15H16Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-upload-folder">  <path d="M9 4h6l.001 2.803a5.971 5.971 0 00-1-.461L14 5H8.382l-1-2H2v10h4.083c.058.345.145.68.259 1H1V2h7l1 2z"></path>  <path d="M9 11l3-3 3 3h-2v3h-2v-3H9zM16 16v-1H8v1h8z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-upload">  <path d="M8 0L3 5h3v6h4V5h3L8 0zM1 13h14v2H1v-2z"></path></symbol><symbol viewBox="0 0 20 16" xmlns="http://www.w3.org/2000/svg" id="icon-variable">  <path d="M3.576 15.173C3.114 14.854 2.685 14.5075 2.289 14.1335C1.904 13.7595 1.5685 13.347 1.2825 12.896C0.9965 12.445 0.771 11.95 0.606 11.411C0.452 10.861 0.375 10.256 0.375 9.596C0.375 8.353 0.573 7.231 0.969 6.23C1.376 5.218 1.893 4.3215 2.52 3.5405C3.147 2.7485 3.84 2.072 4.599 1.511C5.369 0.938999 6.1115 0.477 6.8265 0.125L7.206 0.6365C6.656 1.0985 6.106 1.632 5.556 2.237C5.017 2.842 4.522 3.5185 4.071 4.2665C3.631 5.0035 3.2735 5.8175 2.9985 6.7085C2.7235 7.5885 2.586 8.5345 2.586 9.5465C2.586 10.0415 2.6135 10.5145 2.6685 10.9655C2.7235 11.4055 2.817 11.829 2.949 12.236C3.081 12.654 3.2515 13.0555 3.4605 13.4405C3.6695 13.8365 3.928 14.2325 4.236 14.6285L3.576 15.173Z"></path>  <path d="M8.95539 8.375C8.73539 8.628 8.49889 8.903 8.24589 9.2C7.99289 9.497 7.79489 9.783 7.65189 10.058C7.64089 10.146 7.63539 10.2615 7.63539 10.4045C7.63539 10.5475 7.64089 10.696 7.65189 10.85C7.66289 11.004 7.67389 11.1525 7.68489 11.2955C7.70689 11.4275 7.72889 11.5265 7.75089 11.5925C7.56389 11.6695 7.34389 11.7245 7.09089 11.7575C6.84889 11.7905 6.60689 11.807 6.36489 11.807C6.12289 11.807 5.89739 11.7905 5.68839 11.7575C5.47939 11.7245 5.31439 11.6695 5.19339 11.5925C5.29239 11.2625 5.47939 10.8995 5.75439 10.5035C6.04039 10.1075 6.35389 9.7225 6.69489 9.3485C7.04689 8.9635 7.39889 8.606 7.75089 8.276C8.11389 7.935 8.42189 7.6655 8.67489 7.4675L7.66839 4.7285L6.52989 4.5965V4.0355C6.68389 3.9475 6.86539 3.8595 7.07439 3.7715C7.29439 3.6835 7.51989 3.6065 7.75089 3.5405C7.98189 3.4745 8.21289 3.4195 8.44389 3.3755C8.68589 3.3315 8.90039 3.3095 9.08739 3.3095C9.37339 3.3095 9.58789 3.3865 9.73089 3.5405C9.88489 3.6835 10.0004 3.876 10.0774 4.118L10.8199 6.725C11.0289 6.505 11.2489 6.241 11.4799 5.933C11.7109 5.625 11.8869 5.3445 12.0079 5.0915C12.0189 5.0145 12.0189 4.9045 12.0079 4.7615C12.0079 4.6185 11.9969 4.47 11.9749 4.316C11.9639 4.151 11.9419 4.0025 11.9089 3.8705C11.8869 3.7275 11.8704 3.623 11.8594 3.557C12.2664 3.414 12.7119 3.3425 13.1959 3.3425C13.4159 3.3425 13.6304 3.3645 13.8394 3.4085C14.0484 3.4415 14.2134 3.491 14.3344 3.557C14.2354 3.887 14.0484 4.25 13.7734 4.646C13.5094 5.042 13.2124 5.427 12.8824 5.801C12.5524 6.175 12.2169 6.5215 11.8759 6.8405C11.5459 7.1485 11.2764 7.385 11.0674 7.55L12.1564 10.4375L13.2949 10.5695V11.1305C13.1849 11.2075 13.0309 11.29 12.8329 11.378C12.6349 11.455 12.4204 11.532 12.1894 11.609C11.9584 11.675 11.7219 11.73 11.4799 11.774C11.2379 11.829 11.0179 11.8565 10.8199 11.8565C10.5339 11.8565 10.3084 11.785 10.1434 11.642C9.97839 11.499 9.85739 11.3065 9.78039 11.0645L8.95539 8.375Z"></path>  <path d="M12.6656 14.6285C13.1606 14.2325 13.6776 13.7375 14.2166 13.1435C14.7666 12.5495 15.2616 11.8675 15.7016 11.0975C16.1526 10.3165 16.5211 9.464 16.8071 8.54C17.1041 7.605 17.2526 6.5985 17.2526 5.5205C17.2526 5.0585 17.2306 4.624 17.1866 4.217C17.1426 3.81 17.0546 3.414 16.9226 3.029C16.8016 2.644 16.6366 2.259 16.4276 1.874C16.2186 1.489 15.9491 1.0765 15.6191 0.6365L16.2296 0.125C17.3296 0.851 18.1436 1.6815 18.6716 2.6165C19.1996 3.5515 19.4636 4.6295 19.4636 5.8505C19.4636 7.0055 19.2711 8.078 18.8861 9.068C18.5121 10.047 18.0226 10.9325 17.4176 11.7245C16.8126 12.5165 16.1306 13.1985 15.3716 13.7705C14.6126 14.3535 13.8481 14.821 13.0781 15.173L12.6656 14.6285Z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-view">  <path d="M8 9a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"></path>  <path fill-rule="evenodd" clip-rule="evenodd" d="M16 8s-3.582 5-8 5-8-5-8-5 3.582-5 8-5 8 5 8 5zm-5 0a3 3 0 1 1-6 0 3 3 0 0 1 6 0z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-warning-red">  <path fill-rule="evenodd" clip-rule="evenodd" d="M.855 12.504A1 1 0 0 0 1.723 14h12.554a1 1 0 0 0 .868-1.496L8.868 1.52a1 1 0 0 0-1.736 0L.855 12.504zM9 5H7v1l.5 3h1L9 6V5zm0 6a1 1 0 1 1-2 0 1 1 0 0 1 2 0z" fill="#f53d2c"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-warning">  <path fill-rule="evenodd" clip-rule="evenodd" d="M.855 12.504A1 1 0 0 0 1.723 14h12.554a1 1 0 0 0 .868-1.496L8.868 1.52a1 1 0 0 0-1.736 0L.855 12.504zM9 5H7v1l.5 3h1L9 6V5zm0 6a1 1 0 1 1-2 0 1 1 0 0 1 2 0z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-workbook-alt">  <path d="M14 1v12H3.5a.5.5 0 1 0 0 1H14v1H3a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1h11zM9 6H5v1h4V6zm2-2H5v1h6V4z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-workbook-badged"><path class="icon" fill-rule="evenodd" clip-rule="evenodd" d="M3 1C2.44772 1 2 1.44772 2 2V14C2 14.5523 2.44772 15 3 15H7.99963C7.76849 14.6923 7.57202 14.357 7.41604 14H3.5C3.22386 14 3 13.7761 3 13.5C3 13.2239 3.22386 13 3.5 13H7.10002C7.03443 12.6769 7 12.3425 7 12C7 9.23858 9.23858 7 12 7C12.7111 7 13.3875 7.14845 14 7.41604V1H3ZM5 4H11V5H5V4ZM9 6H5V7H9V6Z"></path><circle class="badge" cx="12" cy="12" r="4"></circle></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-workbooks">    <path d="M9 4h6v2H1V2h7l1 2zM1 7v7h14V7H1z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-worksheet">  <path d="M2 3h12v2H2V3zm0 4h12v2H2V7zm8 4H2v2h8v-2z"></path></symbol><symbol viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" id="icon-zpl-notebook">    <path d="M14 1v12H3.5a.5.5 0 1 0 0 1H14v.999H3a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1h11zM6.08 2.477h-2.7v.72h1.626v.047L3.353 5.43V6H6.13v-.72H4.427v-.047L6.08 3.046v-.569zm2.329 0H6.866V6h.896V4.967h.593c.784 0 1.323-.49 1.323-1.24 0-.757-.512-1.25-1.27-1.25zm2.822 0h-.896V6h2.393v-.74H11.23V2.477zm-3.059.689c.379 0 .6.192.6.563 0 .367-.224.562-.605.562h-.405V3.166h.41z"></path></symbol><symbol viewBox="0 0 301 384" xmlns="http://www.w3.org/2000/svg" id="image-Datalore-vert">  <path d="M71.7112 299.356H58.8445V332.689H71.7112C82.0889 332.689 89.2445 325.4 89.2445 315.978C89.2445 306.667 82.0889 299.356 71.7112 299.356ZM81.6445 316.156C81.7179 317.481 81.5116 318.808 81.039 320.049C80.5663 321.289 79.838 322.417 78.9012 323.358C77.9644 324.299 76.8401 325.032 75.6014 325.51C74.3627 325.989 73.0372 326.201 71.7112 326.133H66.1112V305.978H71.7112C73.0425 305.92 74.3712 306.141 75.6116 306.629C76.852 307.116 77.9765 307.858 78.9125 308.806C79.8485 309.755 80.5752 310.889 81.0458 312.136C81.5163 313.382 81.7203 314.714 81.6445 316.044V316.156ZM102 306.889C98.6204 306.816 95.2687 307.515 92.2 308.933L94 314.489C96.2046 313.572 98.5678 313.096 100.956 313.089C104.556 313.089 106.378 314.756 106.378 317.778V318.2C104.405 317.488 102.32 317.134 100.222 317.156C94.2223 317.156 90.0445 319.733 90.0445 325.311C90.0445 330.378 93.9556 333.156 98.7111 333.156C100.143 333.217 101.571 332.957 102.889 332.396C104.208 331.834 105.385 330.985 106.333 329.911V332.667H113.333V317.822C113.436 316.35 113.248 314.872 112.779 313.472C112.31 312.073 111.57 310.78 110.6 309.667C109.427 308.65 108.06 307.879 106.583 307.402C105.105 306.925 103.547 306.75 102 306.889ZM106.444 323.733C106.444 326.356 104.222 328.178 100.822 328.178C98.6 328.178 96.9112 327.044 96.9112 325.089V324.978C96.9112 322.756 98.8 321.444 101.867 321.444C103.442 321.443 105.001 321.769 106.444 322.4V323.733ZM125.2 300.644H118.089V307.178H115.067V313.333H118.089V325.467C118.089 331.378 121.044 333.156 125.422 333.156C127.415 333.211 129.381 332.695 131.089 331.667V325.844C130.009 326.447 128.792 326.76 127.556 326.756C125.956 326.756 125.333 325.933 125.333 324.267V313.333H131.111V307.133H125.244L125.2 300.644ZM145.2 306.889C141.82 306.816 138.469 307.515 135.4 308.933L137.178 314.489C139.389 313.569 141.76 313.094 144.156 313.089C147.733 313.089 149.578 314.756 149.578 317.778V318.2C147.597 317.489 145.505 317.135 143.4 317.156C137.422 317.156 133.222 319.733 133.222 325.311C133.222 330.378 137.133 333.156 141.889 333.156C143.324 333.215 144.754 332.955 146.076 332.394C147.398 331.833 148.579 330.985 149.533 329.911V332.667H156.444V317.822C156.548 316.35 156.359 314.872 155.89 313.472C155.421 312.073 154.681 310.78 153.711 309.667C152.554 308.659 151.206 307.894 149.748 307.417C148.29 306.94 146.751 306.76 145.222 306.889H145.2ZM149.644 323.733C149.644 326.356 147.422 328.178 144.044 328.178C141.822 328.178 140.133 327.044 140.133 325.089V324.978C140.133 322.756 142.022 321.444 145.067 321.444C146.643 321.439 148.202 321.764 149.644 322.4V323.733ZM160 332.756H167.156V297.911H160V332.756ZM183.933 306.667C182.151 306.616 180.376 306.924 178.715 307.571C177.053 308.219 175.539 309.193 174.26 310.436C172.982 311.679 171.966 313.166 171.272 314.809C170.579 316.452 170.222 318.217 170.222 320C170.222 323.625 171.662 327.101 174.225 329.664C176.788 332.227 180.264 333.667 183.889 333.667C187.514 333.667 190.99 332.227 193.553 329.664C196.116 327.101 197.556 323.625 197.556 320C197.556 318.224 197.202 316.467 196.514 314.83C195.826 313.193 194.818 311.71 193.549 310.468C192.28 309.226 190.776 308.25 189.125 307.598C187.473 306.945 185.708 306.628 183.933 306.667V306.667ZM190.6 320C190.662 320.906 190.535 321.815 190.226 322.669C189.917 323.523 189.433 324.303 188.806 324.959C188.179 325.616 187.421 326.135 186.582 326.482C185.743 326.83 184.841 326.998 183.933 326.978C183.023 326.979 182.122 326.795 181.286 326.435C180.45 326.075 179.697 325.548 179.072 324.886C178.447 324.224 177.965 323.441 177.655 322.585C177.344 321.73 177.212 320.82 177.267 319.911C177.204 319.006 177.332 318.098 177.641 317.245C177.95 316.393 178.434 315.614 179.062 314.959C179.69 314.304 180.447 313.788 181.286 313.443C182.125 313.098 183.027 312.932 183.933 312.956C184.844 312.954 185.744 313.139 186.58 313.498C187.417 313.858 188.17 314.385 188.795 315.047C189.419 315.709 189.902 316.492 190.212 317.348C190.523 318.204 190.655 319.114 190.6 320.022V320ZM207.711 312.222V307.067H200.444V332.644H207.6V323.2C207.6 317.089 210.511 314.178 215.289 314.178H215.667V306.667C213.877 306.547 212.1 307.043 210.632 308.075C209.164 309.106 208.094 310.609 207.6 312.333L207.711 312.222ZM241.289 320.489C241.289 313.222 237.445 306.578 229 306.578C227.294 306.599 225.61 306.965 224.049 307.654C222.488 308.342 221.082 309.339 219.916 310.584C218.749 311.83 217.846 313.298 217.261 314.9C216.676 316.503 216.421 318.207 216.511 319.911C216.439 321.665 216.731 323.414 217.369 325.05C218.007 326.685 218.976 328.17 220.216 329.413C221.456 330.655 222.94 331.627 224.574 332.267C226.208 332.907 227.957 333.202 229.711 333.133C231.684 333.202 233.646 332.805 235.437 331.975C237.228 331.145 238.799 329.905 240.022 328.356L235.933 324.689C235.151 325.53 234.201 326.198 233.145 326.65C232.088 327.102 230.949 327.327 229.8 327.311C228.329 327.399 226.878 326.932 225.734 326.002C224.59 325.072 223.837 323.747 223.622 322.289H241.2C241.133 321.822 241.178 321.156 241.178 320.6L241.289 320.489ZM223.511 317.844C224.067 314.556 226 312.4 228.978 312.4C230.401 312.435 231.754 313.023 232.75 314.04C233.746 315.056 234.306 316.421 234.311 317.844H223.511Z" fill="black"></path>  <path d="M242.407 67.5035C239.747 66.1093 236.889 65.1314 233.932 64.6038C232.145 64.6038 118.152 42.7564 112.13 42.3098C109.23 42.0865 106.108 42.3098 103.208 42.7564C50.334 50.5588 36.9497 114.991 80.6754 141.968C90.937 148.211 103.205 150.44 115.029 147.764C135.776 143.304 229.023 120.34 235.045 119.004C260.924 113.431 266.499 80.2086 242.41 67.5035H242.407Z" fill="url(#paint0_linear)"></path>  <path d="M244.297 166.159C239.818 161.059 158.748 69.9534 141.505 55.1019C138.146 52.2189 134.116 49.5592 129.637 47.1195C121.59 42.9127 112.417 41.3621 103.435 42.69C55.5098 50.0025 39.8326 102.979 69.6174 132.909C72.7502 136.232 161.884 234.214 162.781 235.324C166.814 240.2 171.739 244.856 178.012 248.622C188.31 255.051 200.851 257.044 212.946 254.388C256.838 244.633 270.949 195.642 244.297 166.159Z" fill="url(#paint1_linear)"></path>  <path d="M226.671 153.32C224.892 152.434 223.116 151.544 221.116 150.877C219.56 150.434 100.027 112.658 97.3608 111.992C92.9299 110.885 88.3247 110.659 83.8066 111.325C41.1473 117.548 30.2592 169.765 65.5864 191.762C73.8083 196.871 182.899 251.532 185.789 252.642C194.244 255.781 203.428 256.399 212.227 254.421C263.332 243.309 273.773 177.984 226.671 153.32V153.32Z" fill="url(#paint2_linear)"></path>  <path d="M242.445 67.329C238.446 65.1093 233.78 64.4427 229.114 65.1093C226.671 65.5526 224.449 65.9959 222.226 66.8857C211.784 71.1086 74.918 113.104 71.142 114.88C39.3709 128.655 34.2585 172.206 65.5863 191.761C73.9371 196.949 83.9998 198.626 93.5814 196.427C97.3607 195.537 101.137 194.427 104.246 192.871C121.133 184.872 241.336 116.88 243.778 115.547C261.775 105.104 263.332 78.4411 242.445 67.329V67.329Z" fill="url(#paint3_linear)"></path>  <path d="M83.3334 83.3333H216.667V216.667H83.3334V83.3333Z" fill="black"></path>  <path d="M99.9556 191.467H149.956V199.8H99.9556V191.467Z" fill="white"></path>  <path d="M100 99.8223H119.556C135.311 99.8223 146.222 110.645 146.222 124.756V124.911C146.222 139.022 135.333 149.978 119.556 149.978H100V99.8223ZM111.111 109.778V140H119.644C121.648 140.118 123.655 139.813 125.532 139.103C127.41 138.394 129.118 137.297 130.543 135.884C131.969 134.471 133.081 132.774 133.807 130.902C134.533 129.031 134.856 127.027 134.756 125.022V124.889C134.857 122.877 134.536 120.865 133.813 118.985C133.09 117.104 131.981 115.396 130.557 113.97C129.134 112.544 127.427 111.433 125.547 110.707C123.668 109.981 121.657 109.657 119.644 109.756L111.111 109.778Z" fill="white"></path>  <path d="M153.333 99.8668H164.444V140.733H186.378V150H153.333V99.8668Z" fill="white"></path>  <defs>    <linearGradient id="paint0_linear" x1="109.117" y1="95.2701" x2="239.078" y2="121.188" gradientUnits="userSpaceOnUse">      <stop offset="0.242" stop-color="#3BEA62"></stop>      <stop offset="0.857" stop-color="#FCF84A"></stop>    </linearGradient>    <linearGradient id="paint1_linear" x1="95.3963" y1="57.1916" x2="218.891" y2="246.953" gradientUnits="userSpaceOnUse">      <stop offset="0.018" stop-color="#3BEA62"></stop>      <stop offset="0.786" stop-color="#087CFA"></stop>    </linearGradient>    <linearGradient id="paint2_linear" x1="94.1014" y1="162.172" x2="251.519" y2="219.027" gradientUnits="userSpaceOnUse">      <stop offset="0.121" stop-color="#1FAEB5"></stop>      <stop offset="0.975" stop-color="#087CFA"></stop>    </linearGradient>    <linearGradient id="paint3_linear" x1="48.8159" y1="171.033" x2="252.151" y2="80.9189" gradientUnits="userSpaceOnUse">      <stop offset="0.121" stop-color="#1FAEB5"></stop>      <stop offset="0.856" stop-color="#FCF84A"></stop>    </linearGradient>  </defs></symbol><symbol viewBox="0 0 36 36" xmlns="http://www.w3.org/2000/svg" id="image-brackets">    <defs>        <filter id="a" width="127.3%" height="400%" x="-13.6%" y="-150%" filterUnits="objectBoundingBox">            <feGaussianBlur in="SourceGraphic" stdDeviation="1"></feGaussianBlur>        </filter>    </defs>    <g fill="none" fill-rule="evenodd">        <g fill="#9E9E9E" transform="translate(6 1)">            <path d="M23.864 13.472c0 .19-.185.32-.556.392l-.148.024c-.875.128-1.504.533-1.888 1.216-.295.532-.454 1.4-.477 2.604l-.003.308c0 .299.012.697.036 1.195l.088 1.642c.024.498.036.896.036 1.195 0 1.088-.288 2.07-.864 2.944-.576.875-1.301 1.45-2.176 1.728-.47.15-1.205.224-2.208.224-.47 0-.704-.096-.704-.288 0-.192.352-.288 1.056-.288.832 0 1.413-.24 1.744-.72.33-.48.496-1.285.496-2.416l-.004-.304a62.592 62.592 0 0 0-.032-.992l-.092-2.401v-.047c0-2.24.65-3.893 1.952-4.96a4.25 4.25 0 0 1 1.984-.928c.107-.043.16-.085.16-.128 0-.068-.041-.11-.123-.123l-.069-.005c-.512-.021-1.077-.277-1.696-.768-1.472-1.152-2.208-2.71-2.208-4.672 0-.365.013-.866.039-1.502l.07-1.668c.012-.4.019-.73.019-.99 0-2.176-.63-3.232-1.888-3.168l-.736.032c-.384.021-.576-.075-.576-.288 0-.213.277-.32.832-.32.81 0 1.504.096 2.08.288a3.915 3.915 0 0 1 2.16 1.696c.523.832.784 1.813.784 2.944l-.004.35a43.44 43.44 0 0 1-.044 1.19l-.076 1.482c-.02.443-.032.81-.035 1.1l-.001.166c0 1.45.24 2.437.72 2.96.427.465.9.74 1.42.825l.196.023c.49.043.736.192.736.448z"></path>            <path fill-rule="nonzero" d="M8.832.288c0 .176-.287.271-.86.286l-.164.002c-.81 0-1.387.24-1.728.72-.313.44-.482 1.135-.508 2.086l-.004.266c0 .332.013.793.039 1.383l.07 1.548c.012.37.019.672.019.909 0 2.197-.661 3.84-1.984 4.928-.597.49-1.248.8-1.952.928-.107.021-.16.064-.16.128 0 .068.041.11.123.123l.069.005c.512.021 1.077.277 1.696.768 1.472 1.13 2.208 2.677 2.208 4.64l-.013.759c-.006.222-.015.47-.026.743l-.07 1.668c-.01.32-.016.595-.018.825l-.001.165c0 2.176.619 3.243 1.856 3.2l.768-.032c.384-.021.576.075.576.288 0 .213-.299.32-.896.32-.79 0-1.461-.096-2.016-.288-.896-.32-1.61-.896-2.144-1.728-.533-.832-.8-1.792-.8-2.88 0-.313.012-.735.036-1.266l.088-1.756c.024-.531.036-.953.036-1.266 0-1.472-.24-2.47-.72-2.992-.48-.523-1.03-.805-1.648-.848-.47-.064-.704-.213-.704-.448 0-.213.235-.352.704-.416.917-.15 1.557-.555 1.92-1.216.32-.576.48-1.547.48-2.912 0-.53-.02-1.103-.061-1.72l-.077-1.039a20.204 20.204 0 0 1-.054-1.305c0-1.067.288-2.037.864-2.912.576-.875 1.301-1.45 2.176-1.728C6.442.074 7.179 0 8.16 0c.448 0 .672.096.672.288z"></path>            <ellipse cx="12" cy="33" fill-opacity=".5" filter="url(#a)" rx="11" ry="1"></ellipse>        </g>    </g></symbol><symbol viewBox="0 0 36 36" xmlns="http://www.w3.org/2000/svg" id="image-conda-logo"><g filter="url(#prefix__filter0_f)"><path fill-rule="evenodd" clip-rule="evenodd" d="M18 33c6.075 0 11-.448 11-1s-4.925-1-11-1-11 .448-11 1 4.925 1 11 1z" fill="#9E9E9E" fill-opacity=".5"></path></g><path d="M23.28 2.354a8.172 8.172 0 00-1.758 1.275 8.325 8.325 0 00-1.38-1.627c1.11 0 2.137.108 3.138.352zM24.282 2.68a2.655 2.655 0 00-.433-.136c.162.027.297.081.433.136zM20.737 4.523a7.868 7.868 0 00-1.109 1.925 7.224 7.224 0 00-1.488-1.762 7.174 7.174 0 011.11-1.952 6.473 6.473 0 011.487 1.79zM18.87 7.262c-.162-.298-.487-.895-1.055-1.464a6.477 6.477 0 00-.162 1.87c-.027 0 .514-.27 1.217-.406zM16.354 8.4a6.835 6.835 0 00-1.704-1.03c.216.895.568 1.546.757 1.871 0 .021.058-.036.163-.14.163-.162.438-.436.784-.7zM14.623 10.353a8.775 8.775 0 00-2.3-.136c.594.84 1.269 1.381 1.648 1.626 0 .002 0 .003.002.001l-.002-.001c-.003-.044.214-.742.652-1.49zM13.107 12.305c-.622.082-1.542.353-2.516.976a6.077 6.077 0 01-1.677-1.898 6.53 6.53 0 012.435-1.03c.568.895 1.271 1.546 1.758 1.952zM13.703 13.037a5.265 5.265 0 00-2.408.76 8.468 8.468 0 002.408 1.03 6.602 6.602 0 010-1.79zM14.623 4.062c.947.217 1.704.57 2.3.976a8.823 8.823 0 00-.352 2.332 7.573 7.573 0 00-2.11-1.084 7.189 7.189 0 01.162-2.224zM25.256 3.06s.757 2.331.784 3.524c-.92.217-1.731.542-2.624 1.302.487.244.92.542 1.325.894.433.38.84.543 1.407.271.325-.216 2.138-2.087 2.327-2.331.433-.461.325-1.22-.135-1.573-1.136-1.058-3.084-2.088-3.084-2.088zM10.889 9.54c-.812.19-1.623.542-2.435 1.084a12.611 12.611 0 011.786-3.633c.054.976.297 1.816.649 2.549zM14.406 9.431a8.604 8.604 0 01-.812-2.386 6.764 6.764 0 00-2.489-.108 6.26 6.26 0 00.677 2.467 8.235 8.235 0 012.624.027zM8.21 11.736a7.616 7.616 0 001.732 2.033 7.292 7.292 0 00-1.786 2.17 12.192 12.192 0 01.054-4.203z" fill="#43B02A"></path><path d="M23.984 3.276A6.469 6.469 0 0022.09 4.66c.406.868.595 1.654.704 2.142a8.352 8.352 0 011.975-1.139c-.054-.542-.244-1.545-.785-2.386zM20.575 7.126c.108-.298.325-.84.703-1.437.271.705.406 1.275.433 1.6a8.192 8.192 0 00-1.136-.163zM18.356 2.164a12.839 12.839 0 00-3.244.948c.848.217 1.55.55 2.135.923a8.494 8.494 0 011.11-1.87zM13.486 6.042a9.04 9.04 0 01.185-2.173c-.677.415-1.312.897-1.89 1.44-.225.206-.443.423-.652.65.208-.005 1.703-.043 2.357.083z" fill="#43B02A"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M28.123 20.765a23.924 23.924 0 01-.904-.921c-.992-1.05-1.448-1.534-2.586-.652-3.923 3.091-9.578 1.248-10.768-3.552-.216-.027-1.732-.325-3.274-1.382-.757.596-1.542 1.518-2.191 2.847h-.027c2.462 9.327 14.447 11.496 19.994 5.667.839-.89.215-1.532-.147-1.906a5.521 5.521 0 01-.096-.1zm-7.765 1.491c-3.733 0-6.764-3.064-7.63-5.368 0 0-.784-.027-1.84-.461 0 0-.46.65-.784 1.735 3.95 7.457 12.31 8.08 17.235 3.769 0 0 0-.027-.081-.136l-.3-.326c-.468-.512-1.128-1.235-1.215-1.192a8.227 8.227 0 01-5.384 1.98z" fill="#43B02A"></path><defs><filter id="prefix__filter0_f" x="4.282" y="28.282" width="27.436" height="7.436" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB"><feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood><feBlend in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend><feGaussianBlur stdDeviation="1.359" result="effect1_foregroundBlur"></feGaussianBlur></filter></defs></symbol><symbol viewBox="0 0 36 36" xmlns="http://www.w3.org/2000/svg" id="image-pip-logo"><g filter="url(#prefix__filter0_f)"><path fill-rule="evenodd" clip-rule="evenodd" d="M18 33c6.075 0 11-.448 11-1s-4.925-1-11-1-11 .448-11 1 4.925 1 11 1z" fill="#9E9E9E" fill-opacity=".5"></path></g><path d="M18.922 21.883a.917.917 0 01-.67-.26.901.901 0 01-.255-.657c0-.265.085-.48.256-.647.177-.174.4-.26.669-.26.297 0 .549-.101.754-.303.213-.209.319-.459.319-.75a.981.981 0 00-.319-.741 1.036 1.036 0 00-.754-.303c-.298 0-.55.101-.755.303a.997.997 0 00-.308.74v4.077a.882.882 0 01-.265.657.916.916 0 01-.67.261.917.917 0 01-.669-.26.901.901 0 01-.255-.658v-4.077c0-.813.28-1.494.84-2.044.559-.549 1.253-.823 2.082-.823s1.523.274 2.082.823c.567.55.85 1.23.85 2.044 0 .814-.283 1.498-.85 2.054-.56.55-1.253.824-2.082.824zM24.664 21.602a.916.916 0 01-.67.26.917.917 0 01-.669-.26.866.866 0 01-.255-.647v-6.048c0-.264.085-.48.255-.646.177-.174.4-.261.67-.261.269 0 .492.087.669.26a.848.848 0 01.266.647v6.048c0 .264-.089.48-.266.647zM29.067 21.883a.917.917 0 01-.669-.26.901.901 0 01-.255-.657c0-.265.085-.48.255-.647.177-.174.4-.26.67-.26.297 0 .548-.101.754-.303.212-.209.319-.459.319-.75a.981.981 0 00-.32-.741 1.036 1.036 0 00-.754-.303c-.297 0-.549.101-.754.303a.997.997 0 00-.308.74v4.077a.882.882 0 01-.266.657.917.917 0 01-.669.261.917.917 0 01-.67-.26.901.901 0 01-.254-.658v-4.077c0-.813.28-1.494.839-2.044.56-.549 1.254-.823 2.082-.823.83 0 1.523.274 2.083.823.567.55.85 1.23.85 2.044 0 .814-.283 1.498-.85 2.054-.56.55-1.254.824-2.082.824z" fill="#474747"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M15 7v2a1.5 1.5 0 01-1.5 1.5h-5a.5.5 0 00-.5.5v4.703c0 .384.218.74.578.873.74.273 1.56.424 2.422.424.862 0 1.681-.151 2.422-.424.36-.133.578-.489.578-.873V14h-3v-1h5.703c.384 0 .74-.218.873-.578.273-.74.424-1.56.424-2.422 0-.862-.151-1.681-.424-2.422-.133-.36-.489-.578-.873-.578H15zm-2.5 9a.5.5 0 100-1 .5.5 0 000 1z" fill="#FFDA4C"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M14 4.297c0-.384-.218-.74-.578-.873A7.013 7.013 0 0011 3c-.862 0-1.681.151-2.422.424-.36.133-.578.489-.578.873V6h3v1H5.297c-.384 0-.74.218-.873.578A7.013 7.013 0 004 10c0 .862.151 1.681.424 2.422.133.36.489.578.873.578H7v-2a1.5 1.5 0 011.5-1.5h5A.5.5 0 0014 9V4.297zM9.5 5a.5.5 0 100-1 .5.5 0 000 1z" fill="#3B77A8"></path><defs><filter id="prefix__filter0_f" x="4.282" y="28.282" width="27.436" height="7.436" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB"><feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood><feBlend in="SourceGraphic" in2="BackgroundImageFix" result="shape"></feBlend><feGaussianBlur stdDeviation="1.359" result="effect1_foregroundBlur"></feGaussianBlur></filter></defs></symbol><symbol viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" id="image-status-changed">  <circle cx="12" cy="12" r="12" fill="#008DC0"></circle>  <path fill-rule="evenodd" clip-rule="evenodd" d="M14.25 6H12.75C9.85051 6 7.5 8.35051 7.5 11.25H6L8.625 14.25L11.25 11.25H9.75C9.75 9.59315 11.0931 8.25 12.75 8.25H14.25V6ZM9.75 18H11.25C14.1495 18 16.5 15.6495 16.5 12.75H18L15.375 9.75L12.75 12.75H14.25C14.25 14.4069 12.9069 15.75 11.25 15.75H9.75V18Z" fill="white"></path></symbol><symbol viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" id="image-status-valid">  <circle cx="12" cy="12" r="12" fill="#3CA813"></circle>  <path d="M10.6768 13.0768L15.9 7.85355L17.3464 9.3L10.5 16.1464L6.35355 12L7.8 10.5536L10.3232 13.0768L10.5 13.2536L10.6768 13.0768Z" fill="white" stroke="white" stroke-width="0.5"></path></symbol></svg></div><style>.authTokens__title {
  font-size: 14px;
}
.authTokens__separator {
  margin: 15px 0;
  border-bottom: 1px solid var(--main-color-2);
}
.authTokens__tokensList {
  list-style: none;
  display: block;
  width: 600px;
  margin: 0 4px 20px;
}
.authTokens__newToken {
  margin: 0;
}
.authTokens__token {
  height: 30px;
  padding: 0 10px;
  background-color: var(--main-color-1);
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.authTokens__token:nth-child(2n) {
  background-color: var(--main-color-2);
}
.authTokens__downloadToken {
  text-decoration: none;
  padding: 0 5px;
}
.authTokens__revokeToken {
  cursor: pointer;
}
.icon {
  display: inline-block;
  width: 16px;
  height: 16px;
  background: no-repeat center;
  background-size: contain;
}
.icon-container {
  display: block;
  width: 0;
  height: 0;
  position: absolute;
  overflow: hidden;
}
.icon-container symbol[id^='icon'] path,
.icon-container symbol[id^='icon'] g {
  fill: inherit;
}
.icon-size-xs {
  width: 10px;
  height: 10px;
}
.icon-size-s {
  width: 12px;
  height: 12px;
}
.icon-size-l {
  width: 22px;
  height: 22px;
}
.icon-size-xl {
  width: 36px;
  height: 36px;
}
.icon-arrow-left {
  transform: rotate(180deg);
}
.icon-arrow-down {
  transform: rotate(90deg);
}
.icon-arrow-up {
  transform: rotate(-90deg);
}
.icon-flyout-right {
  transform: rotate(-90deg);
}
.icon-undo {
  transform: rotate(90deg) scale(1, -1);
}
.icon-redo {
  transform: rotate(90deg);
}
.icon use,
.icon g {
  fill: var(--main-color-8);
}
.icon-light use,
.icon-light g {
  fill: var(--contrast-fg);
}
.icon-active use,
.icon-active g {
  fill: var(--action-color-2);
}
.icon-muted {
  opacity: 0.5;
}
.icon-positive use,
.icon-positive g {
  fill: var(--positive-color-2);
}
.icon-negative use,
.icon-negative g {
  fill: var(--negative-color-2);
}
.alert_container {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  z-index: 1101;
  right: 2px;
  bottom: 26px;
  position: fixed;
}
.alert_container > div {
  transition: opacity 0.2s ease-out;
}
.alert-animated > div {
  transition: transform 0.5s ease-out, opacity 0.2s ease-out;
}
.alert_content {
  display: inline-block;
  max-width: 100%;
}
.alert_message {
  position: relative;
  background: var(--alert-bg);
  color: var(--contrast-fg);
  padding: 24px;
  margin: 6px;
  width: 250px;
  opacity: 0;
}
.alert_message-error {
  background: rgba(var(--negative-color-3-rgb), 0.8);
}
.alert_message-error a {
  color: var(--action-color-1);
}
.alert_message-error a:not([disabled]):hover {
  color: var(--action-color-1);
  text-decoration: underline;
}
.alert_message-flex {
  min-width: 285px;
  width: auto;
}
.alert_close.icon {
  position: absolute;
  right: 6px;
  top: 6px;
}
.alert_progress {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-column-gap: 10px;
  align-items: center;
}
.alert_with_icon {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-column-gap: 8px;
}
.alert_action-message {
  margin: 0 0 8px 0;
}
.alert_action_progress {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-column-gap: 10px;
}
.alert_button-full-size.button {
  width: 100%;
  margin: 10px 0 0;
}
.fs-entity-line {
  /* list item */
  border: 0px solid var(--border-color);
  border-bottom-width: 1px;
  border-top-width: 1px;
  margin: -1px 0 0;
  display: flex;
  height: 46px;
  position: relative;
  padding: 0 2px;
  align-items: center;
  cursor: default;
  list-style: none;
  outline: none;
  /* selected */
  /* common styles */
}
.fs-entity-line:first-child {
  margin-top: 0px;
}
.fs-entity-line.hover,
.fs-entity-line:hover {
  background: var(--main-color-1);
}
.fs-entity-line.selected {
  z-index: 1;
}
.fs-entity-line .fs-entity_status {
  position: absolute;
  top: 6px;
  left: 26px;
}
.fs-entity-line .fs-entity_icon-wrapper {
  margin: 0 12px 0 4px;
}
.fs-entity-line.selected {
  background: var(--main-color-8);
  color: var(--primary-bg);
}
.fs-entity-line_column-name {
  display: flex;
  flex-basis: 50%;
  flex-shrink: 0;
  align-items: center;
  cursor: default;
  font-size: 14px;
}
.fs-entity-line_column-owner {
  flex-basis: 20%;
  flex-shrink: 0;
}
.fs-entity-line_column-date {
  cursor: default;
  flex-basis: 30%;
  flex-shrink: 1;
}
.fs-entity-line_column-name,
.fs-entity-line_column-date,
.fs-entity-line_column-owner {
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow: hidden;
  margin-right: 15px;
}
.dl-computation {
  position: relative;
}
.dl-computation_column-name,
.dl-computation_column-user,
.dl-computation_column-agent-type,
.dl-computation_column-users-count {
  margin-left: 17px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.dl-computation_column-name {
  display: flex;
  align-items: center;
  flex-basis: 23%;
}
.dl-computation_column-user {
  flex-basis: 15%;
}
.dl-computation_column-agent-type {
  flex-basis: 25%;
}
.dl-computation_column-users-count {
  flex-basis: 12%;
}
.dl-computation_column-computation-status {
  flex-basis: 15%;
}
.dl-computation_column-stop {
  position: relative;
  text-align: center;
  flex-basis: 10%;
  height: 15px;
}
.dl-computation_stop-button {
  color: var(--negative-color-2);
  outline: none;
}
.dl-computation_stopped {
  color: var(--main-color-7);
}
.dl-computation_stop-button,
.dl-computation_stopping {
  height: auto;
}
.dl-computation_status {
  position: absolute;
  top: 6px;
  left: 26px;
}
.dl-computations {
  display: flex;
  flex-direction: column;
  height: 100%;
  position: relative;
}
.dl-computations_list {
  flex-grow: 1;
  overflow: auto;
}
.dl-computations_header {
  display: flex;
  height: 42px;
  align-items: center;
  border-bottom: 1px solid var(--border-color);
  margin-bottom: -1px;
  font-weight: bold;
}
.dl-computations_empty-label,
.dl-computations_loading-label {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  color: var(--main-color-7);
}
.computations_popup_header {
  display: flex;
  gap: 8px;
}
.computations_popup_header .popup_link {
  color: var(--contrast-fg);
}
.computations_popup_header .popup_link:hover {
  color: var(--contrast-fg);
  text-decoration: underline;
}
@font-face {
  font-family: 'JetBrains Mono';
  font-style: normal;
  font-weight: 400;
  font-display: fallback;
  src: local("JetBrains Mono dev Regular"), local("JetBrainsMonodev-Regular"), local("JetBrains Mono Regular"), local("JetBrainsMono-Regular"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Regular.woff2") format("woff2"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Regular.woff") format("woff");
}
@font-face {
  font-family: 'JetBrains Mono';
  font-style: italic;
  font-weight: 400;
  font-display: fallback;
  src: local("JetBrains Mono dev Italic"), local("JetBrainsMonodev-Italic"), local("JetBrains Mono Italic"), local("JetBrainsMono-Italic"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Italic.woff2") format("woff2"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Italic.woff") format("woff");
}
@font-face {
  font-family: 'JetBrains Mono';
  font-style: normal;
  font-weight: 500;
  font-display: fallback;
  src: local("JetBrains Mono dev Medium"), local("JetBrainsMonodev-Medium"), local("JetBrains Mono Medium"), local("JetBrainsMono-Medium"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Medium.woff2") format("woff2"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Medium.woff") format("woff");
}
@font-face {
  font-family: 'JetBrains Mono';
  font-style: italic;
  font-weight: 500;
  font-display: fallback;
  src: local("JetBrains Mono dev Medium Italic"), local("JetBrainsMonodev-Medium-Italic"), local("JetBrains Mono Medium Italic"), local("JetBrainsMono-Medium-Italic"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Medium-Italic.woff2") format("woff2"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Medium-Italic.woff") format("woff");
}
@font-face {
  font-family: 'JetBrains Mono';
  font-style: normal;
  font-weight: 700;
  font-display: fallback;
  src: local("JetBrains Mono dev Bold"), local("JetBrainsMonodev-Bold"), local("JetBrains Mono Bold"), local("JetBrainsMono-Bold"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Bold.woff2") format("woff2"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Bold.woff") format("woff");
}
@font-face {
  font-family: 'JetBrains Mono';
  font-style: italic;
  font-weight: 700;
  font-display: fallback;
  src: local("JetBrains Mono dev Bold Italic"), local("JetBrainsMonodev-Bold-Italic"), local("JetBrains Mono Bold Italic"), local("JetBrainsMono-Bold-Italic"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-Bold-Italic.woff2") format("woff2"), url("/assets/fonts/JetBrainsMono//JetBrainsMono-Bold-Italic.woff") format("woff");
}
@font-face {
  font-family: 'JetBrains Mono';
  font-style: normal;
  font-weight: 800;
  font-display: fallback;
  src: local("JetBrains Mono dev ExtraBold"), local("JetBrainsMonodev-ExtraBold"), local("JetBrains Mono ExtraBold"), local("JetBrainsMono-ExtraBold"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-ExtraBold.woff2") format("woff2"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-ExtraBold.woff") format("woff");
}
@font-face {
  font-family: 'JetBrains Mono';
  font-style: italic;
  font-weight: 800;
  font-display: fallback;
  src: local("JetBrains Mono dev ExtraBold Italic"), local("JetBrainsMonodev-ExtraBold-Italic"), local("JetBrains Mono ExtraBold Italic"), local("JetBrainsMono-ExtraBold-Italic"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-ExtraBold-Italic.woff2") format("woff2"), url("/assets/fonts/JetBrainsMono/JetBrainsMono-ExtraBold-Italic.woff") format("woff");
}
.text-wrap {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
/* TODO: strange font-family */
/* TODO: migrate from font variables to mixins */
.breadcrumbs {
  display: flex;
  align-items: center;
  cursor: pointer;
}
.breadcrumbs_item {
  vertical-align: middle;
  transition: opacity 100ms ease-in;
}
.breadcrumbs_item:hover {
  opacity: 1;
}
.breadcrumbs_item .icon {
  cursor: default;
}
.breadcrumbs_item .icon use,
.breadcrumbs_item .icon g {
  fill: var(--main-color-5);
}
.breadcrumbs_item a:not([disabled]) {
  color: var(--main-color-8);
}
.breadcrumbs_item a:not([disabled]):hover {
  color: var(--main-color-8);
  border-bottom-color: var(--main-color-8);
}
.breadcrumbs_item:not(:hover):not(:last-child) {
  opacity: .5;
}
.clipboard-area {
  position: relative;
  display: flex;
  align-items: center;
}
.clipboard-area > .clipboard-text {
  padding-bottom: 24px;
  border: 1px solid var(--border-color);
}
.clipboard-area > .button {
  position: absolute;
  bottom: 8px;
  right: 16px;
}
.clipboard-input {
  position: relative;
  display: flex;
  align-items: stretch;
  width: 100%;
}
.clipboard-input .input {
  width: 100%;
  border: none;
  background-color: transparent;
  text-overflow: ellipsis;
  overflow: hidden;
  margin: 0;
  cursor: pointer;
}
.clipboard-input > .clipboard-text {
  border-right-color: transparent;
}
.clipboard-input > .clipboard-text + .button {
  height: 32px;
  margin: 0;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
.clipboard-input_actions {
  display: flex;
  align-items: center;
  padding: 0 8px;
  border: 1px solid var(--border-color);
  background: var(--main-color-1);
  border-left-color: transparent;
}
.clipboard-input_action {
  width: 16px;
  height: 16px;
  cursor: pointer;
}
.clipboard-input_action .icon use {
  fill: var(--main-color-4);
}
.clipboard-input_action:hover .icon use {
  fill: var(--main-color-5);
}
.clipboard-input_action + .clipboard-input_action {
  margin-left: 8px;
}
.clipboard-area > .clipboard-text,
.clipboard-input > .clipboard-text {
  width: 100%;
  outline: none;
  transition: border-color 0.15s ease-out;
  background: var(--main-color-1);
  cursor: pointer;
}
.clipboard-area > .clipboard-text:hover,
.clipboard-input > .clipboard-text:hover,
.clipboard-area > .clipboard-text:active,
.clipboard-input > .clipboard-text:active {
  background-color: var(--main-color-2);
}
.color-picker {
  display: flex;
  align-items: center;
  justify-content: left;
  gap: 12px;
}
.color-picker_left {
  flex-direction: row-reverse;
}
.color-picker_preview {
  display: inline-block;
  flex-shrink: 0;
}
.color-picker.dl-size--small .color-picker_preview {
  width: 16px;
  height: 16px;
}
.color-picker.dl-size--medium .color-picker_preview {
  width: 24px;
  height: 24px;
}
.color-picker.dl-size--large .color-picker_preview {
  width: 32px;
  height: 32px;
}
.color-picker_picker {
  visibility: hidden;
  position: absolute;
  margin-top: 12px;
}
.color-picker .color-picker_value {
  width: 98px;
  vertical-align: middle;
}
.dialog {
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
}
.dialog,
.dialog.dialog_wrap,
.dialog .dialog_overflow {
  width: 100%;
  height: 100%;
}
.dialog_wrap {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 48px 0 0 0;
  box-sizing: border-box;
  z-index: 1100;
  transition: opacity 150ms;
  opacity: 0;
}
.dialog_wrap.dialog--full-screen .dialog_wrap_content {
  width: 100%;
}
.dialog_wrap:not(.dialog--full-screen) {
  padding: 80px 0 0 0;
}
.dialog_wrap.dialog--tall .dialog_wrap_content {
  height: 100%;
}
.dialog_wrap.dialog--tall .dialog_wrap_content_main {
  height: 100%;
}
.dialog_wrap.dialog--tall .dialog_wrap_content_sidebar {
  height: 100%;
}
.dialog_wrap_title {
  display: flex;
  align-items: center;
  font-size: 16px;
  line-height: 24px;
  font-weight: normal;
  padding: 16px 24px 16px 24px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.dialog_wrap_content {
  display: flex;
  z-index: 2;
}
.dialog_wrap_content_main {
  flex: 1 0;
  overflow: auto;
  position: relative;
  background-color: var(--primary-bg);
}
.dialog_wrap_content_sidebar {
  width: 240px;
  background-color: var(--main-color-1);
}
.dialog_wrap_cross {
  position: absolute;
  top: 16px;
  right: 24px;
  cursor: pointer;
}
.dialog_wrap_cross,
.dialog_wrap_cross > .icon {
  width: 16px;
  height: 16px;
}
.dialog_wrap_cross > .icon {
  opacity: .7;
  transition: opacity 0.15s ease-out;
}
.dialog_wrap_cross > .icon > use {
  fill: var(--main-color-8);
}
.dialog_wrap_cross > .icon:hover {
  opacity: 1;
}
.dialog_overflow {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  background-color: var(--main-color-alfa-8);
  z-index: 1;
}
.dialog.fade-in {
  transition-timing-function: ease-in;
  opacity: 1;
}
.dialog.fade-out {
  transition-timing-function: ease-out;
  opacity: 0;
}
.drop-zone {
  background-color: var(--main-color-1);
}
.dnd-drop-zone {
  background-color: var(--main-color-1);
}
.dnd-drop-zone_active {
  background-color: var(--main-color-1);
  animation: blink .4s infinite;
}
.dnd-move[draggable],
.dnd-move[draggable] > div,
.dnd-move[draggable] > div:active,
.dnd-move[draggable] > div:hover,
.dnd-move[draggable] > div:focus,
.dnd-move[draggable] > a:hover,
.dnd-move[draggable] > a:active,
.dnd-move[draggable] > a:focus {
  cursor: grabbing;
}
@keyframes blink {
  0% {
    background-color: var(--main-color-1);
  }
  50% {
    background-color: var(--main-color-2);
  }
  100% {
    background-color: var(--main-color-1);
  }
}
.head-title {
  font-size: 14px;
  line-height: 20px;
}
.list-wrap {
  display: flex;
  flex-direction: column;
  height: 100%;
  box-sizing: border-box;
}
.list-wrap span {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.list-wrap_header {
  display: flex;
  align-items: stretch;
  height: 48px;
  font-weight: 600;
  line-height: 16px;
  cursor: default;
  color: var(--main-color-5);
  border-bottom: 2px solid var(--main-color-2);
  transition: border-bottom-color 200ms ease-in;
  z-index: 1;
}
.list-wrap_header_item {
  display: flex;
  align-items: center;
}
.list-wrap_header_item.sortable {
  cursor: pointer;
  transition: color 200ms ease-in;
}
.list-wrap_header_item.sortable:hover,
.list-wrap_header_item.sortable.sorted {
  color: var(--main-color-8);
}
.list-wrap_header_item.sortable:hover svg use,
.list-wrap_header_item.sortable.sorted svg use {
  fill: var(--main-color-8);
}
.list-wrap_header_item.sortable .arrow {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 16px;
  font-size: 12px;
  margin: 0 4px 0 4px;
}
.list-wrap_header_item.sortable.sorted .arrow.asc {
  transform: rotate(0);
}
.list-wrap_header_item.sortable.sorted .arrow.desc {
  transform: rotate(-180deg);
}
.list-wrap_header_item.sortable svg use {
  transition: fill 200ms ease-in;
  fill: var(--main-color-5);
}
.list-wrap_content {
  padding-bottom: 32px;
}
.list-wrap_content_item {
  display: flex;
  align-items: stretch;
  height: 48px;
  border-bottom: 1px solid var(--main-color-2);
  box-sizing: border-box;
  transition: transform 100ms ease-out, box-shadow 100ms ease-out;
}
.list-wrap_content_item:not([disabled]):not(:active):focus,
.list-wrap_content_item:not([disabled]):not(:active):hover {
  transform: translateY(-2px);
  -webkit-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
}
.list-button {
  min-width: 150px;
  position: relative;
}
.list-button.type--link {
  min-width: 0;
}
.list-button > .button:not(.list-button_main):first-child {
  flex: 1;
}
.list-button > .list-button_main {
  flex: 1;
  justify-content: center;
}
.list-button > .list-button_toggler {
  border-top-right-radius: 2px;
  border-bottom-right-radius: 2px;
}
.list-button .button:last-child .icon {
  margin: 0;
}
.list-button .button.type--link:last-child .icon {
  margin-left: 4px;
}
.list-button .button.type--link:last-child .icon use {
  fill: var(--action-color-2);
}
.list-button .button.type--link:last-child:hover .icon use {
  fill: var(--action-color-3);
}
.list-button .button.type--link:last-child:disabled .icon use {
  fill: var(--action-color-1);
}
.toggable-list-menu {
  display: inline-flex;
}
.toggable-list-menu__opener {
  display: block;
  cursor: pointer;
}
.dl-menu {
  width: 180px;
  display: flex;
  flex-direction: column;
}
.dl-menu .dl-menu-item {
  width: 100%;
  box-sizing: border-box;
  padding: 0 8px 0 0;
  margin: 8px 0 8px 0;
}
.dl-menu .dl-menu-item > a {
  display: flex;
  align-items: center;
  font-weight: 500;
  font-size: 12px;
  color: var(--main-color-5);
  transition: color 200ms ease-in;
  cursor: default;
}
.dl-menu .dl-menu-item_icon {
  width: 16px;
  height: 16px;
  margin-right: 8px;
}
.dl-menu .dl-menu-item_icon use {
  transition: fill 200ms ease-in;
  fill: var(--main-color-5);
}
.dl-menu .dl-menu-item > a:hover,
.dl-menu .dl-menu-item > a.active {
  color: var(--main-color-9);
}
.dl-menu .dl-menu-item:hover > a:not(.active) {
  cursor: pointer;
}
.dl-menu .dl-menu-item > a:hover .dl-menu-item_icon use,
.dl-menu .dl-menu-item > a.active .dl-menu-item_icon use {
  fill: var(--main-color-9);
}
.notification-area {
  position: relative;
  display: flex;
  align-items: stretch;
  padding: 8px;
  border-radius: 4px;
  color: var(--main-color-8);
  border: 1px solid transparent;
  border-radius: 2px;
  box-sizing: border-box;
}
.notification-area_icon {
  width: 32px;
}
.notification-area.area-type--info {
  border-color: var(--action-color-3);
  background: var(--action-color-1);
}
.notification-area.area-type--danger {
  border-color: var(--negative-color-2);
  background: var(--negative-color-1);
}
.notification-area.area-type--warning {
  border-color: var(--attention-color-3);
  background: var(--attention-color-1);
}
.notification-area.area-type--warning .notification-area_icon use,
.notification-area.area-type--warning .notification-area_icon g {
  fill: var(--attention-color-3);
}
.popup-tail-wrap {
  z-index: 1099;
}
.popup-tail-wrap__content,
.popup-tail-wrap__tail {
  background: var(--primary-bg);
  color: initial;
}
.popup-tail-wrap_contrast .popup-tail-wrap__content,
.popup-tail-wrap_contrast .popup-tail-wrap__tail {
  background: var(--tooltip-bg);
  color: var(--tooltip-fg);
}
.popup-tail-wrap_rounded,
.popup-tail-wrap_rounded .popup-tail-wrap__content {
  border-radius: 4px;
}
.popup-tail-wrap__tail {
  position: absolute;
  box-sizing: border-box;
  width: 16px;
  height: 16px;
  z-index: -1;
}
.popup-shadowed .popup-tail-wrap__tail {
  box-shadow: var(--popup-shadow);
}
.popup[data-position="left-top"] .popup-tail-wrap__content {
  border-top-left-radius: 0;
}
.popup[data-position="left-top"] .popup-tail-wrap__tail {
  left: -16px;
  top: 0;
  transform: skew(45deg, 0) translateX(8px);
}
.popup[data-position="left-bottom"] .popup-tail-wrap__content {
  border-bottom-left-radius: 0;
}
.popup[data-position="left-bottom"] .popup-tail-wrap__tail {
  left: -16px;
  bottom: 0;
  transform: skew(-45deg, 0) translateX(8px);
}
.popup[data-position="right-top"] .popup-tail-wrap__content {
  border-top-right-radius: 0;
}
.popup[data-position="right-top"] .popup-tail-wrap__tail {
  right: -16px;
  top: 0;
  transform: skew(-45deg, 0) translateX(-8px);
}
.popup[data-position="right-bottom"] .popup-tail-wrap__content {
  border-bottom-right-radius: 0;
}
.popup[data-position="right-bottom"] .popup-tail-wrap__tail {
  right: -16px;
  bottom: 0;
  transform: skew(45deg, 0) translateX(-8px);
}
.popup[data-position="top-left"] .popup-tail-wrap__content {
  border-top-left-radius: 0;
}
.popup[data-position="top-left"] .popup-tail-wrap__tail {
  top: -16px;
  left: 0;
  transform: skew(0, 45deg) translateY(8px);
}
.popup[data-position="top-right"] .popup-tail-wrap__content {
  border-top-right-radius: 0;
}
.popup[data-position="top-right"] .popup-tail-wrap__tail {
  top: -16px;
  right: 0;
  transform: skew(0, -45deg) translateY(8px);
}
.popup[data-position="bottom-left"] .popup-tail-wrap__content {
  border-bottom-left-radius: 0;
}
.popup[data-position="bottom-left"] .popup-tail-wrap__tail {
  bottom: -16px;
  left: 0;
  transform: skew(0, -45deg) translateY(-8px);
}
.popup[data-position="bottom-right"] .popup-tail-wrap__content {
  border-bottom-right-radius: 0;
}
.popup[data-position="bottom-right"] .popup-tail-wrap__tail {
  bottom: -16px;
  right: 0;
  transform: skew(0, 45deg) translateY(-8px);
}
.pro-badge {
  white-space: nowrap;
}
.pro-badge_visible::after {
  content: 'pro';
  display: inline-block;
  margin-left: 8px;
  padding: 3px 4px;
  background: var(--main-color-5);
  border-radius: 2px;
  font-size: 8px;
  font-weight: bold;
  text-transform: uppercase;
  color: var(--contrast-fg);
  vertical-align: text-top;
}
.search-input {
  display: flex;
  align-items: center;
  padding: 0 8px;
  border: 1px solid var(--border-color);
  height: 32px;
  box-sizing: border-box;
  transition: border-color 0.2s ease-in;
}
.search-input_area {
  flex: 1 0;
  margin: 0 8px;
  height: 16px;
}
.search-input_area > input {
  border: transparent;
  outline: none;
  padding: 0;
  width: 100%;
}
.search-input_area > input::placeholder {
  color: var(--main-color-5);
}
.search-input_search,
.search-input_cross {
  width: 16px;
  height: 16px;
}
.search-input .icon {
  cursor: pointer;
}
.search-input .icon use {
  transition: fill 0.2s ease-in;
  fill: var(--main-color-4);
}
.search-input .icon:hover use {
  fill: var(--main-color-8);
}
.search-input.focus {
  border-color: var(--action-color-2);
}
.search-input_noborder,
.search-input_noborder.focus {
  border-color: transparent;
}
.position-sticky {
  position: -webkit-sticky;
  position: sticky;
}
.dl-table {
  display: flex;
  flex-direction: column;
  height: 100%;
}
.dl-table_header,
.dl-table_body,
.dl-table_row {
  width: -moz-fit-content;
  width: fit-content;
}
.dl-table_title {
  display: flex;
  align-items: center;
  padding: 16px 24px;
}
.dl-table_title > div:first-child {
  font-size: 24px;
  line-height: 28px;
  font-weight: 700;
  color: var(--main-color-9);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.dl-table_content {
  overflow: auto;
  box-sizing: border-box;
  flex-grow: 1;
}
.dl-table_content:not(.dl-table__resizing) .dl-table_cell--sortable {
  cursor: pointer;
}
.dl-table_header {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  flex-shrink: 0;
  z-index: 1;
  background-color: var(--primary-bg);
  border-top: 1px solid var(--main-color-3);
  border-bottom: 2px solid var(--main-color-3);
}
.dl-table_header .dl-table_cell {
  color: var(--main-color-8);
  font-weight: 600;
}
.dl-table_header .dl-table_cell,
.dl-table_header .dl-table_cell > div {
  display: flex;
  align-items: center;
}
.dl-table_header .dl-table_cell--desc .dl-table_icon {
  transform: rotate(180deg);
}
.dl-table_header .dl-table_cell--sortable:hover,
.dl-table_header .dl-table_cell--sorted {
  color: var(--main-color-9);
}
.dl-table_header .dl-table_cell--sortable:hover .dl-table_icon use,
.dl-table_header .dl-table_cell--sorted .dl-table_icon use {
  fill: var(--main-color-8);
}
.dl-table_body {
  font-family: monospace;
}
.dl-table_row {
  display: flex;
  align-items: stretch;
  border-bottom: 1px solid var(--main-color-3);
}
.dl-table_icon {
  margin-left: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  width: 16px;
  height: 16px;
}
.dl-table_icon use {
  fill: var(--main-color-4);
}
.dl-table_cell {
  padding: 8px;
  position: relative;
  box-sizing: border-box;
  min-width: 150px;
  max-width: 0;
  min-height: 31px;
  justify-content: flex-start;
  text-align: left;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
.dl-table_cell--right {
  justify-content: flex-end;
  text-align: right;
}
.dl-table_cell .dl-table_cell__editing {
  width: 100%;
  padding: 0;
  margin: 0;
  border: none;
  line-height: inherit;
}
.dl-table_cell.dl-table_cell--right .dl-table_cell__editing {
  text-align: right;
}
.dl-table_cell--focused:after {
  content: " ";
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  box-sizing: border-box;
  border: 2px solid var(--action-color-1);
}
.dl-table_cell:not(:last-child) {
  border-right: 1px solid var(--main-color-3);
}
.dl-table_footer {
  position: -webkit-sticky;
  position: sticky;
  bottom: 0;
  left: 35%;
  width: max-content;
  padding: 16px 0 16px 0;
}
.dl-table__separator {
  position: absolute;
  top: 0;
  right: 0;
  width: 4px;
  height: 100%;
  background-color: transparent;
  cursor: col-resize;
}
.dl-table__resizing {
  cursor: col-resize;
}
.dl-table--scrolling {
  box-shadow: rgba(0, 0, 0, 0.15) 0 0 12px 8px;
}
.dl-table--added {
  position: relative;
}
.dl-table--added:after {
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: var(--action-color-1);
  transition: opacity 0.5s;
}
.dl-table--added.fade-out:after {
  opacity: 0;
}
.dl-table--deleted {
  height: auto;
  max-height: 5vw;
  overflow: hidden;
  transition: max-height 0.3s ease-out;
  position: relative;
}
.dl-table--deleted.fade-out {
  max-height: 0;
}
.dl-table--deleted:after {
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: var(--negative-color-1);
  transition: opacity 0.5s;
}
.dl-table--deleted.fade-out:after {
  opacity: 0;
}
.dl-table__arrow {
  width: 16px;
  height: 16px;
  box-shadow: 1px -1px 0 1px var(--main-color-3) inset;
  -webkit-box-shadow: 1px -1px var(--main-color-3) inset;
  border: solid transparent;
  box-sizing: border-box;
  transition: 0.2s;
  cursor: pointer;
}
.dl-table__arrow--left {
  transform: rotate(45deg);
}
.dl-table__arrow--right {
  transform: rotate(225deg);
}
.dl-table__arrow[disabled] {
  opacity: .5;
  cursor: not-allowed;
}
.dl-table__arrow:not([disabled]):hover {
  box-shadow: 1px -1px 0 1px var(--main-color-3) inset;
  -webkit-box-shadow: 2px -2px var(--main-color-3) inset;
}
.dl-table__navigation {
  height: 32px;
  border-radius: 16px;
  background-color: var(--primary-bg);
  display: grid;
  grid-template-columns: 32px 1fr 32px;
  gap: 8px;
  align-items: stretch;
  min-width: 180px;
  -webkit-box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.1);
  box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.1);
}
.dl-table__navigation > div {
  display: flex;
  align-items: center;
  justify-content: center;
}
.dl-table__navigation > div:first-child {
  justify-content: flex-end;
}
.dl-table__navigation > div:last-child {
  justify-content: flex-start;
}
.dl-table__navigation__pages {
  width: 160px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.tabs-wrap .tab {
  min-width: 140px;
}
.tabs-wrap .tab_header {
  padding: 8px 24px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  box-sizing: border-box;
  opacity: .6;
  cursor: pointer;
}
.tabs-wrap .tab_title {
  font-size: 14px;
  font-weight: 600;
  line-height: 20px;
}
.tabs-wrap .tab_subtitle {
  font-size: 12px;
  margin: 4px 0 0 0;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.tabs-wrap .tab.selected .tab_header,
.tabs-wrap .tab:hover .tab_header {
  opacity: 1;
}
.tabs-wrap .tab .tab_header[disabled] {
  opacity: .3;
  cursor: not-allowed;
}
.dl-size--small.tabs-wrap .tab {
  min-width: auto;
}
.dl-size--small.tabs-wrap .tab_title {
  font-size: 12px;
  line-height: 16px;
}
.tabs-wrap {
  display: flex;
  align-items: center;
  flex-direction: column;
  flex: 1 0;
}
.tabs-wrap_header {
  display: flex;
  align-items: center;
  width: 100%;
  margin: 0 0 24px;
  position: relative;
  border-bottom: 1px solid var(--main-color-2);
}
.tabs-wrap_header--centered .tabs-wrap_header {
  justify-content: center;
}
.tabs-wrap_header_layout {
  display: flex;
  align-items: center;
}
.tabs-wrap_header--scrollable .tabs-wrap_header_layout {
  flex-grow: 1;
  overflow: auto;
}
.tabs-wrap_header--scrollable .tabs-wrap_header_layout::-webkit-scrollbar-track {
  background-color: transparent;
}
.tabs-wrap_header--scrollable .tabs-wrap_header_layout::-webkit-scrollbar {
  width: 7px;
  height: 7px;
  background-color: transparent;
}
.tabs-wrap_header--scrollable .tabs-wrap_header_layout::-webkit-scrollbar-thumb {
  background-color: var(--main-color-4);
}
.tabs-wrap_header--scrollable .tabs-wrap_header_layout::-webkit-scrollbar-corner {
  background-color: transparent;
}
.tabs-wrap_header > .tabs-wrap_indicator {
  position: absolute;
  bottom: -3px;
  left: 0;
  min-width: 120px;
  height: 5px;
  background-color: var(--action-color-2);
  transition: all 300ms cubic-bezier(0.4, 0, 0.2, 1) 0ms;
}
.tabs-wrap_content {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
}
.tabs-wrap_content_item {
  display: none;
  width: 100%;
}
.tabs-wrap_content_item.selected {
  display: block;
}
.dl-size--small.tabs-wrap .tabs-wrap_header > .tabs-wrap_indicator {
  min-width: auto;
}
.dl-size--small.tabs-wrap .tabs-wrap_header {
  margin: 0 0 8px;
}
.tags-input {
  padding: 2px 8px 6px 8px;
  box-sizing: border-box;
  border: 1px solid var(--main-color-2);
  font-size: 12px;
  color: var(--main-color-8);
  overflow: auto;
}
.tags-input:hover,
.tags-input:focus,
.tags-input.focus {
  border-color: var(--action-color-2);
}
.tags-input_content {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  min-height: 24px;
}
.tags-input_item {
  height: 20px;
  width: auto;
  box-sizing: border-box;
  padding: 2px 4px;
  margin: 4px 8px 0 0;
  display: flex;
  align-items: center;
  background-color: var(--main-color-1);
  border: 1px solid var(--main-color-1);
  border-radius: 4px;
  cursor: pointer;
}
.tags-input_item_delete {
  margin-left: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: .7;
}
.tags-input_item_delete:hover {
  opacity: 1;
}
.tags-input_input {
  margin: 4px 0 0 0;
  max-width: 100%;
  flex: 1 0;
}
.tags-input_input > input {
  border: none;
  width: 100%;
  min-width: 200px;
  padding: 3px 0 2px;
}
.tags-input_input > input:hover,
.tags-input_input > input:focus {
  outline: none;
}
.tip {
  position: relative;
  display: inline-flex;
}
.tip .icon {
  transition: fill 0.2s ease-in;
}
.tip .icon use,
.tip .icon g {
  fill: var(--main-color-4);
}
.tip .icon:hover use,
.tip .icon:hover g {
  fill: var(--main-color-8);
}
.dl-tooltip {
  white-space: initial;
}
.dl-tooltip_header {
  display: block;
  margin: 0 0 8px;
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
  color: var(--tooltip-fg);
}
.dl-tooltip_description {
  color: var(--tooltip-fg);
}
.dl-tooltip_popup.popup {
  display: block;
  box-sizing: border-box;
  padding: 16px;
  width: max-content;
  border-radius: 4px;
  pointer-events: none;
  z-index: 1;
  background: var(--tooltip-bg);
  color: var(--tooltip-fg);
  font-size: 12px;
  line-height: 16px;
  transition: opacity 150ms;
  opacity: 0;
}
.dl-tooltip_popup.popup.fade-in {
  transition-timing-function: ease-in;
  opacity: 1;
}
.dl-tooltip_popup.popup.fade-out {
  transition-timing-function: ease-out;
  opacity: 0;
}
.dl-tooltip_compact .dl-tooltip_popup.popup {
  padding: 8px;
}
.dl-tooltip ul {
  margin-top: 16px;
}
.dl-tooltip ul li {
  margin-bottom: 8px;
}
.dl-tooltip ul li:last-child {
  margin-bottom: 0;
}
.dl-tooltip ul li:before {
  display: inline-block;
  content: '-';
  padding-right: 4px;
}
.avatar {
  display: inline-block;
  width: 28px;
  height: 28px;
  line-height: 28px;
  text-align: center;
  text-transform: uppercase;
  background-size: cover;
  background-repeat: no-repeat;
}
.avatar_rounded {
  border-radius: 50%;
}
.avatar.dl-size--small {
  width: 16px;
  height: 16px;
  line-height: 16px;
  font-size: 7px;
}
.avatar.dl-size--medium {
  width: 24px;
  height: 24px;
  line-height: 24px;
}
.avatar.dl-size--large {
  width: 32px;
  height: 32px;
  line-height: 32px;
}
.button {
  position: relative;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-width: 100px;
  height: 32px;
  font-size: 12px;
  line-height: 16px;
  font-weight: 600;
  box-sizing: border-box;
  padding: 2px 8px;
  cursor: pointer;
  outline: none;
  margin: 0 4px;
  color: var(--action-color-3);
  border: 1px solid transparent;
  border-radius: 2px;
  background: transparent;
  transition: background-color 0.13s ease-in, border-color 0.13s ease-in;
  /* button types */
  /* ------------- */
  /* button-sizes */
}
.button:first-child {
  margin-left: 0;
}
.button:last-child {
  margin-right: 0;
}
.button .icon {
  margin: 0 4px 0 0;
}
.button.type--secondary[disabled],
.button.type--danger[disabled],
.button.type--label[disabled],
.button.type--open[disabled],
.button.type--badge[disabled],
.button.type--secondary:disabled,
.button.type--danger:disabled,
.button.type--label:disabled,
.button.type--open:disabled,
.button.type--badge:disabled,
.button.type--secondary[disabled]:hover,
.button.type--danger[disabled]:hover,
.button.type--label[disabled]:hover,
.button.type--open[disabled]:hover,
.button.type--badge[disabled]:hover,
.button.type--secondary:disabled:hover,
.button.type--danger:disabled:hover,
.button.type--label:disabled:hover,
.button.type--open:disabled:hover,
.button.type--badge:disabled:hover,
.button.type--secondary[disabled]:active,
.button.type--danger[disabled]:active,
.button.type--label[disabled]:active,
.button.type--open[disabled]:active,
.button.type--badge[disabled]:active,
.button.type--secondary:disabled:active,
.button.type--danger:disabled:active,
.button.type--label:disabled:active,
.button.type--open:disabled:active,
.button.type--badge:disabled:active,
.button.type--secondary[disabled]:focus,
.button.type--danger[disabled]:focus,
.button.type--label[disabled]:focus,
.button.type--open[disabled]:focus,
.button.type--badge[disabled]:focus,
.button.type--secondary:disabled:focus,
.button.type--danger:disabled:focus,
.button.type--label:disabled:focus,
.button.type--open:disabled:focus,
.button.type--badge:disabled:focus {
  border-color: var(--main-color-2);
  cursor: not-allowed;
  color: var(--main-color-3);
  background: transparent;
}
.button.type--secondary[disabled] .icon,
.button.type--danger[disabled] .icon,
.button.type--label[disabled] .icon,
.button.type--open[disabled] .icon,
.button.type--badge[disabled] .icon,
.button.type--secondary:disabled .icon,
.button.type--danger:disabled .icon,
.button.type--label:disabled .icon,
.button.type--open:disabled .icon,
.button.type--badge:disabled .icon,
.button.type--secondary[disabled]:hover .icon,
.button.type--danger[disabled]:hover .icon,
.button.type--label[disabled]:hover .icon,
.button.type--open[disabled]:hover .icon,
.button.type--badge[disabled]:hover .icon,
.button.type--secondary:disabled:hover .icon,
.button.type--danger:disabled:hover .icon,
.button.type--label:disabled:hover .icon,
.button.type--open:disabled:hover .icon,
.button.type--badge:disabled:hover .icon,
.button.type--secondary[disabled]:active .icon,
.button.type--danger[disabled]:active .icon,
.button.type--label[disabled]:active .icon,
.button.type--open[disabled]:active .icon,
.button.type--badge[disabled]:active .icon,
.button.type--secondary:disabled:active .icon,
.button.type--danger:disabled:active .icon,
.button.type--label:disabled:active .icon,
.button.type--open:disabled:active .icon,
.button.type--badge:disabled:active .icon,
.button.type--secondary[disabled]:focus .icon,
.button.type--danger[disabled]:focus .icon,
.button.type--label[disabled]:focus .icon,
.button.type--open[disabled]:focus .icon,
.button.type--badge[disabled]:focus .icon,
.button.type--secondary:disabled:focus .icon,
.button.type--danger:disabled:focus .icon,
.button.type--label:disabled:focus .icon,
.button.type--open:disabled:focus .icon,
.button.type--badge:disabled:focus .icon {
  cursor: not-allowed;
}
.button.type--secondary[disabled] .icon use,
.button.type--danger[disabled] .icon use,
.button.type--label[disabled] .icon use,
.button.type--open[disabled] .icon use,
.button.type--badge[disabled] .icon use,
.button.type--secondary:disabled .icon use,
.button.type--danger:disabled .icon use,
.button.type--label:disabled .icon use,
.button.type--open:disabled .icon use,
.button.type--badge:disabled .icon use,
.button.type--secondary[disabled]:hover .icon use,
.button.type--danger[disabled]:hover .icon use,
.button.type--label[disabled]:hover .icon use,
.button.type--open[disabled]:hover .icon use,
.button.type--badge[disabled]:hover .icon use,
.button.type--secondary:disabled:hover .icon use,
.button.type--danger:disabled:hover .icon use,
.button.type--label:disabled:hover .icon use,
.button.type--open:disabled:hover .icon use,
.button.type--badge:disabled:hover .icon use,
.button.type--secondary[disabled]:active .icon use,
.button.type--danger[disabled]:active .icon use,
.button.type--label[disabled]:active .icon use,
.button.type--open[disabled]:active .icon use,
.button.type--badge[disabled]:active .icon use,
.button.type--secondary:disabled:active .icon use,
.button.type--danger:disabled:active .icon use,
.button.type--label:disabled:active .icon use,
.button.type--open:disabled:active .icon use,
.button.type--badge:disabled:active .icon use,
.button.type--secondary[disabled]:focus .icon use,
.button.type--danger[disabled]:focus .icon use,
.button.type--label[disabled]:focus .icon use,
.button.type--open[disabled]:focus .icon use,
.button.type--badge[disabled]:focus .icon use,
.button.type--secondary:disabled:focus .icon use,
.button.type--danger:disabled:focus .icon use,
.button.type--label:disabled:focus .icon use,
.button.type--open:disabled:focus .icon use,
.button.type--badge:disabled:focus .icon use,
.button.type--secondary[disabled] .icon g,
.button.type--danger[disabled] .icon g,
.button.type--label[disabled] .icon g,
.button.type--open[disabled] .icon g,
.button.type--badge[disabled] .icon g,
.button.type--secondary:disabled .icon g,
.button.type--danger:disabled .icon g,
.button.type--label:disabled .icon g,
.button.type--open:disabled .icon g,
.button.type--badge:disabled .icon g,
.button.type--secondary[disabled]:hover .icon g,
.button.type--danger[disabled]:hover .icon g,
.button.type--label[disabled]:hover .icon g,
.button.type--open[disabled]:hover .icon g,
.button.type--badge[disabled]:hover .icon g,
.button.type--secondary:disabled:hover .icon g,
.button.type--danger:disabled:hover .icon g,
.button.type--label:disabled:hover .icon g,
.button.type--open:disabled:hover .icon g,
.button.type--badge:disabled:hover .icon g,
.button.type--secondary[disabled]:active .icon g,
.button.type--danger[disabled]:active .icon g,
.button.type--label[disabled]:active .icon g,
.button.type--open[disabled]:active .icon g,
.button.type--badge[disabled]:active .icon g,
.button.type--secondary:disabled:active .icon g,
.button.type--danger:disabled:active .icon g,
.button.type--label:disabled:active .icon g,
.button.type--open:disabled:active .icon g,
.button.type--badge:disabled:active .icon g,
.button.type--secondary[disabled]:focus .icon g,
.button.type--danger[disabled]:focus .icon g,
.button.type--label[disabled]:focus .icon g,
.button.type--open[disabled]:focus .icon g,
.button.type--badge[disabled]:focus .icon g,
.button.type--secondary:disabled:focus .icon g,
.button.type--danger:disabled:focus .icon g,
.button.type--label:disabled:focus .icon g,
.button.type--open:disabled:focus .icon g,
.button.type--badge:disabled:focus .icon g {
  fill: var(--main-color-3);
}
.button.type--primary {
  color: var(--contrast-fg);
  background-color: var(--action-color-2);
}
.button.type--primary .icon use {
  fill: var(--contrast-fg);
}
.button.type--primary:hover {
  background-color: var(--action-color-3);
}
.button.type--primary:focus {
  background-color: var(--action-color-2);
}
.button.type--primary:active {
  box-shadow: inset 0 1px 0 1px rgba(0, 0, 0, 0.25);
  background-color: var(--action-color-3);
}
.button.type--primary[disabled],
.button.type--primary:disabled,
.button.type--primary[disabled]:hover,
.button.type--primary:disabled:hover,
.button.type--primary[disabled]:active,
.button.type--primary:disabled:active,
.button.type--primary[disabled]:focus,
.button.type--primary:disabled:focus {
  border-color: var(--main-color-2);
  cursor: not-allowed;
  color: var(--main-color-0);
  background: var(--main-color-2);
}
.button.type--primary[disabled] .icon,
.button.type--primary:disabled .icon,
.button.type--primary[disabled]:hover .icon,
.button.type--primary:disabled:hover .icon,
.button.type--primary[disabled]:active .icon,
.button.type--primary:disabled:active .icon,
.button.type--primary[disabled]:focus .icon,
.button.type--primary:disabled:focus .icon {
  cursor: not-allowed;
}
.button.type--primary[disabled] .icon use,
.button.type--primary:disabled .icon use,
.button.type--primary[disabled]:hover .icon use,
.button.type--primary:disabled:hover .icon use,
.button.type--primary[disabled]:active .icon use,
.button.type--primary:disabled:active .icon use,
.button.type--primary[disabled]:focus .icon use,
.button.type--primary:disabled:focus .icon use,
.button.type--primary[disabled] .icon g,
.button.type--primary:disabled .icon g,
.button.type--primary[disabled]:hover .icon g,
.button.type--primary:disabled:hover .icon g,
.button.type--primary[disabled]:active .icon g,
.button.type--primary:disabled:active .icon g,
.button.type--primary[disabled]:focus .icon g,
.button.type--primary:disabled:focus .icon g {
  fill: var(--main-color-0);
}
.button.type--secondary {
  color: var(--main-color-8);
  border-color: var(--main-color-3);
}
.button.type--secondary .icon use,
.button.type--secondary .icon g {
  fill: var(--main-color-4);
}
.button.type--secondary:hover {
  background-color: var(--main-color-2);
}
.button.type--secondary:hover .icon use,
.button.type--secondary:hover .icon g {
  fill: var(--main-color-7);
}
.button.type--secondary:active {
  background-color: var(--main-color-3);
}
.button.type--secondary.mode--contrast {
  color: var(--dark-main-color-10);
  border-color: var(--dark-main-color-6);
}
.button.type--secondary.mode--contrast .icon use,
.button.type--secondary.mode--contrast .icon g {
  fill: var(--dark-main-color-6);
}
.button.type--secondary.mode--contrast:hover {
  background-color: var(--pale-bg);
}
.button.type--secondary.mode--contrast:hover .icon use,
.button.type--secondary.mode--contrast:hover .icon g {
  fill: var(--dark-main-color-9);
}
.button.type--secondary.mode--contrast:active {
  background-color: var(--dark-main-color-5);
}
.button.type--danger {
  color: var(--negative-color-3);
  border-color: var(--negative-color-2);
}
.button.type--danger .icon use,
.button.type--danger .icon g {
  fill: var(--negative-color-3);
}
.button.type--danger:hover {
  background: var(--negative-color-1);
}
.button.type--danger:active {
  color: var(--primary-bg);
  background: var(--negative-color-3);
}
.button.type--label:hover {
  border-color: var(--main-color-3);
  background-color: var(--main-color-2);
}
.button.type--label:active {
  background-color: var(--main-color-3);
}
.button.type--label:disabled {
  border: none;
}
.button.type--link {
  width: auto;
  height: auto;
  padding: 0;
  margin: 0;
  box-shadow: none;
  font-weight: inherit;
  font-size: inherit;
  min-width: 0;
  color: var(--action-color);
  border: none;
  background: transparent;
}
.button.type--link:hover {
  color: var(--action-color);
  background: transparent;
  text-decoration: underline;
}
.button.type--link[disabled],
.button.type--link:disabled,
.button.type--link[disabled]:hover,
.button.type--link:disabled:hover,
.button.type--link[disabled]:active,
.button.type--link:disabled:active,
.button.type--link[disabled]:focus,
.button.type--link:disabled:focus {
  border-color: var(--main-color-2);
  cursor: not-allowed;
  color: var(--action-color-1);
  background: transparent;
}
.button.type--link[disabled] .icon,
.button.type--link:disabled .icon,
.button.type--link[disabled]:hover .icon,
.button.type--link:disabled:hover .icon,
.button.type--link[disabled]:active .icon,
.button.type--link:disabled:active .icon,
.button.type--link[disabled]:focus .icon,
.button.type--link:disabled:focus .icon {
  cursor: not-allowed;
}
.button.type--link[disabled] .icon use,
.button.type--link:disabled .icon use,
.button.type--link[disabled]:hover .icon use,
.button.type--link:disabled:hover .icon use,
.button.type--link[disabled]:active .icon use,
.button.type--link:disabled:active .icon use,
.button.type--link[disabled]:focus .icon use,
.button.type--link:disabled:focus .icon use,
.button.type--link[disabled] .icon g,
.button.type--link:disabled .icon g,
.button.type--link[disabled]:hover .icon g,
.button.type--link:disabled:hover .icon g,
.button.type--link[disabled]:active .icon g,
.button.type--link:disabled:active .icon g,
.button.type--link[disabled]:focus .icon g,
.button.type--link:disabled:focus .icon g {
  fill: var(--action-color-1);
}
.button.type--badge {
  display: inline-flex;
  align-items: center;
  box-sizing: border-box;
  min-width: 0;
  border-radius: 50%;
  color: var(--main-color-8);
  border-color: var(--main-color-3);
}
.button.type--badge:hover {
  background-color: var(--main-color-2);
}
.button.type--badge:active {
  background-color: var(--main-color-3);
}
.button.type--badge .icon {
  margin: 0;
}
.button.type--badge.button.type--badge-size-s {
  padding: 6px;
  border-width: 1px;
}
.button.type--open {
  width: auto;
  padding: 0;
  margin: 0;
  box-shadow: none;
  min-width: 0;
  border: none;
  background: transparent;
  color: var(--main-color-8);
}
.button.type--open .icon use,
.button.type--open .icon g {
  fill: var(--main-color-4);
}
.button.type--open:hover .icon use,
.button.type--open:hover .icon g {
  fill: var(--main-color-8);
}
.button .icon:not(:last-child) {
  margin-right: 6px;
}
.button.button-size-s {
  min-width: initial;
  padding: 3px 8px;
  margin: 0 2px;
  width: 28px;
  height: 28px;
}
.button-group {
  display: flex;
  align-items: center;
}
.button-group .button {
  margin: 0 0 0 -1px;
  border-radius: 0;
  min-width: auto;
  width: auto;
}
.button-group .button.type--primary:not(:first-child) {
  border-left: 1px solid var(--action-color-3);
}
.button-group .button:first-child {
  margin: 0;
  border-top-left-radius: 2px;
  border-bottom-left-radius: 2px;
}
.button-group .button:first-child:not(:first-child) {
  border-left-color: inherit;
}
.button-group .button:last-child {
  border-top-right-radius: 2px;
  border-bottom-right-radius: 2px;
}
.button-group .button:disabled:not(:first-child),
.button-group .button[disabled]:not(:first-child) {
  border-left-color: transparent;
}
.button-group .button:disabled:not(:last-child),
.button-group .button[disabled]:not(:last-child) {
  border-right-color: transparent;
}
.progress-button {
  position: relative;
}
.progress-button__indicator {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 2px;
  border-bottom-left-radius: 1px;
  transition: background 0.1s ease-out, background-color 200ms ease-in, width 0.1s ease-out;
}
.progress-button.type--primary .progress-button__indicator {
  background-color: var(--action-color-3);
}
.progress-button.type--secondary .progress-button__indicator {
  background-color: var(--action-color-2);
}
.checkbox {
  position: relative;
  display: flex;
  align-items: end;
  box-sizing: border-box;
  line-height: 16px;
}
.checkbox input[type=checkbox] {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  margin: 0;
  opacity: 0;
  outline: none;
}
.checkbox input[type=checkbox]:not([disabled]) {
  cursor: pointer;
}
.checkbox__mark {
  position: relative;
  flex-shrink: 0;
  width: 14px;
  height: 14px;
  box-sizing: border-box;
  margin-right: 8px;
  border: 1px solid var(--main-color-3);
  border-radius: 2px;
  background-color: var(--main-color-1);
  pointer-events: none;
  transition: border-color 0.2s ease-out, background-color 0.2s ease-out;
}
.checkbox__mark::after {
  content: '';
  position: absolute;
  display: none;
  top: 0;
  left: 3px;
  width: 6px;
  height: 10px;
  border: solid var(--primary-bg);
  border-width: 0 2px 2px 0;
  transform: rotate(45deg);
  box-sizing: border-box;
}
.checkbox__label {
  opacity: .8;
  white-space: initial;
}
.checkbox input[disabled] {
  cursor: not-allowed;
}
.checkbox input[disabled] + .checkbox__mark,
.checkbox input[disabled] ~ .checkbox__label {
  opacity: .5;
  cursor: not-allowed;
}
input[type=checkbox]:checked ~ .checkbox__mark {
  border-color: var(--action-color-2);
  background-color: var(--action-color-2);
}
input[type=checkbox]:checked ~ .checkbox__mark::after {
  display: block;
}
input[type=checkbox]:not([disabled]):checked ~ .checkbox__label {
  opacity: 1;
}
.checkbox:hover input[type=checkbox]:not([disabled]):not(:checked) ~ .checkbox__mark {
  background-color: var(--main-color-2);
}
.checkbox:hover input[type=checkbox]:not([disabled]):not(:checked) ~ .checkbox__label {
  opacity: 1;
}
.delimiter {
  align-self: center;
  width: 1px;
  height: 16px;
  background-color: var(--border-color);
}
.dl-empty-panel {
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;
  border: solid 1px var(--main-color-2);
  flex-direction: column;
  flex: 0 0 324px;
}
.dl-empty-panel_content {
  width: 176px;
  text-align: center;
}
.dl-empty-panel_bg {
  display: inline-block;
  width: 32px;
  height: 32px;
  background-image: url("/assets/images/brackets.svg");
  background-size: contain;
}
.dl-empty-panel_title {
  font-size: 14px;
  margin: 16px 0 8px;
}
.dl-empty-panel_text {
  color: var(--main-color-5);
}
.empty-page {
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1 0;
  flex-direction: column;
}
.empty-page > p {
  font-size: 17px;
}
.empty-page > p > span {
  font-weight: 600;
  margin-right: 4px;
}
.error-message {
  display: flex;
  flex-direction: column;
  gap: 4px;
}
.error-message__text_error {
  color: var(--negative-color-3);
}
.error-message__text_warning {
  color: var(--attention-color-3);
}
.icon.dl-size--small {
  width: 12px;
  height: 12px;
}
.icon.dl-size--large {
  width: 22px;
  height: 22px;
}
.icon-menu {
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}
.icon-menu > use {
  transition: fill 200ms ease-in;
  fill: var(--main-color-5);
}
.icon-menu:hover > use {
  fill: var(--main-color-8);
}
#icon-workbook-badged .badge,
#icon-report-badged .badge {
  fill: var(--positive-color-2);
}
.with-icon-wrapper {
  position: relative;
}
.with-icon-wrapper__right {
  position: absolute;
  right: 2px;
  top: 2px;
  padding: 8px;
  cursor: pointer;
}
.with-icon-wrapper_has-right > *:first-child {
  width: 100%;
  padding-right: 30px;
}
.with-icon-wrapper_has-right.with-icon-wrapper_separated > *:first-child::after {
  display: inline-block;
  height: 16px;
  margin-left: 8px;
  border-left: 1px solid var(--main-color-2);
  content: " ";
}
.with-icon-wrapper .icon use,
.with-icon-wrapper .icon g {
  fill: var(--main-color-5);
}
.with-icon-wrapper .icon:hover use,
.with-icon-wrapper .icon:hover g {
  fill: var(--main-color-9);
}
.with-icon-wrapper .icon:disabled,
.with-icon-wrapper .icon[disabled] {
  cursor: not-allowed;
}
.with-icon-wrapper .icon:disabled use,
.with-icon-wrapper .icon[disabled] use,
.with-icon-wrapper .icon:disabled g,
.with-icon-wrapper .icon[disabled] g {
  fill: var(--main-color-3);
}
.label {
  display: flex;
  flex-direction: column;
  gap: 4px;
}
.label__header {
  font-size: 12px;
  line-height: 16px;
  font-weight: 400;
  color: var(--main-color-8);
  color: var(--main-color-9);
}
a.dl-link {
  color: var(--main-color-9);
  border-bottom: 1px solid transparent;
  cursor: pointer;
  transition: border-bottom-color 200ms ease-in;
}
a.dl-link:hover {
  color: var(--main-color-9);
  border-bottom-color: var(--main-color-9);
}
.logo {
  display: inline-block;
  margin-right: 16px;
  vertical-align: middle;
  background-image: url('/logo/RGB/Logo-RGB.svg');
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
}
.logo.dl-size--small {
  width: 16px;
  height: 16px;
}
.logo,
.logo.dl-size--medium {
  width: 32px;
  height: 32px;
}
.logo.dl-size--large {
  width: 68px;
  height: 68px;
}
.progress-wrap {
  position: relative;
  display: flex;
  align-items: center;
  line-height: 24px;
  border-bottom: 2px solid var(--main-color-2);
}
.progress-wrap__indicator {
  height: 2px;
  position: absolute;
  left: 0;
  bottom: -2px;
  background-color: var(--action-color-2);
}
.radio {
  position: relative;
  display: flex;
  align-items: center;
  box-sizing: border-box;
  line-height: 16px;
}
.radio input[type=radio] {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  margin: 0;
  opacity: 0;
  outline: none;
}
.radio input[type=radio]:not([disabled]) {
  cursor: pointer;
}
.radio__mark {
  position: relative;
  width: 14px;
  height: 14px;
  min-width: 14px;
  min-height: 14px;
  box-sizing: border-box;
  margin-right: 16px;
  border: 1px solid var(--main-color-3);
  border-radius: 7px;
  background-color: var(--main-color-1);
  transition: border-color 0.2s ease-out, background-color 0.2s ease-out, border-width 0.1s ease-out;
}
input[type=radio]:checked ~ .radio__mark {
  border-color: var(--action-color-2);
  border-width: 5px;
}
input[disabled] ~ .radio__mark {
  opacity: .5;
  cursor: not-allowed;
}
input[disabled] ~ .radio__content {
  opacity: .5;
  cursor: not-allowed;
}
.radio input[disabled] {
  pointer-events: none;
}
.radio:hover input[type=radio]:not([disabled]):not(:checked) ~ .radio__mark {
  background-color: var(--main-color-2);
}
.radio + .radio {
  margin-top: 8px;
}
.dl-select {
  position: relative;
  height: 32px;
  border-radius: 2px;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  border: 1px solid var(--main-color-3);
  background-color: var(--primary-bg);
  max-width: 310px;
  padding: 8px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  color: var(--main-color-8);
  font-weight: normal;
  cursor: pointer;
  transition: background-color 200ms ease-in, box-shadow 100ms ease-in;
  /* component styles */
  /* group */
}
.dl-select_popup {
  z-index: 1;
}
.dl-select_popup_tiny .dl-select_content {
  min-width: 128px;
}
.dl-select_noborder {
  border: none;
  box-shadow: none;
  border-radius: 0;
  padding: 8px 16px;
}
.dl-select_title {
  display: flex;
  flex: 1 0;
  max-width: 100%;
  overflow: hidden;
  align-items: center;
}
.dl-select_title-text {
  flex: 1 0;
  line-height: 16px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.dl-select_title > .dl-select_button {
  width: 16px;
  height: 16px;
  display: flex;
  align-items: center;
  margin-left: 8px;
  transition: transform 200ms ease-in;
}
.dl-select_title > .dl-select_button svg use {
  transition: fill 200ms ease-in;
  fill: var(--main-color-8);
}
.dl-select_content {
  display: flex;
  min-width: 210px;
  max-width: 310px;
  overflow-y: auto;
  background-color: var(--primary-bg);
  box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.5);
  padding: 4px 0;
  flex-direction: column;
}
.dl-select_content_footer {
  margin: 1px 0 0 0;
  padding: 1px 0 0 0;
  border-top: 1px solid var(--main-color-2);
}
.dl-select_content_list {
  display: flex;
  flex-direction: column;
  max-height: 350px;
  overflow-y: auto;
}
.dl-select_item {
  display: flex;
  align-items: center;
  flex-shrink: 0;
  min-height: 32px;
  box-sizing: border-box;
  padding: 0 12px 0 12px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  cursor: pointer;
  transition: background-color 100ms ease-in, color 100ms ease-in;
  color: var(--main-color-8);
}
.dl-select_item svg use {
  transition: fill 100ms ease-in;
  fill: var(--main-color-8);
}
.dl-select_item:not([disabled]):not(.disabled):not(.selected):hover {
  background-color: var(--main-color-1);
}
.dl-select_item.selected {
  background-color: var(--main-color-3);
  cursor: default;
  font-weight: 600;
}
.dl-select_item.disabled,
.dl-select_item[disabled] {
  color: var(--main-color-5);
}
.dl-select:not([disabled]):not(.disabled):not(.select--open).opened,
.dl-select:not([disabled]):not(.disabled):not(.select--open):active,
.dl-select:not([disabled]):not(.disabled):not(.select--open):hover {
  background-color: var(--main-color-2);
}
.dl-select:not([disabled]):not(.disabled):not(.select--open).opened .dl-select_title > .dl-select_button svg use,
.dl-select:not([disabled]):not(.disabled):not(.select--open):active .dl-select_title > .dl-select_button svg use,
.dl-select:not([disabled]):not(.disabled):not(.select--open):hover .dl-select_title > .dl-select_button svg use {
  fill: var(--main-color-8);
}
.dl-select:not([disabled]):not(.disabled).opened .dl-select_title > .dl-select_button,
.dl-select:not([disabled]):not(.disabled):active .dl-select_title > .dl-select_button {
  transform: rotate(-180deg);
}
.dl-select.disabled,
.dl-select[disabled] {
  opacity: .5;
  cursor: not-allowed;
}
.dl-select.select--open {
  border: none;
  box-shadow: none;
  padding: 0;
  height: auto;
}
.dl-select.select--open .dl-select_button {
  transition: none;
}
.dl-select.select--open:not([disabled]):not(.disabled).opened .dl-select_title > .dl-select_button,
.dl-select.select--open:not([disabled]):not(.disabled):active .dl-select_title > .dl-select_button,
.dl-select.select--open:not([disabled]):not(.disabled):hover .dl-select_title > .dl-select_button {
  background-color: var(--main-color-2);
}
.dl-select.select--open:not([disabled]):not(.disabled).opened .dl-select_title > .dl-select_button svg use,
.dl-select.select--open:not([disabled]):not(.disabled):active .dl-select_title > .dl-select_button svg use,
.dl-select.select--open:not([disabled]):not(.disabled):hover .dl-select_title > .dl-select_button svg use {
  fill: var(--main-color-8);
}
.dl-select.select--open .dl-select_content .dl-select_item.selected {
  background-color: transparent;
  font-weight: normal;
}
.dl-select_group {
  padding: 1px 0;
}
.dl-select_group:last-child {
  padding-bottom: 0;
}
.dl-select_group:first-child {
  padding-top: 0;
}
.dl-select_group:not(:last-child) {
  border-bottom: 1px solid var(--main-color-2);
}
.dl-select_group_title {
  display: flex;
  align-items: center;
  height: 24px;
  padding: 0 12px;
  color: var(--main-color-5);
  cursor: default;
}
@keyframes dl-select_fade-in {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, -8px, 0);
    transform: translate3d(0, -8px, 0);
  }
  to {
    opacity: 1;
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}
.dl-select_fade-in {
  -webkit-animation-name: dl-select_fade-in;
  animation-name: dl-select_fade-in;
  -webkit-animation-timing-function: cubic-bezier(0.15, 0.5, 0.2, 1);
  animation-timing-function: cubic-bezier(0.15, 0.5, 0.2, 1);
  -webkit-animation-duration: .25s;
  animation-duration: .25s;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
}
.dl-loader_wrap {
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.dl-loader_wrap .dl-loader {
  border-radius: 50%;
  border-top: solid transparent;
  border-right: solid transparent;
  border-bottom: solid transparent;
  border-left: solid transparent;
  animation: lds-spinner 1.3s infinite linear;
}
.dl-loader_wrap .dl-loader.dl-size--small {
  width: 16px;
  height: 16px;
  border-width: 2px;
}
.dl-loader_wrap .dl-loader.dl-size--medium {
  width: 32px;
  height: 32px;
  border-width: 4px;
}
.dl-loader_wrap .dl-loader.dl-size--large {
  width: 48px;
  height: 48px;
  border-width: 6px;
}
.dl-loader_wrap .dl-loader.type--primary {
  border-left-color: var(--action-color-2);
}
.dl-loader_wrap .dl-loader.type--secondary {
  border-left-color: var(--main-color-3);
}
@keyframes lds-spinner {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.renamed-text-input {
  position: relative;
}
.renamed-text-input__expander {
  display: inline-block;
  box-sizing: border-box;
  min-width: 16px;
  padding: 7px 0;
  visibility: collapse;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
}
.renamed-text-input input {
  position: absolute;
  left: 0;
  right: 0;
  width: 100%;
  padding: 7px 0;
  border: none;
  outline: none;
  background: transparent;
  color: inherit;
}
.renamed-text-input input,
.renamed-text-input input:focus {
  border-top: 1px solid transparent;
  border-bottom: 1px solid var(--action-color-2);
}
.dl-textarea {
  line-height: 18px;
}
.dl-textarea--fixed {
  resize: none;
}
.dl_input {
  background: var(--primary-bg);
  color: var(--primary-fg);
  box-sizing: border-box;
  padding: 7px 8px;
  outline: none;
  border: 1px solid var(--border-color);
  transition: border-color 0.15s ease-out;
  font-size: 12px;
  line-height: 16px;
  /* Hide arrows for number input */
  /* Chrome, Safari, Edge, Opera */
  /* Firefox */
}
.dl_input:not([disabled]):not([readonly]):focus {
  border-color: var(--action-color-3);
}
.dl_input[disabled] {
  background: var(--main-color-1);
}
.dl_input_error {
  border-color: var(--negative-color-2);
}
.dl_input::-webkit-outer-spin-button,
.dl_input::-webkit-inner-spin-button {
  display: none;
}
.dl_input[type=number] {
  -moz-appearance: textfield;
}
h2.dl-title {
  font-size: 20px;
  line-height: 24px;
  font-weight: 700;
  color: var(--main-color-9);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  margin: 0;
}
h4.dl-title {
  font-size: 14px;
  line-height: 20px;
  font-weight: 600;
  color: var(--main-color-9);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  margin: 0;
}
.dl-toggle {
  display: flex;
  align-items: center;
}
.dl-toggle_button {
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;
  padding: 8px;
  border: 1px solid var(--main-color-3);
  transition: background-color 200ms ease-in;
  cursor: pointer;
}
.dl-toggle_button > .icon {
  height: 16px;
  width: 16px;
}
.dl-toggle_button > .icon > use {
  transition: fill 200ms ease-in;
  fill: var(--main-color-5);
}
.dl-toggle_button:first-child {
  border-top-left-radius: 2px;
  border-bottom-left-radius: 2px;
}
.dl-toggle_button:last-child {
  border-top-right-radius: 2px;
  border-bottom-right-radius: 2px;
}
.dl-toggle_button:not(:first-child) {
  border-left-width: 0;
}
.dl-toggle_button.selected,
.dl-toggle_button:hover {
  background-color: var(--main-color-2);
}
.dl-toggle_button.selected svg use,
.dl-toggle_button:hover svg use {
  fill: var(--main-color-8);
}
.toggler.toggler_dark {
  border-color: var(--main-color-3);
}
.toggler.toggler_dark::after {
  background-color: var(--main-color-7);
}
.toggler.toggler_dark.active {
  border-color: var(--positive-color-1);
}
.toggler.toggler_dark.active::after {
  background-color: var(--positive-color-2);
  filter: brightness(120%);
}
.toggler {
  width: 19px;
  height: 10px;
  border-radius: 10px;
  margin: 1px;
  position: relative;
  display: inline-block;
  background-color: var(--main-color-3);
  cursor: pointer;
}
.toggler::after {
  left: -1px;
  top: -1px;
  width: 12px;
  height: 12px;
  border-radius: 12px;
}
.toggler.active::after {
  left: 0;
  transform: translateX(8px);
}
.toggler::after {
  position: absolute;
  display: inline-block;
  content: ' ';
  background-color: var(--main-color-6);
  transition: background-color 0.2s ease-out, transform 0.3s ease-out;
}
.toggler.active {
  background-color: var(--action-color-1);
}
.toggler.active::after {
  background-color: var(--action-color-2);
}
.toggler.dl-size--large {
  width: 31px;
  height: 16px;
  border-radius: 16px;
  margin: 2px;
}
.toggler.dl-size--large::after {
  left: -2px;
  top: -2px;
  width: 20px;
  height: 20px;
  border-radius: 20px;
}
.toggler.dl-size--large.active::after {
  left: 0;
  transform: translateX(13px);
}
.toggler.dl-size--medium {
  width: 23px;
  height: 12px;
  border-radius: 12px;
  margin: 2px;
}
.toggler.dl-size--medium::after {
  left: -2px;
  top: -2px;
  width: 16px;
  height: 16px;
  border-radius: 16px;
}
.toggler.dl-size--medium.active::after {
  left: 0;
  transform: translateX(9px);
}
.dl-files-url-dialog {
  width: 320px;
}
.dl-files-url-dialog_error,
.dl-files-url-dialog_waiting-on-kernel {
  min-height: 28px;
  margin-top: 4px;
  text-align: center;
}
.dl-files-url-dialog_error {
  color: var(--negative-color-2);
}
.dl-files-url-dialog_content {
  margin-top: 32px;
}
.dl-files-url-dialog_url {
  width: 100%;
}
.dl-files-url-dialog_bar {
  text-align: right;
}
.popup {
  display: inline-block;
  background: var(--primary-bg);
  max-height: 95vh;
  /* close button */
  /* loading view */
}
.popup-size-s {
  width: 566px;
  height: 514px;
}
.popup-size-m {
  width: 626px;
  height: 640px;
}
.popup-size-l {
  width: 826px;
  height: 640px;
}
.popup.popup-with-title {
  padding-top: 0;
}
.popup.popup-with-title .popup_header {
  display: block;
}
.popup.popup-with-title .popup_close use,
.popup.popup-with-title .popup_close g {
  fill: var(--main-color-4);
}
.popup.popup-with-title .popup_content {
  height: calc(100% - 30px);
  box-sizing: border-box;
}
.popup.popup-no-close-btn {
  padding-top: 0;
}
.popup.popup-no-close-btn .popup_close {
  display: none;
}
.popup-no-padding .popup_content {
  padding: 0;
}
.popup_header {
  box-sizing: border-box;
  display: none;
  background-color: var(--pale-bg);
  padding: 7px 32px 7px 12px;
  min-height: 30px;
}
.popup_header .input-search {
  width: 100%;
  margin: 8px 0;
}
.popup_footer {
  background-color: var(--pale-bg);
  padding: 4px;
  color: var(--contrast-fg);
  border-radius: 0 0 2px 2px;
  display: inline-flex;
  flex-direction: row-reverse;
  user-select: none;
  width: 100%;
  box-sizing: border-box;
}
.popup_title {
  display: block;
  font-size: 12px;
  font-weight: normal;
  color: var(--contrast-fg);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.popup-global {
  position: fixed;
  /*z-index: 3;*/
  /*TODO: revert to 3 when history popup z-index will be fixed*/
  z-index: 1100;
}
.popup-full-screen {
  width: 100%;
  top: 48px;
  bottom: 0;
  display: flex;
  flex-direction: column;
}
.page-editor .popup-full-screen {
  bottom: 24px;
}
.popup-full-screen .popup_header {
  display: none;
  padding: 0;
}
.popup-full-screen .icon.popup_close {
  right: 16px;
  top: 16px;
  z-index: 3;
}
.popup-full-screen .popup_title {
  box-sizing: border-box;
  width: 100%;
  max-width: 980px;
  margin: 0 auto;
  padding: 7px 40px;
}
.popup-full-screen_content {
  box-sizing: border-box;
  height: 100%;
  width: 100%;
  max-width: 980px;
  margin: 0 auto;
  padding: 0 40px;
}
.popup-full-screen_content-wrapper {
  position: relative;
  overflow: auto;
  height: 100%;
}
.popup-full-screen.popup-with-title .icon.popup_close {
  top: 46px;
}
.popup-full-screen.popup-with-title .icon.popup_close use,
.popup-full-screen.popup-with-title .icon.popup_close g {
  fill: var(--main-color-8);
}
.popup-modal {
  padding-top: 30px;
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.3);
}
.popup-shadowed {
  box-shadow: var(--popup-shadow);
}
.popup_content {
  padding: 12px;
  overflow: auto;
}
.popup_shim {
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  /*z-index: 2;*/
  /*TODO: revert to 2 when history popup z-index will be fixed*/
  z-index: 1100;
  background: var(--main-color-9);
  opacity: 0.04;
}
.popup_close.icon {
  position: absolute;
  right: 12px;
  top: 8px;
  cursor: pointer;
  opacity: 0.7;
  transition: opacity 0.15s ease-out;
  z-index: 1;
}
.popup_close.icon:before {
  font-size: 14px !important;
}
.popup_close:hover {
  opacity: 1;
}
.popup-loading.popup {
  display: flex;
  align-items: center;
  background: transparent;
  color: var(--main-color-6);
  box-shadow: none;
}
.popup-loading .spinner {
  margin-right: 8px;
}
.menu {
  overflow: auto;
  min-width: 220px;
  max-width: 440px;
}
.menu-section {
  position: relative;
  padding: 4px 0;
  border-top: 1px solid var(--main-color-2);
  margin-top: -1px;
}
.menu_no-disabled .menu-item.disabled,
.menu_no-disabled .menu-item[disabled] {
  display: none;
}
.menu_no-icons .menu-item_icon {
  display: none;
}
.menu_no-icons .menu-item_icon.icon-check-mark {
  display: block;
}
.menu_inline-icons .menu-item_icon {
  position: initial;
  margin: 0 0 -1px 8px;
}
.menu_footer {
  padding: 0 0 4px 24px;
  font-size: 10px;
  line-height: 20px;
  color: var(--main-color-7);
  border-top: 1px solid var(--main-color-2);
}
.menu.menu-on-top {
  z-index: 1102;
}
.menu-item {
  display: block;
  position: relative;
  border-radius: 0;
  padding: 6px 12px 6px 24px;
  cursor: pointer;
  user-select: none;
}
.menu-item:hover {
  background: var(--main-color-1);
}
.menu-item_content {
  display: flex;
}
.menu-item_content .icon-flyout {
  transform: rotate(-90deg);
}
.menu-item_content .icon-flyout use,
.menu-item_content .icon-flyout g {
  fill: var(--main-color-7);
}
.menu-item_icon {
  position: absolute;
  left: 6px;
  top: 8px;
  color: var(--main-color-8);
}
.menu-item_label {
  flex-grow: 1;
}
.menu-item_label:first-letter {
  text-transform: uppercase;
}
.menu-item_pro .menu-item_label::after {
  content: 'pro';
  display: inline-block;
  margin-left: 8px;
  padding: 3px 4px;
  background: var(--main-color-5);
  border-radius: 2px;
  font-size: 8px;
  font-weight: bold;
  text-transform: uppercase;
  color: var(--contrast-fg);
  vertical-align: text-top;
}
.menu-item_disabled .menu-item_label {
  color: var(--main-color-5);
}
.menu-item_shortcut {
  position: relative;
  right: -4px;
  color: var(--main-color-6);
  margin-left: 10px;
}
.menu-item.disabled,
.menu-item[disabled] {
  color: var(--main-color-5);
  cursor: default;
}
.menu-item_description {
  font-size: 10px;
  color: var(--main-color-4);
  padding-top: 3px;
}
.tooltip.popup {
  padding: 8px;
  width: max-content;
  max-width: 250px;
  border-radius: 4px;
  pointer-events: none;
  z-index: 1;
  background: var(--tooltip-bg);
  color: var(--tooltip-fg);
  font-size: 12px;
  line-height: 16px;
}
.tooltip.popup_content {
  white-space: nowrap;
}
.tooltip.popup-caret {
  font-weight: bold;
  z-index: 1;
}
.dnd-icons_container {
  position: absolute;
  z-index: -1;
  left: -9999px;
  bottom: -9999px;
  width: 0px;
  height: 0px;
}
.user-avatar {
  display: inline-block;
  width: 30px;
  height: 30px;
  letter-spacing: 0.08em;
  line-height: 30px;
  text-align: center;
  color: rgba(255, 255, 255, 0.9);
  vertical-align: middle;
  text-transform: uppercase;
  background-size: cover;
  background-repeat: no-repeat;
  border-radius: 25px;
  cursor: pointer;
  opacity: 0.85;
}
.monaco-editor .monaco-remote-cursor,
.monaco-editor .monaco-remote-cursor-tooltip {
  z-index: inherit;
}
.setting_numeric {
  width: 72px;
}
.settings {
  height: 100%;
  display: grid;
  grid-template-rows: 1fr auto;
  background: var(--primary-bg);
}
.settings__content {
  overflow: auto;
}
.settings__row {
  margin: 12px 0;
}
.settings__bar {
  margin: 32px 0 16px;
}
.grammar-dictionary-list {
  display: grid;
  grid-row-gap: 8px;
}
.grammar-dictionary-list__list-title {
  margin: 0;
}
.grammar-dictionary-list__edit-zone {
  margin-left: 8px;
}
.grammar-dictionary-list__edit-warning {
  justify-self: center;
  color: var(--main-color-5);
  font-size: 12px;
  line-height: 16px;
}
.grammar-dictionary-list__entries {
  display: grid;
  row-gap: 4px;
  background-color: var(--main-color-1);
  padding: 8px;
}
.grammar-dictionary-list__entry {
  display: grid;
  grid-template-columns: 1fr auto;
  align-items: center;
  padding: 0 8px;
}
.grammar-settings-dialog {
  display: grid;
  grid-row-gap: 16px;
}
.grammar-settings-dialog__toggler {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-column-gap: 8px;
  align-items: center;
}
.extract-code {
  width: 280px;
}
.extract-code .input {
  width: 100%;
}
.extract-code_bar {
  margin-top: 16px;
  text-align: right;
}
.cell-collapse__icon-collapse,
.cell-collapse__icon-expand {
  position: absolute;
  left: -8px;
  z-index: 1;
}
.cell-collapse__icon-collapse use,
.cell-collapse__icon-expand use {
  stroke: var(--main-color-4);
  fill: var(--workbook-bg);
}
.cell-collapse__icon-collapse_highlighted use,
.cell-collapse__icon-expand_highlighted use {
  stroke: var(--action-color-2);
}
.cell-collapse__icon-collapse_top {
  top: 11px;
  transform: rotate(180deg);
  cursor: pointer;
}
.cell-collapse__icon-collapse_bottom {
  bottom: 10px;
  cursor: pointer;
}
.cell-collapse__icon-expand {
  top: 10px;
  cursor: pointer;
}
.code-editor_pending-relayout {
  overflow: hidden;
}
.monaco-diff-editor .lines-content .char-insert {
  background-color: #BEE6BE;
}
.monaco-diff-editor .lines-content .char-delete {
  background-color: #D6D6D6;
}
@font-face {
  font-family: "codicon2";
  src: url(/assets/fonts/codicon.ttf) format("truetype");
}
.monaco-editor .codicon[class*=codicon-] {
  font-family: 'codicon2';
}
.monaco-editor div.hover-row.status-bar {
  display: none !important;
}
.monaco-editor .monaco-remote-selection {
  opacity: 0.3;
}
.monaco-editor .lines-content .view-overlays .current-line {
  display: none;
}
.monaco-editor .lines-content .view-overlays.focused .current-line {
  display: block;
}
.monaco-editor .cursor {
  position: relative;
}
.monaco-editor .parameter-hints-widget span {
  white-space: normal;
}
.monaco-editor .parameter-hints-widget .button {
  padding: 0;
  min-width: 0;
  margin: 0;
  border: 0;
  color: unset;
}
.monaco-editor .parameter-hints-widget hr {
  border-bottom: solid 1px rgba(0, 0, 0, 0.3);
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .monaco-icon-label {
  overflow: unset;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon::before {
  content: " ";
  width: 16px;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-class::before {
  background-image: url("/assets/editor/class.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-color::before {
  background-image: url("/assets/editor/cyan-dot.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-field::before {
  background-image: url("/assets/editor/field.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-file::before {
  background-image: url("/assets/editor/pythonFile.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-folder::before {
  background-image: url("/assets/editor/folder.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-function::before {
  background-image: url("/assets/editor/function.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-keyword + .monaco-icon-label {
  font-weight: bold;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-keyword::before {
  background-image: none !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-method::before {
  background-image: url("/assets/editor/method.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-property::before {
  background-image: url("/assets/editor/property.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-snippet::before {
  background-image: url("/assets/editor/propertyGetter.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-text::before {
  background-image: url("/assets/editor/text.svg") !important;
}
.monaco-editor .suggest-widget .monaco-list .monaco-list-row .suggest-icon.codicon-symbol-variable::before {
  background-image: url("/assets/editor/variable.svg") !important;
}
.monaco-editor .hover-contents {
  white-space: normal;
}
.monaco-editor .hover-contents h1,
.monaco-editor .hover-contents h2,
.monaco-editor .hover-contents h3,
.monaco-editor .hover-contents h4,
.monaco-editor .hover-contents h5,
.monaco-editor .hover-contents h6 {
  margin-top: 0;
  padding-top: 8px;
}
.monaco-editor .hover-contents .definition {
  padding: 4px 17px 1px 8px;
  border-bottom: thin solid rgba(0, 0, 0, 0.3);
}
.monaco-editor .hover-contents .definition-only {
  padding: 4px 17px 0 8px;
}
.monaco-editor .hover-contents .definition-only pre {
  margin-bottom: 0;
}
.monaco-editor .hover-contents .content {
  padding: 5px 16px 0 8px;
  max-width: 100%;
}
.monaco-editor .hover-contents .content-only {
  padding: 8px 16px 0 8px;
  max-width: 100%;
}
.monaco-editor .hover-contents .bottom {
  padding: 3px 16px 0 8px;
}
.monaco-editor .hover-contents .bottom-no-content {
  padding: 5px 16px 0 8px;
}
.monaco-editor .hover-contents p {
  padding: 1px 0 2px 0;
}
.monaco-editor .hover-contents ol {
  padding: 0 16px 0 20px;
  list-style: decimal;
}
.monaco-editor .hover-contents ul {
  padding: 0 16px 0 20px;
}
.monaco-editor .hover-contents li {
  padding: 1px 0 2px 0;
}
.monaco-editor .hover-contents .grayed {
  color: #909090;
  display: inline;
}
.monaco-editor .hover-contents .centered {
  text-align: center;
}
.monaco-editor .hover-contents .sections {
  padding: 0 16px 0 8px;
  border-spacing: 0;
}
.monaco-editor .hover-contents tr {
  margin: 0;
  padding: 0;
}
.monaco-editor .hover-contents table p {
  padding-bottom: 0;
}
.monaco-editor .hover-contents table {
  border-color: transparent;
}
.monaco-editor .hover-contents td {
  margin: 4px 0 0 0;
  padding: 0;
  vertical-align: top;
  border-color: transparent;
}
.monaco-editor .hover-contents th {
  text-align: left;
  border-color: transparent;
}
.monaco-editor .hover-contents .section {
  color: #909090;
  padding-right: 4px;
  white-space: nowrap;
}
.monaco-editor .monaco-hover a:hover {
  text-decoration: underline;
}
.monaco-decoration_stack-frame {
  background: lightpink;
  width: 5px !important;
}
.monaco-decoration_search-match {
  background: var(--attention-color-1);
}
.monaco-decoration_identifier-match {
  background: #a680ff36;
}
.monaco-decoration_variable {
  font-style: italic;
  margin-left: 12px;
  color: var(--main-color-5);
}
.cr-collaborator {
  display: inline-flex;
  margin-left: -10px;
  opacity: 0.9;
  transition: transform 0.2s ease-out, opacity 0.2s ease-out;
  vertical-align: middle;
}
.cr-collaborator.selected,
.cr-collaborator:hover {
  position: relative;
  transform: scale(1, 1);
  opacity: 1;
  z-index: 1;
  animation: cr-collaborator-rollLeft 0.3s ease-out;
}
@keyframes cr-collaborator-rollLeft {
  50% {
    margin-left: -3px;
  }
  100% {
    margin-left: -10px;
  }
}
.cr-collaborator-line {
  margin: 5px 0;
  display: flex;
  align-items: center;
}
.cr-collaborator-line .user-avatar {
  flex-shrink: 0;
}
.cr-collaborator-line_name {
  display: block;
  flex-grow: 1;
  margin-left: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.cr-collaborators {
  display: inline-flex;
  margin: 0 6px;
  vertical-align: middle;
}
.cr-collaborators_items {
  overflow: hidden;
  height: 30px;
  padding-left: 10px;
  white-space: normal;
}
.cr-collaborators .button {
  flex-grow: 1;
  flex-shrink: 0;
  padding: 7px;
}
.cr-collaborators-dialog_collaborators {
  overflow: auto;
  max-height: 100%;
}
.dl-collaborators-label {
  position: fixed;
  left: 50%;
  top: -10px;
  transform: translate(-50%, 0);
  z-index: 10;
  border-radius: 10px;
  padding: 16px 12px 6px;
  background: var(--action-color);
  color: var(--main-color-3);
}
.feedback-container {
  background-color: rgba(46, 173, 251, 0.6);
  border-radius: 20px;
  background-size: calc(100% - 14px);
  background-repeat: no-repeat;
  background-position: center;
  margin-bottom: 10px;
  transition: 0.5s all;
  font-size: 0;
  position: absolute;
  bottom: 55px;
  right: 2px;
  z-index: 1099;
}
.feedback-container .icon {
  margin: 8px;
}
.feedback-container:hover {
  background-color: #2eadfb;
  cursor: pointer;
}
.is-fsrootmapper > .feedback-container {
  bottom: 0;
}
.feedback-shortmessage.is-ok .feedback-shortmessage-less,
.feedback-shortmessage.is-ok .feedback-shortmessage-more {
  display: none;
}
.feedback-shortmessage.is-less .feedback-shortmessage-ok,
.feedback-shortmessage.is-less .feedback-shortmessage-more {
  display: none;
}
.feedback-shortmessage.is-more .feedback-shortmessage-less,
.feedback-shortmessage.is-more .feedback-shortmessage-ok {
  display: none;
}
.feedback-popup {
  min-height: 280px;
  min-width: 400px;
  margin-top: 10px;
}
.feedback-popup input {
  margin-bottom: 10px;
}
.feedback-popup textarea {
  margin-bottom: 2px;
  resize: none;
}
.feedback-popup input,
.feedback-popup textarea {
  display: block;
  width: 100%;
}
.feedback-popup textarea {
  height: 220px;
}
.feedback-popup button {
  float: right;
  margin-top: 5px;
}
.feedback-link {
  margin-bottom: 5px;
}
.feedback-footer {
  overflow: auto;
}
.feedback-flag {
  margin: 10px 0;
}
.dl-password-ch {
  width: 300px;
}
.dl-password-ch_subtitle {
  margin: 20px 0 10px;
}
.dl-password-ch_section:first-child .dl-password-ch_subtitle {
  margin-top: 0;
}
.dl-password-ch .input {
  width: 100%;
}
.zxcvbn {
  width: 100%;
}
.zxcvbn_hidden {
  visibility: hidden;
}
.zxcvbn_theme-dark.zxcvbn_hidden {
  display: none;
}
.zxcvbn-meter {
  -moz-appearance: none;
  appearance: none;
  width: 100%;
}
.zxcvbn-meter::-webkit-meter-bar {
  background: rgba(0, 0, 0, 0.1) none;
}
.zxcvbn-meter[value="1"]::-webkit-meter-optimum-value {
  background: red;
}
.zxcvbn-meter[value="2"]::-webkit-meter-optimum-value {
  background: orange;
}
.zxcvbn-meter[value="3"]::-webkit-meter-optimum-value {
  background: yellow;
}
.zxcvbn-meter[value="4"]::-webkit-meter-optimum-value {
  background: green;
}
.zxcvbn-meter[value="1"]::-moz-meter-bar {
  background: red;
}
.zxcvbn-meter[value="2"]::-moz-meter-bar {
  background: yellow;
}
.zxcvbn-meter[value="3"]::-moz-meter-bar {
  background: orange;
}
.zxcvbn-meter[value="4"]::-moz-meter-bar {
  background: green;
}
.dl-account-settings .tabs {
  box-sizing: border-box;
  position: relative;
}
.dl-account-settings .tabs_content {
  margin: 0 -20px;
  padding: 0 20px;
}
.dl-email {
  display: flex;
  padding: 8px 28px 8px 8px;
  position: relative;
  border-top: 1px solid var(--border-color);
  /* verified status */
  /* primary status */
  /* pending status */
}
.dl-email:last-child {
  border-bottom: 1px solid var(--border-color);
}
.dl-email_text {
  flex-grow: 3;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.dl-email_primary-btn {
  display: none;
}
.dl-email_status,
.dl-email_primary-btn {
  padding-left: 10px;
  flex-basis: 180px;
  flex-shrink: 0;
}
.dl-email_status {
  color: var(--main-color-4);
}
.dl-email_primary-btn {
  color: var(--action-color);
  cursor: pointer;
}
.dl-email_remove {
  position: absolute !important;
  top: 10px !important;
  right: 11px;
  visibility: hidden;
}
.dl-email.dl-email-verified:hover .dl-email_primary-btn {
  display: block;
}
.dl-email.dl-email-verified:hover .dl-email_remove {
  visibility: visible;
}
.dl-email.dl-email-verified:hover .dl-email_status {
  display: none;
}
.dl-email.dl-email-primary .dl-email_status {
  color: var(--main-color-9);
}
.dl-email.dl-email-pending .dl-email_status-icon {
  visibility: collapse;
}
.dl-email.dl-email-pending .dl-email_text {
  color: var(--main-color-4);
}
.dl-email.dl-email-pending:hover .dl-email_remove {
  visibility: visible;
}
.dl-user-email {
  padding: 6px 0;
  border: 0 solid var(--border-color);
  border-top-width: 1px;
}
.dl-user-email:last-child {
  border-bottom-width: 1px;
}
.dl-user-info_subtitle {
  font-size: 14px;
  font-weight: initial;
}
.dl-user-info_section {
  padding: 12px 0;
}
.dl-user-info_bar {
  text-align: right;
}
.dl-user-repo-key {
  padding: 6px 0;
  border: 0 solid var(--border-color);
  border-top-width: 1px;
  word-wrap: break-word;
}
.dl-user-repo-key:last-child {
  border-bottom-width: 1px;
}
.dl-user-settings {
  display: grid;
  grid-template-rows: auto auto auto 1fr auto auto auto auto;
  height: 100%;
}
.dl-user-settings_subtitle {
  font-size: 14px;
  font-weight: initial;
  margin-bottom: 4px;
}
.dl-user-settings_line {
  border-top: 1px solid var(--border-color);
  margin: 10px 0;
}
.dl-user-settings_column:last-child {
  padding-left: 10px;
}
.dl-user-settings_column:first-child {
  padding-right: 10px;
}
.dl-user-settings .input {
  width: 100%;
}
.dl-user-settings .colorpicker .input {
  width: auto;
}
.dl-user-settings_section {
  margin: 8px 0;
}
.dl-user-settings_section:first-child {
  margin-top: 0;
}
.dl-user-settings_section-emails {
  display: grid;
  grid-template-rows: auto 1fr;
}
.dl-user-settings_section-delete-user {
  text-align: right;
}
.dl-user-settings_section-delete-user .button {
  border-color: var(--negative-color-2);
}
.dl-user-settings_row {
  margin-top: 8px;
  overflow: auto;
}
.dl-user-settings_row:first-child {
  margin-top: 0;
}
.dl-user-settings_emails-list {
  list-style: none;
  width: 100%;
  overflow: auto;
  padding: 0;
  box-sizing: border-box;
}
.dl-user-settings_row-emails {
  display: flex;
  margin-top: 4px;
}
.dl-user-settings_row-emails .input {
  width: auto;
  min-width: 0;
  align-self: center;
  flex-grow: 1;
}
.dl-user-settings_row-password {
  display: grid;
  align-items: end;
  grid-template-columns: 1fr auto;
}
.dl-user-settings_row-password .button {
  margin: 0;
}
.dl-user-settings .button:not(.type--link) {
  margin-right: 0;
  width: 210px;
}
.dl-user-settings .select {
  width: 100%;
}
.dl-user-settings_change-password {
  display: inline-block;
  margin: 20px 0;
  cursor: pointer;
}
.dl-user-settings_change-password:hover {
  text-decoration: underline;
  color: var(--action-color);
}
.dl-user-settings .user-avatar {
  margin-top: -2px;
  margin-left: 6px;
}
.dl-delete-user {
  width: 400px;
}
.dl-delete-user_note {
  background: var(--attention-color-1);
  border-radius: 4px;
  padding: 9px 16px;
  margin-top: 10px;
}
.dl-delete-user .input {
  width: 100%;
}
.dl-delete-user_row {
  margin: 18px 0;
}
.dl-delete-user_subtitle {
  margin-bottom: 4px;
}
.dl-delete-user_bar {
  margin-top: 30px;
  text-align: right;
}
.dl-delete-user_bar .button {
  margin-right: 0;
}
.dl-delete-user_forgot-password {
  display: inline-block;
  visibility: collapse;
  cursor: pointer;
  user-select: none;
  margin-top: 8px;
  color: var(--action-color);
  text-decoration: underline;
}
.dl-delete-user_forgot-password-shown {
  visibility: visible;
}
.popup.simple-alert-popup.is-error header:before {
  display: none;
  content: '\e15a';
  color: var(--negative-color-3);
  margin-right: 5px;
}
.popup.simple-alert-popup.is-warning header:before {
  display: none;
  content: '\e267';
  color: var(--attention-color-2);
  margin-right: 5px;
}
.simple-alert {
  max-width: 400px;
}
.simple-alert_text {
  margin: 20px 0 0;
  white-space: pre-wrap;
}
.simple-alert-error .simple-alert_text {
  white-space: initial;
}
.simple-alert_input {
  width: 100%;
  box-sizing: border-box;
}
.simple-alert_input-wrapper {
  padding: 0 3px;
  margin: 16px 0 0;
}
.simple-alert_bar {
  margin: 32px 0 0;
}
.tab-header {
  display: inline-block;
  padding: 10px 16px;
  border-bottom: 3px solid transparent;
  margin-bottom: -1px;
  cursor: pointer;
  color: var(--main-color-4);
  user-select: none;
}
.tab-header-selected {
  color: var(--main-color-9);
  border-bottom-color: var(--action-color);
}
.tabs-tiny .tab-header {
  padding: 10px 8px;
}
.tabs {
  display: flex;
  flex-direction: column;
  height: 100%;
}
.tabs_content {
  flex-grow: 1;
  height: 100%;
  min-height: 0px;
  overflow: auto;
}
.tabs_header {
  flex-shrink: 0;
  margin-bottom: 12px;
  border-bottom: 1px solid var(--border-color);
  text-align: center;
}
.tabs-tiny .tabs_header {
  white-space: nowrap;
}
.billing-report {
  padding: 16px 0;
}
.billing-report_header {
  display: grid;
  grid-template-columns: 1fr auto;
}
.billing-report_header-title {
  margin-top: 4px;
  text-transform: capitalize;
  font-size: 20px;
  line-height: 24px;
  font-weight: 700;
  color: var(--main-color-9);
}
.billing-report_title {
  margin: 8px 0;
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
  font-weight: bold;
}
.billing-report_section {
  margin: 28px 0 8px;
}
.billing-report_resources {
  box-sizing: border-box;
  min-height: 150px;
  padding: 16px;
  border-radius: 8px;
  background: var(--main-color-1);
}
.billing-report_resources-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.billing-report_resources-title span:first-child {
  flex-grow: 1;
  flex-shrink: 0;
}
.billing-report_resources-title span:last-child {
  flex-grow: 0;
  flex-shrink: 1;
}
.billing-report_resources .dl-loader_wrap {
  min-height: 117px;
}
.billing-report_table-header,
.billing-report_table-item {
  display: grid;
  padding: 12px;
  text-align: right;
}
.billing-report_table-header *:first-child,
.billing-report_table-item *:first-child {
  text-align: left;
}
.billing-report_table-header {
  font-weight: bold;
  border-bottom: 2px solid var(--border-color);
}
.billing-report_table-items {
  margin-top: -1px;
}
.billing-report_table-item {
  border-top: 1px solid var(--border-color);
}
.billing-report_table-3 .billing-report_table-header,
.billing-report_table-3 .billing-report_table-item {
  grid-template-columns: 3fr 2fr 4fr;
}
.billing-report_table-2 .billing-report_table-header,
.billing-report_table-2 .billing-report_table-item {
  grid-template-columns: 2fr 2fr;
}
.billing-report_footnote {
  text-align: right;
  font-weight: normal;
  font-size: 12px;
  line-height: 16px;
}
.billing-report_footnote,
.billing-report_footnote a {
  color: var(--main-color-5);
}
.billing-report_footnote a {
  text-decoration: underline;
}
.billing-report_gift .input {
  min-width: 340px;
}
.billing-report_gift-content {
  display: flex;
}
.billing-report_downloads .billing-report_title {
  margin-bottom: 16px;
}
.billing-report_download {
  display: inline-flex;
  align-items: center;
  color: var(--primary-fg);
  opacity: .8;
}
.billing-report_download:hover {
  opacity: 1;
}
.billing-report_download .icon {
  margin-right: 8px;
}
.billing-report_download .icon use,
.billing-report_download .icon g {
  fill: var(--main-color-7);
}
.billing-report_instance-name {
  display: inline-flex;
  align-items: start;
}
.billing-report_instance-name .tip {
  margin-left: 8px;
}
.cr-root {
  position: relative;
  width: 100%;
  height: 100%;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}
.cr-root .wide_row {
  position: relative;
  width: 100%;
}
.cr-root_menu {
  position: relative;
  width: 100%;
}
.cr-root_permanent-alerts {
  position: relative;
  width: 100%;
}
.cr-root_application {
  position: relative;
  width: 100%;
  height: 100%;
  min-height: 0;
  display: flex;
  flex-direction: column;
}
.root-content {
  padding: 40px;
  line-height: 1.8;
}
.root-content__title {
  font: 21px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  margin: 16px 0;
}
.head {
  position: relative;
  width: 100%;
  box-sizing: border-box;
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  padding: 0 10px;
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  white-space: nowrap;
  height: 48px;
  border-radius: 0;
  margin-bottom: 0;
  background: var(--contrast-bg);
  color: var(--contrast-fg);
  /* logo */
  /* layout */
}
.head .button {
  margin: 0;
}
.head .button + .button {
  margin-left: 8px;
}
.head .logo {
  margin-right: 16px;
  vertical-align: middle;
}
.head .avatar {
  cursor: pointer;
}
.head_content-center {
  padding: 0 5px;
}
.head_content-left {
  display: flex;
  align-items: center;
}
.head_content-right {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 10px;
  text-align: right;
}
.head__action {
  display: inline-block;
  padding: 8px;
  cursor: pointer;
}
.head .search-input {
  background-color: var(--pale-bg);
  border-color: var(--pale-bg);
  transition: border-color 0.2s ease-in, width 0.2s ease-in;
  width: 188px;
}
.head .search-input input {
  color: var(--contrast-fg);
  background-color: transparent;
}
.head .search-input:hover {
  border-color: var(--main-color-6);
}
.head .search-input.focus {
  width: 238px;
}
.head .icon {
  vertical-align: sub;
  cursor: pointer;
  opacity: 0.7;
  transition: opacity 0.15s ease-out;
}
.head .icon:hover {
  opacity: 0.9;
}
.terms-page {
  position: relative;
  box-sizing: border-box;
  height: 100%;
}
.terms-page_main {
  width: 700px;
  margin: 0 auto;
  display: grid;
  grid-template-rows: 1fr auto auto;
  height: 100%;
}
.terms-page_warning {
  background: var(--attention-color-1);
  border-radius: 4px;
  padding: 6px 16px;
  margin-top: 10px;
  font-size: 17px;
  text-align: center;
}
.terms-page_logo {
  background-image: url("/logo.ico");
  background-size: contain;
  position: absolute;
  top: 8px;
  right: 20px;
  width: 50px;
  height: 50px;
}
.terms-page_body {
  padding: 10px;
  overflow: auto;
  box-shadow: inset 0px -15px 11px -16px rgba(17, 17, 17, 0.7);
}
.terms-page_body::-webkit-scrollbar {
  -webkit-appearance: none;
  width: 7px;
}
.terms-page_body::-webkit-scrollbar-thumb {
  border-radius: 4px;
  background-color: rgba(0, 0, 0, 0.5);
  -webkit-box-shadow: 0 0 1px rgba(255, 255, 255, 0.5);
}
.terms-page_section {
  margin: 20px;
}
.terms-page_section-title {
  text-transform: uppercase;
  font-weight: 900;
}
.terms-page_section-text {
  margin-top: 5px;
  margin-bottom: 5px;
}
.terms-page_section-sub {
  margin-top: 10px;
}
.terms-page_section-text,
.terms-page_section-sub {
  margin-left: 20px;
}
.terms-page_section-sub .terms-page_section-text {
  margin-left: 40px;
}
.terms-page_tail {
  margin-top: 30px;
}
.terms-page_tail-text {
  margin: 0;
}
.terms-page_flags {
  margin: 10px 0;
  padding: 10px;
  background-color: var(--main-color-1);
}
.terms-page_flags-note {
  font-size: 10px;
}
.terms-page_flag {
  margin: 5px 0;
}
.terms-page_flag:first-child {
  margin-top: 0;
}
.terms-page_footer {
  position: relative;
  overflow: hidden;
  text-align: center;
  margin-bottom: 10px;
}
.terms-page_footer-title {
  font-size: 14px;
  margin: 15px 0;
}
.terms-page_delete-button.button {
  color: var(--main-color-6);
}
.terms {
  position: relative;
  box-sizing: border-box;
  height: 100%;
}
.terms_main {
  width: 700px;
  margin: 0 auto;
  display: grid;
  grid-template-rows: 1fr auto auto;
  height: 100%;
}
.terms_warning {
  background: var(--attention-color-1);
  border-radius: 4px;
  padding: 6px 16px;
  margin-top: 10px;
  font-size: 17px;
  text-align: center;
}
.terms_logo {
  background-image: url("/logo.ico");
  background-size: contain;
  position: absolute;
  top: 8px;
  right: 20px;
  width: 50px;
  height: 50px;
}
.terms_body {
  box-shadow: inset 0px -15px 11px -16px rgba(17, 17, 17, 0.7);
  overflow: hidden;
}
.terms_body::-webkit-scrollbar {
  -webkit-appearance: none;
  width: 7px;
}
.terms_body::-webkit-scrollbar-thumb {
  border-radius: 4px;
  background-color: rgba(0, 0, 0, 0.5);
  -webkit-box-shadow: 0 0 1px rgba(255, 255, 255, 0.5);
}
.terms_section {
  margin: 20px;
}
.terms_section-title {
  text-transform: uppercase;
  font-weight: 900;
}
.terms_section-text {
  margin-top: 5px;
  margin-bottom: 5px;
}
.terms_section-sub {
  margin-top: 10px;
}
.terms_section-text,
.terms_section-sub {
  margin-left: 20px;
}
.terms_section-sub .terms_section-text {
  margin-left: 40px;
}
.terms_tail {
  margin-top: 30px;
}
.terms_tail-text {
  margin: 0;
}
.terms_flags {
  margin: 10px 0;
  padding: 10px;
  background-color: var(--main-color-1);
}
.terms_flags-note {
  font-size: 10px;
}
.terms_flag {
  margin: 5px 0;
}
.terms_flag:first-child {
  margin-top: 0;
}
.terms_footer {
  position: relative;
  overflow: hidden;
  text-align: center;
  margin-bottom: 10px;
}
.terms_footer-title {
  font-size: 14px;
  margin: 15px 0;
}
.terms_delete-button.button {
  color: var(--main-color-6);
}
.terms-content {
  overflow: auto;
  box-sizing: border-box;
  padding: 10px;
  height: 100%;
}
.terms-content h1,
.terms-content h2,
.terms-content h3,
.terms-content h4 {
  line-height: normal;
  color: var(--main-color-9);
}
.terms-content blockquote {
  margin: 12px 24px 8px;
  padding: 0 12px;
  border-left: 5px solid var(--main-color-3);
}
.terms-content p,
.terms-content ul {
  margin: 0 0 1em;
}
.terms-content ul,
.terms-content ol {
  padding-left: 28px;
}
.terms-content ol {
  list-style: decimal;
}
.billing-profile {
  position: relative;
  height: 100%;
}
.plan {
  position: relative;
  display: flex;
  flex: 1;
  flex-direction: column;
  box-sizing: border-box;
  border-radius: 4px;
  background-color: var(--main-color-1);
}
.plan:not(:first-child) {
  margin-left: 32px;
}
.plan.selected {
  box-shadow: 0px 0px 0px 4px var(--action-color);
}
.plan__stamp {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  padding: 4px 16px 8px;
  background-color: var(--action-color);
  color: var(--contrast-fg);
}
.plan__title {
  font-weight: 600;
  text-transform: capitalize;
  margin: 12px 0 16px;
  font-size: 20px;
  line-height: 24px;
  font-weight: 700;
  color: var(--main-color-9);
}
.plan__subtitle {
  font-size: 14px;
  line-height: 20px;
  font-weight: 600;
  color: var(--main-color-9);
  margin: 0 0 16px;
}
.plan__description {
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
}
.plan__options {
  flex: 1 0;
  color: var(--main-color-8);
  margin: 16px 0 16px 0;
}
.plan__option {
  position: relative;
  margin-top: 16px;
  padding-left: 24px;
}
.plan__option .icon-check-mark {
  position: absolute;
  left: 0;
  right: 0;
}
.plan__option .icon-check-mark use,
.plan__option .icon-check-mark g {
  fill: var(--action-color);
}
.plan__price {
  display: flex;
  flex-direction: column;
  margin: 12px 0 16px;
}
.plan__price-text {
  color: var(--main-color-8);
  font-size: 20px;
  line-height: 24px;
}
.plan__price .--crossed {
  text-decoration: line-through;
}
.plan__price .tip {
  margin-left: 8px;
  top: -6px;
}
.plan__promo {
  margin-top: 8px;
}
.plan__info {
  margin: 0 0 16px 0;
  color: var(--main-color-5);
  line-height: 16px;
}
.plan__content,
.plan__footer {
  padding: 16px;
}
.plan__content {
  display: flex;
  flex-direction: column;
  flex: 0 1;
  padding-top: 28px;
}
.plan__bar > .button {
  width: 100%;
}
.plan__footer {
  flex: 1 0;
  border-top: 1px solid var(--main-color-2);
  min-height: 32px;
}
.plan__footer .tip {
  margin-left: 8px;
}
.plan__warning {
  display: flex;
  margin-top: 16px;
  padding: 12px;
  line-height: 16px;
  background-color: var(--attention-color-1);
  border: 1px solid var(--attention-color-3);
}
.plan__warning .icon use {
  fill: var(--attention-color-3);
}
.plan__warning-title {
  font-weight: 700;
}
.plan__warning > :first-child {
  margin-right: 12px;
}
.plans {
  display: flex;
  box-sizing: border-box;
  flex-direction: column;
  min-height: 100%;
  padding: 36px 0 12px 0;
}
.plans__list {
  display: flex;
  align-items: stretch;
}
.plans__footer {
  display: flex;
  flex-direction: column;
  margin: 32px 0 0 0;
}
.plans__enterprise {
  display: grid;
  grid-template-columns: auto 1fr 166px;
  grid-gap: 16px;
  align-items: stretch;
  padding: 16px;
  border-radius: 4px;
  background-color: var(--main-color-1);
}
.plans__enterprise > div {
  display: flex;
  align-items: center;
}
.plans__enterprise-title {
  font-weight: 600;
  text-transform: capitalize;
  font-size: 20px;
  line-height: 24px;
  font-weight: 700;
  color: var(--main-color-9);
}
.plans__enterprise-description {
  color: var(--main-color-5);
}
.plans__enterprise-action button {
  width: 100%;
}
.plans__documentation {
  margin: 12px 0 0 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.plans__documentation,
.plans__documentation a {
  color: var(--main-color-5);
  margin-left: 2px;
}
.plans__documentation a {
  text-decoration: underline;
}
.dl-page-title {
  display: flex;
}
.dl-page-title .publishing-dashboard-title {
  flex: 1 0;
}
.dl-page-title .publishing-dashboard-upload > .progress-button {
  min-width: 200px;
}
.publishing-dashboard_header,
.publishing-dashboard .published-notebook {
  display: grid;
  grid-template-columns: 24px 30% 20% 20% auto 32px;
  grid-gap: 8px;
}
.publishing-dashboard_reactive-enabled .publishing-dashboard_header,
.publishing-dashboard_reactive-enabled .published-notebook {
  grid-template-columns: 24px 30% 15% 20% 20% auto 32px;
}
.publishing-dashboard_header > div:first-child {
  padding-left: 8px;
  grid-column: 1 / 3;
}
.publishing-dashboard .published-notebok-wrap .published-notebook {
  color: var(--main-color-8);
}
.publishing-dashboard .published-notebok-wrap .published-notebook_icon:first-child,
.publishing-dashboard .published-notebok-wrap .published-notebook_access {
  justify-content: flex-end;
}
.publishing-dashboard .published-notebok-wrap .published-notebook_icon:last-child {
  justify-content: flex-start;
}
.publishing-dashboard .published-notebok-wrap .published-notebook_name {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.publishing-dashboard .published-notebok-wrap .published-notebook_author {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.publishing-dashboard .published-notebok-wrap .published-notebook > div:last-child {
  justify-content: center;
}
.publishing-dashboard .published-notebok-wrap .published-notebook > div {
  display: flex;
  align-items: center;
}
.publishing-dashboard .published-notebok-wrap .published-notebook_running {
  margin-left: 8px;
  font-style: italic;
  color: var(--main-color-6);
}
.publishing-dashboard .published-notebok-wrap:hover {
  border-bottom-color: transparent;
  color: var(--main-color-8);
}
.published-settings {
  text-align: left;
  color: var(--primary-fg);
}
.published-settings .dialog_wrap_title > div {
  max-width: 500px;
  font-weight: 600;
  margin: 0 4px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.published-settings .tabs-wrap_content_item {
  padding: 0 16px;
}
.published-settings_row {
  display: flex;
  align-items: center;
  flex: 1 0;
}
.published-settings_row > div:first-child {
  flex: 1 0;
}
.published-settings_row:not(:last-child) {
  margin-bottom: 12px;
}
.published-settings_row--right {
  justify-content: flex-end;
}
.published-settings_info {
  color: var(--main-color-4);
}
.published-settings .tabs-wrap_header_layout {
  padding: 0 16px 0 16px;
}
.add-database-dialog {
  overflow: hidden;
  height: 100%;
}
.database-connection-error-popup {
  width: calc(890px - 2 * 32px);
  background: var(--main-color-1);
}
.database-connection-error-popup__cross {
  position: absolute;
  top: 16px;
  right: 16px;
  cursor: pointer;
}
.database-connection-error-popup__cross,
.database-connection-error-popup__cross > .icon {
  width: 16px;
  height: 16px;
}
.database-connection-error-popup__cross > .icon {
  opacity: .7;
  transition: opacity 0.15s ease-out;
}
.database-connection-error-popup__cross > .icon > use {
  fill: var(--main-color-8);
}
.database-connection-error-popup__cross > .icon:hover {
  opacity: 1;
}
.database-connection-error-popup__header {
  padding: 16px;
  display: flex;
  gap: 24px;
  align-items: center;
  overflow: hidden;
  background: var(--negative-color-1);
  font-size: 12px;
  line-height: 16px;
}
.database-connection-error-popup__title {
  display: flex;
  align-items: center;
  overflow: hidden;
}
.database-connection-error-popup__title .icon {
  padding-right: 8px;
}
.database-connection-error-popup__title .icon use {
  fill: var(--negative-color-3);
}
.database-connection-error-popup__action {
  font-weight: 600;
}
.database-connection-error-popup .clipboard-text {
  height: 160px;
}
.database-connection-status {
  display: flex;
  align-items: center;
  overflow: hidden;
}
.database-connection-status__indicator {
  padding-left: 20px;
  padding-right: 8px;
}
.database-connection-status__indicator_success use {
  fill: var(--positive-color-3);
}
.database-connection-status__indicator_failure use {
  fill: var(--negative-color-3);
}
.database-connection-status__title {
  font-size: 12px;
  line-height: 16px;
}
.database-connection-status__title_checking {
  color: var(--main-color-5);
}
.database-connection-status__title_success {
  color: var(--positive-color-3);
}
.database-connection-status__title_failure {
  color: var(--negative-color-3);
}
.database-form-page {
  display: grid;
  height: 100%;
  grid-template-columns: auto 240px;
  grid-template-rows: min-content auto min-content;
  grid-template-areas: "title title" "content sidebar" "footer footer";
  column-gap: 20px;
}
.database-form-page__title {
  grid-area: title;
  padding: 32px 32px 20px 32px;
  display: flex;
  align-items: baseline;
  gap: 12px;
  overflow: hidden;
}
.database-form-page__content {
  grid-area: content;
  padding: 0 16px 16px 32px;
  display: grid;
  grid-auto-rows: min-content;
  grid-template-columns: 3.3fr 1.7fr;
  gap: 16px 32px;
  overflow: auto;
}
.database-form-page__content-item_wide {
  grid-column-start: 1;
  grid-column-end: 3;
}
.database-form-page__sidebar {
  grid-area: sidebar;
  padding-right: 32px;
}
.database-form-page__sidebar p {
  margin: 0 0 16px 0;
}
.database-form-page__footer {
  grid-area: footer;
  padding: 24px 32px 36px 32px;
  display: flex;
  justify-content: space-between;
  border-top: 1px solid var(--main-color-2);
  overflow: hidden;
}
.database-form-page__footer .button.type--open {
  margin-right: 12px;
}
.database-type-page {
  display: grid;
  height: 100%;
  grid-template-columns: auto 240px;
  grid-template-rows: min-content auto;
  grid-template-areas: "title title" "content sidebar";
  column-gap: 36px;
}
.database-type-page__title {
  grid-area: title;
  padding: 32px 32px 20px 32px;
}
.database-type-page__content {
  grid-area: content;
  padding-left: 32px;
  overflow: hidden;
}
.database-type-page__sidebar {
  grid-area: sidebar;
  padding-right: 32px;
}
.database-type-page__sidebar p {
  margin: 0 0 16px 0;
}
.database-type-page .tabs-wrap,
.database-type-page .tabs-wrap_content {
  height: 100%;
  overflow: hidden;
}
.database-type-page .tabs-wrap_header {
  align-self: flex-start;
}
.database-type-page .tabs-wrap_content_item.selected {
  display: flex;
  flex-direction: column;
  overflow: hidden;
  height: 100%;
}
.database-type-page .search-input {
  margin-bottom: 16px;
}
.database-type-page__list-container {
  flex: 1;
  overflow: auto;
}
.database-type-page .list-wrap {
  height: auto;
}
.database-type-page__list-delimiter {
  display: flex;
  align-items: center;
  overflow: hidden;
  height: 52px;
  margin: 0 12px;
  font-size: 12px;
  line-height: 16px;
  color: var(--main-color-5);
  font-weight: 600;
}
.database-type-page__list-item {
  display: flex;
  align-items: center;
  overflow: hidden;
}
.database-type-page__list-item:hover {
  cursor: pointer;
}
.database-type-page__logo {
  width: 24px;
  height: 24px;
  margin: 0 12px;
  background-size: contain;
}
.database-type-page__name {
  flex: 1;
}
.database-type-page .icon-arrow {
  margin: 0 16px;
  display: none;
}
.database-type-page .icon-arrow use {
  fill: var(--main-color-5);
}
.database-type-page__list-item:hover .icon-arrow {
  display: initial;
}
.database-type-page__url-input {
  margin-bottom: 16px;
}
.database-type-page__url-controls {
  display: flex;
  justify-content: flex-end;
  overflow: hidden;
}
.attached-database-select-item__logo {
  width: 16px;
  height: 16px;
  background-size: contain;
}
.attached-database-tile__logo {
  width: 24px;
  height: 24px;
  background-size: contain;
}
.attached-database-tile__type {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  color: var(--main-color-5);
}
.attached-database-tile__introspection-status {
  display: flex;
  gap: 4px;
  overflow: hidden;
}
.attached-database-tile__introspection-status-text {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  color: var(--main-color-5);
  font-style: italic;
}
.attached-database-trial-tile {
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: hidden;
  gap: 16px;
  border-radius: 4px;
  background: linear-gradient(90.03deg, #0078A4 12.9%, #0F536C 71.5%);
  padding: 16px;
  color: var(--main-color-0);
}
.attached-database-trial-tile__content {
  text-align: center;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.attached-database-trial-tile__countdown {
  font-weight: 600;
}
.sql-cell-actions {
  display: none;
  align-items: center;
  justify-content: end;
  overflow: hidden;
}
.new-cell-toolbar.active .sql-cell-actions {
  display: flex;
}
.sql-cell-actions__label {
  margin-right: 4px;
  margin-top: 1px;
  font-size: 8px;
  line-height: 12px;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: var(--main-color-5);
}
.sql-cell-actions__database {
  display: inline-flex;
  align-items: center;
  font-size: 10px;
  color: var(--main-color-8);
  user-select: none;
  cursor: pointer;
}
.sql-cell-actions__database_empty {
  color: var(--main-color-8);
}
.sql-cell-actions__database .icon-flyout {
  transition: transform 0.15s ease-out;
}
.sql-cell-actions__database.active .icon-flyout {
  transform: rotate(-180deg);
}
.sql-cell-actions__database_active .icon-flyout {
  transform: rotate(-180deg);
}
.sql-cell-actions__database .icon-flyout use,
.sql-cell-actions__database .icon-flyout g {
  fill: var(--main-color-8);
}
.sql-cell-actions__database-icon {
  display: inline-block;
  width: 12px;
  height: 12px;
  margin-right: 4px;
  background-size: cover;
  background-repeat: no-repeat;
}
.sql-cell-actions__database-name {
  display: inline-block;
  overflow: hidden;
  text-overflow: ellipsis;
}
.sql-cell-actions__section {
  display: flex;
  align-items: center;
  margin: 0 12px 0 0;
}
.sql-cell-actions__section.sql-cell-actions__warning {
  margin-right: auto;
}
.sql-cell-actions__navigator {
  cursor: pointer;
}
.sql-cell-actions__navigator use,
.sql-cell-actions__navigator g {
  fill: var(--main-color-6);
}
.sql-cell-actions__navigator:hover use,
.sql-cell-actions__navigator:hover g {
  fill: var(--main-color-8);
}
.sql-cell-actions__variable {
  display: inline-flex;
  align-items: center;
  overflow: hidden;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 10px;
  color: var(--main-color-8);
}
.sql-cell-actions__database-name {
  max-width: 220px;
}
.sql-cell-actions__variable {
  max-width: 220px;
}
.width-l .sql-cell-actions__database-name {
  max-width: 150px;
}
.width-l .sql-cell-actions__variable {
  max-width: 150px;
}
.width-m .sql-cell-actions__database-name,
.width-s .sql-cell-actions__database-name {
  max-width: 130px;
}
.width-m .sql-cell-actions__variable,
.width-s .sql-cell-actions__variable {
  max-width: 130px;
}
.width-m .sql-cell-actions__label,
.width-s .sql-cell-actions__label {
  display: none;
}
.width-s .sql-cell-actions__section {
  display: none;
}
.width-s .sql-cell-actions__section:first-child,
.width-s .sql-cell-actions__section:nth-child(2) {
  display: flex;
}
.width-xs .sql-cell-actions__section,
.width-xs .sql-cell-actions__section:first-child,
.width-xs .sql-cell-actions__section:nth-child(2) {
  display: none;
}
.sql-cell-actions:after {
  content: " ";
  display: inline-block;
  height: 12px;
  margin: 0 8px 0 0;
  border-left: 1px solid var(--main-color-2);
}
.database-item {
  cursor: pointer;
}
.database-item > div {
  display: flex;
  align-items: center;
}
.database-item__icon {
  justify-content: flex-end;
}
.database-item__logo {
  width: 16px;
  height: 16px;
  align-self: center;
  background-size: contain;
  filter: grayscale(1);
}
.database-item__menu {
  justify-content: center;
}
.database-trial-dialog {
  padding: 32px;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}
.database-trial-dialog__title {
  padding-bottom: 20px;
}
.database-trial-dialog__content {
  padding-bottom: 24px;
}
.database-trial-dialog__footer {
  display: flex;
  overflow: hidden;
  gap: 12px;
}
.databases__header,
.databases .database-item {
  display: grid;
  grid-template-columns: 24px 25% 16px auto 32px;
  grid-gap: 8px;
}
.databases__header > div:first-child {
  padding-left: 8px;
  grid-column: 1 / 3;
}
.databases__header > div:first-child + div {
  grid-column: 3 / 5;
}
.databases__title {
  flex: 1 0;
}
.introspection-tree .list-wrap {
  height: auto;
}
.introspection-tree__node {
  height: 40px;
  flex-shrink: 0;
  display: flex;
  gap: 8px;
  align-items: center;
  overflow: hidden;
  cursor: pointer;
  padding: 0 8px;
}
.introspection-tree__node_expanded .icon-arrow {
  transform: rotate(90deg);
}
.introspection-tree__node-icon {
  width: 16px;
  height: 16px;
  background-size: contain;
}
.introspection-tree__node-name {
  flex: 1;
  margin: 0 8px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.introspection-tree__node-info {
  color: var(--main-color-5);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.attached-data-panel {
  height: 100%;
  display: flex;
  flex-direction: column;
}
.attached-data-panel .dl-select {
  max-width: initial;
  margin-bottom: 16px;
}
.attached-data-panel__list {
  flex: 1;
  overflow: auto;
  display: flex;
  flex-direction: column;
  gap: 16px;
  padding-top: 2px;
}
.attached-data-panel__list > div {
  transition: transform 100ms ease-out, box-shadow 100ms ease-out;
  -webkit-transform: translateZ(1px);
}
.attached-data-panel__list > div:hover {
  transform: translateY(-2px);
  -webkit-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
}
.attached-data-select-item {
  display: flex;
  align-items: center;
  overflow: hidden;
  gap: 8px;
  width: 320px;
}
.attached-data-select-item :first-child {
  flex-shrink: 0;
}
.attached-data-select-item__name {
  flex-grow: 1;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.attached-data-select-item__marker {
  color: var(--main-color-5);
}
.attached-data-tile {
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
  min-height: 0;
  border-radius: 4px;
  background-color: var(--main-color-1);
  border: 1px solid var(--border-color);
}
.attached-data-tile:not(.attached-data-tile_expanded) {
  cursor: pointer;
}
.attached-data-tile_expanded {
  border-bottom: none;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.attached-data-tile__header {
  padding: 16px 16px 12px 16px;
  display: flex;
  align-items: center;
  overflow: hidden;
  gap: 12px;
}
.attached-data-tile__header use {
  fill: var(--main-color-5);
}
.attached-data-tile:not(.attached-data-tile_expanded):hover .attached-data-tile__header .icon-arrow use {
  fill: var(--main-color-8);
}
.attached-data-tile_expanded .attached-data-tile__header .icon-arrow:hover use {
  fill: var(--main-color-8);
}
.attached-data-tile_expanded .attached-data-tile__header .icon-arrow {
  cursor: pointer;
  transform: rotate(180deg);
}
.attached-data-tile__header .icon-menu {
  cursor: pointer;
}
.attached-data-tile__header .icon-menu :hover use {
  fill: var(--main-color-8);
}
.attached-data-tile__tools {
  padding: 0 16px 16px 16px;
  display: flex;
  gap: 12px;
}
.attached-data-tile__tools button {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.attached-data-tile__name {
  flex: 1;
  font-size: 14px;
  line-height: 20px;
  font-weight: 600;
  color: var(--main-color-9);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.attached-data-tile__content {
  flex: 1;
  overflow: auto;
  background-color: var(--tile-bg);
  padding: 0 16px;
}
.attached-files-tile__quota {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  color: var(--main-color-5);
}
.attached-files-tile__warning {
  position: relative;
}
.attached-files-tile__path {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  color: var(--main-color-5);
  font-style: italic;
}
.datasource-list {
  margin-bottom: 1em;
}
.datasource-list_item {
  display: grid;
  min-height: 138px;
  padding: 16px;
  border: 1px solid var(--main-color-2);
  border-radius: 2px;
  cursor: pointer;
  -webkit-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  -moz-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  transition: transform 100ms ease-out, box-shadow 100ms ease-out;
}
.datasource-list_item_kind {
  font-style: italic;
}
.datasource-list_item_name {
  font-weight: bold;
  display: flex;
}
.datasource-list_item_name svg use {
  fill: var(--main-color-5);
}
.datasource-list_item_name svg {
  padding-right: 8px;
}
.datasource-list_item_controls {
  text-align: right;
}
.datasource-list_item_description {
  word-break: break-word;
}
.datasource-list_item_menu {
  width: 16px;
  height: 16px;
  display: inline-block;
  align-items: center;
  justify-content: center;
  padding: 8px;
  margin-right: -8px;
  cursor: pointer;
}
.datasource-list_item_menu .icon > use {
  transition: fill 200ms ease-in;
  fill: var(--main-color-5);
}
.datasource-list_item_menu .icon:hover > use {
  fill: var(--main-color-8);
}
.datasource-list_item:not(.renamed):hover {
  transform: translateY(-2px);
  -webkit-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
}
.datasource-list_item.highlighted {
  transform: none;
  animation: highlight 2s ease-out;
}
.datasource-list_item:not(.renamed):active {
  transform: none;
  -webkit-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  -moz-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
}
.datasource-list_item > div {
  padding: 8px 0 8px 0;
}
.datasource-list_item > div:first-child {
  padding: 0 0 8px 0;
  border-bottom: 1px solid var(--main-color-2);
}
.datasource-list_item > div:last-child {
  padding: 0;
}
.datasource-list-grid {
  padding: 8px;
  display: grid;
  grid-gap: 32px;
  grid-auto-flow: dense;
  grid-auto-columns: max-content;
  grid-auto-rows: minmax(100px, auto);
  grid-template-columns: repeat(3, minmax(230px, 1fr));
}
.datasource-list-grid .datasource-list_item {
  grid-template-rows: 40px 1fr 24px;
}
.datasource-list-vertical .datasource-list_item {
  padding: 8px 12px;
  min-height: 0;
  grid-template-columns: 2fr 4fr 1fr;
}
.datasource-list-vertical .datasource-list_item > div {
  padding: 0;
}
.datasource-list-vertical .datasource-list_item > div:first-child {
  padding: 0;
  border-bottom: none;
}
.datasource-list-vertical p {
  white-space: normal;
}
.datasource-disclaimer {
  color: var(--main-color-4);
  white-space: normal;
  padding: 1em 0;
}
.datasource-controls {
  text-align: right;
  display: flex;
  justify-content: flex-end;
}
.datasource-controls .dl-button {
  width: auto;
}
.datasource-controls > .list-button {
  width: 230px;
}
.datasource-controls_add_datasource svg use {
  fill: var(--primary-bg);
}
.datasource-restart-disclaimer {
  background-color: var(--attention-color-1);
  white-space: normal;
  padding: 14px;
}
.datasource-select-element-create {
  font-weight: bold;
}
.delete-datasource-dialog_bar {
  margin: 12px 0 0 0;
  text-align: right;
}
.delete-datasource-dialog_bar .dl-button {
  width: auto;
}
.delete-datasource-dialog_bar .dl-button:first-child {
  margin-right: 12px;
}
.edit-datasource-dialog_bar {
  display: flex;
  justify-content: space-between;
  margin: 12px 0 0 0;
}
.edit-datasource-dialog_bar .dl-button {
  width: auto;
  margin-left: 2px;
}
.edit-datasource-dialog_bar .dl-button:first-child {
  margin-right: 12px;
}
.edit-datasource-dialog_section {
  padding-bottom: 12px;
}
.edit-datasource-dialog_text {
  height: 515px;
  overflow-y: auto;
}
.edit-datasource-dialog_text_input {
  width: 100%;
}
.edit-datasource-dialog_text_input_invalid {
  background-color: var(--negative-color-1);
}
.edit-datasource-dialog_description_text {
  width: 100%;
  min-height: 120px;
}
.edit-datasource-dialog_entry > div {
  display: grid;
  grid-template-columns: 1fr 1fr 32px;
  padding-bottom: 6px;
}
.edit-datasource-dialog_entry > div > div {
  padding-right: 12px;
}
.explore-datasource_toolbar-action {
  background: #ffffff;
  border: 1px solid var(--main-color-3);
  display: inline-block;
  padding: 5px;
  opacity: 0.9;
}
.explore-datasource_toolbar-action:hover {
  opacity: 1;
}
.explore-datasource_toolbar {
  display: flex;
  flex-flow: row-reverse;
  padding: 0.25em 0;
}
.explore-datasource_run-button {
  width: 150px;
  margin-right: 0.25em;
}
.explore-datasource_transfer-button {
  width: 250px;
  background-color: transparent;
  border: 1px solid #000;
  margin-right: 1em;
}
.explore-datasource_transfer-button > .list-button_main {
  color: #000;
}
.explore-datasource_input {
  width: 100%;
  padding: 0.25em;
  background-color: #fff;
}
.explore-datasource_result {
  display: flex;
  flex-direction: row;
  padding: 0.25em 0;
  overflow: auto;
}
.explore-datasource_result > div {
  padding: 0 0.25em 0 0;
}
.explore-datasource_result table {
  font-size: 12px;
  border-collapse: collapse;
  border: 1px solid var(--main-color-3);
  background-color: #ffffff;
  width: 100%;
  margin-bottom: 0.25em;
}
.explore-datasource_result th {
  padding: 0.25em 0.5em;
  border: 1px solid var(--main-color-3);
  background-color: #f3f3f3;
}
.explore-datasource_result th .icon.asc {
  transform: rotate(-180deg);
}
.explore-datasource_result th > div {
  display: flex;
}
.explore-datasource_result td {
  border: 1px solid var(--main-color-3);
  padding: 0.25em 0.5em;
}
.explore-datasource_database-info {
  background-color: #ffffff;
  border: 1px solid #c5c5c5;
  padding: 0;
}
.explore-datasource_database-info ul {
  padding: 0.25em 0.5em;
}
.explore-datasource_database-info_header {
  background-color: var(--main-color-1);
  padding: 0.25em;
  display: flex;
  flex-flow: row;
  border-bottom: 1px solid var(--main-color-3);
}
.explore-datasource_database-info_header_collapsed {
  border-bottom: none;
}
.explore-datasource_database-info_header > span {
  flex-grow: 1;
  font-weight: bold;
}
.explore-datasource_database-info_header .icon-rotated-180 {
  transform: rotate(180deg);
}
.explore-datasource_database-info_history_row {
  display: flex;
  flex-flow: row;
  padding: 0.25em 0 0.25em 0.5em;
}
.explore-datasource_database-info_history_row_query {
  flex-grow: 1;
}
.explore-datasource_database-info_history_row .icon-unset use,
.explore-datasource_database-info_history_row .icon-unset g {
  fill: var(--main-color-3);
}
.explore-datasource_sql-editor {
  background-color: #ffffff;
}
.explore-datasource_sql-error-install {
  background-color: var(--attention-color-1);
  white-space: normal;
  padding: 14px !important;
}
.explore-datasource_sql-error > pre {
  white-space: pre-wrap;
  max-width: 100%;
  margin: 1em;
}
.explore-datasource_sql-table_sorted_column {
  text-decoration: underline;
}
.explore-datasource_history_menu_container {
  display: flex;
  align-items: center;
}
.explore-datasource_history_menu {
  display: flex;
  justify-content: center;
  cursor: pointer;
  margin-right: 0.5em;
}
.explore-datasource_history_menu .icon > use {
  transition: fill 200ms ease-in;
  fill: var(--main-color-5);
}
.explore-datasource_history_menu .icon:hover > use {
  fill: var(--main-color-8);
}
.dp-activity-monitor {
  min-width: 280px;
  padding: 32px;
}
.dp-activity-monitor_content {
  text-align: center;
  margin-top: 12px;
  margin-bottom: 32px;
}
.dp-activity-monitor_bar {
  text-align: right;
}
.dp-closed-connection_popup .popup-close {
  display: none;
}
.dp-closed-connection_content {
  text-align: center;
  margin-top: 12px;
  margin-bottom: 32px;
}
.dp-closed-connection_bar {
  text-align: center;
}
.code-cell-output {
  transition: opacity 0.3s ease-in-out;
}
.code-cell-output__section {
  overflow-x: auto;
  overflow-y: hidden;
  margin-bottom: -6px;
  padding-bottom: 6px;
}
.code-cell-output .code-cell-output__toolbar {
  display: none;
}
.code-cell-output__repr {
  position: relative;
}
.code-cell-output__action {
  padding: 8px;
  line-height: 0;
  cursor: pointer;
  opacity: .8;
}
.code-cell-output__action:hover {
  opacity: 1;
}
.code-cell-output__action[disabled],
.code-cell-output__action[disabled]:hover {
  opacity: .3;
}
.code-cell-output.disabled {
  opacity: .3;
}
.traceback {
  padding: 8px;
  margin-top: 8px;
  background-color: rgba(var(--negative-color-1-rgb), 0.24);;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
  min-width: calc(100% - 16px);
  width: max-content;
}
.traceback_link {
  color: var(--traceback-link);
}
.traceback_link:hover {
  text-decoration: underline;
  cursor: pointer;
}
.disabled .traceback_link {
  opacity: 0.8;
}
.output-scroll-button {
  display: block;
  width: 100%;
  cursor: pointer;
  margin: 0 0 10px;
  position: relative;
  text-align: center;
}
.output-scroll-button_text {
  display: inline-block;
  position: relative;
  padding: 0 8px;
  font: 12px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  text-align: center;
  background: var(--primary-bg);
  z-index: 1 !important;
}
.output-scroll-button_line {
  border-top: 1px solid var(--border-color);
  position: absolute;
  left: 0;
  right: 0;
  top: 7px;
}
.output-scroll_content {
  white-space: pre !important;
  height: auto !important;
  width: auto !important;
  outline: none;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.output-scroll_drag {
  position: relative;
  padding: 8px 0;
  height: 1px;
  cursor: pointer;
}
.output-scroll_drag::after {
  display: block;
  content: ' ';
  position: absolute;
  left: 0;
  right: 0;
  top: 8px;
  border-top: 1px solid transparent;
}
.output-scroll_drag:hover .output-scroll_drag::after {
  border-color: var(--border-color);
}
.control-multi-settings__select-item {
  display: flex;
  align-items: center;
}
.control-multi-settings__select-item .icon:first-child {
  margin-right: 8px;
}
.control-multi-settings__select-item .icon:first-child use,
.control-multi-settings__select-item .icon:first-child g {
  fill: var(--main-color-5);
}
.control-settings {
  width: 300px;
}
.control-settings__header {
  padding: 8px 16px;
}
.control-settings .input {
  width: 100%;
}
.control-settings .checkbox {
  margin-top: 16px;
}
.control-settings__section {
  padding: 8px 16px 16px;
  border-top: 1px solid var(--border-color);
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.control-settings__section_noborder {
  border: none;
}
.control-settings__bar {
  padding-top: 16px;
  flex-direction: row;
  justify-content: flex-end;
  gap: initial;
}
.control-settings__bar .button:last-child {
  margin-left: 16px;
}
.control-settings .tags-input {
  height: 96px;
}
.dl-removableControl {
  display: flex;
}
.dl-removableControl_removeButton {
  font-size: 20px;
  padding: 2px 10px;
  cursor: pointer;
}
.dl-controls_title {
  font-weight: bold;
}
.dl-controls_addControl {
  cursor: pointer;
  display: inline-block;
  border: 1px solid var(--action-color-2);
  background-color: var(--action-color-2);
  color: var(--primary-bg);
  font-size: 13px;
  border-radius: 2px;
  padding: 4px 5px;
  margin: 5px 0 0 0;
  border-radius: 1px;
}
.dl-controls_addControlItem {
  cursor: pointer;
  padding: 2px 5px;
}
.dl-controls_addControlItem:hover {
  background-color: var(--main-color-3);
}
input[type=text].dl-controls_variableName.invalid {
  color: var(--negative-color-2);
}
input[type=text].dl-controls_variableName.highlighted {
  background-color: var(--negative-color-1);
  color: var(--main-color-9);
}
.cell-control {
  box-sizing: border-box;
  max-width: 333px;
  padding: 8px 12px 12px 12px;
}
.cell-control_edit_mode {
  background-color: var(--editor-bg);
}
.cell-control-drop-down .dl-select {
  max-width: initial;
}
.cell-control-drop-down .dl-select_popup {
  z-index: 2;
}
.cell-control-header {
  margin-bottom: 12px;
}
.cell-control-header__popup {
  z-index: 3;
}
.cell-control-header__label-row {
  display: flex;
  align-items: center;
  min-height: 20px;
  margin: 4px 0 8px;
}
.cell-control-header__label {
  flex-grow: 1;
  font-size: 10px;
  line-height: 20px;
  line-height: 12px;
  text-transform: uppercase;
  letter-spacing: 0.75px;
  font-weight: 500;
  overflow: hidden;
  text-overflow: ellipsis;
  color: var(--main-color-5);
}
.cell-control-header__bar {
  display: none;
  flex-grow: 0;
  flex-shrink: 0;
  line-height: 0;
}
.cell-control-header__bar .icon {
  padding: 4px;
}
.cell-control-header__bar .icon use,
.cell-control-header__bar .icon g {
  fill: var(--main-color-5);
}
.cell-control-header__bar .icon:hover use,
.cell-control-header_opened .cell-control-header__bar .icon.icon-settings use,
.cell-control-header__bar .icon:hover g,
.cell-control-header_opened .cell-control-header__bar .icon.icon-settings g {
  fill: var(--main-color-9);
}
.cell-control-header__variable {
  display: flex;
  overflow: hidden;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.cell-control-header__variable span {
  display: inline-block;
  max-width: 100%;
  padding: 4px;
  overflow: hidden;
  text-overflow: ellipsis;
  background-color: var(--main-color-2);
}
.cell-control-header_opened .cell-control-header__bar,
.cell-control:hover .cell-control-header__bar {
  display: block;
}
.cell-control-input__value {
  width: 100%;
}
.cell-control-slider__content {
  display: flex;
}
.cell-control-slider__slider {
  flex-grow: 1;
  padding: 6px 4px 0;
  margin-right: 12px;
}
.cell-control-slider__slider-line {
  position: relative;
  width: 100%;
  height: 4px;
  transform: translateY(-2px);
  background: var(--main-color-2);
  box-shadow: inset 0px 1px 2px rgba(0, 0, 0, 0.15);
  border-radius: 2px;
}
.cell-control-slider__footer {
  display: flex;
  justify-content: space-between;
  font-size: 10px;
  line-height: 20px;
  line-height: 12px;
  color: var(--main-color-6);
}
.cell-control-slider__value {
  flex-shrink: 0;
  width: 44px;
}
.cell-control-slider__roller {
  position: relative;
  display: block;
  box-sizing: border-box;
  width: 12px;
  height: 12px;
  transform: translate3d(-6px, -4px, 0);
  background: var(--main-color-1);
  box-shadow: 0px 1px 1px rgba(0, 0, 0, 0.15);
  border: 1px solid var(--main-color-5);
  border-radius: 6px;
}
.cell-control-slider__roller:hover {
  cursor: ew-resize;
}
.cell-control-slider__roller.active {
  background: var(--action-color);
  border-color: var(--action-color);
}
.cell-control-slider__steps {
  position: relative;
  height: 4px;
  margin: 4px 0 2px;
}
.cell-control-slider__step {
  position: absolute;
  display: inline-block;
  width: 3px;
  height: 3px;
  transform: translate(-1.5px, 0);
  border-radius: 3px;
  background-color: var(--main-color-3);
}
.cell-control-slider__step:first-child {
  transform: translate(0, 0);
}
.cell-control-slider__step:last-child {
  transform: translate(-3px, 0);
}
.static-editor {
  margin: 0;
  padding: 24px 16px;
  overflow: auto;
  background-color: var(--editor-bg);
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.markdown-navigation {
  height: 100%;
  min-height: 200px;
  box-sizing: border-box;
  padding-top: 16px;
  background-color: var(--primary-bg);
  outline: none;
}
.markdown-navigation_popup {
  width: 300px;
  height: 400px;
}
.markdown-navigation_items {
  height: 100%;
  overflow: auto;
}
.markdown-navigation_item {
  padding: 8px 0;
  background-repeat: no-repeat;
  background-position: center;
  border-left: 2px solid transparent;
}
.markdown-navigation_item:hover {
  cursor: pointer;
  text-decoration: underline;
}
.markdown-navigation_item.selected {
  font-weight: bold;
}
.markdown-navigation_item[data-nesting="1"] {
  padding-left: 16px;
}
.markdown-navigation_item[data-nesting="2"] {
  padding-left: 32px;
}
.markdown-navigation_item[data-nesting="3"] {
  padding-left: 48px;
}
.markdown-navigation_item[data-nesting="4"] {
  padding-left: 64px;
}
.markdown-navigation_item[data-nesting="5"] {
  padding-left: 80px;
}
.overlay {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  background: var(--primary-bg);
  z-index: 2;
  font-size: 12px;
}
.overlay_content {
  position: absolute;
  left: 50%;
  top: 50%;
  margin-left: 6px;
  transform: translate(-50%, -50%);
}
.overlay_text {
  color: var(--main-color-7);
  margin-left: 12px;
}
.overlay_text,
.overlay .spinner {
  vertical-align: middle;
}
.overlay .overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
}
.spinner {
  display: inline-block;
  box-sizing: border-box;
  width: 24px;
  height: 24px;
  border: 3px solid var(--main-color-5);
  border-right-color: transparent;
  border-bottom-color: transparent;
  border-left-color: transparent;
  border-radius: 50%;
  z-index: 2;
  -webkit-transform: translzateZ(0);
  -moz-transform: translzateZ(0);
  -ms-transform: translzateZ(0);
  -o-transform: translzateZ(0);
  transform: translzateZ(0);
  -webkit-animation: spinner-rotate 1s ease-in-out infinite;
  -moz-animation: spinner-rotate 1s ease-in-out infinite;
  -o-animation: spinner-rotate 1s ease-in-out infinite;
  animation: spinner-rotate 1s ease-in-out infinite;
  -webkit-transition: border-color 0.15s ease-out;
  -moz-transition: border-color 0.15s ease-out;
  -o-transition: border-color 0.15s ease-out;
  transition: border-color 0.15s ease-out;
  /* spinner ellipses */
}
.spinner-centred.spinner {
  position: absolute;
  top: 50%;
  left: 50%;
  margin-top: -12px;
  margin-left: -12px;
}
.spinner-relative-size.spinner {
  width: 100%;
  height: 100%;
}
.spinner-ellipses.spinner {
  height: auto;
  border: none;
  border-radius: 0;
  vertical-align: middle;
  overflow: hidden;
  z-index: 2;
  -webkit-transform: none;
  -moz-transform: none;
  -ms-transform: none;
  -o-transform: none;
  transform: none;
  -webkit-animation: none;
  -moz-animation: none;
  -o-animation: none;
  animation: none;
  -webkit-transition: none;
  -moz-transition: none;
  -o-transition: none;
  transition: none;
}
.spinner-ellipses.spinner::after {
  display: inline-block;
  box-sizing: border-box;
  border: none;
  border-radius: 0;
  content: '...';
  z-index: 2;
  font-size: 22px;
  color: var(--main-color-7);
  -webkit-animation: spinner-left-shift 1.5s infinite step-end;
  -moz-animation: spinner-left-shift 1.5s infinite step-end;
  -o-animation: spinner-left-shift 1.5s infinite step-end;
  animation: spinner-left-shift 1.5s infinite step-end;
}
@keyframes spinner-rotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes spinner-left-shift {
  0% {
    transform: translateX(-12px);
  }
  33% {
    transform: translateX(-6px);
  }
  66% {
    transform: translateX(0);
  }
}
.stub {
  display: flex;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  align-items: center;
  justify-content: center;
  align-content: center;
  text-align: center;
  white-space: normal;
  user-select: none;
}
.stub_content {
  max-width: 90%;
  color: var(--main-color-8);
  font-size: 14px;
}
.md-output {
  min-height: 16px;
  white-space: initial;
  overflow-x: auto;
  overflow-y: hidden;
}
.md-output_lazy {
  padding: 35px;
  visibility: hidden;
  white-space: pre-line;
}
.md-output ul,
.md-output ol {
  padding-left: 28px;
}
.md-output ul {
  list-style: disc;
}
.md-output ol {
  list-style: decimal;
}
span.mjx-chtml[tabindex]:focus,
body :focus span.mjx-chtml[tabindex] {
  display: inline-block;
}
.visualization-control {
  display: grid;
  grid-template-columns: 216px auto;
  min-height: 425px;
}
.visualization-control__empty-item {
  color: var(--main-color-5);
}
.visualization-control__input-row {
  margin-top: 16px;
}
.visualization-control__table-info {
  margin-top: 20px;
  white-space: normal;
}
.visualization-control__table-info .label__header {
  color: var(--main-color-5);
  font-size: 10px;
  line-height: 12px;
}
.visualization-control__actions {
  margin-top: 10px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  white-space: pre-wrap;
}
.visualization-control__actions .button {
  line-height: 12px;
  font-size: 10px;
}
.visualization-control__actions .label__header {
  color: var(--main-color-5);
  font-size: 10px;
  line-height: 12px;
}
.visualization-control__spinner {
  opacity: 85%;
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
}
.visualization-control__spinner .dl-loader_wrap {
  position: relative;
  top: 50%;
}
.visualization-control__output {
  position: relative;
  min-width: 200px;
  padding: 24px 12px;
}
.visualization-control__output .error-message {
  position: relative;
  top: 40%;
  text-align: center;
}
.visualization-control__output > div {
  width: 100%;
}
.table-insight-tabs .tab-header {
  float: left;
}
.table-insight-tabs .tabs_content {
  overflow: visible;
}
.table_vis-aes-label {
  padding: 0 5px 0 0px;
}
.table_vis-var-suggest {
  flow: left;
  min-width: 100px;
  max-width: 200px;
  margin-right: 15px;
}
.table_vis-axis-configurator {
  padding-bottom: 8px;
}
.table_vis-kind {
  flow: left;
}
.table_vis-plot-container {
  position: relative;
  min-width: 500px;
  min-height: 300px;
  padding-top: 8px;
  padding-bottom: 12px;
}
.table_vis-options-line {
  padding-bottom: 4px;
}
.table_vis-actions {
  float: right;
}
.plot_kind_group {
  display: inline-block;
  overflow: hidden;
  padding-bottom: 8px;
}
.plot_kind_group-item {
  display: inline-block;
  float: left;
}
.plot_kind_group input[type=radio] {
  display: none;
}
.plot_kind_group label {
  color: var(--main-color-5);
  line-height: 16px;
  font-size: 12px;
  display: inline-block;
  cursor: pointer;
  padding: 0px 16px;
  border-right: none;
  user-select: none;
}
.plot_kind_group input[type=radio]:checked + label {
  border-bottom: 3px solid;
  border-bottom-color: var(--action-color);
  color: var(--main-color-9);
}
.plot_kind_group input[type=radio]:disabled + label {
  background: #efefef;
  color: #666;
}
.collapsible-options {
  padding-bottom: 8px;
}
.collapsible-options-button {
  display: block;
  width: 100%;
  cursor: pointer;
  margin: 0 0 8px;
  position: relative;
  text-align: left;
}
.collapsible-options-button_text {
  display: inline-block;
  position: relative;
  padding: 0 4px;
  text-align: left;
  z-index: 1;
}
.collapsible-options-button_line {
  border-top: 1px solid var(--border-color);
}
.plot_mapping_group {
  display: inline-block;
  overflow: hidden;
  border: 1px solid var(--main-color-3);
}
.plot_mapping_group label {
  display: inline-block;
  width: 15%;
}
.plot_mapping_group select {
  flow: left;
  min-width: 100px;
  max-width: 200px;
  border: 1px solid var(--main-color-3);
}
.plot_titles_group {
  display: inline-block;
  overflow: hidden;
  min-width: 350px;
  min-height: 105px;
  border: 1px solid var(--main-color-3);
  vertical-align: top;
}
.plot_titles_group label {
  display: inline-block;
  width: 30%;
}
.plot_titles_group input {
  display: inline-block;
  width: 65%;
  color: black;
  background: var(--primary-bg);
  color: var(--primary-fg);
  border: 1px solid var(--main-color-3);
}
.plot_stat_group {
  display: inline-block;
  overflow: hidden;
  min-width: 200px;
  min-height: 105px;
  border: 1px solid var(--main-color-3);
  vertical-align: top;
}
.plot_stat_group input {
  display: inline-block;
  min-width: 20px;
  max-width: 50px;
  border: 1px solid var(--main-color-3);
  color: black;
  background: var(--primary-bg);
  color: var(--primary-fg);
}
.plot_stat_group label {
  display: inline-block;
  width: 30%;
}
table {
  font-size: 12px;
  border-collapse: collapse;
  border: 1px solid var(--border-color);
}
th {
  padding: 0.5em 0.25em;
  border: 1px solid var(--border-color);
  background-color: var(--main-color-1);
  font-weight: normal;
}
.dataframe thead th {
  text-align: left !important;
}
td {
  border: 1px solid var(--border-color);
  padding: 0.25em;
  min-width: 32px;
}
.table_cell {
  position: relative;
  box-sizing: border-box;
  padding: 0 4px;
  line-height: 26px;
  min-height: 27px;
  border-bottom: 1px solid var(--border-color);
  border-right: 1px solid var(--border-color);
}
.table_cell-content {
  max-height: 100%;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.table_cell-selected,
.table_cell.selected {
  background: Highlight;
}
.table_column {
  position: relative;
  display: inline-block;
  vertical-align: top;
}
.table_column-name {
  position: relative;
  border-right: 1px solid var(--border-color);
  display: inline-block;
  box-sizing: border-box;
  height: 100%;
  font-weight: bold;
  transition: color 0.15s ease-out;
  cursor: default;
}
.table_column-name.selected {
  background: Highlight;
}
.table_column-name-value {
  display: inline-block;
  box-sizing: border-box;
  width: 100%;
  vertical-align: middle;
  padding: 0 4px;
  line-height: 27px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.table_row {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.table_row-name {
  box-sizing: border-box;
  border-bottom: 1px solid var(--border-color);
  padding: 0 4px;
  font-weight: bold;
  cursor: default;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.table_row-name.selected {
  background: Highlight;
}
.table_splitter {
  width: 8px;
  position: absolute;
  top: 0;
  bottom: 0;
  right: -4px;
  margin-left: -4px;
  cursor: col-resize;
  z-index: 1;
}
.table_splitter-horizontal {
  width: auto;
  height: 8px;
  top: auto;
  bottom: -4px;
  left: 0;
  right: 0;
  cursor: row-resize;
}
.table_selecting .table_splitter {
  display: none;
}
.splitter-splitter_container_vertical {
  height: 100%;
  width: 100%;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  user-select: none;
}
.splitter-row {
  border: 1px solid var(--main-color-4);
  overflow: hidden;
  flex-grow: 1;
  -webkit-flex-grow: 1;
  width: 100%;
  -webkit-box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
  position: relative;
}
.splitter-vertical_splitter {
  width: 100%;
  height: 10px;
  cursor: row-resize;
  border: 0;
}
.splitter-dp_panel_vertical {
  margin-top: 0;
  margin-bottom: 0;
  padding: 0;
  min-width: 100%;
}
.splitter-splitter_container_horizontal {
  height: 100%;
  width: 100%;
  display: flex;
  display: -webkit-flex;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  user-select: none;
}
.splitter-column {
  box-sizing: border-box;
  overflow: hidden;
  flex-grow: 1;
  -webkit-flex-grow: 1;
  flex-shrink: 1;
  -webkit-flex-shrink: 1;
  height: 100%;
  position: relative;
}
.splitter-horizontal_splitter {
  height: 100%;
  width: 10px;
  margin-left: -5px;
  cursor: col-resize;
  border: 0;
  z-index: 1;
}
.splitter-dp_panel_horizontal {
  margin-left: -5px;
  padding: 0;
  min-height: 100%;
}
.splitter-dp_panel_horizontal:first-child {
  margin-left: 0;
  border-right: 1px solid var(--main-color-2);
}
.table {
  position: relative;
  display: grid;
  grid-template-columns: auto 1fr;
  grid-template-rows: auto auto 1fr;
  font: 12px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  outline: none;
  border: 1px solid var(--border-color);
  --table-shadow-color: rgba(0, 0, 0, 0.1);
  --shadow-top: inset 0 16px 12px -8px var(--table-shadow-color);
  --shadow-bottom: inset 0 -16px 12px -8px var(--table-shadow-color);
  --shadow-left: inset 16px 0 12px -8px var(--table-shadow-color);
  --shadow-right: inset -16px 0 12px -8px var(--table-shadow-color);
}
.table_no-row-names {
  grid-template-rows: auto 0 1fr;
}
.table_no-row-names .table_stub-row {
  border-bottom: none;
}
.table_grid {
  display: grid;
  grid-template-rows: 27px;
}
.table_rows-container {
  background: var(--main-color-1);
}
.table_columns-container {
  background: var(--main-color-1);
}
.table_row-names-container {
  flex-shrink: 0;
  line-height: 0;
}
.table_column-names-container {
  flex-shrink: 0;
  line-height: 0;
}
.table_rows {
  width: 100%;
}
.table_data-container {
  overflow: auto;
  box-sizing: border-box;
  position: relative;
  flex-grow: 1;
}
.table_data {
  line-height: 0;
  width: fit-content;
  width: -moz-fit-content;
  overflow: hidden;
  white-space: nowrap;
}
.table_columns {
  line-height: 0;
  width: fit-content;
  width: -moz-fit-content;
  height: 100%;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.table-disabled .table_scroll-root {
  overflow: hidden !important;
}
.table-disabled .table_indicator {
  opacity: 0;
}
.table_scroll-root {
  position: relative;
}
.table_scroll-root.scrolling .table_splitter {
  display: none;
}
.table_scrolled {
  position: absolute;
  z-index: 1;
  transform: translateZ(0);
}
.table_separator {
  position: absolute;
  top: 0;
  bottom: 0;
  right: -5px;
  padding: 0 5px;
  cursor: col-resize;
  z-index: 1;
}
.table_separator-line {
  display: inline-block;
  height: 100%;
  width: 1px;
  background: var(--border-color);
}
.table_column-row .table_cell {
  display: inline-block;
}
.table_stub-row {
  border-bottom: 1px solid var(--border-color);
}
.table > .table_splitter-horizontal {
  bottom: -10px;
}
.table-wrapper__footer {
  font-size: 10px;
  line-height: 20px;
  color: var(--main-color-7);
}
.dropdown_popup.popup {
  max-height: 320px;
  overflow: auto;
}
.dropdown_item {
  display: block;
  padding: 0 10px;
  height: 32px;
  line-height: 32px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  cursor: pointer;
  user-select: none;
}
.dropdown_item:hover,
.dropdown_item:focus,
.dropdown_item.focused,
.dropdown_item.selected {
  background: var(--main-color-1);
}
.dropdown_item.selected {
  font-weight: normal;
}
.dropdown_item-disabled {
  color: var(--main-color-4);
}
.suggest {
  position: relative;
  display: inline-block;
}
.suggest_input {
  text-overflow: ellipsis;
  padding-right: 24px !important;
  width: 100%;
}
.suggest_popup {
  position: absolute;
  min-width: 100%;
  z-index: 2;
}
.suggest_close,
.suggest_arrow {
  position: absolute !important;
  right: 8px;
}
.suggest_close {
  top: 10px !important;
}
.suggest_arrow {
  top: 8px !important;
  transform: rotate(0deg);
  transition: transform 0.15s ease-out, opacity 0.15s ease-out;
  cursor: pointer;
}
.suggest-opened .suggest_arrow {
  transform: rotate(180deg);
}
.select {
  display: inline-block;
  position: relative;
  line-height: 0;
}
.select[disabled] {
  opacity: 0.4;
}
.select_popup {
  position: absolute;
  min-width: 100%;
  z-index: 1;
}
.select_items {
  position: absolute;
  min-width: 120px;
  z-index: 1;
}
.select_button {
  box-sizing: border-box;
  position: relative;
  display: inline-block;
  width: 100%;
  min-width: 70px;
  min-height: 27px;
  padding: 6px 16px 6px 0;
  font-size: 12px;
  line-height: 1.25;
  overflow: hidden;
  text-overflow: ellipsis;
  vertical-align: middle;
}
.select.dropdown-opened .select_toggler {
  transform: rotate(-180deg);
}
.select-empty .select-value {
  color: var(--main-color-7);
}
.select-bordered {
  border: 1px solid var(--border-color);
  box-sizing: border-box;
}
.select-bordered.error {
  border-color: var(--negative-color-2);
}
.select-bordered .select_button {
  padding: 6px 28px 6px 8px;
  background: var(--primary-bg);
}
.select_toggler.icon {
  position: absolute;
  right: 6px;
  transition: transform 0.15s ease-out;
}
.select:hover {
  cursor: pointer;
}
.ipywidget {
  width: 100%;
  border: none;
}
.plot-axis-control__popup {
  z-index: 1;
}
.plot-axis-control_settings-opened .icon-settings use,
.plot-axis-control_settings-opened .icon-settings g {
  fill: var(--main-color-9);
}
.plot-axis-control__color-item::before {
  display: inline-block;
  width: 16px;
  height: 16px;
  margin-right: 8px;
  vertical-align: middle;
  background-color: var(--main-color-5);
  content: " ";
}
.plot-axis-control__empty-item {
  color: var(--main-color-5);
}
.plot-cell-control {
  padding: 24px 16px;
}
.plot-cell-control__section {
  margin-top: 16px;
}
.plot-cell-control__tabs-bar .icon {
  padding: 4px;
  cursor: pointer;
}
.plot-cell-control__tabs-bar .icon use,
.plot-cell-control__tabs-bar .icon g {
  fill: var(--main-color-6);
}
.plot-cell-control__tabs-bar .icon:hover use,
.plot-cell-control__tabs-bar .icon:hover g {
  fill: var(--main-color-9);
}
.plot-cell-control__popup {
  z-index: 1;
}
.plot-cell-control_settings-opened .icon-settings use,
.plot-cell-control_settings-opened .icon-settings g {
  fill: var(--main-color-9);
}
.plot-node-settings__row {
  margin-top: 8px;
}
.plot-node-settings__row_double {
  display: grid;
  grid-template-columns: calc(50% - 16px / 2) calc(50% - 16px / 2);
  grid-column-gap: 16px;
}
.plot-cell-content {
  display: grid;
  grid-template-columns: minmax(120px, 328px) auto;
  min-height: 425px;
}
.plot-cell-content_collapsed {
  grid-template-columns: 0 auto;
}
.plot-cell-content_collapsed .plot-cell-content__input {
  display: none;
}
.plot-cell-content_collapsed .plot-cell-content__toggler {
  left: 84px;
  right: initial;
  background: var(--editor-bg);
  transform: rotate(0deg);
}
.plot-cell-content:hover .plot-cell-content__toggler {
  display: block;
}
.plot-cell-content__toggler {
  display: none;
  padding: 2px;
  position: absolute;
  right: 16px;
  top: 4px;
  border-radius: 8px;
  cursor: pointer;
  background: var(--primary-bg);
  transform: rotate(180deg);
}
.plot-cell-content__input-container {
  position: relative;
  background: var(--editor-bg);
}
.plot-cell-content__output {
  display: flex;
  min-width: 200px;
  padding: 24px 12px;
  align-items: center;
  justify-content: center;
  overflow: auto;
}
.plot-cell-content__output > div {
  width: 100%;
}
.report-cell {
  box-sizing: border-box;
  padding: 0 40px;
  margin: 16px 0;
}
.report-cell_has-toolbar:hover > div:first-child {
  box-shadow: -1px 0px 0px 0px var(--main-color-2);
}
.report-cell_has-toolbar:hover .code-cell-output__toolbar {
  display: block;
}
.report-cell_has-toolbar .code-cell-output__toolbar {
  display: none;
  position: absolute;
  left: -48px;
  bottom: -8px;
}
.report-cell-content__output {
  font-size: 14px;
}
.report-cell-content__output .code-cell-output {
  padding: 16px;
}
.report-error-message {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 0;
  transition: height 0.15s ease-out;
  overflow: hidden;
  background-color: var(--negative-color-1);
  color: var(--negative-color-3);
}
.report-error-message_shown {
  height: 36px;
}
.report-progress-button__progress {
  visibility: hidden;
  margin-top: 4px;
  text-align: center;
  color: var(--main-color-5);
}
.report-progress-button_inprogress .report-progress-button__progress {
  visibility: initial;
}
.report-notebook {
  width: 100%;
  height: 100%;
  overflow: auto;
}
.report-notebook__content {
  box-sizing: border-box;
  max-width: 1248px;
  margin: 0 auto;
}
.report-notebook__notebook {
  margin: 0 auto;
  padding: 32px 0;
  max-width: 760px;
  min-width: 140px;
}
.report-notebook__notebook-wrapper {
  padding: 0 244px;
}
.report-notebook__aside {
  position: absolute;
  top: 0;
  width: 244px;
  height: 100%;
  box-sizing: border-box;
  padding: 48px 12px 0 52px;
  display: grid;
  grid-template-rows: auto 1fr;
  grid-template-columns: 100%;
}
.report-notebook__aside .progress-button {
  width: 100%;
}
.report-notebook__toc {
  margin-top: 8px;
  min-height: 0;
}
.onboarding-popup {
  border-radius: 4px;
  z-index: 1099;
}
.onboarding-popup .icon-close {
  position: absolute;
  top: 16px;
  right: 16px;
  opacity: 0.6;
}
.onboarding-popup .icon-close:hover {
  opacity: 1;
  cursor: pointer;
}
.onboarding-tip {
  box-sizing: border-box;
  width: 292px;
  padding: 16px;
}
.onboarding-tip_title {
  margin: 0 0 8px;
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
}
.onboarding-tip_text {
  color: var(--main-color-8);
}
.onboarding-tip_bar {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  margin-top: 16px;
}
.onboarding-tip_bar .button.type--primary {
  width: auto;
  min-width: 0;
  margin: 0 0 0 16px;
}
.onboarding-tip_step {
  color: var(--main-color-5);
}
.onboarding-tip_toggle {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 16px;
  padding: 8px 12px;
  border-radius: 2px;
  background-color: var(--main-color-1);
}
.terminal {
  height: 100%;
}
.terminal .xterm {
  padding: 8px;
}
.terminal-panel {
  width: 100%;
  height: 100%;
  overflow: hidden;
}
.admin-panel-page {
  height: 100%;
}
.admin-panel-page_main {
  height: calc(100% - 48px);
}
.admin-panel {
  display: grid;
  grid-template-columns: 244px 1fr;
  grid-template-areas: "aside main";
  width: 100%;
  height: 100%;
  max-height: 100%;
  overflow: hidden;
  font-size: 14px;
}
.admin-panel_aside {
  padding: 20px 0 0 48px;
  grid-area: aside;
}
.admin-panel_main {
  grid-area: main;
  overflow: auto;
  padding: 20px 64px 20px 48px;
  display: grid;
}
.computations-list_main {
  display: grid;
}
.computations-list_entries {
  width: 100%;
  overflow-x: auto;
}
.computations-list_header,
.computations-list_row {
  display: grid;
  width: 100%;
  align-items: center;
  border-bottom: solid 1px var(--border-color);
  grid-template-columns: 4% 10% auto 15% 10% 10% 10% 10% 10%;
  grid-column-gap: 8px;
  height: 48px;
}
.computations-list_header {
  font-weight: bold;
}
.computations-list_list-content {
  min-height: 49px;
  flex: 1;
}
.computations-list_row_background-computation {
  text-align: center;
}
.computations-list_row_notebook {
  display: grid;
  grid-template-columns: auto 1fr;
  column-gap: 8px;
  align-items: center;
  overflow: hidden;
}
.computations-list_row_notebook-name {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.computations-list_row_notebook-id {
  margin-top: 5px;
  font-size: smaller;
}
.admin-computations-tab_main {
  display: grid;
  grid-template-rows: auto auto 1fr;
}
.admin-computations-tab_header {
  text-align: center;
}
.admin-computations-tab_number {
  display: grid;
  text-align: center;
  grid-template-columns: max-content max-content;
  grid-column-gap: 16px;
  justify-content: center;
  align-items: center;
}
.admin-gift-code-generator {
  display: grid;
  grid-row-gap: 16px;
}
.admin-gift-code-generator_generate-form {
  display: grid;
  grid-row-gap: 16px;
}
.admin-gift-code-generator_generate-form-inputs {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-row-gap: 8px;
  grid-column-gap: 32px;
}
.admin-gift-code-generator_generate-form-inputs .dl-select,
.admin-gift-code-generator_generate-form-inputs input {
  margin-top: 8px;
}
.admin-gift-code-generator_gift-codes-list {
  display: grid;
  grid-row-gap: 8px;
}
.admin-gift-code-generator_storage-duration-inputs {
  display: flex;
  gap: 16px;
}
.admin-gift-code-search {
  display: grid;
  grid-row-gap: 16px;
}
.admin-gift-code-search_search-form-inputs {
  display: grid;
  grid-row-gap: 8px;
}
.admin-gift-code-search_search-form-inputs .dl-select,
.admin-gift-code-search_search-form-inputs .id-input {
  margin-top: 8px;
}
.admin-gift-code-search_search-form-inputs .id-input input {
  max-width: 310px;
  width: 100%;
}
.admin-gift-code-search_search-form-actions {
  margin-top: 16px;
}
.admin-gift-code-search_gift-codes-list {
  display: grid;
  grid-row-gap: 8px;
}
.admin-gift-code-tab {
  display: grid;
  grid-row-gap: 16px;
  grid-template-rows: auto 1fr;
}
.admin-gift-code-tab_header {
  text-align: center;
}
.admin-gift-code-tab_not-supported-message {
  text-align: center;
}
.admin-gift-code-tab_main {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.admin-gift-code-tab_section-header {
  text-align: center;
}
.admin-gift-code-view_short-info {
  cursor: pointer;
  display: grid;
  grid-template-columns: max-content 250px auto auto auto;
  grid-column-gap: 8px;
  width: max-content;
  align-items: center;
}
.admin-gift-code-view_short-info .icon-flyout {
  transition: transform 0.15s ease-out;
}
.admin-gift-code-view_short-info .icon-flyout.opened {
  transform: rotate(-180deg);
}
.admin-gift-code-view_short-info.redeemed {
  text-decoration: line-through;
  color: var(--main-color-4);
}
.admin-gift-code-view_detailed-info {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-row-gap: 8px;
  grid-column-gap: 8px;
  width: max-content;
  margin-left: 16px;
  padding-left: 8px;
  padding-right: 8px;
  background-color: var(--main-color-2);
  transition-property: max-height, margin, padding;
  transition-duration: .30s;
  transition-timing-function: ease-out;
  max-height: 0;
  overflow: hidden;
}
.admin-gift-code-view_detailed-info.opened {
  margin-top: 8px;
  margin-bottom: 8px;
  padding-top: 8px;
  padding-bottom: 8px;
  max-height: 200px;
}
.admin-license-tab {
  display: grid;
  grid-row-gap: 16px;
  grid-template-rows: auto 1fr;
}
.admin-license-tab_header {
  text-align: center;
}
.admin-license-tab_section-header {
  text-align: center;
}
.admin-license-tab_main {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.admin-license-tab_current-license-content {
  display: grid;
  font-size: 17px;
  grid-row-gap: 8px;
  justify-content: center;
}
.admin-license-tab_current-license-content span {
  width: max-content;
}
.admin-license-tab_add-license-content {
  display: grid;
  grid-row-gap: 16px;
}
.admin-license-tab_add-license-footer {
  display: grid;
  grid-template-columns: 3fr 1fr;
}
.admin-license-tab_add-license-success {
  color: var(--positive-color-3);
}
.admin-license-tab_add-license-error {
  color: var(--negative-color-3);
}
.admin-license-tab_license-list-contents {
  display: grid;
  grid-row-gap: 16px;
}
.admin-license-tab_license-list-entry {
  display: grid;
  grid-template-columns: 1fr auto;
  align-items: center;
}
.admin-license-tab_users-count {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-column-gap: 16px;
  align-items: center;
}
.admin-license-tab_users-count button {
  width: max-content;
}
.admin-user-tab {
  display: grid;
  grid-row-gap: 16px;
  grid-template-rows: auto auto 1fr;
}
.admin-user-tab_header {
  text-align: center;
}
.admin-user-tab_search {
  display: grid;
  grid-row-gap: 16px;
}
.admin-user-tab_search-form {
  display: grid;
  grid-row-gap: 16px;
}
.admin-user-tab_search-form-input {
  display: grid;
  grid-row-gap: 16px;
  grid-column-gap: 8px;
  align-items: center;
}
.admin-user-tab_search-form-input input {
  width: 300px;
}
.admin-user-tab_result .users-table {
  min-width: 100%;
}
.admin-user-tab_result .users-table .user-row:hover {
  cursor: pointer;
  background-color: var(--main-color-3);
}
.delete-alert {
  display: grid;
  justify-content: center;
}
.admin-user-tab_result {
  display: grid;
  overflow-x: auto;
}
.admin-user-tab_result-user {
  display: grid;
}
.admin-user-tab_result .user-view {
  display: grid;
  grid-row-gap: 16px;
  padding: 16px;
  grid-template-rows: auto auto 1fr;
}
.admin-user-tab_result .user-view_header {
  display: grid;
  grid-template-columns: max-content 1fr 1fr 1fr;
  align-items: center;
  margin: 0 16px;
}
.admin-user-tab_result .user-view_header-back {
  margin-right: 16px;
}
.admin-user-tab_result .user-view_header-ids {
  display: grid;
  font-size: 17px;
  text-align: center;
  font-weight: bold;
}
.admin-user-tab_result .user-view_header-ids_name {
  display: flex;
  gap: 8px;
  justify-content: center;
  align-items: center;
}
.admin-user-tab_result .user-view_header-actions {
  justify-self: end;
  display: flex;
}
.admin-user-tab_result .user-view_tabs {
  display: flex;
  justify-content: space-around;
}
.admin-user-tab_result .user-view_tabs-tab {
  width: 100%;
}
.admin-user-tab_result .user-view_tabs-tab button {
  width: 100%;
}
.admin-user-tab_result .user-view_tabs-tab:not(:last-child) {
  border-right: solid 2px var(--border-color);
}
.admin-user-tab_result .user-view_tabs-tab.active {
  background-color: var(--main-color-1);
}
.user-view-computations_main {
  display: grid;
  grid-template-rows: auto 1fr;
}
.user-view-general_main {
  display: grid;
  grid-template-columns: 1fr 1fr;
  height: max-content;
}
.user-view-general_main-fields {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-row-gap: 8px;
  grid-column-gap: 8px;
  align-items: center;
  height: max-content;
}
.user-view-general_main-fields-header {
  grid-column-start: 1;
  grid-column-end: -1;
}
.user-view-general_main-fields .icon {
  margin-right: 0 8px;
}
.user-view-general_main-fields-consents {
  display: grid;
}
.user-view-general_main-fields .allowed {
  color: var(--positive-color-2);
}
.user-view-general_main-fields .non-allowed {
  color: var(--negative-color-2);
}
.user-view-general_main-emails {
  display: grid;
  grid-row-gap: 8px;
  height: max-content;
}
.user-view-general_main-emails .primary-email {
  font-weight: bold;
}
.user-view-general_main-emails .email-line {
  display: flex;
  align-items: center;
  height: 32px;
}
.user-view-general_main-emails .email-verified-info {
  font-size: smaller;
  margin-left: 16px;
}
.user-view-general_main-emails .email-verified-info button {
  margin-left: 16px;
}
.user-view-general_main-role-selector {
  display: flex;
}
.user-view-resources_main {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-row-gap: 8px;
  grid-column-gap: 8px;
  height: max-content;
}
.user-view-resources_header {
  grid-column-start: 1;
  grid-column-end: -1;
}
.user-view-resources_license-validity {
  display: flex;
  column-gap: 8px;
}
.user-view-resources_license-validity .icon-warning use,
.user-view-resources_license-validity .icon-warning g {
  fill: var(--negative-color-3);
}
.dl-cell-status {
  display: none;
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 6px;
  background: transparent;
}
.dl-cell-status_anim {
  display: none;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  background-color: var(--positive-color-2);
  -webkit-animation: dl-cell-status_blink 2s infinite;
  -moz-animation: dl-cell-status_blink 2s infinite;
  -o-animation: dl-cell-status_blink 2s infinite;
  animation: dl-cell-status_blink 2s infinite;
}
@-moz-keyframes dl-cell-status_blink {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 0.6;
  }
  100% {
    opacity: 0;
  }
}
@-webkit-keyframes dl-cell-status_blink {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 0.6;
  }
  100% {
    opacity: 0;
  }
}
@keyframes dl-cell-status_blink {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 0.6;
  }
  100% {
    opacity: 0;
  }
}
.dl-cell-status_waiting,
.dl-cell-status_running {
  display: block;
  background-color: var(--positive-color-1);
}
.dl-cell-status_error {
  display: block;
  background-color: var(--negative-color-2);
}
.dl-cell-status_warning {
  display: block;
  background-color: var(--attention-color-2);
}
.dl-cell-status_running .dl-cell-status_anim {
  display: block;
}
.csv-viewer-content {
  height: 100%;
  overflow: hidden;
}
.csv-viewer-header {
  display: flex;
  box-sizing: border-box;
  align-items: center;
  gap: 12px;
  width: 100%;
  padding: 16px 24px;
  overflow: hidden;
  font-size: 24px;
  line-height: 28px;
  font-weight: 700;
  color: var(--main-color-9);
}
.csv-viewer-header__title {
  flex: 1 0;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.csv-viewer-header__info {
  display: flex;
  align-items: center;
  font-size: 12px;
  line-height: 16px;
  font-weight: 400;
  color: var(--main-color-8);
  color: var(--main-color-5);
}
.csv-viewer-panel {
  height: 100%;
  display: grid;
  grid-template-rows: auto 1fr;
}
.default-text-viewer {
  padding: 16px 24px;
}
.md-action {
  display: inline-block;
  padding: 4px;
  line-height: 0;
  cursor: pointer;
}
.md-action use,
.md-action g {
  fill: var(--main-color-6);
}
.md-action:hover use,
.md-action:hover g {
  fill: var(--main-color-9);
}
.md-action[disabled] use,
.md-action:disabled use,
.md-action[disabled]:hover use,
.md-action:disabled:hover use,
.md-action[disabled] g,
.md-action:disabled g,
.md-action[disabled]:hover g,
.md-action:disabled:hover g {
  fill: var(--main-color-3);
}
.md-cell-actions {
  display: flex;
  align-items: center;
}
.ed-shortcut-item {
  display: flex;
  color: var(--main-color-7);
  padding: 16px 12px;
  border-bottom: 1px solid var(--border-color);
}
.ed-shortcut-item:last-child {
  border-bottom: none;
}
.ed-shortcut-item_name {
  flex-grow: 1;
  font-size: 12px;
  line-height: 16px;
  font-weight: 400;
  color: var(--main-color-8);
}
.ed-shortcut-item_key-strokes {
  flex-shrink: 0;
}
.ed-shortcut-item_key-stroke {
  margin: 0 12px;
}
.ed-shortcut-item_key-stroke:first-child {
  margin-left: 0;
}
.ed-shortcut-item_key-stroke:last-child {
  margin-right: 0;
}
.ed-shortcut-item_key {
  padding: 4px 8px;
  margin: 0 2px;
  border-radius: 2px;
  border: 1px solid var(--border-color);
  box-shadow: 0px 2px 0px var(--border-color);
  background: var(--main-color-1);
}
.ed-shortcut-item_key:first-child {
  margin-left: 0;
}
.ed-shortcut-item_key:last-child {
  margin-right: 0;
}
.ed-shortcut-item_highlight {
  background-color: yellow;
}
.ed-shortcuts {
  height: 100%;
  display: grid;
  grid-template-rows: auto 1fr;
  overflow: hidden;
}
.ed-shortcuts_header {
  margin: 16px 0;
}
.ed-shortcuts_header .input {
  width: 100%;
}
.ed-shortcuts_list-container {
  height: 100%;
  overflow: auto;
}
.ed-shortcuts_list {
  min-width: fit-content;
}
.presentation-mode .editor-head {
  z-index: 3;
  top: 0;
  transform: translateY(calc(-100%));
  position: absolute;
  transition: 0.15s ease-out transform;
  left: 0;
  right: 0;
}
.presentation-mode .editor-head:hover {
  transform: none;
}
.presentation-mode .editor-head::after {
  content: " ";
  display: block;
  position: absolute;
}
.presentation-mode .editor-head::after {
  left: 0;
  right: 0;
  height: 20px;
}
.out-top.presentation-mode .editor-head {
  transform: none;
}
.presentation-mode .editor-head:after {
  bottom: 0;
  margin-bottom: -20px;
}
.presentation-mode .editor-head .head_menu-opened {
  transform: none;
}
.editor-head_collaborators {
  flex-grow: 1;
}
.editor-head .icon-fav {
  margin-right: 6px;
  margin-left: -6px;
}
input[type=text].editor-head_document-name {
  color: var(--main-color-1);
  font-size: 14px;
  pointer-events: initial;
  border-bottom: 1px solid transparent;
  border-top: 1px solid transparent;
}
input[type=text].editor-head_document-name:focus {
  border-bottom: 1px solid var(--main-color-1);
}
@media only screen and (max-width: 720px) {
  input[type=text] .editor-head_document-name {
    max-width: unset;
  }
  .editor-head .head_user-name {
    display: none;
  }
}
@media only screen and (max-width: 570px) {
  .editor-head .cr-collaborators {
    display: none;
  }
}
.editor-head .disconnected-block {
  display: inline;
}
.editor-head .disconnected-block .icon {
  margin-left: 12px;
  cursor: default;
}
.editor-head .disconnected-block .icon use,
.editor-head .disconnected-block .icon g {
  fill: var(--negative-color-2);
}
.instance {
  display: flex;
  flex-direction: column;
  height: 100%;
}
.instance_main {
  flex: 1;
}
.instance_main .instance-item {
  display: flex;
  align-items: center;
  padding: 16px 8px;
  box-sizing: border-box;
  border-bottom: 1px solid var(--main-color-2);
}
.instance_main .instance-item__content {
  display: grid;
  grid-template-columns: 240px repeat(4, 120px) auto;
  gap: 12px;
}
.instance_main .instance-item__label {
  font-weight: 600;
}
.instance_info {
  display: flex;
  justify-content: flex-end;
  color: var(--main-color-5);
  margin: 16px 0 0 0;
}
.instance_info a {
  margin-left: 4px;
  color: var(--action-color-2);
}
.instance_info a:hover {
  color: var(--action-color-2);
  text-decoration: none;
  border-bottom-color: transparent;
}
.kernel-info {
  position: relative;
  display: flex;
  cursor: pointer;
}
.kernel-info_label {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.kernel-info_title {
  font-weight: 600;
}
.kernel-info_description {
  color: var(--main-color-8);
}
.kernel-form__footer {
  margin-top: 32px;
  display: flex;
  flex-direction: column;
}
.kernel-form__label {
  display: flex;
  flex-direction: column;
}
.kernel-form__settings_title {
  font-size: 14px;
  font-weight: 600;
  line-height: 20px;
  margin-bottom: 16px;
}
.kernel-form__languages {
  display: flex;
  align-items: center;
  gap: 16px;
}
.kernel-form__languages__item {
  width: 180px;
  height: 92px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 8px;
  box-sizing: border-box;
  background-color: transparent;
  border: 1px solid var(--main-color-3);
}
.kernel-form__languages__item--selected {
  border: 2px solid var(--action-color-3);
}
.kernel-form__languages__item:not(.kernel-form__languages__item--selected):hover {
  cursor: pointer;
  background-color: var(--main-color-2);
}
.kernel-form__image {
  max-width: 100%;
  height: auto;
  object-fit: none;
  border-top-left-radius: 4px;
}
.notebook-form {
  display: flex;
  flex-direction: column;
}
.notebook-form_input {
  margin: 8px 0 28px 0;
}
.notebook-form_input > h3 {
  font-weight: 600;
  margin: 0 0 8px 0;
}
.notebook-form_input > h3 > span {
  font-size: 12px;
  font-weight: normal;
  color: var(--main-color-5);
  margin-left: 8px;
}
.notebook-form_input > input {
  width: 100%;
}
.notebook-form_input > input::placeholder {
  color: var(--main-color-10);
  opacity: 1;
}
.notebook-form_header > h1 {
  margin-top: 38px;
}
.notebook-form_footer {
  display: flex;
  align-items: center;
  border-top: 1px solid var(--main-color-2);
  padding: 16px 0 16px 0;
  margin: 16px 0 0 0;
}
.notebook-form_actions {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  width: 100%;
}
.notebook-form_actions .button + .button {
  margin-left: 20px;
}
.notebook-form .notebook-form_header,
.notebook-form .notebook-form_actions,
.notebook-form .tabs-wrap_header_layout,
.notebook-form .tabs-wrap_content {
  width: 900px;
  margin: 0 auto;
}
.notebook-form .tabs-wrap_content {
  min-height: 325px;
}
.env-manager-dialog {
  display: grid;
  grid-template-rows: 1fr auto;
  box-sizing: border-box;
  padding: 8px;
  height: 100%;
}
.env-manager-dialog__bar {
  text-align: right;
}
.env-manager-dialog__bar .button {
  margin-left: 16px;
}
.env-manager-form__title {
  font-size: 14px;
  line-height: 20px;
  font-weight: 600;
  color: var(--main-color-9);
  margin: 32px 0 16px;
}
.env-manager-form__title:first-child {
  margin-top: 8px;
}
.env-manager-form__section {
  margin: 16px 0;
}
.env-manager-form__environments {
  display: flex;
}
.env-manager-form .dl-select {
  display: inline-block;
  width: fit-content;
  min-width: 180px;
  margin-right: 16px;
}
.env-manager-form__select-item {
  flex: 1;
  align-self: stretch;
  display: flex;
  align-items: center;
}
.env-manager-form a {
  white-space: nowrap;
}
.pckg-mngr-info {
  display: flex;
  cursor: pointer;
}
.pckg-mngr-info__icon {
  display: inline-block;
  width: 36px;
  height: 36px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
}
.pckg-mngr-info__label {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 16px;
}
.pckg-mngr-info__title {
  font-weight: 600;
  text-transform: capitalize;
}
.pckg-mngr-info__description {
  color: var(--main-color-8);
}
.packages-list {
  display: grid;
  grid-template-rows: auto auto 1fr;
  height: 100%;
}
.packages-list__title {
  padding: 8px 0;
}
.packages-list__list {
  overflow: auto;
}
.packages-list__header {
  font-weight: 700;
}
.packages-list__item {
  display: flex;
  justify-content: space-between;
  padding: 16px 12px;
  border-bottom: 1px solid var(--border-color);
}
.packages-list__item:last-child {
  border-bottom: none;
}
.datasource-files-panel {
  height: 100%;
}
.datasource-files-panel__tiles {
  height: 100%;
}
.datasource-files-panel__tiles > div {
  height: 100%;
}
.datasource-files-panel__expanded-tile {
  display: flex;
  flex-direction: column;
  height: 100%;
  overflow: auto;
}
.datasource-files-panel__tile-header.external-content {
  flex: 1;
  overflow: hidden;
}
.datasource-files-panel__tile-header.external-content > div {
  height: 100%;
  display: flex;
  flex-direction: column;
}
.datasource-files-panel__tile-header.external-content > div .attached-data-tile_expanded {
  flex: 1;
}
.datasource-files-panel__tile-content {
  flex: 1;
  overflow: auto;
  background-color: var(--tile-bg);
  border-left: 1px solid;
  border-right: 1px solid;
  padding: 0 12px;
  border-color: var(--border-color);
}
.datasource-files-panel__tile-content > div {
  height: 100%;
}
.dl-file {
  position: relative;
  padding: 5px;
  user-select: none;
  margin-top: -1px;
  border: 0 solid var(--border-color);
  border-width: 1px 0;
}
.dl-file-drag-possibility {
  background: var(--main-color-1);
}
.dl-file-drag-here {
  background: var(--main-color-2);
}
.dl-file.selected .icon use,
.dl-file.selected .icon g {
  fill: var(--contrast-fg);
}
.dl-file .icon {
  margin-right: 8px;
  flex-shrink: 0;
}
.dl-file_footer {
  margin-top: 8px;
}
.dl-file_content {
  display: flex;
  align-items: center;
}
.uploading .dl-file_content {
  opacity: 0.6;
}
.dl-file_column-name {
  flex-basis: 50%;
}
.dl-file_column-date {
  flex-basis: 35%;
}
.dl-file_column-size {
  flex-basis: 15%;
}
.dl-file_column-name,
.dl-file_column-date,
.dl-file_column-size {
  padding-left: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
input[type=text] .dl-file_column-name {
  border-bottom: 1px solid transparent;
}
input[type=text] .dl-file_column-name:focus {
  border-bottom: 1px solid var(--primary-bg);
}
.dl-file.selected {
  background-color: var(--main-color-8);
  color: var(--primary-bg);
  border-color: var(--primary-bg);
  z-index: 1;
}
.dl-file-preview {
  width: 100%;
  height: 100%;
  box-sizing: border-box;
  background: var(--primary-bg);
  padding: 10px;
}
.dl-file-preview_popup {
  width: 60%;
  height: 80%;
}
.dl-file-preview_content {
  height: 100%;
  overflow: auto;
  white-space: pre-wrap;
}
.dl-file-preview_img {
  text-align: center;
  font-size: 0;
}
.dl-file-preview_img img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}
.dl-files_content {
  position: relative;
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  color: var(--main-color-9);
  box-sizing: border-box;
  padding: 10px 0;
}
.dl-files_content .button.type--badge {
  margin: 0;
  border: none;
}
.dl-files-hover {
  background: var(--main-color-1);
}
.dl-files_header {
  display: flex;
  flex-shrink: 0;
  height: 32px;
  align-items: center;
  border-bottom: 1px solid var(--border-color);
  font-weight: bold;
}
.dl-files_list {
  flex-grow: 1;
  overflow-y: auto;
}
.dl-files_file-upload {
  width: 0.1px;
  height: 0.1px;
  opacity: 0;
  overflow: hidden;
  position: absolute;
  z-index: -1;
}
.dl-files_buttons-bar-left {
  flex-grow: 1;
}
.dl-files_buttons-bar {
  display: flex;
  flex-shrink: 0;
  align-items: center;
  margin-bottom: 6px;
  min-height: 30px;
}
.dl-files_list-empty {
  text-align: center;
}
.dl-files_footer {
  height: 35px;
  margin-top: 16px;
  flex-shrink: 0;
  display: grid;
  grid-template-columns: 1fr auto;
  align-items: center;
  text-align: end;
}
.dl-files_footer .list-button {
  display: inline-flex;
  min-width: 150px;
  width: auto;
}
.dl-files_footer_unpack-progress {
  text-align: start;
  overflow: hidden;
  text-overflow: ellipsis;
  max-width: 100%;
}
.dl-files_footer_unpack-progress .spinner {
  width: 12px;
  height: 12px;
}
.dl-files-upload-cancel-dialog {
  width: 300px;
}
.dl-files-upload-cancel-dialog_content {
  margin-top: 32px;
  margin-bottom: 32px;
}
.dl-files-upload-cancel-dialog_bar {
  text-align: right;
}
.dl-files_progress {
  position: relative;
  width: 100%;
}
.dl-files_progress .icon.icon-close {
  position: absolute;
  right: 0;
  top: 2px;
}
.dl-files_progress .dl-files_progress-bar {
  background-color: var(--action-color-1);
  width: 0%;
  height: 2px;
  margin-top: 6px;
  border-radius: 2px;
  -webkit-transition: width .1s linear;
  transition: width .1s linear;
}
.dl-files_progress-speed,
.dl-files_progress-completed {
  font-size: 11px;
  color: var(--main-color-3);
  font-weight: 200;
}
.dl-files_progress-completed {
  display: inline-block;
  min-width: 130px;
  margin-right: 10px;
}
.dl-files_progress-round .dl-files_progress-bar {
  display: inline-block;
  position: relative;
  width: 30px;
  height: 30px;
  border-radius: 30px;
  vertical-align: middle;
}
.dl-files_progress-round .dl-files_progress-bar-bg {
  position: absolute;
  left: 2px;
  right: 2px;
  top: 2px;
  bottom: 2px;
  border-radius: 13px;
  background: var(--primary-bg);
}
.dl-files_progress-round .dl-files_progress-info {
  display: inline-block;
  vertical-align: middle;
  margin-right: 12px;
}
.dl-files_progress-round .dl-files_progress-completed {
  margin: 0;
}
.dl-files_progress-round .dl-files_progress-speed {
  font-size: 9px;
}
.dl-files_progress-round .icon.icon-close {
  position: absolute;
  left: 7px;
  top: 7px;
}
.cr-import-dialog {
  display: flex;
  flex-direction: column;
}
.cr-import-dialog_hover {
  background: var(--main-color-1);
}
.cr-import-dialog_wrapper {
  display: flex;
  flex-grow: 1;
}
.cr-import-dialog_content-wrapper {
  box-sizing: border-box;
  flex-grow: 1;
  border: 2px dashed var(--border-color);
  display: flex;
  justify-content: center;
  align-items: center;
}
.cr-import-dialog_content {
  text-align: center;
}
.cr-import-dialog_text {
  margin-top: 14px;
  font-size: 17px;
}
.cr-import-dialog_subtext {
  font: 10px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}
.cr-import-dialog_line {
  display: inline-block;
  width: 180px;
  margin: 0 6px;
  border-bottom: 1px solid var(--main-color-3);
  vertical-align: middle;
}
.cr-import-dialog_row-line {
  margin: 20px 0;
  color: var(--main-color-6);
}
.cr-import-dialog .button input {
  display: none;
}
.cr-import-dialog_upload-url-section {
  display: flex;
  width: 100%;
  margin-bottom: 13px;
}
.cr-import-dialog_url-input {
  flex-grow: 1;
}
.cr-import-dialog_upload-button {
  width: auto;
}
.dl-overlay .spinner {
  margin-top: 4px;
}
.dl-overlay_content {
  display: grid;
  grid-template-columns: auto 1fr;
}
.dl-overlay_content_text {
  display: flex;
  align-items: center;
}
.dl-overlay_content-exceed-limit {
  text-align: center;
  padding: 10px;
}
.dl-overlay_status-bar {
  display: inline-block;
  margin-left: 10px;
}
.dl-overlay_additional-data {
  display: block;
  word-break: normal;
  max-width: 200px;
  margin-top: 12px;
  margin-left: 10px;
}
.dl-overlay_actions-bar {
  margin-top: 10px;
}
.button.notification-button {
  width: 100%;
  box-sizing: border-box;
  margin: 10px 0 0;
}
.instance-switch_dialog {
  width: 360px;
  text-align: left;
}
.instance-switch_main-section {
  font-size: 14px;
  margin-bottom: 20px;
}
.instance-switch_display-text {
  font-weight: 500;
}
.cr-menu {
  display: inline-block;
  white-space: nowrap;
  user-select: none;
  vertical-align: middle;
  margin: -1px 0 0 -8px;
}
.cr-menu-item_separator {
  margin: 5px 0;
  border-bottom: 1px solid var(--border-color);
}
.cr-menu-sub {
  display: inline-block;
  padding: 12px 0;
  color: var(--main-color-3);
  cursor: default;
}
.cr-menu-sub:hover {
  cursor: pointer;
}
.cr-menu-sub:hover,
.cr-menu-sub_hovered {
  color: var(--contrast-fg);
}
.cr-menu-sub_title {
  display: inline-block;
  margin: 0 8px;
}
.cr-menu-sub_popup {
  min-width: 150px;
  max-height: unset;
}
div.publish-dialog {
  padding: 0 16px 16px;
  width: 364px;
  overflow: visible;
}
div.publish-dialog .share-form_section {
  padding: 0;
}
div.publish-dialog .share-form_section .button {
  flex-grow: 1;
  margin: 0;
}
div.publish-dialog .share-form_action_row {
  display: flex;
  align-items: center;
}
div.publish-dialog .dl-select {
  width: 100%;
  max-width: 100%;
}
.report-type-item {
  display: flex;
  padding: 8px 0;
}
.report-type-item__icon {
  display: block;
  width: 24px;
  flex-shrink: 0;
}
.report-type-item__description {
  color: var(--main-color-5);
  white-space: initial;
  font-weight: 400;
}
.share-popup_wrap {
  position: relative;
}
.share-popup_wrap .share-popup_open {
  margin: 0;
}
.share-popup_wrap .icon {
  opacity: 1;
}
.collaboration-popup {
  width: 364px;
  color: var(--main-color-9);
  text-align: left;
  white-space: break-spaces;
  -webkit-box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.25);
  -moz-box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.25);
  box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.25);
}
.collaboration-popup .share-form_section {
  padding: 16px;
}
.collaboration-popup .share-form_section:last-child {
  border-top: 1px solid var(--main-color-2);
}
.collaboration-popup .share-form_section .share-form_action_row {
  display: flex;
  align-items: center;
}
.collaboration-popup .share-form_section .share-form_action_info {
  flex: 1 0;
}
.collaboration-popup .share-form_section .workspace-name {
  font-style: italic;
}
.collaboration-popup_button {
  width: 100%;
}
.collaboration-popup_button .icon-side-panel {
  transform: rotate(-90deg);
}
.collaboration-popup_button .icon-side-panel use,
.collaboration-popup_button .icon-side-panel g {
  fill: var(--main-color-5);
}
.collaboration-popup .dl-select {
  width: 100%;
  max-width: 100%;
}
.share-form_section {
  padding: 16px 24px;
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.share-form_section_title {
  display: flex;
  align-items: center;
  font-weight: 600;
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
}
.share-form_section_title .icon {
  margin-right: 8px;
}
.share-form_section_emphasizing {
  font-weight: 700;
}
.share-form_section_action {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.share-form_select_title {
  display: flex;
  align-items: center;
  gap: 8px;
}
.share-form_select_title > .icon use {
  fill: var(--action-color-2);
}
.share-form_select_item {
  display: grid;
  grid-template-columns: 24px auto 16px;
  gap: 4px;
  width: 100%;
}
.share-form_select-popup,
.share-form_select-popup > div {
  width: 100%;
  max-width: 100%;
}
.share-form_select-popup .selected {
  background-color: transparent;
}
.share-form {
  display: flex;
  flex-direction: column;
  height: 100%;
}
.share-form_title,
.share-form_warning,
.share-form_message {
  padding: 16px 24px 16px 24px;
}
.share-form_title {
  display: flex;
  align-items: center;
  font-size: 16px;
  line-height: 24px;
  font-weight: normal;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.share-form_title > div {
  max-width: 500px;
  font-weight: 600;
  margin: 0 4px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.share-form_message {
  line-height: 16px;
  margin: 0;
}
.share-form_warning {
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  background-color: var(--attention-color-1);
  overflow: hidden;
  transition: max-height 0.2s;
  min-height: 28px;
}
.share-form_warning_title {
  flex: 1 0;
  margin: 0 16px 0 16px;
  font-weight: 600;
}
.share-form_warning.--hide {
  max-height: 48px;
  transition-timing-function: cubic-bezier(0.39, 0.58, 0.57, 1);
}
.share-form_warning.--show {
  max-height: 125px;
  transition-timing-function: cubic-bezier(0.39, 0.58, 0.57, 1);
}
.share-form_warning_header {
  display: flex;
  align-items: center;
  flex: 1 0;
}
.share-form_warning_header > .icon use {
  fill: var(--attention-color-3);
}
.share-form_warning > p {
  margin: 16px 0 0 0;
  color: var(--main-color-8);
}
.share-form_main {
  display: flex;
  flex-direction: column;
  flex: 1 0;
  padding: 0 0 24px 0;
  box-sizing: border-box;
  overflow: hidden;
}
.share-form_invitation {
  display: flex;
  align-items: stretch;
  justify-content: flex-end;
}
.share-form_invitation > .button {
  min-width: 160px;
  margin-left: 12px;
}
.share-form_leave {
  display: flex;
}
.share-form_list {
  display: flex;
  flex-direction: column;
  flex: 1 0;
  overflow: auto;
  border-top: 1px solid var(--main-color-2);
  padding: 0 24px 0 24px;
}
.share-form_link {
  cursor: pointer;
}
.share-form-access-row-item {
  display: grid;
  grid-template-columns: 40px auto 200px 75px 32px;
  align-items: center;
  height: 40px;
  box-sizing: border-box;
  padding: 8px;
  border-bottom: 1px solid var(--main-color-2);
}
.share-form-access-row-item .dl-select_title {
  font-weight: normal;
}
.share-form-access-row-item .dl-select_title .icon use {
  fill: var(--main-color-4);
}
.share-form-access-row-item__select-item {
  width: 100%;
  display: flex;
  align-items: center;
}
.share-form-access-row-item__select-item > span {
  flex: 1;
}
.share-form-access-row-item__select-item_selected {
  opacity: .7;
}
.share-form-access-row-item_pending {
  color: var(--main-color-5);
}
.share-form-access-row-item__menu {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  cursor: pointer;
}
.share-form-access-row-item__menu .icon use {
  transition: fill 0.2s ease-in;
  fill: var(--main-color-4);
}
.share-form-access-row-item__menu:hover .icon use {
  fill: var(--main-color-9);
}
.share-form-access-row-item__default-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 24px;
  height: 24px;
}
.share-form-access-row-item__default-icon > .icon {
  width: 24px;
  height: 24px;
}
.run-out-memory-alert .button {
  margin-top: 8px;
}
.dl-cell-error {
  color: var(--negative-color-2);
  cursor: pointer;
  padding: 4px 8px;
  margin: 0 -8px;
}
.dl-cell-error:hover {
  background-color: var(--main-color-1);
}
.dl-cell-error.selected {
  background-color: var(--negative-color-2);
  color: var(--primary-bg);
}
.dl-cell-errors {
  padding-bottom: 4px;
  max-width: 280px;
}
.dl-cell-errors_header {
  padding: 4px 12px;
  background-color: var(--main-color-2);
}
.dl-cell-errors .popup-close {
  top: 7px !important;
  right: 8px !important;
}
.dl-cell-errors .popup-close:before {
  font-size: 12px !important;
}
.dp-application-block {
  width: 100%;
  height: 100%;
  display: grid;
  grid-template-columns: auto 1fr;
  grid-template-rows: 1fr auto;
  flex-grow: 1;
  outline: none;
}
/* fix grid overflow */
.dp-sidebar-panel,
.dp-editor-panel {
  min-height: 0;
  min-width: 0;
}
.dp-sidebar-panel {
  box-shadow: 0px 0px 12px rgba(0, 0, 0, 0.15);
  z-index: 1;
}
.dp-editor-panel {
  outline: none;
}
.dp-status-panel {
  grid-column: span 2;
}
.side-tab-content_auto {
  box-sizing: border-box;
  padding: 30px;
  width: 100%;
  min-height: 100%;
}
.side-tab-content_fit {
  width: 100%;
  height: 100%;
}
.error-panel {
  height: 100%;
  padding: 8px;
  box-sizing: border-box;
  overflow: auto;
  white-space: normal;
  background: var(--primary-bg);
}
.error-panel_title {
  padding: 12px 0 8px;
}
.dl-kernel-error {
  padding: 4px 8px;
  margin: 0 -8px;
}
.dl-kernel-error_time {
  margin-right: 8px;
}
.dl-kernel-error_message {
  color: var(--negative-color-2);
}
.kernel-errors_bar .button {
  margin-right: 8px;
}
.dl-status-bar {
  color: var(--contrast-fg);
  background-color: var(--contrast-bg);
  font-size: 11px;
  user-select: none;
  -webkit-user-select: none;
  overflow: hidden;
  /* bar sections */
  /* errors-label */
}
.presentation-mode .dl-status-bar {
  display: none;
}
.dl-status-bar_bar {
  display: flex;
  justify-content: space-between;
  padding: 5px 10px;
  white-space: nowrap;
}
.dl-status-bar_left {
  align-self: flex-start;
}
.dl-status-bar_right {
  display: inline-flex;
  align-self: flex-end;
  flex-shrink: 1;
  min-width: 0;
}
.dl-status-bar_close {
  flex-shrink: 0;
  align-self: center;
}
.dl-status-bar .dl-status-content {
  display: inline;
}
.dl-status-bar_bar .dl-status-bar_section,
.dl-status-bar_bar .dl-status,
.dl-status-bar_bar .dl-status_section {
  display: inline;
  margin-right: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  flex-shrink: 0;
}
.dl-status-bar_cpu {
  display: inline-block;
  text-align: right;
  min-width: 4.1ch;
}
.dl-status-bar_mem {
  display: inline-block;
  text-align: right;
  min-width: 8ch;
}
.dl-status-bar_cells_count {
  display: inline-block;
  min-width: 2.1ch;
}
.dl-status-bar_right .dl-status-bar_section:last-child {
  margin-right: 0;
}
.dl-status-bar_section-extended {
  flex-shrink: 1;
  min-width: 0;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  user-select: initial;
  -webkit-user-select: initial;
}
.dl-status-bar_separator {
  display: inline-block;
  width: 1px;
  height: 12px;
  flex-shrink: 0;
  margin: 0 10px;
  background-color: var(--main-color-7);
  vertical-align: top;
}
.dl-status-bar_errors-label {
  margin-right: 8px;
  flex-shrink: 0;
  align-self: center;
}
.dl-status-bar_errors-label use,
.dl-status-bar_errors-label g {
  fill: var(--negative-color-3);
}
.dl-status-bar_section-uploader {
  display: none !important;
}
.dl-status-bar_section-uploader-progress {
  background-color: var(--action-color);
  display: inline-block;
  width: 100px;
  height: 4px;
  border-radius: 2px;
  position: relative;
  top: -2px;
}
.dl-status-bar_background-computation {
  font: 17px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  line-height: 10px;
  opacity: 0.7;
}
.dl-status-bar_background-computation.active {
  color: var(--action-color);
  opacity: 1;
}
.dl-status-bar_reactive-mode .toggler {
  margin-bottom: -1px;
  margin-right: 2px;
}
.dl-status-bar_reactive-mode .toggler-disabled {
  cursor: default;
}
.dl-status-bar_hover {
  cursor: pointer;
}
.dl-status-bar_hover:hover {
  color: var(--attention-color-2);
  text-decoration: underline;
}
.dl-status-bar_kernel-type {
  cursor: pointer;
}
.dl-status-bar_kernel-type .icon {
  vertical-align: middle;
  margin-top: -4px;
  opacity: 0.8;
}
.dl-status-bar_language .icon {
  vertical-align: middle;
  margin-top: -4px;
  margin-right: 8px;
  opacity: 0.8;
}
.dl-status-bar_status {
  cursor: pointer;
}
.dl-status-bar_library-manager-container {
  display: inline-block;
  margin-left: 5px;
  margin-right: 5px;
}
.dl-status-bar_library-manager-btn {
  display: inline-block;
  width: 16px;
  height: 100%;
  background-repeat: no-repeat;
  background-size: contain;
  background-position: center;
}
.dl-status-bar-uploader {
  position: relative;
  display: inline-block;
  width: 100px;
  padding-right: 16px;
  cursor: pointer;
}
.dl-status-bar-uploader_progress-container {
  display: inline-block;
  width: 100%;
  margin-bottom: 1px;
  background: var(--main-color-3);
  border-radius: 5px;
  overflow: hidden;
}
.dl-status-bar-uploader_progress-bar {
  background: var(--action-color-1);
  height: 5px;
}
.dl-status-bar-uploader_tooltip {
  max-width: 250px;
}
.dl-status-bar-uploader_tooltip-file {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.dl-status-bar-uploader_tooltip-bar {
  margin-top: 6px;
}
.dl-status-bar-uploader .icon.icon-close {
  vertical-align: middle;
  margin-top: -2px;
}
.dp-tabs-panel {
  display: grid;
  grid-template-columns: auto auto;
  justify-content: space-between;
}
.dp-tabs-panel_btn {
  padding: 8px;
  line-height: 0;
  cursor: pointer;
  opacity: 0.8;
}
.dp-tabs-panel_btn:hover {
  opacity: 1;
}
.dp-tabs-panel_menu {
  z-index: 2;
}
.text-file-editor {
  background: var(--editor-bg);
  padding: 10px;
}
.text-file-editor_toolbar {
  margin-top: -20px;
  text-align: right;
  line-height: 0;
}
.text-file-editor_button {
  display: inline-block;
  padding: 5px;
  border: 1px solid var(--border-color);
  border-radius: 3px;
  background: var(--primary-bg);
  opacity: 0.9;
}
.text-file-editor_buttons {
  margin: 0 0 12px 0;
  display: flex;
  align-items: center;
}
.text-file-editor > div {
  margin: 20px 0 0 0;
}
.inspection-profile {
  display: grid;
  grid-template-rows: 1fr auto auto;
  grid-gap: 12px;
}
.inspection-profile_items {
  overflow: auto;
  border-bottom: 1px solid var(--main-color-2);
}
.inspection-profile_item {
  display: flex;
  padding: 2px 12px;
  cursor: pointer;
}
.inspection-profile_item.selected {
  background-color: var(--main-color-2);
}
.inspection-profile_item_name {
  flex-grow: 1;
  user-select: none;
}
.inspection-profile_item_description {
  overflow: auto;
  height: 10em;
  border-bottom: 1px solid var(--main-color-2);
  padding-bottom: 12px;
}
.inspection-profile_buttons {
  display: flex;
  justify-content: flex-end;
}
.inspection-profile_input {
  position: absolute;
  width: 0;
  height: 0;
  padding: 0;
  margin: 0;
  border: none;
}
.editor-tab {
  display: inline-flex;
  align-items: center;
  position: relative;
  padding: 8px 10px;
  background: var(--workbook-bg);
  border-right: 2px solid var(--border-color);
  user-select: none;
  overflow: hidden;
}
.editor-tab_name {
  margin: 0 8px;
  overflow: hidden;
  text-overflow: ellipsis;
}
.editor-tab .icon {
  flex-shrink: 0;
}
.editor-tab.selected {
  background: var(--primary-bg);
}
.editor-tab.selected::after {
  content: ' ';
  display: block;
  height: 3px;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: var(--action-color);
}
.editor-tab_dragged {
  position: absolute;
  background: var(--primary-bg);
  z-index: 10;
  pointer-events: none;
}
.editor-tab-content-wrapper {
  height: 100%;
}
.editor-tabs {
  height: 100%;
  display: flex;
  flex-direction: column;
  background: var(--workbook-bg);
  outline: none;
}
.presentation-mode .editor-tabs_tabs-container {
  bottom: 0;
  transform: translateY(calc(100%));
  position: absolute;
  transition: 0.15s ease-out transform;
  left: 0;
  right: 0;
}
.presentation-mode .editor-tabs_tabs-container:hover {
  transform: none;
}
.presentation-mode .editor-tabs_tabs-container::after {
  content: " ";
  display: block;
  position: absolute;
}
.presentation-mode .editor-tabs_tabs-container::after {
  left: 0;
  right: 0;
  height: 20px;
}
.out-bottom.presentation-mode .editor-tabs_tabs-container {
  transform: none;
}
.presentation-mode .editor-tabs_tabs-container::after {
  top: 0;
  margin-top: -20px;
}
.editor-tabs_content-container {
  flex-grow: 1;
  overflow: auto;
}
.editor-tabs_content {
  height: 100%;
  outline: none;
}
.editor-tabs_tabs-container {
  display: flex;
  flex-shrink: 0;
  z-index: 1;
  border-top: 2px solid var(--border-color);
  background: var(--tabs-container);
}
.split-section:first-child .editor-tabs_tabs-container {
  border-left: 2px solid var(--border-color);
}
.editor-tabs_panel {
  flex-grow: 1;
}
.editor-tabs_tabs {
  display: flex;
  flex-shrink: 1;
  overflow: hidden;
  white-space: nowrap;
}
.sidebar {
  display: flex;
  height: 100%;
  background: var(--primary-bg);
  outline: none;
}
.presentation-mode .sidebar.closed {
  left: 0;
  transform: translateX(calc(-100%));
  position: absolute;
  transition: 0.15s ease-out transform;
  top: 0;
  bottom: 0;
}
.presentation-mode .sidebar.closed:hover {
  transform: none;
}
.presentation-mode .sidebar.closed::after {
  content: " ";
  display: block;
  position: absolute;
}
.presentation-mode .sidebar.closed::after {
  top: 0;
  bottom: 0;
  width: 20px;
}
.out-left.presentation-mode .sidebar.closed {
  transform: none;
}
.presentation-mode .sidebar.closed::after {
  right: 0;
  margin-right: -20px;
}
.sidebar.closed .sidebar_panel {
  display: none;
}
.sidebar_action {
  position: relative;
  display: block;
  padding: 5px;
  margin-bottom: 12px;
  opacity: 0.7;
  line-height: 0;
  user-select: none;
}
.sidebar_action:last-child {
  margin-bottom: 0;
}
.sidebar_action:hover,
.sidebar_action.active {
  opacity: 1;
  cursor: pointer;
}
.sidebar_bar {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 12px 8px 16px;
  flex-shrink: 0;
}
.sidebar_main-actions .sidebar_action.active:before {
  display: block;
  width: 6px;
  position: absolute;
  top: 0;
  bottom: 0;
  left: -8px;
  content: ' ';
  background: var(--action-color-2);
}
.sidebar_secondary-actions .sidebar_action {
  padding: 8px;
}
.sidebar_panel {
  display: flex;
  flex-direction: column;
  flex-shrink: 0;
  position: relative;
  padding: 16px 12px 0 12px;
  box-sizing: border-box;
  max-width: 70vw;
}
.sidebar_panel.hidden {
  display: none;
}
.sidebar_panel-header {
  position: relative;
  margin-bottom: 12px;
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
}
.sidebar_panel-close {
  position: absolute;
  right: -4px;
  padding: 4px;
  cursor: pointer;
}
.sidebar_panel-content {
  height: 100%;
}
.sidebar_panel-contents {
  height: 100%;
  overflow: hidden;
}
.sidebar_resizer {
  position: absolute;
  right: -4px;
  top: 0;
  bottom: 0;
  width: 8px;
  cursor: col-resize;
}
.split-panel {
  width: 100%;
  height: 100%;
  white-space: nowrap;
}
.split-section {
  position: relative;
  display: inline-block;
  vertical-align: top;
  height: 100%;
  padding: 0 1px;
  box-sizing: border-box;
}
.split-section_content {
  height: 100%;
}
.split-section_splitter {
  position: absolute;
  top: 0;
  bottom: 0;
  right: -5px;
  padding: 0 4px;
  z-index: 1;
  cursor: col-resize;
}
.split-section_splitter-bg {
  width: 2px;
  height: 100%;
  background: var(--main-color-2);
}
.split-section:last-child {
  padding-right: 0;
}
.split-section:last-child .split-section_splitter {
  display: none;
}
.split-section:first-child {
  padding-left: 0;
}
.ed-cell {
  position: relative;
  margin-bottom: 16px;
  background: var(--cell-bg);
  outline: none;
  box-sizing: border-box;
}
.ed-cell.in-block-selection {
  outline: var(--main-color-3) solid 1px;
}
.worksheet-focused .ed-cell.in-block-selection {
  outline-color: var(--action-color-2);
}
.ed-cell.focused {
  outline: var(--main-color-3) solid 1px;
  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.1) !important;
}
.worksheet-focused .ed-cell.focused {
  outline-color: var(--action-color-2);
}
.ed-cell:hover {
  box-shadow: -1px 0px 0px 0px var(--main-color-2);
}
.ed-cell img {
  max-width: 100%;
}
.ed-cell table {
  font-size: 12px;
  border-collapse: collapse;
  border: 1px solid var(--main-color-3);
}
.ed-cell table th {
  padding: 0.25em;
  border: 1px solid var(--main-color-3);
  background-color: var(--main-color-1);
}
.ed-cell table td {
  border: 1px solid var(--main-color-3);
  padding: 0.25em;
}
.ed-cell.ed-cell-output {
  padding: 16px;
  font-size: 14px;
}
.ed-cell.ed-cell-output .button-type-secondary {
  font: 12px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  width: 100%;
  margin: 10px 0;
  cursor: default;
}
.mixed-cell {
  outline: none;
  padding: 0;
}
.mixed-cell-input-container,
.mixed-cell-output-container {
  position: relative;
}
.mixed-cell-input .code-editor-container,
.mixed-cell-input .md-editor-container,
.mixed-cell-input .controls-container,
.mixed-cell-input .collapsed-input {
  padding: 24px 16px 17px;
}
.is-touch .mixed-cell-input .code-editor-container,
.is-touch .mixed-cell-input .md-editor-container,
.is-touch .mixed-cell-input .controls-container,
.is-touch .mixed-cell-input .collapsed-input {
  padding-top: 36px;
}
.mixed-cell-input .code-editor-container,
.mixed-cell-input .md-editor-container,
.mixed-cell-input .collapsed-input {
  background: var(--editor-bg);
}
.line-numbers-enabled .mixed-cell-input .code-editor-container,
.line-numbers-enabled .mixed-cell-input .md-editor-container {
  padding-left: 8px;
}
.mixed-cell-input .md-editor-container {
  padding-top: 36px;
}
.mixed-cell-input-container-controlls .mixed-cell-input .collapsed-input {
  background: var(--workbook-bg);
}
.mixed-cell-input-container-markdown .mixed-cell-input .collapsed-input {
  padding-top: 36px;
}
.mixed-cell-output {
  padding: 16px;
  position: relative;
  user-select: text !important;
  font-size: 14px;
}
.mixed-cell-separator {
  display: block;
  margin: 0 16px;
  height: 1px;
  background-color: var(--input-output-separator);
}
.mixed-cell-execution-counter {
  position: absolute;
  top: 6px;
  right: calc(100% + 12px);
  text-align: left;
  font-size: 10px;
  line-height: 20px;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  color: var(--main-color-6);
}
.mixed-worksheet {
  position: relative;
  box-sizing: border-box;
  padding: 30px 50px;
  width: 100% !important;
  min-height: 100%;
  min-width: 320px;
}
.mixed-worksheet-blocks {
  overflow: visible !important;
  margin: 0 auto;
  min-height: 100%;
  box-sizing: border-box;
  width: 100% !important;
  max-width: 1064px;
  min-width: 140px;
}
.mixed-worksheet-toolbar {
  min-width: 140px;
  font: 12px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  margin-top: 20px;
  text-align: center;
}
.add-block-area {
  position: absolute;
  left: 6px;
  right: 6px;
  bottom: -16px;
  height: 16px;
  text-align: center;
}
.add-block-area__content {
  position: relative;
  z-index: 2;
  width: 100%;
  transform: translateY(calc(-50% - 2px / 2));
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.1s cubic-bezier(0.65, 0.05, 0.36, 1) 0.1s;
}
.add-block-area__actions {
  display: inline-block;
}
.add-block-area__line {
  display: block;
  transform: scaleX(0);
  transition: transform 0.1s ease-in-out, opacity 0.15s ease-out;
  background: var(--action-color);
  border-radius: 8px;
  height: 2px;
  margin-top: 7px;
  opacity: 0.05;
}
.add-block-area:hover .add-block-area__content,
.add-block-area.active .add-block-area__content {
  opacity: 1;
  pointer-events: initial;
}
.add-block-area:hover .add-block-area__line,
.add-block-area.active .add-block-area__line {
  transform: scaleX(0.7);
  opacity: .9;
}
.add-block-area__button {
  display: inline-block;
  line-height: initial;
  cursor: pointer;
  border: 1px solid var(--border-color);
  border-right: none;
  padding: 4px 8px;
  background: var(--primary-bg);
  color: var(--main-color-8);
  box-shadow: 1px 2px 4px 0px rgba(0, 0, 0, 0.08);
  transition: background-color 0.1s ease-in, border-color 0.1s ease-in;
}
.add-block-area__button:hover,
.add-block-area__button.active {
  background-color: var(--main-color-1);
}
.add-block-area__button:active {
  background-color: var(--main-color-2);
}
.add-block-area__button:first-child {
  border-top-left-radius: 50px;
  border-bottom-left-radius: 50px;
  margin-left: -20px;
}
.add-block-area__button:last-child {
  border-right: 1px solid var(--border-color);
  border-top-right-radius: 50px;
  border-bottom-right-radius: 50px;
}
.add-block-area__button-shortcut {
  color: var(--main-color-6);
}
.width-xs .add-block-area__button:first-child {
  margin-left: 0;
}
.width-xs .add-block-area__button-shortcut {
  display: none;
}
.collapsed-input {
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.collapsed-output {
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.dl-cell-time {
  min-width: 35px;
  margin: 0 0 0 4px;
}
.code-cell-actions {
  display: flex;
  align-items: center;
}
.code-cell-actions__time {
  font-size: 10px;
  line-height: 20px;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  color: var(--main-color-5);
}
.computation-status-tooltip {
  display: flex;
  box-sizing: border-box;
  min-width: 300px;
  max-width: 350px;
  padding: 12px;
  gap: 12px;
}
.computation-status-tooltip__status {
  display: inline-block;
  width: 24px;
  height: 24px;
  flex-shrink: 0;
  background-size: contain;
  background-repeat: no-repeat;
}
.computation-status-tooltip_finished .computation-status-tooltip__status {
  background-image: url("/assets/images/status-valid.svg");
}
.computation-status-tooltip_changed .computation-status-tooltip__status {
  background-image: url("/assets/images/status-changed.svg");
}
.computation-status-tooltip h3 {
  margin: 4px 0 8px;
}
.new-cell-toolbar {
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  display: grid;
  align-items: center;
  grid-template-columns: auto minmax(0, 1fr) auto auto;
  grid-template-areas: "runnable custom visibility-indicator common";
  min-width: 0;
  height: 24px;
  padding: 0 16px 0 12px;
  z-index: 1;
  pointer-events: none;
}
.new-cell-toolbar__runnable {
  grid-area: runnable;
  pointer-events: initial;
}
.new-cell-toolbar__custom {
  grid-area: custom;
  pointer-events: initial;
}
.new-cell-toolbar__visibility-indicator {
  grid-area: visibility-indicator;
}
.new-cell-toolbar__common {
  display: none;
  grid-area: common;
  pointer-events: initial;
}
.new-cell-toolbar.active .new-cell-toolbar__common {
  display: block;
}
.new-cell-toolbar__common .new-cell-toolbar-action {
  position: relative;
  margin: 0 2px;
}
.new-cell-toolbar__common .new-cell-toolbar-action_lang,
.new-cell-toolbar__common .new-cell-toolbar-action_visibility {
  padding: 4px 0 4px 4px;
}
.is-touch .new-cell-toolbar__common .new-cell-toolbar-action_lang,
.is-touch .new-cell-toolbar__common .new-cell-toolbar-action_visibility {
  padding: 8px 0 8px 8px;
}
.new-cell-toolbar__common .new-cell-toolbar-action:last-child {
  margin-right: 0;
}
.new-cell-toolbar__common .new-cell-toolbar-action:first-child {
  margin-left: 0;
}
.new-cell-toolbar-action {
  display: inline-block;
  padding: 4px;
  line-height: 0;
  cursor: pointer;
}
.new-cell-toolbar-action use,
.new-cell-toolbar-action g {
  fill: var(--main-color-6);
}
.new-cell-toolbar-action:hover use,
.new-cell-toolbar-action:hover g {
  fill: var(--main-color-9);
}
.new-cell-toolbar-action[disabled] use,
.new-cell-toolbar-action:disabled use,
.new-cell-toolbar-action[disabled]:hover use,
.new-cell-toolbar-action:disabled:hover use,
.new-cell-toolbar-action[disabled] g,
.new-cell-toolbar-action:disabled g,
.new-cell-toolbar-action[disabled]:hover g,
.new-cell-toolbar-action:disabled:hover g {
  fill: var(--main-color-3);
}
.new-cell-toolbar-action .icon {
  width: 12px;
  height: 12px;
}
.is-touch .new-cell-toolbar-action {
  padding: 8px;
}
.is-touch .new-cell-toolbar-action .icon {
  width: 16px;
  height: 16px;
}
.new-cell-toolbar-action_menu {
  padding-right: 0;
}
.new-cell-toolbar-action_menu .icon-flyout {
  transition: transform 0.15s ease-out;
}
.new-cell-toolbar-action_menu.active .icon-flyout {
  transform: rotate(-180deg);
}
.new-cell-toolbar-action_menu_active .icon-flyout {
  transform: rotate(-180deg);
}
.new-cell-toolbar-action .icon-run use,
.new-cell-toolbar-action .icon-run g {
  fill: var(--action-color-2);
}
.new-cell-toolbar-action .icon-run:hover use,
.new-cell-toolbar-action .icon-run:hover g {
  fill: var(--action-color-3);
}
.focused .new-cell-toolbar-action.active .icon-run {
  animation: showRun 0.25s cubic-bezier(0.45, 1.45, 0.8, 1);
}
@keyframes showRun {
  from {
    transform: translate(-16px, 0);
    opacity: 0;
  }
  to {
    transform: translate(0, 0);
    opacity: 1;
  }
}
.new-cell-visibility-indicator {
  padding: 0 8px;
  height: 20px;
  display: flex;
  align-items: center;
  font-size: 10px;
  line-height: 20px;
  color: var(--main-color-4);
}
.is-touch .new-cell-visibility-indicator {
  height: 32px;
}
.new-cell-visibility-indicator .icon-hide {
  padding: 0 4px;
  width: 10px;
  height: 10px;
}
.new-cell-visibility-indicator .icon-hide use {
  fill: var(--main-color-4);
}
.is-touch .new-cell-visibility-indicator .icon-hide {
  width: 12px;
  height: 12px;
}
.dl-search {
  height: calc(100% - 73px) !important;
  display: flex;
  flex-direction: column;
}
.dl-search_content {
  position: relative;
  padding-top: 30px;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
.dl-search_content .stub {
  background-color: var(--primary-bg);
}
.dl-search_info {
  position: absolute;
  left: 0;
  right: 0;
  top: 5px;
  font-size: 10px;
  color: var(--main-color-4);
}
.dl-search_results {
  height: 160px;
  overflow: auto;
  flex-shrink: 0;
}
.dl-search_line {
  margin: 8px 0;
  border-bottom: 1px solid var(--border-color);
  flex-shrink: 0;
}
.dl-search_preview {
  flex-grow: 1;
  overflow: hidden;
}
.dl-search_highlight {
  display: inline-block;
  position: absolute;
  top: 0;
  background: var(--attention-color-1);
}
.dl-search-preview {
  position: relative;
  height: 100%;
  overflow: hidden;
  flex-grow: 1;
}
.dl-search-preview_code {
  position: relative;
  z-index: 1;
  margin: 0;
  color: black;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.dl-search-preview .dl-search_highlight {
  bottom: auto;
  height: 14px;
}
.dl-search-result {
  display: flex;
  padding: 2px;
  outline: none;
  cursor: initial;
  user-select: none;
}
.dl-search-result.selected {
  background-color: var(--main-color-2);
}
.dl-search-result_preview {
  position: relative;
  flex-grow: 1;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  color: var(--main-color-9);
}
.dl-search-result_preview-code {
  position: relative;
  z-index: 1;
  margin: 0;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.dl-search-result_info {
  flex-shrink: 0;
  color: var(--main-color-4);
  padding-left: 10px;
}
.command {
  display: flex;
  align-items: center;
  height: 45px;
  padding: 0 16px;
  box-sizing: border-box;
  cursor: pointer;
  gap: 4px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
}
.command:last-child {
  border-bottom-color: var(--border-color);
}
.command.selected,
.command:hover {
  background-color: var(--main-color-1);
}
.command.disabled {
  color: var(--main-color-6);
  cursor: default;
}
.command__side {
  width: 24px;
  display: inline-block;
  line-height: 0;
}
.command__title {
  flex-grow: 1;
}
.command__match {
  font-weight: bold;
  color: var(--action-color-3);
}
.command__shortcut {
  color: var(--main-color-6);
}
.command__description {
  color: var(--main-color-5);
}
.command-palette {
  display: grid;
  grid-template-rows: auto 1fr;
  width: 500px;
  height: 507px;
}
.command-palette_header {
  padding: 12px;
  box-shadow: 0px 0px 7px 0px rgba(0, 0, 0, 0.11);
}
.command-palette_header .input {
  width: 100%;
}
.command-palette_actions {
  height: 100%;
  overflow: auto;
}
.command-palette_section:last-child .command:last-child {
  border-bottom-color: transparent;
}
.block {
  position: relative;
  box-sizing: border-box;
  width: 100%;
  font-size: 14px;
}
.block_item:not(:first-child) {
  margin: 0 0 0 0;
}
.block_input {
  border-left: 1px solid var(--main-color-3);
}
.block_input:empty {
  padding: 0;
}
.block_output {
  border-left: 1px solid var(--main-color-3);
  padding: 8px;
}
.block_execute {
  position: absolute;
  box-sizing: border-box;
  width: 100px;
  padding: 0 4px 8px 8px;
  margin-left: -100px;
  user-select: none;
  cursor: default;
  color: var(--main-color-7);
  font-size: 10px;
  text-align: right;
}
.block .block_output-wrap .edge:not(:first-child) {
  width: 4px;
  height: 1px;
  background-color: var(--main-color-3);
  border: none;
}
.block-output {
  border-left: 1px solid var(--main-color-3);
  overflow: hidden;
  padding: 8px 16px;
}
.block-output > div {
  overflow: auto;
}
.block-output img {
  max-width: 100%;
}
.block-output .publishing-text-output {
  margin: 0;
  white-space: pre;
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.block-output table {
  border: none;
  border-spacing: 0;
  border-collapse: collapse;
}
.block-output table td,
.block-output table th {
  border: none;
}
.block-output table td,
.block-output table th,
.block-output table tr {
  padding: 4px;
}
.block-output table tr:nth-child(2n) {
  background-color: var(--main-color-1);
}
.block-output table tbody tr:hover {
  background-color: rgba(33, 150, 243, 0.18);
}
.block-wrap + .block-wrap {
  margin-top: 12px;
}
.block-wrap__content__wrap {
  position: relative;
}
.block-wrap__actions {
  position: absolute;
  bottom: 0;
  left: -99px;
  box-sizing: border-box;
  display: none;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-end;
  min-width: 100px;
  height: 100%;
  padding-right: 8px;
  border-right: 1px solid var(--main-color-3);
}
.block-wrap__actions > .button {
  height: auto;
  flex-direction: row-reverse;
}
.block-wrap__actions > .button > .icon {
  margin: 0;
}
.block-wrap__actions > .button > span {
  color: var(--main-color-7);
  margin-right: 8px;
  max-width: 56px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.block-wrap:hover .block-wrap__actions,
.block-wrap.active .block-wrap__actions {
  display: flex;
}
.markdown-output {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  font-size: 14px;
  line-height: 24px;
  color: var(--main-color-8);
  padding: 16px 16px 16px 16px;
}
.markdown-output h1,
.markdown-output h2,
.markdown-output h3,
.markdown-output h4 {
  line-height: normal;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  color: var(--main-color-9);
  margin: 0 0 16px 0;
}
.markdown-output blockquote {
  margin: 12px 24px 8px;
  padding: 0 12px;
  border-left: 5px solid var(--main-color-3);
}
.markdown-output p,
.markdown-output ul {
  margin: 0 0 1em;
}
.markdown-output h1:last-child,
.markdown-output h2:last-child,
.markdown-output h3:last-child,
.markdown-output h4:last-child,
.markdown-output p:last-child,
.markdown-output ul:last-child {
  margin: 0;
}
.markdown-output pre ~ p,
.markdown-output pre ~ p:last-child {
  margin: 1em 0 0 0;
}
.markdown-output ul,
.markdown-output ol {
  padding-left: 28px;
}
.markdown-output ul {
  list-style: disc;
}
.markdown-output ol {
  list-style: decimal;
}
.markdown-output code {
  padding: 1px 5px;
  background-color: var(--main-color-1);
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
  font-size: 13px;
  line-height: 18px;
  font-feature-settings: "liga" 0, "calt" 0;
}
.markdown-output pre {
  background: var(--main-color-1);
  width: 100%;
  overflow-x: auto;
}
.markdown-output img {
  max-width: 100%;
}
.comments {
  position: relative;
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
}
.comments:not(.comments--full-screen) {
  background-color: #fff1ce;
  width: 500px;
  border-left: 1px solid var(--main-color-3);
}
.comments:not(.comments--full-screen) .comment {
  border-top-color: var(--main-color-0);
}
.comments:not(.comments--full-screen)::after {
  content: " ";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 4px;
  height: 1px;
  background-color: var(--main-color-3);
}
.comments.comments--full-screen .comment {
  border-top-color: var(--main-color-3);
}
.comments__form,
.comments .comment {
  padding: 16px;
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.comments__form .avatar {
  min-width: 24px;
}
.comments__form__input {
  display: flex;
  align-items: baseline;
}
.comments__form__input textarea {
  padding: 6px;
  width: 100%;
  height: 32px;
  min-height: 32px;
  resize: none;
  overflow-y: hidden;
}
.comments__form__actions {
  display: flex;
  align-items: center;
}
.comments__form__actions--key-helper {
  color: var(--main-color-0);
  margin: 0 8px 0;
  font-weight: 400;
}
.comments__form__actions .button + .button {
  margin-left: 8px;
}
.comments__unauth {
  display: flex;
  align-items: center;
  justify-content: center;
}
.comments .comment {
  color: var(--main-color-9);
  border-top: 1px solid;
}
.comments .comment__header {
  display: grid;
  grid-template-columns: 24px auto 1fr 16px;
  gap: 8px;
  align-items: center;
}
.comments .comment__author {
  font-weight: bold;
  font-size: 12px;
  line-height: 16px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
.comments .comment__date {
  flex: 1;
  color: var(--main-color-8);
}
.comments .comment__content {
  position: relative;
  box-sizing: border-box;
  white-space: pre-wrap;
  word-break: break-word;
  font-size: 12px;
  line-height: 16px;
}
.comments .comment__content > p {
  margin: 0;
  padding: 0;
}
.comments .comment__actions {
  display: flex;
  align-items: center;
}
.comments .comment__actions__delete {
  display: flex;
  align-items: center;
  opacity: .5;
  cursor: pointer;
}
.comments .comment__actions__delete > use {
  fill: var(--main-color-6);
}
.comments .comment__actions__delete:hover {
  opacity: 1;
}
.embed-code_header h2 {
  display: flex;
  min-width: 0;
  margin: 0;
  font-size: 16px;
  line-height: 24px;
  font-weight: 700;
}
.embed-code_content {
  position: relative;
  padding: 24px 24px 24px 24px;
}
.embed-code_content > div:not(:last-child) {
  margin-bottom: 12px;
}
.embed-code_error {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  box-sizing: border-box;
  height: 160px;
  padding: 8px;
  border: 1px solid var(--main-color-2);
  color: var(--main-color-4);
  white-space: pre;
  text-align: center;
}
body.page-embed .embed {
  display: flex;
  flex-direction: column;
  max-height: 100%;
  min-height: 100%;
}
body.page-embed .embed_content {
  display: flex;
  flex: 1;
  overflow: auto;
}
body.page-embed .embed_footer {
  display: flex;
  gap: 12px;
  align-items: center;
  height: 32px;
  padding: 0 8px;
  margin: 12px 0 0 0;
  border-bottom-left-radius: 4px;
  border-bottom-right-radius: 4px;
  background-color: var(--main-color-1);
}
body.page-embed .embed_footer > div:first-child {
  flex: 1 0;
}
body.page-embed .embed_footer a > span {
  font-weight: 600;
}
body.page-embed .embed_footer a:hover {
  color: var(--main-color-9);
}
body.page-embed .embed_logo {
  width: 22px;
  height: 22px;
  background-image: url('/logo/RGB/Logo-RGB.svg');
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
}
.print-page {
  -webkit-print-color-adjust: exact;
  color-adjust: exact;
  overflow: visible;
  height: auto;
}
@page {
  size: portrait;
}
.print-page .static-editor {
  page-break-inside: avoid;
}
.print-page .block {
  margin-bottom: 12px;
}
.notebook_content .datalore-sheet:not(:first-child) {
  margin: 20px 0 0 0;
}
.notebook_content .datalore-sheet_title {
  margin: 0 0 16px 0;
  color: var(--main-color-8);
  border-bottom: 1px solid var(--border-color);
  opacity: .7;
  font-size: 14px;
  line-height: 20px;
  font-weight: 600;
  color: var(--main-color-9);
}
.notebook_content .datalore-block-output {
  padding: 0;
  overflow: hidden;
}
.notebook_content .datalore-block-output > div:not(.block-output-empty):not(.edge) {
  padding: 8px 16px;
  overflow: auto;
}
.notebook_content .datalore-error {
  display: flex;
  flex-direction: column;
}
.notebook {
  width: 802px;
  margin: 0 auto;
  padding: 0 32px;
  flex-grow: 1;
}
.notebook_content {
  display: flex;
  flex-grow: 1;
  padding: 20px 0 0 0;
}
.notebook_content > div {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}
.notebook_sidebar .badge {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background-color: var(--main-color-1);
  box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.06);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
}
.notebook_sidebar .badge use,
.notebook_sidebar .badge g {
  fill: var(--main-color-6);
}
.notebook_sidebar .badge > a,
.notebook_sidebar .badge > span {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.notebook_sidebar .badge:not(:first-child) {
  margin: 16px 0 0 0;
}
.notebook_sidebar .badge:hover {
  background-color: var(--main-color-2);
}
.notebook_sidebar .badge:hover use,
.notebook_sidebar .badge:hover g {
  fill: var(--main-color-7);
}
.notebook_sidebar .badge:active {
  background-color: var(--main-color-3);
}
.notebook_sidebar .badge:active use,
.notebook_sidebar .badge:active g {
  fill: var(--main-color-8);
}
.notebook .block-output:not(.block-output-empty) + .edge,
.notebook .block-output > div:not(.block-output-empty) + .edge {
  width: 4px;
  height: 1px;
  background-color: var(--main-color-3);
  border: none;
}
.publishing-notebook {
  position: relative;
  display: grid;
  grid-template-rows: max-content auto max-content;
  grid-template-areas: "header" "content" "footer";
  gap: 20px;
  min-height: 100%;
}
.publishing-notebook .wrapper-center {
  width: 802px;
  padding: 0 32px;
  margin: 0 auto;
}
.publishing-notebook_header,
.publishing-notebook_footer {
  background-color: var(--main-color-1);
  padding: 24px 0;
}
.publishing-notebook_header {
  border-bottom: 1px solid var(--main-color-2);
  grid-area: header;
}
.publishing-notebook_header_title {
  margin-bottom: 4px;
  font-size: 24px;
  line-height: 28px;
  font-weight: 700;
  color: var(--main-color-9);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.publishing-notebook_header_sub {
  color: var(--main-color-4);
  margin-bottom: 12px;
}
.publishing-notebook_header_description {
  white-space: pre-wrap;
  word-wrap: break-word;
}
.publishing-notebook_footer {
  grid-area: footer;
}
.publishing-notebook_footer h3 {
  margin-bottom: 0;
  color: var(--main-color-7);
}
.publishing-notebook_content {
  grid-area: content;
  display: flex;
}
.publishing-notebook_sidebar {
  position: fixed;
  right: 24px;
  bottom: 24px;
}
.notebook-page {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  overflow: hidden;
  background-color: var(--primary-bg);
}
.notebook-page_main {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  overflow: auto;
}
.notebook-page .head .head_content-center {
  overflow: hidden;
  min-width: 120px;
}
.notebook-page .head .publishing-actions {
  display: flex;
}
.notebook-page .head .button.type--open {
  margin: 0 6px;
}
.notebook-page__name {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.variable__name,
.variable__type {
  display: inline-block;
  flex-shrink: 0;
}
.variable__repr {
  flex-shrink: 1;
  flex-grow: 1;
  overflow: hidden;
  text-overflow: ellipsis;
}
.variable__name {
  font-weight: bold;
  padding: 0 4px;
}
.variable__type {
  color: var(--main-color-6);
  padding: 0 4px;
}
.variable__loading {
  padding: 0 20px;
  color: var(--main-color-6);
}
.variable .icon-loupe {
  margin: 0 4px;
  display: none;
  cursor: pointer;
  flex-shrink: 0;
}
.variable .icon-loupe use,
.variable .icon-loupe g {
  fill: var(--main-color-7);
}
.variable__head_has_detailed:hover .icon-loupe {
  display: inline-block;
}
.variable__head__has_detailed .variable__repr {
  cursor: pointer;
}
.variable-detailed-view__header {
  display: flex;
  margin-bottom: 16px;
}
.variable-detailed-view__variable {
  font-size: 14px;
  line-height: 20px;
  font-weight: 600;
  color: var(--main-color-9);
}
.variable-detailed-view__type {
  margin-left: 8px;
  font-size: 14px;
  color: var(--main-color-7);
}
.variable-detailed-view__title {
  flex-grow: 1;
}
.variable-detailed-view__bar {
  display: none;
  flex-shrink: 0;
}
.variable-detailed-view__button {
  margin-left: 4px;
}
.variable-detailed-view_dialog.popup {
  padding: 12px;
  width: 540px;
}
.variable-detailed-view_dialog .variable-detailed-view__bar {
  display: block;
}
.variable-group__name {
  font-weight: bold;
  padding: 0 4px;
  color: var(--main-color-6);
}
.variable-toggleable__top {
  padding: 6px 0;
  display: flex;
  align-items: center;
}
.variable-toggleable__head {
  display: flex;
  align-items: center;
  flex-grow: 1;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
.variable-toggleable__content {
  padding-left: 18px;
  display: none;
}
.variable-toggleable.expanded > .variable-toggleable__content {
  display: block;
}
.variable-toggleable.expanded > .variable-toggleable__top .icon-flyout {
  transform: initial;
}
.variable-toggleable .icon-flyout {
  display: inline-block;
  flex-shrink: 0;
  cursor: pointer;
  user-select: none;
  opacity: .5;
  transition: transform 0.1s ease-in-out, opacity 0.2s ease-out;
  transform: rotate(-90deg);
}
.variable-toggleable .icon-flyout:hover {
  opacity: .8;
}
.vars-container {
  height: 100%;
  overflow: auto;
}
.vars-viewer {
  height: 100%;
  box-sizing: border-box;
  padding-top: 16px;
  background: var(--primary-bg);
}
.vars-viewer_vars {
  font-family: 'JetBrains Mono', Menlo, Consolas, monospace;
}
.vars-viewer_empty {
  padding: 40px 20px;
  color: var(--main-color-8);
  font-size: 14px;
  white-space: initial;
  text-align: center;
}
.dl-applicationsList_container {
  display: flex;
  flex-direction: column;
}
.dl-applicationsList_addApplication {
  align-self: flex-end;
  cursor: pointer;
  color: var(--primary-bg);
  background-color: var(--action-color);
  padding: 5px;
  margin: 10px 20px;
}
.dl-applicationsList_item,
.dl-applicationsList_header,
.dl-applicationsList_noApps {
  display: flex;
  justify-content: flex-start;
  height: 30px;
  border-bottom: 1px solid #e5e5e5;
  align-items: center;
}
.dl-applicationsList_header {
  font-weight: bolder;
}
.dl-applicationsList_noApps {
  justify-content: center;
}
.dl-applicationsList_itemName {
  flex-basis: 40%;
}
.dl-applicationsList_itemAction {
  flex-basis: 30px;
  cursor: pointer;
}
.dl-applicationsList_itemAction.icon:hover use,
.dl-applicationsList_itemAction.icon:hover g {
  fill: var(--action-color);
}
.dl-application {
  display: flex;
  flex-direction: column;
  height: 100%;
  background-color: var(--main-color-1);
}
.dl-application_header {
  flex-basis: 48px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: var(--main-color-8);
}
.dl-application_title {
  color: #fff;
}
.dl-application_title-link {
  margin-left: 5px;
}
.dl-application_title-link .icon use {
  fill: var(--primary-bg);
}
.dl-application_title-input {
  width: 200px;
  background-color: var(--main-color-8);
  text-align: center;
  border: none;
  color: var(--primary-bg);
}
.dl-application_body {
  display: flex;
  justify-content: stretch;
  align-items: stretch;
  height: calc(100% - 48px);
  width: 100%;
  background-color: var(--main-color-1);
}
.dl-application_block-controls {
  padding: 15px 15px 5px;
  height: 40px;
}
.dl-application_control {
  display: inline-block;
  border: 1px solid var(--main-color-3);
  padding: 10px;
  border-radius: 5px;
}
.dl-application_blocks {
  transform-origin: left top;
  width: 1000px;
  transform: scale(0.5);
  height: calc(200% - 60px / 0.5);
  overflow-y: auto;
}
.dl-application_canvas-wrapper {
  flex-basis: calc(100% - 500px);
  margin-left: -500px;
  position: relative;
  background-color: var(--main-color-2);
  box-shadow: 0 0 4px var(--main-color-6);
}
.dl-application_canvas {
  position: relative;
  width: 100%;
  height: 100%;
  overflow: auto;
}
.dl-application_remove-application {
  display: inline-block;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid;
  margin: 0 0 0 15px;
  cursor: pointer;
}
.dl-application_close-builder {
  display: inline-block;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid;
  margin: 0 0 0 15px;
  cursor: pointer;
}
.dl-application_grid {
  background-color: var(--main-color-2);
  width: calc(100% - 32px);
  height: calc(100% - 32px);
  padding: 32px 0 0 32px;
  background-position: 32px 32px;
  background-clip: content-box;
  background-attachment: local;
}
.dl-application_grid__small {
  background-image: url("/assets/bg/gridSmall.svg");
}
.dl-application_worksheet {
  display: flex;
  flex-direction: column;
  border-top: 1px solid #C4C4C4;
  margin: 12px 24px 24px;
  padding: 8px;
}
.dl-application_worksheet_name {
  font-size: 24px;
  line-height: 28px;
  color: black;
}
.dl-application_worksheet_container {
  display: flex;
  justify-content: flex-start;
}
.dl-application_content {
  max-width: 440px;
  width: 440px;
  display: inline-block;
  margin-right: 48px;
}
.dl-application_mixed-content {
  max-width: 900px;
  width: 900px;
  display: inline-block;
  margin-right: 48px;
}
.dl-application-block {
  position: relative;
  box-shadow: 0 0 4px rgba(0, 0, 0, 0.25);
  margin: 16px 0;
}
.dl-application-block_code {
  margin: 5px 0;
  background-color: var(--primary-bg);
  overflow-x: auto;
}
.dl-application-block_output {
  margin: 5px 0;
  background-color: var(--primary-bg);
  overflow-x: auto;
}
.dl-application-block_overlay {
  width: 100%;
  height: 100%;
  top: 0px;
  left: 0px;
  z-index: 1;
  position: absolute;
}
.dl-application-block_overlay_actions {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.dl-application-block_overlay_actions__hidden {
  display: none;
}
.dl-application-block_overlay__disabled {
  background-color: rgba(200, 200, 200, 0.25);
}
.dl-application-block_overlay__disabled:hover {
  background-color: rgba(200, 200, 200, 0.25);
}
.dl-application-block_overlay:hover {
  background-color: rgba(0, 104, 142, 0.25);
}
.dl-application-block_action {
  width: 72px;
  height: 72px;
  border-radius: 36px;
  cursor: pointer;
  transform: scale(2);
  margin: 20px;
}
.dl-application-block_action__preview {
  background-repeat: no-repeat;
  background-position: center;
  background-image: url("/assets/icon/preview.svg?v=0.2");
}
.dl-application-block_action__add {
  background-repeat: no-repeat;
  background-position: center;
  background-image: url("/assets/icon/add-blue.svg?v=0.2");
}
.dl-application-block-view {
  position: absolute;
  border: 2px solid var(--main-color-2);
  z-index: 0;
  border-radius: 5px 0 5px 5px;
  box-sizing: border-box;
  min-width: 100px;
}
.dl-application-block-view__immutable {
  border-radius: 5px;
}
.dl-application-block-view__active {
  z-index: 1;
}
.dl-application-block-view__outlined {
  border-color: var(--action-color-2);
}
.dl-application-block-view_code {
  background-color: var(--primary-bg);
  height: 100%;
}
.dl-application-block-view_overlay {
  background-color: transparent;
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
}
.dl-application-block-view_controls {
  position: absolute;
  top: -33px;
  right: -2px;
  background-color: var(--primary-bg);
  border: 2px solid var(--action-color-2);
  border-bottom: 0 solid var(--primary-bg);
  border-radius: 5px 5px 0 0;
}
.dl-application-block-view_remove {
  margin: 6px;
}
.dl-application-block-view_resize {
  position: absolute;
  width: 16px;
  height: 16px;
  background-color: transparent;
  right: 0;
  bottom: 0;
}
.dl-library {
  position: relative;
  outline: none;
  height: 100%;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
}
.dl-library_content {
  flex: 1 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  margin-top: 5px;
}
.library-info {
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}
.library-info_select {
  margin-left: 26px;
  margin-right: 14px;
  user-select: none;
  display: none;
}
.library-info .show-select {
  display: inline-block;
}
.library-info .is-action {
  display: none;
}
.library-info[data-status=CAN_REMOVE] .is-action.action-remove {
  display: inline-block;
}
.library-info[data-status=CAN_INSTALL] .is-action.action-install {
  display: inline-block;
}
.library-info[data-status=CAN_UPDATE] .is-action.action-update {
  display: inline-block;
}
.library-info_head {
  white-space: nowrap;
  display: flex;
  justify-content: space-between;
  margin-bottom: 18px;
  padding-bottom: 11px;
  border-bottom: 1px solid #e5e5e5;
}
.library-info_head .button {
  margin: 0;
}
.library-info_name {
  font-weight: bold;
  font-size: 2em;
  flex-grow: 1;
  overflow: hidden;
  text-overflow: ellipsis;
}
.library-info_description {
  flex: 1 0;
  overflow: auto;
}
.library-info_description ul,
.library-info_description ol {
  padding-left: 28px;
}
.library-info_description ul {
  list-style: disc;
}
.library-info_description ol {
  list-style: decimal;
}
.library-info .dl-library-report {
  margin-bottom: 20px;
}
.dl-library-item {
  height: 32px;
  border: 1px solid transparent;
  border-top-color: var(--main-color-1);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.dl-library-item:hover {
  background: var(--main-color-1);
}
.dl-library-item:last-child {
  border-bottom-color: var(--main-color-1);
}
.dl-library-item_status {
  display: inline-block;
  margin: 0 7px;
  opacity: 0.7;
}
.dl-library-item_name {
  font-weight: bold;
}
.dl-library-item_version,
.dl-library-item_source {
  color: var(--main-color-7);
  overflow: hidden;
  white-space: nowrap;
}
.dl-library-item_version:not(:empty)::before {
  color: var(--main-color-7);
  display: inline-block;
  content: '@';
  text-align: center;
  padding-left: 2px;
  padding-right: 2px;
}
.dl-library-item_action {
  visibility: hidden;
  vertical-align: middle;
  padding: 0 4px;
}
.dl-library-item_enabled.dl-library-item:hover .dl-library-item_action {
  visibility: visible;
}
.dl-library-repository-key {
  border: 1px solid var(--border-color);
  border-radius: 2px;
  padding: 16px;
  padding-left: 104px;
  margin: 8px 0;
  background-position: center;
  background-image: url("/assets/icon/key.svg?v=0.2");
  background-repeat: no-repeat;
  background-position: 16px;
}
.dl-library-repository-key:hover {
  border-color: var(--action-color);
}
.dl-library-repository-key.selected {
  border-color: var(--action-color-3);
}
.dl-library-repository-key_name,
.dl-library-repository-key_user,
.dl-library-repository-key_host,
.dl-library-repository-key_title {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.dl-library-repository-key_title {
  font-weight: initial;
}
.dl-library-repository-key-dialog_label {
  margin: 20px 1px 8px;
  color: var(--main-color-7);
}
.dl-library-repository-key-dialog_section:first-child .dl-library-repository-key-dialog_label {
  margin-top: 10px;
}
.dl-library-repository-key-dialog_host,
.dl-library-repository-key-dialog_user,
.dl-library-repository-key-dialog_title {
  width: 100%;
}
.dl-library-repository-key-dialog_key {
  min-width: 350px;
  min-height: 150px;
}
.dl-library-repository-key-dialog_bar {
  margin-top: 20px;
  text-align: right;
}
.dl-library-repository-keys {
  height: 100%;
  display: flex;
  flex-direction: column;
}
.dl-library-repository-keys_head {
  margin-bottom: 12px;
  flex-shrink: 0;
  clear: both;
}
.dl-library-repository-keys_head-left {
  float: left;
}
.dl-library-repository-keys_head-left .button {
  min-width: 200px;
}
.dl-library-repository-keys_head-right {
  float: right;
}
.dl-library-repository-keys_list {
  box-sizing: border-box;
  height: 100%;
  overflow: auto;
}
.dl-library-repository-keys_content {
  flex-grow: 1;
  box-sizing: border-box;
  height: 100%;
  min-height: 0%;
}
.dl-library-repository-keys_subtitle {
  font-size: 14px;
  font-weight: initial;
  margin-bottom: 6px;
}
.dl-library-repository-keys_line {
  margin: 22px 0;
  border-bottom: 1px solid var(--border-color);
}
.dl-library-public-key-dialog_label {
  margin: 10px 1px 8px;
  color: var(--main-color-7);
}
.dl-library-public-key-dialog_key {
  min-width: 350px;
  min-height: 150px;
}
.dl-library-report_status {
  padding: 10px 15px;
  color: var(--main-color-9);
}
.dl-library-report_status__success {
  background: var(--positive-color-1);
}
.dl-library-report_status__failure {
  background: var(--negative-color-1);
}
.dl-library-report_text {
  background: var(--main-color-9);
  color: var(--primary-bg);
  box-sizing: border-box;
  height: 200px;
  padding: 20px;
  overflow: auto;
  white-space: pre-wrap;
  word-break: break-word;
}
.dl-library-repositories {
  height: 100%;
  display: flex;
  flex-direction: column;
  padding: 10px;
  box-sizing: border-box;
}
.dl-library-repositories_head {
  margin-bottom: 12px;
  flex-shrink: 0;
  clear: both;
}
.dl-library-repositories_head-left {
  float: left;
}
.dl-library-repositories_head-right {
  float: right;
}
.dl-library-repositories_list {
  box-sizing: border-box;
  height: 100%;
  overflow: auto;
}
.dl-library-repositories_content {
  flex-grow: 1;
  box-sizing: border-box;
  min-height: 0%;
}
.dl-library-repository {
  height: 32px;
  line-height: 32px;
  border-top: 1px solid var(--main-color-1);
  padding: 0 2px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.dl-library-repository:hover {
  background: var(--main-color-1);
}
.dl-library-repository:last-child {
  border-bottom: 1px solid var(--main-color-1);
}
.dl-library-repository.selected {
  background: var(--main-color-8);
  color: var(--primary-bg);
}
.dl-library-repository_name,
.dl-library-repository .icon,
.dl-library-repository .spinner {
  vertical-align: middle;
}
.dl-library-repository_name {
  padding-right: 16px;
}
.dl-library-repository-dialog {
  width: 300px;
  overflow: visible;
}
.dl-library-repository-dialog_title {
  font: 21px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  text-align: center;
}
.dl-library-repository-dialog_error {
  min-height: 28px;
  margin-top: 4px;
  color: var(--negative-color-2);
  text-align: center;
}
.dl-library-repository-dialog_content {
  margin-top: 20px;
}
.dl-library-repository-dialog_url {
  margin: 12px 0px;
  width: 100%;
}
.dl-library-repository-dialog .select {
  width: 100%;
  margin-top: 12px;
}
.dl-library-repository-dialog_bar {
  display: flex;
  justify-content: flex-end;
}
.dl-library-repository-dialog .spinner {
  width: 12px;
  height: 12px;
}
.pckg-mngr-status {
  color: var(--main-color-5);
  margin: 8px 0;
}
.pckg-mngr-init-sh {
  color: var(--main-color-5);
  margin: 8px 0 16px 0;
}
.pckg-mngr-second-title {
  font-size: 12px;
  line-height: 16px;
  font-weight: 600;
  color: var(--main-color-9);
  margin: 0;
}
.loading-content {
  position: relative;
  width: 100%;
  height: 100%;
}
.secret-list.secret-list-vertical,
.secret-list .secret-list_item {
  margin-bottom: 12px;
}
.secret-list.secret-list-vertical {
  max-height: 384px;
  overflow-y: auto;
}
.secret-list_item {
  display: grid;
  min-height: 138px;
  padding: 16px;
  border: 1px solid var(--main-color-2);
  border-radius: 2px;
  cursor: pointer;
  -webkit-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  -moz-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  transition: transform 100ms ease-out, box-shadow 100ms ease-out;
}
.secret-list_item_kind {
  font-size: smaller;
}
.secret-list_item_entries {
  font-style: italic;
}
.secret-list_item_name {
  font-weight: bold;
  display: flex;
}
.secret-list_item_name svg use {
  fill: var(--main-color-5);
}
.secret-list_item_name svg {
  padding-right: 8px;
}
.secret-list_item_controls {
  text-align: right;
}
.secret-list_item_description {
  word-break: break-word;
}
.secret-list_item_menu {
  width: 16px;
  height: 16px;
  display: inline-block;
  align-items: center;
  justify-content: center;
  padding: 8px;
  margin-right: -8px;
  cursor: pointer;
}
.secret-list_item_menu .icon > use {
  transition: fill 200ms ease-in;
  fill: var(--main-color-5);
}
.secret-list_item_menu .icon:hover > use {
  fill: var(--main-color-8);
}
.secret-list_item:not(.renamed):hover {
  transform: translateY(-2px);
  -webkit-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
}
.secret-list_item.highlighted {
  transform: none;
  animation: highlight 2s ease-out;
}
.secret-list_item:not(.renamed):active {
  transform: none;
  -webkit-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  -moz-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
}
.secret-list_item > div {
  padding: 8px 0 8px 0;
}
.secret-list_item > div:first-child {
  padding: 0 0 8px 0;
  border-bottom: 1px solid var(--main-color-2);
}
.secret-list_item > div:last-child {
  padding: 0;
}
.secret-list-grid {
  padding: 8px;
  display: grid;
  grid-gap: 32px;
  grid-auto-flow: dense;
  grid-auto-columns: max-content;
  grid-auto-rows: minmax(100px, auto);
  grid-template-columns: repeat(3, minmax(230px, 1fr));
}
.secret-list-grid .secret-list_item {
  grid-template-rows: 40px 1fr 24px;
}
.secret-list-vertical .secret-list_item {
  padding: 8px 12px;
  min-height: 0;
  grid-template-columns: 2fr 4fr 1fr;
}
.secret-list-vertical .secret-list_item > div {
  padding: 0;
}
.secret-list-vertical .secret-list_item > div:first-child {
  padding: 0;
  border-bottom: none;
}
.secret-list-vertical p {
  white-space: normal;
}
.secret-controls {
  margin: 24px 0;
  text-align: right;
  display: flex;
  justify-content: flex-end;
}
.secret-controls .dl-button {
  width: auto;
}
.secret-controls > .list-button {
  width: 160px;
  margin-right: 10px;
}
.secret-controls_add_secret svg use {
  fill: var(--primary-bg);
}
.secret-restart-disclaimer {
  background-color: var(--attention-color-1);
  white-space: normal;
  padding: 14px;
}
.secret-select-element-create {
  font-weight: bold;
}
.delete-secret-dialog_bar {
  margin: 12px 0 0 0;
  text-align: right;
}
.delete-secret-dialog_bar .dl-button {
  width: auto;
}
.delete-secret-dialog_bar .dl-button:first-child {
  margin-right: 12px;
}
.edit-secret-dialog_bar {
  margin: 12px 0 0 0;
  text-align: right;
}
.edit-secret-dialog_bar .dl-button {
  width: auto;
  margin-left: 2px;
}
.edit-secret-dialog_bar .dl-button:first-child {
  margin-right: 12px;
}
.edit-secret-dialog_section {
  padding-bottom: 12px;
}
.edit-secret-dialog_text {
  height: 515px;
  overflow-y: auto;
}
.edit-secret-dialog_text_input {
  width: 100%;
}
.edit-secret-dialog_text_input_invalid {
  background-color: var(--negative-color-1);
}
.edit-secret-dialog_description_text {
  width: 100%;
  min-height: 120px;
}
.edit-secret-dialog_entry > div {
  display: grid;
  grid-template-columns: 1fr 1fr 32px;
  padding-bottom: 6px;
}
.edit-secret-dialog_entry > div > div {
  padding-right: 12px;
}
.diff-editor {
  display: grid;
  grid-template-rows: auto auto 1fr;
  height: 100%;
  background: var(--main-color-1);
  outline: none;
}
.diff-editor_actions {
  margin: 0 5px;
  user-select: none;
}
.diff-editor_action {
  cursor: pointer;
  vertical-align: middle;
  margin: 4px;
}
.diff-editor_action.checkbox {
  display: inline-flex;
}
.diff-editor_titles {
  margin: 8px 55px 0 10px;
  color: var(--main-color-7);
}
.diff-editor_title {
  overflow: hidden;
  text-overflow: ellipsis;
  margin: 2px;
}
.diff-editor_side-by-side {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.diff-editor_blocks {
  padding: 0 10px;
  overflow-y: scroll;
}
.diff-editor_block {
  padding-bottom: 10px;
}
.cr-history .cropped-text {
  text-overflow: ellipsis;
  overflow: hidden;
}
.cr-history .non-selectable {
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.cr-history .icon_control {
  padding: 0;
  border: none;
  outline: none;
  cursor: pointer;
}
.cr-history-item-container:hover,
.cr-history-item-container.selected {
  background-color: var(--main-color-1);
}
.cr-history-user-checkpoint {
  font-weight: 400;
}
.cr-history-controls {
  display: flex;
  justify-content: space-between;
}
.cr-history_popup {
  width: 95%;
  height: 95%;
}
.cr-history-container {
  background: var(--main-color-1);
}
.cr-history-container .overlay {
  opacity: 0.7;
  overflow: hidden;
  z-index: 2;
}
.cr-history-container.popup_content {
  padding: 0;
}
.cr-history-content {
  position: relative;
  box-sizing: border-box;
  height: 100%;
  overflow: hidden;
}
.cr-history-control-item {
  cursor: pointer;
  color: var(--main-color-7);
}
.cr-history-control-item:hover {
  color: var(--action-color);
}
.cr-history-container-child {
  display: flex;
  align-content: stretch;
  overflow: hidden;
  width: 100%;
  height: 100%;
}
.cr-history-checkpoints-panel {
  flex: 0 1 auto;
  position: relative;
  border-right: 1px solid var(--border-color);
  display: flex;
  align-content: flex-start;
  background: var(--primary-bg);
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.cr-history-checkpoints-toggler {
  position: absolute;
  box-sizing: border-box;
  top: 50%;
  height: 60px;
  margin-top: -30px;
  right: -10px;
  width: 10px;
  padding: 20px 0 10px;
  background: var(--primary-bg);
  border: 1px solid var(--main-color-2);
  border-left: 1px solid var(--primary-bg);
  color: rgba(0, 0, 0, 0.2);
  border-radius: 0 5px 5px 0;
  box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.3);
  z-index: 1000;
  cursor: pointer;
}
.cr-history-checkpoints-list {
  width: 220px;
  height: 100%;
  padding: 8px 0;
  overflow-y: auto;
  outline: none;
  box-sizing: border-box;
}
.cr-history-preview-area {
  position: relative;
  flex: 1 1 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}
.cr-history-preview-container {
  height: 100%;
  width: 100%;
  overflow: hidden;
}
.cr-history-diff-area {
  height: 100%;
  width: 100%;
}
.cr-history-checkpoint-item {
  cursor: pointer;
  white-space: nowrap;
  padding: 5px;
}
.cr-history-checkpoint-message {
  font-size: 14px;
  text-overflow: ellipsis;
  overflow: hidden;
}
.cr-history-checkpoint-author {
  color: var(--main-color-6);
  text-overflow: ellipsis;
  overflow: hidden;
}
.cr-history-checkpoint-time {
  color: var(--main-color-5);
  text-overflow: ellipsis;
  overflow: hidden;
}
.cr-permanent-alert_items {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  background-color: var(--permanent-alert-bg, var(--attention-color-2));
}
.cr-permanent-alert_item {
  display: flex;
  flex-grow: 1;
  align-items: center;
  justify-content: space-between;
  height: 54px;
  border-bottom: var(--main-color-8) 1px solid;
  padding-left: 10px;
  padding-right: 10px;
}
.cr-permanent-alert_item .popup_close {
  position: relative;
  display: flex;
  right: 0;
  top: 0;
  padding-left: 10px;
  color: var(--main-color-8);
}
.cr-permanent-alert_item .popup_close:hover {
  color: var(--main-color-9);
}
.cr-permanent-alert_item_content {
  flex-grow: 1;
}
.cr-permanent-alert_content {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.cr-permanent-alert_content .button {
  width: auto;
}
.cr-permanent-alert_content .button:hover {
  background-color: var(--attention-color-3);
}
.cr-permanent-alert_content .button[disabled]:hover {
  background-color: transparent;
}
.fs-promo {
  position: relative;
  padding: 8px 40px;
  background: linear-gradient(90.03deg, #0078A4 12.9%, #0F536C 71.5%);
}
.fs-promo_content {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 790px;
  margin: 0 auto;
  color: var(--main-color-0);
}
.fs-promo_content .button {
  margin-left: 24px;
}
.fs-promo .icon-close {
  position: absolute;
  top: 16px;
  right: 16px;
  cursor: pointer;
}
.fs-promo .icon-close use,
.fs-promo .icon-close g {
  fill: var(--main-color-0);
}
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  font-size: 12px;
  font-weight: normal;
  color: var(--main-color-9);
}
.actions_bar,
.simple-alert_bar {
  display: flex;
  justify-content: flex-end;
}
.actions_bar > button,
.simple-alert_bar > button,
.actions_bar > .button,
.simple-alert_bar > .button {
  width: auto;
}
.header_icon {
  width: 32px;
  height: 32px;
  margin-right: 8px;
}
.header_main {
  width: 100%;
  display: grid;
  grid-template-columns: auto 1fr auto;
  align-items: center;
}
.header_main .dl-select_title-text {
  font-size: 24px;
  line-height: 28px;
  font-weight: 700;
  color: var(--main-color-9);
}
.header_main .dl-select_title .dl-select_button,
.header_main .dl-select_title .dl-select_button > .icon {
  width: 28px;
  height: 28px;
  justify-content: center;
  border-radius: 2px;
}
.header_main .dl-select_title .header-select-item_text {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.header_main .header-select-item {
  width: 100%;
  display: grid;
  align-items: center;
  grid-template-columns: 24px auto 16px;
}
.header_main .header-select-item_text {
  line-height: 16px;
  flex: 1;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.header_main .header-select-item_text:not(:last-child) {
  padding-right: 12px;
}
.header_main .header-select-item > .icon {
  background-color: transparent;
}
.header_main .header-select_action {
  height: 32px;
  display: flex;
  align-items: center;
  padding: 0 0 0 12px;
  transition: background-color 200ms ease-in, color 200ms ease-in;
}
.header_main .header-select_action:hover {
  background-color: var(--main-color-1);
}
.header_main .header-select_action .icon {
  margin-right: 8px;
}
.header_actions {
  text-align: right;
}
.dl-layout {
  display: grid;
  grid-template-columns: 244px 1fr;
  grid-template-rows: 64px 1fr;
  grid-template-areas: "header header" "aside main";
  width: 100%;
  height: 100%;
  max-height: 100%;
  overflow: hidden;
}
.dl-header {
  grid-area: header;
  display: flex;
  align-items: center;
  z-index: 100;
  border-bottom: 1px solid var(--main-color-2);
  -webkit-box-shadow: 0px 8px 8px 0px var(--primary-bg);
  -moz-box-shadow: 0px 8px 8px 0px var(--primary-bg);
  box-shadow: 0px 8px 8px 0px var(--primary-bg);
}
.dl-aside {
  grid-area: aside;
}
.dl-aside_actions {
  margin: 38px 0 0 0;
}
.dl-aside_separator {
  margin: 12px 0;
  border-top: 1px solid var(--main-color-2);
}
.dl-header {
  margin: 0 64px 0 64px;
}
.dl-aside {
  padding: 20px 0 0 64px;
}
.dl-main-wrapper {
  grid-area: main;
  overflow: auto;
  padding: 20px 64px 0 48px;
}
.dl-main {
  display: grid;
  grid-template-rows: 32px 20px 1fr;
  grid-template-areas: "page-title" "page-sub" "page-content";
  min-height: 100%;
}
.dl-main .dl-page-title {
  align-items: center;
  grid-area: page-title;
}
.dl-main .dl-page-sub {
  display: flex;
  align-items: center;
  grid-area: page-sub;
}
.dl-main .dl-page-content {
  grid-area: page-content;
}
.create-workspace-dialog {
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  margin: 0 auto;
  max-width: 820px;
  overflow: hidden;
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
}
.create-workspace-dialog_header {
  margin: 32px 0 24px;
  font-weight: bold;
  font-size: 20px;
  line-height: 24px;
  font-weight: 700;
  color: var(--main-color-9);
}
.create-workspace-dialog_separator {
  display: block;
  width: 100%;
  margin: 28px 0 14px;
  border-bottom: 1px solid var(--border-color);
}
.create-workspace-dialog .input {
  width: 100%;
}
.create-workspace-dialog_bar {
  text-align: right;
}
.breadcrumbs {
  display: flex;
  align-items: center;
}
.breadcrumbs .icon,
.breadcrumbs .breadcrumb {
  vertical-align: middle;
  transition: opacity 100ms ease-in;
}
.breadcrumbs .icon:hover,
.breadcrumbs .breadcrumb:hover {
  opacity: 1;
}
.breadcrumbs .icon {
  cursor: default;
}
.breadcrumbs .icon use,
.breadcrumbs .icon g {
  fill: var(--main-color-5);
}
.breadcrumbs a.breadcrumb-link {
  color: var(--main-color-8);
}
.breadcrumbs a.breadcrumb-link:hover {
  border-bottom-color: var(--main-color-8);
}
.breadcrumbs .breadcrumb:not(:hover):not(:last-child) {
  opacity: .5;
}
a.file-wrap:hover {
  border-bottom-color: transparent;
}
.file {
  min-width: 100%;
  box-sizing: border-box;
  overflow: hidden;
  word-break: break-word;
  user-select: none;
  color: var(--main-color-8);
}
.file.selected {
  background-color: var(--main-color-1);
}
.file.cut {
  opacity: .7;
}
.file.renamed {
  background-color: var(--primary-bg);
}
.file > div {
  display: flex;
  align-items: center;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.file .file-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 8px;
}
.file_date {
  flex: 1;
  white-space: initial;
}
.file_author {
  flex: 1;
}
.file_running {
  margin-left: 8px;
  font-style: italic;
  color: var(--main-color-6);
}
.files-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  width: 16px;
  height: 16px;
}
.files-empty {
  height: 10rem;
}
.files-list > .files-header {
  border-bottom-color: var(--main-color-2);
}
.files-list > .files-content .file {
  border-bottom: 1px solid var(--main-color-2);
  height: 48px;
  display: grid;
  align-items: stretch;
  grid-template-columns: 30% 20% auto 32px;
  transition: transform 100ms ease-out, box-shadow 100ms ease-out;
}
.files-list > .files-content .file:not(.renamed):hover {
  transform: translateY(-2px);
  -webkit-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
}
.files-list > .files-content .file.highlighted {
  transform: none;
  animation: highlight 2s ease-out;
}
.files-list > .files-content .file:not(.renamed):active {
  transform: none;
  box-shadow: none;
}
.files-list > .files-content .file > div {
  padding: 12px 8px 12px 8px;
}
.files-list > .files-content .file_with-access-level {
  grid-template-columns: 30% 15% 20% auto 32px;
}
.files-tiles > .files-header > :first-child {
  grid-column: 1 / 4;
}
.files-tiles > .files-header > div {
  padding: 0;
}
.files-tiles > .files-content {
  padding-top: 22px;
  display: grid;
  grid-gap: 32px;
  grid-auto-flow: dense;
  grid-auto-columns: max-content;
  grid-auto-rows: minmax(100px, auto);
  grid-template-columns: repeat(3, minmax(230px, 1fr));
}
.files-tiles > .files-content .file {
  display: grid;
  grid-template-rows: 40px 1fr 1fr;
  min-height: 138px;
  padding: 16px;
  border: 1px solid var(--main-color-2);
  border-radius: 2px;
  cursor: pointer;
  -webkit-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  -moz-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  transition: transform 100ms ease-out, box-shadow 100ms ease-out;
}
.files-tiles > .files-content .file:not(.renamed):hover {
  transform: translateY(-2px);
  -webkit-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
}
.files-tiles > .files-content .file.highlighted {
  transform: none;
  animation: highlight 2s ease-out;
}
.files-tiles > .files-content .file:not(.renamed):active {
  transform: none;
  -webkit-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  -moz-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
}
.files-tiles > .files-content .file > div {
  padding: 8px 0 8px 0;
}
.files-tiles > .files-content .file > div:first-child {
  padding: 0 0 8px 0;
  border-bottom: 1px solid var(--main-color-2);
}
.files-tiles > .files-content .file > div:last-child {
  padding: 0;
}
.files-tiles > .files-content .file > div:not(.file_menu):not(.file_author-wrap) {
  grid-column-start: 1;
  grid-column-end: 3;
}
.files-tiles > .files-content .file > .file_author-wrap {
  grid-row-start: 3;
  grid-column-start: 1;
}
.files-tiles > .files-content .file > .file_menu {
  grid-row-start: 3;
  grid-column-start: 2;
  justify-content: flex-end;
}
.files.drop-zone {
  background-color: var(--primary-bg);
}
@keyframes highlight {
  0% {
    box-shadow: 0 0px 8px 0 var(--action-color-3);
  }
  50% {
    box-shadow: 0 0px 8px 0 var(--action-color-2);
  }
  100% {
    box-shadow: none;
  }
}
.files-header {
  height: 48px;
  min-width: 100%;
  top: 0;
  display: grid;
  grid-template-columns: 30% 20% auto 70px;
  border-collapse: collapse;
  align-items: stretch;
  font-weight: 600;
  line-height: 16px;
  cursor: default;
  color: var(--main-color-5);
  border-bottom: 2px solid transparent;
  transition: border-bottom-color 200ms ease-in;
  z-index: 1;
}
.files-header > div {
  display: flex;
  align-items: center;
  padding: 12px 8px 12px 8px;
}
.files-header > :last-child {
  justify-content: flex-end;
  padding: 0;
}
.files-header_with-access-level {
  grid-template-columns: 30% 15% 20% auto 70px;
}
.sort-item {
  display: flex;
  align-items: stretch;
}
.sort-item > .icon {
  margin-left: 8px;
}
.sort-item > .icon.arrow_down {
  transform: rotate(-180deg);
}
.search-page {
  display: flex;
  flex-direction: column;
  padding: 34px 54px;
  overflow: hidden;
}
.search-page_title {
  display: flex;
  align-items: center;
  padding: 0 0 32px 0;
  border-bottom: 1px solid var(--main-color-2);
}
.search-page_title > h2 {
  flex: 1;
}
.search-page_title-light {
  font-weight: normal;
}
.search-page_content {
  overflow-y: auto;
}
.settings-page_main {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.settings-page_footer {
  display: flex;
  justify-content: space-between;
  padding: 16px 0;
  margin: 72px 0 0 0;
  border-top: 1px solid var(--main-color-2);
}
.settings-page_name.input {
  width: 100%;
  max-width: 412px;
}
.drop-notebook-dialog {
  max-width: 380px;
  padding: 16px;
}
.drop-notebook-dialog__text {
  margin: 0 0 8px;
}
.drop-notebook-dialog__footnote {
  margin: 8px 0 24px;
}
.drop-notebook-dialog__bar {
  text-align: right;
  margin-top: 24px;
}
.attached-file-item {
  cursor: pointer;
}
.attached-file-item > div {
  display: flex;
  align-items: center;
}
.attached-file-item__icon {
  justify-content: flex-end;
}
.attached-file-item__menu {
  justify-content: center;
}
.attached-file-item__status {
  font-style: italic;
  color: var(--main-color-5);
  margin-left: 32px;
}
.attached-file-item[disabled] .attached-file-item__name,
.attached-file-item[disabled] .attached-file-item__icon {
  opacity: .5;
}
.dl-page-title {
  display: flex;
}
.attached-files__title {
  flex: 1 0;
}
.attached-files__tools {
  min-width: 200px;
}
.attached-files__header,
.attached-files .attached-file-item {
  display: grid;
  grid-template-columns: 24px 30% 20% auto 32px;
  grid-gap: 8px;
}
.attached-files__header > div:first-child,
.attached-files .attached-file-item__back-folder {
  padding-left: 8px;
  grid-column: 1 / 3;
}
.attached-files.drop-zone {
  background-color: var(--primary-bg);
}
.tokens {
  display: flex;
  flex-direction: column;
  height: 100%;
  padding: 16px;
  box-sizing: border-box;
}
.tokens h3 {
  text-align: center;
}
.tokens_token,
.tokens_head {
  display: grid;
  grid-template-columns: 1fr 200px 200px;
  grid-column-gap: 8px;
  padding: 8px 6px;
}
.tokens_head {
  flex-shrink: 0;
  color: var(--main-color-6);
}
.tokens_content {
  flex-grow: 1;
  overflow: auto;
}
.tokens_token {
  position: relative;
}
.tokens_token .icon-close {
  display: none;
  position: absolute;
  right: 6px;
  top: 10px;
  cursor: pointer;
}
.tokens_token:hover {
  background-color: var(--main-color-1);
}
.tokens_token:hover .icon-close {
  display: block;
}
.tokens_token-date {
  color: var(--main-color-6);
}
.confirm-page {
  display: flex;
  flex-direction: column;
  height: 100%;
  width: 100%;
  overflow: hidden;
  background-color: var(--primary-bg);
}
.confirm-page_content {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
}
.confirm-page_bar {
  margin-top: 32px;
}
.confirm-page_title {
  font-size: 14px;
  line-height: 20px;
  font-weight: 600;
  color: var(--main-color-9);
  margin: 6px 0 12px;
}
.publishing-run-in-datalore {
  height: 100%;
}
.publishing-run-in-datalore_main {
  display: grid;
  width: 100%;
  height: 100%;
  max-height: 100%;
  overflow: hidden;
  align-content: center;
  justify-content: center;
  background-color: var(--primary-bg);
}
.publishing-run-in-datalore_main_container {
  width: 400px;
  text-align: center;
}
.publishing-run-in-datalore_main_message {
  font-size: 17px;
  margin-bottom: 16px;
}
.loading-page {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  top: 0;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr;
  align-content: center;
  z-index: 999;
  background-color: var(--primary-bg);
}
.loading-page__content {
  display: flex;
  flex-direction: column;
  align-self: center;
  align-items: center;
}
.loading-page .logo {
  opacity: 0;
  animation: logo_rolling_up 1s 0.3s cubic-bezier(0.22, 0.74, 0.62, 0.96), logo_opacity 0.5s 0.3s ease-in forwards;
}
.loading-page__title {
  margin-top: 24px;
  font-size: 14px;
  line-height: 20px;
  color: var(--main-color-8);
  color: var(--main-color-5);
  opacity: 0;
  animation: title_opacity 0.3s 1.3s ease-in forwards;
}
@keyframes logo_rolling_up {
  from {
    transform: translate(0, 12px);
  }
  to {
    transform: translate(0, 0);
  }
}
@keyframes logo_opacity {
  0% {
    opacity: 0;
  }
  20% {
    opacity: 0.1;
  }
  100% {
    opacity: 1;
  }
}
@keyframes title_opacity {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
:root {
  --light-main-color-0: #fff;
  --light-main-color-1: #f3f3f3;
  --light-main-color-2: #e5e5e5;
  --light-main-color-3: #c5c5c5;
  --light-main-color-4: #b3b3b3;
  --light-main-color-5: #9e9e9e;
  --light-main-color-6: #848484;
  --light-main-color-7: #616161;
  --light-main-color-8: #474747;
  --light-main-color-9: #171717;
  --light-main-color-10: #000000;
  --dark-main-color-0: #fff;
  --dark-main-color-1: #3c3c3c;
  --dark-main-color-2: #464646;
  --dark-main-color-3: #707070;
  --dark-main-color-4: #777777;
  --dark-main-color-5: #848484;
  --dark-main-color-6: #9e9e9e;
  --dark-main-color-7: #b3b3b3;
  --dark-main-color-8: #b1b1b1;
  --dark-main-color-9: #b2b2b2;
  --dark-main-color-10: #dddddd;
  --action-color-1: #97e1fb;
  --action-color-2: #008dc0;
  --action-color-3: #00688e;
  --main-color-0: var(--light-main-color-0);
  --main-color-1: var(--light-main-color-1);
  --main-color-2: var(--light-main-color-2);
  --main-color-3: var(--light-main-color-3);
  --main-color-4: var(--light-main-color-4);
  --main-color-5: var(--light-main-color-5);
  --main-color-6: var(--light-main-color-6);
  --main-color-7: var(--light-main-color-7);
  --main-color-8: var(--light-main-color-8);
  --main-color-9: var(--light-main-color-9);
  --main-color-10: var(--light-main-color-10);
  --main-color-alfa-2: rgba(229, 229, 229, 0.4);
  --main-color-alfa-8: rgba(71, 71, 71, 0.4);
  --positive-color-1: #b9e1aa;
  --positive-color-2: #369711;
  --positive-color-3: #286f0c;
  --negative-color-1-rgb: 252, 202, 198;
  --negative-color-2-rgb: 245, 61, 44;
  --negative-color-3-rgb: 194, 20, 4;
  --negative-color-1: rgba(var(--negative-color-1-rgb), 1);
  --negative-color-2: rgba(var(--negative-color-2-rgb), 1);
  --negative-color-3: rgba(var(--negative-color-3-rgb), 1);
  --attention-color-1: #fee39d;
  --attention-color-2: #fdba0d;
  --attention-color-3: #e8a800;
  --action-color: var(--action-color-2);
  --border-color: var(--main-color-2);
  --primary-fg: var(--main-color-9);
  --contrast-fg: var(--main-color-0);
  --primary-bg: #ffffff;
  --contrast-bg: var(--main-color-8);
  --pale-bg: var(--main-color-7);
  --tooltip-bg: var(--contrast-bg);
  --tooltip-fg: var(--contrast-fg);
  --popup-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.3);
  --alert-bg: rgba(48, 48, 48, 0.95);
  --traceback-link: blue;
  --tabs-container: transparent;
  --input-output-separator: transparent;
  --editor-bg: #f9f9f9;
  --tile-bg: #f9f9f9;
  --cell-bg: transparent;
  --workbook-bg: var(--primary-bg);
  --vscode-editorSuggestWidget-background: #f3f3f3;
  --vscode-editorSuggestWidget-border: #c8c8c8;
  --vscode-editorSuggestWidget-highlightForeground: #0066bf;
  --vscode-editorSuggestWidget-focusHighlightForeground: #0066bf;
}
:root[theme="idea-old"] {
  --tabs-container: var(--main-color-2);
  --input-output-separator: var(--main-color-1);
  --editor-bg: transparent;
  --cell-bg: var(--primary-bg);
  --workbook-bg: var(--main-color-1);
}
:root[theme="dark"] {
  --tabs-container: transparent;
  --input-output-separator: transparent;
  --editor-bg: var(--primary-bg);
  --tile-bg: var(--primary-bg);
  --cell-bg: transparent;
  --workbook-bg: #3b3b3b;
}
:root[theme="dark-old"] {
  --tabs-container: transparent;
  --input-output-separator: var(--main-color-2);
  --editor-bg: transparent;
  --tile-bg: var(--primary-bg);
  --cell-bg: var(--primary-bg);
  --workbook-bg: #3b3b3b;
}
:root[theme="dark"],
:root[theme="dark-old"] {
  --action-color-1: #97e1fb;
  --action-color-2: #008dc0;
  --action-color-3: #00688e;
  --main-color-0: var(--dark-main-color-0);
  --main-color-1: var(--dark-main-color-1);
  --main-color-2: var(--dark-main-color-2);
  --main-color-3: var(--dark-main-color-3);
  --main-color-4: var(--dark-main-color-4);
  --main-color-5: var(--dark-main-color-5);
  --main-color-6: var(--dark-main-color-6);
  --main-color-7: var(--dark-main-color-7);
  --main-color-8: var(--dark-main-color-8);
  --main-color-9: var(--dark-main-color-9);
  --main-color-10: var(--dark-main-color-10);
  --main-color-alfa-2: rgba(229, 229, 229, 0.4);
  --main-color-alfa-8: rgba(71, 71, 71, 0.4);
  --positive-color-1: #b9e1aa;
  --positive-color-2: #369711;
  --positive-color-3: #286f0c;
  --negative-color-1-rgb: 108, 14, 5;
  --negative-color-2-rgb: 220, 33, 16;
  --negative-color-3-rgb: 248, 94, 79;
  --negative-color-1: rgba(var(--negative-color-1-rgb), 1);
  --negative-color-2: rgba(var(--negative-color-2-rgb), 1);
  --negative-color-3: rgba(var(--negative-color-3-rgb), 1);
  --attention-color-1: #4f462d;
  --attention-color-2: #7e692e;
  --attention-color-3: #d9ba63;
  --action-color: var(--action-color-2);
  --border-color: var(--main-color-2);
  --primary-fg: var(--main-color-10);
  --contrast-fg: var(--main-color-0);
  --primary-bg: #303030;
  --contrast-bg: #2a2a2a;
  --pale-bg: var(--main-color-1);
  --tooltip-bg: var(--main-color-2);
  --tooltip-fg: var(--contrast-fg);
  --popup-shadow: 0 0 25px 0 rgba(0, 0, 0, 0.5);
  --alert-bg: #4e4e4e;
  --traceback-link: #85b9cc;
  --vscode-editorSuggestWidget-background: #3c3f41;
  --vscode-editorSuggestWidget-border: #464646;
}
div,
ul,
li,
span,
body,
html {
  margin: 0;
  padding: 0;
}
ul,
ol {
  list-style-type: none;
}
hr {
  -webkit-margin-before: auto;
  -webkit-margin-after: auto;
  -webkit-margin-start: auto;
  -webkit-margin-end: auto;
  border: none;
}
input[type=text] {
  outline: none;
}
button {
  background: transparent;
  color: inherit;
}
input,
textarea,
keygen,
select,
button {
  font: inherit;
}
*::-webkit-scrollbar-track {
  background-color: transparent;
}
*::-webkit-scrollbar {
  width: 10px;
  height: 10px;
  background-color: transparent;
}
*::-webkit-scrollbar-thumb {
  background-color: var(--main-color-4);
}
*::-webkit-scrollbar-corner {
  background-color: transparent;
}
.has-scroll::-webkit-scrollbar-track {
  background-color: transparent;
}
.has-scroll::-webkit-scrollbar {
  width: 7px;
  height: 7px;
  background-color: transparent;
}
.has-scroll::-webkit-scrollbar-thumb {
  background-color: var(--main-color-4);
}
.has-scroll::-webkit-scrollbar-corner {
  background-color: transparent;
}
body {
  font: 12px / 1.25 -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  font-weight: 400;
  color: var(--main-color-9);
  background-color: var(--primary-bg);
}
body,
html {
  height: 100%;
  overflow: hidden;
}
:root[sandbox="true"] body,
html:root[sandbox="true"] {
  height: initial;
  overflow: auto;
}
.hidden {
  display: none !important;
}
div[tabindex] {
  outline: none;
}
input,
textarea {
  background: var(--primary-bg);
  color: var(--primary-fg);
}
input.input {
  box-sizing: border-box;
  padding: 7px 8px;
  outline: none;
  border: 1px solid var(--border-color);
  transition: border-color 0.15s ease-out;
  font-size: 12px;
  line-height: 16px;
}
input.input:not([disabled]):not([readonly]):focus {
  border-color: var(--action-color-3);
}
input.input[disabled] {
  background: var(--main-color-1);
}
a {
  color: var(--action-color-2);
  text-decoration: none;
}
a:hover {
  color: var(--action-color-3);
}
a[disabled],
a[disabled]:hover,
a[disabled]:active {
  cursor: not-allowed;
  color: var(--main-color-4);
}
textarea.input {
  box-sizing: border-box;
  padding: 6px 8px;
  outline: none;
  border: 1px solid var(--border-color);
  transition: border-color 0.15s ease-out;
}
textarea.input:focus {
  border-color: var(--action-color-3);
}
textarea.input[disabled] {
  background: var(--main-color-1);
}
input[type=text].input-transparent,
textarea.input-transparent {
  box-sizing: border-box;
  width: 100%;
  background: transparent;
  border: none;
  color: inherit;
  text-overflow: ellipsis;
  outline: none;
  resize: none;
  transition: border-color 0.2s ease-out;
}
input[type=text].input-transparent {
  padding: 4px 0;
}
textarea.input-transparent {
  padding: 0 4px;
}
input.input:invalid,
input.input.error,
textarea:invalid,
textarea.error {
  border-color: var(--negative-color-2);
}
/* Hide arrows for number input */
/* Chrome, Safari, Edge, Opera */
input.input::-webkit-outer-spin-button,
input.input::-webkit-inner-spin-button {
  display: none;
}
/* Firefox */
input.input[type=number] {
  -moz-appearance: textfield;
}
input[type=text].input-transparent:focus,
input[type=password].input-transparent:focus,
textarea.input-transparent:focus {
  text-overflow: initial;
}
input.input-muted {
  background: var(--main-color-8);
  border: none;
  border-radius: 2px;
  color: var(--primary-bg);
  padding-left: 28px;
}
input.input-muted::placeholder {
  color: var(--primary-bg);
}
input.input-search {
  background-repeat: no-repeat;
  background-position-y: center;
  background-position-x: 5px;
}
.hovered {
  transition: opacity 0.15s ease-out;
  opacity: 0.4;
  cursor: pointer;
}
.hovered:hover {
  opacity: 0.9;
}
</style><style>html { overflow: auto; }</style></body></html>