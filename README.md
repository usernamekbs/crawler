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
    "sellerProductName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13",
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
            "id": 32619,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플라워영수증_동백",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146021,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플라워영수증_동백"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32620,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플라워영수증_목련",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146022,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플라워영수증_목련"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32621,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플라워영수증_데이지",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146023,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플라워영수증_데이지"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32622,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플라워영수증_튤립",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146024,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플라워영수증_튤립"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32623,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플라워영수증_장미",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146025,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플라워영수증_장미"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32624,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플라워영수증_라벤더",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146026,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플라워영수증_라벤더"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32625,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13트로피컬플로랄_핑크블로썸",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146027,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "트로피컬플로랄_핑크블로썸"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32626,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13트로피컬플로랄_러브",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146028,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "트로피컬플로랄_러브"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32627,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13트로피컬플로랄_헬로스윗",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146029,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "트로피컬플로랄_헬로스윗"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32628,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13트로피컬플로랄_어썸투데이",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146030,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "트로피컬플로랄_어썸투데이"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32629,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13트로피컬플로랄_굿데이",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146031,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "트로피컬플로랄_굿데이"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32630,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13클래식플라워_그린",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146032,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "클래식플라워_그린"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32631,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13클래식플라워_레드",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146033,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "클래식플라워_레드"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32632,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13클래식플라워_퍼플",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146034,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "클래식플라워_퍼플"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32633,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13클래식플라워_네이비",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146035,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "클래식플라워_네이비"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32634,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13클래식플라워_핑크",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146036,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "클래식플라워_핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32635,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13러블리튤립_블랙",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146037,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "러블리튤립_블랙"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32636,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13러블리튤립_화이트",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146038,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "러블리튤립_화이트"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32637,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13러블리튤립_민트",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146039,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "러블리튤립_민트"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32638,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13러블리튤립_퍼플",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146040,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "러블리튤립_퍼플"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32639,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13러블리튤립_핑크",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146041,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "러블리튤립_핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32640,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13러블리튤립_오렌지",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146042,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "러블리튤립_오렌지"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32641,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플로럴패턴_핑크",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146043,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플로럴패턴_핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32642,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플로럴패턴_네이비",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146044,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플로럴패턴_네이비"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32643,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플로럴패턴_옐로우",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146045,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플로럴패턴_옐로우"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32644,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13플로럴패턴_민트",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146046,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "플로럴패턴_민트"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32645,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13컬러팝튤립_핑크",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146047,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "컬러팝튤립_핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32646,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13컬러팝튤립_오렌지",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146048,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "컬러팝튤립_오렌지"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32647,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13컬러팝튤립_네이비",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146049,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "컬러팝튤립_네이비"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32648,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13컬러팝튤립_옐로우",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146050,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "컬러팝튤립_옐로우"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32649,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13컬러팝튤립_스카이",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146051,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "컬러팝튤립_스카이"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32650,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔도트_핑크",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146052,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔도트_핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32651,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔도트_베이지",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146053,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔도트_베이지"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32652,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔도트_퍼플",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146054,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔도트_퍼플"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32653,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔도트_블루",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146055,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔도트_블루"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32654,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13스몰도트_핑크",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146056,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "스몰도트_핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32655,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13스몰도트_아이보리",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146057,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "스몰도트_아이보리"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32656,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13스몰도트_민트",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146058,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "스몰도트_민트"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32657,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13스몰도트_네이비",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146059,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "스몰도트_네이비"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32658,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔레터링_핑크",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146060,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔레터링_핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32659,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔레터링_블루",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146061,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔레터링_블루"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32660,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔레터링_베이지",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146062,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔레터링_베이지"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32661,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔레터링_민트",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146063,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔레터링_민트"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32662,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔레터링_연핑크",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146064,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔레터링_연핑크"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        },
        {
            "id": 32663,
            "itemName": "[Trycozy]트라이코지 맥세이프 충전기 하드케이스 모음 시즌13파스텔레터링_블랙",
            "originalPrice": 18000,
            "salePrice": 18000,
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
                    "id": 146065,
                    "attributeTypeName": "옵션",
                    "attributeValueName": "파스텔레터링_블랙"
                }
            ],
            "contents": [
                {
                    "contentsType": "TEXT",
                    "contentDetails": [
                        {
                            "content": "<p style='color:red; font-size: medium;' align=\"center\">주문 제작 상품입니다. 출고 소요일 까지 약 2일 정도 소요됩니다 주문 제작 상품이라 반품이 어렵습니다! 제품에 하자가 있을 시에만 반품 가능합니다</p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/download.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-1_shop1_145947.jpeg'/></p><p align=\"center\"><img src='https://qudtn0295.cafe24.com/detailImage25/트라이코지 맥세이프 충전기 하드케이스_시즌13-2_shop1_145947.jpeg'/></p>",
                            "detailType": "TEXT"
                        }
                    ]
                }
            ]
        }
    ]
}
