# Install dependencies and compile
# npm install -g browserify babel \
#   && npm install \
#   && browserify -t babelify app/app.js -o public/js/app.js \
#   && npm prune --production

FROM node

ENV PORT 3000
ENV LOGIC_URL http://logic

EXPOSE $PORT

CMD npm install -g browserify babel \
   && npm install \
   && browserify -t babelify app/app.js -o public/js/app.js \
   && npm prune --production

CMD [node server.js]