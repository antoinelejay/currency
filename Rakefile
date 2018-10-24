desc "Installation of the package"
task :ins do 
    sh "pdflatex currency.ins"
    sh "pdflatex currency.dtx"
    sh "makeindex -s gind.ist currency.idx"
    sh "makeindex -s gglo.ist -o currency.gls currency.glo"
    sh "pdflatex currency.dtx"
end

desc "Compile the user's guide"
task :doc do 
    sh "pdflatex currency_doc.tex"
    sh "biber currency_doc"
    sh "pdflatex currency_doc.tex"
end

desc "Compile the user's guide"
file "currency_doc.pdf" => :doc do
end

desc "Compilte the package"
file "currency.sty" => :ins do
end

desc "Create a zip file"
task :zip do 
    f=%W(currency.ins currency.dtx currency.pdf currency_doc.tex currency_doc.pdf README.md)
    sh "zip currency.zip %s" %[f.join(" ")]
end
