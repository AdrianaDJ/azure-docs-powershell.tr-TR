---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277687"
---
# <span data-ttu-id="2e13b-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2e13b-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="2e13b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e13b-102">SYNOPSIS</span></span>
<span data-ttu-id="2e13b-103">Kurtarma Hizmetleri Kasası 'nda ASR depolama sınıflandırması eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e13b-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="2e13b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e13b-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e13b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e13b-105">DESCRIPTION</span></span>
<span data-ttu-id="2e13b-106">**Yeni-Azrecoveryservicesasrstorageclassıficationmapping** cmdlet 'ı, kurtarma hizmetleri kasası ile eşleşen bir depolama sınıflandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e13b-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="2e13b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e13b-107">EXAMPLES</span></span>

### <span data-ttu-id="2e13b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2e13b-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="2e13b-109">Belirtilen parametrelerle depolama sınıflandırması eşlemesi oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2e13b-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2e13b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e13b-110">PARAMETERS</span></span>

### <span data-ttu-id="2e13b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e13b-111">-DefaultProfile</span></span>
<span data-ttu-id="2e13b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e13b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e13b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e13b-113">-Name</span></span>
<span data-ttu-id="2e13b-114">ASR depolama sınıflandırması eşlemesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e13b-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="2e13b-115">-Primarystorageclassıfbir</span><span class="sxs-lookup"><span data-stu-id="2e13b-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="2e13b-116">Eşleme için birincil ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e13b-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="2e13b-117">-Recoverystorageclassıf'</span><span class="sxs-lookup"><span data-stu-id="2e13b-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="2e13b-118">Eşleme için kurtarma ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e13b-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="2e13b-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e13b-119">-Confirm</span></span>
<span data-ttu-id="2e13b-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e13b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e13b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e13b-121">-WhatIf</span></span>
<span data-ttu-id="2e13b-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e13b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e13b-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e13b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e13b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e13b-124">CommonParameters</span></span>
<span data-ttu-id="2e13b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e13b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e13b-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2e13b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e13b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e13b-127">INPUTS</span></span>

### <span data-ttu-id="2e13b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıfbakımı</span><span class="sxs-lookup"><span data-stu-id="2e13b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2e13b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e13b-129">OUTPUTS</span></span>

### <span data-ttu-id="2e13b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2e13b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2e13b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e13b-131">NOTES</span></span>

## <span data-ttu-id="2e13b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e13b-132">RELATED LINKS</span></span>

[<span data-ttu-id="2e13b-133">Get-Azrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="2e13b-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="2e13b-134">Remove-Azrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="2e13b-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
