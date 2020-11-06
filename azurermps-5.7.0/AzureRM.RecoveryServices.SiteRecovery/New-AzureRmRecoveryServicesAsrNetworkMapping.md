---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a989b93b2c2ac2a1c292b736275da5cb91c7042d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591646"
---
# <span data-ttu-id="3f5c7-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3f5c7-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="3f5c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5c7-103">İki ağ arasında ASR ağ eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f5c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f5c7-104">SYNTAX</span></span>

### <span data-ttu-id="3f5c7-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f5c7-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f5c7-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3f5c7-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5c7-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="3f5c7-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f5c7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f5c7-108">DESCRIPTION</span></span>
<span data-ttu-id="3f5c7-109">**Yeni-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'i, iki ağ arasında ASR ağ eşlemesi oluşturma işlemini başlatır ve işlemi izlemek IÇIN kullanılan ASR ışı için ASR iş nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3f5c7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f5c7-110">EXAMPLES</span></span>

### <span data-ttu-id="3f5c7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3f5c7-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="3f5c7-112">Belirtilen adı, birincil ve kurtarma ağlarını kullanarak ağ eşlemesi oluşturma işlemini başlatır ve işlemi izlemek için bir ASR işi döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="3f5c7-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3f5c7-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="3f5c7-114">Belirtilen adı, birincil ve kurtarma ağlarını kullanarak oluşturma işlemi için Ağ eşlemesini başlatır ve işlemi izlemek için bir ASR işi (Azure 'dan Azure 'a) döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="3f5c7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f5c7-115">PARAMETERS</span></span>

### <span data-ttu-id="3f5c7-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3f5c7-116">-AzureToAzure</span></span>
<span data-ttu-id="3f5c7-117">Oluşturulan ağ eşlemesinin iki Azure bölgesi arasında Azure sanal makinelerini çoğaltmakta kullanılacağını belirten anahtar parametresi.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5c7-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f5c7-118">-Confirm</span></span>
<span data-ttu-id="3f5c7-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f5c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5c7-120">-DefaultProfile</span></span>
<span data-ttu-id="3f5c7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="3f5c7-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f5c7-122">-Name</span></span>
<span data-ttu-id="3f5c7-123">Oluşturulacak ASR ağ eşlemesinin adı.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-123">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="3f5c7-124">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="3f5c7-124">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="3f5c7-125">Eşleme için birincil ağın Azure sanal ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-125">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5c7-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="3f5c7-126">-PrimaryFabric</span></span>
<span data-ttu-id="3f5c7-127">Eşlemenin oluşturulması gereken ASR yapınızı belirtimi.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-127">Specifes the ASR fabric where mapping should be created.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5c7-128">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="3f5c7-128">-PrimaryNetwork</span></span>
<span data-ttu-id="3f5c7-129">ASR ağ eşlemesi için birincil ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-129">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5c7-130">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="3f5c7-130">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="3f5c7-131">Ağ eşlemesi için kurtarma Azure ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-131">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5c7-132">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="3f5c7-132">-RecoveryFabric</span></span>
<span data-ttu-id="3f5c7-133">Kurtarma Azure bölgesine karşılık gelen Azure Site Recovery Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-133">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5c7-134">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="3f5c7-134">-RecoveryNetwork</span></span>
<span data-ttu-id="3f5c7-135">ASR ağ eşlemesi için kurtarma ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-135">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5c7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f5c7-136">-WhatIf</span></span>
<span data-ttu-id="3f5c7-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f5c7-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f5c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5c7-139">CommonParameters</span></span>
<span data-ttu-id="3f5c7-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5c7-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f5c7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5c7-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f5c7-142">INPUTS</span></span>

### <span data-ttu-id="3f5c7-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="3f5c7-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="3f5c7-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f5c7-144">OUTPUTS</span></span>

### <span data-ttu-id="3f5c7-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3f5c7-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3f5c7-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f5c7-146">NOTES</span></span>

## <span data-ttu-id="3f5c7-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f5c7-147">RELATED LINKS</span></span>

[<span data-ttu-id="3f5c7-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3f5c7-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="3f5c7-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3f5c7-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
