# jubilant-spoon
Web Programming with Python and Django 
import cs50
db = cs50.SQL("sqlite:///foo.db")
db.execute("CREATE TABLE IF NOT EXISTS cs50 (id INTEGER PRIMARY KEY, val TEXT, bin BLOB)")
db.execute("INSERT INTO cs50 (val) VALUES('a')")
db.execute("INSERT INTO cs50 (val) VALUES('b')")
db.execute("BEGIN")
db.execute("INSERT INTO cs50 (val) VALUES('c')")
db.execute("INSERT INTO cs50 (val) VALUES('x')")
db.execute("INSERT INTO cs50 (val) VALUES('y')")
db.execute("ROLLBACK")
db.execute("INSERT INTO cs50 (val) VALUES('z')")
db.execute("COMMIT")

---

import cs50
db = cs50.SQL("mysql://root@localhost/test")
db.execute("CREATE TABLE IF NOT EXISTS cs50 (id INTEGER PRIMARY KEY, val TEXT, bin BLOB)")
db.execute("INSERT INTO cs50 (val) VALUES('a')")
db.execute("INSERT INTO cs50 (val) VALUES('b')")
db.execute("BEGIN")
db.execute("INSERT INTO cs50 (val) VALUES('c')")
db.execute("INSERT INTO cs50 (val) VALUES('x')")
db.execute("INSERT INTO cs50 (val) VALUES('y')")
db.execute("ROLLBACK")
db.execute("INSERT INTO cs50 (val) VALUES('z')")
db.execute("COMMIT")

---

import cs50
db = cs50.SQL("postgresql://postgres@localhost/test")
db.execute("CREATE TABLE IF NOT EXISTS cs50 (id SERIAL PRIMARY KEY, val VARCHAR(16), bin BYTEA)")
db.execute("INSERT INTO cs50 (val) VALUES('a')")
db.execute("INSERT INTO cs50 (val) VALUES('b')")
db.execute("BEGIN")
db.execute("INSERT INTO cs50 (val) VALUES('c')")
db.execute("INSERT INTO cs50 (val) VALUES('x')")
db.execute("INSERT INTO cs50 (val) VALUES('y')")
db.execute("ROLLBACK")
db.execute("INSERT INTO cs50 (val) VALUES('z')")
db.execute("COMMIT")
