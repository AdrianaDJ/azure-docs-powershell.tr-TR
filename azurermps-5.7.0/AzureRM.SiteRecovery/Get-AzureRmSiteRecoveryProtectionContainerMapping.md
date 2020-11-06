---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 31887397c6b9b0a3a18a4af3cb4b4faca7c4a91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593403"
---
# <span data-ttu-id="d8a03-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d8a03-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="d8a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a03-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a03-103">Azure Site Recovery koruma kapsayıcısı eşleştirmelerini alır.</span><span class="sxs-lookup"><span data-stu-id="d8a03-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8a03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8a03-104">SYNTAX</span></span>

### <span data-ttu-id="d8a03-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8a03-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8a03-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d8a03-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8a03-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8a03-107">DESCRIPTION</span></span>
<span data-ttu-id="d8a03-108">**Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet 'i, kasadaki ilke eşlemelerine yönelik koruma kapsayıcısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d8a03-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="d8a03-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8a03-109">EXAMPLES</span></span>

## <span data-ttu-id="d8a03-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8a03-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a03-111">-DefaultProfile</span></span>
<span data-ttu-id="d8a03-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8a03-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8a03-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8a03-113">-Name</span></span>
<span data-ttu-id="d8a03-114">Koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a03-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="d8a03-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d8a03-115">-ProtectionContainer</span></span>
<span data-ttu-id="d8a03-116">Azure Site Recovery koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a03-116">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="d8a03-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a03-117">CommonParameters</span></span>
<span data-ttu-id="d8a03-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8a03-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a03-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a03-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a03-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8a03-120">INPUTS</span></span>

### <span data-ttu-id="d8a03-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d8a03-121">ASRProtectionContainer</span></span>
<span data-ttu-id="d8a03-122">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d8a03-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="d8a03-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8a03-123">OUTPUTS</span></span>

### <span data-ttu-id="d8a03-124">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d8a03-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d8a03-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8a03-125">NOTES</span></span>

## <span data-ttu-id="d8a03-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8a03-126">RELATED LINKS</span></span>

[<span data-ttu-id="d8a03-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d8a03-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="d8a03-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d8a03-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
