FROM ubuntu:16.04

# Install deps
RUN apt-get -qq update
RUN apt-get -y -qq install postgresql libpq-dev pwgen inotify-tools wget

# Install elixir
RUN wget https://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb && dpkg -i erlang-solutions_1.0_all.deb
RUN apt-get update
RUN apt-get -y install esl-erlang
RUN apt-get -y install elixir

# Install node
RUN apt-get -y install nodejs
RUN apt-get -y install npm

# Install mix + phoenix
RUN mix local.hex
RUN yes | mix archive.install https://github.com/phoenixframework/archives/raw/master/phx_new.ez
