---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 76238516065dffc7a8a38ee6ad025f67d54b47c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589172"
---
# <span data-ttu-id="00463-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="00463-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="00463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00463-102">SYNOPSIS</span></span>
<span data-ttu-id="00463-103">Belirtilen yedekleme koruma ilkesine sahip bir öğe için yedeklemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="00463-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00463-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00463-104">SYNTAX</span></span>

### <span data-ttu-id="00463-105">AzureVMComputeEnableProtection (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00463-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00463-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="00463-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00463-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="00463-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00463-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="00463-108">DESCRIPTION</span></span>
<span data-ttu-id="00463-109">**Enable-AzureRmRecoveryServicesBackupProtection** cmdlet 'i bir öğedeki Azure yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="00463-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="00463-110">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="00463-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="00463-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00463-111">EXAMPLES</span></span>

### <span data-ttu-id="00463-112">Örnek 1: bir öğe için yedekleme korumasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="00463-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="00463-113">İlk cmdlet varsayılan ilke nesnesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="00463-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="00463-114">İkinci cmdlet $Pol ilkeyi kullanarak V2VM adındaki ARM sanal makinesi için yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="00463-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="00463-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00463-115">PARAMETERS</span></span>

### <span data-ttu-id="00463-116">-Öğe</span><span class="sxs-lookup"><span data-stu-id="00463-116">-Item</span></span>
<span data-ttu-id="00463-117">Bu cmdlet 'in korumayı etkinleştirmesine yönelik yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00463-117">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="00463-118">**Azurermrecoveryservicesbackupıtem** almak için Get-AzureRmRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="00463-118">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="00463-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="00463-119">-Name</span></span>
<span data-ttu-id="00463-120">Yedekleme öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00463-120">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00463-121">-İlke</span><span class="sxs-lookup"><span data-stu-id="00463-121">-Policy</span></span>
<span data-ttu-id="00463-122">Bu cmdlet 'in bir öğeyle ilişkilenirse koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00463-122">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="00463-123">**Azurermrecoveryservicesbackupprotectionpolicy** nesnesi almak için Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="00463-123">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="00463-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00463-124">-ResourceGroupName</span></span>
<span data-ttu-id="00463-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00463-125">Specifies the name of the resource group.</span></span>
<span data-ttu-id="00463-126">Bu parametreyi yalnızca ARM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="00463-126">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="00463-127">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="00463-127">-ServiceName</span></span>
<span data-ttu-id="00463-128">Hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00463-128">Specifies the service name.</span></span>
<span data-ttu-id="00463-129">Bu parametreyi yalnızca ASM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="00463-129">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="00463-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00463-130">-DefaultProfile</span></span>
<span data-ttu-id="00463-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00463-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00463-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00463-132">CommonParameters</span></span>
<span data-ttu-id="00463-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00463-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00463-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00463-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00463-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00463-135">INPUTS</span></span>

### <span data-ttu-id="00463-136">Itembase</span><span class="sxs-lookup"><span data-stu-id="00463-136">ItemBase</span></span>
<span data-ttu-id="00463-137">Parametre ' öğe ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="00463-137">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="00463-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00463-138">OUTPUTS</span></span>

### <span data-ttu-id="00463-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="00463-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="00463-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00463-140">NOTES</span></span>

## <span data-ttu-id="00463-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00463-141">RELATED LINKS</span></span>

[<span data-ttu-id="00463-142">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="00463-142">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="00463-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="00463-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


