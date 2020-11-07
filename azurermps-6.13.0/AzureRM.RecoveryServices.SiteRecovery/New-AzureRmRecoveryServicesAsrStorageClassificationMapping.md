---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 6ab8102de0deb27c18c6e50f8d78db2f23a5155a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762459"
---
# <span data-ttu-id="c3b66-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c3b66-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="c3b66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b66-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b66-103">Kurtarma Hizmetleri Kasası 'nda ASR depolama sınıflandırması eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3b66-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3b66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3b66-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3b66-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3b66-105">DESCRIPTION</span></span>
<span data-ttu-id="c3b66-106">**Yeni-Azurermrecoveryservicesasrstorageclassıficationmapping** cmdlet 'ı, kurtarma hizmetleri kasasıyla eşleşen bir depolama sınıflandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3b66-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="c3b66-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3b66-107">EXAMPLES</span></span>

### <span data-ttu-id="c3b66-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c3b66-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="c3b66-109">Belirtilen parametrelerle depolama sınıflandırması eşlemesi oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c3b66-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c3b66-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3b66-110">PARAMETERS</span></span>

### <span data-ttu-id="c3b66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b66-111">-DefaultProfile</span></span>
<span data-ttu-id="c3b66-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3b66-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c3b66-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3b66-113">-Name</span></span>
<span data-ttu-id="c3b66-114">ASR depolama sınıflandırması eşlemesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3b66-114">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b66-115">-Primarystorageclassıfbir</span><span class="sxs-lookup"><span data-stu-id="c3b66-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="c3b66-116">Eşleme için birincil ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3b66-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b66-117">-Recoverystorageclassıf'</span><span class="sxs-lookup"><span data-stu-id="c3b66-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="c3b66-118">Eşleme için kurtarma ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3b66-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b66-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3b66-119">-Confirm</span></span>
<span data-ttu-id="c3b66-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3b66-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b66-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b66-121">-WhatIf</span></span>
<span data-ttu-id="c3b66-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3b66-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3b66-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c3b66-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b66-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b66-124">CommonParameters</span></span>
<span data-ttu-id="c3b66-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3b66-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b66-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3b66-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b66-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3b66-127">INPUTS</span></span>

### <span data-ttu-id="c3b66-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıfbakımı</span><span class="sxs-lookup"><span data-stu-id="c3b66-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="c3b66-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3b66-129">OUTPUTS</span></span>

### <span data-ttu-id="c3b66-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c3b66-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c3b66-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3b66-131">NOTES</span></span>

## <span data-ttu-id="c3b66-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3b66-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3b66-133">Get-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="c3b66-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="c3b66-134">Remove-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="c3b66-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
