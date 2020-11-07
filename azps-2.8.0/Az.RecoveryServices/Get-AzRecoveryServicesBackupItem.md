---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933020"
---
# <span data-ttu-id="450c2-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="450c2-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="450c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="450c2-102">SYNOPSIS</span></span>

<span data-ttu-id="450c2-103">Yedeklemede öğeleri bir kapsayıcıdan alır.</span><span class="sxs-lookup"><span data-stu-id="450c2-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="450c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="450c2-104">SYNTAX</span></span>

### <span data-ttu-id="450c2-105">Getıtemsforcontainer (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="450c2-105">GetItemsForContainer (Default)</span></span>

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="450c2-106">Getıtemsforkasası</span><span class="sxs-lookup"><span data-stu-id="450c2-106">GetItemsForVault</span></span>

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="450c2-107">Getıtemsforpolicy</span><span class="sxs-lookup"><span data-stu-id="450c2-107">GetItemsForPolicy</span></span>

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="450c2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="450c2-108">DESCRIPTION</span></span>

<span data-ttu-id="450c2-109">**Get-Azrecoveryservicesbackupıtem** cmdlet 'i bir kapsayıcıdaki öğeleri veya Azure Backup 'daki bir değeri ve öğelerin koruma durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="450c2-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="450c2-110">Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.</span><span class="sxs-lookup"><span data-stu-id="450c2-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="450c2-111">Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir yedekleme öğesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="450c2-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="450c2-112">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="450c2-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="450c2-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="450c2-113">EXAMPLES</span></span>

### <span data-ttu-id="450c2-114">Örnek 1: yedekleme kapsayıcısından öğe alma</span><span class="sxs-lookup"><span data-stu-id="450c2-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="450c2-115">İlk komut AzureVM türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="450c2-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="450c2-116">İkinci komut $Container V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="450c2-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="450c2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="450c2-117">PARAMETERS</span></span>

### <span data-ttu-id="450c2-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="450c2-118">-BackupManagementType</span></span>

<span data-ttu-id="450c2-119">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="450c2-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="450c2-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="450c2-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="450c2-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="450c2-121">AzureVM</span></span>
- <span data-ttu-id="450c2-122">MARS</span><span class="sxs-lookup"><span data-stu-id="450c2-122">MARS</span></span>
- <span data-ttu-id="450c2-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="450c2-123">SCDPM</span></span>
- <span data-ttu-id="450c2-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="450c2-124">AzureBackupServer</span></span>
- <span data-ttu-id="450c2-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="450c2-125">AzureSQL</span></span>
- <span data-ttu-id="450c2-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="450c2-126">AzureStorage</span></span>
- <span data-ttu-id="450c2-127">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="450c2-127">AzureWorkload</span></span>

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

### <span data-ttu-id="450c2-128">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="450c2-128">-Container</span></span>

<span data-ttu-id="450c2-129">Bu cmdlet 'in yedekleme öğelerini aldığı bir kapsayıcı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="450c2-129">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="450c2-130">**Azurermrecoveryservicesbackupcontainer** almak için **Get-azrecoveryservicesbackupcontainer** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="450c2-130">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="450c2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450c2-131">-DefaultProfile</span></span>

<span data-ttu-id="450c2-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="450c2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="450c2-133">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="450c2-133">-DeleteState</span></span>
<span data-ttu-id="450c2-134">Öğenin DeleteState değerini belirtir; Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="450c2-134">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="450c2-135">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="450c2-135">ToBeDeleted</span></span>
- <span data-ttu-id="450c2-136">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="450c2-136">NotDeleted</span></span>

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

### <span data-ttu-id="450c2-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="450c2-137">-Name</span></span>

<span data-ttu-id="450c2-138">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="450c2-138">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="450c2-139">-İlke</span><span class="sxs-lookup"><span data-stu-id="450c2-139">-Policy</span></span>

<span data-ttu-id="450c2-140">Koruma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="450c2-140">Protection policy object.</span></span>

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

### <span data-ttu-id="450c2-141">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="450c2-141">-ProtectionState</span></span>

<span data-ttu-id="450c2-142">Korumanın durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="450c2-142">Specifies the state of protection.</span></span>
<span data-ttu-id="450c2-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="450c2-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="450c2-144">Irtpending.</span><span class="sxs-lookup"><span data-stu-id="450c2-144">IRPending.</span></span>
<span data-ttu-id="450c2-145">İlk eşitleme başlatılmadı ve henüz kurtarma noktası yok.</span><span class="sxs-lookup"><span data-stu-id="450c2-145">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="450c2-146">Korunamaz.</span><span class="sxs-lookup"><span data-stu-id="450c2-146">Protected.</span></span>
<span data-ttu-id="450c2-147">Koruma devam etmektedir.</span><span class="sxs-lookup"><span data-stu-id="450c2-147">Protection is ongoing.</span></span>
- <span data-ttu-id="450c2-148">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="450c2-148">ProtectionError.</span></span>
<span data-ttu-id="450c2-149">Koruma hatası var.</span><span class="sxs-lookup"><span data-stu-id="450c2-149">There is a protection error.</span></span>
- <span data-ttu-id="450c2-150">Protectiondurdurdu.</span><span class="sxs-lookup"><span data-stu-id="450c2-150">ProtectionStopped.</span></span>
<span data-ttu-id="450c2-151">Koruma devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="450c2-151">Protection is disabled.</span></span>

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

### <span data-ttu-id="450c2-152">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="450c2-152">-ProtectionStatus</span></span>

<span data-ttu-id="450c2-153">Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="450c2-153">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="450c2-154">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="450c2-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="450c2-155">Sağlık</span><span class="sxs-lookup"><span data-stu-id="450c2-155">Healthy</span></span>
- <span data-ttu-id="450c2-156">Sağlıklı</span><span class="sxs-lookup"><span data-stu-id="450c2-156">Unhealthy</span></span>

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

### <span data-ttu-id="450c2-157">-VaultId</span><span class="sxs-lookup"><span data-stu-id="450c2-157">-VaultId</span></span>

<span data-ttu-id="450c2-158">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="450c2-158">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="450c2-159">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="450c2-159">-WorkloadType</span></span>

<span data-ttu-id="450c2-160">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="450c2-160">Specifies the workload type.</span></span>
<span data-ttu-id="450c2-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="450c2-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="450c2-162">AzureVM</span><span class="sxs-lookup"><span data-stu-id="450c2-162">AzureVM</span></span>
- <span data-ttu-id="450c2-163">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="450c2-163">AzureSQLDatabase</span></span>
- <span data-ttu-id="450c2-164">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="450c2-164">AzureFiles</span></span>
- <span data-ttu-id="450c2-165">KLASÖRÜNÜN</span><span class="sxs-lookup"><span data-stu-id="450c2-165">MSSQL</span></span>

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

### <span data-ttu-id="450c2-166">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450c2-166">-CommonParameters</span></span>

<span data-ttu-id="450c2-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="450c2-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450c2-168">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="450c2-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450c2-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="450c2-169">INPUTS</span></span>

### <span data-ttu-id="450c2-170">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="450c2-170">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="450c2-171">System. String</span><span class="sxs-lookup"><span data-stu-id="450c2-171">System.String</span></span>

## <span data-ttu-id="450c2-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="450c2-172">OUTPUTS</span></span>

### <span data-ttu-id="450c2-173">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="450c2-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="450c2-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="450c2-174">NOTES</span></span>

## <span data-ttu-id="450c2-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="450c2-175">RELATED LINKS</span></span>

[<span data-ttu-id="450c2-176">Backup-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="450c2-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="450c2-177">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="450c2-177">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="450c2-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="450c2-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="450c2-179">Restore-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="450c2-179">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
