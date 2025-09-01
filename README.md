# kivor

A Leveldb wrapper that allows easy store hash, zset data, base on [goleveldb](https://github.com/syndtr/goleveldb)

## Example

```
db, _ := kivor.Open("testdb", nil)

db.Hset("name", []byte("k"), []byte("v"))
db.Hget("name", []byte("k"))
db.Hdel("name", []byte("k"))
db.Hincr("name", []byte("k"), 3)
db.Hscan("name", nil, 10)
db.Hrscan("name", nil, 10)

db.Zset("name", []byte("k"), 1)
db.Zget("name", []byte("k"))
db.Zdel("name", []byte("k"))
db.Zincr("name", []byte("k"), 3)
db.Zscan("name", nil, nil, 10)
db.Zrscan("name", nil, nil, 10)
```
