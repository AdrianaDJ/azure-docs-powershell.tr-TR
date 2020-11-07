---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 5627b94f87d69fab6b760bf05f1e22566992048b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763653"
---
# <span data-ttu-id="91369-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="91369-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="91369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91369-102">SYNOPSIS</span></span>
<span data-ttu-id="91369-103">Belirtilen çoğaltma korumalı öğesi için hedef ağ ve sanal makine boyutu gibi kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="91369-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91369-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91369-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91369-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91369-105">DESCRIPTION</span></span>
<span data-ttu-id="91369-106">**Set-Azurermrecoveryservicesasrreplicationkorunabilir** .</span><span class="sxs-lookup"><span data-stu-id="91369-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="91369-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91369-107">EXAMPLES</span></span>

### <span data-ttu-id="91369-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91369-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="91369-109">Belirtilen parametreleri kullanarak çoğaltma koruması öğesini güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="91369-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="91369-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91369-110">PARAMETERS</span></span>

### <span data-ttu-id="91369-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91369-111">-InputObject</span></span>
<span data-ttu-id="91369-112">Cmdlet 'e giriş nesnesi: Bu, güncelleştirilecek çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="91369-112">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91369-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="91369-113">-LicenseType</span></span>
<span data-ttu-id="91369-114">Windows Server sanal makinelerinde kullanılacak lisans türü seçimini belirtin.</span><span class="sxs-lookup"><span data-stu-id="91369-114">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="91369-115">Geçiş için Azure Karma Kullanım avantajını (HUB) kullanmaya hak duyuyorsanız ve bu korumalı öğenin yerine çalışırken HUB ayarının kullanılacağını belirtmek istiyorsanız, lisans türünü WindowsServer olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="91369-115">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="91369-116">-Name</span></span>
<span data-ttu-id="91369-117">Yük devretmenin ardından oluşturulacak kurtarma sanal makinesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91369-117">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-118">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="91369-118">-NicSelectionType</span></span>
<span data-ttu-id="91369-119">Kullanıcı tarafından ayarlanan ağ arabirim kartı (NIC) özelliklerini belirtir veya varsayılan olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="91369-119">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="91369-120">Varsayılan değerlere dönmek için NotSelected belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="91369-120">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-121">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="91369-121">-PrimaryNic</span></span>
<span data-ttu-id="91369-122">Bu cmdlet 'in kurtarma ağı özelliğini ayarladığı sanal makinenin NIC 'ini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91369-122">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-123">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="91369-123">-RecoveryNetworkId</span></span>
<span data-ttu-id="91369-124">Korunan öğenin yük devri gerektiği Azure sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="91369-124">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-125">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="91369-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="91369-126">Kurtarmada birincil NIC 'ye atanması gereken statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91369-126">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-127">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="91369-127">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="91369-128">Korumalı öğenin bu NIC 'in yük devretmeye bağlanması gereken, kurtarma Azure sanal ağında alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91369-128">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-129">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="91369-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="91369-130">Korunan öğenin yük devretmeye kurtarılacağı kurtarma bölgesindeki Azure Kaynak grubunun KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="91369-130">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-131">-Boyut</span><span class="sxs-lookup"><span data-stu-id="91369-131">-Size</span></span>
<span data-ttu-id="91369-132">Kurtarma sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="91369-132">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="91369-133">Değer, Azure sanal makinelerinin desteklediği boyutlar kümesinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="91369-133">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91369-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="91369-134">-Confirm</span></span>
<span data-ttu-id="91369-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91369-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91369-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91369-136">-WhatIf</span></span>
<span data-ttu-id="91369-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91369-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91369-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91369-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91369-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91369-139">CommonParameters</span></span>
<span data-ttu-id="91369-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91369-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91369-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91369-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91369-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91369-142">INPUTS</span></span>

### <span data-ttu-id="91369-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="91369-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="91369-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91369-144">OUTPUTS</span></span>

### <span data-ttu-id="91369-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="91369-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="91369-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91369-146">NOTES</span></span>

## <span data-ttu-id="91369-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91369-147">RELATED LINKS</span></span>

[<span data-ttu-id="91369-148">Get-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="91369-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="91369-149">New-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="91369-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="91369-150">Remove-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="91369-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
