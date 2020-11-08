---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106199"
---
# <span data-ttu-id="e2e0c-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e2e0c-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="e2e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e0c-103">SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="e2e0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2e0c-104">SYNTAX</span></span>

### <span data-ttu-id="e2e0c-105">Storageurisurserverautobackup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2e0c-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2e0c-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="e2e0c-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e2e0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2e0c-107">DESCRIPTION</span></span>
<span data-ttu-id="e2e0c-108">**New-AzureVMSqlServerAutoBackupConfig** CMDLET 'ı SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="e2e0c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2e0c-109">EXAMPLES</span></span>

### <span data-ttu-id="e2e0c-110">Örnek 1: depolama URI 'sini ve hesap anahtarını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="e2e0c-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="e2e0c-111">Bu komut, depolama URL 'sini ve hesap anahtarını belirterek otomatik yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="e2e0c-112">Örnek 2: depolama bağlamını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="e2e0c-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="e2e0c-113">Bu komut, depolama bağlamını belirterek otomatik yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="e2e0c-114">Örnek 3: şifreleme ve parolayla depolama bağlamını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="e2e0c-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="e2e0c-115">Bu komut, depolama bağlamını belirterek ve parola ile şifreleme seçeneğini etkinleştirerek otomatik yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="e2e0c-116">Sertifikaparolası $CertPasswd adlı değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="e2e0c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2e0c-117">PARAMETERS</span></span>

### <span data-ttu-id="e2e0c-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="e2e0c-118">-BackupScheduleType</span></span>
<span data-ttu-id="e2e0c-119">Yedekleme zamanlama türü, el ile veya otomatik</span><span class="sxs-lookup"><span data-stu-id="e2e0c-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="e2e0c-120">-BackupSystemDbs</span></span>
<span data-ttu-id="e2e0c-121">Sistem veritabanlarını yedekleme</span><span class="sxs-lookup"><span data-stu-id="e2e0c-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e2e0c-122">-CertificatePassword</span></span>
<span data-ttu-id="e2e0c-123">SQL Server şifreli yedeklemelerini gerçekleştirmek için kullanılan sertifikayı şifrelemek için parola belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="e2e0c-124">-Enable</span></span>
<span data-ttu-id="e2e0c-125">SQL Server sanal makinesinin otomatik yedeklemesinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="e2e0c-126">Bu parametreyi kullanırsanız, otomatik yedekleme tüm geçerli ve yeni veritabanları için bir yedekleme zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="e2e0c-127">Bu işlem, yönetilen yedekleme ayarlarınızı bu zamanlamayı izleyecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="e2e0c-128">-EnableEncryption</span></span>
<span data-ttu-id="e2e0c-129">Şifrelemenin etkin olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="e2e0c-130">-FullBackupFrequency</span></span>
<span data-ttu-id="e2e0c-131">Günlük veya hafta SQL Server tam yedekleme sıklığı</span><span class="sxs-lookup"><span data-stu-id="e2e0c-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="e2e0c-132">-FullBackupStartHour</span></span>
<span data-ttu-id="e2e0c-133">SQL Server tam yedekleme başlaması gereken günün saati (0-23)</span><span class="sxs-lookup"><span data-stu-id="e2e0c-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-134">-Fullbackupwindowınhours</span><span class="sxs-lookup"><span data-stu-id="e2e0c-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="e2e0c-135">SQL Server tam yedekleme penceresi saat cinsinden</span><span class="sxs-lookup"><span data-stu-id="e2e0c-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-136">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e2e0c-136">-InformationAction</span></span>
<span data-ttu-id="e2e0c-137">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e2e0c-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e2e0c-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2e0c-139">'A</span><span class="sxs-lookup"><span data-stu-id="e2e0c-139">Continue</span></span>
- <span data-ttu-id="e2e0c-140">Manıza</span><span class="sxs-lookup"><span data-stu-id="e2e0c-140">Ignore</span></span>
- <span data-ttu-id="e2e0c-141">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="e2e0c-141">Inquire</span></span>
- <span data-ttu-id="e2e0c-142">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="e2e0c-142">SilentlyContinue</span></span>
- <span data-ttu-id="e2e0c-143">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="e2e0c-143">Stop</span></span>
- <span data-ttu-id="e2e0c-144">Biliriz</span><span class="sxs-lookup"><span data-stu-id="e2e0c-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-145">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="e2e0c-145">-InformationVariable</span></span>
<span data-ttu-id="e2e0c-146">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="e2e0c-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="e2e0c-148">SQL Server günlük yedekleme sıklığı, her 1-60 dakikada bir</span><span class="sxs-lookup"><span data-stu-id="e2e0c-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-149">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2e0c-149">-Profile</span></span>
<span data-ttu-id="e2e0c-150">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2e0c-151">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="e2e0c-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="e2e0c-153">Bekletme süresinin uzunluğunu gün olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-154">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e2e0c-154">-StorageContext</span></span>
<span data-ttu-id="e2e0c-155">Yedekleri depolamak için kullanılacak depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="e2e0c-156">Varsayılan, SQL Server sanal makinesiyle ilişkili depolama hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="e2e0c-157">-StorageKey</span></span>
<span data-ttu-id="e2e0c-158">BLOB depolama hesabının depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="e2e0c-159">-StorageUri</span></span>
<span data-ttu-id="e2e0c-160">BLOB depolama hesabının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e0c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e0c-161">CommonParameters</span></span>
<span data-ttu-id="e2e0c-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2e0c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e0c-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e0c-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e0c-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2e0c-164">INPUTS</span></span>

## <span data-ttu-id="e2e0c-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2e0c-165">OUTPUTS</span></span>

## <span data-ttu-id="e2e0c-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2e0c-166">NOTES</span></span>

## <span data-ttu-id="e2e0c-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2e0c-167">RELATED LINKS</span></span>

[<span data-ttu-id="e2e0c-168">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e2e0c-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


