---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: df865864962a4cbbf5aef86cf5392bf0736f5a3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761302"
---
# <span data-ttu-id="b5b0d-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="b5b0d-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="b5b0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b0d-103">SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="b5b0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5b0d-104">SYNTAX</span></span>

### <span data-ttu-id="b5b0d-105">Storageurisurserverautobackup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5b0d-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b0d-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="b5b0d-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b0d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5b0d-107">DESCRIPTION</span></span>
<span data-ttu-id="b5b0d-108">**New-AzVMSqlServerAutoBackupConfig** CMDLET 'ı SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="b5b0d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5b0d-109">EXAMPLES</span></span>

### <span data-ttu-id="b5b0d-110">Örnek 1: depolama URI 'sini ve hesap anahtarını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5b0d-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="b5b0d-111">Bu komut, depolama URI 'sini ve hesap anahtarını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="b5b0d-112">Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="b5b0d-113">Komut sonucu $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="b5b0d-114">Bu yapılandırma öğesini, Set-AzVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="b5b0d-115">Örnek 2: depolama alanı kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5b0d-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="b5b0d-116">İlk komut depolama bağlamı oluşturur ve $StorageContext değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="b5b0d-117">Daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="b5b0d-118">İkinci komut $StorageContext 'da depolama bağlamını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="b5b0d-119">Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="b5b0d-120">Örnek 3: şifreleme ve parolayla depolama bağlamını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5b0d-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="b5b0d-121">Bu komut otomatik yedek yapılandırma nesnesi oluşturur ve depolar.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="b5b0d-122">Komut, önceki örnekte oluşturulan depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="b5b0d-123">Komut parola ile şifrelemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-123">The command enables encryption with password.</span></span>
<span data-ttu-id="b5b0d-124">Parola daha önce $CertificatePassword değişkeninde güvenli bir dize olarak depolanmıştı.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="b5b0d-125">Güvenli bir dize oluşturmak için ConvertTo-SecureString cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="b5b0d-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5b0d-126">PARAMETERS</span></span>

### <span data-ttu-id="b5b0d-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="b5b0d-127">-BackupScheduleType</span></span>
<span data-ttu-id="b5b0d-128">Yedekleme zamanlama türü, el ile veya otomatik</span><span class="sxs-lookup"><span data-stu-id="b5b0d-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b0d-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="b5b0d-129">-BackupSystemDbs</span></span>
<span data-ttu-id="b5b0d-130">Sistem veritabanlarını yedekleme</span><span class="sxs-lookup"><span data-stu-id="b5b0d-130">Backup system databases</span></span>

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

### <span data-ttu-id="b5b0d-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b5b0d-131">-CertificatePassword</span></span>
<span data-ttu-id="b5b0d-132">SQL Server şifreli yedeklemelerini gerçekleştirmek için kullanılan sertifikayı şifrelemek için parola belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b0d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b0d-133">-DefaultProfile</span></span>
<span data-ttu-id="b5b0d-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5b0d-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="b5b0d-135">-Enable</span></span>
<span data-ttu-id="b5b0d-136">SQL Server sanal makinesinin otomatik yedeklemesinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="b5b0d-137">Bu parametreyi belirtirseniz, otomatik yedekleme tüm geçerli ve yeni veritabanları için bir yedekleme zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="b5b0d-138">Bu işlem, yönetilen yedekleme ayarlarınızı bu zamanlamayı izleyecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b0d-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="b5b0d-139">-EnableEncryption</span></span>
<span data-ttu-id="b5b0d-140">Bu cmdlet 'in şifrelemeyi etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b0d-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="b5b0d-141">-FullBackupFrequency</span></span>
<span data-ttu-id="b5b0d-142">Günlük veya haftalık SQL Server tam yedekleme sıklığı</span><span class="sxs-lookup"><span data-stu-id="b5b0d-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b0d-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="b5b0d-143">-FullBackupStartHour</span></span>
<span data-ttu-id="b5b0d-144">SQL Server tam yedekleme başlaması gereken günün saati (0-23)</span><span class="sxs-lookup"><span data-stu-id="b5b0d-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="b5b0d-145">-Fullbackupwindowınhours</span><span class="sxs-lookup"><span data-stu-id="b5b0d-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="b5b0d-146">SQL Server tam yedekleme penceresi saat cinsinden</span><span class="sxs-lookup"><span data-stu-id="b5b0d-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="b5b0d-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="b5b0d-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="b5b0d-148">SQL Server günlük yedekleme sıklığı, her 1-60 dakikada bir</span><span class="sxs-lookup"><span data-stu-id="b5b0d-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="b5b0d-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b0d-149">-ResourceGroupName</span></span>
<span data-ttu-id="b5b0d-150">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b0d-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="b5b0d-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="b5b0d-152">Yedeklemenin tutulacağı gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b0d-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b5b0d-153">-StorageContext</span></span>
<span data-ttu-id="b5b0d-154">Yedekleri depolamak için kullanılacak depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="b5b0d-155">**Azurestoragecontext** nesnesi edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="b5b0d-156">Varsayılan, SQL Server sanal makinesiyle ilişkili depolama hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b0d-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="b5b0d-157">-StorageKey</span></span>
<span data-ttu-id="b5b0d-158">BLOB depolama hesabının depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="b5b0d-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="b5b0d-159">-StorageUri</span></span>
<span data-ttu-id="b5b0d-160">BLOB depolama hesabının Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="b5b0d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b0d-161">CommonParameters</span></span>
<span data-ttu-id="b5b0d-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5b0d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b0d-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b0d-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b0d-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5b0d-164">INPUTS</span></span>

### <span data-ttu-id="b5b0d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b0d-165">System.String</span></span>

### <span data-ttu-id="b5b0d-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b5b0d-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b5b0d-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b5b0d-167">System.Int32</span></span>

### <span data-ttu-id="b5b0d-168">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="b5b0d-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="b5b0d-169">System. Uri</span><span class="sxs-lookup"><span data-stu-id="b5b0d-169">System.Uri</span></span>

### <span data-ttu-id="b5b0d-170">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b5b0d-170">System.Security.SecureString</span></span>

### <span data-ttu-id="b5b0d-171">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="b5b0d-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b5b0d-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5b0d-172">OUTPUTS</span></span>

### <span data-ttu-id="b5b0d-173">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="b5b0d-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="b5b0d-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5b0d-174">NOTES</span></span>

## <span data-ttu-id="b5b0d-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5b0d-175">RELATED LINKS</span></span>

[<span data-ttu-id="b5b0d-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="b5b0d-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="b5b0d-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b5b0d-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


