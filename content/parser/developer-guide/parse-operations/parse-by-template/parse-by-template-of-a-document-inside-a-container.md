---
id: "parse-by-template-of-a-document-inside-a-container"
url: "parser/parse-by-template-of-a-document-inside-a-container"
title: "Parse by Template of a Document Inside a Container"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

This REST API allows extracting fields and tables from a document placed in a container like ZIP archive, emails, PDF portfolios, etc. by specifying the ContainerItemInfo parameter.

The following example demonstrates how to extract data from a container item. Here you can see how to parse text fields by regular expressions and a table inside the container item document.

## Resource

The following GroupDocs.Parser Cloud REST API resource has been used in the [Parse by Template of a document inside a container](https://apireference.groupdocs.cloud/parser/#/Template) example.

## cURL example

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The client credentials are taken from environment variables.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to parse a document
curl -v "https://api.groupdocs.cloud/v1.0/parser/parse" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
        "FilePath": "containers/archive/sample.zip"
    },
    "TemplatePath": "templates/template-for-companies.json",
    "ContainerItemInfo": {
        "RelativePath": "companies.docx"
    }
}'
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The client credentials are taken from environment variables.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to parse a document
curl.exe -v "https://api.groupdocs.cloud/v1.0/parser/parse" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{ 'FileInfo': { 'FilePath': 'containers/archive/sample.zip' }, 'TemplatePath': 'templates/template-for-companies.json', 'ContainerItemInfo': { 'RelativePath': 'companies.docx' } }"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
rem First get JSON Web Token
rem Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
rem The client credentials are taken from environment variables.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

rem cURL example to parse a document
curl -v "https://api.groupdocs.cloud/v1.0/parser/parse" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"containers/archive/sample.zip\"},\"TemplatePath\":\"templates/template-for-companies.json\",\"ContainerItemInfo\":{\"RelativePath\":\"companies.docx\"}}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "count": 5,
    "fieldsData": [
        {
            "name": "ADDRESS",
            "pageIndex": 0,
            "pageArea": {
                "rectangle": {
                    "position": {
                        "x": 85.050003051757813,
                        "y": 79.191001892089844
                    },
                    "size": {
                        "height": 13.428000450134277,
                        "width": 82.430992126464844
                    },
                    "coordinates": {
                        "top": 79.191001892089844,
                        "bottom": 92.619002342224121,
                        "left": 85.050003051757813,
                        "right": 167.48099517822266
                    }
                },
                "page": {
                    "index": 0,
                    "size": {
                        "height": 841.9000244140625,
                        "width": 595.29998779296875
                    }
                },
                "pageTextArea": {
                    "text": "Company address:",
                    "baseLine": 92.619002342224121,
                    "areas": []
                }
            }
        },
        {
            "name": "COMPANYADDRESS",
            "pageIndex": 0,
            "pageArea": {
                "rectangle": {
                    "position": {
                        "x": 169.96800231933594,
                        "y": 79.191001892089844
                    },
                    "size": {
                        "height": 13.428000450134277,
                        "width": 98.3180046081543
                    },
                    "coordinates": {
                        "top": 79.191001892089844,
                        "bottom": 92.619002342224121,
                        "left": 169.96800231933594,
                        "right": 268.28600692749023
                    }
                },
                "page": {
                    "index": 0,
                    "size": {
                        "height": 841.9000244140625,
                        "width": 595.29998779296875
                    }
                },
                "pageTextArea": {
                    "text": "address of the Aspose",
                    "baseLine": 92.619002342224121,
                    "areas": [
                        {
                            "text": "address",
                            "baseLine": 92.619002342224121,
                            "areas": []
                        },
                        {
                            "text": "of",
                            "baseLine": 92.619002342224121,
                            "areas": []
                        },
                        {
                            "text": "the",
                            "baseLine": 92.619002342224121,
                            "areas": []
                        },
                        {
                            "text": "Aspose",
                            "baseLine": 92.619002342224121,
                            "areas": []
                        }
                    ]
                }
            },
            "linkedField": {
                "name": "ADDRESS",
                "pageIndex": 0,
                "pageArea": {
                    "rectangle": {
                        "position": {
                            "x": 85.050003051757813,
                            "y": 79.191001892089844
                        },
                        "size": {
                            "height": 13.428000450134277,
                            "width": 82.430992126464844
                        },
                        "coordinates": {
                            "top": 79.191001892089844,
                            "bottom": 92.619002342224121,
                            "left": 85.050003051757813,
                            "right": 167.48099517822266
                        }
                    },
                    "page": {
                        "index": 0,
                        "size": {
                            "height": 841.9000244140625,
                            "width": 595.29998779296875
                        }
                    },
                    "pageTextArea": {
                        "text": "Company address:",
                        "baseLine": 92.619002342224121,
                        "areas": []
                    }
                }
            }
        },
        {
            "name": "COMPANY",
            "pageIndex": 0,
            "pageArea": {
                "rectangle": {
                    "position": {
                        "x": 85.050003051757813,
                        "y": 56.700000762939453
                    },
                    "size": {
                        "height": 13.428000450134277,
                        "width": 72.998994827270508
                    },
                    "coordinates": {
                        "top": 56.700000762939453,
                        "bottom": 70.12800121307373,
                        "left": 85.050003051757813,
                        "right": 158.04899787902832
                    }
                },
                "page": {
                    "index": 0,
                    "size": {
                        "height": 841.9000244140625,
                        "width": 595.29998779296875
                    }
                },
                "pageTextArea": {
                    "text": "Company name:",
                    "baseLine": 70.12800121307373,
                    "areas": []
                }
            }
        },
        {
            "name": "COMPANYNAME",
            "pageIndex": 0,
            "pageArea": {
                "rectangle": {
                    "position": {
                        "x": 160.53599548339844,
                        "y": 56.700000762939453
                    },
                    "size": {
                        "height": 13.428000450134277,
                        "width": 32.021999359130859
                    },
                    "coordinates": {
                        "top": 56.700000762939453,
                        "bottom": 70.12800121307373,
                        "left": 160.53599548339844,
                        "right": 192.5579948425293
                    }
                },
                "page": {
                    "index": 0,
                    "size": {
                        "height": 841.9000244140625,
                        "width": 595.29998779296875
                    }
                },
                "pageTextArea": {
                    "text": "Aspose",
                    "baseLine": 70.12800121307373,
                    "areas": [
                        {
                            "text": "Aspose",
                            "baseLine": 70.12800121307373,
                            "areas": []
                        }
                    ]
                }
            },
            "linkedField": {
                "name": "COMPANY",
                "pageIndex": 0,
                "pageArea": {
                    "rectangle": {
                        "position": {
                            "x": 85.050003051757813,
                            "y": 56.700000762939453
                        },
                        "size": {
                            "height": 13.428000450134277,
                            "width": 72.998994827270508
                        },
                        "coordinates": {
                            "top": 56.700000762939453,
                            "bottom": 70.12800121307373,
                            "left": 85.050003051757813,
                            "right": 158.04899787902832
                        }
                    },
                    "page": {
                        "index": 0,
                        "size": {
                            "height": 841.9000244140625,
                            "width": 595.29998779296875
                        }
                    },
                    "pageTextArea": {
                        "text": "Company name:",
                        "baseLine": 70.12800121307373,
                        "areas": []
                    }
                }
            }
        },
        {
            "name": "COMPANIES",
            "pageIndex": 0,
            "pageArea": {
                "rectangle": {
                    "position": {
                        "x": 90.699996948242188,
                        "y": 124.67299652099609
                    },
                    "size": {
                        "height": 27.356001853942871,
                        "width": 331.91801071166992
                    },
                    "coordinates": {
                        "top": 124.67299652099609,
                        "bottom": 152.02899837493896,
                        "left": 90.699996948242188,
                        "right": 422.61800765991211
                    }
                },
                "page": {
                    "index": 0,
                    "size": {
                        "height": 841.9000244140625,
                        "width": 595.29998779296875
                    }
                },
                "pageTableArea": {
                    "rowCount": 1,
                    "columnCount": 2,
                    "pageTableAreaCells": [
                        {
                            "columnIndex": 0,
                            "columnSpan": 1,
                            "pageArea": {
                                "rectangle": {
                                    "position": {
                                        "x": 90.699996948242188,
                                        "y": 124.67299652099609
                                    },
                                    "size": {
                                        "height": 27.356001853942871,
                                        "width": 32.021999359130859
                                    },
                                    "coordinates": {
                                        "top": 124.67299652099609,
                                        "bottom": 152.02899837493896,
                                        "left": 90.699996948242188,
                                        "right": 122.72199630737305
                                    }
                                },
                                "page": {
                                    "index": 0,
                                    "size": {
                                        "height": 841.9000244140625,
                                        "width": 595.29998779296875
                                    }
                                },
                                "pageTextArea": {
                                    "text": "Name\r\nAspose",
                                    "baseLine": 152.02899837493896,
                                    "areas": [
                                        {
                                            "text": "Name",
                                            "baseLine": 138.10099697113037,
                                            "areas": []
                                        },
                                        {
                                            "text": "Aspose",
                                            "baseLine": 152.02899837493896,
                                            "areas": []
                                        }
                                    ]
                                }
                            },
                            "rowIndex": 0,
                            "rowSpan": 1
                        },
                        {
                            "columnIndex": 1,
                            "columnSpan": 1,
                            "pageArea": {
                                "rectangle": {
                                    "position": {
                                        "x": 324.29998779296875,
                                        "y": 124.67299652099609
                                    },
                                    "size": {
                                        "height": 27.356001853942871,
                                        "width": 98.318019866943359
                                    },
                                    "coordinates": {
                                        "top": 124.67299652099609,
                                        "bottom": 152.02899837493896,
                                        "left": 324.29998779296875,
                                        "right": 422.61800765991211
                                    }
                                },
                                "page": {
                                    "index": 0,
                                    "size": {
                                        "height": 841.9000244140625,
                                        "width": 595.29998779296875
                                    }
                                },
                                "pageTextArea": {
                                    "text": "Address\r\naddress of the Aspose",
                                    "baseLine": 152.02899837493896,
                                    "areas": [
                                        {
                                            "text": "Address",
                                            "baseLine": 138.10099697113037,
                                            "areas": []
                                        },
                                        {
                                            "text": "address",
                                            "baseLine": 152.02899837493896,
                                            "areas": []
                                        },
                                        {
                                            "text": "of",
                                            "baseLine": 152.02899837493896,
                                            "areas": []
                                        },
                                        {
                                            "text": "the",
                                            "baseLine": 152.02899837493896,
                                            "areas": []
                                        },
                                        {
                                            "text": "Aspose",
                                            "baseLine": 152.02899837493896,
                                            "areas": []
                                        }
                                    ]
                                }
                            },
                            "rowIndex": 0,
                            "rowSpan": 1
                        }
                    ]
                }
            }
        }
    ]
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Parser API](https://apireference.groupdocs.cloud/parser/#/Parse) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Parse_by_Template_document_inside_container.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Parse_by_Template_document_inside_container.java >}}
{{< /tab >}}
{{< /tabs >}}
