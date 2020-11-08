---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108390"
---
# <span data-ttu-id="78a48-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="78a48-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="78a48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a48-102">SYNOPSIS</span></span>
<span data-ttu-id="78a48-103">Sanal makinede Azure SQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="78a48-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="78a48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78a48-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78a48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="78a48-105">DESCRIPTION</span></span>
<span data-ttu-id="78a48-106">**Set-AzVMSqlServerExtension** cmdlet 'i, bir sanal makinede AzureSQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="78a48-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="78a48-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78a48-107">EXAMPLES</span></span>

### <span data-ttu-id="78a48-108">Örnek 1: sanal makinede otomatik düzeltme eki ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="78a48-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="78a48-109">İlk komut, **New-AzVMSqlServerAutoPatchingConfig** cmdlet 'ini kullanarak bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78a48-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="78a48-110">Komut, yapılandırmayı $AutoPatchingConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="78a48-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="78a48-111">İkinci komut, Get-AzVM cmdlet 'ini kullanarak Service02 adındaki hizmette VirtualMachine11 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="78a48-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="78a48-112">Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="78a48-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="78a48-113">Geçerli cmdlet, sanal makinenin $AutoPatchingConfig otomatik düzeltme eki ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="78a48-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="78a48-114">Komut, sanal makineyi Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="78a48-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="78a48-115">Örnek 2: sanal makinede otomatik yedekleme ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="78a48-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="78a48-116">İlk komut, **New-AzVMSqlServerAutoBackupConfig** cmdlet 'ini kullanarak bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78a48-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="78a48-117">Komut, yapılandırmayı $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="78a48-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="78a48-118">İkinci komut, Service02 adındaki hizmette VirtualMachine11 adındaki sanal makineyi alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="78a48-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="78a48-119">Geçerli cmdlet, sanal makine için $AutoBackupConfig otomatik yedekleme ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="78a48-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="78a48-120">Komut, sanal makineyi Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="78a48-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="78a48-121">Örnek 3: sanal makinede SQL Server uzantısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="78a48-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="78a48-122">Bu komut, VirtualMachine08 adındaki bir sanal makineyi Service03 üzerinde alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="78a48-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="78a48-123">Komut, bu sanal makinede SQL Server sanal makine uzantısını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="78a48-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="78a48-124">Örnek 4: belirli bir sanal makinede SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="78a48-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="78a48-125">Bu komut, VirtualMachine08 adındaki bir sanal makineyi Service03 üzerinde alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="78a48-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="78a48-126">Bu komut, bu sanal makinede SQL Server sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="78a48-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="78a48-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78a48-127">PARAMETERS</span></span>

### <span data-ttu-id="78a48-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="78a48-128">-AutoBackupSettings</span></span>
<span data-ttu-id="78a48-129">Otomatik SQL Server Yedekleme ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a48-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="78a48-130">**Autobackupsettings** nesnesi oluşturmak için New-AzVMSqlServerAutoBackupConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="78a48-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="78a48-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="78a48-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="78a48-132">Otomatik SQL Server düzeltme eki ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a48-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="78a48-133">**Autopatchingsettings** nesnesi oluşturmak için New-AzVMSqlServerAutoPatchingConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="78a48-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="78a48-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a48-134">-DefaultProfile</span></span>
<span data-ttu-id="78a48-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78a48-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78a48-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="78a48-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="78a48-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="78a48-137">-Location</span></span>
<span data-ttu-id="78a48-138">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a48-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="78a48-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="78a48-139">-Name</span></span>
<span data-ttu-id="78a48-140">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a48-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="78a48-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a48-141">-ResourceGroupName</span></span>
<span data-ttu-id="78a48-142">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a48-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="78a48-143">-Version</span><span class="sxs-lookup"><span data-stu-id="78a48-143">-Version</span></span>
<span data-ttu-id="78a48-144">SQL Server uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a48-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="78a48-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="78a48-145">-VMName</span></span>
<span data-ttu-id="78a48-146">Bu cmdlet 'in SQL Server uzantısını ayarladığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a48-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="78a48-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a48-147">CommonParameters</span></span>
<span data-ttu-id="78a48-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78a48-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a48-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="78a48-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a48-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78a48-150">INPUTS</span></span>

### <span data-ttu-id="78a48-151">System. String</span><span class="sxs-lookup"><span data-stu-id="78a48-151">System.String</span></span>

### <span data-ttu-id="78a48-152">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="78a48-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="78a48-153">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="78a48-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="78a48-154">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="78a48-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="78a48-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78a48-155">OUTPUTS</span></span>

### <span data-ttu-id="78a48-156">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="78a48-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="78a48-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78a48-157">NOTES</span></span>

## <span data-ttu-id="78a48-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78a48-158">RELATED LINKS</span></span>

[<span data-ttu-id="78a48-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="78a48-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="78a48-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="78a48-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="78a48-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="78a48-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="78a48-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="78a48-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="78a48-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="78a48-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="78a48-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="78a48-164">Update-AzVM</span></span>](./Update-AzVM.md)


