---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 1da06582d442c96f74579e9fdf3009325f996012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764319"
---
# <span data-ttu-id="6c3f1-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6c3f1-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="6c3f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="6c3f1-103">Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c3f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c3f1-104">SYNTAX</span></span>

### <span data-ttu-id="6c3f1-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6c3f1-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c3f1-106">'Ye</span><span class="sxs-lookup"><span data-stu-id="6c3f1-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c3f1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c3f1-107">DESCRIPTION</span></span>
<span data-ttu-id="6c3f1-108">**New-AzureRmRecoveryServicesAsrFabric** cmdlet 'i belirtilen türde bir Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="6c3f1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c3f1-109">EXAMPLES</span></span>

### <span data-ttu-id="6c3f1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6c3f1-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="6c3f1-111">Geçirilen adla yapı oluşturmayı başlatır ve doku oluşturma işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="6c3f1-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6c3f1-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="6c3f1-113">Geçilen adla Azure Fabric oluşturmayı başlatır ve doku oluşturma işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="6c3f1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c3f1-114">PARAMETERS</span></span>

### <span data-ttu-id="6c3f1-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="6c3f1-115">-Azure</span></span>
<span data-ttu-id="6c3f1-116">Switch parametresi, Azure Fabric oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-116">Switch parameter indicates creation of azure fabric.</span></span>

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

### <span data-ttu-id="6c3f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c3f1-117">-DefaultProfile</span></span>
<span data-ttu-id="6c3f1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c3f1-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="6c3f1-119">-Location</span></span>
<span data-ttu-id="6c3f1-120">Oluşturulan Fabric nesnesine karşılık gelen Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="6c3f1-121">Azure Site Recovery Fabric nesnesi bir bölgeyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="6c3f1-122">İki Azure bölgesi arasında çoğaltılan sanal makinelerin birincil yapısı birincil Azure bölgesini ve kurtarma yapınızı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="6c3f1-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c3f1-123">-Name</span></span>
<span data-ttu-id="6c3f1-124">Azure Site Recovery yapısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="6c3f1-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="6c3f1-125">-Type</span></span>
<span data-ttu-id="6c3f1-126">Azure Site Recovery Fabric türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="6c3f1-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c3f1-127">-Confirm</span></span>
<span data-ttu-id="6c3f1-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c3f1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c3f1-129">-WhatIf</span></span>
<span data-ttu-id="6c3f1-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c3f1-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c3f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c3f1-132">CommonParameters</span></span>
<span data-ttu-id="6c3f1-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c3f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c3f1-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c3f1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c3f1-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c3f1-135">INPUTS</span></span>

### <span data-ttu-id="6c3f1-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6c3f1-136">None</span></span>

## <span data-ttu-id="6c3f1-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c3f1-137">OUTPUTS</span></span>

### <span data-ttu-id="6c3f1-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6c3f1-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6c3f1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c3f1-139">NOTES</span></span>

## <span data-ttu-id="6c3f1-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c3f1-140">RELATED LINKS</span></span>

[<span data-ttu-id="6c3f1-141">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6c3f1-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="6c3f1-142">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6c3f1-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
