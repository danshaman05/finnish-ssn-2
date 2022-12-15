# Finnish SSN validation and creation

 ![License](https://img.shields.io/npm/l/finnish-ssn.svg)

- A micro Javascript library for validating and creating Finnish social security numbers
- Zero dependencies
- This is a fork of [vkomulai/finnish-ssn](https://github.com/vkomulai/finnish-ssn). See the original project for more information on installation and usage.
- adds support for new formats of Finnish personal identity codes (valid from 2023)
- not part of NPM Registry

## Functions

### #validate(ssn)

- Validates parameter given SSN. Returns true if SSN is valid, otherwise false

### #parse(ssn)

- Parses parameter given SSN. Returns object `{valid: boolean, sex: "male|female", ageInYears: Number, dateOfBirth: Date }`

```js
{
  valid: false,
  sex: null,
  ageInYears: null,
  dateOfBirth: null
}
{
  valid: true,
  sex: 'male',
  ageInYears: 15,
  dateOfBirth: Tue Feb 29 2000 00:00:00 GMT+0200 (EET)
}
{
  valid: true,
  sex: 'female',
  ageInYears: 15,
  dateOfBirth: Mon Feb 28 2000 00:00:00 GMT+0200 (EET)
}
```

### #createWithAge(age)

- Creates a valid SSN using the given age (Integer). Generates randomly male and female SSN's.

## Building

```sh
npm run dist

# Run tests
npm run test

# Run tests in watch-mode
npm run test:watch
```

## Changelog

### 0.9.0

- Initial release (forked from [vkomulai/finnish-ssn](https://github.com/vkomulai/finnish-ssn))

## License

[MIT License](LICENSE)
