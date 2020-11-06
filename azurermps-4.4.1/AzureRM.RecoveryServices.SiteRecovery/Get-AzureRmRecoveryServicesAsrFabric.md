---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587815"
---
# <span data-ttu-id="073f1-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="073f1-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="073f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="073f1-102">SYNOPSIS</span></span>
<span data-ttu-id="073f1-103">Azure Site kurtarma yapısı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="073f1-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="073f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="073f1-104">SYNTAX</span></span>

### <span data-ttu-id="073f1-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="073f1-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="073f1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="073f1-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="073f1-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="073f1-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="073f1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="073f1-108">DESCRIPTION</span></span>
<span data-ttu-id="073f1-109">**Get-AzureRmRecoveryServicesAsrFabric** cmdlet 'i, belirli bir Azure Site Recovery yapısı veya kurtarma hizmeti kasasındaki tüm Azure Site kurtarma yapılarını alır.</span><span class="sxs-lookup"><span data-stu-id="073f1-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="073f1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="073f1-110">EXAMPLES</span></span>

### <span data-ttu-id="073f1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="073f1-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="073f1-112">Kasadaki tüm Azure Site kurtarma yapılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="073f1-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="073f1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="073f1-113">PARAMETERS</span></span>

### <span data-ttu-id="073f1-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="073f1-114">-FriendlyName</span></span>
<span data-ttu-id="073f1-115">, Dokunun kolay adıyla ASR dokusunda arama yapın.</span><span class="sxs-lookup"><span data-stu-id="073f1-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073f1-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="073f1-116">-Name</span></span>
<span data-ttu-id="073f1-117">, Dokunun adına göre ASR yapınızı arayın.</span><span class="sxs-lookup"><span data-stu-id="073f1-117">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073f1-118">CommonParameters</span></span>
<span data-ttu-id="073f1-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="073f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073f1-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="073f1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073f1-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="073f1-121">INPUTS</span></span>

### <span data-ttu-id="073f1-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="073f1-122">None</span></span>

## <span data-ttu-id="073f1-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="073f1-123">OUTPUTS</span></span>

### <span data-ttu-id="073f1-124">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="073f1-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="073f1-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="073f1-125">NOTES</span></span>

## <span data-ttu-id="073f1-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="073f1-126">RELATED LINKS</span></span>

[<span data-ttu-id="073f1-127">Yeni-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="073f1-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="073f1-128">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="073f1-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
