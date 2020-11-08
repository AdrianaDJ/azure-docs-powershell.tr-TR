---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277922"
---
# <span data-ttu-id="9bed8-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9bed8-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="9bed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bed8-102">SYNOPSIS</span></span>

<span data-ttu-id="9bed8-103">Yedeklenmiş öğenin kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="9bed8-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="9bed8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bed8-104">SYNTAX</span></span>

### <span data-ttu-id="9bed8-105">NoFilterParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9bed8-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bed8-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="9bed8-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bed8-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9bed8-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bed8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bed8-108">DESCRIPTION</span></span>

<span data-ttu-id="9bed8-109">**Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet 'i, yedeklenen bir Azure yedekleme öğesi için kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="9bed8-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="9bed8-110">Bir öğe yedeklendikten sonra, **Azurermrecoveryservicesbackuprecoverypoint** nesnesinin bir veya daha fazla kurtarma noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="9bed8-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="9bed8-111">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9bed8-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="9bed8-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bed8-112">EXAMPLES</span></span>

### <span data-ttu-id="9bed8-113">Örnek 1: öğenin son haftasından kurtarma noktaları alma</span><span class="sxs-lookup"><span data-stu-id="9bed8-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="9bed8-114">İlk komut, vaultName 'i temel alarak kasa nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="9bed8-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="9bed8-115">İkinci komut yedi günden önce tarihini alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9bed8-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="9bed8-116">Üçüncü komut bugünün tarihini alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9bed8-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="9bed8-117">Dördüncü komut AzureVM yedekleme kapsayıcılarını alır ve bunları $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9bed8-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="9bed8-118">Beşinci komut, workloadType 'a dayalı olarak yedek öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9bed8-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="9bed8-119">Son komut, $BackupItem öğenin kurtarma noktaları dizisini alır ve $RP değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9bed8-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="9bed8-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bed8-120">PARAMETERS</span></span>

### <span data-ttu-id="9bed8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bed8-121">-DefaultProfile</span></span>

<span data-ttu-id="9bed8-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bed8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bed8-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9bed8-123">-EndDate</span></span>

<span data-ttu-id="9bed8-124">Tarih aralığının sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bed8-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="9bed8-125">-Öğe</span><span class="sxs-lookup"><span data-stu-id="9bed8-125">-Item</span></span>

<span data-ttu-id="9bed8-126">Bu cmdlet 'in kurtarma noktalarını aldığı öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bed8-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="9bed8-127">**Azurermrecoveryservicesbackupıtem** nesnesi almak için **Get-azrecoveryservicesbackupıtem** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9bed8-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="9bed8-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="9bed8-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="9bed8-129">Şifrelenmiş bir sanal makinenin tuş Kasası anahtarını geri yüklemek için giriş dosyasının indirileceği konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bed8-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="9bed8-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9bed8-130">-RecoveryPointId</span></span>

<span data-ttu-id="9bed8-131">Kurtarma noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bed8-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="9bed8-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9bed8-132">-StartDate</span></span>

<span data-ttu-id="9bed8-133">Tarih aralığının başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bed8-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="9bed8-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9bed8-134">-VaultId</span></span>

<span data-ttu-id="9bed8-135">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9bed8-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9bed8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bed8-136">CommonParameters</span></span>
<span data-ttu-id="9bed8-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bed8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bed8-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9bed8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bed8-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bed8-139">INPUTS</span></span>

### <span data-ttu-id="9bed8-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="9bed8-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="9bed8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9bed8-141">System.String</span></span>

## <span data-ttu-id="9bed8-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bed8-142">OUTPUTS</span></span>

### <span data-ttu-id="9bed8-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="9bed8-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="9bed8-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bed8-144">NOTES</span></span>

## <span data-ttu-id="9bed8-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bed8-145">RELATED LINKS</span></span>

[<span data-ttu-id="9bed8-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9bed8-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="9bed8-147">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="9bed8-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
