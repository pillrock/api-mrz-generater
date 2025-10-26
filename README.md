# api-mrz-generater

- API: `https://www.dynamsoft.com/api-common/api/marketing/generateMRZ`
- Method: `POST`
- Content-Type: `application/json`
- 
### 1. Random (Tạo MRZ ngẫu nhiên theo loại tài liệu)
**PayLoad**: (Dữ liệu gửi lên)
```json
{
  "DocumentType": "<Loại tài liệu>",
  "random": true
}
```
| Mô tả loại tài kiệu | DocumentType
|-|-|
| Passport (TD3) | `TD3` 
| ID Card (TD1) | `TD1` 
| ID Card (TD2) | `TD2` 
| Visa (A) | `MRVA` 
| Visa (B) | `MRVB` 

### 2. Create (Tạo MRZ theo dữ liệu đầu vào)
**Payload** (Dữ liệu gửi lên)
Ví dụ dữ liệu gửi lên
```json
{
  "Birthday": "520904",
  "Country": "SVK",
  "DocumentNumber": "USVYWIBSA",
  "DocumentType": "MRVA",
  "ExpiryDate": "341030",
  "GivenName": "Kathy",
  "Nationality": "SVK",
  "Optional1": "",
  "Optional2": "",
  "Sex": "M",
  "Surname": "Quintanar"
}
```


**Data Response** (Dữ liệu trả về)
```json
{
    "code": 0,
    "data": "{\u0022MRZ\u0022: \u0022V\u003CSVKQUINTANAR\u003C\u003CKATHY\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\\nUSVYWIBSA8SVK5209048M3410303\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u003C\u0022, \u0022success\u0022: true}"
}
```

