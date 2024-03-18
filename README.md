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
    "sellerProductName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스",
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
            "id": 10737,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스-------------------",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10738,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스갤럭시Z플립5(F731)",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [
                {
                    "id": 124768,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z플립5(F731)"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10739,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스갤럭시Z플립4(F721)",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [
                {
                    "id": 124769,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z플립4(F721)"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10740,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스갤럭시Z플립3(F711)",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [
                {
                    "id": 124770,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "갤럭시Z플립3(F711)"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10741,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스-------------------",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10742,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스로얄블루",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [
                {
                    "id": 124771,
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "로얄블루"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10743,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스딥그레이",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [
                {
                    "id": 124772,
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "딥그레이"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10744,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스진핑크",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [
                {
                    "id": 124773,
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "진핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10745,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스연보라",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [
                {
                    "id": 124774,
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "연보라"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 10746,
            "itemName": "[TryCozy]트라이코지 러브러브 레터링 미러 스마트톡 갤럭시Z플립시리즈 카드 3D곡면하드케이스블랙",
            "originalPrice": 26000,
            "salePrice": 26000,
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
                    "cdnPath": null,
                    "vendorPath": null
                }
            ],
            "attributes": [
                {
                    "id": 124775,
                    "attributeTypeName": "옵션2",
                    "attributeValueName": "블랙"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/3D_notice.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/상판 디테일 변경 공지.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/Z플립4_카드하드 동영상.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지_러브러브 레터링_Z플립 카드하드 미러 스마트톡.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        }
    ]
}
