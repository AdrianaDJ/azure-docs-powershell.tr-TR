---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 869b22c881652680be31c541c6d70d95a45be43d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589075"
---
# <span data-ttu-id="c1c84-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c1c84-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="c1c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c84-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c84-103">Azure Site Recovery koruma kapsayıcısı eşleştirmelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c1c84-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1c84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1c84-104">SYNTAX</span></span>

### <span data-ttu-id="c1c84-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1c84-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1c84-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c1c84-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1c84-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1c84-107">DESCRIPTION</span></span>
<span data-ttu-id="c1c84-108">**Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet 'i, kasadaki ilke eşlemelerine yönelik koruma kapsayıcısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c1c84-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="c1c84-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1c84-109">EXAMPLES</span></span>

## <span data-ttu-id="c1c84-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1c84-110">PARAMETERS</span></span>

### <span data-ttu-id="c1c84-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1c84-111">-Name</span></span>
<span data-ttu-id="c1c84-112">Koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1c84-112">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="c1c84-113">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c1c84-113">-ProtectionContainer</span></span>
<span data-ttu-id="c1c84-114">Azure Site Recovery koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1c84-114">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="c1c84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c84-115">-DefaultProfile</span></span>
<span data-ttu-id="c1c84-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1c84-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1c84-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c84-117">CommonParameters</span></span>
<span data-ttu-id="c1c84-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1c84-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c84-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c84-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c84-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1c84-120">INPUTS</span></span>

### <span data-ttu-id="c1c84-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c1c84-121">ASRProtectionContainer</span></span>
<span data-ttu-id="c1c84-122">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c1c84-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="c1c84-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1c84-123">OUTPUTS</span></span>

### <span data-ttu-id="c1c84-124">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c1c84-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c1c84-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1c84-125">NOTES</span></span>

## <span data-ttu-id="c1c84-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1c84-126">RELATED LINKS</span></span>

[<span data-ttu-id="c1c84-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c1c84-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="c1c84-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c1c84-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
