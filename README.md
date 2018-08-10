Vue Modify Array Object Demo
============================

```
npm install
npm run serve
```

Then open <http://localhost:8080/>, click on the users,
their `clicked` property should be modified to `true`,
but nothing changes on page.

---

Update:

Change `user.clicked = true` to `Vue.set(user, 'clicked', true)` fixed this problem.

Thanks @skribe! <https://stackoverflow.com/a/51780364/342235>