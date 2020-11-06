---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: de13a33aeaf60dbd83fcacebb8380bee27c18c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588480"
---
# <span data-ttu-id="33919-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="33919-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="33919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33919-102">SYNOPSIS</span></span>
<span data-ttu-id="33919-103">Ön kapı oluşturmak için PSLoadBalancingSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="33919-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33919-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33919-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33919-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33919-105">DESCRIPTION</span></span>
<span data-ttu-id="33919-106">Ön kapı oluşturmak için PSLoadBalancingSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="33919-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="33919-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33919-107">EXAMPLES</span></span>

### <span data-ttu-id="33919-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="33919-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="33919-109">Ön kapı oluşturmak için PSLoadBalancingSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="33919-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="33919-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33919-110">PARAMETERS</span></span>

### <span data-ttu-id="33919-111">-Addilatencya</span><span class="sxs-lookup"><span data-stu-id="33919-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="33919-112">Sondada en düşük gecikme demetini olan sonbaharın mili saniye cinsinden ek gecikme süresi.</span><span class="sxs-lookup"><span data-stu-id="33919-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="33919-113">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="33919-113">Default value is 0</span></span>

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

### <span data-ttu-id="33919-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33919-114">-DefaultProfile</span></span>
<span data-ttu-id="33919-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33919-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33919-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="33919-116">-Name</span></span>
<span data-ttu-id="33919-117">durum araştırma ayarı adı.</span><span class="sxs-lookup"><span data-stu-id="33919-117">health probe setting name.</span></span>

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

### <span data-ttu-id="33919-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="33919-118">-SampleSize</span></span>
<span data-ttu-id="33919-119">Yük Dengelemesi kararlarını göz önünde bulundurmanız gereken örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="33919-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="33919-120">Varsayılan değer 4 ' dir</span><span class="sxs-lookup"><span data-stu-id="33919-120">Default value is 4</span></span>

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

### <span data-ttu-id="33919-121">-Başarılı</span><span class="sxs-lookup"><span data-stu-id="33919-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="33919-122">Örnek dönem içindeki, varsayılan değeri 2 olan örnek sayısı</span><span class="sxs-lookup"><span data-stu-id="33919-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="33919-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33919-123">CommonParameters</span></span>
<span data-ttu-id="33919-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33919-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33919-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33919-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33919-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33919-126">INPUTS</span></span>

### <span data-ttu-id="33919-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="33919-127">None</span></span>

## <span data-ttu-id="33919-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33919-128">OUTPUTS</span></span>

### <span data-ttu-id="33919-129">Microsoft. Azure. Commands. Frontkapısı. modeller. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="33919-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="33919-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33919-130">NOTES</span></span>

## <span data-ttu-id="33919-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33919-131">RELATED LINKS</span></span>

<span data-ttu-id="33919-132">[Yeni-Azurermfrontkapısı](./New-AzureRmFrontDoor.md) 
 [Set-Azurermfrontkapısı](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="33919-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
