---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759750"
---
# <span data-ttu-id="0d408-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0d408-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="0d408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d408-102">SYNOPSIS</span></span>
<span data-ttu-id="0d408-103">Belirtilen yedekleme koruma ilkesine sahip bir öğe için yedeklemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="0d408-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="0d408-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d408-104">SYNTAX</span></span>

### <span data-ttu-id="0d408-105">AzureVMComputeEnableProtection (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d408-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d408-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="0d408-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d408-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="0d408-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d408-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="0d408-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d408-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="0d408-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d408-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d408-110">DESCRIPTION</span></span>
<span data-ttu-id="0d408-111">**Enable-AzRecoveryServicesBackupProtection** cmdlet 'i bir öğede Azure yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0d408-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="0d408-112">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0d408-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0d408-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d408-113">EXAMPLES</span></span>

### <span data-ttu-id="0d408-114">Örnek 1: bir öğe için yedekleme korumasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0d408-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="0d408-115">İlk cmdlet varsayılan ilke nesnesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0d408-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="0d408-116">İkinci cmdlet $Pol ilkeyi kullanarak V2VM adındaki ARM sanal makinesi için yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0d408-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="0d408-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d408-117">PARAMETERS</span></span>

### <span data-ttu-id="0d408-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d408-118">-DefaultProfile</span></span>
<span data-ttu-id="0d408-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d408-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d408-120">-Öğe</span><span class="sxs-lookup"><span data-stu-id="0d408-120">-Item</span></span>
<span data-ttu-id="0d408-121">Bu cmdlet 'in korumayı etkinleştirmesine yönelik yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d408-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="0d408-122">**Azurermrecoveryservicesbackupıtem** almak için Get-AzRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0d408-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d408-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d408-123">-Name</span></span>
<span data-ttu-id="0d408-124">Yedekleme öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d408-124">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d408-125">-İlke</span><span class="sxs-lookup"><span data-stu-id="0d408-125">-Policy</span></span>
<span data-ttu-id="0d408-126">Bu cmdlet 'in bir öğeyle ilişkilenirse koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d408-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="0d408-127">**Azurermrecoveryservicesbackupprotectionpolicy** nesnesi almak için Get-AzRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0d408-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d408-128">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="0d408-128">-ProtectableItem</span></span>
<span data-ttu-id="0d408-129">İş durumu için filtre değeri.</span><span class="sxs-lookup"><span data-stu-id="0d408-129">Filter value for status of job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d408-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d408-130">-ResourceGroupName</span></span>
<span data-ttu-id="0d408-131">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d408-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="0d408-132">Bu parametreyi yalnızca ARM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="0d408-132">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d408-133">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="0d408-133">-ServiceName</span></span>
<span data-ttu-id="0d408-134">Hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d408-134">Specifies the service name.</span></span>
<span data-ttu-id="0d408-135">Bu parametreyi yalnızca ASM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="0d408-135">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d408-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0d408-136">-StorageAccountName</span></span>
<span data-ttu-id="0d408-137">Azure dosya paylaşımı depolama hesabı adı</span><span class="sxs-lookup"><span data-stu-id="0d408-137">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d408-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0d408-138">-VaultId</span></span>
<span data-ttu-id="0d408-139">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0d408-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0d408-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d408-140">-Confirm</span></span>
<span data-ttu-id="0d408-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d408-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d408-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d408-142">-WhatIf</span></span>
<span data-ttu-id="0d408-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d408-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d408-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d408-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d408-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d408-145">CommonParameters</span></span>
<span data-ttu-id="0d408-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d408-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d408-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d408-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d408-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d408-148">INPUTS</span></span>

### <span data-ttu-id="0d408-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0d408-149">System.String</span></span>

### <span data-ttu-id="0d408-150">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="0d408-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="0d408-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d408-151">OUTPUTS</span></span>

### <span data-ttu-id="0d408-152">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="0d408-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0d408-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d408-153">NOTES</span></span>

## <span data-ttu-id="0d408-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d408-154">RELATED LINKS</span></span>

[<span data-ttu-id="0d408-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0d408-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="0d408-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0d408-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

