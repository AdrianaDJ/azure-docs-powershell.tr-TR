---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 9dc42a137d3abcd23a64e096117be8d287571ecf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277551"
---
# <span data-ttu-id="fa7fb-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="fa7fb-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="fa7fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7fb-103">Yedekleme korumalı öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="fa7fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa7fb-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa7fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa7fb-105">DESCRIPTION</span></span>
<span data-ttu-id="fa7fb-106">**Disable-AzRecoveryServicesBackupProtection** cmdlet 'ı Azure yedekleme korumalı bir öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="fa7fb-107">Bu cmdlet, bir öğenin olağan zamanlanmış yedeklemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="fa7fb-108">Bu cmdlet, RemoveRecoveryPoints parametresiyle yürütülürse yedekleme öğesi için var olan kurtarma noktalarını silebilir.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="fa7fb-109">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fa7fb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa7fb-110">EXAMPLES</span></span>

### <span data-ttu-id="fa7fb-111">Örnek 1: yedekleme korumasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="fa7fb-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="fa7fb-112">İlk komut, yedekleme kapsayıcıları dizisini alır ve sonra bunu $Cont dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="fa7fb-113">İkinci komut ilk kapsayıcı öğeye karşılık gelen yedekleme öğesini alır ve $PI değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="fa7fb-114">Son komut $PI 0 ' da öğenin yedekleme korumasını devre dışı \[ bırakır \] , ancak verileri korur.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="fa7fb-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fa7fb-115">Example 2</span></span>

<span data-ttu-id="fa7fb-116">Yedekleme korumalı öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="fa7fb-117">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="fa7fb-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="fa7fb-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa7fb-118">PARAMETERS</span></span>

### <span data-ttu-id="fa7fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7fb-119">-DefaultProfile</span></span>
<span data-ttu-id="fa7fb-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa7fb-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fa7fb-121">-Force</span></span>
<span data-ttu-id="fa7fb-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fb-123">-Öğe</span><span class="sxs-lookup"><span data-stu-id="fa7fb-123">-Item</span></span>
<span data-ttu-id="fa7fb-124">Bu cmdlet 'in korumayı devre dışı bırakacağını belirten yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="fa7fb-125">**Azurermrecoveryservicesbackupıtem** almak için Get-AzRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-125">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fb-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="fa7fb-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="fa7fb-127">Bu cmdlet 'in var olan kurtarma noktalarını sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fb-128">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fa7fb-128">-VaultId</span></span>
<span data-ttu-id="fa7fb-129">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fa7fb-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa7fb-130">-Confirm</span></span>
<span data-ttu-id="fa7fb-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa7fb-132">-WhatIf</span></span>
<span data-ttu-id="fa7fb-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa7fb-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7fb-135">CommonParameters</span></span>
<span data-ttu-id="fa7fb-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7fb-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fa7fb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7fb-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa7fb-138">INPUTS</span></span>

### <span data-ttu-id="fa7fb-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="fa7fb-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="fa7fb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fa7fb-140">System.String</span></span>

## <span data-ttu-id="fa7fb-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa7fb-141">OUTPUTS</span></span>

### <span data-ttu-id="fa7fb-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="fa7fb-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="fa7fb-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa7fb-143">NOTES</span></span>

## <span data-ttu-id="fa7fb-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa7fb-144">RELATED LINKS</span></span>

[<span data-ttu-id="fa7fb-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="fa7fb-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="fa7fb-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fa7fb-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="fa7fb-147">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="fa7fb-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


