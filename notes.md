# reqs:
pandoc 
inkscape

# Commands
pandoc /Users/everardoj.barojasm./Downloads/FINALPROCESO\ 10.1-FEB14.docx -t gfm -o ~/Desktop/output.md --extract-media=media

find media -iname "*.emf" -print0 | xargs -0 -I{} sh -c 'inkscape "{}" --export-type=png --export-filename="{}.png" --export-dpi=300'

## Notes, files end up iwht .emf.png - not ideal
