---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 4093e236f84d7587586ba30c8bd4653c4ba7358f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936820"
---
# <span data-ttu-id="61c5d-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="61c5d-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="61c5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="61c5d-103">Sanal makinede Azure SQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61c5d-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="61c5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61c5d-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61c5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="61c5d-106">**Set-AzVMSqlServerExtension** cmdlet 'i, bir sanal makinede AzureSQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61c5d-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="61c5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61c5d-107">EXAMPLES</span></span>

### <span data-ttu-id="61c5d-108">Örnek 1: sanal makinede otomatik düzeltme eki ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="61c5d-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="61c5d-109">İlk komut, **New-AzureVMSqlServerAutoPatchingConfig** cmdlet 'ini kullanarak bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61c5d-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="61c5d-110">Komut, yapılandırmayı $AutoPatchingConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61c5d-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="61c5d-111">İkinci komut, Get-AzVM cmdlet 'ini kullanarak Service02 adındaki hizmette VirtualMachine11 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="61c5d-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="61c5d-112">Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="61c5d-113">Geçerli cmdlet, sanal makinenin $AutoPatchingConfig otomatik düzeltme eki ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61c5d-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="61c5d-114">Komut, sanal makineyi Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="61c5d-115">Örnek 2: sanal makinede otomatik yedekleme ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="61c5d-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="61c5d-116">İlk komut, **New-AzureVMSqlServerAutoBackupConfig** cmdlet 'ini kullanarak bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61c5d-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="61c5d-117">Komut, yapılandırmayı $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61c5d-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="61c5d-118">İkinci komut, Service02 adındaki hizmette VirtualMachine11 adındaki sanal makineyi alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="61c5d-119">Geçerli cmdlet, sanal makine için $AutoBackupConfig otomatik yedekleme ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61c5d-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="61c5d-120">Komut, sanal makineyi Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="61c5d-121">Örnek 3: sanal makinede SQL Server uzantısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="61c5d-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="61c5d-122">Bu komut, VirtualMachine08 adındaki bir sanal makineyi Service03 üzerinde alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="61c5d-123">Komut, bu sanal makinede SQL Server sanal makine uzantısını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="61c5d-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="61c5d-124">Örnek 4: belirli bir sanal makinede SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="61c5d-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="61c5d-125">Bu komut, VirtualMachine08 adındaki bir sanal makineyi Service03 üzerinde alır ve geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="61c5d-126">Bu komut, bu sanal makinede SQL Server sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61c5d-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="61c5d-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61c5d-127">PARAMETERS</span></span>

### <span data-ttu-id="61c5d-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="61c5d-128">-AutoBackupSettings</span></span>
<span data-ttu-id="61c5d-129">Otomatik SQL Server Yedekleme ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="61c5d-130">**Autobackupsettings** nesnesi oluşturmak için New-AzureVMSqlServerAutoBackupConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="61c5d-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="61c5d-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="61c5d-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="61c5d-132">Otomatik SQL Server düzeltme eki ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="61c5d-133">**Autopatchingsettings** nesnesi oluşturmak için New-AzureVMSqlServerAutoPatchingConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="61c5d-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="61c5d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c5d-134">-DefaultProfile</span></span>
<span data-ttu-id="61c5d-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61c5d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61c5d-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="61c5d-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="61c5d-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="61c5d-137">-Location</span></span>
<span data-ttu-id="61c5d-138">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="61c5d-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="61c5d-139">-Name</span></span>
<span data-ttu-id="61c5d-140">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="61c5d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c5d-141">-ResourceGroupName</span></span>
<span data-ttu-id="61c5d-142">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="61c5d-143">-Version</span><span class="sxs-lookup"><span data-stu-id="61c5d-143">-Version</span></span>
<span data-ttu-id="61c5d-144">SQL Server uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="61c5d-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="61c5d-145">-VMName</span></span>
<span data-ttu-id="61c5d-146">Bu cmdlet 'in SQL Server uzantısını ayarladığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c5d-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="61c5d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c5d-147">CommonParameters</span></span>
<span data-ttu-id="61c5d-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61c5d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c5d-149">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c5d-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c5d-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61c5d-150">INPUTS</span></span>

### <span data-ttu-id="61c5d-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="61c5d-151">None</span></span>
<span data-ttu-id="61c5d-152">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="61c5d-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61c5d-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61c5d-153">OUTPUTS</span></span>

### <span data-ttu-id="61c5d-154">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="61c5d-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="61c5d-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61c5d-155">NOTES</span></span>

## <span data-ttu-id="61c5d-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61c5d-156">RELATED LINKS</span></span>

[<span data-ttu-id="61c5d-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="61c5d-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="61c5d-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="61c5d-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="61c5d-159">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="61c5d-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="61c5d-160">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="61c5d-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="61c5d-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="61c5d-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="61c5d-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="61c5d-162">Update-AzVM</span></span>](./Update-AzVM.md)


