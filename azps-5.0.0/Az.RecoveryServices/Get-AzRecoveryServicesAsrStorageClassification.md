---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325537"
---
# <span data-ttu-id="2f474-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f474-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="2f474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f474-102">SYNOPSIS</span></span>
<span data-ttu-id="2f474-103">Kurtarma Hizmetleri kasasındaki kullanılabilir (keşfedilen) ASR depolama sınıflandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="2f474-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2f474-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f474-104">SYNTAX</span></span>

### <span data-ttu-id="2f474-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f474-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f474-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2f474-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f474-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2f474-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f474-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f474-108">DESCRIPTION</span></span>
<span data-ttu-id="2f474-109">**Get-Azrecoveryservicesasrstorageclassıfınıal** cmdlet 'ı, kurtarma hizmetleri KASASıNDAKI bulunan ASR depolama sınıflandırmalarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="2f474-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2f474-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f474-110">EXAMPLES</span></span>

### <span data-ttu-id="2f474-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f474-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="2f474-112">Belirtilen ASR dokusunda belirtilen bulunan depolama sınıflandırmalarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="2f474-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="2f474-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f474-113">PARAMETERS</span></span>

### <span data-ttu-id="2f474-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f474-114">-DefaultProfile</span></span>
<span data-ttu-id="2f474-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f474-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2f474-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="2f474-116">-Fabric</span></span>
<span data-ttu-id="2f474-117">ASR Fabric nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f474-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="2f474-118">Cmdlet, belirtilen ASR dokusunda belirtilen bulunan depolama sınıflandırmaları ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="2f474-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f474-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2f474-119">-FriendlyName</span></span>
<span data-ttu-id="2f474-120">Alınacak depolama sınıflandırması nesnesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f474-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f474-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f474-121">-Name</span></span>
<span data-ttu-id="2f474-122">Alınacak depolama sınıflandırması nesnesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f474-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2f474-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f474-123">CommonParameters</span></span>
<span data-ttu-id="2f474-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f474-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f474-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2f474-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f474-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f474-126">INPUTS</span></span>

### <span data-ttu-id="2f474-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2f474-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2f474-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f474-128">OUTPUTS</span></span>

### <span data-ttu-id="2f474-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıfbakımı</span><span class="sxs-lookup"><span data-stu-id="2f474-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2f474-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f474-130">NOTES</span></span>

## <span data-ttu-id="2f474-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f474-131">RELATED LINKS</span></span>
