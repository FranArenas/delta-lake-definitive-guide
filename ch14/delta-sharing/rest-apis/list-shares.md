## List Shares
This endpoint allows us to view the shares available using your `*.share` profile file.

**Request**
~~~bash
export DELTA_SHARING_URL="https://sharing.delta.io"
export DELTA_SHARING_PREFIX="delta-sharing"
export DELTA_SHARING_ENDPOINT="$DELTA_SHARING_URL/$DELTA_SHARING_PREFIX"
export BEARER_TOKEN="faaie590d541265bcab1f2de9813274bf233"
export REQUEST_URI="shares"
export REQUEST_URL="$DELTA_SHARING_ENDPOINT/$REQUEST_URI"
export QUERY_PARAMS="maxResults=10"
curl \
  --request GET \
  --header 'Content-Type: application/json' \
  --header 'Authorization: Bearer $BEARER_TOKEN' \
  --url "$REQUEST_URL?$QUERY_PARAMS"
~~~

**Response**
~~~bash
{"items":[{"name":"delta_sharing"}]}
~~~