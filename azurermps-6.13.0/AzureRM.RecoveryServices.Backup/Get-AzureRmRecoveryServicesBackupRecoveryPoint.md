---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: d9c53d550f64b17a7ee821b43322dd974b7b5676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591300"
---
# <span data-ttu-id="a36fc-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a36fc-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="a36fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a36fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a36fc-103">Yedeklenmiş öğenin kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="a36fc-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a36fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a36fc-104">SYNTAX</span></span>

### <span data-ttu-id="a36fc-105">NoFilterParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a36fc-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a36fc-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="a36fc-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a36fc-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="a36fc-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a36fc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a36fc-108">DESCRIPTION</span></span>
<span data-ttu-id="a36fc-109">**Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet 'i, yedeklenen bir Azure yedekleme öğesi için kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="a36fc-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="a36fc-110">Bir öğe yedeklendikten sonra, **Azurermrecoveryservicesbackuprecoverypoint** nesnesinin bir veya daha fazla kurtarma noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="a36fc-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="a36fc-111">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a36fc-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a36fc-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a36fc-112">EXAMPLES</span></span>

### <span data-ttu-id="a36fc-113">Örnek 1: öğenin son haftasından kurtarma noktaları alma</span><span class="sxs-lookup"><span data-stu-id="a36fc-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="a36fc-114">İlk komut yedi günden önce tarihini alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a36fc-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="a36fc-115">İkinci komut bugünün tarihini alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a36fc-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="a36fc-116">Üçüncü komut AzureVM yedekleme kapsayıcılarını alır ve bunları $Containers değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a36fc-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="a36fc-117">Dördüncü komut V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a36fc-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a36fc-118">Son komut, $BackupItem öğenin kurtarma noktaları dizisini alır ve $RP değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a36fc-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="a36fc-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a36fc-119">PARAMETERS</span></span>

### <span data-ttu-id="a36fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36fc-120">-DefaultProfile</span></span>
<span data-ttu-id="a36fc-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a36fc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a36fc-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a36fc-122">-EndDate</span></span>
<span data-ttu-id="a36fc-123">Tarih aralığının sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a36fc-123">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36fc-124">-Öğe</span><span class="sxs-lookup"><span data-stu-id="a36fc-124">-Item</span></span>
<span data-ttu-id="a36fc-125">Bu cmdlet 'in kurtarma noktalarını aldığı öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a36fc-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="a36fc-126">**Azurermrecoveryservicesbackupıtem** nesnesi almak için Get-AzureRmRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a36fc-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a36fc-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="a36fc-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="a36fc-128">Şifrelenmiş bir sanal makinenin tuş Kasası anahtarını geri yüklemek için giriş dosyasının indirileceği konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a36fc-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36fc-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="a36fc-129">-RecoveryPointId</span></span>
<span data-ttu-id="a36fc-130">Kurtarma noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a36fc-130">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36fc-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a36fc-131">-StartDate</span></span>
<span data-ttu-id="a36fc-132">Tarih aralığının başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a36fc-132">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36fc-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a36fc-133">-VaultId</span></span>
<span data-ttu-id="a36fc-134">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a36fc-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a36fc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36fc-135">CommonParameters</span></span>
<span data-ttu-id="a36fc-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a36fc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36fc-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a36fc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36fc-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a36fc-138">INPUTS</span></span>

### <span data-ttu-id="a36fc-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="a36fc-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="a36fc-140">Parametreler: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a36fc-140">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="a36fc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a36fc-141">System.String</span></span>
<span data-ttu-id="a36fc-142">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a36fc-142">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="a36fc-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a36fc-143">OUTPUTS</span></span>

### <span data-ttu-id="a36fc-144">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a36fc-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="a36fc-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a36fc-145">NOTES</span></span>

## <span data-ttu-id="a36fc-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a36fc-146">RELATED LINKS</span></span>

[<span data-ttu-id="a36fc-147">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a36fc-147">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="a36fc-148">Get-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="a36fc-148">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


