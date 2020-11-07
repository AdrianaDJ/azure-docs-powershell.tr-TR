---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd5f27a942a33082b9488f74cac2779107f7371f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934502"
---
# <span data-ttu-id="b4a10-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4a10-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="b4a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a10-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a10-103">Belirtilen konumda yedekleme yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b4a10-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="b4a10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4a10-104">SYNTAX</span></span>

### <span data-ttu-id="b4a10-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4a10-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a10-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4a10-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4a10-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b4a10-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4a10-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4a10-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a10-109">Belirtilen konumda yedekleme yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b4a10-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="b4a10-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4a10-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a10-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="b4a10-111">EXAMPLE 1</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath
```

<span data-ttu-id="b4a10-112">Azure yığın yedekleme yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b4a10-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="b4a10-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4a10-113">PARAMETERS</span></span>

### <span data-ttu-id="b4a10-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b4a10-114">-AsJob</span></span>
<span data-ttu-id="b4a10-115">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="b4a10-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="b4a10-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="b4a10-117">Zamanlayıcı 'nın yedekleme yapacağı sıklık için saat cinsinden Aralık.</span><span class="sxs-lookup"><span data-stu-id="b4a10-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="b4a10-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="b4a10-119">Depolama konumundaki yedekler için gün cinsinden Bekletme dönemi.</span><span class="sxs-lookup"><span data-stu-id="b4a10-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-120">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="b4a10-120">-EncryptionCertPath</span></span>
<span data-ttu-id="b4a10-121">Ortak anahtarı (. cer) içeren şifreleme sertifikası dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="b4a10-121">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4a10-122">-InputObject</span></span>
<span data-ttu-id="b4a10-123">Get-AzsBackupConfiguration tarafından döndürülen yedekleme konumu yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="b4a10-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="b4a10-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="b4a10-125">Yedekleme çizelgeleyicinin etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="b4a10-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="b4a10-126">-Location</span></span>
<span data-ttu-id="b4a10-127">Yapılandırılacak konum.</span><span class="sxs-lookup"><span data-stu-id="b4a10-127">Location to configure.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-128">-Parola</span><span class="sxs-lookup"><span data-stu-id="b4a10-128">-Password</span></span>
<span data-ttu-id="b4a10-129">Yedekleme konumuna erişmek için parola gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b4a10-129">Password required to access backup location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="b4a10-130">-Path</span></span>
<span data-ttu-id="b4a10-131">Yedeklemelerin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="b4a10-131">Location where backups will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a10-132">-ResourceGroupName</span></span>
<span data-ttu-id="b4a10-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4a10-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4a10-134">-ResourceId</span></span>
<span data-ttu-id="b4a10-135">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b4a10-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-136">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="b4a10-136">-Username</span></span>
<span data-ttu-id="b4a10-137">Yedekleme konumuna erişmek için Kullanıcı adı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b4a10-137">Username required to access backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a10-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4a10-138">-Confirm</span></span>
<span data-ttu-id="b4a10-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4a10-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a10-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a10-140">-WhatIf</span></span>
<span data-ttu-id="b4a10-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4a10-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4a10-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4a10-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4a10-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a10-143">CommonParameters</span></span>
<span data-ttu-id="b4a10-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4a10-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a10-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4a10-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a10-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4a10-146">INPUTS</span></span>

## <span data-ttu-id="b4a10-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4a10-147">OUTPUTS</span></span>

### <span data-ttu-id="b4a10-148">Microsoft. AzureStack. Management. Backup. admin. modeller. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="b4a10-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="b4a10-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4a10-149">NOTES</span></span>

## <span data-ttu-id="b4a10-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4a10-150">RELATED LINKS</span></span>
