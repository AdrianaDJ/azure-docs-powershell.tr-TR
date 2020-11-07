---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 1ff53a29fa26ebe7ac78cac5140a9105b43bb27d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936955"
---
# <span data-ttu-id="a0cd9-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="a0cd9-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="a0cd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cd9-103">SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="a0cd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0cd9-104">SYNTAX</span></span>

### <span data-ttu-id="a0cd9-105">Storageurisurserverautobackup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0cd9-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0cd9-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="a0cd9-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0cd9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0cd9-107">DESCRIPTION</span></span>
<span data-ttu-id="a0cd9-108">**New-AzVMSqlServerAutoBackupConfig** CMDLET 'ı SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="a0cd9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0cd9-109">EXAMPLES</span></span>

### <span data-ttu-id="a0cd9-110">Örnek 1: depolama URI 'sini ve hesap anahtarını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="a0cd9-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="a0cd9-111">Bu komut, depolama URI 'sini ve hesap anahtarını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="a0cd9-112">Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="a0cd9-113">Komut sonucu $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="a0cd9-114">Bu yapılandırma öğesini, Set-AzVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="a0cd9-115">Örnek 2: depolama alanı kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="a0cd9-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="a0cd9-116">İlk komut depolama bağlamı oluşturur ve $StorageContext değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="a0cd9-117">Daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="a0cd9-118">İkinci komut $StorageContext 'da depolama bağlamını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="a0cd9-119">Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="a0cd9-120">Örnek 3: şifreleme ve parolayla depolama bağlamını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="a0cd9-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="a0cd9-121">Bu komut otomatik yedek yapılandırma nesnesi oluşturur ve depolar.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="a0cd9-122">Komut, önceki örnekte oluşturulan depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="a0cd9-123">Komut parola ile şifrelemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-123">The command enables encryption with password.</span></span>
<span data-ttu-id="a0cd9-124">Parola daha önce $CertificatePassword değişkeninde güvenli bir dize olarak depolanmıştı.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="a0cd9-125">Güvenli bir dize oluşturmak için ConvertTo-SecureString cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="a0cd9-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0cd9-126">PARAMETERS</span></span>

### <span data-ttu-id="a0cd9-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="a0cd9-127">-BackupScheduleType</span></span>
<span data-ttu-id="a0cd9-128">Yedekleme zamanlama türü, el ile veya otomatik</span><span class="sxs-lookup"><span data-stu-id="a0cd9-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cd9-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="a0cd9-129">-BackupSystemDbs</span></span>
<span data-ttu-id="a0cd9-130">Sistem veritabanlarını yedekleme</span><span class="sxs-lookup"><span data-stu-id="a0cd9-130">Backup system databases</span></span>

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

### <span data-ttu-id="a0cd9-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a0cd9-131">-CertificatePassword</span></span>
<span data-ttu-id="a0cd9-132">SQL Server şifreli yedeklemelerini gerçekleştirmek için kullanılan sertifikayı şifrelemek için parola belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cd9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cd9-133">-DefaultProfile</span></span>
<span data-ttu-id="a0cd9-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0cd9-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="a0cd9-135">-Enable</span></span>
<span data-ttu-id="a0cd9-136">SQL Server sanal makinesinin otomatik yedeklemesinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="a0cd9-137">Bu parametreyi belirtirseniz, otomatik yedekleme tüm geçerli ve yeni veritabanları için bir yedekleme zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="a0cd9-138">Bu işlem, yönetilen yedekleme ayarlarınızı bu zamanlamayı izleyecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cd9-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="a0cd9-139">-EnableEncryption</span></span>
<span data-ttu-id="a0cd9-140">Bu cmdlet 'in şifrelemeyi etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cd9-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="a0cd9-141">-FullBackupFrequency</span></span>
<span data-ttu-id="a0cd9-142">Günlük veya haftalık SQL Server tam yedekleme sıklığı</span><span class="sxs-lookup"><span data-stu-id="a0cd9-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cd9-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="a0cd9-143">-FullBackupStartHour</span></span>
<span data-ttu-id="a0cd9-144">SQL Server tam yedekleme başlaması gereken günün saati (0-23)</span><span class="sxs-lookup"><span data-stu-id="a0cd9-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="a0cd9-145">-Fullbackupwindowınhours</span><span class="sxs-lookup"><span data-stu-id="a0cd9-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="a0cd9-146">SQL Server tam yedekleme penceresi saat cinsinden</span><span class="sxs-lookup"><span data-stu-id="a0cd9-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="a0cd9-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="a0cd9-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="a0cd9-148">SQL Server günlük yedekleme sıklığı, her 1-60 dakikada bir</span><span class="sxs-lookup"><span data-stu-id="a0cd9-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="a0cd9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0cd9-149">-ResourceGroupName</span></span>
<span data-ttu-id="a0cd9-150">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cd9-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a0cd9-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="a0cd9-152">Yedeklemenin tutulacağı gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cd9-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="a0cd9-153">-StorageContext</span></span>
<span data-ttu-id="a0cd9-154">Yedekleri depolamak için kullanılacak depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="a0cd9-155">**Azurestoragecontext** nesnesi edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="a0cd9-156">Varsayılan, SQL Server sanal makinesiyle ilişkili depolama hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cd9-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="a0cd9-157">-StorageKey</span></span>
<span data-ttu-id="a0cd9-158">BLOB depolama hesabının depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="a0cd9-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="a0cd9-159">-StorageUri</span></span>
<span data-ttu-id="a0cd9-160">BLOB depolama hesabının Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="a0cd9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cd9-161">CommonParameters</span></span>
<span data-ttu-id="a0cd9-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cd9-163">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0cd9-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cd9-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0cd9-164">INPUTS</span></span>

### <span data-ttu-id="a0cd9-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a0cd9-165">None</span></span>
<span data-ttu-id="a0cd9-166">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a0cd9-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0cd9-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0cd9-167">OUTPUTS</span></span>

### <span data-ttu-id="a0cd9-168">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="a0cd9-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="a0cd9-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0cd9-169">NOTES</span></span>

## <span data-ttu-id="a0cd9-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0cd9-170">RELATED LINKS</span></span>

[<span data-ttu-id="a0cd9-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="a0cd9-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="a0cd9-172">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a0cd9-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


