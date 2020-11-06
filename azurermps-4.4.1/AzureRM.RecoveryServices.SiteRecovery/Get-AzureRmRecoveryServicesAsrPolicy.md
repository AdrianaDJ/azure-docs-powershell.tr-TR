---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594597"
---
# <span data-ttu-id="0e97f-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0e97f-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="0e97f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e97f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e97f-103">ASR çoğaltma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="0e97f-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e97f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e97f-104">SYNTAX</span></span>

### <span data-ttu-id="0e97f-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0e97f-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="0e97f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0e97f-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="0e97f-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0e97f-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="0e97f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e97f-108">DESCRIPTION</span></span>
<span data-ttu-id="0e97f-109">**Get-AzureRmRecoveryServicesAsrPolicy** cmdlet 'i, yapılandırılmış Azure Site Recovery çoğaltma ilkelerinin listesini veya ad ile belirli bir çoğaltma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="0e97f-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="0e97f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e97f-110">EXAMPLES</span></span>

### <span data-ttu-id="0e97f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0e97f-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="0e97f-112">Belirtilen ad ile çoğaltma ilkesini retruns.</span><span class="sxs-lookup"><span data-stu-id="0e97f-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="0e97f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e97f-113">PARAMETERS</span></span>

### <span data-ttu-id="0e97f-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0e97f-114">-FriendlyName</span></span>
<span data-ttu-id="0e97f-115">ASR çoğaltma ilkesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e97f-115">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="0e97f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e97f-116">-Name</span></span>
<span data-ttu-id="0e97f-117">ASR çoğaltma ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e97f-117">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="0e97f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e97f-118">CommonParameters</span></span>
<span data-ttu-id="0e97f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e97f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e97f-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e97f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e97f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e97f-121">INPUTS</span></span>

### <span data-ttu-id="0e97f-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0e97f-122">None</span></span>

## <span data-ttu-id="0e97f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e97f-123">OUTPUTS</span></span>

### <span data-ttu-id="0e97f-124">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., 4.0.0.0 covery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version =, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0e97f-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0e97f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e97f-125">NOTES</span></span>

## <span data-ttu-id="0e97f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e97f-126">RELATED LINKS</span></span>

[<span data-ttu-id="0e97f-127">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0e97f-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="0e97f-128">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0e97f-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
