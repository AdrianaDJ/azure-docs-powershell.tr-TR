---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: c3a146b99119ab94bf98176d202cda52e1dc5704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591711"
---
# <span data-ttu-id="efc78-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="efc78-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="efc78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efc78-102">SYNOPSIS</span></span>
<span data-ttu-id="efc78-103">Sanal makinede Azure SQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="efc78-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efc78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efc78-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="efc78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="efc78-105">DESCRIPTION</span></span>
<span data-ttu-id="efc78-106">**Set-AzureRmVMSqlServerExtension** cmdlet 'i, bir sanal makinede AzureSQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="efc78-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="efc78-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efc78-107">EXAMPLES</span></span>

### <span data-ttu-id="efc78-108">Örnek 1: sanal makinede otomatik düzeltme eki ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="efc78-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="efc78-109">İlk komut, **New-AzureVMSqlServerAutoPatchingConfig** cmdlet 'ini kullanarak bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="efc78-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="efc78-110">Komut, yapılandırmayı $AutoPatchingConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="efc78-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="efc78-111">İkinci komut, Get-AzureRmVM cmdlet 'ini kullanarak Service02 adındaki hizmette VirtualMachine11 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="efc78-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="efc78-112">Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="efc78-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="efc78-113">Geçerli cmdlet, sanal makinenin $AutoPatchingConfig otomatik düzeltme eki ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="efc78-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="efc78-114">Komut, sanal makineyi Update-AzureRmVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="efc78-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="efc78-115">Örnek 2: sanal makinede otomatik yedekleme ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="efc78-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="efc78-116">İlk komut, **New-AzureVMSqlServerAutoBackupConfig** cmdlet 'ini kullanarak bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="efc78-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="efc78-117">Komut, yapılandırmayı $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="efc78-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="efc78-118">İkinci komut, Service02 adındaki hizmette VirtualMachine11 adındaki sanal makineyi alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="efc78-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="efc78-119">Geçerli cmdlet, sanal makine için $AutoBackupConfig otomatik yedekleme ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="efc78-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="efc78-120">Komut, sanal makineyi Update-AzureRmVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="efc78-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="efc78-121">Örnek 3: sanal makinede SQL Server uzantısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="efc78-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="efc78-122">Bu komut, VirtualMachine08 adındaki bir sanal makineyi Service03 üzerinde alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="efc78-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="efc78-123">Komut, bu sanal makinede SQL Server sanal makine uzantısını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="efc78-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="efc78-124">Örnek 4: belirli bir sanal makinede SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="efc78-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="efc78-125">Bu komut, VirtualMachine08 adındaki bir sanal makineyi Service03 üzerinde alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="efc78-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="efc78-126">Bu komut, bu sanal makinede SQL Server sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="efc78-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="efc78-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efc78-127">PARAMETERS</span></span>

### <span data-ttu-id="efc78-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="efc78-128">-AutoBackupSettings</span></span>
<span data-ttu-id="efc78-129">Otomatik SQL Server Yedekleme ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efc78-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="efc78-130">**Autobackupsettings** nesnesi oluşturmak için New-AzureVMSqlServerAutoBackupConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="efc78-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc78-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="efc78-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="efc78-132">Otomatik SQL Server düzeltme eki ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efc78-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="efc78-133">**Autopatchingsettings** nesnesi oluşturmak için New-AzureVMSqlServerAutoPatchingConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="efc78-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc78-134">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="efc78-134">-KeyVaultCredentialSettings</span></span>
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc78-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="efc78-135">-Location</span></span>
<span data-ttu-id="efc78-136">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="efc78-136">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc78-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="efc78-137">-Name</span></span>
<span data-ttu-id="efc78-138">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efc78-138">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc78-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc78-139">-ResourceGroupName</span></span>
<span data-ttu-id="efc78-140">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efc78-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc78-141">-Version</span><span class="sxs-lookup"><span data-stu-id="efc78-141">-Version</span></span>
<span data-ttu-id="efc78-142">SQL Server uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="efc78-142">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc78-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="efc78-143">-VMName</span></span>
<span data-ttu-id="efc78-144">Bu cmdlet 'in SQL Server uzantısını ayarladığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efc78-144">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc78-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc78-145">CommonParameters</span></span>
<span data-ttu-id="efc78-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efc78-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc78-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc78-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc78-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efc78-148">INPUTS</span></span>

### <span data-ttu-id="efc78-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="efc78-149">None</span></span>
<span data-ttu-id="efc78-150">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="efc78-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efc78-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efc78-151">OUTPUTS</span></span>

## <span data-ttu-id="efc78-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efc78-152">NOTES</span></span>

## <span data-ttu-id="efc78-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efc78-153">RELATED LINKS</span></span>

[<span data-ttu-id="efc78-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="efc78-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="efc78-155">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="efc78-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="efc78-156">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="efc78-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="efc78-157">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="efc78-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="efc78-158">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="efc78-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="efc78-159">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="efc78-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


