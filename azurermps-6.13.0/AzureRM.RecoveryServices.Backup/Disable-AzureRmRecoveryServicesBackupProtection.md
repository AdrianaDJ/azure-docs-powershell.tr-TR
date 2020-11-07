---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 07406378df0439171c5be2e7558e8ac33cb32687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762460"
---
# <span data-ttu-id="9cd59-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9cd59-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="9cd59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd59-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd59-103">Yedekleme korumalı öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9cd59-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cd59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cd59-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cd59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cd59-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd59-106">**Disable-AzureRmRecoveryServicesBackupProtection** cmdlet 'ı Azure yedekleme korumalı bir öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9cd59-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="9cd59-107">Bu cmdlet, bir öğenin olağan zamanlanmış yedeklemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="9cd59-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="9cd59-108">Bu cmdlet, yedekleme öğesi için var olan kurtarma noktalarını da silebilir.</span><span class="sxs-lookup"><span data-stu-id="9cd59-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="9cd59-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9cd59-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9cd59-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cd59-110">EXAMPLES</span></span>

### <span data-ttu-id="9cd59-111">Örnek 1: yedekleme korumasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9cd59-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="9cd59-112">İlk komut, yedekleme kapsayıcıları dizisini alır ve sonra bunu $Cont dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="9cd59-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="9cd59-113">İkinci komut ilk kapsayıcı öğeye karşılık gelen yedekleme öğesini alır ve $PI değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9cd59-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="9cd59-114">Son komut $PI 0 ' da öğenin yedekleme korumasını devre dışı \[ bırakır \] , ancak verileri korur.</span><span class="sxs-lookup"><span data-stu-id="9cd59-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="9cd59-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cd59-115">PARAMETERS</span></span>

### <span data-ttu-id="9cd59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd59-116">-DefaultProfile</span></span>
<span data-ttu-id="9cd59-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cd59-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cd59-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9cd59-118">-Force</span></span>
<span data-ttu-id="9cd59-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9cd59-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9cd59-120">-Öğe</span><span class="sxs-lookup"><span data-stu-id="9cd59-120">-Item</span></span>
<span data-ttu-id="9cd59-121">Bu cmdlet 'in korumayı devre dışı bırakacağını belirten yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cd59-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="9cd59-122">**Azurermrecoveryservicesbackupıtem** almak için Get-AzureRmRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9cd59-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="9cd59-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="9cd59-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="9cd59-124">Bu cmdlet 'in var olan kurtarma noktalarını sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cd59-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="9cd59-125">Depolanan kurtarma noktalarını daha sonra silmek için, bu cmdlet 'i yeniden çalıştırın ve bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="9cd59-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="9cd59-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9cd59-126">-VaultId</span></span>
<span data-ttu-id="9cd59-127">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9cd59-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9cd59-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cd59-128">-Confirm</span></span>
<span data-ttu-id="9cd59-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cd59-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cd59-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd59-130">-WhatIf</span></span>
<span data-ttu-id="9cd59-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cd59-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cd59-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cd59-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cd59-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd59-133">CommonParameters</span></span>
<span data-ttu-id="9cd59-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cd59-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd59-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd59-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd59-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cd59-136">INPUTS</span></span>

### <span data-ttu-id="9cd59-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="9cd59-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="9cd59-138">Parametreler: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9cd59-138">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="9cd59-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd59-139">System.String</span></span>
<span data-ttu-id="9cd59-140">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9cd59-140">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="9cd59-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cd59-141">OUTPUTS</span></span>

### <span data-ttu-id="9cd59-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="9cd59-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9cd59-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cd59-143">NOTES</span></span>

## <span data-ttu-id="9cd59-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cd59-144">RELATED LINKS</span></span>

[<span data-ttu-id="9cd59-145">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9cd59-145">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="9cd59-146">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9cd59-146">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="9cd59-147">Get-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="9cd59-147">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

