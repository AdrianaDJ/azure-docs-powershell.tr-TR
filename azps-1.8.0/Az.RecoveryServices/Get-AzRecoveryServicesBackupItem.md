---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: c861bbe3b422360f58f36cbe859343f7dcc7ed37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759713"
---
# <span data-ttu-id="19992-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="19992-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="19992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19992-102">SYNOPSIS</span></span>
<span data-ttu-id="19992-103">Yedeklemede öğeleri bir kapsayıcıdan alır.</span><span class="sxs-lookup"><span data-stu-id="19992-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="19992-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19992-104">SYNTAX</span></span>

### <span data-ttu-id="19992-105">Getıtemsforcontainer (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19992-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19992-106">Getıtemsforkasası</span><span class="sxs-lookup"><span data-stu-id="19992-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19992-107">Getıtemsforpolicy</span><span class="sxs-lookup"><span data-stu-id="19992-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19992-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="19992-108">DESCRIPTION</span></span>
<span data-ttu-id="19992-109">**Get-Azrecoveryservicesbackupıtem** cmdlet 'i bir kapsayıcıdaki öğeleri veya Azure Backup 'daki bir değeri ve öğelerin koruma durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="19992-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="19992-110">Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.</span><span class="sxs-lookup"><span data-stu-id="19992-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="19992-111">Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir yedekleme öğesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="19992-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="19992-112">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="19992-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="19992-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19992-113">EXAMPLES</span></span>

### <span data-ttu-id="19992-114">Örnek 1: yedekleme kapsayıcısından öğe alma</span><span class="sxs-lookup"><span data-stu-id="19992-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="19992-115">İlk komut AzureVM türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="19992-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="19992-116">İkinci komut $Container V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="19992-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="19992-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19992-117">PARAMETERS</span></span>

### <span data-ttu-id="19992-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="19992-118">-BackupManagementType</span></span>
<span data-ttu-id="19992-119">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19992-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="19992-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19992-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19992-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="19992-121">AzureVM</span></span> 
- <span data-ttu-id="19992-122">MARS</span><span class="sxs-lookup"><span data-stu-id="19992-122">MARS</span></span> 
- <span data-ttu-id="19992-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="19992-123">SCDPM</span></span> 
- <span data-ttu-id="19992-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="19992-124">AzureBackupServer</span></span> 
- <span data-ttu-id="19992-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="19992-125">AzureSQL</span></span>
- <span data-ttu-id="19992-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="19992-126">AzureStorage</span></span>

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

### <span data-ttu-id="19992-127">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="19992-127">-Container</span></span>
<span data-ttu-id="19992-128">Bu cmdlet 'in yedekleme öğelerini aldığı bir kapsayıcı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="19992-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="19992-129">**Azurermrecoveryservicesbackupcontainer** almak için Get-AzRecoveryServicesBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="19992-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="19992-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19992-130">-DefaultProfile</span></span>
<span data-ttu-id="19992-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19992-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19992-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="19992-132">-Name</span></span>
<span data-ttu-id="19992-133">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19992-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="19992-134">-İlke</span><span class="sxs-lookup"><span data-stu-id="19992-134">-Policy</span></span>
<span data-ttu-id="19992-135">Koruma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="19992-135">Protection policy object.</span></span>

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

### <span data-ttu-id="19992-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="19992-136">-ProtectionState</span></span>
<span data-ttu-id="19992-137">Korumanın durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="19992-137">Specifies the state of protection.</span></span>
<span data-ttu-id="19992-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19992-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19992-139">Irtpending.</span><span class="sxs-lookup"><span data-stu-id="19992-139">IRPending.</span></span>
<span data-ttu-id="19992-140">İlk eşitleme başlatılmadı ve henüz kurtarma noktası yok.</span><span class="sxs-lookup"><span data-stu-id="19992-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="19992-141">Korunamaz.</span><span class="sxs-lookup"><span data-stu-id="19992-141">Protected.</span></span>
<span data-ttu-id="19992-142">Koruma devam etmektedir.</span><span class="sxs-lookup"><span data-stu-id="19992-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="19992-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="19992-143">ProtectionError.</span></span>
<span data-ttu-id="19992-144">Koruma hatası var.</span><span class="sxs-lookup"><span data-stu-id="19992-144">There is a protection error.</span></span>
- <span data-ttu-id="19992-145">Protectiondurdurdu.</span><span class="sxs-lookup"><span data-stu-id="19992-145">ProtectionStopped.</span></span>
<span data-ttu-id="19992-146">Koruma devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="19992-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="19992-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="19992-147">-ProtectionStatus</span></span>
<span data-ttu-id="19992-148">Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="19992-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="19992-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19992-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19992-150">Sağlık</span><span class="sxs-lookup"><span data-stu-id="19992-150">Healthy</span></span>
- <span data-ttu-id="19992-151">Sağlıklı</span><span class="sxs-lookup"><span data-stu-id="19992-151">Unhealthy</span></span>

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

### <span data-ttu-id="19992-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="19992-152">-VaultId</span></span>
<span data-ttu-id="19992-153">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="19992-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="19992-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="19992-154">-WorkloadType</span></span>
<span data-ttu-id="19992-155">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19992-155">Specifies the workload type.</span></span> <span data-ttu-id="19992-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19992-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19992-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="19992-157">AzureVM</span></span> 
- <span data-ttu-id="19992-158">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="19992-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="19992-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="19992-159">AzureFiles</span></span>

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

### <span data-ttu-id="19992-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19992-160">CommonParameters</span></span>
<span data-ttu-id="19992-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19992-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19992-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19992-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19992-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19992-163">INPUTS</span></span>

### <span data-ttu-id="19992-164">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="19992-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="19992-165">System. String</span><span class="sxs-lookup"><span data-stu-id="19992-165">System.String</span></span>

## <span data-ttu-id="19992-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19992-166">OUTPUTS</span></span>

### <span data-ttu-id="19992-167">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="19992-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="19992-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19992-168">NOTES</span></span>

## <span data-ttu-id="19992-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19992-169">RELATED LINKS</span></span>

[<span data-ttu-id="19992-170">Backup-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="19992-170">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="19992-171">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="19992-171">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="19992-172">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="19992-172">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="19992-173">Restore-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="19992-173">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


