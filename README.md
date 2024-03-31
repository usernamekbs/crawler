# crawler
https://developers.coupangcorp.com/hc/ko/articles/360033877853-%EC%83%81%ED%92%88-%EC%83%9D%EC%84%B1 << 쿠팡 상품 생성 API 

https://coupang.com/vm/products/7998889347 <<영상으로 찍은 데이터 쿠팡에 올린상품입니다.
https://coupang.com/vm/products/7992412669 <<영상으로 찍은 데이터 쿠팡에 올린상품입니다.

셀레니움으로 읽어온 도매 데이터를 
쿠팡 API에 전송 할 수있는 데이터로 만들어봤습니다. 
쿠팡이나 11번가 등과 같은 플랫폼들은 gif파일을 허용하지 안습니다.
제가 읽어온 도매사이트에 꽤 많은 썸네일 이미지들이 gif로 되어있을겁니다.
실제로 영상에서도 gif파일들만 있었고요 
이 데이터를 png나 jpg로 변환하지 안으면 쿠팡에 올리는게 불가합니다.
또 이미지의 크기는 500px 500px을 맞춰야합니다.
상세이미지는 5000px 5000px을 넘어가면 안돼서 5000 5000으로 고정해뒀습니다.
이런 이유 때문에 이미지의 확장자를 변환하고 크기를 변환해야 했습니다.
카페 24에 ftp 글자 수는 50자 이상 넘어가면 안됩니다. 
50자가 넘어가게 하지 않기 위해서 uuid로 변환을 했습니다.중복 문제도 어느정도 해결이 가능합니다.(파일업로드를 할 때 문제가 없게 하기위해서) uuid는 50자가 넘지 안습니다.
쿠팡은 옵션을 중심으로 상세페이지가 나눠지게 됩니다.
그래서 옵션을 중심으로 데이터를 구조화 하는데에 있어서 시간이 조금 오래걸렸습니다.
덕분에 많이 배우기도 한거같습니다.
사실 여러가지로 문제가 많았습니다.webp확장자는 bufferdimage가 읽지를 못합니다.
이문제에 대해서도 꽤 오랜시간이 걸려서 해결을 햇습니다.
특이한 경험이었지만 나름 만족하고있습니다.
추후에 개선할 작업은 자바 스케쥴러를 이용해 12시에 하루 5천개의 데이터를 쿠팡에 보내려고 하고있습니다.(현재는 제 아이디만 보내고있지만 다른사람들도 보내려고 하고있습니다!)
당연히 중복된 데이터는 보내지 안을것입니다. 그래서 해당 사이트에있는 모든 데이터를 db화하는게 목적에있습니다.
감사합니다.
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
}
