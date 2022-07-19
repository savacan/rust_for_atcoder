FROM rust:1.42.0
RUN apt-get update && \
    apt-get -y install git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rustup component add rustfmt clippy rust-src rust-analysis
RUN cd $(rustc --print sysroot)/lib/rustlib/src/rust && \
    ln -sv src library