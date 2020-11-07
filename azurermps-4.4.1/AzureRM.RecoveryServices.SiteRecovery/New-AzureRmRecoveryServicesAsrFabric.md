---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764526"
---
# <span data-ttu-id="51bef-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="51bef-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="51bef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51bef-102">SYNOPSIS</span></span>
<span data-ttu-id="51bef-103">Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51bef-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51bef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51bef-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51bef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51bef-105">DESCRIPTION</span></span>
<span data-ttu-id="51bef-106">**New-AzureRmRecoveryServicesAsrFabric** cmdlet 'i belirtilen türde bir Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51bef-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="51bef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51bef-107">EXAMPLES</span></span>

### <span data-ttu-id="51bef-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="51bef-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="51bef-109">Geçirilen adla yapı oluşturmayı başlatır ve doku oluşturma işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="51bef-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="51bef-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51bef-110">PARAMETERS</span></span>

### <span data-ttu-id="51bef-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="51bef-111">-Name</span></span>
<span data-ttu-id="51bef-112">Azure Site Recovery yapısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51bef-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bef-113">-Tür</span><span class="sxs-lookup"><span data-stu-id="51bef-113">-Type</span></span>
<span data-ttu-id="51bef-114">Azure Site Recovery Fabric türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="51bef-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bef-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="51bef-115">-Confirm</span></span>
<span data-ttu-id="51bef-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51bef-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bef-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51bef-117">-WhatIf</span></span>
<span data-ttu-id="51bef-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51bef-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51bef-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51bef-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bef-120">CommonParameters</span></span>
<span data-ttu-id="51bef-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51bef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bef-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51bef-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bef-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51bef-123">INPUTS</span></span>

### <span data-ttu-id="51bef-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="51bef-124">None</span></span>

## <span data-ttu-id="51bef-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51bef-125">OUTPUTS</span></span>

### <span data-ttu-id="51bef-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="51bef-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="51bef-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51bef-127">NOTES</span></span>

## <span data-ttu-id="51bef-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51bef-128">RELATED LINKS</span></span>

[<span data-ttu-id="51bef-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="51bef-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="51bef-130">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="51bef-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
