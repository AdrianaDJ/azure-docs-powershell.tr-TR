---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: a3ae73e9831202418d35481270a1d04b1cb09a59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589721"
---
# <span data-ttu-id="debf2-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="debf2-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="debf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="debf2-102">SYNOPSIS</span></span>
<span data-ttu-id="debf2-103">Belirtilen çoğaltma korumalı öğesi için hedef ağ ve sanal makine boyutu gibi kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="debf2-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="debf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="debf2-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="debf2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="debf2-105">DESCRIPTION</span></span>
<span data-ttu-id="debf2-106">**Set-Azurermrecoveryservicesasrreplicationkorunabilir** .</span><span class="sxs-lookup"><span data-stu-id="debf2-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="debf2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="debf2-107">EXAMPLES</span></span>

### <span data-ttu-id="debf2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="debf2-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="debf2-109">Belirtilen parametreleri kullanarak çoğaltma koruması öğesini güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="debf2-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="debf2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="debf2-110">PARAMETERS</span></span>

### <span data-ttu-id="debf2-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="debf2-111">-Confirm</span></span>
<span data-ttu-id="debf2-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="debf2-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="debf2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debf2-113">-DefaultProfile</span></span>
<span data-ttu-id="debf2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="debf2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="debf2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="debf2-115">-InputObject</span></span>
<span data-ttu-id="debf2-116">Cmdlet 'e giriş nesnesi: Bu, güncelleştirilecek çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="debf2-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="debf2-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="debf2-117">-LicenseType</span></span>
<span data-ttu-id="debf2-118">Windows Server sanal makinelerinde kullanılacak lisans türü seçimini belirtin.</span><span class="sxs-lookup"><span data-stu-id="debf2-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="debf2-119">Geçiş için Azure Karma Kullanım avantajını (HUB) kullanmaya hak duyuyorsanız ve bu korumalı öğenin yerine çalışırken HUB ayarının kullanılacağını belirtmek istiyorsanız, lisans türünü WindowsServer olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="debf2-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="debf2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="debf2-120">-Name</span></span>
<span data-ttu-id="debf2-121">Yük devretmenin ardından oluşturulacak kurtarma sanal makinesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="debf2-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="debf2-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="debf2-122">-NicSelectionType</span></span>
<span data-ttu-id="debf2-123">Kullanıcı tarafından ayarlanan ağ arabirim kartı (NIC) özelliklerini belirtir veya varsayılan olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="debf2-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="debf2-124">Varsayılan değerlere dönmek için NotSelected belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="debf2-124">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="debf2-125">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="debf2-125">-PrimaryNic</span></span>
<span data-ttu-id="debf2-126">Bu cmdlet 'in kurtarma ağı özelliğini ayarladığı sanal makinenin NIC 'ini belirtir.</span><span class="sxs-lookup"><span data-stu-id="debf2-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="debf2-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="debf2-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="debf2-128">Yük devretme sonrasında çoğaltma korumalı öğe için kullanılabilirlik kümesi.</span><span class="sxs-lookup"><span data-stu-id="debf2-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="debf2-129">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="debf2-129">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="debf2-130">Bu sanal makinenin yük devretmesine yönelik kurtarma bulut hizmetinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="debf2-130">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="debf2-131">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="debf2-131">-RecoveryNetworkId</span></span>
<span data-ttu-id="debf2-132">Korunan öğenin yük devri gerektiği Azure sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="debf2-132">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="debf2-133">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="debf2-133">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="debf2-134">Kurtarmada birincil NIC 'ye atanması gereken statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="debf2-134">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="debf2-135">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="debf2-135">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="debf2-136">Korumalı öğenin bu NIC 'in yük devretmeye bağlanması gereken, kurtarma Azure sanal ağında alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="debf2-136">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="debf2-137">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="debf2-137">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="debf2-138">Korunan öğenin yük devretmeye kurtarılacağı kurtarma bölgesindeki Azure Kaynak grubunun KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="debf2-138">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="debf2-139">-Boyut</span><span class="sxs-lookup"><span data-stu-id="debf2-139">-Size</span></span>
<span data-ttu-id="debf2-140">Kurtarma sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="debf2-140">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="debf2-141">Değer, Azure sanal makinelerinin desteklediği boyutlar kümesinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="debf2-141">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="debf2-142">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="debf2-142">-UseManagedDisk</span></span>
<span data-ttu-id="debf2-143">Yük devretmenin üstünde oluşturulan Azure sanal makinesinin yönetilen diskleri kullanıp kullanmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="debf2-143">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debf2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="debf2-144">-WhatIf</span></span>
<span data-ttu-id="debf2-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="debf2-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="debf2-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="debf2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="debf2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debf2-147">CommonParameters</span></span>
<span data-ttu-id="debf2-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="debf2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debf2-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debf2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debf2-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="debf2-150">INPUTS</span></span>

### <span data-ttu-id="debf2-151">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="debf2-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="debf2-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="debf2-152">OUTPUTS</span></span>

### <span data-ttu-id="debf2-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="debf2-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="debf2-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="debf2-154">NOTES</span></span>

## <span data-ttu-id="debf2-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="debf2-155">RELATED LINKS</span></span>

[<span data-ttu-id="debf2-156">Get-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="debf2-156">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="debf2-157">New-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="debf2-157">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="debf2-158">Remove-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="debf2-158">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
