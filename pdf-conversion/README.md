To generate the PDF files, from the main repository directory (where "LPID core documents.md" is located), run:

```sh
docker run --rm -it -v .:/data $(docker buildx build --ulimit nofile=1024:10240 -q pdf-conversion) /data/LPID\ core\ documents.md --shift-heading-level-by=-1 --pdf-engine=weasyprint -o '/data/LPID core documents.pdf' --toc -f markdown+fancy_lists --metadata title='Libertarian Party of Idaho Governing Documents' -c /data/pdf-conversion/pixyll-tweaked.css -c /data/pdf-conversion/local-governing-documents.css -s --title-prefix='Libertarian Party of Idaho'

docker run --rm -it -v .:/data $(docker buildx build --ulimit nofile=1024:10240 -q pdf-conversion) /data/Platform.md --shift-heading-level-by=0 --pdf-engine=weasyprint -o '/data/Platform.pdf' --toc -f markdown+fancy_lists --metadata title='Platform' -c /data/pdf-conversion/pixyll-tweaked.css -c /data/pdf-conversion/local-platform.css -s --title-prefix='Libertarian Party of Idaho'
```
