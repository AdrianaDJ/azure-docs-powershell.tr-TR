---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 2a857c538188c2b9ddf7516ccebda291f3161e1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593405"
---
# <span data-ttu-id="54c80-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="54c80-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="54c80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c80-102">SYNOPSIS</span></span>
<span data-ttu-id="54c80-103">Koruma kapsayıcısındaki korunabilir öğeleri edinin.</span><span class="sxs-lookup"><span data-stu-id="54c80-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54c80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54c80-104">SYNTAX</span></span>

### <span data-ttu-id="54c80-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54c80-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c80-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="54c80-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c80-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="54c80-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c80-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="54c80-108">DESCRIPTION</span></span>
<span data-ttu-id="54c80-109">**Get-AzureRmSiteRecoveryProtectableItem** cmdlet 'ı bir Azure Site Recovery Protection kapsayıcısındaki korunabilir öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="54c80-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="54c80-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54c80-110">EXAMPLES</span></span>

## <span data-ttu-id="54c80-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54c80-111">PARAMETERS</span></span>

### <span data-ttu-id="54c80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c80-112">-DefaultProfile</span></span>
<span data-ttu-id="54c80-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54c80-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54c80-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="54c80-114">-FriendlyName</span></span>
<span data-ttu-id="54c80-115">Azure Site Recovery korunabilir öğesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c80-115">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c80-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="54c80-116">-Name</span></span>
<span data-ttu-id="54c80-117">Azure Site Recovery korunabilir öğesi öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c80-117">Specifies the name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c80-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="54c80-118">-ProtectionContainer</span></span>
<span data-ttu-id="54c80-119">Azure Site Recovery koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c80-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54c80-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c80-120">CommonParameters</span></span>
<span data-ttu-id="54c80-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54c80-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c80-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c80-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c80-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54c80-123">INPUTS</span></span>

### <span data-ttu-id="54c80-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="54c80-124">ASRProtectionContainer</span></span>
<span data-ttu-id="54c80-125">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="54c80-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="54c80-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54c80-126">OUTPUTS</span></span>

### <span data-ttu-id="54c80-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. Asrkorunabilir \ 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="54c80-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54c80-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54c80-128">NOTES</span></span>

## <span data-ttu-id="54c80-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54c80-129">RELATED LINKS</span></span>

[<span data-ttu-id="54c80-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="54c80-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="54c80-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="54c80-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
