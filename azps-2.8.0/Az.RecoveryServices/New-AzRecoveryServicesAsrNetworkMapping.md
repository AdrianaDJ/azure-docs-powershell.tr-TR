---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 0af3ffc25571273ebe572ee315b4e3c97de8f116
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932980"
---
# <span data-ttu-id="eae27-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="eae27-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="eae27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eae27-102">SYNOPSIS</span></span>
<span data-ttu-id="eae27-103">İki ağ arasında ASR ağ eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eae27-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="eae27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eae27-104">SYNTAX</span></span>

### <span data-ttu-id="eae27-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eae27-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eae27-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="eae27-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eae27-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="eae27-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eae27-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eae27-108">DESCRIPTION</span></span>
<span data-ttu-id="eae27-109">**Yeni-AzRecoveryServicesAsrNetworkMapping** cmdlet 'i, iki ağ arasında ASR ağ eşlemesi oluşturma işlemini başlatır ve işlemi izlemek IÇIN kullanılan ASR ışı için ASR iş nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="eae27-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="eae27-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eae27-110">EXAMPLES</span></span>

### <span data-ttu-id="eae27-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eae27-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="eae27-112">Belirtilen adı, birincil ve kurtarma ağlarını kullanarak ağ eşlemesi oluşturma işlemini başlatır ve işlemi izlemek için bir ASR işi döndürür.</span><span class="sxs-lookup"><span data-stu-id="eae27-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="eae27-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="eae27-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="eae27-114">Belirtilen adı, birincil ve kurtarma ağlarını kullanarak oluşturma işlemi için Ağ eşlemesini başlatır ve işlemi izlemek için bir ASR işi (Azure 'dan Azure 'a) döndürür.</span><span class="sxs-lookup"><span data-stu-id="eae27-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="eae27-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eae27-115">PARAMETERS</span></span>

### <span data-ttu-id="eae27-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="eae27-116">-AzureToAzure</span></span>
<span data-ttu-id="eae27-117">{{Fill AzureToAzure açıklama}}</span><span class="sxs-lookup"><span data-stu-id="eae27-117">{{Fill AzureToAzure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eae27-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae27-118">-DefaultProfile</span></span>
<span data-ttu-id="eae27-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eae27-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="eae27-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="eae27-120">-Name</span></span>
<span data-ttu-id="eae27-121">Oluşturulacak ASR ağ eşlemesinin adı.</span><span class="sxs-lookup"><span data-stu-id="eae27-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="eae27-122">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="eae27-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="eae27-123">Eşleme için birincil ağın Azure sanal ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="eae27-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eae27-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="eae27-124">-PrimaryFabric</span></span>
<span data-ttu-id="eae27-125">Eşlemenin oluşturulması gereken ASR yapınızı belirtir.</span><span class="sxs-lookup"><span data-stu-id="eae27-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eae27-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="eae27-126">-PrimaryNetwork</span></span>
<span data-ttu-id="eae27-127">ASR ağ eşlemesi için birincil ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eae27-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eae27-128">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="eae27-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="eae27-129">Ağ eşlemesi için kurtarma Azure ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="eae27-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eae27-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="eae27-130">-RecoveryFabric</span></span>
<span data-ttu-id="eae27-131">Kurtarma Azure bölgesine karşılık gelen Azure Site Recovery Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="eae27-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eae27-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="eae27-132">-RecoveryNetwork</span></span>
<span data-ttu-id="eae27-133">ASR ağ eşlemesi için kurtarma ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eae27-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eae27-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="eae27-134">-Confirm</span></span>
<span data-ttu-id="eae27-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eae27-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eae27-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eae27-136">-WhatIf</span></span>
<span data-ttu-id="eae27-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eae27-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eae27-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eae27-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eae27-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae27-139">CommonParameters</span></span>
<span data-ttu-id="eae27-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eae27-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae27-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eae27-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae27-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eae27-142">INPUTS</span></span>

### <span data-ttu-id="eae27-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="eae27-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="eae27-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eae27-144">OUTPUTS</span></span>

### <span data-ttu-id="eae27-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eae27-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eae27-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eae27-146">NOTES</span></span>

## <span data-ttu-id="eae27-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eae27-147">RELATED LINKS</span></span>

[<span data-ttu-id="eae27-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="eae27-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="eae27-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="eae27-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)