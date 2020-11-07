---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764898"
---
# <span data-ttu-id="edf31-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="edf31-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="edf31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf31-102">SYNOPSIS</span></span>
<span data-ttu-id="edf31-103">SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edf31-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edf31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edf31-104">SYNTAX</span></span>

### <span data-ttu-id="edf31-105">Storageurisurserverautobackup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="edf31-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="edf31-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="edf31-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="edf31-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="edf31-107">DESCRIPTION</span></span>
<span data-ttu-id="edf31-108">**New-AzureVMSqlServerAutoBackupConfig** CMDLET 'ı SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edf31-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="edf31-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edf31-109">EXAMPLES</span></span>

### <span data-ttu-id="edf31-110">Örnek 1: depolama URI 'sini ve hesap anahtarını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="edf31-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="edf31-111">Bu komut, depolama URI 'sini ve hesap anahtarını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edf31-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="edf31-112">Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.</span><span class="sxs-lookup"><span data-stu-id="edf31-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="edf31-113">Komut sonucu $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="edf31-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="edf31-114">Bu yapılandırma öğesini, Set-AzureRmVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="edf31-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="edf31-115">Örnek 2: depolama alanı kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="edf31-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="edf31-116">İlk komut depolama bağlamı oluşturur ve $StorageContext değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="edf31-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="edf31-117">Daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="edf31-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="edf31-118">İkinci komut $StorageContext 'da depolama bağlamını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edf31-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="edf31-119">Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.</span><span class="sxs-lookup"><span data-stu-id="edf31-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="edf31-120">Örnek 3: şifreleme ve parolayla depolama bağlamını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="edf31-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="edf31-121">Bu komut otomatik yedek yapılandırma nesnesi oluşturur ve depolar.</span><span class="sxs-lookup"><span data-stu-id="edf31-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="edf31-122">Komut, önceki örnekte oluşturulan depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf31-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="edf31-123">Komut parola ile şifrelemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="edf31-123">The command enables encryption with password.</span></span>
<span data-ttu-id="edf31-124">Parola daha önce $CertificatePassword değişkeninde güvenli bir dize olarak depolanmıştı.</span><span class="sxs-lookup"><span data-stu-id="edf31-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="edf31-125">Güvenli bir dize oluşturmak için ConvertTo-SecureString cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="edf31-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="edf31-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edf31-126">PARAMETERS</span></span>

### <span data-ttu-id="edf31-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="edf31-127">-Enable</span></span>
<span data-ttu-id="edf31-128">SQL Server sanal makinesinin otomatik yedeklemesinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="edf31-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="edf31-129">Bu parametreyi belirtirseniz, otomatik yedekleme tüm geçerli ve yeni veritabanları için bir yedekleme zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="edf31-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="edf31-130">Bu işlem, yönetilen yedekleme ayarlarınızı bu zamanlamayı izleyecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="edf31-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="edf31-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="edf31-132">Yedeklemenin tutulacağı gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf31-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="edf31-133">-EnableEncryption</span></span>
<span data-ttu-id="edf31-134">Bu cmdlet 'in şifrelemeyi etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf31-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="edf31-135">-CertificatePassword</span></span>
<span data-ttu-id="edf31-136">SQL Server şifreli yedeklemelerini gerçekleştirmek için kullanılan sertifikayı şifrelemek için parola belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf31-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="edf31-137">-StorageUri</span></span>
<span data-ttu-id="edf31-138">BLOB depolama hesabının Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf31-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="edf31-139">-StorageKey</span></span>
<span data-ttu-id="edf31-140">BLOB depolama hesabının depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf31-140">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="edf31-141">-Profile</span></span>
<span data-ttu-id="edf31-142">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf31-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="edf31-143">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="edf31-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-144">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="edf31-144">-InformationAction</span></span>
<span data-ttu-id="edf31-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="edf31-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-146">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="edf31-146">-InformationVariable</span></span>
<span data-ttu-id="edf31-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="edf31-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="edf31-148">-StorageContext</span></span>
<span data-ttu-id="edf31-149">Yedekleri depolamak için kullanılacak depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf31-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="edf31-150">**Azurestoragecontext** nesnesi edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="edf31-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="edf31-151">Varsayılan, SQL Server sanal makinesiyle ilişkili depolama hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="edf31-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="edf31-152">-BackupScheduleType</span></span>
<span data-ttu-id="edf31-153">Yedekleme zamanlama türü, el ile veya otomatik</span><span class="sxs-lookup"><span data-stu-id="edf31-153">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="edf31-154">-BackupSystemDbs</span></span>
<span data-ttu-id="edf31-155">Sistem veritabanlarını yedekleme</span><span class="sxs-lookup"><span data-stu-id="edf31-155">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="edf31-156">-FullBackupFrequency</span></span>
<span data-ttu-id="edf31-157">Günlük veya hafta SQL Server tam yedekleme sıklığı</span><span class="sxs-lookup"><span data-stu-id="edf31-157">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-158">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="edf31-158">-FullBackupStartHour</span></span>
<span data-ttu-id="edf31-159">SQL Server tam yedekleme başlaması gereken günün saati (0-23)</span><span class="sxs-lookup"><span data-stu-id="edf31-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-160">-Fullbackupwindowınhours</span><span class="sxs-lookup"><span data-stu-id="edf31-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="edf31-161">SQL Server tam yedekleme penceresi saat cinsinden</span><span class="sxs-lookup"><span data-stu-id="edf31-161">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="edf31-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="edf31-163">SQL Server günlük yedekleme sıklığı, her 1-60 dakikada bir</span><span class="sxs-lookup"><span data-stu-id="edf31-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf31-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf31-164">CommonParameters</span></span>
<span data-ttu-id="edf31-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edf31-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf31-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edf31-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf31-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edf31-167">INPUTS</span></span>

## <span data-ttu-id="edf31-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edf31-168">OUTPUTS</span></span>

## <span data-ttu-id="edf31-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edf31-169">NOTES</span></span>

## <span data-ttu-id="edf31-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edf31-170">RELATED LINKS</span></span>

[<span data-ttu-id="edf31-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="edf31-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="edf31-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="edf31-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


