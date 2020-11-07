---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 12c5132037e451681434620b65afd6e93235d65b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759660"
---
# <span data-ttu-id="106b3-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="106b3-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="106b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="106b3-102">SYNOPSIS</span></span>
<span data-ttu-id="106b3-103">Belirtilen yapıda bir Azure Site Recovery koruma kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="106b3-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="106b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="106b3-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="106b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="106b3-105">DESCRIPTION</span></span>
<span data-ttu-id="106b3-106">New-AzRecoveryServicesAsrProtectionContainer cmdlet 'i belirtilen Azure Site Recovery yapısı altında bir koruma kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="106b3-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="106b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="106b3-107">EXAMPLES</span></span>

### <span data-ttu-id="106b3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="106b3-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="106b3-109">Belirtilen parametrelerle koruma kapsayıcısının oluşturulmasını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="106b3-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="106b3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="106b3-110">PARAMETERS</span></span>

### <span data-ttu-id="106b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106b3-111">-DefaultProfile</span></span>
<span data-ttu-id="106b3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="106b3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="106b3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="106b3-113">-InputObject</span></span>
<span data-ttu-id="106b3-114">Belirtilen giriş nesnesinde (Azure Fabric) çoğaltma koruma kapsayıcısını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="106b3-114">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="106b3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="106b3-115">-Name</span></span>
<span data-ttu-id="106b3-116">Koruma kapsayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="106b3-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="106b3-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="106b3-117">-Confirm</span></span>
<span data-ttu-id="106b3-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="106b3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="106b3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="106b3-119">-WhatIf</span></span>
<span data-ttu-id="106b3-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="106b3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="106b3-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="106b3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="106b3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106b3-122">CommonParameters</span></span>
<span data-ttu-id="106b3-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="106b3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106b3-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="106b3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106b3-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="106b3-125">INPUTS</span></span>

### <span data-ttu-id="106b3-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="106b3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="106b3-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="106b3-127">OUTPUTS</span></span>

### <span data-ttu-id="106b3-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="106b3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="106b3-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="106b3-129">NOTES</span></span>

## <span data-ttu-id="106b3-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="106b3-130">RELATED LINKS</span></span>
