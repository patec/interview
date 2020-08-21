# EHR Software

## About

Electronic Health Record Software is used by practices to keep track of the medical records for the patients they see. In order to do so, they will need to keep track of the patient, visit, and the procedure(s) performed.

## Database

In the `data` folder, there is an file called `eligibility.json`. This file contains the insurance information for a given patient. This file should be loaded into a
database to be accessed by the application.

## TODO

Create an application that will accept EHR records and store them in a database. You can expect records to come in the following format:

```
{
  "patient": {
    "first_name": XXXXX,
    "last_name": XXXXX,
    "dob": XXXXX
  },
  "date": XXXXX,
  "procedures": [
    {
      "code": XXXXX,
      "units": XXXXX,
    }...
  ],
  "provider": {
    "first_name": XXXXX,
    "last_name": XXXXX
  }
}
```

Once a visit is submitted, we will want to create a claim submission to their insurance. The claim submission will need to include their
insurance information pulled from the eligibility databse along with the information supplied by the provider.
