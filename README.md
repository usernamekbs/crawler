# crawler
https://developers.coupangcorp.com/hc/ko/articles/360033877853-%EC%83%81%ED%92%88-%EC%83%9D%EC%84%B1 << 쿠팡 상품 생성 API 

<PRE style="color:blue;">현재는 상세이미지를 삭제한 상태입니다. 다른 상품을 올릴때 해당 ftp에서 이미지 데이터를 삭제하고 다시올립니다.</PRE>
<PRE>

쿠팡은 아이템 같은 상품이면 아이템 위너로 묶이는 현상이 있습니다.
저 같은경우는 데이터를 변경하여 상품등록을 합니다.
타이틀을 바꾸고 이미지의 확장자,용량,width,height등을 일괄적으로 변경하다보니 위너 상품만 27만개 정도가있습니다.
위너가 아닌상품은 2만개 정도있습니다.
이것만 봐도 데이터를 변경하면 어떠한 이점이 있는지 확인할 수  있습니다.
위너에 묶이지 않고 상품을 등록하는건 쿠팡에서는 매우 중요하다고 생각합니다. 
</PRE>
https://coupang.com/vm/products/7998889347 <<영상으로 찍은 데이터 쿠팡에 올린상품입니다.
https://coupang.com/vm/products/7992412669 <<영상으로 찍은 데이터 쿠팡에 올린상품입니다.
<PRE>
JPA를 사용했습니다.
셀레니움으로 읽어온 도매 데이터를 
쿠팡 API에 전송 할 수있는 데이터로 만들어봤습니다. 
쿠팡은 gif파일을 허용하지 않습니다.
쿠팡 업로드시 고려해야 할 사항이 Coupang Api를 보면 상당히 많이있습니다.
그중에서 가장 어렵다고 생각했던걸 적어보려합니다.
쿠팡 API는 SELECT BOX를 3개까지만 생성이 가능합니다.
옵션에 개수는 최대 200개입니다.
만약 SELECT BOX 1,2,3이있고 
옵션에 개수가 2개,2개,2개가 잇다면 최대 8개의 옵션의 개수를 가지게 됩니다.(중첩 포문과 똑같음)
그래서 포문이 상당히 많이 필요하게 되서 이 포문을 줄일 수 있는 방법을 찾게되었습니다.
RECURSIVE 입니다. RECURSIVE를 이용해 소스에 길이를 매우 줄였고
해당 옵션 정보를 읽어올 때 BATCH SIZE를 이용해서 일괄 인설트가 되게 변경도 했습니다.
아래가 SELENIUM으로 읽어온 데이터이고 이 데이터를 COUPANG API에 전송하는게 가능합니다.
감사합니다.
</PRE>
<PRE>
{
    "sellerProductName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스",
    "vendorId": "A00962060",
    "saleStartedAt": "2024-01-19T00:00:00",
    "saleEndedAt": "2099-01-19T00:00:00",
    "displayProductName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스",
    "deliveryMethod": "SEQUENCIAL",
    "deliveryCompanyCode": "EPOST",
    "deliveryChargeType": "NOT_FREE",
    "deliveryCharge": 3000,
    "freeShipOverAmount": 30000,
    "deliveryChargeOnReturn": 3000,
    "remoteAreaDeliverable": "N",
    "unionDeliveryType": "NOT_UNION_DELIVERY",
    "returnCenterCode": "1001694769",
    "returnChargeName": "경기도 안산시 상록구 충장로 565 111동1203호",
    "companyContactNumber": "010-8900-6085",
    "returnZipCode": "15287",
    "returnAddress": "경기도 안산시 상록구 충장로 565",
    "returnAddressDetail": "111동1203호",
    "returnCharge": 3000,
    "outboundShippingPlaceCode": 19389011,
    "vendorUserId": "qudtn0295",
    "requested": true,
    "items": [
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드2(F916)헬로",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "헬로"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드2(F916)와우",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "와우"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드2(F916)러브",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "러브"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드2(F916)굿",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "굿"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드2(F916)투데이",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "투데이"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드2(F916)붐",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "붐"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드3(F926)헬로",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "헬로"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드3(F926)와우",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "와우"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드3(F926)러브",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "러브"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드3(F926)굿",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "굿"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드3(F926)투데이",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "투데이"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드3(F926)붐",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "붐"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드4(F936)헬로",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "헬로"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드4(F936)와우",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "와우"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드4(F936)러브",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "러브"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드4(F936)굿",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "굿"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드4(F936)투데이",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "투데이"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드4(F936)붐",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "붐"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드5(F946)헬로",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "헬로"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드5(F946)와우",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "와우"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드5(F946)러브",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "러브"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드5(F946)굿",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "굿"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드5(F946)투데이",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "투데이"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "itemName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스갤럭시Z폴드5(F946)붐",
            "originalPrice": 23100,
            "salePrice": 23100,
            "maximumBuyCount": 10,
            "maximumBuyForPerson": 0,
            "maximumBuyForPersonPeriod": 1,
            "outboundShippingTimeDay": 2,
            "unitCount": 0,
            "adultOnly": "EVERYONE",
            "taxType": "TAX",
            "parallelImported": "NOT_PARALLEL_IMPORTED",
            "overseasPurchased": "NOT_OVERSEAS_PURCHASED",
            "pccNeeded": false,
            "images": [
                {
                    "imageOrder": 0,
                    "imageType": "REPRESENTATION",
                    "vendorPath": "https://qudtn0295.cafe24.com/web/product/big/thmb70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.png"
                }
            ],
            "attributes": [
                {
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "붐"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/트라이코지_말랑말랑 키치 레터링_Z폴드 하드.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage70/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        }
    ]
}</PRE>
