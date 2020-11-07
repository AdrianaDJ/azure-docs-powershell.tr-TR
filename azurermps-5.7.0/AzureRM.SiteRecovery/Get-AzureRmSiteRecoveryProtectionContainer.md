---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: d5c2032828c5d34b94af8d448155c18b6d8b06c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763984"
---
# <span data-ttu-id="57af3-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="57af3-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="57af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57af3-102">SYNOPSIS</span></span>
<span data-ttu-id="57af3-103">Geçerli site kurtarma Kasası için koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="57af3-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57af3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57af3-104">SYNTAX</span></span>

### <span data-ttu-id="57af3-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57af3-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57af3-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="57af3-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57af3-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="57af3-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57af3-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="57af3-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57af3-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="57af3-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57af3-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="57af3-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57af3-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="57af3-111">DESCRIPTION</span></span>
<span data-ttu-id="57af3-112">**Get-AzureRmSiteRecoveryProtectionContainer** cmdlet 'ı geçerli Azure Site Recovery Kasası için koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="57af3-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="57af3-113">Koruma kapsayıcısı sanal makineler gibi korumalı nesneler için mantıksal bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="57af3-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="57af3-114">Koruma ilkeleri, korumalı öğeler için çoğaltma ayarlarını tanımlar ve bir koruma konteyneriyle ilişkilendirilebilir ve korumalı bir varlığa uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="57af3-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="57af3-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57af3-115">EXAMPLES</span></span>

## <span data-ttu-id="57af3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57af3-116">PARAMETERS</span></span>

### <span data-ttu-id="57af3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57af3-117">-DefaultProfile</span></span>
<span data-ttu-id="57af3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57af3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57af3-119">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="57af3-119">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57af3-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="57af3-120">-FriendlyName</span></span>
<span data-ttu-id="57af3-121">Koruma kapsayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57af3-121">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57af3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="57af3-122">-Name</span></span>
<span data-ttu-id="57af3-123">Koruma kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57af3-123">Specifies the name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57af3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57af3-124">CommonParameters</span></span>
<span data-ttu-id="57af3-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57af3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57af3-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57af3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57af3-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57af3-127">INPUTS</span></span>

### <span data-ttu-id="57af3-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="57af3-128">ASRFabric</span></span>
<span data-ttu-id="57af3-129">Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="57af3-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="57af3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57af3-130">OUTPUTS</span></span>

### <span data-ttu-id="57af3-131">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="57af3-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="57af3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57af3-132">NOTES</span></span>

## <span data-ttu-id="57af3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57af3-133">RELATED LINKS</span></span>

