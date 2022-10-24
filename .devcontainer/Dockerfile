FROM ocaml/opam:ubuntu-18.04-ocaml-5.0

USER opam

RUN opam update && \
  opam install ocamlformat ocaml-lsp-server 
RUN sudo apt-get update && \
  sudo apt-get install -y gcc nasm
RUN cd /home/opam && \
  mkdir workspace && \
  cd -