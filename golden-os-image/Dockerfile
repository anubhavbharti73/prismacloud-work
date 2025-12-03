FROM public.ecr.aws/amazonlinux/amazonlinux:2023
LABEL maintainer="devops@acpl.com"
LABEL base_image=" acpl-os-golden "
LABEL version="2025.01"
HEALTHCHECK --interval=30s --timeout=3s --retries=3 CMD curl -f http://localhost/health || exit 1
RUN dnf update -y && \
    dnf install -y unzip shadow-utils ca-certificates \
                   java-17-amazon-corretto-headless && \
    dnf clean all && rm -rf /var/cache/dnf
# Create non-root user
RUN useradd -m appuser
USER appuser
WORKDIR /usr/src/app

