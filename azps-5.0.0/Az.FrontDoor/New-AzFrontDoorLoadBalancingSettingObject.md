---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277413"
---
# <span data-ttu-id="75f68-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="75f68-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="75f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f68-102">SYNOPSIS</span></span>
<span data-ttu-id="75f68-103">Ön kapı oluşturmak için PSLoadBalancingSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="75f68-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="75f68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75f68-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f68-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75f68-105">DESCRIPTION</span></span>
<span data-ttu-id="75f68-106">Ön kapı oluşturmak için PSLoadBalancingSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="75f68-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="75f68-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75f68-107">EXAMPLES</span></span>

### <span data-ttu-id="75f68-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="75f68-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="75f68-109">Ön kapı oluşturmak için PSLoadBalancingSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="75f68-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="75f68-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75f68-110">PARAMETERS</span></span>

### <span data-ttu-id="75f68-111">-Addilatencya</span><span class="sxs-lookup"><span data-stu-id="75f68-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="75f68-112">Sondada en düşük gecikme demetini olan sonbaharın mili saniye cinsinden ek gecikme süresi.</span><span class="sxs-lookup"><span data-stu-id="75f68-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="75f68-113">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="75f68-113">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f68-114">-DefaultProfile</span></span>
<span data-ttu-id="75f68-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75f68-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f68-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="75f68-116">-Name</span></span>
<span data-ttu-id="75f68-117">durum araştırma ayarı adı.</span><span class="sxs-lookup"><span data-stu-id="75f68-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f68-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="75f68-118">-SampleSize</span></span>
<span data-ttu-id="75f68-119">Yük Dengelemesi kararlarını göz önünde bulundurmanız gereken örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="75f68-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="75f68-120">Varsayılan değer 4 ' dir</span><span class="sxs-lookup"><span data-stu-id="75f68-120">Default value is 4</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f68-121">-Başarılı</span><span class="sxs-lookup"><span data-stu-id="75f68-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="75f68-122">Örnek dönem içindeki, varsayılan değeri 2 olan örnek sayısı</span><span class="sxs-lookup"><span data-stu-id="75f68-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f68-123">CommonParameters</span></span>
<span data-ttu-id="75f68-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75f68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f68-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="75f68-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f68-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75f68-126">INPUTS</span></span>

### <span data-ttu-id="75f68-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="75f68-127">None</span></span>

## <span data-ttu-id="75f68-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75f68-128">OUTPUTS</span></span>

### <span data-ttu-id="75f68-129">Microsoft. Azure. Commands. Frontkapısı. modeller. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="75f68-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="75f68-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75f68-130">NOTES</span></span>

## <span data-ttu-id="75f68-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75f68-131">RELATED LINKS</span></span>

<span data-ttu-id="75f68-132">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="75f68-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
