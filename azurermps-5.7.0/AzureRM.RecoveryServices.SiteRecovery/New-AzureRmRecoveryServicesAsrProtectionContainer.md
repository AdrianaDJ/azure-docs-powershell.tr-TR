---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 73d57e6e73b0e7e84dd3fb8bfff04ac8705bd108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763562"
---
# <span data-ttu-id="68b0f-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="68b0f-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="68b0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="68b0f-103">Belirtilen yapıda bir Azure Site Recovery koruma kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68b0f-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68b0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68b0f-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68b0f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="68b0f-106">New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet 'i belirtilen Azure Site Recovery yapısı altında bir koruma kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68b0f-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="68b0f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="68b0f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="68b0f-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="68b0f-109">Belirtilen parametrelerle koruma kapsayıcısının oluşturulmasını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="68b0f-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="68b0f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68b0f-110">PARAMETERS</span></span>

### <span data-ttu-id="68b0f-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="68b0f-111">-Confirm</span></span>
<span data-ttu-id="68b0f-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68b0f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b0f-113">-DefaultProfile</span></span>
<span data-ttu-id="68b0f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68b0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b0f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68b0f-115">-InputObject</span></span>
<span data-ttu-id="68b0f-116">Belirtilen giriş nesnesinde (Azure Fabric) çoğaltma koruma kapsayıcısını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68b0f-116">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68b0f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="68b0f-117">-Name</span></span>
<span data-ttu-id="68b0f-118">Koruma kapsayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="68b0f-118">Name of the protection container.</span></span>

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

### <span data-ttu-id="68b0f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b0f-119">-WhatIf</span></span>
<span data-ttu-id="68b0f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68b0f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68b0f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68b0f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b0f-122">CommonParameters</span></span>
<span data-ttu-id="68b0f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68b0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b0f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b0f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68b0f-125">INPUTS</span></span>

### <span data-ttu-id="68b0f-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="68b0f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="68b0f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68b0f-127">OUTPUTS</span></span>

### <span data-ttu-id="68b0f-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="68b0f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68b0f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68b0f-129">NOTES</span></span>

## <span data-ttu-id="68b0f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68b0f-130">RELATED LINKS</span></span>
