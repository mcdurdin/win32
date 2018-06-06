---
Description: The GetRate method retrieves the playback rate. This method implements the IMediaSeeking::GetRate method.
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: CPosPassThru.GetRate method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# CPosPassThru.GetRate method

The `GetRate` method retrieves the playback rate. This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.

## Syntax


```C++
HRESULT GetRate(
   double *pdRate
);
```



## Parameters

<dl> <dt>

*pdRate* 
</dt> <dd>

Pointer to a variable that receives the playback rate.

</dd> </dl>

## Return value

Returns the **HRESULT** value from the connected pin.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CPosPassThru Class**](cpospassthru.md)
</dt> </dl>

 

 



