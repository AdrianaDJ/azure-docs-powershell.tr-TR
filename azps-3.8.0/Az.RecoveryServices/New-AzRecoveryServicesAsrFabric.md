---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104704"
---
# <span data-ttu-id="10963-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="10963-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="10963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10963-102">SYNOPSIS</span></span>
<span data-ttu-id="10963-103">Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10963-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="10963-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10963-104">SYNTAX</span></span>

### <span data-ttu-id="10963-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="10963-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10963-106">'Ye</span><span class="sxs-lookup"><span data-stu-id="10963-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10963-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="10963-107">DESCRIPTION</span></span>
<span data-ttu-id="10963-108">**New-AzRecoveryServicesAsrFabric** cmdlet 'i belirtilen türde bir Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10963-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="10963-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10963-109">EXAMPLES</span></span>

### <span data-ttu-id="10963-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="10963-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="10963-111">Geçirilen adla yapı oluşturmayı başlatır ve doku oluşturma işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="10963-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="10963-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="10963-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="10963-113">Geçilen adla Azure Fabric oluşturmayı başlatır ve doku oluşturma işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="10963-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="10963-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10963-114">PARAMETERS</span></span>

### <span data-ttu-id="10963-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="10963-115">-Azure</span></span>
<span data-ttu-id="10963-116">Switch parametresi, Azure Fabric oluşturulacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10963-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10963-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10963-117">-DefaultProfile</span></span>
<span data-ttu-id="10963-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10963-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="10963-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="10963-119">-Location</span></span>
<span data-ttu-id="10963-120">Oluşturulan Fabric nesnesine karşılık gelen Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10963-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="10963-121">Azure Site Recovery Fabric nesnesi bir bölgeyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="10963-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="10963-122">İki Azure bölgesi arasında çoğaltılan sanal makinelerin birincil yapısı birincil Azure bölgesini ve kurtarma yapınızı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="10963-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10963-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="10963-123">-Name</span></span>
<span data-ttu-id="10963-124">Azure Site Recovery yapısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10963-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="10963-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="10963-125">-Type</span></span>
<span data-ttu-id="10963-126">Azure Site Recovery Fabric türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="10963-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10963-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="10963-127">-Confirm</span></span>
<span data-ttu-id="10963-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10963-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10963-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10963-129">-WhatIf</span></span>
<span data-ttu-id="10963-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10963-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10963-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="10963-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10963-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10963-132">CommonParameters</span></span>
<span data-ttu-id="10963-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10963-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10963-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="10963-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10963-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10963-135">INPUTS</span></span>

### <span data-ttu-id="10963-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="10963-136">None</span></span>

## <span data-ttu-id="10963-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10963-137">OUTPUTS</span></span>

### <span data-ttu-id="10963-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="10963-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="10963-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10963-139">NOTES</span></span>

## <span data-ttu-id="10963-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10963-140">RELATED LINKS</span></span>

[<span data-ttu-id="10963-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="10963-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="10963-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="10963-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
