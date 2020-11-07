---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764534"
---
# <span data-ttu-id="ef1d1-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ef1d1-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="ef1d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1d1-103">Yedeklemede öğeleri bir kapsayıcıdan alır.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef1d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef1d1-104">SYNTAX</span></span>

### <span data-ttu-id="ef1d1-105">Getıtemsforcontainer (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef1d1-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef1d1-106">Getıtemsforkasası</span><span class="sxs-lookup"><span data-stu-id="ef1d1-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef1d1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef1d1-107">DESCRIPTION</span></span>
<span data-ttu-id="ef1d1-108">**Get-Azurermrecoveryservicesbackupıtem** cmdlet 'i bir kapsayıcıdaki öğeleri veya Azure Backup 'daki bir değeri ve öğelerin koruma durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="ef1d1-109">Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="ef1d1-110">Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir yedekleme öğesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="ef1d1-111">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ef1d1-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef1d1-112">EXAMPLES</span></span>

### <span data-ttu-id="ef1d1-113">Örnek 1: yedekleme kapsayıcısından öğe alma</span><span class="sxs-lookup"><span data-stu-id="ef1d1-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="ef1d1-114">İlk komut AzureVM türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="ef1d1-115">İkinci komut $Container V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="ef1d1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef1d1-116">PARAMETERS</span></span>

### <span data-ttu-id="ef1d1-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ef1d1-117">-BackupManagementType</span></span>
<span data-ttu-id="ef1d1-118">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="ef1d1-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ef1d1-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef1d1-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ef1d1-120">AzureVM</span></span> 
- <span data-ttu-id="ef1d1-121">MARS</span><span class="sxs-lookup"><span data-stu-id="ef1d1-121">MARS</span></span> 
- <span data-ttu-id="ef1d1-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="ef1d1-122">SCDPM</span></span> 
- <span data-ttu-id="ef1d1-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="ef1d1-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef1d1-124">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ef1d1-124">-Container</span></span>
<span data-ttu-id="ef1d1-125">Bu cmdlet 'in yedekleme öğelerini aldığı bir kapsayıcı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="ef1d1-126">**Azurermrecoveryservicesbackupcontainer** almak için Get-AzureRmRecoveryServicesBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="ef1d1-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef1d1-127">-Name</span></span>
<span data-ttu-id="ef1d1-128">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-128">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="ef1d1-129">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="ef1d1-129">-ProtectionState</span></span>
<span data-ttu-id="ef1d1-130">Korumanın durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-130">Specifies the state of protection.</span></span>
<span data-ttu-id="ef1d1-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ef1d1-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef1d1-132">Irtpending.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-132">IRPending.</span></span>
<span data-ttu-id="ef1d1-133">İlk eşitleme başlatılmadı ve henüz kurtarma noktası yok.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="ef1d1-134">Korunamaz.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-134">Protected.</span></span>
<span data-ttu-id="ef1d1-135">Koruma devam etmektedir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="ef1d1-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-136">ProtectionError.</span></span>
<span data-ttu-id="ef1d1-137">Koruma hatası var.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-137">There is a protection error.</span></span>
- <span data-ttu-id="ef1d1-138">Protectiondurdurdu.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-138">ProtectionStopped.</span></span>
<span data-ttu-id="ef1d1-139">Koruma devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-139">Protection is disabled.</span></span>

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

### <span data-ttu-id="ef1d1-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="ef1d1-140">-ProtectionStatus</span></span>
<span data-ttu-id="ef1d1-141">Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="ef1d1-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ef1d1-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef1d1-143">Sağlık</span><span class="sxs-lookup"><span data-stu-id="ef1d1-143">Healthy</span></span>
- <span data-ttu-id="ef1d1-144">Sağlıklı</span><span class="sxs-lookup"><span data-stu-id="ef1d1-144">Unhealthy</span></span>

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

### <span data-ttu-id="ef1d1-145">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ef1d1-145">-WorkloadType</span></span>
<span data-ttu-id="ef1d1-146">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-146">Specifies the workload type.</span></span> <span data-ttu-id="ef1d1-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ef1d1-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef1d1-148">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ef1d1-148">AzureVM</span></span> 
- <span data-ttu-id="ef1d1-149">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="ef1d1-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef1d1-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1d1-150">-DefaultProfile</span></span>
<span data-ttu-id="ef1d1-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef1d1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1d1-152">CommonParameters</span></span>
<span data-ttu-id="ef1d1-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef1d1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1d1-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1d1-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1d1-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef1d1-155">INPUTS</span></span>

## <span data-ttu-id="ef1d1-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef1d1-156">OUTPUTS</span></span>

### <span data-ttu-id="ef1d1-157">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="ef1d1-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="ef1d1-158">System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="ef1d1-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="ef1d1-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef1d1-159">NOTES</span></span>

## <span data-ttu-id="ef1d1-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef1d1-160">RELATED LINKS</span></span>

[<span data-ttu-id="ef1d1-161">Backup-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ef1d1-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="ef1d1-162">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ef1d1-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="ef1d1-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ef1d1-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="ef1d1-164">Restore-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ef1d1-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


