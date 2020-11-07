---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 8bea83b033ffb8a2e56ba6d28759e88280529a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763246"
---
# <span data-ttu-id="5eadd-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5eadd-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="5eadd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eadd-102">SYNOPSIS</span></span>
<span data-ttu-id="5eadd-103">Kurtarma Hizmetleri kasasındaki kullanılabilir (keşfedilen) ASR depolama sınıflandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="5eadd-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5eadd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5eadd-104">SYNTAX</span></span>

### <span data-ttu-id="5eadd-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5eadd-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eadd-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="5eadd-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eadd-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5eadd-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eadd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5eadd-108">DESCRIPTION</span></span>
<span data-ttu-id="5eadd-109">**Get-Azurermrecoveryservicesasrstorageclassıfist** cmdlet 'ı, kurtarma hizmetleri KASASıNDAKI bulunan ASR depolama sınıflandırmalarını ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5eadd-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="5eadd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5eadd-110">EXAMPLES</span></span>

### <span data-ttu-id="5eadd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5eadd-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="5eadd-112">Belirtilen ASR dokusunda belirtilen bulunan depolama sınıflandırmalarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="5eadd-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="5eadd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5eadd-113">PARAMETERS</span></span>

### <span data-ttu-id="5eadd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eadd-114">-DefaultProfile</span></span>
<span data-ttu-id="5eadd-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5eadd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="5eadd-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="5eadd-116">-Fabric</span></span>
<span data-ttu-id="5eadd-117">ASR Fabric nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5eadd-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="5eadd-118">Cmdlet, belirtilen ASR dokusunda belirtilen bulunan depolama sınıflandırmaları ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5eadd-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eadd-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5eadd-119">-FriendlyName</span></span>
<span data-ttu-id="5eadd-120">Alınacak depolama sınıflandırması nesnesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5eadd-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eadd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5eadd-121">-Name</span></span>
<span data-ttu-id="5eadd-122">Alınacak depolama sınıflandırması nesnesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5eadd-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="5eadd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eadd-123">CommonParameters</span></span>
<span data-ttu-id="5eadd-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5eadd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eadd-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eadd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eadd-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5eadd-126">INPUTS</span></span>

### <span data-ttu-id="5eadd-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5eadd-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5eadd-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5eadd-128">OUTPUTS</span></span>

### <span data-ttu-id="5eadd-129">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., Services. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5eadd-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5eadd-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5eadd-130">NOTES</span></span>

## <span data-ttu-id="5eadd-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5eadd-131">RELATED LINKS</span></span>
