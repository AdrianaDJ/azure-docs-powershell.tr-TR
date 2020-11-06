---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 86d8cc4b48342b49e807635e6fb51c5f4028b172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588754"
---
# <span data-ttu-id="2af75-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2af75-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="2af75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2af75-102">SYNOPSIS</span></span>
<span data-ttu-id="2af75-103">Site kurtarmada bir depolama sınıflandırması eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2af75-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2af75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2af75-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2af75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2af75-105">DESCRIPTION</span></span>
<span data-ttu-id="2af75-106">**New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet 'ı Azure Site Recovery 'de bir depolama sınıflandırması eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2af75-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="2af75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2af75-107">EXAMPLES</span></span>

## <span data-ttu-id="2af75-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2af75-108">PARAMETERS</span></span>

### <span data-ttu-id="2af75-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af75-109">-DefaultProfile</span></span>
<span data-ttu-id="2af75-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2af75-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2af75-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="2af75-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af75-112">-Primarystorageclassıfbir</span><span class="sxs-lookup"><span data-stu-id="2af75-112">-PrimaryStorageClassification</span></span>
<span data-ttu-id="2af75-113">Birincil depolama sınıflandırması eşlemesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2af75-113">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2af75-114">-Recoverystorageclassıf'</span><span class="sxs-lookup"><span data-stu-id="2af75-114">-RecoveryStorageClassification</span></span>
<span data-ttu-id="2af75-115">Kurtarma depolama sınıflandırması eşlemesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2af75-115">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af75-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af75-116">CommonParameters</span></span>
<span data-ttu-id="2af75-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2af75-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af75-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2af75-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af75-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2af75-119">INPUTS</span></span>

### <span data-ttu-id="2af75-120">Asrstorageclassıfın</span><span class="sxs-lookup"><span data-stu-id="2af75-120">ASRStorageClassification</span></span>
<span data-ttu-id="2af75-121">' Primarystorageclassıfmak ' parametresi, ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="2af75-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="2af75-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2af75-122">OUTPUTS</span></span>

### <span data-ttu-id="2af75-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2af75-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2af75-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2af75-124">NOTES</span></span>

## <span data-ttu-id="2af75-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2af75-125">RELATED LINKS</span></span>

[<span data-ttu-id="2af75-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2af75-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="2af75-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2af75-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
