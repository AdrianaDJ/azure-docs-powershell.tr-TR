---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c479869cb150633ca926542552fab2aa7dc80b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588002"
---
# <span data-ttu-id="ceaf4-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ceaf4-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="ceaf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceaf4-102">SYNOPSIS</span></span>
<span data-ttu-id="ceaf4-103">Bir öğeyi Azure yedekleme koruma ilkesiyle ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceaf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ceaf4-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceaf4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ceaf4-105">DESCRIPTION</span></span>
<span data-ttu-id="ceaf4-106">**Enable-AzureRmBackupProtection** cmdlet 'i bir öğeyi Azure yedekleme koruma ilkesiyle ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="ceaf4-107">Koruma ilkesini etkinleştirmek için, önce var olan bir yedekleme öğesine ve var olan ilkeye sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="ceaf4-108">Her ikisi de aynı yedek kasaya ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="ceaf4-109">Yedekleme zamanlaması, öğenin ilk kopyasını ve sonraki yedeklemelerin artımlı kopyasını yapar.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="ceaf4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ceaf4-110">EXAMPLES</span></span>

### <span data-ttu-id="ceaf4-111">Örnek 1: Azure sanal makinesinde korumayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ceaf4-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="ceaf4-112">İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ceaf4-113">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ceaf4-114">İkinci komut $Vault içinde kasa için DefaultPolicy adındaki yedekleme koruma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="ceaf4-115">Komut bu nesneyi $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="ceaf4-116">Final komutu, değerleri bir cmdlet 'ten sonrakine geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="ceaf4-117">Get-AzureRmBackupContainer cmdlet 'ini kullanarak bir kapsayıcı alır.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="ceaf4-118">Komut, Get-AzureRmBackupItem cmdlet 'ini kullanarak bu kapsayıcıdaki yedekleme öğesini alır.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="ceaf4-119">Geçerli cmdlet, komutun bu cmdlet 'e geçirdiği öğe için $Policy depolanan ilkenin kullanılmasını olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="ceaf4-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ceaf4-120">PARAMETERS</span></span>

### <span data-ttu-id="ceaf4-121">-Öğe</span><span class="sxs-lookup"><span data-stu-id="ceaf4-121">-Item</span></span>
<span data-ttu-id="ceaf4-122">Bu cmdlet 'in korumayı etkinleştirmesine yönelik yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-122">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="ceaf4-123">**Azurermbackupöğesi** almak için Get-AzureRmBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-123">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-124">-İlke</span><span class="sxs-lookup"><span data-stu-id="ceaf4-124">-Policy</span></span>
<span data-ttu-id="ceaf4-125">Bu cmdlet 'in bir öğeyle ilişkilenirse koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="ceaf4-126">**Azurermbackupprotectionpolicy** nesnesi almak için Get-AzureRmBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-126">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceaf4-127">-DefaultProfile</span></span>
<span data-ttu-id="ceaf4-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceaf4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceaf4-129">CommonParameters</span></span>
<span data-ttu-id="ceaf4-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceaf4-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceaf4-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ceaf4-132">INPUTS</span></span>

### <span data-ttu-id="ceaf4-133">Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ceaf4-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="ceaf4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ceaf4-134">OUTPUTS</span></span>

### <span data-ttu-id="ceaf4-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ceaf4-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="ceaf4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ceaf4-136">NOTES</span></span>

## <span data-ttu-id="ceaf4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ceaf4-137">RELATED LINKS</span></span>

[<span data-ttu-id="ceaf4-138">Backup-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ceaf4-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="ceaf4-139">Get-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ceaf4-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="ceaf4-140">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ceaf4-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


