FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update --quiet \
    && apt upgrade --quiet -y \
    && apt install --quiet --no-install-recommends -y \
        texlive-full \
        texlive-fonts-recommended \
        texlive-fonts-extra \
        texlive-lang-cjk \
        xdvik-ja \
    && apt clean \
    && apt autoremove -y \
    && rm -rf /var/lib/apt/lists/*

RUN apt update --quiet \
    && apt install --quiet --no-install-recommends -y \
        curl \
    && curl -fsSL https://deb.nodesource.com/setup_lts.x | bash - \
    && apt install --quiet --no-install-recommends -y \
        nodejs \
    && npm install -y -g \
        textlint \
        textlint-filter-rule-comments \
        textlint-plugin-latex2e \
        textlint-rule-preset-ja-engineering-paper \
        textlint-rule-preset-ja-spacing \
        textlint-rule-preset-ja-technical-writing \
        textlint-rule-preset-jtf-style \
        textlint-rule-prh \
        textlint-rule-spellcheck-tech-word \
    && apt clean \
    && apt autoremove -y \
    && rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]

