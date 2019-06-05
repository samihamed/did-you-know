# TIL
> This is a list of notes and helpful tips I collected about all dev-related things.

## Git
`git reset HEAD~1 --soft` Uncommit without losing work

`git fetch -p && git branch -vv | grep gone | gawk '{print $1}' | xargs -n 1 git branch -D $1` => Remove all non-remote branches locally

`git commit --amend` Change message of last commit

`git add . && git commit --amend` Add small change after previous changes have been staged and commited already

`cd .. && sudo rm -rf ${GIT_REPO_NAME} && git clone https://${AUTHOR}.github.com/${GIT_REPO_NAME}.git && cd ${GIT_REPO_NAME}` ¯\\_ (ツ) __/¯

## MongoDB
`db.collection.find({"${ANYKEY}":{$elemMatch:{"$in":[null], "$exists":true}}})` Finds all objects in a collection which contain the key ${ANYKEY}

`db.collection.find({${ANYKEY}: {$ne: "${PROPERTY_ONE}", $ne: "${PROPERTY_TWO}"}}, {${KEY_ONE}:1, ${KEY_ONE}:2, ${KEY_ONE}: 3}).sort({date:-1}).limit(${LIMIT}).pretty()` Shows all objects in a collection which do NOT have the ${PROPERTY_ONE} key and also do NOT have the ${PROPERTY_TWO} key. All results are returned mapped with the keys ${KEY_ONE}, ${KEY_TWO} and ${KEY_THREE}, sorted by date (-1 === 'Descending'), limited to ${LIMIT} results and displayed 'pretty'.

## Google
`"quotation marks"` Searches exactly for a query

`-dash` excludes a word from a search

`~tilde` includes synonyms of a word

`site:` search within a specific site

`| vertical bar` search for this || that

## About
I shamelessly stole this idea from [kale-stew/TIL](https://github.com/kale-stew/TIL), who stole it from [jbranchaud/til](https://github.com/jbranchaud/til), whole stole it from [thoughtbot/til](https://github.com/thoughtbot/til).

## License
© 2019 Sami Hamed

This repository is licensed under the MIT license. See LICENSE for details.