---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 152bd9cce3622f0ef0f04049b96791dc08627308
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759663"
---
# <span data-ttu-id="d7330-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d7330-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="d7330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7330-102">SYNOPSIS</span></span>
<span data-ttu-id="d7330-103">Kurtarma Hizmetleri Kasası 'nda ASR depolama sınıflandırması eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7330-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="d7330-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7330-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7330-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7330-105">DESCRIPTION</span></span>
<span data-ttu-id="d7330-106">**Yeni-Azrecoveryservicesasrstorageclassıficationmapping** cmdlet 'ı, kurtarma hizmetleri kasası ile eşleşen bir depolama sınıflandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7330-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="d7330-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7330-107">EXAMPLES</span></span>

### <span data-ttu-id="d7330-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d7330-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="d7330-109">Belirtilen parametrelerle depolama sınıflandırması eşlemesi oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d7330-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d7330-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7330-110">PARAMETERS</span></span>

### <span data-ttu-id="d7330-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7330-111">-DefaultProfile</span></span>
<span data-ttu-id="d7330-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7330-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d7330-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7330-113">-Name</span></span>
<span data-ttu-id="d7330-114">ASR depolama sınıflandırması eşlemesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7330-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="d7330-115">-Primarystorageclassıfbir</span><span class="sxs-lookup"><span data-stu-id="d7330-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="d7330-116">Eşleme için birincil ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7330-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="d7330-117">-Recoverystorageclassıf'</span><span class="sxs-lookup"><span data-stu-id="d7330-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="d7330-118">Eşleme için kurtarma ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7330-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="d7330-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7330-119">-Confirm</span></span>
<span data-ttu-id="d7330-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7330-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7330-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7330-121">-WhatIf</span></span>
<span data-ttu-id="d7330-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7330-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7330-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7330-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7330-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7330-124">CommonParameters</span></span>
<span data-ttu-id="d7330-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7330-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7330-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7330-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7330-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7330-127">INPUTS</span></span>

### <span data-ttu-id="d7330-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıfbakımı</span><span class="sxs-lookup"><span data-stu-id="d7330-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="d7330-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7330-129">OUTPUTS</span></span>

### <span data-ttu-id="d7330-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d7330-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d7330-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7330-131">NOTES</span></span>

## <span data-ttu-id="d7330-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7330-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7330-133">Get-Azrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="d7330-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="d7330-134">Remove-Azrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="d7330-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
