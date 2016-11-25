# Install dependencies and compile
# npm install -g browserify babel \
#   && npm install \
#   && browserify -t babelify app/app.js -o public/js/app.js \
#   && npm prune --production

FROM node

ENV PORT 3000
ENV LOGIC_URL http://logic



ADD . /app/

RUN npm install -g browserify babel \
   && npm install \
   && browserify -t babelify app/app.js -o public/js/app.js \
   && npm prune --production

RUN useradd -ms /bin/bash usafe
RUN chown -R usafe:usafe /app

WORKDIR /app

USER usafe

EXPOSE $PORT

CMD ["node", "server.js"]