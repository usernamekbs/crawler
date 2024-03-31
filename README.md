# crawler
https://developers.coupangcorp.com/hc/ko/articles/360033877853-%EC%83%81%ED%92%88-%EC%83%9D%EC%84%B1 << 쿠팡 상품 생성 API 

셀레니움으로 데이터 읽어오는건 완벽하게 됩니다.

WEBP확장자의 이미지 또한 읽어오는 작업이 가능합니다.

SELENIUM으로 데이터 크롤링 이후 쿠팡 상품 생성API를 데이터화 해봤습니다.

참고 : 쿠팡은 옵션을 기준으로 상품 상세페이지가 나눠지게됩니다.

옵션1이 10개이고 옵션2가 10개이면 해당 옵션은 총 100개가 됩니다.

옵션1이 20개이고 옵션2가 20개이면 총 400개의 옵션을 가지게 됩니다.

그래서 옵션이 더 많아질 경우를 대비해 해당 옵션을 기준으로 상품 상세페이지를 나눠주는 작업을 진행중에있습니다.

옵션이 400개면 200개 200개 상품상세페이지 2개 로 보내겠다는 의미입니다.

쿠팡은 하루 최대 5000개만 보낼 수 있습니다 

쿠팡의 옵션의 최대개수는 200개이고 ITEMS는 쿠팡의 옵션 개수만큼 가지게 됩니다.

ITEMNAME은 유니크한 값을 가져야 하기때문에 상품이름 + OPTION으로 지정했습니다.

참고로 어떤 사이트든 옵션은 중복값이 존재할수없습니다.

쿠팡은 옵션(SLEECTBOX)를 4개이상 가지지 못합니다.

IMAGES는 썸네일,이미지 추가목록을 의미합니다.

ENUM으로 REPRESENTATION 데이터를 선택해서 사용이 가능합니다.

CONTENTS는 상세페이지 이미지들을 의미합니다.

HTML태그로 글자로도 채워넣는게가능 합니다.

현재 SELENIUM으로 쿠팡 데이터를 전송하는게 완벽하지는 안습니다.

옵션 부분을 해결만 한다면 그때 부터는 문제없이 해결이 가능할거같습니다.

{
    "sellerProductName": "[TryCozy]트라이코지 말랑말랑 키치 레터링 갤럭시Z폴드시리즈 하드케이스",
    "vendorId": "A00962060",
    "saleStartedAt": "2024-01-19T00:00:00",
    "saleEndedAt": "2099-01-19T00:00:00",
    "displayProductName": null,
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
            "id": 36631,
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
                    "id": 349998,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "id": 349999,
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
            "id": 36632,
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
                    "id": 350000,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "id": 350001,
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
            "id": 36633,
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
                    "id": 350002,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "id": 350003,
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
            "id": 36634,
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
                    "id": 350004,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "id": 350005,
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
            "id": 36635,
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
                    "id": 350006,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "id": 350007,
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
            "id": 36636,
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
                    "id": 350008,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드2(F916)"
                },
                {
                    "id": 350009,
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
            "id": 36637,
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
                    "id": 350010,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "id": 350011,
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
            "id": 36638,
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
                    "id": 350012,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "id": 350013,
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
            "id": 36639,
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
                    "id": 350015,
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "러브"
                },
                {
                    "id": 350014,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
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
            "id": 36640,
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
                    "id": 350016,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "id": 350017,
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
            "id": 36641,
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
                    "id": 350018,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "id": 350019,
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
            "id": 36642,
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
                    "id": 350020,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드3(F926)"
                },
                {
                    "id": 350021,
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
            "id": 36643,
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
                    "id": 350022,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "id": 350023,
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
            "id": 36644,
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
                    "id": 350024,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "id": 350025,
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
            "id": 36645,
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
                    "id": 350026,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "id": 350027,
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
            "id": 36646,
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
                    "id": 350028,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "id": 350029,
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
            "id": 36647,
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
                    "id": 350030,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "id": 350031,
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
            "id": 36648,
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
                    "id": 350032,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드4(F936)"
                },
                {
                    "id": 350033,
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
            "id": 36649,
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
                    "id": 350034,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "id": 350035,
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
            "id": 36650,
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
                    "id": 350036,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "id": 350037,
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
            "id": 36651,
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
                    "id": 350038,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "id": 350039,
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
            "id": 36652,
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
                    "id": 350040,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "id": 350041,
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
            "id": 36653,
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
                    "id": 350042,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "id": 350043,
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
            "id": 36654,
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
                    "id": 350044,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z폴드5(F946)"
                },
                {
                    "id": 350045,
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
