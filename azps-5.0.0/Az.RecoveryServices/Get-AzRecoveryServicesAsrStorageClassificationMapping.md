---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278488"
---
# <span data-ttu-id="e2a1b-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e2a1b-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="e2a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a1b-103">ASR depolama sınıflandırması eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="e2a1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2a1b-104">SYNTAX</span></span>

### <span data-ttu-id="e2a1b-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2a1b-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2a1b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e2a1b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2a1b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2a1b-107">DESCRIPTION</span></span>
<span data-ttu-id="e2a1b-108">**Get-Azrecoveryservicesasrstorageclassıficationmapping** cmdlet 'i, bir ASR depolama sınıflandırması eşlemesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="e2a1b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2a1b-109">EXAMPLES</span></span>

### <span data-ttu-id="e2a1b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2a1b-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="e2a1b-111">Belirtilen depolama sınıflandırmasına karşılık gelen tüm depolama sınıflandırması eşlemelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="e2a1b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2a1b-112">PARAMETERS</span></span>

### <span data-ttu-id="e2a1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a1b-113">-DefaultProfile</span></span>
<span data-ttu-id="e2a1b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e2a1b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2a1b-115">-Name</span></span>
<span data-ttu-id="e2a1b-116">Alınacak depolama sınıflandırması eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="e2a1b-117">-Storageclassıfın</span><span class="sxs-lookup"><span data-stu-id="e2a1b-117">-StorageClassification</span></span>
<span data-ttu-id="e2a1b-118">ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="e2a1b-119">Cmdlet, belirtilen depolama sınıflandırmasına karşılık gelen ASR depolama sınıflandırması eşlemelerini alır</span><span class="sxs-lookup"><span data-stu-id="e2a1b-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="e2a1b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a1b-120">CommonParameters</span></span>
<span data-ttu-id="e2a1b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a1b-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a1b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2a1b-123">INPUTS</span></span>

### <span data-ttu-id="e2a1b-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıfbakımı</span><span class="sxs-lookup"><span data-stu-id="e2a1b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="e2a1b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2a1b-125">OUTPUTS</span></span>

### <span data-ttu-id="e2a1b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="e2a1b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="e2a1b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2a1b-127">NOTES</span></span>

## <span data-ttu-id="e2a1b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2a1b-128">RELATED LINKS</span></span>

[<span data-ttu-id="e2a1b-129">New-Azrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="e2a1b-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="e2a1b-130">Remove-Azrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="e2a1b-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
