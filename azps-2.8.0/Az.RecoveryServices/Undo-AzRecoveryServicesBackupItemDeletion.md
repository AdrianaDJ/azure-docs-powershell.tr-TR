---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 36b93041a2dfa4ba64779b2a92aeee50da53ce44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933434"
---
# <span data-ttu-id="788d8-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="788d8-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="788d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="788d8-102">SYNOPSIS</span></span>
<span data-ttu-id="788d8-103">Yumuşak silinmiş bir öğeyi yeniden doldurma</span><span class="sxs-lookup"><span data-stu-id="788d8-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="788d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="788d8-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="788d8-105">DESCRIPTION</span></span>
<span data-ttu-id="788d8-106">Undo-AzRecoveryServicesBackupItemDeletion cmdlet 'i, yumuşak silinmiş bir öğeyi yeniden doldurma.</span><span class="sxs-lookup"><span data-stu-id="788d8-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="788d8-107">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="788d8-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="788d8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="788d8-108">EXAMPLES</span></span>

### <span data-ttu-id="788d8-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="788d8-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="788d8-110">İlk komut, yedekleme kapsayıcıları dizisini alır ve sonra bunu $Cont dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="788d8-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="788d8-111">İkinci komut ilk kapsayıcı öğeye karşılık gelen yedekleme öğesini alır ve $PI değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="788d8-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="788d8-112">Üçüncü komut, 0 $PI öğenin yedekleme korumasını devre dışı bırakır \[ \] ve öğeyi softdeleted durumuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="788d8-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="788d8-113">Dördüncü komut, sofdeleted durumundaki yeni öğedir.</span><span class="sxs-lookup"><span data-stu-id="788d8-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="788d8-114">Son komut, softdeleted VM 'yi yeniden doldurma.</span><span class="sxs-lookup"><span data-stu-id="788d8-114">The last command rehydrates the softdeleted VM.</span></span>


## <span data-ttu-id="788d8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="788d8-115">PARAMETERS</span></span>

### <span data-ttu-id="788d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788d8-116">-DefaultProfile</span></span>
<span data-ttu-id="788d8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="788d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="788d8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="788d8-118">-Force</span></span>
<span data-ttu-id="788d8-119">Force yedekleme korumasını devre dışı bırakır (onay iletişim kutusu).</span><span class="sxs-lookup"><span data-stu-id="788d8-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="788d8-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="788d8-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="788d8-121">-Öğe</span><span class="sxs-lookup"><span data-stu-id="788d8-121">-Item</span></span>
<span data-ttu-id="788d8-122">Bu cmdlet 'in korumayı devre dışı bırakacağını belirten yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="788d8-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="788d8-123">Azurermrecoveryservicesbackupıtem almak için Get-AzRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="788d8-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="788d8-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="788d8-124">-VaultId</span></span>
<span data-ttu-id="788d8-125">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="788d8-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="788d8-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="788d8-126">-Confirm</span></span>
<span data-ttu-id="788d8-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="788d8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="788d8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788d8-128">-WhatIf</span></span>
<span data-ttu-id="788d8-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="788d8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788d8-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="788d8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="788d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788d8-131">CommonParameters</span></span>
<span data-ttu-id="788d8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="788d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788d8-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="788d8-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788d8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="788d8-134">INPUTS</span></span>

### <span data-ttu-id="788d8-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="788d8-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="788d8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="788d8-136">System.String</span></span>

## <span data-ttu-id="788d8-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="788d8-137">OUTPUTS</span></span>

### <span data-ttu-id="788d8-138">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="788d8-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="788d8-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="788d8-139">NOTES</span></span>

## <span data-ttu-id="788d8-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="788d8-140">RELATED LINKS</span></span>

[<span data-ttu-id="788d8-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="788d8-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="788d8-142">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="788d8-142">Get-AzRecoveryServicesBackupItem</span></span>]()

