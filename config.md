
Listed below are all the directives that are supported in Shiny Server config files.

**Applies to** indicates the kind of parent scope that this directive normally appears inside.

**Inheritable** means that you can put this directive at a higher level in the hierarchy and it will be inherited by any children to which it might apply. Inherited directives can be overridden by using the directive again in a child scope.

{{#each directives}}

### {{name}}

{{{desc}}}

{{#if params}}
  \begin{tabular}{ c c  c  p{8cm}  c }
  \hline
  Parameter & Data type & Type & Description & Default \\
  {{#each params}}
    \hline
    \texttt{ {{name}} } & \texttt{ {{type}} } & \texttt{ {{#if optional}}optional{{else}}{{#if vararg}}multiple{{else}}required{{/if}}{{/if}} } & {{{desc}}} & \texttt{ {{defaultValue}} } \\
  {{/each}}
  \hline
  \end{tabular}
{{else}}
  This directive has no parameters.
{{/if}}

Applies to: {{{scopelist at}}}

Inheritable: {{YesNo otherLocs}}

{{#if children}}
  Child directives: {{{scopelist children}}}
{{/if}}

{{/each}}
