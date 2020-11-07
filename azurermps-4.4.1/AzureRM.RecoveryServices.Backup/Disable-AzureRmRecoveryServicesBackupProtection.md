---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: a9caa2a40a6ae2ee6e29f6f24ff8266b73868fe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763340"
---
# <span data-ttu-id="f37d0-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f37d0-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="f37d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f37d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f37d0-103">Yedekleme korumalı öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f37d0-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f37d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f37d0-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f37d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f37d0-105">DESCRIPTION</span></span>
<span data-ttu-id="f37d0-106">**Disable-AzureRmRecoveryServicesBackupProtection** cmdlet 'ı Azure yedekleme korumalı bir öğenin korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f37d0-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="f37d0-107">Bu cmdlet, bir öğenin olağan zamanlanmış yedeklemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="f37d0-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="f37d0-108">Bu cmdlet, yedekleme öğesi için var olan kurtarma noktalarını da silebilir.</span><span class="sxs-lookup"><span data-stu-id="f37d0-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>

<span data-ttu-id="f37d0-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f37d0-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f37d0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f37d0-110">EXAMPLES</span></span>

### <span data-ttu-id="f37d0-111">Örnek 1: yedekleme korumasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="f37d0-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="f37d0-112">İlk komut, yedekleme kapsayıcıları dizisini alır ve sonra bunu $Cont dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="f37d0-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>

<span data-ttu-id="f37d0-113">İkinci komut ilk kapsayıcı öğeye karşılık gelen yedekleme öğesini alır ve $PI değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f37d0-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>

<span data-ttu-id="f37d0-114">Son komut $PI 0 ' da öğenin yedekleme korumasını devre dışı \[ bırakır \] , ancak verileri korur.</span><span class="sxs-lookup"><span data-stu-id="f37d0-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="f37d0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f37d0-115">PARAMETERS</span></span>

### <span data-ttu-id="f37d0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f37d0-116">-Force</span></span>
<span data-ttu-id="f37d0-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f37d0-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f37d0-118">-Öğe</span><span class="sxs-lookup"><span data-stu-id="f37d0-118">-Item</span></span>
<span data-ttu-id="f37d0-119">Bu cmdlet 'in korumayı devre dışı bırakacağını belirten yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f37d0-119">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="f37d0-120">**Azurermrecoveryservicesbackupıtem** almak için Get-AzureRmRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f37d0-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="f37d0-121">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="f37d0-121">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="f37d0-122">Bu cmdlet 'in var olan kurtarma noktalarını sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f37d0-122">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="f37d0-123">Depolanan kurtarma noktalarını daha sonra silmek için, bu cmdlet 'i yeniden çalıştırın ve bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="f37d0-123">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="f37d0-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="f37d0-124">-Confirm</span></span>
<span data-ttu-id="f37d0-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f37d0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f37d0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f37d0-126">-WhatIf</span></span>
<span data-ttu-id="f37d0-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f37d0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f37d0-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f37d0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f37d0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37d0-129">-DefaultProfile</span></span>
<span data-ttu-id="f37d0-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f37d0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f37d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37d0-131">CommonParameters</span></span>
<span data-ttu-id="f37d0-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f37d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37d0-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f37d0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37d0-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f37d0-134">INPUTS</span></span>

### <span data-ttu-id="f37d0-135">Itembase</span><span class="sxs-lookup"><span data-stu-id="f37d0-135">ItemBase</span></span>
<span data-ttu-id="f37d0-136">Parametre ' öğe ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="f37d0-136">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="f37d0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f37d0-137">OUTPUTS</span></span>

### <span data-ttu-id="f37d0-138">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="f37d0-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f37d0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f37d0-139">NOTES</span></span>

## <span data-ttu-id="f37d0-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f37d0-140">RELATED LINKS</span></span>

[<span data-ttu-id="f37d0-141">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f37d0-141">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="f37d0-142">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f37d0-142">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f37d0-143">Get-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="f37d0-143">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


