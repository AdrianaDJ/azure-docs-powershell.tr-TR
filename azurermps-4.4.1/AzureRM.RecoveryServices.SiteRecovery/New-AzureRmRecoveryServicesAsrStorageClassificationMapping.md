---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 14cd1606bc4c8d1709b0ddd64e845a2e84b26df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589158"
---
# <span data-ttu-id="daa91-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="daa91-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="daa91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa91-102">SYNOPSIS</span></span>
<span data-ttu-id="daa91-103">Kurtarma Hizmetleri Kasası 'nda ASR depolama sınıflandırması eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="daa91-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daa91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="daa91-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa91-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="daa91-105">DESCRIPTION</span></span>
<span data-ttu-id="daa91-106">**Yeni-Azurermrecoveryservicesasrstorageclassıficationmapping** cmdlet 'ı, kurtarma hizmetleri kasasıyla eşleşen bir depolama sınıflandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="daa91-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="daa91-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="daa91-107">EXAMPLES</span></span>

### <span data-ttu-id="daa91-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="daa91-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="daa91-109">Belirtilen parametrelerle depolama sınıflandırması eşlemesi oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="daa91-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="daa91-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="daa91-110">PARAMETERS</span></span>

### <span data-ttu-id="daa91-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="daa91-111">-Name</span></span>
<span data-ttu-id="daa91-112">ASR depolama sınıflandırması eşlemesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="daa91-112">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa91-113">-Primarystorageclassıfbir</span><span class="sxs-lookup"><span data-stu-id="daa91-113">-PrimaryStorageClassification</span></span>
<span data-ttu-id="daa91-114">Eşleme için birincil ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="daa91-114">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="daa91-115">-Recoverystorageclassıf'</span><span class="sxs-lookup"><span data-stu-id="daa91-115">-RecoveryStorageClassification</span></span>
<span data-ttu-id="daa91-116">Eşleme için kurtarma ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="daa91-116">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="daa91-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="daa91-117">-Confirm</span></span>
<span data-ttu-id="daa91-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="daa91-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa91-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa91-119">-WhatIf</span></span>
<span data-ttu-id="daa91-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="daa91-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="daa91-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="daa91-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa91-122">CommonParameters</span></span>
<span data-ttu-id="daa91-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="daa91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa91-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa91-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa91-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="daa91-125">INPUTS</span></span>

### <span data-ttu-id="daa91-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıfbakımı</span><span class="sxs-lookup"><span data-stu-id="daa91-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="daa91-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="daa91-127">OUTPUTS</span></span>

### <span data-ttu-id="daa91-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="daa91-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="daa91-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="daa91-129">NOTES</span></span>

## <span data-ttu-id="daa91-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="daa91-130">RELATED LINKS</span></span>

[<span data-ttu-id="daa91-131">Get-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="daa91-131">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="daa91-132">Remove-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="daa91-132">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
