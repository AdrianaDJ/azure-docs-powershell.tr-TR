---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 2805ebfd5849306dadb4cf913660c8fac1602d79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591081"
---
# <span data-ttu-id="9df6d-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9df6d-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="9df6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9df6d-102">SYNOPSIS</span></span>
<span data-ttu-id="9df6d-103">Yedeklenmiş öğenin kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="9df6d-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9df6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9df6d-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9df6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9df6d-105">DESCRIPTION</span></span>
<span data-ttu-id="9df6d-106">**Get-AzureRmBackupRecoveryPoint** cmdlet 'i, yedeklenen bir Azure yedekleme öğesi için kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="9df6d-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="9df6d-107">Bir öğe yedeklendikten sonra, yedekleme bir veya daha fazla kurtarma noktasını depolar.</span><span class="sxs-lookup"><span data-stu-id="9df6d-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="9df6d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9df6d-108">EXAMPLES</span></span>

### <span data-ttu-id="9df6d-109">Örnek 1: öğenin kurtarma noktalarını alma</span><span class="sxs-lookup"><span data-stu-id="9df6d-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="9df6d-110">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="9df6d-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="9df6d-111">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9df6d-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9df6d-112">İkinci komut, **Get-AzureRmBackupContainer** cmdlet 'ini kullanarak $Vault kasada belirtilen ada sahip bir kapsayıcı alır.</span><span class="sxs-lookup"><span data-stu-id="9df6d-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="9df6d-113">Komut bu nesneyi $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9df6d-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="9df6d-114">Üçüncü komut, **Get-Azurermbackupıtem** cmdlet 'ini kullanarak $Container kapsayıcısındaki kapsayıcıda alır.</span><span class="sxs-lookup"><span data-stu-id="9df6d-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="9df6d-115">Komut bu nesneyi $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9df6d-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="9df6d-116">Son komutu $BackupItem öğenin kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="9df6d-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="9df6d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9df6d-117">PARAMETERS</span></span>

### <span data-ttu-id="9df6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df6d-118">-DefaultProfile</span></span>
<span data-ttu-id="9df6d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9df6d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df6d-120">-Öğe</span><span class="sxs-lookup"><span data-stu-id="9df6d-120">-Item</span></span>
<span data-ttu-id="9df6d-121">Bu cmdlet 'in kurtarma noktalarını aldığı öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9df6d-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="9df6d-122">**Azurermbackupöğesi** almak için Get-AzureRmBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9df6d-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9df6d-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9df6d-123">-RecoveryPointId</span></span>
<span data-ttu-id="9df6d-124">Bu cmdlet 'in aldığı bir kurtarma noktasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9df6d-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df6d-125">CommonParameters</span></span>
<span data-ttu-id="9df6d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9df6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df6d-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9df6d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df6d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9df6d-128">INPUTS</span></span>

### <span data-ttu-id="9df6d-129">Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="9df6d-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="9df6d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9df6d-130">OUTPUTS</span></span>

### <span data-ttu-id="9df6d-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9df6d-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="9df6d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9df6d-132">NOTES</span></span>

## <span data-ttu-id="9df6d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9df6d-133">RELATED LINKS</span></span>

[<span data-ttu-id="9df6d-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9df6d-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="9df6d-135">Get-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="9df6d-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="9df6d-136">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="9df6d-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


