---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763659"
---
# <span data-ttu-id="f4c50-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f4c50-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f4c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4c50-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c50-103">ASR depolama sınıflandırması eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f4c50-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4c50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4c50-104">SYNTAX</span></span>

### <span data-ttu-id="f4c50-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4c50-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="f4c50-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f4c50-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="f4c50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4c50-107">DESCRIPTION</span></span>
<span data-ttu-id="f4c50-108">**Get-Azurermrecoveryservicesasrstorageclassıficationmapping** cmdlet 'i, bir ASR depolama sınıflandırması eşlemesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f4c50-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="f4c50-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4c50-109">EXAMPLES</span></span>

### <span data-ttu-id="f4c50-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4c50-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="f4c50-111">Belirtilen depolama sınıflandırmasına karşılık gelen tüm depolama sınıflandırması eşlemelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="f4c50-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="f4c50-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4c50-112">PARAMETERS</span></span>

### <span data-ttu-id="f4c50-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4c50-113">-Name</span></span>
<span data-ttu-id="f4c50-114">Alınacak depolama sınıflandırması eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4c50-114">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c50-115">-Storageclassıfın</span><span class="sxs-lookup"><span data-stu-id="f4c50-115">-StorageClassification</span></span>
<span data-ttu-id="f4c50-116">ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4c50-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="f4c50-117">Cmdlet, belirtilen depolama sınıflandırmasına karşılık gelen ASR depolama sınıflandırması eşlemelerini alır</span><span class="sxs-lookup"><span data-stu-id="f4c50-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="f4c50-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c50-118">CommonParameters</span></span>
<span data-ttu-id="f4c50-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4c50-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c50-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4c50-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c50-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4c50-121">INPUTS</span></span>

### <span data-ttu-id="f4c50-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f4c50-122">None</span></span>

## <span data-ttu-id="f4c50-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4c50-123">OUTPUTS</span></span>

### <span data-ttu-id="f4c50-124">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıficationmapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f4c50-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f4c50-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4c50-125">NOTES</span></span>

## <span data-ttu-id="f4c50-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4c50-126">RELATED LINKS</span></span>

[<span data-ttu-id="f4c50-127">New-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="f4c50-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f4c50-128">Remove-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="f4c50-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
