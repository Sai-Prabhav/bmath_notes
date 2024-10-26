[

    //custom commands
    {
        trigger: /(inn)([\n\s.,?!:'])/,
        replacement: "$\\in$[[1]]",
        options: "rtAw",
    },
    {
        trigger: /([A-Za-z])x([A-Za-z])([\n\s.,?!:'])/,
        replacement: "$[[0]] \\times [[1]]$ [[2]]",
        options: "rtAw",
    },
    {
        trigger: /(RR)([\n\s.,?!:'])/,
        replacement: "$\\RR$[[1]]",
        options: "rtAw",
    },
    {
        trigger: /(?<!\\)(\b[0-9a-zA-Z]*[a-zA-Z])(\d+)(\b)/,
        replacement: "[[0]]_{[[1]]}",
        options: "rmA",
        description: "Auto letter subscript",
        priority: -1,
    },
    
    { trigger: "Ex", replacement: "\\ex[${0:X}] $1", options: "mA" },
    {
        trigger: "sset",
        replacement: "\\left\\{${0:x}_${1:n} \\right\\}_${2:{n \\in \\NN}} $3",
        options: "mA",
    },
    { trigger: "mod", replacement: "\\Mod[${0:X}] $1", options: "mA" },
    { trigger: "var", replacement: "\\var[${0:X}] $1", options: "mA" },
    { trigger: "cov", replacement: "\\cov{${0:X}}{${1:X}} $2", options: "mA" },
    { trigger: "cor", replacement: "\\cov{${0:X}}{${1:X}} $2", options: "mA" },
    { trigger: "csp", replacement: "\\csp{${0:A}} $1", options: "mA" },
    { trigger: "rsp", replacement: "\\rsp{${0:A}} $1", options: "mA" },
    { trigger: "nsp", replacement: "\\nsp{${0:A}} $1", options: "mA" },

    { trigger: "+RR", replacement: "\\RR^{+}", options: "mA" },
    { trigger: "-RR", replacement: "\\RR^{-}", options: "mA" },
    { trigger: "+ZZ", replacement: "\\ZZ^{+}", options: "mA" },
    { trigger: "-ZZ", replacement: "\\ZZ^{-}", options: "mA" },

    { trigger: "BB", replacement: "\\mathcal{B}", options: "mA" },

    { trigger: "cal", replacement: "\\mathcal{$0} $1", options: "mA" },

    { trigger: "pm", replacement: "\\pmod{${0:p}} $1", options: "mA" },

    //visual operators
    { trigger: "H", replacement: "\\Huge{ ${VISUAL} }", options: "mA" },
    {
        trigger: "P",
        replacement: "`\\begin{proof}` ${VISUAL} `\\end{proof}`",
        options: "t",
    },
    { trigger: "L", replacement: "\\Large{ ${VISUAL} }", options: "mA" },
    { trigger: "T", replacement: "\\tiny{ ${VISUAL} }", options: "mA" },
    // Colors
    { trigger: "r", replacement: "{\\color{red} ${VISUAL} }", options: "mA" },
    { trigger: "g", replacement: "{\\color{green} ${VISUAL} }", options: "mA" },
    { trigger: "b", replacement: "{\\color{blue} ${VISUAL} }", options: "mA" },

    // Automatically convert text of the form "x=2" and "x=n+1" to math.
    {
        trigger: /([A-Za-z][=><][A-Za-z][+-]\d+)([\n\s.,?!:'])/,
        replacement: "$[[0]]$[[1]]",
        options: "tAw",
    },
    {
        trigger: /([A-Za-z][=><][+-]?\d+)([\n\s.,?!:'])/,
        replacement: "$[[0]]$[[1]]",
        options: "rtAw",
    },
    {
        trigger: /([A-Za-z][=><][+-]?[A-Za-z]+)([\n\s.,?!:'])/,
        replacement: "$[[0]]$[[1]]",
        options: "rtAw",
    },
    {
        trigger: /([A-Za-z]+)_([A-Za-z0-9]+)([\n\s.,?!:'])/,
        replacement: "$[[0]]_{[[1]]}$[[2]]",
        options: "rtAw",
    },
    {
        trigger: /([A-Za-z]\([^)]*\))([\n\s.,?!:'])/,
        replacement: "$[[0]]$[[1]]",
        options: "rtAw",
    },
    {
        trigger: /([A-Za-z][=><][+-]?[\d]?[A-Za-z][+-]\d+)([\n\s.,?!:'])/,
        replacement: "$[[0]]$[[1]]",
        options: "rtAw",
    },
    {
        trigger: /([A-Za-z][_\^][+-]?[\d])([\n\s.,?!:'])/,
        replacement: "$[[0]]$[[1]]",
        options: "rtAw",
    },

    // Math mode
    { trigger: "mk", replacement: "$$0$", options: "tA" },
    {
        trigger: "dm",
        replacement: "$$\n\\begin{align}\n$0\n\\end{align}\n$$",
        options: "tAw",
    },

    {
        trigger: /(\d)byb(\d)/,
        replacement: (match) => {
            const r = match[1];
            const c = match[2];
            let arr = [];

            let num = 0;
            for (let j = 0; j < r; j++) {
                arr[j] = [];
                for (let i = 0; i < c; i++) {
                    num = j * c + (i + 1) + 1;
                    arr[j][i] = "${" + num + ":0}";
                }
            }

            let output = arr.map((el) => el.join(" & ")).join(" \\\\\n");
            output = `\\begin{\${0:b}matrix}\n${output}\n\\end{\${0:b}matrix}  \${${
                num + 1
            }: }`;
            return output;
        },
        options: "mA",
        description: "N x N matrix",
    },

    // martices
    {
        trigger: "col2",
        replacement:
            "\\begin{${0:b}matrix}${1:x} \\\\ ${2:y}\\end{${0:b}matrix} $3",
        options: "mA",
    },
    {
        trigger: "col3",
        replacement:
            "\\begin{${0:b}matrix}${1:0} \\\\ ${2:0} \\\\ ${3:0}\\end{${0:b}matrix} $4",
        options: "mA",
    },
    {
        trigger: "col4",
        replacement:
            "\\begin{${0:b}matrix}${1:0} \\\\ ${2:0} \\\\ ${3:0} \\\\ ${4:0}\\end{${0:b}matrix} $5",
        options: "mA",
    },
    {
        trigger: "col5",
        replacement:
            "\\begin{${0:b}matrix}${1:0} \\\\ ${2:0} \\\\ ${3:0} \\\\ ${4:0}\\\\ ${5:0}\\end{${0:b}matrix} $6",
        options: "mA",
    },
    {
        trigger: "col6",
        replacement:
            "\\begin{${0:b}matrix}${1:0} \\\\ ${2:0} \\\\ ${3:0} \\\\ ${4:0}\\\\ ${5:0}\\\\ ${6:0}\\end{${0:b}matrix} $7",
        options: "mA",
    },
    {
        trigger: "2by1",
        replacement:
            "\\begin{${0:b}matrix}${1:x} \\\\ ${2:y}\\end{${0:b}matrix} $3",
        options: "mA",
    },
    {
        trigger: "3by1",
        replacement:
            "\\begin{${0:b}matrix}${1:0} \\\\ ${2:0} \\\\ ${3:0}\\end{${0:b}matrix} $4",
        options: "mA",
    },
    {
        trigger: "4by1",
        replacement:
            "\\begin{${0:b}matrix}${1:0} \\\\ ${2:0} \\\\ ${3:0} \\\\ ${4:0}\\end{${0:b}matrix} $5",
        options: "mA",
    },
    {
        trigger: "5by1",
        replacement:
            "\\begin{${0:b}matrix}${1:0} \\\\ ${2:0} \\\\ ${3:0} \\\\ ${4:0}\\\\ ${5:0}\\end{${0:b}matrix} $6",
        options: "mA",
    },
    {
        trigger: "6by1",
        replacement:
            "\\begin{${0:b}matrix}${1:0} \\\\ ${2:0} \\\\ ${3:0} \\\\ ${4:0}\\\\ ${5:0}\\\\ ${6:0}\\end{${0:b}matrix} $7",
        options: "mA",
    },
    {
        trigger: "2by2",
        replacement:
            "\\begin{${0:b}matrix}${1:0} & ${2:0} \\\\ ${3:0} & ${4:0}\\end{${0:b}matrix} $5",
        options: "mA",
    },
    {
        trigger: "2by3",
        replacement:
            "\\begin{${0:b}matrix}${1:0} & ${2:0} & ${3:0}\\\\ ${4:0} & ${5:0}& ${6:0}\\end{${0:b}matrix} $7",
        options: "mA",
    },
    {
        trigger: "3by2",
        replacement:
            "\\begin{${0:b}matrix}${1:0} & ${2:0} \\\\ ${3:0} & ${4:0}\\\\ ${5:0} & ${6:0}\\end{${0:b}matrix} $7",
        options: "mA",
    },
    {
        trigger: "3by3",
        replacement:
            "\\begin{${0:b}matrix}${1:0} & ${2:0} & ${3:0}\\\\ ${4:0} & ${5:0}& ${6:0}\\\\ ${7:0} & ${8:0}& ${9:0}\\end{${0:b}matrix} ${10: }",
        options: "mA",
    },

    //custom commands end here
];
