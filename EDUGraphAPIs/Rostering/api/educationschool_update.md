# Update educationschool

Update the properties of a school object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  Not supported.  |
|Delegated (personal Microsoft account) |  Not supported.  |
|Application | EduRoster.ReadWrite.All |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/schools/<id>
```
## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |
| Content-Type  | application/json  |

## Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName| String| Display name of the school| 
|description| String | Description of the school| 
|principalEmail| String| Email address of the principal|
|principalName| String | Name of the principal|
|externalPrincipalId| String | Id of principal in syncing system. |
|highestGrade|String| Highest grade taught. |
|lowestGrade|String| Lowest grade taught. |
|schoolNumber|String| School Number.|
|externalId|String| Id of school in syncing system. |
|phone|String| Phone number of school. |
|fax|String| Fax number of school. |
|address|[physicalAddress](physicaladdress.md)| Address of the School.|
|createdBy|[identitySet](identityset.md)|Entity who created the school.|

## Response
If successful, this method returns a `200 OK` response code and updated [educationSchool](../resources/educationschool.md) object in the response body.
## Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_educationschool"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/schools/<id>
Content-type: application/json
Content-length: 292

{
  "displayName": "String",
  "description": "String",
}
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 292

{
  "id": "String",
  "displayName": "String",
  "description": "String",
  "status": "String",
  "externalSource": "String",
  "principalEmail": "String",
  "principalName": "String",
  "externalPrincipalId": "String",
  "highestGrade": "String",
  "lowestGrade": "String",
  "schoolNumber": "String",
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "externalId": "String",
  "fax": "String",
  "phone": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationschool",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->