#---------------------#
#     Repo install    #
#---------------------#

    export REPO=$(mktemp /tmp/repo.XXXXXXXXX) && \
    curl -o ${REPO} https://storage.googleapis.com/git-repo-downloads/repo && \
    gpg --recv-key 8BB9AD793E8E6153AF0F9A4416530D5E920F5C65 && \
    mkdir ./bin && \
    curl -s https://storage.googleapis.com/git-repo-downloads/repo.asc | gpg --verify - ${REPO} && install -m 755 ${REPO} ~/.bin/repo


# mkdir -p ~/.bin
# PATH="${HOME}/.bin:${PATH}"
# curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
# chmod a+rx ~/.bin/repo
