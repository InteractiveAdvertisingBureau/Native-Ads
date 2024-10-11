# ***8*** ***Implementation*** ***Notes***

## ***8.1*** ***Multi*** ***Placement*** ***Bid*** ***Requests***

 If the bid request has a placement count (“plcmtcnt”) greater than 1,
 then the implication is that the bidder is submitting bids to a
 Generalized Second Price auction where multiple identical placements
 are being offered in the same content feed or stream.

 Example If a bid request is for 5 ad placements within a feed based
 layout. The bidder can return 1-5 bids. The exchange runs a
 generalized second price auction across these bids. The bidder can
 potentially win between 0-5 placements in the auction.

 An example bid response would look like

```javascript
 {
   "id": "1234567890",
   "seatbid": [{
     "bid": [{
     "id": "1",
     "impid": "1",
     "price": 10,
     "nurl": "http://adserver.com/WinNoticeUrlThatReturnsNative1",
     "adm":"<native response>"
   },
     "bid": \[{
     "id": "2",
     "impid": "1",
     "price": 20,
     "nurl": "http://adserver.com/WinNoticeUrlThatReturnsNative2"
     "adm":"<native response>"
   }]
 }]
}
```
