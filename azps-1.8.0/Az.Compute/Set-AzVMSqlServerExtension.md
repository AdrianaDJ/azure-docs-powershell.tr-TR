---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 25fdd6eaf7271a48e65b871d10d5264d75d3fe23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761223"
---
# <span data-ttu-id="64b1f-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="64b1f-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="64b1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="64b1f-103">Sanal makinede Azure SQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64b1f-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="64b1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64b1f-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64b1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="64b1f-106">**Set-AzVMSqlServerExtension** cmdlet 'i, bir sanal makinede AzureSQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64b1f-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="64b1f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64b1f-107">EXAMPLES</span></span>

### <span data-ttu-id="64b1f-108">Örnek 1: sanal makinede otomatik düzeltme eki ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="64b1f-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="64b1f-109">İlk komut, **New-AzVMSqlServerAutoPatchingConfig** cmdlet 'ini kullanarak bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64b1f-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="64b1f-110">Komut, yapılandırmayı $AutoPatchingConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="64b1f-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="64b1f-111">İkinci komut, Get-AzVM cmdlet 'ini kullanarak Service02 adındaki hizmette VirtualMachine11 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="64b1f-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="64b1f-112">Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="64b1f-113">Geçerli cmdlet, sanal makinenin $AutoPatchingConfig otomatik düzeltme eki ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64b1f-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="64b1f-114">Komut, sanal makineyi Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="64b1f-115">Örnek 2: sanal makinede otomatik yedekleme ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="64b1f-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="64b1f-116">İlk komut, **New-AzVMSqlServerAutoBackupConfig** cmdlet 'ini kullanarak bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64b1f-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="64b1f-117">Komut, yapılandırmayı $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="64b1f-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="64b1f-118">İkinci komut, Service02 adındaki hizmette VirtualMachine11 adındaki sanal makineyi alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="64b1f-119">Geçerli cmdlet, sanal makine için $AutoBackupConfig otomatik yedekleme ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64b1f-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="64b1f-120">Komut, sanal makineyi Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="64b1f-121">Örnek 3: sanal makinede SQL Server uzantısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="64b1f-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="64b1f-122">Bu komut, VirtualMachine08 adındaki bir sanal makineyi Service03 üzerinde alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="64b1f-123">Komut, bu sanal makinede SQL Server sanal makine uzantısını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="64b1f-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="64b1f-124">Örnek 4: belirli bir sanal makinede SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="64b1f-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="64b1f-125">Bu komut, VirtualMachine08 adındaki bir sanal makineyi Service03 üzerinde alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="64b1f-126">Bu komut, bu sanal makinede SQL Server sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="64b1f-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="64b1f-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64b1f-127">PARAMETERS</span></span>

### <span data-ttu-id="64b1f-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="64b1f-128">-AutoBackupSettings</span></span>
<span data-ttu-id="64b1f-129">Otomatik SQL Server Yedekleme ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="64b1f-130">**Autobackupsettings** nesnesi oluşturmak için New-AzVMSqlServerAutoBackupConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64b1f-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b1f-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="64b1f-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="64b1f-132">Otomatik SQL Server düzeltme eki ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="64b1f-133">**Autopatchingsettings** nesnesi oluşturmak için New-AzVMSqlServerAutoPatchingConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64b1f-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b1f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b1f-134">-DefaultProfile</span></span>
<span data-ttu-id="64b1f-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64b1f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64b1f-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="64b1f-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b1f-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="64b1f-137">-Location</span></span>
<span data-ttu-id="64b1f-138">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b1f-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="64b1f-139">-Name</span></span>
<span data-ttu-id="64b1f-140">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-140">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b1f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b1f-141">-ResourceGroupName</span></span>
<span data-ttu-id="64b1f-142">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b1f-143">-Version</span><span class="sxs-lookup"><span data-stu-id="64b1f-143">-Version</span></span>
<span data-ttu-id="64b1f-144">SQL Server uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b1f-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="64b1f-145">-VMName</span></span>
<span data-ttu-id="64b1f-146">Bu cmdlet 'in SQL Server uzantısını ayarladığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64b1f-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b1f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b1f-147">CommonParameters</span></span>
<span data-ttu-id="64b1f-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64b1f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b1f-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b1f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b1f-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64b1f-150">INPUTS</span></span>

### <span data-ttu-id="64b1f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="64b1f-151">System.String</span></span>

### <span data-ttu-id="64b1f-152">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="64b1f-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="64b1f-153">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="64b1f-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="64b1f-154">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="64b1f-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="64b1f-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64b1f-155">OUTPUTS</span></span>

### <span data-ttu-id="64b1f-156">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="64b1f-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="64b1f-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64b1f-157">NOTES</span></span>

## <span data-ttu-id="64b1f-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64b1f-158">RELATED LINKS</span></span>

[<span data-ttu-id="64b1f-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="64b1f-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="64b1f-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="64b1f-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="64b1f-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="64b1f-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="64b1f-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="64b1f-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="64b1f-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="64b1f-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="64b1f-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="64b1f-164">Update-AzVM</span></span>](./Update-AzVM.md)


