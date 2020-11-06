---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: 2595d8feaa01c2f3ccd9f16ca193be195a8e303a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594169"
---
# <span data-ttu-id="af4b2-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="af4b2-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="af4b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af4b2-102">SYNOPSIS</span></span>
<span data-ttu-id="af4b2-103">Geçerli site kurtarma Kasası için koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="af4b2-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af4b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af4b2-104">SYNTAX</span></span>

### <span data-ttu-id="af4b2-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af4b2-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af4b2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="af4b2-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af4b2-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="af4b2-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af4b2-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="af4b2-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af4b2-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="af4b2-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af4b2-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="af4b2-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af4b2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="af4b2-111">DESCRIPTION</span></span>
<span data-ttu-id="af4b2-112">**Get-AzureRmSiteRecoveryProtectionContainer** cmdlet 'ı geçerli Azure Site Recovery Kasası için koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="af4b2-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="af4b2-113">Koruma kapsayıcısı sanal makineler gibi korumalı nesneler için mantıksal bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="af4b2-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="af4b2-114">Koruma ilkeleri, korumalı öğeler için çoğaltma ayarlarını tanımlar ve bir koruma konteyneriyle ilişkilendirilebilir ve korumalı bir varlığa uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="af4b2-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="af4b2-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af4b2-115">EXAMPLES</span></span>

## <span data-ttu-id="af4b2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af4b2-116">PARAMETERS</span></span>

### <span data-ttu-id="af4b2-117">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="af4b2-117">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af4b2-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="af4b2-118">-FriendlyName</span></span>
<span data-ttu-id="af4b2-119">Koruma kapsayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af4b2-119">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4b2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="af4b2-120">-Name</span></span>
<span data-ttu-id="af4b2-121">Koruma kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af4b2-121">Specifies the name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4b2-122">-DefaultProfile</span></span>
<span data-ttu-id="af4b2-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af4b2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af4b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4b2-124">CommonParameters</span></span>
<span data-ttu-id="af4b2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af4b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4b2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af4b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4b2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af4b2-127">INPUTS</span></span>

### <span data-ttu-id="af4b2-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="af4b2-128">ASRFabric</span></span>
<span data-ttu-id="af4b2-129">Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="af4b2-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="af4b2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af4b2-130">OUTPUTS</span></span>

### <span data-ttu-id="af4b2-131">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="af4b2-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="af4b2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af4b2-132">NOTES</span></span>

## <span data-ttu-id="af4b2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af4b2-133">RELATED LINKS</span></span>

