import os

env =       Environment(ENV = os.environ)
env['ENV']['TEXINPUTS'] = '.'
targets =   [os.path.splitext(f)[0] for f in os.listdir('.') if os.path.splitext(f)[1] == '.tex']

pdfOpener = Builder(action = 'open -a /Applications/Skim.app/ $SOURCE', src_suffix = '.pdf')
env.Append(BUILDERS = {'PDFOpen': pdfOpener})


# Use synctex
env.AppendUnique(PDFLATEXFLAGS='-synctex=1')

Help("""
This is a generic pdfLaTeX builder.
Available targets in this directory:\n
""")

for tgt in targets:
    env.Alias(tgt, env.PDFOpen(env.PDF(source = tgt + '.tex')))
    Help('    scons [-c] ' + str(tgt) + '\n')
Help('    scons -c   (to clean all targets)\n')

Default('lausanne-example')
