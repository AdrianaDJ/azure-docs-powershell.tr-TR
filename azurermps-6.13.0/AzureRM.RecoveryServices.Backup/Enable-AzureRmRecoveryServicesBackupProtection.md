---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763818"
---
# <span data-ttu-id="f4e3a-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f4e3a-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="f4e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e3a-103">Belirtilen yedekleme koruma ilkesine sahip bir öğe için yedeklemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4e3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4e3a-104">SYNTAX</span></span>

### <span data-ttu-id="f4e3a-105">AzureVMComputeEnableProtection (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4e3a-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e3a-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="f4e3a-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e3a-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="f4e3a-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e3a-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="f4e3a-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e3a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4e3a-109">DESCRIPTION</span></span>
<span data-ttu-id="f4e3a-110">**Enable-AzureRmRecoveryServicesBackupProtection** cmdlet 'i bir öğedeki Azure yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="f4e3a-111">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f4e3a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4e3a-112">EXAMPLES</span></span>

### <span data-ttu-id="f4e3a-113">Örnek 1: bir öğe için yedekleme korumasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f4e3a-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="f4e3a-114">İlk cmdlet varsayılan ilke nesnesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="f4e3a-115">İkinci cmdlet $Pol ilkeyi kullanarak V2VM adındaki ARM sanal makinesi için yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="f4e3a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4e3a-116">PARAMETERS</span></span>

### <span data-ttu-id="f4e3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e3a-117">-DefaultProfile</span></span>
<span data-ttu-id="f4e3a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e3a-119">-Öğe</span><span class="sxs-lookup"><span data-stu-id="f4e3a-119">-Item</span></span>
<span data-ttu-id="f4e3a-120">Bu cmdlet 'in korumayı etkinleştirmesine yönelik yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="f4e3a-121">**Azurermrecoveryservicesbackupıtem** almak için Get-AzureRmRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="f4e3a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4e3a-122">-Name</span></span>
<span data-ttu-id="f4e3a-123">Yedekleme öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-123">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="f4e3a-124">-İlke</span><span class="sxs-lookup"><span data-stu-id="f4e3a-124">-Policy</span></span>
<span data-ttu-id="f4e3a-125">Bu cmdlet 'in bir öğeyle ilişkilenirse koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="f4e3a-126">**Azurermrecoveryservicesbackupprotectionpolicy** nesnesi almak için Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="f4e3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="f4e3a-128">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f4e3a-129">Bu parametreyi yalnızca ARM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-129">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="f4e3a-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="f4e3a-130">-ServiceName</span></span>
<span data-ttu-id="f4e3a-131">Hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-131">Specifies the service name.</span></span>
<span data-ttu-id="f4e3a-132">Bu parametreyi yalnızca ASM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-132">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="f4e3a-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f4e3a-133">-StorageAccountName</span></span>
<span data-ttu-id="f4e3a-134">Azure dosya paylaşımı depolama hesabı adı</span><span class="sxs-lookup"><span data-stu-id="f4e3a-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3a-135">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f4e3a-135">-VaultId</span></span>
<span data-ttu-id="f4e3a-136">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f4e3a-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4e3a-137">-Confirm</span></span>
<span data-ttu-id="f4e3a-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e3a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e3a-139">-WhatIf</span></span>
<span data-ttu-id="f4e3a-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4e3a-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e3a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e3a-142">CommonParameters</span></span>
<span data-ttu-id="f4e3a-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e3a-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e3a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e3a-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4e3a-145">INPUTS</span></span>

### <span data-ttu-id="f4e3a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e3a-146">System.String</span></span>
<span data-ttu-id="f4e3a-147">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4e3a-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="f4e3a-148">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="f4e3a-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="f4e3a-149">Parametreler: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4e3a-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="f4e3a-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4e3a-150">OUTPUTS</span></span>

### <span data-ttu-id="f4e3a-151">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="f4e3a-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f4e3a-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4e3a-152">NOTES</span></span>

## <span data-ttu-id="f4e3a-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4e3a-153">RELATED LINKS</span></span>

[<span data-ttu-id="f4e3a-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f4e3a-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="f4e3a-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f4e3a-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


