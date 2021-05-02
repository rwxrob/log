## Saturday, April 17, 2021, 3:12:46PM EDT <1618686766>

Today I found a bug in Go's handling of commas to the `fmt.Sprint()` and
`fmt.Print()` functions:

```golang
func TestSprint(t *testing.T) {
	i := 42
	b := true
	s := "doh"
	fl := 2.4
	want := _fmt.Sprint(i, b, s, fl) + "doh"
	got := Sprint(i, b, s, fl, fdoh)
	if want != got {
		t.Errorf("\nwant: %v\ngot:  %v\n", want, got)
	}
}
```

Which fails this test:

```
 FAIL: TestSprint (0.00s)
    fmt_test.go:175:
        want: 42 truedoh2.4doh
        got:  42truedoh2.4doh
```

## Saturday, April 17, 2021, 12:13:11PM EDT <1618675991>

Just hit a fatal flaw in Alacritty. It doesn't not support the escapes
used in the `gh` GitHub command line tool. Bubye Alacritty, you've
burned me for the last time. (Works fine in Windows new terminal.)

