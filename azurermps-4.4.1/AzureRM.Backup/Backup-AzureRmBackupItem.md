---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588011"
---
# <span data-ttu-id="2e4ef-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="2e4ef-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="2e4ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e4ef-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4ef-103">Yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e4ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e4ef-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e4ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e4ef-105">DESCRIPTION</span></span>
<span data-ttu-id="2e4ef-106">**Backup-Azurermbackupıtem** cmdlet 'i, yedekleme zamanlamasına bağlı olmayan korumalı bir Azure yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="2e4ef-107">Zamanlanmış bir yedekleme başarısız olduktan sonra, korumayı etkinleştirdikten veya yedekleme başlattıktan sonra bir ilk yedekleme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="2e4ef-108">Var olan bir yedekleme işi çalışıyorsa, bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="2e4ef-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e4ef-109">EXAMPLES</span></span>

### <span data-ttu-id="2e4ef-110">Örnek 1: sanal makineyi Yedeklemeyi başlatma</span><span class="sxs-lookup"><span data-stu-id="2e4ef-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="2e4ef-111">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="2e4ef-112">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="2e4ef-113">İkinci komut, Get-AzureRmBackupContainer cmdlet 'ini kullanarak $Vault belirtilen ada sahip bir kapsayıcı alır.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="2e4ef-114">Komut bu nesneyi $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="2e4ef-115">Son komut, Get-AzureRmBackupItem cmdlet 'ini kullanarak $Container yedekleme öğelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="2e4ef-116">Komut, ardışık düzen işlecini kullanarak öğeleri geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2e4ef-117">Geçerli cmdlet, kapsayıcıdaki sanal makineyi yedeklemeye başlar.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="2e4ef-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e4ef-118">PARAMETERS</span></span>

### <span data-ttu-id="2e4ef-119">-Öğe</span><span class="sxs-lookup"><span data-stu-id="2e4ef-119">-Item</span></span>
<span data-ttu-id="2e4ef-120">Bu cmdlet 'in yedekleme işlemini başlattığı yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="2e4ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4ef-121">-DefaultProfile</span></span>
<span data-ttu-id="2e4ef-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e4ef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4ef-123">CommonParameters</span></span>
<span data-ttu-id="2e4ef-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e4ef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4ef-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e4ef-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4ef-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e4ef-126">INPUTS</span></span>

### <span data-ttu-id="2e4ef-127">Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="2e4ef-127">AzureRMBackupItem</span></span>

## <span data-ttu-id="2e4ef-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e4ef-128">OUTPUTS</span></span>

### <span data-ttu-id="2e4ef-129">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="2e4ef-129">AzureRmBackupJob</span></span>

## <span data-ttu-id="2e4ef-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e4ef-130">NOTES</span></span>

## <span data-ttu-id="2e4ef-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e4ef-131">RELATED LINKS</span></span>

[<span data-ttu-id="2e4ef-132">Get-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="2e4ef-132">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="2e4ef-133">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="2e4ef-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="2e4ef-134">Restore-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="2e4ef-134">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


