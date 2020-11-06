---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593039"
---
# <span data-ttu-id="ed35b-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ed35b-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ed35b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed35b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed35b-103">Belirtilen ASR depolama sınıflandırması eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="ed35b-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed35b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed35b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed35b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed35b-105">DESCRIPTION</span></span>
<span data-ttu-id="ed35b-106">**Remove-Azurermrecoveryservicesasrstorageclassıficationmapping** cmdlet 'ı belirtilen Azure Site Recovery depolama sınıflandırması eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="ed35b-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="ed35b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed35b-107">EXAMPLES</span></span>

### <span data-ttu-id="ed35b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed35b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="ed35b-109">Belirtilen depolama sınıflandırması eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed35b-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ed35b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed35b-110">PARAMETERS</span></span>

### <span data-ttu-id="ed35b-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed35b-111">-InputObject</span></span>
<span data-ttu-id="ed35b-112">Cmdlet 'e giriş nesnesi: ASR depolama sınıflandırması eşlemesine, ASR depolama sınıflandırması eşleme nesnesi silinecektir.</span><span class="sxs-lookup"><span data-stu-id="ed35b-112">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed35b-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed35b-113">-Confirm</span></span>
<span data-ttu-id="ed35b-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed35b-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed35b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed35b-115">-WhatIf</span></span>
<span data-ttu-id="ed35b-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed35b-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed35b-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed35b-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed35b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed35b-118">CommonParameters</span></span>
<span data-ttu-id="ed35b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed35b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed35b-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed35b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed35b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed35b-121">INPUTS</span></span>

### <span data-ttu-id="ed35b-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="ed35b-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="ed35b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed35b-123">OUTPUTS</span></span>

### <span data-ttu-id="ed35b-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed35b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed35b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed35b-125">NOTES</span></span>

## <span data-ttu-id="ed35b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed35b-126">RELATED LINKS</span></span>

[<span data-ttu-id="ed35b-127">Get-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="ed35b-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ed35b-128">New-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="ed35b-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
