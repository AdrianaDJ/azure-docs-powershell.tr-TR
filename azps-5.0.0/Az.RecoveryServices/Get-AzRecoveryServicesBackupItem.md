---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323068"
---
# <span data-ttu-id="a35eb-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a35eb-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="a35eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35eb-102">SYNOPSIS</span></span>

<span data-ttu-id="a35eb-103">Yedeklemede öğeleri bir kapsayıcıdan alır.</span><span class="sxs-lookup"><span data-stu-id="a35eb-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="a35eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a35eb-104">SYNTAX</span></span>

### <span data-ttu-id="a35eb-105">Getıtemsforcontainer (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a35eb-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35eb-106">Getıtemsforkasası</span><span class="sxs-lookup"><span data-stu-id="a35eb-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35eb-107">Getıtemsforpolicy</span><span class="sxs-lookup"><span data-stu-id="a35eb-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a35eb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a35eb-108">DESCRIPTION</span></span>

<span data-ttu-id="a35eb-109">**Get-Azrecoveryservicesbackupıtem** cmdlet 'i kapsayıcıdaki korumalı öğelerin listesini ve öğelerin koruma durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a35eb-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="a35eb-110">Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.</span><span class="sxs-lookup"><span data-stu-id="a35eb-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="a35eb-111">Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir yedekleme öğesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="a35eb-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="a35eb-112">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a35eb-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="a35eb-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a35eb-113">EXAMPLES</span></span>

### <span data-ttu-id="a35eb-114">Örnek 1: yedekleme kapsayıcısından öğe alma</span><span class="sxs-lookup"><span data-stu-id="a35eb-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="a35eb-115">İlk komut AzureVM türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a35eb-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a35eb-116">İkinci komut $Container V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a35eb-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="a35eb-117">Örnek 2: FriendlyName 'dan bir Azure dosya paylaşımı öğesi alma</span><span class="sxs-lookup"><span data-stu-id="a35eb-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="a35eb-118">İlk komut AzureStorage türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a35eb-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a35eb-119">İkinci komut, friendlyName FriendlyName parametresinde geçirilen değeri eşleştiren yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a35eb-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a35eb-120">FriendlyName parametresi kullanmak birden fazla Azure dosya paylaşımı döndürmeye neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="a35eb-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="a35eb-121">Böyle durumlarda, $BackupItem sonuç kümesinde döndürülen Name özelliği olarak-name parametresini geçirerek cmdlet 'i yürütün.</span><span class="sxs-lookup"><span data-stu-id="a35eb-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="a35eb-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a35eb-122">PARAMETERS</span></span>

### <span data-ttu-id="a35eb-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a35eb-123">-BackupManagementType</span></span>

<span data-ttu-id="a35eb-124">Korunan kaynakların sınıfı.</span><span class="sxs-lookup"><span data-stu-id="a35eb-124">The class of resources being protected.</span></span> <span data-ttu-id="a35eb-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a35eb-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a35eb-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="a35eb-126">AzureVM</span></span>
- <span data-ttu-id="a35eb-127">MAB</span><span class="sxs-lookup"><span data-stu-id="a35eb-127">MAB</span></span>
- <span data-ttu-id="a35eb-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="a35eb-128">AzureStorage</span></span>
- <span data-ttu-id="a35eb-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="a35eb-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-130">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="a35eb-130">-Container</span></span>

<span data-ttu-id="a35eb-131">Bu cmdlet 'in yedekleme öğelerini aldığı bir kapsayıcı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a35eb-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="a35eb-132">**Azurermrecoveryservicesbackupcontainer** almak için **Get-azrecoveryservicesbackupcontainer** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a35eb-132">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35eb-133">-DefaultProfile</span></span>

<span data-ttu-id="a35eb-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a35eb-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a35eb-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="a35eb-135">-DeleteState</span></span>
<span data-ttu-id="a35eb-136">Öğenin DeleteState değerini belirtir; Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a35eb-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a35eb-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="a35eb-137">ToBeDeleted</span></span>
- <span data-ttu-id="a35eb-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="a35eb-138">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a35eb-139">-FriendlyName</span></span>
<span data-ttu-id="a35eb-140">Yedeklenen öğenin FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a35eb-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="a35eb-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="a35eb-141">-Name</span></span>

<span data-ttu-id="a35eb-142">Yedekleme öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a35eb-142">Specifies the name of backup item.</span></span> <span data-ttu-id="a35eb-143">Dosya paylaşımı için, korumalı dosya paylaşımının benzersiz KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="a35eb-143">For file share, specify the unique ID of protected file share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-144">-İlke</span><span class="sxs-lookup"><span data-stu-id="a35eb-144">-Policy</span></span>

<span data-ttu-id="a35eb-145">Koruma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a35eb-145">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="a35eb-146">-ProtectionState</span></span>

<span data-ttu-id="a35eb-147">Korumanın durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a35eb-147">Specifies the state of protection.</span></span>
<span data-ttu-id="a35eb-148">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a35eb-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a35eb-149">Irtpending.</span><span class="sxs-lookup"><span data-stu-id="a35eb-149">IRPending.</span></span>
<span data-ttu-id="a35eb-150">İlk eşitleme başlatılmadı ve henüz kurtarma noktası yok.</span><span class="sxs-lookup"><span data-stu-id="a35eb-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="a35eb-151">Korunamaz.</span><span class="sxs-lookup"><span data-stu-id="a35eb-151">Protected.</span></span>
<span data-ttu-id="a35eb-152">Koruma devam etmektedir.</span><span class="sxs-lookup"><span data-stu-id="a35eb-152">Protection is ongoing.</span></span>
- <span data-ttu-id="a35eb-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="a35eb-153">ProtectionError.</span></span>
<span data-ttu-id="a35eb-154">Koruma hatası var.</span><span class="sxs-lookup"><span data-stu-id="a35eb-154">There is a protection error.</span></span>
- <span data-ttu-id="a35eb-155">Protectiondurdurdu.</span><span class="sxs-lookup"><span data-stu-id="a35eb-155">ProtectionStopped.</span></span>
<span data-ttu-id="a35eb-156">Koruma devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="a35eb-156">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="a35eb-157">-ProtectionStatus</span></span>

<span data-ttu-id="a35eb-158">Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a35eb-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="a35eb-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a35eb-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a35eb-160">Sağlık</span><span class="sxs-lookup"><span data-stu-id="a35eb-160">Healthy</span></span>
- <span data-ttu-id="a35eb-161">Sağlıklı</span><span class="sxs-lookup"><span data-stu-id="a35eb-161">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a35eb-162">-VaultId</span></span>

<span data-ttu-id="a35eb-163">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a35eb-163">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="a35eb-164">-WorkloadType</span></span>

<span data-ttu-id="a35eb-165">Kaynağın iş yükü türü.</span><span class="sxs-lookup"><span data-stu-id="a35eb-165">Workload type of the resource.</span></span> <span data-ttu-id="a35eb-166">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a35eb-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a35eb-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="a35eb-167">AzureVM</span></span>
- <span data-ttu-id="a35eb-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="a35eb-168">AzureFiles</span></span>
- <span data-ttu-id="a35eb-169">KLASÖRÜNÜN</span><span class="sxs-lookup"><span data-stu-id="a35eb-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35eb-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35eb-170">CommonParameters</span></span>
<span data-ttu-id="a35eb-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a35eb-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35eb-172">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a35eb-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35eb-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a35eb-173">INPUTS</span></span>

### <span data-ttu-id="a35eb-174">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="a35eb-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="a35eb-175">System. String</span><span class="sxs-lookup"><span data-stu-id="a35eb-175">System.String</span></span>

## <span data-ttu-id="a35eb-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a35eb-176">OUTPUTS</span></span>

### <span data-ttu-id="a35eb-177">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="a35eb-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="a35eb-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a35eb-178">NOTES</span></span>

## <span data-ttu-id="a35eb-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a35eb-179">RELATED LINKS</span></span>

[<span data-ttu-id="a35eb-180">Backup-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="a35eb-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a35eb-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="a35eb-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="a35eb-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a35eb-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="a35eb-183">Restore-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="a35eb-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
