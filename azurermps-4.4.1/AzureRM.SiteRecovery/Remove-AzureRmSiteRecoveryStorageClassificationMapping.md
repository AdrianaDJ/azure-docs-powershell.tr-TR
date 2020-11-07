---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 59ae0324a5e42e87192e655352fce074413907ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763315"
---
# <span data-ttu-id="6c831-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6c831-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="6c831-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c831-102">SYNOPSIS</span></span>
<span data-ttu-id="6c831-103">Bir depolama sınıflandırması eşlemesini site kurtarması 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6c831-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c831-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c831-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c831-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c831-105">DESCRIPTION</span></span>
<span data-ttu-id="6c831-106">**Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet 'ı Azure Site Recovery 'den bir depolama sınıflandırması eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6c831-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="6c831-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c831-107">EXAMPLES</span></span>

## <span data-ttu-id="6c831-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c831-108">PARAMETERS</span></span>

### <span data-ttu-id="6c831-109">-Storageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="6c831-109">-StorageClassificationMapping</span></span>
<span data-ttu-id="6c831-110">Bu cmdlet 'in kaldırıldığı bir depolama sınıflandırması eşlemesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c831-110">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c831-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c831-111">-DefaultProfile</span></span>
<span data-ttu-id="6c831-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c831-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c831-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c831-113">CommonParameters</span></span>
<span data-ttu-id="6c831-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c831-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c831-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c831-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c831-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c831-116">INPUTS</span></span>

### <span data-ttu-id="6c831-117">Asrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="6c831-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="6c831-118">' Storageclassıficationmapping ' parametresi ardışık düzenin ' Asrstorageclassıficationmapping ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6c831-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="6c831-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c831-119">OUTPUTS</span></span>

### <span data-ttu-id="6c831-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6c831-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6c831-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c831-121">NOTES</span></span>

## <span data-ttu-id="6c831-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c831-122">RELATED LINKS</span></span>

[<span data-ttu-id="6c831-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6c831-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="6c831-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6c831-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
