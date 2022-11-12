FROM ocaml/opam:ubuntu-18.04-ocaml-5.0

USER opam

RUN opam update && \
  opam install ocamlformat ocaml-lsp-server utop
RUN sudo apt-get update && \
    sudo apt-get install -y software-properties-common && \
    sudo add-apt-repository ppa:plt/racket && \
    sudo apt-get install -y gcc nasm racket
RUN raco pkg update && raco pkg install --auto racket-langserver
RUN cd /home/opam && \
  mkdir workspace && \
  cd -