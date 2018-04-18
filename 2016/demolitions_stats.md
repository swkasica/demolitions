  1. PermitType
	<class 'str'>
	Nulls: False
	Values: DS, BP, EP, PP, MP
  2. PermitTypeDesc
	<class 'str'>
	Nulls: False
	Values: Driveway / Sidewalks, Mechanical Permit, Plumbing Permit, Electrical Permit, Building Permit
  3. PermitNum
	<class 'str'>
	Nulls: False
	Unique values: 27557
	Max length: 14
  4. PermitClass
	<class 'str'>
	Nulls: True
	Unique values: 29
	5 most frequent values:
		R- 434 Addition & Alterations:	13111
		R- 645 Demolition One Family Homes:	7342
		C- 649 Demolition All Other Bldgs Com:	2681
		R- 435 Renovations/Remodel:	1820
		R- 649 Demolition All Other Bldgs Res:	1797
	Max length: 40
  5. WorkClass
	<class 'str'>
	Nulls: True
	Unique values: 13
	5 most frequent values:
		Demolition:	12148
		Addition and Remodel:	10954
		Addition:	2176
		Remodel:	1810
		New:	248
	Max length: 20
  6. Condominium
	<class 'bool'>
	Nulls: True
	Unique values: 1
	5 most frequent values:
		False:	25871
  7. ProjectName
	<class 'str'>
	Nulls: True
	Unique values: 14161
	5 most frequent values:
		7337 MANCHACA RD:	20
		12610 BRODIE LN:	19
		206 E ELIZABETH ST:	17
		2401 S LAKESHORE BLVD:	16
		2900 MANOR RD:	15
	Max length: 54
  8. Description
	<class 'str'>
	Nulls: False
	Unique values: 12779
	5 most frequent values:
		Demolish Residence:	653
		Demo Sf Residence:	203
		Demo Sf Res:	177
		Demolish Commercial Building:	123
		Total demo of home:	114
	Max length: 1509
  9. TCAD_ID
	<class 'str'>
	Nulls: True
	Unique values: 12234
	5 most frequent values:
		WCAD:	101
		0233100220:	55
		0300010501:	39
		0315310601:	29
		0221021115:	26
	Max length: 10
 10. PropertyLegalDescription
	<class 'str'>
	Nulls: True
	Unique values: 8285
	5 most frequent values:
		Lot 2 Block   Subdivision:	75
		Lot 4 Block   Subdivision:	62
		Lot 6 Block   Subdivision:	61
		Lot   Block   Subdivision:	50
		Lot 8 Block   Subdivision:	46
	Max length: 151
 11. AppliedDate
	<class 'datetime.date'>
	Nulls: False
	Min: 1978-05-04
	Max: 2016-04-08
	Unique values: 4854
	5 most frequent values:
		2013-08-28:	77
		2015-05-13:	76
		1996-07-16:	75
		2015-09-30:	64
		2014-02-19:	59
 12. IssuedDate
	<class 'datetime.date'>
	Nulls: False
	Min: 1978-05-04
	Max: 2016-04-13
	Unique values: 5134
	5 most frequent values:
		1996-07-16:	75
		2005-12-07:	58
		2015-03-30:	49
		1996-12-12:	43
		2016-02-11:	35
 13. DayIssued
	<class 'str'>
	Nulls: False
	Unique values: 7
	5 most frequent values:
		WEDNESDAY:	5951
		TUESDAY:	5698
		THURSDAY:	5378
		FRIDAY:	5374
		MONDAY:	5076
	Max length: 9
 14. CalendarYearIssued
	<class 'int'>
	Nulls: False
	Min: 1978
	Max: 2016
	Sum: 55356676
	Mean: 2008.8063287005116
	Median: 2012
	Standard Deviation: 8.068849901075506
	Unique values: 38
	5 most frequent values:
		2015:	3878
		2014:	3435
		2013:	2820
		2012:	2624
		2011:	2392
 15. FiscalYearIssued
	<class 'int'>
	Nulls: False
	Min: 1978
	Max: 2016
	Sum: 55363313
	Mean: 2009.0471749464746
	Median: 2012
	Standard Deviation: 8.073281486155203
	Unique values: 38
	5 most frequent values:
		2015:	3675
		2014:	3311
		2013:	2663
		2012:	2575
		2016:	2334
 16. IssuedInLast30Days
	<class 'bool'>
	Nulls: False
	Unique values: 2
	5 most frequent values:
		False:	27210
		True:	347
 17. IssuanceMethod
	<class 'str'>
	Nulls: False
	Values: Online, Permit Center
 18. StatusCurrent
	<class 'str'>
	Nulls: False
	Unique values: 11
	5 most frequent values:
		Final:	20105
		Active:	3265
		Expired:	2537
		VOID:	1370
		Withdrawn:	263
	Max length: 31
 19. ExpiresDate
	<class 'datetime.date'>
	Nulls: False
	Min: 1929-12-23
	Max: 2018-04-13
	Unique values: 5860
	5 most frequent values:
		2016-10-10:	138
		2007-08-29:	136
		2016-10-09:	128
		2016-09-24:	112
		2016-10-08:	81
 20. CompletedDate
	<class 'datetime.date'>
	Nulls: True
	Min: 1929-12-23
	Max: 2016-04-13
	Unique values: 4478
	5 most frequent values:
		1995-02-22:	66
		2012-08-24:	41
		2014-11-21:	35
		1991-02-11:	33
		1984-12-06:	32
 21. TotalExistingBldgSQFT
	<class 'int'>
	Nulls: True
	Min: 0
	Max: 448668
	Sum: 33144690
	Mean: 2111.933860073914
	Median: 1500.0
	Standard Deviation: 7295.411028316902
	Unique values: 3214
	5 most frequent values:
		0:	2085
		1600:	179
		400:	118
		1000:	101
		1200:	88
 22. RemodelRepairSQFT
	<class 'int'>
	Nulls: True
	Min: 0
	Max: 187000
	Sum: 1713302
	Mean: 910.3623804463336
	Median: 300.0
	Standard Deviation: 4438.117538707591
	Unique values: 250
	5 most frequent values:
		0:	725
		1000:	61
		400:	48
		500:	40
		300:	34
 23. TotalNewAddSQFT
	<class 'int'>
	Nulls: True
	Min: -496
	Max: 505600
	Sum: 10571738
	Mean: 797.3855785186303
	Median: 572.0
	Standard Deviation: 4445.398851213035
	Unique values: 1619
	5 most frequent values:
		0:	598
		500:	51
		540:	47
		180:	44
		420:	42
 24. TotalValuationRemodel
	<class 'str'>
	Nulls: True
	Unique values: 1002
	5 most frequent values:
		$0.00:	218
		$50000.00:	122
		$20000.00:	116
		$10000.00:	110
		$40000.00:	104
	Max length: 11
 25. TotalJobValuation
	<class 'str'>
	Nulls: True
	Unique values: 1456
	5 most frequent values:
		$0.00:	2049
		$500.00:	1083
		$5000.00:	938
		$44.00:	484
		$10000.00:	365
	Max length: 12
 26. NumberOfFloors
	<class 'int'>
	Nulls: True
	Min: 0
	Max: 23
	Sum: 29315
	Mean: 1.3179427235534775
	Median: 1
	Standard Deviation: 0.6738348223099231
	Unique values: 14
	5 most frequent values:
		1:	15348
		2:	6228
		3:	393
		0:	237
		4:	19
 27. HousingUnits
	<class 'int'>
	Nulls: True
	Min: 0
	Max: 224
	Sum: 30329
	Mean: 1.1967407173578504
	Median: 1
	Standard Deviation: 6.115324402642133
	Unique values: 29
	5 most frequent values:
		1:	22555
		0:	2157
		2:	478
		4:	28
		5:	22
 28. BuildingValuation
	<class 'str'>
	Nulls: True
	Values: $400000.00, $3000.00, $200.00, $10000.00
 29. BuildingValuationRemodel
	<class 'str'>
	Nulls: True
	Unique values: 786
	5 most frequent values:
		$0.00:	250
		$10000.00:	219
		$5000.00:	157
		$20000.00:	141
		$15000.00:	119
	Max length: 11
 30. ElectricalValuation
	<class 'str'>
	Nulls: True
	Values: $0.00, $65000.00
 31. ElectricalValuationRemodel
	<class 'str'>
	Nulls: True
	Unique values: 369
	5 most frequent values:
		$0.00:	986
		$5000.00:	743
		$2000.00:	489
		$10000.00:	445
		$1000.00:	404
	Max length: 10
 32. MechanicalValuation
	<class 'str'>
	Nulls: True
	Values: $0.00, $50000.00
 33. MechanicalValuationRemodel
	<class 'str'>
	Nulls: True
	Unique values: 359
	5 most frequent values:
		$0.00:	1579
		$5000.00:	599
		$10000.00:	365
		$1000.00:	334
		$2000.00:	313
	Max length: 10
 34. PlumbingValuation
	<class 'str'>
	Nulls: True
	Values: $0.00, $35000.00
 35. PlumbingValuationRemodel
	<class 'str'>
	Nulls: True
	Unique values: 362
	5 most frequent values:
		$0.00:	1273
		$5000.00:	630
		$10000.00:	458
		$2000.00:	390
		$3000.00:	334
	Max length: 10
 36. MedGasValuation
	<class 'NoneType'>
	Nulls: True
	Values: 
 37. MedGasValuationRemodel
	<class 'str'>
	Nulls: True
	Values: $0.00
 38. OriginalAddress1
	<class 'str'>
	Nulls: True
	Unique values: 13106
	5 most frequent values:
		1600 1/2 N LAMAR BLVD:	93
		1524 1/2 E ANDERSON LN WB:	63
		2500 E SH 71 SVRD EB:	62
		2674 1/2 N LAMAR BLVD:	41
		1201 S CONGRESS AVE:	37
	Max length: 40
 39. OriginalCity
	<class 'str'>
	Nulls: True
	Values: PFLUGERVILLE, LAKEWAY, ROUND ROCK, AUSTIN
 40. OriginalState
	<class 'str'>
	Nulls: True
	Values: TX
 41. OriginalZip
	<class 'int'>
	Nulls: True
	Min: 78610
	Max: 78759
	Sum: 2145455375
	Mean: 78726.52924555996
	Median: 78727.0
	Standard Deviation: 22.594068156704978
	Unique values: 47
	5 most frequent values:
		78704:	3794
		78703:	3508
		78702:	2573
		78757:	2235
		78731:	2131
 42. CouncilDistrict
	<class 'int'>
	Nulls: True
	Min: 1
	Max: 10
	Sum: 180812
	Mean: 6.701953371140517
	Median: 7
	Standard Deviation: 3.0710141933721227
	Unique values: 10
	5 most frequent values:
		9:	6116
		10:	5938
		7:	3652
		1:	2564
		3:	2520
 43. Jurisdiction
	<class 'str'>
	Nulls: True
	Values: AUSTIN LTD, PFLUGERVILLE FULL PURPOSE, AUSTIN FULL PURPOSE, AUSTIN 2 MILE ETJ, OTHER
 44. Link
	<class 'str'>
	Nulls: False
	Unique values: 27557
	Max length: 92
 45. ProjectID
	<class 'int'>
	Nulls: False
	Min: 500079
	Max: 11515912
	Sum: 241883346618
	Mean: 8777564.561381863
	Median: 10698614
	Standard Deviation: 4099905.24833367
	Unique values: 27557
 46. Latitude
	<class 'float'>
	Nulls: True
	Min: 30.1228513
	Max: 30.502516
	Sum: 824567.1776322392
	Mean: 30.294921655971752
	Median: 30.293640089999997
	Standard Deviation: 0.055818781297898634
	Unique values: 12766
	5 most frequent values:
		30.28117781:	93
		30.33251521:	63
		30.2125426:	62
		30.33942906:	58
		30.29274394:	41
 47. Longitude
	<class 'float'>
	Nulls: True
	Min: -97.93283281
	Max: -97.5868926
	Sum: -2660534.0220896956
	Mean: -97.7490639315782
	Median: -97.74837307
	Standard Deviation: 0.03871415068082917
	Unique values: 12761
	5 most frequent values:
		-97.75068768:	93
		-97.684873:	63
		-97.65899663:	62
		-97.71888445:	58
		-97.74718985:	41
 48. Location
	<class 'str'>
	Nulls: True
	Unique values: 12770
	5 most frequent values:
		(30.28117781, -97.75068768):	93
		(30.33251521, -97.684873):	63
		(30.2125426, -97.65899663):	62
		(30.33942906, -97.71888445):	58
		(30.29274394, -97.74718985):	41
	Max length: 27

Row count: 27557
