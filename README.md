# Scheme-Interpreter-Scala
This was a project in EPFL Functional Programming course. It is basically a Scala implementation of https://github.com/jshin49/Scheme-Interpreter-CPP

## Usage

```
> (+ 1 2 3)
6
> (define (map f l) (if (not (null? l)) (cons (f (car l)) (map f (cdr l)))))
()
> (map (lambda (x) (* x x)) (cons 1 (cons 2 (cons 3 (quote ())))))
(1, 4, 9)
> (define (foreach f l) (if (not (null? l)) (begin (f (car l)) (foreach f (cdr l)))))
()
> (foreach display (cons 1 (cons foo (cons 2 (cons bar (quote ()))))))
1
foo
2
bar
()
> > (+ 2 3 4 5)
14
> (+ 2 3.5)
5.5
> (+ 2)
2
> (+)
0
> (+ (+ -2 5 -1) 3.5)
5.5
> (ceiling 4.7)
5
> (ceiling 4.0)
4
> (ceiling -4.7)
-4
> (if 5 7 8.3)
7
> (if 0 7 8.3)
8.3
> (if (+ 2 3) (ceiling 6.1) (+ 4 2.3 2))
7
> (if (+ 2 -2) (ceiling 6.1) (+ 4 2.3 2))
8.3
> (+ 1 (if (+ 2 -2) (ceiling 6.1) (+ 4 2.3 2)))
9.3
