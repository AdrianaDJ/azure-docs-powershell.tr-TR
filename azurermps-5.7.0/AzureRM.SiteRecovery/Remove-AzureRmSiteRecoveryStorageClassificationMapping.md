---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2d215afda7c2c26aa178421fb52ddaff8c6ac831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591589"
---
# <span data-ttu-id="6226a-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6226a-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="6226a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6226a-102">SYNOPSIS</span></span>
<span data-ttu-id="6226a-103">Bir depolama sınıflandırması eşlemesini site kurtarması 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6226a-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6226a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6226a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6226a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6226a-105">DESCRIPTION</span></span>
<span data-ttu-id="6226a-106">**Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet 'ı Azure Site Recovery 'den bir depolama sınıflandırması eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6226a-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="6226a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6226a-107">EXAMPLES</span></span>

## <span data-ttu-id="6226a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6226a-108">PARAMETERS</span></span>

### <span data-ttu-id="6226a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6226a-109">-DefaultProfile</span></span>
<span data-ttu-id="6226a-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6226a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6226a-111">-Storageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="6226a-111">-StorageClassificationMapping</span></span>
<span data-ttu-id="6226a-112">Bu cmdlet 'in kaldırıldığı bir depolama sınıflandırması eşlemesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6226a-112">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6226a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6226a-113">CommonParameters</span></span>
<span data-ttu-id="6226a-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6226a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6226a-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6226a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6226a-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6226a-116">INPUTS</span></span>

### <span data-ttu-id="6226a-117">Asrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="6226a-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="6226a-118">' Storageclassıficationmapping ' parametresi ardışık düzenin ' Asrstorageclassıficationmapping ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6226a-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="6226a-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6226a-119">OUTPUTS</span></span>

### <span data-ttu-id="6226a-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6226a-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6226a-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6226a-121">NOTES</span></span>

## <span data-ttu-id="6226a-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6226a-122">RELATED LINKS</span></span>

[<span data-ttu-id="6226a-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6226a-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="6226a-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6226a-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
