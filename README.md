# infix-rpn-eval

[![Build Status](https://travis-ci.org/taxnuke/infix-rpn-eval.svg?branch=master)](https://travis-ci.org/taxnuke/infix-rpn-eval) [![npm version](https://badge.fury.io/js/infix-rpn-eval.svg)](https://badge.fury.io/js/infix-rpn-eval)

A JavaScript Implementation of Edsger Dijkstra's Shunting-yard algorithm. Works in Node.js and web browsers.

## Installation

```bash
$ npm install infix-rpn-eval
```

## Usage

> Tokens must be space-separated! Unary `-` goes with its operand, e.g. `-4`

```js
var infixRpnEval = require("infix-rpn-eval");

infixRpnEval.toPostfix('2 + 3 * 3');      // '2 3 3 * +'
infixRpnEval.toInfix('2 3 3 * +');        // '2 + 3 * 3'
infixRpnEval.evaluatePostfix('2 3 3 * +') // 11
```

## API

```js
/**
 * Convert from infix to postfix notation
 * @param {string} infix tokens must be space separated
 * @returns {string}
 */
infixRpnEval.toPostfix = (infix) {...}

/**
 * Convert from postfix to infix notation
 * @param {string} postfix tokens must be space separated
 * @returns {string}
 */
infixRpnEval.toPostfix = (postfix) {...}

/**
 * Evaluate postfix expression
 * @param {string} postfix tokens must be space separated
 * @returns {number}
 */
infixRpnEval.evaluatePostfix = (postfix) {...}
```
