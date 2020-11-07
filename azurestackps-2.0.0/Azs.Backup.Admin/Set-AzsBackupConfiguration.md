---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937170"
---
# <span data-ttu-id="837b3-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="837b3-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="837b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="837b3-102">SYNOPSIS</span></span>
<span data-ttu-id="837b3-103">Yedekleme konumunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="837b3-103">Update a backup location.</span></span>

## <span data-ttu-id="837b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="837b3-104">SYNTAX</span></span>

### <span data-ttu-id="837b3-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="837b3-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="837b3-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="837b3-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="837b3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="837b3-107">DESCRIPTION</span></span>
<span data-ttu-id="837b3-108">Yedekleme konumunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="837b3-108">Update a backup location.</span></span>

## <span data-ttu-id="837b3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="837b3-109">EXAMPLES</span></span>

### <span data-ttu-id="837b3-110">Örnek 1: Yedekleme yapılandırmasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="837b3-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="837b3-111">Azure yığın yedekleme yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="837b3-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="837b3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="837b3-112">PARAMETERS</span></span>

### <span data-ttu-id="837b3-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="837b3-113">-AsJob</span></span>
<span data-ttu-id="837b3-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="837b3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="837b3-115">-Yedekleme</span><span class="sxs-lookup"><span data-stu-id="837b3-115">-Backup</span></span>
<span data-ttu-id="837b3-116">Yedekleme konumuyla ilgili bilgiler.</span><span class="sxs-lookup"><span data-stu-id="837b3-116">Information about the backup location.</span></span>
<span data-ttu-id="837b3-117">Oluşturmak için, yedekleme özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="837b3-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="837b3-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="837b3-119">Zamanlayıcı 'nın yedekleme yapacağı sıklık için saat cinsinden Aralık.</span><span class="sxs-lookup"><span data-stu-id="837b3-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="837b3-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="837b3-121">Depolama konumundaki geri göndermeler için gün cinsinden Bekletme dönemi.</span><span class="sxs-lookup"><span data-stu-id="837b3-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837b3-122">-DefaultProfile</span></span>
<span data-ttu-id="837b3-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="837b3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="837b3-124">-EncryptionCertPath</span></span>
<span data-ttu-id="837b3-125">Ortak anahtarı (. cer) içeren şifreleme sertifikası dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="837b3-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="837b3-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="837b3-127">Yedekleme Zamanlayıcısı etkinleştirilmişse, doğru.</span><span class="sxs-lookup"><span data-stu-id="837b3-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="837b3-128">-Location</span></span>
<span data-ttu-id="837b3-129">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="837b3-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="837b3-130">-NoWait</span></span>
<span data-ttu-id="837b3-131">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="837b3-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="837b3-132">-Parola</span><span class="sxs-lookup"><span data-stu-id="837b3-132">-Password</span></span>
<span data-ttu-id="837b3-133">Konuma erişim için parola.</span><span class="sxs-lookup"><span data-stu-id="837b3-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="837b3-134">-Path</span></span>
<span data-ttu-id="837b3-135">Güncelleştirme konumunun yolu</span><span class="sxs-lookup"><span data-stu-id="837b3-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837b3-136">-ResourceGroupName</span></span>
<span data-ttu-id="837b3-137">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="837b3-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="837b3-138">-SubscriptionId</span></span>
<span data-ttu-id="837b3-139">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="837b3-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="837b3-140">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="837b3-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="837b3-141">-Tag</span></span>
<span data-ttu-id="837b3-142">Anahtar değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="837b3-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-143">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="837b3-143">-UserName</span></span>
<span data-ttu-id="837b3-144">Konuma erişmek için Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="837b3-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="837b3-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="837b3-145">-Confirm</span></span>
<span data-ttu-id="837b3-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="837b3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837b3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="837b3-147">-WhatIf</span></span>
<span data-ttu-id="837b3-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="837b3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="837b3-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="837b3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837b3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837b3-150">CommonParameters</span></span>
<span data-ttu-id="837b3-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="837b3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837b3-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="837b3-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837b3-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="837b3-153">INPUTS</span></span>

### <span data-ttu-id="837b3-154">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. Api20180901. ıbackuplocation</span><span class="sxs-lookup"><span data-stu-id="837b3-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="837b3-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="837b3-155">OUTPUTS</span></span>

### <span data-ttu-id="837b3-156">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. Api20180901. ıbackuplocation</span><span class="sxs-lookup"><span data-stu-id="837b3-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="837b3-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="837b3-157">NOTES</span></span>

<span data-ttu-id="837b3-158">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="837b3-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="837b3-159">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="837b3-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="837b3-160">Yedekleme <IBackupLocation> : yedekleme konumuyla ilgili bilgiler.</span><span class="sxs-lookup"><span data-stu-id="837b3-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="837b3-161">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="837b3-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="837b3-162">`[Tag <IResourceTags>]`: Anahtar değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="837b3-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="837b3-163">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="837b3-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="837b3-164">`[BackupFrequencyInHours <Int32?>]`: Scheduler 'ın bir yedekleme sürdüğü sıklık için saat cinsinden Aralık.</span><span class="sxs-lookup"><span data-stu-id="837b3-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="837b3-165">`[BackupRetentionPeriodInDays <Int32?>]`: Depolama konumunda geri kalan tutma süresi (gün olarak).</span><span class="sxs-lookup"><span data-stu-id="837b3-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="837b3-166">`[EncryptionCertBase64 <String>]`: Yedekleme şifreleme sertifikasının Base64 RAW verileri.</span><span class="sxs-lookup"><span data-stu-id="837b3-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="837b3-167">`[IsBackupSchedulerEnabled <Boolean?>]`: Yedekleme Zamanlayıcısı etkinleştirilmişse doğru.</span><span class="sxs-lookup"><span data-stu-id="837b3-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="837b3-168">`[Password <String>]`: Konuma erişme parolası.</span><span class="sxs-lookup"><span data-stu-id="837b3-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="837b3-169">`[Path <String>]`: Güncelleştirme konumunun yolu</span><span class="sxs-lookup"><span data-stu-id="837b3-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="837b3-170">`[UserName <String>]`: Konuma erişmek için Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="837b3-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="837b3-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="837b3-171">RELATED LINKS</span></span>

