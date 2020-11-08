---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276845"
---
# <span data-ttu-id="f4a0d-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="f4a0d-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="f4a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a0d-103">Bir yedekleme öğesi silinip, yumuşak silinmiş bir durumda varsa, bu komut öğeyi, verilerin sürekli tutulacağı bir duruma getirir</span><span class="sxs-lookup"><span data-stu-id="f4a0d-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="f4a0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4a0d-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="f4a0d-106">Undo-AzRecoveryServicesBackupItemDeletion cmdlet 'i, yumuşak silinmiş bir öğeyi korumanın durdurulduğu bir duruma döndürür ancak veriler sürekli tutulur.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="f4a0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="f4a0d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4a0d-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="f4a0d-109">İlk komut, yedekleme kapsayıcıları dizisini alır ve sonra bunu $Cont dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="f4a0d-110">İkinci komut ilk kapsayıcı öğeye karşılık gelen yedekleme öğesini alır ve $PI değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="f4a0d-111">Üçüncü komut, 0 $PI öğenin yedekleme korumasını devre dışı bırakır \[ \] ve öğeyi softdeleted durumuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="f4a0d-112">Dördüncü komut, sofdeleted durumundaki öğeyi alır.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="f4a0d-113">Son komut, softdeleted VM 'yi korumanın durdurulduğu bir duruma getirir ancak veriler sürekli tutulur.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="f4a0d-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f4a0d-114">Example 2</span></span>

<span data-ttu-id="f4a0d-115">Yumuşak silinmiş bir öğeyi yeniden doldurma.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="f4a0d-116">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="f4a0d-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="f4a0d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4a0d-117">PARAMETERS</span></span>

### <span data-ttu-id="f4a0d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a0d-118">-DefaultProfile</span></span>
<span data-ttu-id="f4a0d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4a0d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f4a0d-120">-Force</span></span>
<span data-ttu-id="f4a0d-121">Force yedekleme korumasını devre dışı bırakır (onay iletişim kutusu).</span><span class="sxs-lookup"><span data-stu-id="f4a0d-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="f4a0d-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="f4a0d-123">-Öğe</span><span class="sxs-lookup"><span data-stu-id="f4a0d-123">-Item</span></span>
<span data-ttu-id="f4a0d-124">Bu cmdlet 'in silme işlemini geri aldığı yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="f4a0d-125">Azurermrecoveryservicesbackupıtem almak için Get-AzRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="f4a0d-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f4a0d-126">-VaultId</span></span>
<span data-ttu-id="f4a0d-127">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f4a0d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4a0d-128">-Confirm</span></span>
<span data-ttu-id="f4a0d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a0d-130">-WhatIf</span></span>
<span data-ttu-id="f4a0d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a0d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a0d-133">CommonParameters</span></span>
<span data-ttu-id="f4a0d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a0d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a0d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4a0d-136">INPUTS</span></span>

### <span data-ttu-id="f4a0d-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="f4a0d-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="f4a0d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f4a0d-138">System.String</span></span>

## <span data-ttu-id="f4a0d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4a0d-139">OUTPUTS</span></span>

### <span data-ttu-id="f4a0d-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="f4a0d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f4a0d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4a0d-141">NOTES</span></span>

## <span data-ttu-id="f4a0d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4a0d-142">RELATED LINKS</span></span>

[<span data-ttu-id="f4a0d-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f4a0d-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="f4a0d-144">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="f4a0d-144">Get-AzRecoveryServicesBackupItem</span></span>]()

