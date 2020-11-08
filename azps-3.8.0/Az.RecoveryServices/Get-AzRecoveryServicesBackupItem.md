---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096368"
---
# <span data-ttu-id="7bf5c-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7bf5c-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="7bf5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bf5c-102">SYNOPSIS</span></span>

<span data-ttu-id="7bf5c-103">Yedeklemede öğeleri bir kapsayıcıdan alır.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="7bf5c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bf5c-104">SYNTAX</span></span>

### <span data-ttu-id="7bf5c-105">Getıtemsforcontainer (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7bf5c-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bf5c-106">Getıtemsforkasası</span><span class="sxs-lookup"><span data-stu-id="7bf5c-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bf5c-107">Getıtemsforpolicy</span><span class="sxs-lookup"><span data-stu-id="7bf5c-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bf5c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bf5c-108">DESCRIPTION</span></span>

<span data-ttu-id="7bf5c-109">**Get-Azrecoveryservicesbackupıtem** cmdlet 'i bir kapsayıcıdaki öğeleri veya Azure Backup 'daki bir değeri ve öğelerin koruma durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="7bf5c-110">Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="7bf5c-111">Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir yedekleme öğesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="7bf5c-112">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="7bf5c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bf5c-113">EXAMPLES</span></span>

### <span data-ttu-id="7bf5c-114">Örnek 1: yedekleme kapsayıcısından öğe alma</span><span class="sxs-lookup"><span data-stu-id="7bf5c-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="7bf5c-115">İlk komut AzureVM türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7bf5c-116">İkinci komut $Container V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="7bf5c-117">Örnek 2: FriendlyName 'dan bir Azure dosya paylaşımı öğesi alma</span><span class="sxs-lookup"><span data-stu-id="7bf5c-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="7bf5c-118">İlk komut AzureStorage türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7bf5c-119">İkinci komut, friendlyName FriendlyName parametresinde geçirilen değeri eşleştiren yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="7bf5c-120">FriendlyName parametresi kullanmak birden fazla Azure dosya paylaşımı döndürmeye neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="7bf5c-121">Böyle durumlarda, $BackupItem değişkeninde döndürülen Name özelliği olarak parametre değerini içeren-name parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="7bf5c-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bf5c-122">PARAMETERS</span></span>

### <span data-ttu-id="7bf5c-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7bf5c-123">-BackupManagementType</span></span>

<span data-ttu-id="7bf5c-124">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="7bf5c-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7bf5c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7bf5c-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7bf5c-126">AzureVM</span></span>
- <span data-ttu-id="7bf5c-127">MARS</span><span class="sxs-lookup"><span data-stu-id="7bf5c-127">MARS</span></span>
- <span data-ttu-id="7bf5c-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="7bf5c-128">SCDPM</span></span>
- <span data-ttu-id="7bf5c-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="7bf5c-129">AzureBackupServer</span></span>
- <span data-ttu-id="7bf5c-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="7bf5c-130">AzureSQL</span></span>
- <span data-ttu-id="7bf5c-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="7bf5c-131">AzureStorage</span></span>
- <span data-ttu-id="7bf5c-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="7bf5c-132">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf5c-133">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="7bf5c-133">-Container</span></span>

<span data-ttu-id="7bf5c-134">Bu cmdlet 'in yedekleme öğelerini aldığı bir kapsayıcı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="7bf5c-135">**Azurermrecoveryservicesbackupcontainer** almak için **Get-azrecoveryservicesbackupcontainer** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="7bf5c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf5c-136">-DefaultProfile</span></span>

<span data-ttu-id="7bf5c-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bf5c-138">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="7bf5c-138">-DeleteState</span></span>
<span data-ttu-id="7bf5c-139">Öğenin DeleteState değerini belirtir; Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7bf5c-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7bf5c-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="7bf5c-140">ToBeDeleted</span></span>
- <span data-ttu-id="7bf5c-141">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="7bf5c-141">NotDeleted</span></span>

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

### <span data-ttu-id="7bf5c-142">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7bf5c-142">-FriendlyName</span></span>
<span data-ttu-id="7bf5c-143">Yedeklenen öğenin FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7bf5c-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="7bf5c-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="7bf5c-144">-Name</span></span>

<span data-ttu-id="7bf5c-145">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="7bf5c-146">-İlke</span><span class="sxs-lookup"><span data-stu-id="7bf5c-146">-Policy</span></span>

<span data-ttu-id="7bf5c-147">Koruma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-147">Protection policy object.</span></span>

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

### <span data-ttu-id="7bf5c-148">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="7bf5c-148">-ProtectionState</span></span>

<span data-ttu-id="7bf5c-149">Korumanın durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-149">Specifies the state of protection.</span></span>
<span data-ttu-id="7bf5c-150">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7bf5c-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7bf5c-151">Irtpending.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-151">IRPending.</span></span>
<span data-ttu-id="7bf5c-152">İlk eşitleme başlatılmadı ve henüz kurtarma noktası yok.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="7bf5c-153">Korunamaz.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-153">Protected.</span></span>
<span data-ttu-id="7bf5c-154">Koruma devam etmektedir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-154">Protection is ongoing.</span></span>
- <span data-ttu-id="7bf5c-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-155">ProtectionError.</span></span>
<span data-ttu-id="7bf5c-156">Koruma hatası var.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-156">There is a protection error.</span></span>
- <span data-ttu-id="7bf5c-157">Protectiondurdurdu.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-157">ProtectionStopped.</span></span>
<span data-ttu-id="7bf5c-158">Koruma devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="7bf5c-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="7bf5c-159">-ProtectionStatus</span></span>

<span data-ttu-id="7bf5c-160">Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="7bf5c-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7bf5c-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7bf5c-162">Sağlık</span><span class="sxs-lookup"><span data-stu-id="7bf5c-162">Healthy</span></span>
- <span data-ttu-id="7bf5c-163">Sağlıklı</span><span class="sxs-lookup"><span data-stu-id="7bf5c-163">Unhealthy</span></span>

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

### <span data-ttu-id="7bf5c-164">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7bf5c-164">-VaultId</span></span>

<span data-ttu-id="7bf5c-165">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7bf5c-166">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7bf5c-166">-WorkloadType</span></span>

<span data-ttu-id="7bf5c-167">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-167">Specifies the workload type.</span></span>
<span data-ttu-id="7bf5c-168">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7bf5c-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7bf5c-169">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7bf5c-169">AzureVM</span></span>
- <span data-ttu-id="7bf5c-170">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="7bf5c-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="7bf5c-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="7bf5c-171">AzureFiles</span></span>
- <span data-ttu-id="7bf5c-172">KLASÖRÜNÜN</span><span class="sxs-lookup"><span data-stu-id="7bf5c-172">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf5c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf5c-173">CommonParameters</span></span>
<span data-ttu-id="7bf5c-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf5c-175">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7bf5c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf5c-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bf5c-176">INPUTS</span></span>

### <span data-ttu-id="7bf5c-177">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="7bf5c-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="7bf5c-178">System. String</span><span class="sxs-lookup"><span data-stu-id="7bf5c-178">System.String</span></span>

## <span data-ttu-id="7bf5c-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bf5c-179">OUTPUTS</span></span>

### <span data-ttu-id="7bf5c-180">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="7bf5c-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="7bf5c-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bf5c-181">NOTES</span></span>

## <span data-ttu-id="7bf5c-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bf5c-182">RELATED LINKS</span></span>

[<span data-ttu-id="7bf5c-183">Backup-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="7bf5c-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="7bf5c-184">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7bf5c-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="7bf5c-185">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7bf5c-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="7bf5c-186">Restore-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="7bf5c-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
