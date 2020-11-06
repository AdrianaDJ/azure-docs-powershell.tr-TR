---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594562"
---
# <span data-ttu-id="e37cc-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e37cc-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="e37cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e37cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e37cc-103">Geçerli site kurtarma kasasındaki korunabilir veya korunan varlıkların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e37cc-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e37cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e37cc-104">SYNTAX</span></span>

### <span data-ttu-id="e37cc-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e37cc-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e37cc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e37cc-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e37cc-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e37cc-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e37cc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e37cc-108">DESCRIPTION</span></span>
<span data-ttu-id="e37cc-109">**Get-AzureRmSiteRecoveryProtectionEntity** cmdlet 'ı geçerli Azure Site Recovery kasasındaki sanal makineler gibi korunabilir veya korumalı varlıkların bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e37cc-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e37cc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e37cc-110">EXAMPLES</span></span>

## <span data-ttu-id="e37cc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e37cc-111">PARAMETERS</span></span>

### <span data-ttu-id="e37cc-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e37cc-112">-FriendlyName</span></span>
<span data-ttu-id="e37cc-113">Koruma varlığının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e37cc-113">Specifies the friendly name of the protection entity.</span></span>

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

### <span data-ttu-id="e37cc-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="e37cc-114">-Name</span></span>
<span data-ttu-id="e37cc-115">Koruma varlığının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e37cc-115">Specifies the name of the protection entity.</span></span>

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

### <span data-ttu-id="e37cc-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e37cc-116">-ProtectionContainer</span></span>
<span data-ttu-id="e37cc-117">Koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e37cc-117">Specifies the protection container object.</span></span>

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

### <span data-ttu-id="e37cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e37cc-118">-DefaultProfile</span></span>
<span data-ttu-id="e37cc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e37cc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e37cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e37cc-120">CommonParameters</span></span>
<span data-ttu-id="e37cc-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e37cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e37cc-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e37cc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e37cc-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e37cc-123">INPUTS</span></span>

### <span data-ttu-id="e37cc-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e37cc-124">ASRProtectionContainer</span></span>
<span data-ttu-id="e37cc-125">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e37cc-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="e37cc-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e37cc-126">OUTPUTS</span></span>

### <span data-ttu-id="e37cc-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="e37cc-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="e37cc-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e37cc-128">NOTES</span></span>

## <span data-ttu-id="e37cc-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e37cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="e37cc-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e37cc-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
