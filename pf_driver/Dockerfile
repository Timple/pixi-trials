FROM ghcr.io/prefix-dev/pixi:noble
WORKDIR /app
COPY pixi.toml /app/pixi.toml
COPY pf_driver /app/pf_driver
RUN --mount=type=cache,target=/root/.cache pixi install
# RUN pixi install
RUN pixi run build
