
# Prioritas Dana 3.0
Prioritas Dana 3.0 adalah project ACCCash versi ke 3 yang menambah 2 produk baru, yaitu:
- Topup
- Pendanaan Baru
Dan membuat Landing Page baru khusus Prioritas Dana di website ACC One.


## Endpoints
````
- POST /restv2/acccash/cms/updapplycmsacccash
- POST /restv2/acccash/transactionplafond/getavlplafondacccash
- POST /restv2/acccash/transactionplafond/getlistplafondacccash
- POST /restv2/acccash/transactionplafond/getlistplafondacccash
- POST /restv2/acccoid/gcm/getdetailgcmaccweb
- POST /restv2/acccoid/gcm/getcontentacccash
- POST /restv2/acccash/transactionplafond/checkautodebet
- POST /restv2/acccash/transactionplafond/checkplafondacccash
- POST /restv2/acccash/transactionplafond/updateflagreadplafond
- POST /restv2/acccash/transactionplafond/getwordproductacccash
- POST /restv2/acccash/transactionplafond/checksourceacccash
- POST /restv2/acccash/transactionplafond/checktopupacccash
- POST /restv2/acccash/transactionplafond/getphoneacccash
- POST /restv2/acccash/transactionplafond/checkphoneacccash

````

## POST /restv2/acccash/cms/updapplycmsacccash

> Update customer data in CMS for Topup and New Financing Product

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doUpdApplyCmsAcccash" : {
        "P_GUID" : null,
        "P_LANGUAGE" : null,
        "P_NO_AGGR" : null,
        "P_DISBURSEMENT" : null,
        "P_AMT_INSTALLMENT" : null,
        "P_TENOR" : null,
        "P_TUJUAN_PENGGUNAAN" : null,
        "P_ID_USER_UPDATED" : "1",
        "P_STATUS" : null,
        "P_REASON" : null,
        "P_PENYEDIA" : null,
        "P_LEADS_ID" : null,
        "P_NO_REGISTRATION" : null,
        "P_PEFINDO_SCORE" : null,
        "P_PEFINDO_DETAIL" : null,
        "P_ID_SIMULATION" : null,
        "P_CD_BANK" : null,
        "P_ACCOUNT_NUMBER" : null,
        "P_ACCOUNT_NAME" : null,
        "P_BANK_NAME" : null,
        "P_EXP_STNK" : null,
        "P_FLAG_READ" : null,
        "P_SOURCE" : null,
        "P_FLAG_DISBURSEMENT" : null,
        "P_STATUS_MASKAPAI" : null,
        "P_NO_POLIS" : null,
        "P_AR_TLO" : null,
        "P_PLATFORM" : null,
        "P_STATUS_PERNIKAHAN" : null,
        "P_NO_NPWP" : null,
        "P_NO_KK" : null,
        "P_FLAG_BPKB" : null,
        "P_SIGNATURE" : "f0520be62240617148c28c7c38bab752fa837717a145a17c744f21ce522b0057"
    }
}
```

_Response (200 - OK)_
```json
{
    "out_stat": "T",
    "out_mess": "Berhasil Mengubah Data CMS"
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Terdapat Spesial karakter. Gagal Ubah Data"
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Gagal Mengubah Data CMS"
}
```

## POST /restv2/acccash/transactionplafond/getavlplafondacccash

> Admin CMS can check availability customer's plafond by input their agreement number or their car plate number

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doGetAvlPlafondAcccash" : {
        "P_LANGUAGE" : "IN",
        "P_INPUT" : "1"
    }
}
```

_Response (200 - OK)_
```json
{
    "out_stat": "T",
    "out_mess": "DATA BERHASIL"
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "TERJADI KESALAHAN"
}
```

## POST /restv2/acccash/transactionplafond/getlistplafondacccash

> On the Prioritas Dana Landing Page, customer will see their availability plafond cards

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doGetListPlafondAcccash" : {
        "P_LANGUAGE" : null,
        "P_NO_AGGR" : null
    }
}
```

_Response (200 - OK)_
```json
{
        "out_stat": "T",
        "out_mess": "DATA BERHASIL",
        "out_data": [
        {
            "NOMINAL": "8000000",
            "PRODUCT": "Upgrade Asuransi",
            "WORDING": "E-endorsement langsung terbit",
            "ID": "4",
            "FLAG_READ": "Y",
            "FLAG_CALCULATOR": "N",
            "SOURCE": "ENDORSEMENT",
            "STATUS_APPL": null
        }
    ]
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Terdapat spesial karakter, Gagal ubah data"
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "ERROR"
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Terjadi Kesalahan"
}
```

## POST /restv2/acccoid/gcm/getdetailgcmaccweb

> For content on the Prioritas Dana Landing Page

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doGetDetailGcmAccweb" : {
        "P_GUID" : "3166"
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "Success",
    "OUT_DATA": [
        {
            "GUID": "11001692",
            "CHAR_VALUE1": null,
            "CHAR_VALUE2": null,
            "DT_ADDED": "2021-11-17 10:30:03.0",
            "ID_USER_ADDED": "ADMIN",
            "DT_UPDATED": "2021-11-17 10:30:03.0",
            "ID_USER_UPDATED": null,
            "CONDITION": "DETAIL-CONTENT-ACCCASH",
            "FLAG_ACTIVE": "Y",
            "CHAR_DESC": "Pencairan maksimal 30 juta",
            "URL": null,
            "ID_HEAD": "3166",
            "CHAR_CONTENT": null,
            "META_DESCRIPTION": null,
            "META_KEYWORD": null,
            "META_TAG": null
        },
        {
            "GUID": "11001694",
            "CHAR_VALUE1": null,
            "CHAR_VALUE2": null,
            "DT_ADDED": "2021-11-17 10:32:38.0",
            "ID_USER_ADDED": "ADMIN",
            "DT_UPDATED": "2021-11-17 10:32:38.0",
            "ID_USER_UPDATED": null,
            "CONDITION": "DETAIL-CONTENT-ACCCASH",
            "FLAG_ACTIVE": "Y",
            "CHAR_DESC": "Cukup Lampirkan foto STNK dan 2 sisi mobil",
            "URL": null,
            "ID_HEAD": "3166",
            "CHAR_CONTENT": null,
            "META_DESCRIPTION": null,
            "META_KEYWORD": null,
            "META_TAG": null
        }
    ]
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Failed To Get Content"
}
```

## POST /restv2/acccoid/gcm/getcontentacccash

> For content on the Prioritas Dana Landing Page

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doGetContentAccCash": {
        "P_CATEGORY" :"CONTENT-ACCCASH",
        "P_CHAR_DESC": ""
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "Success",
    "OUT_DATA": [
        {
            "TITLE": "Pendanaan Jangka Pendek",
            "SUBTITLE": "Pendanaan dengan tenor singkat",
            "ID": "1",
            "DETAIL": [
                {
                    "ITEM": "Pencairan maksimal 30 juta"
                },
                {
                    "ITEM": "Cukup Lampirkan foto STNK dan 2 sisi mobil"
                }
            ]
        },
        {
            "TITLE": "Topup",
            "SUBTITLE": "Pendanaan dengan tenor sampai dengan 3 tahun",
            "ID": "2",
            "DETAIL": [
                {
                    "ITEM": "Pencairan lebih dari 30 juta"
                }
            ]
        },
        {
            "TITLE": "Pendanaan Baru",
            "SUBTITLE": "Pendanaan dengan tenor sampai dengan 3 tahun",
            "ID": "3",
            "DETAIL": [
                {
                    "ITEM": "Pencairan lebih besar dengan menggunakan jaminan baru"
                }
            ]
        },
        {
            "TITLE": "Upgrade Asuransi",
            "SUBTITLE": "Upgrade Asuransi kendara dari TLO ke All Risk dengan tenor singkat",
            "ID": "4",
            "DETAIL": [
                {
                    "ITEM": "E-endorsement langsung terbit"
                }
            ]
        }
    ]
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Data gagal diproses"
}
```

## POST /restv2/acccash/transactionplafond/checkautodebet

> For check if the customer using autodebet for payment their agreement with ACC in our database

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doCheckAutoDebet" : {
        "P_NO_AGGR" : "01200273001719964"
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "AUTO DEBET",
    "OUT_DATA": []
}
```

_Response (200)_
```json
{
    "OUT_STAT": "F",
    "OUT_MESS": "ERROR",
    "OUT_DATA": []
}
```

## POST /restv2/acccash/transactionplafond/checkplafondacccash

> To give the total plafond from all of products that available for one agreement number, and give a flag is it the agreement number already registered in ACC One

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doCheckPlafondAcccash" : {
        "P_LANGUAGE" : null,
        "P_INPUT" : "01100103005288849"
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "PROCES SUCCEDED",
    "OUT_DATA": [
        {
            "TOTAL_PLAFOND": "91560000",
            "FLAG_REGIS": "F"
        }
    ]
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Maaf, nomor kontrak tidak ditemukan. Silahkan periksa kembali"
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Maaf, kamu belum mendapatkan plafon atas kontrak ini"
}
```

_Response (200)_
```json
{
    "out_stat": "F",
    "out_mess": "Terdapat Spesial Karakter, Gagal Ubah Data"
}
```

## POST /restv2/acccash/transactionplafond/updateflagreadplafond

> Once customer open the cards list products there are on boarding message, and this API to update that the customer already read the message

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doUpdateFlagreadPlafond" : {
        "P_NO_AGGR" : "01100103005288849"
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "Success",
    "OUT_DATA": []
}
```

## POST /restv2/acccash/transactionplafond/getwordproductacccash

> For content on the Prioritas Dana Landing Page

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doGetWordProductAcccash" : {
        "P_PRODUCT_ID" : "1"
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "Success Get Content",
    "OUT_DATA": [
        {
            "PRODUCT_ID": "1",
            "PRODUCT": "Pendanaan Jangka Pendek",
            "CONTENT": "<h4>Pendanaan Jangka Pendek</h4>\n<p>Pendanaan dengan tenor sepanjang sisa tenor kontrak berjalan dengan pencairan sampai dengan 30 juta. Cukup lampirkan foto STNK dan 2 sisi mobil!</p>\n<p>&nbsp;</p>\n<h4>Bagaimana cara pencairannya?</h4>\n<ol>\n<li>Masukkan nominal pencairan (maksimal pencairan 30 juta)</li>\n<li>Pilih periode pembiayaan</li>\n<li>Pastikan informasi yang dimasukkan sudah sesuai (STNK wajib masih dalam keadaan berlaku)</li>\n</ol>"
        }
    ]
}
```

_Response (200)_
```json
{
    "OUT_STAT": "F",
    "OUT_MESS": "Something went wrong",
    "OUT_DATA": []
}
```

## POST /restv2/acccash/transactionplafond/checksourceacccash

> For checking the product source

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doCheckSourceAcccash" : {
        "P_NO_AGGR" : "01100102003550849"
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "DATA BERHASIL DIPROSES",
    "OUT_DATA": [
        {
            "SOURCE": "ENDORSEMENT"
        }
    ]
}
```

_Response (200)_
```json
{
    "OUT_STAT": "F",
    "OUT_MESS": "ERROR",
    "OUT_DATA": []
}
```

## POST /restv2/acccash/transactionplafond/checktopupacccash

> Check that the parent agreement already has child agreement or not

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doCheckTopupAcccash" : {
        "P_NO_AGGR" : null
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "Data ditemukan",
    "OUT_DATA": [
        {
            "LIST": "Pendanaan Jangka Pendek-01100103004798554"
        }
    ]
}
```

_Response (200)_
```json
{
    "OUT_STAT": "F",
    "OUT_MESS": "Data tidak ditemukan",
    "OUT_DATA": []
}
```

## POST /restv2/acccash/transactionplafond/getphoneacccash

> IF the customer input their car police, then they have to input their last 3 digit phone number

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doGetPhoneAcccash" : {
        "P_NOPOL" : "B1357UFY"
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "DATA DITEMUKAN",
    "OUT_DATA": [
        {
            "PHONE_NUMBER": "082111137XXX"
        }
    ]
}
```

_Response (200)_
```json
{
    "OUT_STAT": "F",
    "OUT_MESS": "TERJADI KESALAHAN",
    "OUT_DATA": []
}
```

## POST /restv2/acccash/transactionplafond/checkphoneacccash

> IF the customer input their car police, then they have to input their last 3 digit phone number

_Request Header_
```json
{
    "X-Content-Type-Options": "nosniff",
    "X-XSS-Protection": "1; mode=block",
    "Strict-Transport-Security": "max-age=31536000; includeSubDomains; preload",
    "X-Frame-Options": "SAMEORIGIN",
    "Content-Type": "application/json",
    "APIKey": "Rz5yS2oiT45Kio1WYOLO"
}
```

_Request Body_
```json
{
    "doCheckPhoneAcccash" : {
        "P_NOPOL" : "B1357UFY",
        "P_PHONE" : "777"
    }
}
```

_Response (200 - OK)_
```json
{
    "OUT_STAT": "T",
    "OUT_MESS": "DATA DITEMUKAN",
    "OUT_DATA": [
        {
            "NO_AGGR": "01100102003072169"
        }
    ]
}
```

_Response (200)_
```json
{
    "OUT_STAT": "F",
    "OUT_MESS": "TERJADI KESALAHAN",
    "OUT_DATA": []
}
```