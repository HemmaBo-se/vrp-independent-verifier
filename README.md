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
