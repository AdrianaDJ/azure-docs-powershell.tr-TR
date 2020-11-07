---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 0b2fe8f500e17bc21407870a712ad4b9f00fd544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762400"
---
# <span data-ttu-id="3db85-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3db85-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="3db85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3db85-102">SYNOPSIS</span></span>
<span data-ttu-id="3db85-103">Koruma kapsayıcısındaki korunabilir öğeleri edinin.</span><span class="sxs-lookup"><span data-stu-id="3db85-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3db85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3db85-104">SYNTAX</span></span>

### <span data-ttu-id="3db85-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3db85-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3db85-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3db85-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3db85-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3db85-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3db85-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3db85-108">DESCRIPTION</span></span>
<span data-ttu-id="3db85-109">**Get-AzureRmSiteRecoveryProtectableItem** cmdlet 'ı bir Azure Site Recovery Protection kapsayıcısındaki korunabilir öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="3db85-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="3db85-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3db85-110">EXAMPLES</span></span>

## <span data-ttu-id="3db85-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3db85-111">PARAMETERS</span></span>

### <span data-ttu-id="3db85-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3db85-112">-FriendlyName</span></span>
<span data-ttu-id="3db85-113">Azure Site Recovery korunabilir öğesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db85-113">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db85-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="3db85-114">-Name</span></span>
<span data-ttu-id="3db85-115">Azure Site Recovery korunabilir öğesi öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db85-115">Specifies the name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db85-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3db85-116">-ProtectionContainer</span></span>
<span data-ttu-id="3db85-117">Azure Site Recovery koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db85-117">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3db85-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db85-118">-DefaultProfile</span></span>
<span data-ttu-id="3db85-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3db85-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3db85-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db85-120">CommonParameters</span></span>
<span data-ttu-id="3db85-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3db85-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db85-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db85-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db85-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3db85-123">INPUTS</span></span>

### <span data-ttu-id="3db85-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3db85-124">ASRProtectionContainer</span></span>
<span data-ttu-id="3db85-125">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3db85-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="3db85-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3db85-126">OUTPUTS</span></span>

### <span data-ttu-id="3db85-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. Asrkorunabilir \ 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3db85-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3db85-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3db85-128">NOTES</span></span>

## <span data-ttu-id="3db85-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3db85-129">RELATED LINKS</span></span>

[<span data-ttu-id="3db85-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3db85-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="3db85-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3db85-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
