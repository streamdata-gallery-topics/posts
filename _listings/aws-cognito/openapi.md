swagger: "2.0"
x-collection-name: AWS Cognito
x-complete: 1
info:
  title: AWS Cognito Merged API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=UpdateRecords:
    get:
      summary: Update Records
      description: Posts updates to records and adds and deletes records for a dataset
        and user.
      operationId: updateRecords
      x-api-path-slug: actionupdaterecords-get
      parameters:
      - in: query
        name: ClientContext
        description: Intended to supply a device ID that will populate the lastModifiedBy
          field referenced in other methods
        type: string
      - in: query
        name: DatasetName
        description: A string of up to 128 characters
        type: string
      - in: query
        name: IdentityId
        description: A name-spaced GUID (for example, us-east-1:23EC4050-6AEA-7089-A2DD-08002EXAMPLE)
          created by Amazon Cognito
        type: string
      - in: query
        name: IdentityPoolId
        description: A name-spaced GUID (for example, us-east-1:23EC4050-6AEA-7089-A2DD-08002EXAMPLE)
          created by Amazon Cognito
        type: string
      responses:
        200:
          description: OK
      tags:
      - Records