---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 4c023de04cb431e18dc027c0ca3563aa6a2410e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933065"
---
# <span data-ttu-id="ece2d-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ece2d-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="ece2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ece2d-102">SYNOPSIS</span></span>
<span data-ttu-id="ece2d-103">Yedekleme korumalı öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ece2d-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="ece2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ece2d-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece2d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ece2d-105">DESCRIPTION</span></span>
<span data-ttu-id="ece2d-106">**Disable-AzRecoveryServicesBackupProtection** cmdlet 'ı Azure yedekleme korumalı bir öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ece2d-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="ece2d-107">Bu cmdlet, bir öğenin olağan zamanlanmış yedeklemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ece2d-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="ece2d-108">Bu cmdlet, yedekleme öğesi için var olan kurtarma noktalarını da silebilir.</span><span class="sxs-lookup"><span data-stu-id="ece2d-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="ece2d-109">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ece2d-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ece2d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ece2d-110">EXAMPLES</span></span>

### <span data-ttu-id="ece2d-111">Örnek 1: yedekleme korumasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="ece2d-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="ece2d-112">İlk komut, yedekleme kapsayıcıları dizisini alır ve sonra bunu $Cont dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="ece2d-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="ece2d-113">İkinci komut ilk kapsayıcı öğeye karşılık gelen yedekleme öğesini alır ve $PI değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ece2d-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="ece2d-114">Son komut $PI 0 ' da öğenin yedekleme korumasını devre dışı \[ bırakır \] , ancak verileri korur.</span><span class="sxs-lookup"><span data-stu-id="ece2d-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="ece2d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ece2d-115">PARAMETERS</span></span>

### <span data-ttu-id="ece2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece2d-116">-DefaultProfile</span></span>
<span data-ttu-id="ece2d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ece2d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece2d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ece2d-118">-Force</span></span>
<span data-ttu-id="ece2d-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ece2d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ece2d-120">-Öğe</span><span class="sxs-lookup"><span data-stu-id="ece2d-120">-Item</span></span>
<span data-ttu-id="ece2d-121">Bu cmdlet 'in korumayı devre dışı bırakacağını belirten yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ece2d-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="ece2d-122">**Azurermrecoveryservicesbackupıtem** almak için Get-AzRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ece2d-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="ece2d-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="ece2d-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="ece2d-124">Bu cmdlet 'in var olan kurtarma noktalarını sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ece2d-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="ece2d-125">Depolanan kurtarma noktalarını daha sonra silmek için, bu cmdlet 'i yeniden çalıştırın ve bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="ece2d-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="ece2d-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ece2d-126">-VaultId</span></span>
<span data-ttu-id="ece2d-127">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ece2d-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ece2d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ece2d-128">-Confirm</span></span>
<span data-ttu-id="ece2d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ece2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece2d-130">-WhatIf</span></span>
<span data-ttu-id="ece2d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ece2d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece2d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ece2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece2d-133">CommonParameters</span></span>
<span data-ttu-id="ece2d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ece2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece2d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece2d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece2d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ece2d-136">INPUTS</span></span>

### <span data-ttu-id="ece2d-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="ece2d-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="ece2d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ece2d-138">System.String</span></span>

## <span data-ttu-id="ece2d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ece2d-139">OUTPUTS</span></span>

### <span data-ttu-id="ece2d-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="ece2d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ece2d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ece2d-141">NOTES</span></span>

## <span data-ttu-id="ece2d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ece2d-142">RELATED LINKS</span></span>

[<span data-ttu-id="ece2d-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ece2d-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="ece2d-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ece2d-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="ece2d-145">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ece2d-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


