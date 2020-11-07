---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9a5d0f0607692217cf4016a1261f23b725d07e68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759692"
---
# <span data-ttu-id="f7821-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f7821-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="f7821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7821-102">SYNOPSIS</span></span>
<span data-ttu-id="f7821-103">Yedeklenmiş öğenin kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="f7821-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="f7821-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7821-104">SYNTAX</span></span>

### <span data-ttu-id="f7821-105">NoFilterParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7821-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7821-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="f7821-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7821-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f7821-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7821-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7821-108">DESCRIPTION</span></span>
<span data-ttu-id="f7821-109">**Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet 'i, yedeklenen bir Azure yedekleme öğesi için kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="f7821-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="f7821-110">Bir öğe yedeklendikten sonra, **Azurermrecoveryservicesbackuprecoverypoint** nesnesinin bir veya daha fazla kurtarma noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="f7821-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="f7821-111">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f7821-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f7821-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7821-112">EXAMPLES</span></span>

### <span data-ttu-id="f7821-113">Örnek 1: öğenin son haftasından kurtarma noktaları alma</span><span class="sxs-lookup"><span data-stu-id="f7821-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="f7821-114">İlk komut yedi günden önce tarihini alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f7821-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f7821-115">İkinci komut bugünün tarihini alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f7821-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f7821-116">Üçüncü komut AzureVM yedekleme kapsayıcılarını alır ve bunları $Containers değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f7821-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="f7821-117">Dördüncü komut V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f7821-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f7821-118">Son komut, $BackupItem öğenin kurtarma noktaları dizisini alır ve $RP değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f7821-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="f7821-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7821-119">PARAMETERS</span></span>

### <span data-ttu-id="f7821-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7821-120">-DefaultProfile</span></span>
<span data-ttu-id="f7821-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7821-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7821-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f7821-122">-EndDate</span></span>
<span data-ttu-id="f7821-123">Tarih aralığının sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7821-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="f7821-124">-Öğe</span><span class="sxs-lookup"><span data-stu-id="f7821-124">-Item</span></span>
<span data-ttu-id="f7821-125">Bu cmdlet 'in kurtarma noktalarını aldığı öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7821-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="f7821-126">**Azurermrecoveryservicesbackupıtem** nesnesi almak için Get-AzRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f7821-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="f7821-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="f7821-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="f7821-128">Şifrelenmiş bir sanal makinenin tuş Kasası anahtarını geri yüklemek için giriş dosyasının indirileceği konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7821-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="f7821-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f7821-129">-RecoveryPointId</span></span>
<span data-ttu-id="f7821-130">Kurtarma noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7821-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="f7821-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="f7821-131">-StartDate</span></span>
<span data-ttu-id="f7821-132">Tarih aralığının başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7821-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="f7821-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f7821-133">-VaultId</span></span>
<span data-ttu-id="f7821-134">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f7821-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f7821-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7821-135">CommonParameters</span></span>
<span data-ttu-id="f7821-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7821-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7821-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7821-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7821-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7821-138">INPUTS</span></span>

### <span data-ttu-id="f7821-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="f7821-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="f7821-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f7821-140">System.String</span></span>

## <span data-ttu-id="f7821-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7821-141">OUTPUTS</span></span>

### <span data-ttu-id="f7821-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f7821-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="f7821-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7821-143">NOTES</span></span>

## <span data-ttu-id="f7821-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7821-144">RELATED LINKS</span></span>

[<span data-ttu-id="f7821-145">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f7821-145">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f7821-146">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="f7821-146">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


