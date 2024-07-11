# 스크래핑
<pre>
    대부분은 스크래핑 관련된건 python을 사용하고 파이썬에는 https://wikidocs.net/198941 이러한 프레임워크 ? 등이있는걸로 알고있습니다.
    저는 파이썬을 모르기 때문에 자바로 할 수있는 방법이 뭐가있을까 고민을 하다가 selenium으로 처리하게됐습니다.(아파치 넛츠도 있습니다)
    https://developers.coupangcorp.com/hc/ko/articles/360033877853-%EC%83%81%ED%92%88-%EC%83%9D%EC%84%B1
    << 해당 링크는 쿠팡 상품 생성 api 입니다.이 데이터를 토대로 상품 생성 api로 만들었습니다.(아래가 json 데이터입니다)
</pre>
<pre>
    https://www.coupang.com/vp/products/8220541336?itemId=23626101518&vendorItemId=90651620794&q=%5B%EC%BB%A4%EB%B2%84%ED%95%8F%5D%EC%BF%BC%EC%B9%B4+%ED%94%8C%EB%9D%BC%EC%9B%8C+%EC%82%AC%ED%94%BC%EC%95%84%EB%85%B8+%EB%8B%A4%EC%9D%B4%EC%96%B4%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%8A%A4&itemsCount=36&searchId=e44402f58e424c31a6c518518434fe58&rank=1&isAddedCart= 
    <<해당 상품도 올렸습니다.
</pre>
<pre>
    올린상품이 매우많습니다 모두 selenium으로 도매사이트에 상품정보를 읽어와 db에 저장을 했고 저장한 데이터를 coupang_api 상품 생성 json형식으로 
    모두 출력했습니다. 
    사용한기술은 java,jpa,postgresql 등이 있습니다.
    여러 문제들도 많았습니다.
    쿠팡은 상품 1개가있으면 옵션 개수가 최대 200개만 전송이 될수잇습니다.
    fetch join을 사용하면 paging을 사용할수없는 https://junhyunny.github.io/spring-boot/jpa/jpa-fetch-join-paging-problem/ 문제또한 있었습니다.
    페이징을 사용못하는 상황에 맞닥뜨리게 되기도합니다. (memory.. 에러)
    이문제를 해결하기위해서 fetchjoin을 사용하지않고 페이징 처리를 햇습니다.
    사실 이문제 말고도 여러가지 문제 사항들이 좀 있었습니다.
    모두 해결 하고 아래와 같이 jpa를 통해서 모두 보낼수있게되었습니다.
    
    또 selenium은 대용량으로 데이터를 읽어오기엔 적합하지 않은 라이브러리로 알고있습니다.
    그래서 셀리니움 이용시에는 페이징을 최대 100페이지만 잡아두고 크롤링을 할까 생각중에있습니다.
</pre>
<pre>
    폰케이스 도매사이트를 크롤링한이유 ? (폰 케이스는 옵션 정보가 매우많습니다 옵션 정보가 많으면 더 노출될 확률이 올라가요 ) 
</pre>
<PRE>
    아래 json 데이터에 상세이미지를 삭제한 상태입니다. 
    저는 제 local pc에 이미지를 저장하고 그 이미지를 
    카페 24 ftp에 올리기 때문에
    다른 상품을 올릴때 해당 ftp에서 이미지 데이터를 삭제하고 다시올립니다.
    하지만 쿠팡에서는 상세이미지가 잘보입니다.
    쿠팡 서버에 전송을 하게 되면 쿠팡 서버에 올라가기 때문에
    저는 ftp에 있는 이미지만 삭제하고 다시올리고 합니다.
    이런 방식을 이용해 저는 매우 간편하게 쿠팡에 상품 업로드를 하고 있습니다.
</PRE>
<pre>
    소스 배포는 어렵습니다.
    쿠팡은 모두 끝났고 
    이제 11번가에 데이터를 전송 해볼까 합니다.
    감사합니다.
</pre>
https://coupang.com/vm/products/7998889347 <<영상으로 찍은 데이터 쿠팡에 올린상품입니다.
https://coupang.com/vm/products/7992412669 <<영상으로 찍은 데이터 쿠팡에 올린상품입니다.
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
