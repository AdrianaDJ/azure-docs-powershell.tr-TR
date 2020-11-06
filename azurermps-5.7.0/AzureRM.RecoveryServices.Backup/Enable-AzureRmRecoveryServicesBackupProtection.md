---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: efe4392fd57c5cb0beb6731fefb83878001b489b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587507"
---
# <span data-ttu-id="79665-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="79665-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="79665-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79665-102">SYNOPSIS</span></span>
<span data-ttu-id="79665-103">Belirtilen yedekleme koruma ilkesine sahip bir öğe için yedeklemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="79665-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79665-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79665-104">SYNTAX</span></span>

### <span data-ttu-id="79665-105">AzureVMComputeEnableProtection (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79665-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79665-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="79665-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79665-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="79665-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79665-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="79665-108">DESCRIPTION</span></span>
<span data-ttu-id="79665-109">**Enable-AzureRmRecoveryServicesBackupProtection** cmdlet 'i bir öğedeki Azure yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="79665-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="79665-110">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="79665-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="79665-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79665-111">EXAMPLES</span></span>

### <span data-ttu-id="79665-112">Örnek 1: bir öğe için yedekleme korumasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="79665-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="79665-113">İlk cmdlet varsayılan ilke nesnesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="79665-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="79665-114">İkinci cmdlet $Pol ilkeyi kullanarak V2VM adındaki ARM sanal makinesi için yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="79665-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="79665-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79665-115">PARAMETERS</span></span>

### <span data-ttu-id="79665-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79665-116">-DefaultProfile</span></span>
<span data-ttu-id="79665-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79665-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79665-118">-Öğe</span><span class="sxs-lookup"><span data-stu-id="79665-118">-Item</span></span>
<span data-ttu-id="79665-119">Bu cmdlet 'in korumayı etkinleştirmesine yönelik yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79665-119">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="79665-120">**Azurermrecoveryservicesbackupıtem** almak için Get-AzureRmRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="79665-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79665-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="79665-121">-Name</span></span>
<span data-ttu-id="79665-122">Yedekleme öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79665-122">Specifies the name of the Backup item.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79665-123">-İlke</span><span class="sxs-lookup"><span data-stu-id="79665-123">-Policy</span></span>
<span data-ttu-id="79665-124">Bu cmdlet 'in bir öğeyle ilişkilenirse koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79665-124">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="79665-125">**Azurermrecoveryservicesbackupprotectionpolicy** nesnesi almak için Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="79665-125">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79665-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79665-126">-ResourceGroupName</span></span>
<span data-ttu-id="79665-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79665-127">Specifies the name of the resource group.</span></span>
<span data-ttu-id="79665-128">Bu parametreyi yalnızca ARM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="79665-128">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79665-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="79665-129">-ServiceName</span></span>
<span data-ttu-id="79665-130">Hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79665-130">Specifies the service name.</span></span>
<span data-ttu-id="79665-131">Bu parametreyi yalnızca ASM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="79665-131">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79665-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="79665-132">-Confirm</span></span>
<span data-ttu-id="79665-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79665-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79665-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79665-134">-WhatIf</span></span>
<span data-ttu-id="79665-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79665-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79665-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79665-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79665-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79665-137">CommonParameters</span></span>
<span data-ttu-id="79665-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79665-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79665-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79665-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79665-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79665-140">INPUTS</span></span>

### <span data-ttu-id="79665-141">Itembase</span><span class="sxs-lookup"><span data-stu-id="79665-141">ItemBase</span></span>
<span data-ttu-id="79665-142">Parametre ' öğe ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="79665-142">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="79665-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79665-143">OUTPUTS</span></span>

### <span data-ttu-id="79665-144">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="79665-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="79665-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79665-145">NOTES</span></span>

## <span data-ttu-id="79665-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79665-146">RELATED LINKS</span></span>

[<span data-ttu-id="79665-147">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="79665-147">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="79665-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="79665-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


