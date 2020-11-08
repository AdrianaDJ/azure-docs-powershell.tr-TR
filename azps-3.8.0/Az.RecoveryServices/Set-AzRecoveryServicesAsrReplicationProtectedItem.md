---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 494edd4f399855512cd7b0a847f261e711bb01cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103531"
---
# <span data-ttu-id="6dbeb-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6dbeb-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="6dbeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dbeb-102">SYNOPSIS</span></span>
<span data-ttu-id="6dbeb-103">Belirtilen çoğaltma korumalı öğesi için hedef ağ ve sanal makine boyutu gibi kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="6dbeb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dbeb-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dbeb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dbeb-105">DESCRIPTION</span></span>
<span data-ttu-id="6dbeb-106">**Set-Azrecoveryservicesasrreplicationkoruttıtem** cmdlet 'ı, çoğaltma korumalı bir öğenin kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="6dbeb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dbeb-107">EXAMPLES</span></span>

### <span data-ttu-id="6dbeb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6dbeb-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="6dbeb-109">Belirtilen parametreleri kullanarak çoğaltma korumalı öğe ayarlarını güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6dbeb-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6dbeb-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="6dbeb-111">Belirtilen parametreleri kullanarak çoğaltma korumalı öğe ağı arabirim kartı (NIC azaltma) ayarlarını güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6dbeb-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6dbeb-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="6dbeb-113">Belirtilen parametreleri kullanarak çoğaltma korumalı öğesini (kurtarılan VM için kullanılacak) ayarlar 'ı güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6dbeb-114">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="6dbeb-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="6dbeb-115">Belirtilen parametreleri kullanarak çoğaltma korumalı öğe NIC 'ı (kurtarılan VM için kullanılacak) ayarlar ve işlemi izlemek için kullanılan ASR işini döndüren işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6dbeb-116">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="6dbeb-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="6dbeb-117">Çoğaltma korumalı öğesini güncelleştirme işlemini başlatır kurtarma VM 'de (Azure 'dan Azure için olağanüstü durum kurtarması için)</span><span class="sxs-lookup"><span data-stu-id="6dbeb-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="6dbeb-118">EnableAcceleratedNetworkingOnRecovery-hızlandırılmış ağı devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="6dbeb-119">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="6dbeb-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="6dbeb-120">Belirtilen şifreli çoğaltma korumalı öğesinin güncelleştirme işlemini başlatıp yük devretme VM için sağlanan şifreleme ayrıntılarını kullanma.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

## <span data-ttu-id="6dbeb-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dbeb-121">PARAMETERS</span></span>

### <span data-ttu-id="6dbeb-122">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dbeb-122">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="6dbeb-123">Test yük devretmesi ve yük devretme NIC yapılandırma ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-123">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dbeb-124">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dbeb-124">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="6dbeb-125">Yönetilen disk VM için motive edilecek disk yapılandırmasını belirtir (Azure 'dan Azure 'a Azure DR manzara).</span><span class="sxs-lookup"><span data-stu-id="6dbeb-125">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="6dbeb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dbeb-126">-DefaultProfile</span></span>
<span data-ttu-id="6dbeb-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6dbeb-128">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="6dbeb-128">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="6dbeb-129">Yük devretme sonrasında kurtarma VM olarak kullanılacak sürüm (Azure disk şifrelemesi) içeren disk şifrelemesi gizlilik URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-129">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6dbeb-130">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="6dbeb-130">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="6dbeb-131">Yük devretmenin ardından kurtarma VM olarak kullanılacak disk şifrelemesi gizli Anahtar Kasası KIMLIĞINI (Azure disk şifrelemesi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-131">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6dbeb-132">-Diskivseçtodiskencryptionsetmap</span><span class="sxs-lookup"><span data-stu-id="6dbeb-132">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="6dbeb-133">Disk kaynağı kimliği 'nin disk şifrelemesi kümesi ARM kimliğine sahip sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-133">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dbeb-134">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="6dbeb-134">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="6dbeb-135">Yük devretme işlemi hızlandırılmış ağ kullanır</span><span class="sxs-lookup"><span data-stu-id="6dbeb-135">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dbeb-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dbeb-136">-InputObject</span></span>
<span data-ttu-id="6dbeb-137">Cmdlet 'e giriş nesnesi: Bu, güncelleştirilecek çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-137">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="6dbeb-138">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="6dbeb-138">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="6dbeb-139">Yük devretmenin ardından kurtarma VM olarak kullanılacak disk şifrelemesi anahtar URL sürümünü (Azure disk şifrelemesi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-139">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6dbeb-140">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="6dbeb-140">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="6dbeb-141">Yük devretmenin ardından kurtarma VM olarak kullanılacak Anahtar Kasası KIMLIĞI 'ni (Azure disk şifrelemesi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-141">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="6dbeb-142">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6dbeb-142">-LicenseType</span></span>
<span data-ttu-id="6dbeb-143">Windows Server sanal makinelerinde kullanılacak lisans türü seçimini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-143">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="6dbeb-144">Geçiş için Azure Karma Kullanım avantajını (HUB) kullanmaya hak duyuyorsanız ve bu korumalı öğenin yerine çalışırken HUB ayarının kullanılacağını belirtmek istiyorsanız, lisans türünü WindowsServer olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-144">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="6dbeb-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="6dbeb-145">-Name</span></span>
<span data-ttu-id="6dbeb-146">Yük devretmenin ardından oluşturulacak kurtarma sanal makinesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-146">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="6dbeb-147">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="6dbeb-147">-NicSelectionType</span></span>
<span data-ttu-id="6dbeb-148">Kullanıcı tarafından ayarlanan ağ arabirim kartı (NIC) özelliklerini belirtir veya varsayılan olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-148">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="6dbeb-149">Varsayılan değerlere dönmek için NotSelected belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-149">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="6dbeb-150">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="6dbeb-150">-PrimaryNic</span></span>
<span data-ttu-id="6dbeb-151">Yük devretmenin ardından, recvcovery VM için birincil NIC olarak kullanılacak NIC 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-151">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="6dbeb-152">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6dbeb-152">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="6dbeb-153">Yük devretme sonrasında çoğaltma korumalı öğe için kullanılabilirlik kümesi.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-153">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="6dbeb-154">-Recoverybootdiagstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="6dbeb-154">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="6dbeb-155">Kurtarma Azure VM için önyükleme tanılaması depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-155">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="6dbeb-156">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="6dbeb-156">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="6dbeb-157">Bu sanal makinenin yük devretmesine yönelik kurtarma bulut hizmetinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-157">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="6dbeb-158">-Recoverylbbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="6dbeb-158">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="6dbeb-159">Kurtarma NIC ile ilişkilendirilecek hedef arka uç adres havuzlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-159">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dbeb-160">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="6dbeb-160">-RecoveryNetworkId</span></span>
<span data-ttu-id="6dbeb-161">Korunan öğenin yük devri gerektiği Azure sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-161">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="6dbeb-162">-Recoverynetworksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="6dbeb-162">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="6dbeb-163">Kurtarma NIC ile ilişkilendirilecek ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-163">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="6dbeb-164">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="6dbeb-164">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="6dbeb-165">Kurtarmada birincil NIC 'ye atanması gereken statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-165">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="6dbeb-166">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="6dbeb-166">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="6dbeb-167">Korumalı öğenin bu NIC 'in yük devretmeye bağlanması gereken, kurtarma Azure sanal ağında alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-167">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="6dbeb-168">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="6dbeb-168">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="6dbeb-169">Kurtarma NIC ile ilişkilendirilecek genel IP adresi kaynağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-169">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="6dbeb-170">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="6dbeb-170">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="6dbeb-171">Korunan öğenin yük devretmeye kurtarılacağı kurtarma bölgesindeki Azure Kaynak grubunun KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-171">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="6dbeb-172">-Boyut</span><span class="sxs-lookup"><span data-stu-id="6dbeb-172">-Size</span></span>
<span data-ttu-id="6dbeb-173">Kurtarma sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-173">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="6dbeb-174">Değer, Azure sanal makinelerinin desteklediği boyutlar kümesinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-174">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="6dbeb-175">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="6dbeb-175">-TfoAzureVMName</span></span>
<span data-ttu-id="6dbeb-176">Test yük devretme VM 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-176">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="6dbeb-177">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="6dbeb-177">-UpdateNic</span></span>
<span data-ttu-id="6dbeb-178">Bu cmdlet 'in kurtarma ağı özelliğini motive olarak ayarladığı sanal makinenin NIC 'ini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-178">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="6dbeb-179">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6dbeb-179">-UseManagedDisk</span></span>
<span data-ttu-id="6dbeb-180">Yük devretmenin üstünde oluşturulan Azure sanal makinesinin yönetilen diskleri kullanıp kullanmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-180">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="6dbeb-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="6dbeb-181">-Confirm</span></span>
<span data-ttu-id="6dbeb-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dbeb-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dbeb-183">-WhatIf</span></span>
<span data-ttu-id="6dbeb-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dbeb-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dbeb-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dbeb-186">CommonParameters</span></span>
<span data-ttu-id="6dbeb-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dbeb-188">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dbeb-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dbeb-189">INPUTS</span></span>

### <span data-ttu-id="6dbeb-190">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="6dbeb-190">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6dbeb-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dbeb-191">OUTPUTS</span></span>

### <span data-ttu-id="6dbeb-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6dbeb-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6dbeb-193">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dbeb-193">NOTES</span></span>

## <span data-ttu-id="6dbeb-194">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dbeb-194">RELATED LINKS</span></span>

[<span data-ttu-id="6dbeb-195">Get-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6dbeb-196">New-Azrecoveryservicesasrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="6dbeb-196">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6dbeb-197">Remove-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="6dbeb-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
