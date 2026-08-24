# VRP Independent Verifier

An independent implementation of the [Vacation Rental Protocol (VRP)](https://github.com/vacationrentalprotocol/vrp-spec) verifier.

This project is an independently maintained verifier implementation and does not depend on the verifier implementation in the VRP specification repository.

**VRP Specification:** [vacationrentalprotocol/vrp-spec](https://github.com/vacationrentalprotocol/vrp-spec)

This repository provides a standalone verifier for validating signed VRP offers and receipts without depending on the JavaScript implementation in the VRP specification repository.

## Status

This verifier has been tested against the VRP conformance vectors and is intended to provide an independent implementation of the verification rules defined by the specification.

## What this verifies

The verifier implements the verification rules defined by VRP, including:

* Ed25519 signature verification
* JWKS-based public key resolution
* Signed-offer validation
* Freshness checks
* Safe-to-Quote validation
* Fail-closed verification
* Receipt envelope verification

The implementation is designed to be independently runnable and testable against the VRP conformance vectors.

## Requirements

* Node.js 18 or later
* Git

No external services or network access are required to run the conformance tests.

## Installation

Clone the repository:

```bash
git clone https://github.com/Swarnabha753/vrp-independent-verifier.git
cd vrp-independent-verifier
```

No additional dependencies are required if the repository uses only Node.js built-ins.

## Running the tests

Run the verifier test suite:

```bash
node verify-test.mjs
```

Run the receipt verification tests:

```bash
node verify-receipt-test.mjs
```

The test suite runs the committed VRP conformance vectors and reports whether each vector produces the expected result.

A successful run should report all test vectors as passing.

## Conformance vectors

The verifier is tested against the VRP conformance vectors from the specification repository.

The vectors are self-describing and contain the information required for verification, including:

* Input data
* Public keys
* Evaluation clock
* Expected verification result

This allows the verifier to be tested without relying on the implementation contained in the VRP specification repository.

## Repository structure

```text
.
├── src/
│   ├── verifier.mjs
│   └── receipt-verifier.mjs
├── verify-test.mjs
├── verify-receipt-test.mjs
├── package.json
└── README.md
```

## Independence

This project is intentionally maintained as a separate implementation from the VRP specification repository.

It does not import or execute the verifier implementation from the specification repository. Its purpose is to provide an independently maintained verifier that can be used to validate the VRP specification and its conformance vectors.

## Specification

The implementation follows the VRP specification:

[VRP Specification](https://github.com/vacationrentalprotocol/vrp-spec)

In particular, see the sections covering:

* Signed Offers
* Freshness
* Safe-to-Quote
* Fail-Closed verification
* Receipt verification

## License

This repository is licensed under the [MIT License](LICENSE).
