---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d387774ebf5f269474df959de981568141f90fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588395"
---
# <span data-ttu-id="287d1-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="287d1-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="287d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287d1-102">SYNOPSIS</span></span>
<span data-ttu-id="287d1-103">Belirtilen çoğaltma korumalı öğesi için hedef ağ ve sanal makine boyutu gibi kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="287d1-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="287d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="287d1-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="287d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="287d1-105">DESCRIPTION</span></span>
<span data-ttu-id="287d1-106">**Set-Azurermrecoveryservicesasrreplicationkorunabilir** .</span><span class="sxs-lookup"><span data-stu-id="287d1-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="287d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="287d1-107">EXAMPLES</span></span>

### <span data-ttu-id="287d1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="287d1-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="287d1-109">Belirtilen parametreleri kullanarak çoğaltma koruması öğesini güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="287d1-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="287d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="287d1-110">PARAMETERS</span></span>

### <span data-ttu-id="287d1-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="287d1-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="287d1-112">Güncelleştirme güvenilme yapılandırması 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-112">Specifies the update relication configration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287d1-113">-DefaultProfile</span></span>
<span data-ttu-id="287d1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="287d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="287d1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="287d1-115">-InputObject</span></span>
<span data-ttu-id="287d1-116">Cmdlet 'e giriş nesnesi: Bu, güncelleştirilecek çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="287d1-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="287d1-117">-LicenseType</span></span>
<span data-ttu-id="287d1-118">Windows Server sanal makinelerinde kullanılacak lisans türü seçimini belirtin.</span><span class="sxs-lookup"><span data-stu-id="287d1-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="287d1-119">Geçiş için Azure Karma Kullanım avantajını (HUB) kullanmaya hak duyuyorsanız ve bu korumalı öğenin yerine çalışırken HUB ayarının kullanılacağını belirtmek istiyorsanız, lisans türünü WindowsServer olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="287d1-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="287d1-120">-Name</span></span>
<span data-ttu-id="287d1-121">Yük devretmenin ardından oluşturulacak kurtarma sanal makinesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="287d1-122">-NicSelectionType</span></span>
<span data-ttu-id="287d1-123">Kullanıcı tarafından ayarlanan ağ arabirim kartı (NIC) özelliklerini belirtir veya varsayılan olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="287d1-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="287d1-124">Varsayılan değerlere dönmek için NotSelected belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="287d1-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-125">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="287d1-125">-PrimaryNic</span></span>
<span data-ttu-id="287d1-126">Bu cmdlet 'in kurtarma ağı özelliğini ayarladığı sanal makinenin NIC 'ini belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="287d1-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="287d1-128">Yük devretme sonrasında çoğaltma korumalı öğe için kullanılabilirlik kümesi.</span><span class="sxs-lookup"><span data-stu-id="287d1-128">Availability set for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-129">-Recoverybootdiagstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="287d1-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="287d1-130">Kurtarma Azure VM için önyükleme tanılaması depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-131">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="287d1-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="287d1-132">Bu sanal makinenin yük devretmesine yönelik kurtarma bulut hizmetinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="287d1-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-133">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="287d1-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="287d1-134">Korunan öğenin yük devri gerektiği Azure sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-135">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="287d1-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="287d1-136">Kurtarmada birincil NIC 'ye atanması gereken statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="287d1-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="287d1-138">Korumalı öğenin bu NIC 'in yük devretmeye bağlanması gereken, kurtarma Azure sanal ağında alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-139">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="287d1-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="287d1-140">Korunan öğenin yük devretmeye kurtarılacağı kurtarma bölgesindeki Azure Kaynak grubunun KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="287d1-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-141">-Boyut</span><span class="sxs-lookup"><span data-stu-id="287d1-141">-Size</span></span>
<span data-ttu-id="287d1-142">Kurtarma sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="287d1-143">Değer, Azure sanal makinelerinin desteklediği boyutlar kümesinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="287d1-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="287d1-144">-UseManagedDisk</span></span>
<span data-ttu-id="287d1-145">Yük devretmenin üstünde oluşturulan Azure sanal makinesinin yönetilen diskleri kullanıp kullanmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="287d1-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287d1-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="287d1-146">-Confirm</span></span>
<span data-ttu-id="287d1-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="287d1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="287d1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287d1-148">-WhatIf</span></span>
<span data-ttu-id="287d1-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="287d1-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="287d1-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="287d1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="287d1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287d1-151">CommonParameters</span></span>
<span data-ttu-id="287d1-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="287d1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287d1-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287d1-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287d1-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="287d1-154">INPUTS</span></span>

### <span data-ttu-id="287d1-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="287d1-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="287d1-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="287d1-156">OUTPUTS</span></span>

### <span data-ttu-id="287d1-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="287d1-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="287d1-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="287d1-158">NOTES</span></span>

## <span data-ttu-id="287d1-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="287d1-159">RELATED LINKS</span></span>

[<span data-ttu-id="287d1-160">Get-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="287d1-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="287d1-161">New-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="287d1-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="287d1-162">Remove-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="287d1-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
