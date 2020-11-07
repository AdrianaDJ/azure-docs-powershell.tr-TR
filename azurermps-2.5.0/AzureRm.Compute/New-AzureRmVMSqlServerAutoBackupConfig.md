---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
ms.openlocfilehash: bb00a3e4fc953510d2ec32b7c213d07d6c8801c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939949"
---
# <span data-ttu-id="d4b92-101">New-AzureRmVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="d4b92-101">New-AzureRmVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="d4b92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b92-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b92-103">SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4b92-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4b92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4b92-104">SYNTAX</span></span>

### <span data-ttu-id="d4b92-105">Storageurisurserverautobackup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4b92-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4b92-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="d4b92-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4b92-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4b92-107">DESCRIPTION</span></span>
<span data-ttu-id="d4b92-108">**Yeni-AzureRmVMSqlServerAutoBackupConfig** CMDLET 'ı SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4b92-108">The **New-AzureRmVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="d4b92-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4b92-109">EXAMPLES</span></span>

### <span data-ttu-id="d4b92-110">Örnek 1: depolama URI 'sini ve hesap anahtarını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4b92-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="d4b92-111">Bu komut, depolama URI 'sini ve hesap anahtarını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4b92-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="d4b92-112">Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.</span><span class="sxs-lookup"><span data-stu-id="d4b92-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="d4b92-113">Komut sonucu $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d4b92-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="d4b92-114">Bu yapılandırma öğesini, Set-AzureRmVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b92-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="d4b92-115">Örnek 2: depolama alanı kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4b92-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="d4b92-116">İlk komut depolama bağlamı oluşturur ve $StorageContext değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d4b92-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="d4b92-117">Daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="d4b92-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="d4b92-118">İkinci komut $StorageContext 'da depolama bağlamını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4b92-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="d4b92-119">Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.</span><span class="sxs-lookup"><span data-stu-id="d4b92-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="d4b92-120">Örnek 3: şifreleme ve parolayla depolama bağlamını kullanarak otomatik yedekleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4b92-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="d4b92-121">Bu komut otomatik yedek yapılandırma nesnesi oluşturur ve depolar.</span><span class="sxs-lookup"><span data-stu-id="d4b92-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="d4b92-122">Komut, önceki örnekte oluşturulan depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="d4b92-123">Komut parola ile şifrelemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-123">The command enables encryption with password.</span></span>
<span data-ttu-id="d4b92-124">Parola daha önce $CertificatePassword değişkeninde güvenli bir dize olarak depolanmıştı.</span><span class="sxs-lookup"><span data-stu-id="d4b92-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="d4b92-125">Güvenli bir dize oluşturmak için ConvertTo-SecureString cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4b92-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="d4b92-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4b92-126">PARAMETERS</span></span>

### <span data-ttu-id="d4b92-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="d4b92-127">-BackupScheduleType</span></span>
<span data-ttu-id="d4b92-128">Yedekleme zamanlama türü, el ile veya otomatik</span><span class="sxs-lookup"><span data-stu-id="d4b92-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="d4b92-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="d4b92-129">-BackupSystemDbs</span></span>
<span data-ttu-id="d4b92-130">Sistem veritabanlarını yedekleme</span><span class="sxs-lookup"><span data-stu-id="d4b92-130">Backup system databases</span></span>

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

### <span data-ttu-id="d4b92-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d4b92-131">-CertificatePassword</span></span>
<span data-ttu-id="d4b92-132">SQL Server şifreli yedeklemelerini gerçekleştirmek için kullanılan sertifikayı şifrelemek için parola belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="d4b92-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b92-133">-DefaultProfile</span></span>
<span data-ttu-id="d4b92-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4b92-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4b92-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="d4b92-135">-Enable</span></span>
<span data-ttu-id="d4b92-136">SQL Server sanal makinesinin otomatik yedeklemesinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="d4b92-137">Bu parametreyi belirtirseniz, otomatik yedekleme tüm geçerli ve yeni veritabanları için bir yedekleme zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d4b92-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="d4b92-138">Bu işlem, yönetilen yedekleme ayarlarınızı bu zamanlamayı izleyecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="d4b92-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="d4b92-139">-EnableEncryption</span></span>
<span data-ttu-id="d4b92-140">Bu cmdlet 'in şifrelemeyi etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="d4b92-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="d4b92-141">-FullBackupFrequency</span></span>
<span data-ttu-id="d4b92-142">Günlük veya haftalık SQL Server tam yedekleme sıklığı</span><span class="sxs-lookup"><span data-stu-id="d4b92-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="d4b92-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="d4b92-143">-FullBackupStartHour</span></span>
<span data-ttu-id="d4b92-144">SQL Server tam yedekleme başlaması gereken günün saati (0-23)</span><span class="sxs-lookup"><span data-stu-id="d4b92-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="d4b92-145">-Fullbackupwindowınhours</span><span class="sxs-lookup"><span data-stu-id="d4b92-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="d4b92-146">SQL Server tam yedekleme penceresi saat cinsinden</span><span class="sxs-lookup"><span data-stu-id="d4b92-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="d4b92-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="d4b92-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="d4b92-148">SQL Server günlük yedekleme sıklığı, her 1-60 dakikada bir</span><span class="sxs-lookup"><span data-stu-id="d4b92-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="d4b92-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4b92-149">-ResourceGroupName</span></span>
<span data-ttu-id="d4b92-150">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d4b92-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="d4b92-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="d4b92-152">Yedeklemenin tutulacağı gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="d4b92-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="d4b92-153">-StorageContext</span></span>
<span data-ttu-id="d4b92-154">Yedekleri depolamak için kullanılacak depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="d4b92-155">**Azurestoragecontext** nesnesi edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4b92-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="d4b92-156">Varsayılan, SQL Server sanal makinesiyle ilişkili depolama hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="d4b92-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="d4b92-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="d4b92-157">-StorageKey</span></span>
<span data-ttu-id="d4b92-158">BLOB depolama hesabının depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="d4b92-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d4b92-159">-StorageUri</span></span>
<span data-ttu-id="d4b92-160">BLOB depolama hesabının Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b92-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="d4b92-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b92-161">CommonParameters</span></span>
<span data-ttu-id="d4b92-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4b92-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b92-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b92-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b92-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4b92-164">INPUTS</span></span>

### <span data-ttu-id="d4b92-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d4b92-165">None</span></span>
<span data-ttu-id="d4b92-166">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d4b92-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4b92-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4b92-167">OUTPUTS</span></span>

### <span data-ttu-id="d4b92-168">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="d4b92-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="d4b92-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4b92-169">NOTES</span></span>

## <span data-ttu-id="d4b92-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4b92-170">RELATED LINKS</span></span>



[<span data-ttu-id="d4b92-171">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d4b92-171">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


