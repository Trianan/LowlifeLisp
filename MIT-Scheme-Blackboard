#lang sicp
; Some large-growing functions implemented in Scheme.

(define (factorial n) (if (= n 0) 1 (* n (factorial (- n 1))))) ; Practical memory/time limit around n = ~100,000.



(define (exp n p) (cond ((= p 0) 1) ; n raised to the power p.
                        ((= p 1) n)
                        ((< p 0) (/ 1 (/ n (exp n (+ p 1)))))
                        (else (* n (exp n (- p 1))))
                        ))

(define (tetrate n h)(cond ((= h 0) 1) ; This runs out of memory for small arguments (~ n=2, h=6).
                           ((> h 0) (exp n (tetrate n (- h 1))))
                       ))
