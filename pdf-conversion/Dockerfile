FROM greyltc/archlinux-aur:yay
RUN sudo -u ab -D~ bash -c 'yay -Syu --removemake --needed --noprogressbar --noconfirm pandoc-cli python-weasyprint ttf-lato ttf-merriweather'
ENTRYPOINT ["pandoc"]
