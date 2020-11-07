---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a1037f742fab47ae84edae6e1558e313e563c25a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763816"
---
# <span data-ttu-id="79440-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="79440-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="79440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79440-102">SYNOPSIS</span></span>
<span data-ttu-id="79440-103">Yedeklemede öğeleri bir kapsayıcıdan alır.</span><span class="sxs-lookup"><span data-stu-id="79440-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79440-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79440-104">SYNTAX</span></span>

### <span data-ttu-id="79440-105">Getıtemsforcontainer (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79440-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79440-106">Getıtemsforkasası</span><span class="sxs-lookup"><span data-stu-id="79440-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79440-107">Getıtemsforpolicy</span><span class="sxs-lookup"><span data-stu-id="79440-107">GetItemsForPolicy</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79440-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="79440-108">DESCRIPTION</span></span>
<span data-ttu-id="79440-109">**Get-Azurermrecoveryservicesbackupıtem** cmdlet 'i bir kapsayıcıdaki öğeleri veya Azure Backup 'daki bir değeri ve öğelerin koruma durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="79440-109">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="79440-110">Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.</span><span class="sxs-lookup"><span data-stu-id="79440-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="79440-111">Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir yedekleme öğesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="79440-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="79440-112">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="79440-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="79440-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79440-113">EXAMPLES</span></span>

### <span data-ttu-id="79440-114">Örnek 1: yedekleme kapsayıcısından öğe alma</span><span class="sxs-lookup"><span data-stu-id="79440-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="79440-115">İlk komut AzureVM türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="79440-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="79440-116">İkinci komut $Container V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="79440-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="79440-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79440-117">PARAMETERS</span></span>

### <span data-ttu-id="79440-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="79440-118">-BackupManagementType</span></span>
<span data-ttu-id="79440-119">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="79440-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="79440-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79440-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79440-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="79440-121">AzureVM</span></span> 
- <span data-ttu-id="79440-122">MARS</span><span class="sxs-lookup"><span data-stu-id="79440-122">MARS</span></span> 
- <span data-ttu-id="79440-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="79440-123">SCDPM</span></span> 
- <span data-ttu-id="79440-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="79440-124">AzureBackupServer</span></span> 
- <span data-ttu-id="79440-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="79440-125">AzureSQL</span></span>
- <span data-ttu-id="79440-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="79440-126">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79440-127">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="79440-127">-Container</span></span>
<span data-ttu-id="79440-128">Bu cmdlet 'in yedekleme öğelerini aldığı bir kapsayıcı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="79440-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="79440-129">**Azurermrecoveryservicesbackupcontainer** almak için Get-AzureRmRecoveryServicesBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="79440-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="79440-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79440-130">-DefaultProfile</span></span>
<span data-ttu-id="79440-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79440-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79440-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="79440-132">-Name</span></span>
<span data-ttu-id="79440-133">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79440-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="79440-134">-İlke</span><span class="sxs-lookup"><span data-stu-id="79440-134">-Policy</span></span>
<span data-ttu-id="79440-135">Koruma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="79440-135">Protection policy object.</span></span>

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

### <span data-ttu-id="79440-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="79440-136">-ProtectionState</span></span>
<span data-ttu-id="79440-137">Korumanın durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79440-137">Specifies the state of protection.</span></span>
<span data-ttu-id="79440-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79440-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79440-139">Irtpending.</span><span class="sxs-lookup"><span data-stu-id="79440-139">IRPending.</span></span>
<span data-ttu-id="79440-140">İlk eşitleme başlatılmadı ve henüz kurtarma noktası yok.</span><span class="sxs-lookup"><span data-stu-id="79440-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="79440-141">Korunamaz.</span><span class="sxs-lookup"><span data-stu-id="79440-141">Protected.</span></span>
<span data-ttu-id="79440-142">Koruma devam etmektedir.</span><span class="sxs-lookup"><span data-stu-id="79440-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="79440-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="79440-143">ProtectionError.</span></span>
<span data-ttu-id="79440-144">Koruma hatası var.</span><span class="sxs-lookup"><span data-stu-id="79440-144">There is a protection error.</span></span>
- <span data-ttu-id="79440-145">Protectiondurdurdu.</span><span class="sxs-lookup"><span data-stu-id="79440-145">ProtectionStopped.</span></span>
<span data-ttu-id="79440-146">Koruma devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="79440-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="79440-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="79440-147">-ProtectionStatus</span></span>
<span data-ttu-id="79440-148">Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79440-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="79440-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79440-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79440-150">Sağlık</span><span class="sxs-lookup"><span data-stu-id="79440-150">Healthy</span></span>
- <span data-ttu-id="79440-151">Sağlıklı</span><span class="sxs-lookup"><span data-stu-id="79440-151">Unhealthy</span></span>

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

### <span data-ttu-id="79440-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="79440-152">-VaultId</span></span>
<span data-ttu-id="79440-153">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="79440-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="79440-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="79440-154">-WorkloadType</span></span>
<span data-ttu-id="79440-155">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="79440-155">Specifies the workload type.</span></span> <span data-ttu-id="79440-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79440-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79440-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="79440-157">AzureVM</span></span> 
- <span data-ttu-id="79440-158">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="79440-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="79440-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="79440-159">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79440-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79440-160">CommonParameters</span></span>
<span data-ttu-id="79440-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79440-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79440-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79440-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79440-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79440-163">INPUTS</span></span>

### <span data-ttu-id="79440-164">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="79440-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="79440-165">System. String</span><span class="sxs-lookup"><span data-stu-id="79440-165">System.String</span></span>
<span data-ttu-id="79440-166">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79440-166">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="79440-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79440-167">OUTPUTS</span></span>

### <span data-ttu-id="79440-168">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="79440-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="79440-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79440-169">NOTES</span></span>

## <span data-ttu-id="79440-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79440-170">RELATED LINKS</span></span>

[<span data-ttu-id="79440-171">Backup-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="79440-171">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="79440-172">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="79440-172">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="79440-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="79440-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="79440-174">Restore-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="79440-174">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


