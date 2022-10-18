FROM ocaml/opam:ubuntu-18.04-ocaml-5.0

USER opam
# Install Opam packages
RUN opam update && \
  opam install ocamlformat ocaml-lsp-server 
RUN apt update && \
  apt install gcc nasm


