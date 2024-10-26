[

    //theorems
    { trigger: "axm", replacement: "> [!axiom] $0\n> $1", options: "t" },
    { trigger: "def", replacement: "> [!definition] $0\n> $1", options: "t" },
    { trigger: "lem", replacement: "> [!lemma] $0\n> $1", options: "t" },
    { trigger: "prp", replacement: "> [!proposition] $0\n> $1", options: "t" },
    { trigger: "thm", replacement: "> [!theorem] $0\n> $1", options: "t" },
    { trigger: "cor", replacement: "> [!corollary] $0\n> $1", options: "t" },
    { trigger: "clm", replacement: "> [!claim] $0\n> $1", options: "t" },
    { trigger: "asm", replacement: "> [!assumption] $0\n> $1", options: "t" },
    { trigger: "exm", replacement: "> [!example] $0\n> $1", options: "t" },
    { trigger: "exr", replacement: "> [!exercise] $0\n> $1", options: "t" },
    { trigger: "cnj", replacement: "> [!conjecture] $0\n> $1", options: "t" },
    { trigger: "hyp", replacement: "> [!hypothesis] $0\n> $1", options: "t" },
    { trigger: "rmk", replacement: "> [!remark] $0\n> $1", options: "t" },
    { trigger: "axiom", replacement: "> [!axiom] $0\n> $1", options: "t" },
    {
        trigger: "definition",
        replacement: "> [!definition] $0\n> $1",
        options: "t",
    },
    { trigger: "lemma", replacement: "> [!lemma] $0\n> $1", options: "t" },
    {
        trigger: "proposition",
        replacement: "> [!proposition] $0\n> $1",
        options: "t",
    },
    { trigger: "theorem", replacement: "> [!theorem] $0\n> $1", options: "t" },
    {
        trigger: "corollary",
        replacement: "> [!corollary] $0\n> $1",
        options: "t",
    },
    { trigger: "claim", replacement: "> [!claim] $0\n> $1", options: "t" },
    {
        trigger: "assumption",
        replacement: "> [!assumption] $0\n> $1",
        options: "t",
    },
    { trigger: "example", replacement: "> [!example] $0\n> $1", options: "t" },
    {
        trigger: "exercise",
        replacement: "> [!exercise] $0\n> $1",
        options: "t",
    },
    {
        trigger: "conjecture",
        replacement: "> [!conjecture] $0\n> $1",
        options: "t",
    },
    {
        trigger: "hypothesis",
        replacement: "> [!hypothesis] $0\n> $1",
        options: "t",
    },
    { trigger: "remark", replacement: "> [!remark] $0\n> $1", options: "t" },

    // Greek letters
    { trigger: "@a", replacement: "\\alpha", options: "mA" },
    { trigger: "@b", replacement: "\\beta", options: "mA" },
    { trigger: "@g", replacement: "\\gamma", options: "mA" },
    { trigger: "@G", replacement: "\\Gamma", options: "mA" },
    { trigger: "@d", replacement: "\\delta", options: "mA" },
    { trigger: "@D", replacement: "\\Delta", options: "mA" },
    { trigger: "@e", replacement: "\\upvarepsilon", options: "mA" },
    { trigger: ":e", replacement: "\\epsilon", options: "mA" },
    { trigger: "@z", replacement: "\\zeta", options: "mA" },
    { trigger: "@t", replacement: "\\theta", options: "mA" },
    { trigger: "@T", replacement: "\\Theta", options: "mA" },
    { trigger: ":t", replacement: "\\vartheta", options: "mA" },
    { trigger: "@i", replacement: "\\iota", options: "mA" },
    { trigger: "@k", replacement: "\\kappa", options: "mA" },
    { trigger: "@l", replacement: "\\lambda", options: "mA" },
    { trigger: "@L", replacement: "\\Lambda", options: "mA" },
    { trigger: "@s", replacement: "\\sigma", options: "mA" },
    { trigger: "@S", replacement: "\\Sigma", options: "mA" },
    { trigger: "@u", replacement: "\\upsilon", options: "mA" },
    { trigger: "@U", replacement: "\\Upsilon", options: "mA" },
    { trigger: "@o", replacement: "\\omega", options: "mA" },
    { trigger: "@O", replacement: "\\Omega", options: "mA" },
    { trigger: "ome", replacement: "\\omega", options: "mA" },
    { trigger: "Ome", replacement: "\\Omega", options: "mA" },

    // Text environment
    { trigger: "text", replacement: "\\text{$0}$1", options: "mA" },
    { trigger: '"', replacement: "\\text{$0}$1", options: "mA" },

    // Basic operations
    { trigger: "sr", replacement: "^{2} ", options: "mA" },
    { trigger: "cb", replacement: "^{3} ", options: "mA" },
    { trigger: "^", replacement: "^{$0} $1", options: "mA" },
    { trigger: "_", replacement: "_{$0} $1", options: "mA" },
    { trigger: "sq", replacement: "\\sqrt{ $0 }$1", options: "mA" },
    { trigger: "//", replacement: "\\frac{$0}{$1}$2", options: "mA" },
    { trigger: "ee", replacement: "e^{ $0 }$1", options: "mA" },
    { trigger: "invs", replacement: "^{-1}", options: "mA" },
    { trigger: "conj", replacement: "^{*}", options: "mA" },
    { trigger: "bf", replacement: "\\mathbf{$0}", options: "mA" },
    { trigger: "bb", replacement: "\\mathbb{$0}", options: "mA" },
    { trigger: "rm", replacement: "\\mathrm{$0}$1", options: "mA" },

    // Linear algebra
    { trigger: /([^\\])(det)/, replacement: "[[0]]\\[[1]]", options: "rmA" },
    { trigger: "trace", replacement: "\\mathrm{Tr}", options: "mA" },

    // More operations
    { trigger: "([a-zA-Z])hat", replacement: "\\hat{[[0]]}", options: "rmA" },
    { trigger: "([a-zA-Z])bar", replacement: "\\bar{[[0]]}", options: "rmA" },
    {
        trigger: "([a-zA-Z])dot",
        replacement: "\\dot{[[0]]}",
        options: "rmA",
        priority: -1,
    },
    {
        trigger: "([a-zA-Z])ddot",
        replacement: "\\ddot{[[0]]}",
        options: "rmA",
        priority: 1,
    },
    {
        trigger: "([a-zA-Z])tilde",
        replacement: "\\tilde{[[0]]}",
        options: "rmA",
    },
    {
        trigger: "([a-zA-Z])und",
        replacement: "\\underline{[[0]]}",
        options: "rmA",
    },
    { trigger: "([a-zA-Z])vec", replacement: "\\vec{[[0]]}", options: "rmA" },
    {
        trigger: "([a-zA-Z]),\\.",
        replacement: "\\mathbf{[[0]]}",
        options: "rmA",
    },
    {
        trigger: "([a-zA-Z])\\.,",
        replacement: "\\mathbf{[[0]]}",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}),\\.",
        replacement: "\\boldsymbol{\\[[0]]}",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK})\\.,",
        replacement: "\\boldsymbol{\\[[0]]}",
        options: "rmA",
    },

    { trigger: "hat", replacement: "\\hat{$0}$1", options: "mA" },
    { trigger: "bar", replacement: "\\bar{$0}$1", options: "mA" },
    { trigger: "dot", replacement: "\\dot{$0}$1", options: "mA", priority: -1 },
    { trigger: "ddot", replacement: "\\ddot{$0}$1", options: "mA" },
    { trigger: "cdot", replacement: "\\cdot", options: "mA" },
    { trigger: "tilde", replacement: "\\tilde{$0}$1", options: "mA" },
    { trigger: "und", replacement: "\\underline{$0}$1", options: "mA" },
    { trigger: "vec", replacement: "\\vec{$0}$1", options: "mA" },

    // More auto letter subscript
    {
        trigger: /([A-Za-z])_(\d\d)/,
        replacement: "[[0]]_{[[1]]}",
        options: "rmA",
    },
    {
        trigger: /\\hat{([A-Za-z])}(\d)/,
        replacement: "\\hat{[[0]]}_{[[1]]}",
        options: "rmA",
    },
    {
        trigger: /\\vec{([A-Za-z])}(\d)/,
        replacement: "\\vec{[[0]]}_{[[1]]}",
        options: "rmA",
    },
    {
        trigger: /\\mathbf{([A-Za-z])}(\d)/,
        replacement: "\\mathbf{[[0]]}_{[[1]]}",
        options: "rmA",
    },

    { trigger: "xnn", replacement: "x_{n}", options: "mA" },
    { trigger: "\\xii", replacement: "x_{i}", priority: 10, options: "mA" },
    { trigger: "\\xi nn", replacement: "x \\in", priority: 10, options: "mA" },
    { trigger: "xjj", replacement: "x_{j}", options: "mA" },
    { trigger: "xp1", replacement: "x_{n+1}", options: "mA" },
    { trigger: "ynn", replacement: "y_{n}", options: "mA" },
    { trigger: "yii", replacement: "y_{i}", options: "mA" },
    { trigger: "yjj", replacement: "y_{j}", options: "mA" },

    // Symbols
    { trigger: "ooo", replacement: "\\infty", options: "mA" },
    {
        trigger: "sum",
        replacement: "\\sum_{${0:i}=${1:1}}^{${2:N}} $3",
        options: "mA",
    },

    {
        trigger: "prod",
        replacement: "\\prod_{${0:i}=${1:1}}^{${2:N}} $3",
        options: "mA",
    },
    {
        trigger: "\\sum",
        replacement: "\\sum_{${0:i}=${1:1}}^{${2:N}} $3",
        options: "m",
    },
    {
        trigger: "\\prod",
        replacement: "\\prod_{${0:i}=${1:1}}^{${2:N}} $3",
        options: "m",
    },
    {
        trigger: "lim",
        replacement: "\\lim_{ ${0:n} \\to ${1:\\infty} } $2",
        options: "mA",
    },
    { trigger: "+-", replacement: "\\pm", options: "mA" },
    { trigger: "-+", replacement: "\\mp", options: "mA" },
    { trigger: "...", replacement: "\\dots", options: "mA" },
    { trigger: "nabl", replacement: "\\nabla", options: "mA" },
    { trigger: "del", replacement: "\\nabla", options: "mA" },
    { trigger: "xx", replacement: "\\times", options: "mA" },
    { trigger: "**", replacement: "\\cdot", options: "mA" },
    { trigger: "para", replacement: "\\parallel", options: "mA" },

    { trigger: "===", replacement: "\\equiv", options: "mA" },
    { trigger: "!=", replacement: "\\neq", options: "mA" },
    { trigger: ">=", replacement: "\\geq", options: "mA" },
    { trigger: "<=", replacement: "\\leq", options: "mA" },
    { trigger: ">>", replacement: "\\gg", options: "mA" },
    { trigger: "<<", replacement: "\\ll", options: "mA" },
    { trigger: "simm", replacement: "\\sim", options: "mA" },
    { trigger: "sim=", replacement: "\\simeq", options: "mA" },
    { trigger: "prop", replacement: "\\propto", options: "mA" },

    { trigger: "<->", replacement: "\\leftrightarrow ", options: "mA" },
    { trigger: "->", replacement: "\\to", options: "mA" },
    { trigger: "!>", replacement: "\\mapsto", options: "mA" },
    { trigger: "=>", replacement: "\\implies", options: "mA" },
    { trigger: "=<", replacement: "\\impliedby", options: "mA" },

    { trigger: "and", replacement: "\\cap", options: "mA" },
    { trigger: "band", replacement: "\\bigcap_{$0}^{$1}", options: "mA" },
    {
        trigger: "b\\orr",
        replacement: "\\bigcup_{$0}^{$1}",
        priority: 20,
        options: "mA",
    },
    { trigger: "\\orr", replacement: "\\cup", priority: 10, options: "mA" },

    { trigger: "inn", replacement: "\\in", options: "mA" },
    { trigger: "notin", replacement: "\\not\\in", options: "mA" },
    { trigger: "\\\\\\", replacement: "\\setminus", options: "mA" },
    { trigger: "sub=", replacement: "\\subseteq", options: "mA" },
    { trigger: "sup=", replacement: "\\supseteq", options: "mA" },
    { trigger: "eset", replacement: "\\phi", options: "mA" },
    { trigger: "set", replacement: "\\left\\{ $0 \\right\\}$1", options: "mA" },
    {
        trigger: "exi",
        replacement: "\\exists \\ ",
        options: "mA",
        priority: 10,
    },

    // Handle spaces and backslashes

    // Snippet variables can be used as shortcuts when writing snippets.
    // For example, ${GREEK} below is shorthand for "alpha|beta|gamma|Gamma|delta|..."
    // You can edit snippet variables under the Advanced snippet settings section.

    {
        trigger: "([^\\\\])(${GREEK})",
        replacement: "[[0]]\\[[1]]",
        options: "rmA",
        description: "Add backslash before Greek letters",
    },
    {
        trigger: "([^\\\\])(${SYMBOL})",
        replacement: "[[0]]\\[[1]]",
        options: "rmA",
        description: "Add backslash before symbols",
    },

    // Insert space after Greek letters and symbols
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}|${MORE_SYMBOLS})([A-Za-z])",
        replacement: "\\[[0]] [[1]]",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) sr",
        replacement: "\\[[0]]^{2} ",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) cb",
        replacement: "\\[[0]]^{3} ",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) rd",
        replacement: "\\[[0]]^{$0}$1",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) hat",
        replacement: "\\hat{\\[[0]]}",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) dot",
        replacement: "\\dot{\\[[0]]}",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) bar",
        replacement: "\\bar{\\[[0]]}",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) vec",
        replacement: "\\vec{\\[[0]]}",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) tilde",
        replacement: "\\tilde{\\[[0]]}",
        options: "rmA",
    },
    {
        trigger: "\\\\(${GREEK}|${SYMBOL}) und",
        replacement: "\\underline{\\[[0]]}",
        options: "rmA",
    },

    // Derivatives and integrals
    {
        trigger: "par",
        replacement: "\\frac{ \\partial ${0:y} }{ \\partial ${1:x} } $2",
        options: "m",
    },
    {
        trigger: /pa([A-Za-z])([A-Za-z])/,
        replacement: "\\frac{ \\partial [[0]] }{ \\partial [[1]] } ",
        options: "rm",
    },
    { trigger: "ddt", replacement: "\\frac{d}{dt} ", options: "mA" },

    {
        trigger: /([^\\])int/,
        replacement: "[[0]]\\int",
        options: "mA",
        priority: -1,
    },
    { trigger: "\\int", replacement: "\\int $0 \\, d${1:x} $2", options: "m" },
    {
        trigger: "dint",
        replacement: "\\int_{${0:0}}^{${1:1}} $2 \\, d${3:x} $4",
        options: "mA",
    },
    { trigger: "oint", replacement: "\\oint", options: "mA" },
    { trigger: "iint", replacement: "\\iint", options: "mA" },
    { trigger: "iiint", replacement: "\\iiint", options: "mA" },
    {
        trigger: "oinf",
        replacement: "\\int_{0}^{\\infty} $0 \\, d${1:x} $2",
        options: "mA",
    },
    {
        trigger: "infi",
        replacement: "\\int_{-\\infty}^{\\infty} $0 \\, d${1:x} $2",
        options: "mA",
    },

    // Trigonometry
    {
        trigger: /([^\\])(arcsin|sin|arccos|cos|arctan|tan|csc|sec|cot)/,
        replacement: "[[0]]\\[[1]]",
        options: "rmA",
        description: "Add backslash before trig funcs",
    },

    {
        trigger:
            /\\(arcsin|sin|arccos|cos|arctan|tan|csc|sec|cot)([A-Za-gi-z])/,
        replacement: "\\[[0]] [[1]]",
        options: "rmA",
        description:
            "Add space after trig funcs. Skips letter h to allow sinh, cosh, etc.",
    },

    {
        trigger: /\\(sinh|cosh|tanh|coth)([A-Za-z])/,
        replacement: "\\[[0]] [[1]]",
        options: "rmA",
        description: "Add space after hyperbolic trig funcs",
    },

    // Visual operations
    {
        trigger: "U",
        replacement: "\\underbrace{ ${VISUAL} }_{ $0 }",
        options: "mA",
    },
    {
        trigger: "O",
        replacement: "\\overbrace{ ${VISUAL} }^{ $0 }",
        options: "mA",
    },
    {
        trigger: "B",
        replacement: "\\underset{ $0 }{ ${VISUAL} }",
        options: "mA",
    },
    { trigger: "C", replacement: "\\cancel{ ${VISUAL} }", options: "mA" },
    {
        trigger: "K",
        replacement: "\\cancelto{ $0 }{ ${VISUAL} }",
        options: "mA",
    },
    { trigger: "S", replacement: "\\sqrt{ ${VISUAL} }", options: "mA" },

    // Quantum mechanics
    { trigger: "dag", replacement: "^{\\dagger}", options: "mA" },
    { trigger: "o+", replacement: "\\oplus ", options: "mA" },
    { trigger: "ox", replacement: "\\otimes ", options: "mA" },

    // Environments
    {
        trigger: "pmat",
        replacement: "\\begin{pmatrix}\n$0\n\\end{pmatrix}",
        options: "MA",
    },

    {
        trigger: "bmat",
        replacement: "\\begin{bmatrix}\n$0\n\\end{bmatrix}",
        options: "MA",
    },
    {
        trigger: "Bmat",
        replacement: "\\begin{Bmatrix}\n$0\n\\end{Bmatrix}",
        options: "MA",
    },
    {
        trigger: "vmat",
        replacement: "\\begin{vmatrix}\n$0\n\\end{vmatrix}",
        options: "MA",
    },
    {
        trigger: "Vmat",
        replacement: "\\begin{Vmatrix}\n$0\n\\end{Vmatrix}",
        options: "MA",
    },
    {
        trigger: "matrix",
        replacement: "\\begin{matrix}\n$0\n\\end{matrix}",
        options: "MA",
    },

    {
        trigger: "pmat",
        replacement: "\\begin{pmatrix}$0\\end{pmatrix}",
        options: "nA",
    },
    {
        trigger: "bmat",
        replacement: "\\begin{bmatrix}$0\\end{bmatrix}",
        options: "nA",
    },
    {
        trigger: "Bmat",
        replacement: "\\begin{Bmatrix}$0\\end{Bmatrix}",
        options: "nA",
    },
    {
        trigger: "vmat",
        replacement: "\\begin{vmatrix}$0\\end{vmatrix}",
        options: "nA",
    },
    {
        trigger: "Vmat",
        replacement: "\\begin{Vmatrix}$0\\end{Vmatrix}",
        options: "nA",
    },
    {
        trigger: "matrix",
        replacement: "\\begin{matrix}$0\\end{matrix}",
        options: "nA",
    },

    {
        trigger: "cases",
        replacement: "\\begin{cases}\n$0\n\\end{cases}",
        options: "mA",
    },
    {
        trigger: "align",
        replacement: "\\begin{align}\n$0\n\\end{align}",
        options: "mA",
    },
    {
        trigger: "array",
        replacement: "\\begin{array}\n$0\n\\end{array}",
        options: "mA",
    },

    // Brackets
    { trigger: "avg", replacement: "\\langle $0 \\rangle $1", options: "mA" },
    {
        trigger: "norm",
        replacement: "\\lvert $0 \\rvert $1",
        options: "mA",
        priority: 1,
    },
    {
        trigger: "Norm",
        replacement: "\\lVert $0 \\rVert $1",
        options: "mA",
        priority: 1,
    },
    { trigger: "ceil", replacement: "\\lceil $0 \\rceil $1", options: "mA" },
    { trigger: "floor", replacement: "\\lfloor $0 \\rfloor $1", options: "mA" },
    // {trigger: "mod", replacement: "|$0|$1", options: "mA"},
    { trigger: "(", replacement: "\\left(${VISUAL}\\right)", options: "mA" },
    { trigger: "[", replacement: "\\left[${VISUAL}\\right]", options: "mA" },
    {
        trigger: "{",
        replacement: "\\left\\{ ${VISUAL} \\right\\}",
        options: "mA",
    },
    { trigger: "|", replacement: "\\left|${VISUAL}\\right|", options: "mA" },
    { trigger: "(", replacement: "($0)$1", options: "mA" },
    { trigger: "{", replacement: "{$0}$1", options: "mA" },
    { trigger: "[", replacement: "[$0]$1", options: "mA" },
    { trigger: "lr(", replacement: "\\left( $0 \\right) $1", options: "mA" },
    {
        trigger: "lr{",
        replacement: "\\left\\{ $0 \\right\\} $1",
        options: "mA",
    },
    { trigger: "lr[", replacement: "\\left[ $0 \\right] $1", options: "mA" },
    { trigger: "lr|", replacement: "\\left| $0 \\right| $1", options: "mA" },
    { trigger: "lra", replacement: "\\left< $0 \\right> $1", options: "mA" },

    // Misc

    // Automatically convert standalone letters in text to math (except a, A, I).
    // (Un-comment to enable)
    {
        trigger: /([^'])\b([B-HJ-Zb-z])\b([\n\s.,?!:'])/,
        replacement: "[[0]]$[[1]]$[[2]]",
        options: "tA",
    },

    // Automatically convert Greek letters in text to math.
    {
        trigger: "(${GREEK})([\\n\\s.,?!:'])",
        replacement: "$\\[[0]]$[[1]]",
        options: "rtAw",
    },

    // Snippet replacements can also be JavaScript functions.
    // See the documentation for more information.
    {
        trigger: /iden(\d)/,
        replacement: (match) => {
            const n = match[1];

            let arr = [];
            for (let j = 0; j < n; j++) {
                arr[j] = [];
                for (let i = 0; i < n; i++) {
                    arr[j][i] = i === j ? 1 : 0;
                }
            }

            let output = arr.map((el) => el.join(" & ")).join(" \\\\\n");
            output = `\\begin{pmatrix}\n${output}\n\\end{pmatrix}`;
            return output;
        },
        options: "mA",
        description: "N x N identity matrix",
    },
];
