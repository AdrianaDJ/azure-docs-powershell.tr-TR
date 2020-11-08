---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107039"
---
# <span data-ttu-id="0f396-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="0f396-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="0f396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f396-102">SYNOPSIS</span></span>
<span data-ttu-id="0f396-103">Yedeği geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="0f396-103">Restore a backup.</span></span>

## <span data-ttu-id="0f396-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f396-104">SYNTAX</span></span>

### <span data-ttu-id="0f396-105">Restoregenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f396-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0f396-106">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="0f396-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0f396-107">Restoreviaıdentity</span><span class="sxs-lookup"><span data-stu-id="0f396-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0f396-108">Restoreviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="0f396-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f396-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f396-109">DESCRIPTION</span></span>
<span data-ttu-id="0f396-110">Yedeği geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="0f396-110">Restore a backup.</span></span>

## <span data-ttu-id="0f396-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f396-111">EXAMPLES</span></span>

### <span data-ttu-id="0f396-112">Örnek 1: yedeği geri yükleme</span><span class="sxs-lookup"><span data-stu-id="0f396-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="0f396-113">Azure yığın yedeklemesinden geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="0f396-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="0f396-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f396-114">PARAMETERS</span></span>

### <span data-ttu-id="0f396-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="0f396-115">-AsJob</span></span>
<span data-ttu-id="0f396-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="0f396-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0f396-117">-Şifre \ parola</span><span class="sxs-lookup"><span data-stu-id="0f396-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="0f396-118">Şifre çözme sertifikasının parolası.</span><span class="sxs-lookup"><span data-stu-id="0f396-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="0f396-119">-DecryptionCertPath</span></span>
<span data-ttu-id="0f396-120">Özel anahtarı (. pfx) içeren şifre çözme sertifikası dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="0f396-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f396-121">-DefaultProfile</span></span>
<span data-ttu-id="0f396-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f396-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f396-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0f396-123">-Force</span></span>
<span data-ttu-id="0f396-124">Onay sorma</span><span class="sxs-lookup"><span data-stu-id="0f396-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="0f396-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f396-125">-InputObject</span></span>
<span data-ttu-id="0f396-126">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f396-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="0f396-127">-Location</span></span>
<span data-ttu-id="0f396-128">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="0f396-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f396-129">-Name</span></span>
<span data-ttu-id="0f396-130">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="0f396-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0f396-131">-NoWait</span></span>
<span data-ttu-id="0f396-132">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="0f396-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0f396-133">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0f396-133">-PassThru</span></span>
<span data-ttu-id="0f396-134">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="0f396-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0f396-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f396-135">-ResourceGroupName</span></span>
<span data-ttu-id="0f396-136">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0f396-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-137">-Restoreoptıon</span><span class="sxs-lookup"><span data-stu-id="0f396-137">-RestoreOption</span></span>
<span data-ttu-id="0f396-138">Geri yükleme seçeneklerinin özellikleri.</span><span class="sxs-lookup"><span data-stu-id="0f396-138">Properties for restore options.</span></span>
<span data-ttu-id="0f396-139">Oluşturmak için, RESTOREOPTıON özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f396-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-140">-RoleName</span><span class="sxs-lookup"><span data-stu-id="0f396-140">-RoleName</span></span>
<span data-ttu-id="0f396-141">Restore için Azure Stack rol adı, tüm altyapı rolü için boş olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="0f396-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0f396-142">-SubscriptionId</span></span>
<span data-ttu-id="0f396-143">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="0f396-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0f396-144">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0f396-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0f396-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f396-145">-Confirm</span></span>
<span data-ttu-id="0f396-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f396-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f396-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f396-147">-WhatIf</span></span>
<span data-ttu-id="0f396-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f396-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f396-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f396-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f396-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f396-150">CommonParameters</span></span>
<span data-ttu-id="0f396-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f396-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f396-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0f396-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f396-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f396-153">INPUTS</span></span>

### <span data-ttu-id="0f396-154">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. ıbackupadminıdentity</span><span class="sxs-lookup"><span data-stu-id="0f396-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="0f396-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f396-155">OUTPUTS</span></span>

### <span data-ttu-id="0f396-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f396-156">System.Boolean</span></span>



## <span data-ttu-id="0f396-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f396-157">NOTES</span></span>

<span data-ttu-id="0f396-158">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f396-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f396-159">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f396-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0f396-160">INPUTOBJECT <IBackupAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0f396-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0f396-161">`[Backup <String>]`: Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="0f396-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="0f396-162">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0f396-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0f396-163">`[Location <String>]`: Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="0f396-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="0f396-164">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0f396-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0f396-165">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="0f396-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0f396-166">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0f396-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="0f396-167">RESTOREOPTıON <IRestoreOptions> : geri yükleme seçeneklerinin özellikleri.</span><span class="sxs-lookup"><span data-stu-id="0f396-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="0f396-168">`[DecryptionCertBase64 <String>]`: Base64 dizesindeki sertifika dosyası RAW verileri.</span><span class="sxs-lookup"><span data-stu-id="0f396-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="0f396-169">Bu, özel anahtarı olan. pfx dosyası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0f396-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="0f396-170">`[DecryptionCertPassword <String>]`: Şifre çözme sertifikasının parolası.</span><span class="sxs-lookup"><span data-stu-id="0f396-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="0f396-171">`[RoleName <String>]`: Restore için Azure Stack rol adı, tüm altyapı rolü için boş olarak ayarlandı</span><span class="sxs-lookup"><span data-stu-id="0f396-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="0f396-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f396-172">RELATED LINKS</span></span>

