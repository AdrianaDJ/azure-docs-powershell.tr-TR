---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: fecc6f1911a82b20d3f96643ceed83486727f29f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276565"
---
# <span data-ttu-id="6c854-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6c854-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="6c854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c854-102">SYNOPSIS</span></span>
<span data-ttu-id="6c854-103">Belirtilen yapıda bir Azure Site Recovery koruma kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c854-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="6c854-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c854-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c854-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c854-105">DESCRIPTION</span></span>
<span data-ttu-id="6c854-106">New-AzRecoveryServicesAsrProtectionContainer cmdlet 'i belirtilen Azure Site Recovery yapısı altında bir koruma kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c854-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="6c854-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c854-107">EXAMPLES</span></span>

### <span data-ttu-id="6c854-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6c854-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="6c854-109">Belirtilen parametrelerle koruma kapsayıcısının oluşturulmasını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6c854-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6c854-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c854-110">PARAMETERS</span></span>

### <span data-ttu-id="6c854-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c854-111">-DefaultProfile</span></span>
<span data-ttu-id="6c854-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c854-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c854-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c854-113">-InputObject</span></span>
<span data-ttu-id="6c854-114">Belirtilen giriş nesnesinde (Azure Fabric) çoğaltma koruma kapsayıcısını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c854-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c854-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c854-115">-Name</span></span>
<span data-ttu-id="6c854-116">Koruma kapsayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="6c854-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="6c854-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c854-117">-Confirm</span></span>
<span data-ttu-id="6c854-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c854-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c854-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c854-119">-WhatIf</span></span>
<span data-ttu-id="6c854-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c854-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c854-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c854-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c854-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c854-122">CommonParameters</span></span>
<span data-ttu-id="6c854-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c854-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c854-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6c854-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c854-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c854-125">INPUTS</span></span>

### <span data-ttu-id="6c854-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6c854-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6c854-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c854-127">OUTPUTS</span></span>

### <span data-ttu-id="6c854-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6c854-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6c854-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c854-129">NOTES</span></span>

## <span data-ttu-id="6c854-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c854-130">RELATED LINKS</span></span>
