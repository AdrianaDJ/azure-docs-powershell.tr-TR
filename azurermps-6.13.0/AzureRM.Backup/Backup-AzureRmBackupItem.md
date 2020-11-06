---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/backup-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: e87ab3ec04378dc97e144d2b444ee5398ff4f4f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593324"
---
# <span data-ttu-id="c8c07-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="c8c07-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="c8c07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c07-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c07-103">Yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="c8c07-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8c07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8c07-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8c07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8c07-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c07-106">**Backup-Azurermbackupıtem** cmdlet 'i, yedekleme zamanlamasına bağlı olmayan korumalı bir Azure yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="c8c07-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="c8c07-107">Zamanlanmış bir yedekleme başarısız olduktan sonra, korumayı etkinleştirdikten veya yedekleme başlattıktan sonra bir ilk yedekleme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8c07-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="c8c07-108">Var olan bir yedekleme işi çalışıyorsa, bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="c8c07-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="c8c07-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8c07-109">EXAMPLES</span></span>

### <span data-ttu-id="c8c07-110">Örnek 1: sanal makineyi Yedeklemeyi başlatma</span><span class="sxs-lookup"><span data-stu-id="c8c07-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="c8c07-111">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="c8c07-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="c8c07-112">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c8c07-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="c8c07-113">İkinci komut, Get-AzureRmBackupContainer cmdlet 'ini kullanarak $Vault belirtilen ada sahip bir kapsayıcı alır.</span><span class="sxs-lookup"><span data-stu-id="c8c07-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="c8c07-114">Komut bu nesneyi $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c8c07-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="c8c07-115">Son komut, Get-AzureRmBackupItem cmdlet 'ini kullanarak $Container yedekleme öğelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c8c07-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="c8c07-116">Komut, ardışık düzen işlecini kullanarak öğeleri geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c8c07-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c8c07-117">Geçerli cmdlet, kapsayıcıdaki sanal makineyi yedeklemeye başlar.</span><span class="sxs-lookup"><span data-stu-id="c8c07-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="c8c07-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8c07-118">PARAMETERS</span></span>

### <span data-ttu-id="c8c07-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c07-119">-DefaultProfile</span></span>
<span data-ttu-id="c8c07-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c8c07-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8c07-121">-Öğe</span><span class="sxs-lookup"><span data-stu-id="c8c07-121">-Item</span></span>
<span data-ttu-id="c8c07-122">Bu cmdlet 'in yedekleme işlemini başlattığı yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8c07-122">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c07-123">CommonParameters</span></span>
<span data-ttu-id="c8c07-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8c07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c07-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8c07-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c07-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8c07-126">INPUTS</span></span>

### <span data-ttu-id="c8c07-127">Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="c8c07-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="c8c07-128">Parametreler: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8c07-128">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="c8c07-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8c07-129">OUTPUTS</span></span>

### <span data-ttu-id="c8c07-130">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="c8c07-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="c8c07-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8c07-131">NOTES</span></span>

## <span data-ttu-id="c8c07-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8c07-132">RELATED LINKS</span></span>

[<span data-ttu-id="c8c07-133">Get-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="c8c07-133">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="c8c07-134">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="c8c07-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="c8c07-135">Restore-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="c8c07-135">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


