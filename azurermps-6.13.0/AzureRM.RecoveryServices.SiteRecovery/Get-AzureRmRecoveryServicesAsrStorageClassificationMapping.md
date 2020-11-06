---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: ec5ba90fd0c3dbdbf96ddf2370948de090306611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593928"
---
# <span data-ttu-id="0c9a4-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0c9a4-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="0c9a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9a4-103">ASR depolama sınıflandırması eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c9a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c9a4-104">SYNTAX</span></span>

### <span data-ttu-id="0c9a4-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c9a4-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c9a4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0c9a4-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c9a4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c9a4-107">DESCRIPTION</span></span>
<span data-ttu-id="0c9a4-108">**Get-Azurermrecoveryservicesasrstorageclassıficationmapping** cmdlet 'i, bir ASR depolama sınıflandırması eşlemesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="0c9a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c9a4-109">EXAMPLES</span></span>

### <span data-ttu-id="0c9a4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c9a4-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="0c9a4-111">Belirtilen depolama sınıflandırmasına karşılık gelen tüm depolama sınıflandırması eşlemelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="0c9a4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c9a4-112">PARAMETERS</span></span>

### <span data-ttu-id="0c9a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9a4-113">-DefaultProfile</span></span>
<span data-ttu-id="0c9a4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0c9a4-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c9a4-115">-Name</span></span>
<span data-ttu-id="0c9a4-116">Alınacak depolama sınıflandırması eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="0c9a4-117">-Storageclassıfın</span><span class="sxs-lookup"><span data-stu-id="0c9a4-117">-StorageClassification</span></span>
<span data-ttu-id="0c9a4-118">ASR depolama sınıflandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="0c9a4-119">Cmdlet, belirtilen depolama sınıflandırmasına karşılık gelen ASR depolama sınıflandırması eşlemelerini alır</span><span class="sxs-lookup"><span data-stu-id="0c9a4-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="0c9a4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9a4-120">CommonParameters</span></span>
<span data-ttu-id="0c9a4-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9a4-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c9a4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9a4-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c9a4-123">INPUTS</span></span>

### <span data-ttu-id="0c9a4-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0c9a4-124">None</span></span>

## <span data-ttu-id="0c9a4-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c9a4-125">OUTPUTS</span></span>

### <span data-ttu-id="0c9a4-126">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıficationmapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0c9a4-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0c9a4-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c9a4-127">NOTES</span></span>

## <span data-ttu-id="0c9a4-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c9a4-128">RELATED LINKS</span></span>

[<span data-ttu-id="0c9a4-129">New-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="0c9a4-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="0c9a4-130">Remove-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="0c9a4-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
