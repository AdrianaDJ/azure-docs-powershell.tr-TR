---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935144"
---
# <span data-ttu-id="eb570-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb570-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="eb570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb570-102">SYNOPSIS</span></span>
<span data-ttu-id="eb570-103">Belirtilen konumda yedekleme yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb570-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="eb570-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb570-104">SYNTAX</span></span>

### <span data-ttu-id="eb570-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eb570-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb570-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="eb570-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb570-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="eb570-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb570-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb570-108">DESCRIPTION</span></span>
<span data-ttu-id="eb570-109">Belirtilen konumda yedekleme yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb570-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="eb570-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb570-110">EXAMPLES</span></span>

### <span data-ttu-id="eb570-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb570-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="eb570-112">Azure yığın yedekleme yapılandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb570-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="eb570-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb570-113">PARAMETERS</span></span>

### <span data-ttu-id="eb570-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="eb570-114">-AsJob</span></span>
<span data-ttu-id="eb570-115">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="eb570-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="eb570-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="eb570-117">Zamanlayıcı 'nın yedekleme yapacağı sıklık için saat cinsinden Aralık.</span><span class="sxs-lookup"><span data-stu-id="eb570-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="eb570-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="eb570-119">Depolama konumundaki yedekler için gün cinsinden Bekletme dönemi.</span><span class="sxs-lookup"><span data-stu-id="eb570-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-120">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="eb570-120">-EncryptionKey</span></span>
<span data-ttu-id="eb570-121">Yedekleri şifrelemede kullanılan şifreleme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="eb570-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb570-122">-InputObject</span></span>
<span data-ttu-id="eb570-123">Get-AzsBackupConfiguration tarafından döndürülen yedekleme konumu yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="eb570-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="eb570-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="eb570-125">Yedekleme çizelgeleyicinin etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="eb570-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="eb570-126">-Location</span></span>
<span data-ttu-id="eb570-127">Yapılandırılacak konum.</span><span class="sxs-lookup"><span data-stu-id="eb570-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-128">-Parola</span><span class="sxs-lookup"><span data-stu-id="eb570-128">-Password</span></span>
<span data-ttu-id="eb570-129">Yedekleme konumuna erişmek için parola gereklidir.</span><span class="sxs-lookup"><span data-stu-id="eb570-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="eb570-130">-Path</span></span>
<span data-ttu-id="eb570-131">Yedeklemelerin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="eb570-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb570-132">-ResourceGroupName</span></span>
<span data-ttu-id="eb570-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="eb570-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eb570-134">-ResourceId</span></span>
<span data-ttu-id="eb570-135">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="eb570-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-136">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="eb570-136">-Username</span></span>
<span data-ttu-id="eb570-137">Yedekleme konumuna erişmek için Kullanıcı adı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="eb570-137">Username required to access backup location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb570-138">-Confirm</span></span>
<span data-ttu-id="eb570-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb570-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb570-140">-WhatIf</span></span>
<span data-ttu-id="eb570-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb570-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb570-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb570-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb570-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb570-143">CommonParameters</span></span>
<span data-ttu-id="eb570-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb570-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb570-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb570-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb570-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb570-146">INPUTS</span></span>

## <span data-ttu-id="eb570-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb570-147">OUTPUTS</span></span>

### <span data-ttu-id="eb570-148">Microsoft. AzureStack. Management. Backup. admin. modeller. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="eb570-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="eb570-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb570-149">NOTES</span></span>

## <span data-ttu-id="eb570-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb570-150">RELATED LINKS</span></span>

