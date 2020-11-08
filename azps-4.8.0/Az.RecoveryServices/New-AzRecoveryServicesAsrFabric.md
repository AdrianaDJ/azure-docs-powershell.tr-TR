---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267666"
---
# <span data-ttu-id="c487f-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c487f-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="c487f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c487f-102">SYNOPSIS</span></span>
<span data-ttu-id="c487f-103">Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c487f-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="c487f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c487f-104">SYNTAX</span></span>

### <span data-ttu-id="c487f-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c487f-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c487f-106">'Ye</span><span class="sxs-lookup"><span data-stu-id="c487f-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c487f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c487f-107">DESCRIPTION</span></span>
<span data-ttu-id="c487f-108">**New-AzRecoveryServicesAsrFabric** cmdlet 'i belirtilen türde bir Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c487f-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="c487f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c487f-109">EXAMPLES</span></span>

### <span data-ttu-id="c487f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c487f-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="c487f-111">Geçirilen adla yapı oluşturmayı başlatır ve doku oluşturma işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c487f-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="c487f-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c487f-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="c487f-113">Geçilen adla Azure Fabric oluşturmayı başlatır ve doku oluşturma işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c487f-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="c487f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c487f-114">PARAMETERS</span></span>

### <span data-ttu-id="c487f-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="c487f-115">-Azure</span></span>
<span data-ttu-id="c487f-116">Switch parametresi, Azure Fabric oluşturulacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c487f-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="c487f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c487f-117">-DefaultProfile</span></span>
<span data-ttu-id="c487f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c487f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c487f-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="c487f-119">-Location</span></span>
<span data-ttu-id="c487f-120">Oluşturulan Fabric nesnesine karşılık gelen Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c487f-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="c487f-121">Azure Site Recovery Fabric nesnesi bir bölgeyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c487f-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="c487f-122">İki Azure bölgesi arasında çoğaltılan sanal makinelerin birincil yapısı birincil Azure bölgesini ve kurtarma yapınızı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c487f-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="c487f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c487f-123">-Name</span></span>
<span data-ttu-id="c487f-124">Azure Site Recovery yapısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c487f-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="c487f-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="c487f-125">-Type</span></span>
<span data-ttu-id="c487f-126">Azure Site Recovery Fabric türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c487f-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="c487f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="c487f-127">-Confirm</span></span>
<span data-ttu-id="c487f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c487f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c487f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c487f-129">-WhatIf</span></span>
<span data-ttu-id="c487f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c487f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c487f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c487f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c487f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c487f-132">CommonParameters</span></span>
<span data-ttu-id="c487f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c487f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c487f-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c487f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c487f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c487f-135">INPUTS</span></span>

### <span data-ttu-id="c487f-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c487f-136">None</span></span>

## <span data-ttu-id="c487f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c487f-137">OUTPUTS</span></span>

### <span data-ttu-id="c487f-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c487f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c487f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c487f-139">NOTES</span></span>

## <span data-ttu-id="c487f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c487f-140">RELATED LINKS</span></span>

[<span data-ttu-id="c487f-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c487f-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="c487f-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c487f-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
